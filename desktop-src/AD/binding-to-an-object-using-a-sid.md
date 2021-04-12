---
title: Associazione a un oggetto tramite un SID
description: In Windows Server 2003, è possibile eseguire l'associazione a un oggetto usando l'ID di sicurezza (SID) dell'oggetto e un GUID. Il SID dell'oggetto viene archiviato nell'attributo objectSID. Il binding a un SID non funziona in Windows 2000.
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- Associazione a un oggetto tramite un annuncio SID
- Active Directory, utilizzo di, associazione, associazione a un oggetto tramite un SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad4ecf2d6faa385ab8085730e4f1cb0689e403
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472691"
---
# <a name="binding-to-an-object-using-a-sid"></a>Associazione a un oggetto tramite un SID

In Windows Server 2003, è possibile eseguire l'associazione a un oggetto usando l'ID di sicurezza (SID) dell'oggetto e un GUID. Il SID dell'oggetto viene archiviato nell'attributo **objectSID** . Il binding a un SID non funziona in Windows 2000.

Il provider LDAP per Active Directory Domain Services fornisce un metodo per l'associazione a un oggetto tramite il SID dell'oggetto. Il formato della stringa di associazione è:


```C++
LDAP://servername/<SID=XXXXX>
```



In questo esempio "ServerName" è il nome del server di directory e "XXXXX" è la rappresentazione di stringa del valore esadecimale del SID. "ServerName" è facoltativo. La stringa SID viene specificata in un form in cui ogni carattere della stringa è la rappresentazione esadecimale di ogni byte del SID. Ad esempio, se la matrice è:


```C++
0xAB 0x14 0xE2
```



la stringa di associazione SID è " &lt; SID = AB14E2 &gt; ". La funzione [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) non deve essere usata per convertire la matrice SID in una stringa perché precede ogni carattere byte con una barra rovesciata, che non è un formato di stringa di binding valido.

La stringa SID può inoltre assumere il formato " &lt; SID = S-x-x-xx-xxxxxxxxxx-xxxxxxxxxx-xxxxxxxxx-XXX &gt; ", dove la parte "S-X-x-xx-XXXXXXXXXX-xxxxxxxxxx-xxxxxxxxx-xxx" è uguale alla stringa restituita dalla funzione [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .

Quando si esegue l'associazione utilizzando il SID dell'oggetto, alcuni metodi e proprietà [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) non sono supportati. Le proprietà **IADs** seguenti non sono supportate dagli oggetti ottenuti tramite binding mediante il SID dell'oggetto:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nome**](/windows/desktop/ADSI/iads-property-methods)
-   [**Padre**](/windows/desktop/ADSI/iads-property-methods)

I metodi **IADsContainer** seguenti non sono supportati dagli oggetti ottenuti dall'associazione usando il SID dell'oggetto:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Creare**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Per utilizzare questi metodi e proprietà dopo l'associazione a un oggetto utilizzando il SID oggetto, utilizzare il metodo [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare il nome distinto dell'oggetto e quindi utilizzare il nome distinto per associare nuovamente l'oggetto.

Nell'esempio di codice seguente viene illustrato come convertire un **objectSID** in una stringa associabile.


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



 

 