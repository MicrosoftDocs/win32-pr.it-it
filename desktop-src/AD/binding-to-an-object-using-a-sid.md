---
title: Associazione a un oggetto usando un SID
description: In Windows Server 2003 è possibile eseguire l'associazione a un oggetto usando l'identificatore di sicurezza (SID) dell'oggetto e un GUID. Il SID dell'oggetto viene archiviato nell'attributo objectSID. L'associazione a un SID non funziona Windows 2000.
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- Associazione a un oggetto tramite un SID AD
- Active Directory, uso, associazione, associazione a un oggetto usando un SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11508d82ddc415e304503a7fee67296b8d2fc966262cf054437fe8a4bd5523a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118023763"
---
# <a name="binding-to-an-object-using-a-sid"></a>Associazione a un oggetto usando un SID

In Windows Server 2003 è possibile eseguire l'associazione a un oggetto usando l'identificatore di sicurezza (SID) dell'oggetto e un GUID. Il SID dell'oggetto viene archiviato **nell'attributo objectSID.** L'associazione a un SID non funziona Windows 2000.

Il provider LDAP per Active Directory Domain Services un metodo da associare a un oggetto usando il SID dell'oggetto. Il formato della stringa di associazione è:


```C++
LDAP://servername/<SID=XXXXX>
```



In questo esempio "servername" è il nome del server di directory e "XXXXX" è la rappresentazione di stringa del valore esadecimale del SID. "servername" è facoltativo. La stringa SID viene specificata in un formato in cui ogni carattere nella stringa è la rappresentazione esadecimale di ogni byte del SID. Ad esempio, se la matrice è:


```C++
0xAB 0x14 0xE2
```



la stringa di associazione SID sarà " &lt; SID=AB14E2 &gt; ". La [**funzione ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) non deve essere usata per convertire la matrice SID in una stringa perché precede ogni carattere di byte con una barra rovesciata, che non è un formato di stringa di associazione valido.

La stringa SID può anche assumere il formato " &lt; SID=S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX ", dove la parte &gt; "S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX" corrisponde alla stringa restituita dalla funzione [**ConvertSidToStringSid.**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida)

Quando si esegue l'associazione usando il SID dell'oggetto, alcuni [**metodi**](/windows/desktop/api/iads/nn-iads-iads) e proprietà [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) non sono supportati. Le proprietà **IAD** seguenti non sono supportate dagli oggetti ottenuti tramite l'associazione tramite il SID dell'oggetto:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nome**](/windows/desktop/ADSI/iads-property-methods)
-   [**Padre**](/windows/desktop/ADSI/iads-property-methods)

I metodi **IADsContainer** seguenti non sono supportati dagli oggetti ottenuti tramite l'associazione tramite il SID dell'oggetto:

-   [**Getobject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Crea**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Elimina**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Per usare questi metodi e proprietà dopo l'associazione a un oggetto usando il SID dell'oggetto, usare il metodo [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare il nome distinto dell'oggetto e quindi usare il nome distinto per eseguire nuovamente l'associazione all'oggetto.

Nell'esempio di codice seguente viene illustrato come convertire **un objectSid** in una stringa associabile.


```C++
HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes);

/********

    GetSIDBindStringFromVariant()

    Converts a SID in VARIANT form, such as an objectSid value, and 
    converts it into a bindable string in the form:

    LDAP://<SID=xxxxxxx...>

    The returned string is allocated with AllocADsMem and must be 
    freed by the caller with FreeADsMem.

*********/

LPWSTR GetSIDBindStringFromVariant(VARIANT vSID)
{
    LPWSTR pwszReturn = NULL;

    if(VT_ARRAY & vSID.vt) 
    {
        HRESULT hr;
        LPBYTE pByte;
        DWORD dwBytes = 0;

        hr = VariantArrayToBytes(vSID, &pByte, &dwBytes);
        if(S_OK == hr)
        {
            // Convert the BYTE array into a string of hex 
            // characters.
            CComBSTR sbstrTemp = "LDAP://<SID=";

            for(DWORD i = 0; i < dwBytes; i++)
            {
                WCHAR wszByte[3];

                swprintf_s(wszByte, L"%02x", pByte[i]);
                sbstrTemp += wszByte;
            }

            sbstrTemp += ">";
            pwszReturn = 
               (LPWSTR)AllocADsMem((sbstrTemp.Length() + 1) * 
                sizeof(WCHAR));
            if(pwszReturn)
            {
                wcscpy_s(pwszReturn, sbstrTemp.m_str);
            }

            FreeADsMem(pByte);
        }
    }

    return pwszReturn;
}

/*********

    VariantArrayToBytes()

    This function converts a VARIANT array into an array of BYTES. 
    This function allocates the buffer using AllocADsMem. The 
    caller must free this memory with FreeADsMem when it is no 
    longer required.

**********/

HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes)
{
    if(!(Variant.vt & VT_ARRAY) ||
        !Variant.parray ||
        !ppBytes ||
        !pdwBytes)
    {
        return E_INVALIDARG;
    }

    *ppBytes = NULL;
    *pdwBytes = 0;

    HRESULT hr = E_FAIL;
    SAFEARRAY *pArrayVal = NULL;
    CHAR HUGEP *pArray = NULL;
    
    // Retrieve the safe array.
    pArrayVal = Variant.parray;
    DWORD dwBytes = pArrayVal->rgsabound[0].cElements;
    *ppBytes = (LPBYTE)AllocADsMem(dwBytes);
    if(NULL == *ppBytes) 
    {
        return E_OUTOFMEMORY;
    }

    hr = SafeArrayAccessData(pArrayVal, (void HUGEP * FAR *) &pArray);
    if(SUCCEEDED(hr))
    {
        // Copy the bytes to the safe array.
        CopyMemory(*ppBytes, pArray, dwBytes);
        SafeArrayUnaccessData( pArrayVal );
        *pdwBytes = dwBytes;
    }
    
    return hr;
}
```



 

 