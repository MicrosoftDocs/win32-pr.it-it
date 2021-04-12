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
# <a name="binding-to-an-object-using-a-sid"></a><span data-ttu-id="e9d02-107">Associazione a un oggetto tramite un SID</span><span class="sxs-lookup"><span data-stu-id="e9d02-107">Binding to an Object Using a SID</span></span>

<span data-ttu-id="e9d02-108">In Windows Server 2003, è possibile eseguire l'associazione a un oggetto usando l'ID di sicurezza (SID) dell'oggetto e un GUID.</span><span class="sxs-lookup"><span data-stu-id="e9d02-108">In Windows Server 2003, it is possible to bind to an object using the object Security Identifier (SID) as well as a GUID.</span></span> <span data-ttu-id="e9d02-109">Il SID dell'oggetto viene archiviato nell'attributo **objectSID** .</span><span class="sxs-lookup"><span data-stu-id="e9d02-109">The object SID is stored in the **objectSID** attribute.</span></span> <span data-ttu-id="e9d02-110">Il binding a un SID non funziona in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e9d02-110">Binding to an SID does not work on Windows 2000.</span></span>

<span data-ttu-id="e9d02-111">Il provider LDAP per Active Directory Domain Services fornisce un metodo per l'associazione a un oggetto tramite il SID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9d02-111">The LDAP provider for Active Directory Domain Services provides a method to bind to an object using the object SID.</span></span> <span data-ttu-id="e9d02-112">Il formato della stringa di associazione è:</span><span class="sxs-lookup"><span data-stu-id="e9d02-112">The binding string format is:</span></span>


```C++
LDAP://servername/<SID=XXXXX>
```



<span data-ttu-id="e9d02-113">In questo esempio "ServerName" è il nome del server di directory e "XXXXX" è la rappresentazione di stringa del valore esadecimale del SID.</span><span class="sxs-lookup"><span data-stu-id="e9d02-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the SID.</span></span> <span data-ttu-id="e9d02-114">"ServerName" è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e9d02-114">The "servername" is optional.</span></span> <span data-ttu-id="e9d02-115">La stringa SID viene specificata in un form in cui ogni carattere della stringa è la rappresentazione esadecimale di ogni byte del SID.</span><span class="sxs-lookup"><span data-stu-id="e9d02-115">The SID string is specified in a form where each character in the string is the hexadecimal representation of each byte of the SID.</span></span> <span data-ttu-id="e9d02-116">Ad esempio, se la matrice è:</span><span class="sxs-lookup"><span data-stu-id="e9d02-116">For example, if the array is:</span></span>


```C++
0xAB 0x14 0xE2
```



<span data-ttu-id="e9d02-117">la stringa di associazione SID è " &lt; SID = AB14E2 &gt; ".</span><span class="sxs-lookup"><span data-stu-id="e9d02-117">the SID binding string would be "&lt;SID=AB14E2&gt;".</span></span> <span data-ttu-id="e9d02-118">La funzione [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) non deve essere usata per convertire la matrice SID in una stringa perché precede ogni carattere byte con una barra rovesciata, che non è un formato di stringa di binding valido.</span><span class="sxs-lookup"><span data-stu-id="e9d02-118">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function should not be used to convert the SID array into a string because it precedes each byte character with a backslash, which is not a valid bind string format.</span></span>

<span data-ttu-id="e9d02-119">La stringa SID può inoltre assumere il formato " &lt; SID = S-x-x-xx-xxxxxxxxxx-xxxxxxxxxx-xxxxxxxxx-XXX &gt; ", dove la parte "S-X-x-xx-XXXXXXXXXX-xxxxxxxxxx-xxxxxxxxx-xxx" è uguale alla stringa restituita dalla funzione [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .</span><span class="sxs-lookup"><span data-stu-id="e9d02-119">The SID string can also take the form "&lt;SID=S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX&gt;", where the "S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX" portion is the same as the string returned by the [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) function.</span></span>

<span data-ttu-id="e9d02-120">Quando si esegue l'associazione utilizzando il SID dell'oggetto, alcuni metodi e proprietà [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="e9d02-120">When binding using the object SID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="e9d02-121">Le proprietà **IADs** seguenti non sono supportate dagli oggetti ottenuti tramite binding mediante il SID dell'oggetto:</span><span class="sxs-lookup"><span data-stu-id="e9d02-121">The following **IADs** properties are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="e9d02-122">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="e9d02-122">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="e9d02-123">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e9d02-123">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="e9d02-124">**Padre**</span><span class="sxs-lookup"><span data-stu-id="e9d02-124">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="e9d02-125">I metodi **IADsContainer** seguenti non sono supportati dagli oggetti ottenuti dall'associazione usando il SID dell'oggetto:</span><span class="sxs-lookup"><span data-stu-id="e9d02-125">The following **IADsContainer** methods are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="e9d02-126">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="e9d02-126">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="e9d02-127">**Creare**</span><span class="sxs-lookup"><span data-stu-id="e9d02-127">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="e9d02-128">**Delete**</span><span class="sxs-lookup"><span data-stu-id="e9d02-128">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="e9d02-129">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="e9d02-129">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="e9d02-130">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="e9d02-130">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="e9d02-131">Per utilizzare questi metodi e proprietà dopo l'associazione a un oggetto utilizzando il SID oggetto, utilizzare il metodo [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare il nome distinto dell'oggetto e quindi utilizzare il nome distinto per associare nuovamente l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9d02-131">To use these methods and properties after binding to an object using the object SID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="e9d02-132">Nell'esempio di codice seguente viene illustrato come convertire un **objectSID** in una stringa associabile.</span><span class="sxs-lookup"><span data-stu-id="e9d02-132">The following code example shows how to convert an **objectSid** into a bindable string.</span></span>


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



 

 