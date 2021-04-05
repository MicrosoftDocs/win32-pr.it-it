---
title: Abilitazione dell'account del servizio per l'accesso alle proprietà SCP
description: Nell'esempio di codice seguente viene impostata una coppia di voci di controllo di accesso (ACE) in un oggetto punto di connessione del servizio (SCP).
ms.assetid: 663dcf55-5f0d-49af-8b51-4c1e35b79ef1
ms.tgt_platform: multiple
keywords:
- Abilitazione dell'account del servizio per l'accesso alle proprietà SCP AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49adcd1b4747b1c13a64a5af54c6cc6a42e6afe
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872310"
---
# <a name="enabling-service-account-to-access-scp-properties"></a><span data-ttu-id="fffc6-104">Abilitazione dell'account del servizio per l'accesso alle proprietà SCP</span><span class="sxs-lookup"><span data-stu-id="fffc6-104">Enabling Service Account to Access SCP Properties</span></span>

<span data-ttu-id="fffc6-105">Nell'esempio di codice seguente viene impostata una coppia di voci di controllo di accesso (ACE) in un oggetto punto di connessione del servizio (SCP).</span><span class="sxs-lookup"><span data-stu-id="fffc6-105">The following code example sets a pair of Access Control Entries (ACEs) on a service connection point (SCP) object.</span></span> <span data-ttu-id="fffc6-106">Le voci ACE concedono l'accesso in lettura/scrittura all'account utente o computer con cui verrà eseguita l'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="fffc6-106">The ACEs grant read/write access to the user or computer account under which the service instance will be running.</span></span> <span data-ttu-id="fffc6-107">Il programma di installazione del servizio Usa codice simile al seguente per garantire che il servizio possa aggiornarne le proprietà in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fffc6-107">The service installer uses code similar to the following to ensure that the service can update its properties at run time.</span></span> <span data-ttu-id="fffc6-108">Se gli ACE simili a questi non sono impostati, il servizio non avrà accesso alle proprietà del SCP.</span><span class="sxs-lookup"><span data-stu-id="fffc6-108">If ACEs similar to these these are not set, the service will not have access to the properties of the SCP.</span></span>

<span data-ttu-id="fffc6-109">In genere, un programma di installazione del servizio imposterà le voci ACE dopo la creazione dell'oggetto SCP.</span><span class="sxs-lookup"><span data-stu-id="fffc6-109">Typically, a service installer will set these ACEs after creating the SCP object.</span></span> <span data-ttu-id="fffc6-110">Per altre informazioni e un esempio di codice che crea un SCP e chiama questa funzione, vedere [come i client trovano e usano un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="fffc6-110">For more information, and a code example that creates an SCP and calls this function, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="fffc6-111">Se il servizio viene riconfigurato per l'esecuzione con un account diverso, è necessario aggiornare le voci ACE.</span><span class="sxs-lookup"><span data-stu-id="fffc6-111">If the service is reconfigured to run under a different account, the ACEs must be updated.</span></span> <span data-ttu-id="fffc6-112">Per una corretta esecuzione, questo esempio di codice deve essere eseguito nel contesto di sicurezza di un amministratore di dominio.</span><span class="sxs-lookup"><span data-stu-id="fffc6-112">To run successfully, this code example must be run in the security context of a domain administrator.</span></span>

<span data-ttu-id="fffc6-113">Il primo parametro della funzione di esempio specifica il nome dell'account utente a cui concedere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="fffc6-113">The first parameter of the sample function specifies the name of the user account to be granted access.</span></span> <span data-ttu-id="fffc6-114">La funzione presuppone che il nome sia in formato *dominio ***\\*** nomeutente* .</span><span class="sxs-lookup"><span data-stu-id="fffc6-114">The function assumes the name is in *Domain ***\\*** UserName* format.</span></span> <span data-ttu-id="fffc6-115">Se non viene specificato alcun account, la funzione presuppone che il servizio usi l'account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="fffc6-115">If no account is specified, the function assumes the service uses the LocalSystem account.</span></span> <span data-ttu-id="fffc6-116">Ciò significa che la funzione deve concedere l'accesso all'account computer del server host in cui è in esecuzione il servizio.</span><span class="sxs-lookup"><span data-stu-id="fffc6-116">This means the function must grant access to the computer account of the host server on which the service is running.</span></span> <span data-ttu-id="fffc6-117">A tale scopo, nell'esempio di codice viene chiamata la funzione [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) per ottenere il dominio e il nome utente del computer locale.</span><span class="sxs-lookup"><span data-stu-id="fffc6-117">To do this, the code example calls the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to obtain the domain and user name of the local computer.</span></span>

<span data-ttu-id="fffc6-118">L'esempio di codice seguente può essere modificato per concedere al servizio l'accesso completo all'oggetto SCP, ma la procedura consigliata consiste nel concedere solo i diritti di accesso specifici richiesti dal servizio in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fffc6-118">The following code example can be modified to grant the service full access to the SCP object, but the best practice is to grant only the specific access rights that the service requires at run time.</span></span> <span data-ttu-id="fffc6-119">In questo caso, la funzione concede l'accesso a due proprietà.</span><span class="sxs-lookup"><span data-stu-id="fffc6-119">In this case, the function grants access to two properties.</span></span>



| <span data-ttu-id="fffc6-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fffc6-120">Property</span></span>                                                              | <span data-ttu-id="fffc6-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fffc6-121">Description</span></span>                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="fffc6-122">**serviceDNSName**</span><span class="sxs-lookup"><span data-stu-id="fffc6-122">**serviceDNSName**</span></span>](/windows/desktop/ADSchema/a-servicednsname)                       | <span data-ttu-id="fffc6-123">Nome del server host in cui è in esecuzione il servizio.</span><span class="sxs-lookup"><span data-stu-id="fffc6-123">The name of the host server on which the service is running.</span></span>         |
| [<span data-ttu-id="fffc6-124">**serviceBindingInformation**</span><span class="sxs-lookup"><span data-stu-id="fffc6-124">**serviceBindingInformation**</span></span>](/windows/desktop/ADSchema/a-servicebindinginformation) | <span data-ttu-id="fffc6-125">Informazioni sul binding privato che il servizio Aggiorna all'avvio.</span><span class="sxs-lookup"><span data-stu-id="fffc6-125">Private binding information that the service updates when it starts.</span></span> |



 

<span data-ttu-id="fffc6-126">Ogni proprietà è identificata da **schemaIDGUID** della classe **attributeSchema** della proprietà.</span><span class="sxs-lookup"><span data-stu-id="fffc6-126">Each property is identified by the **schemaIDGUID** of the property's **attributeSchema** class.</span></span> <span data-ttu-id="fffc6-127">Ogni proprietà nello schema ha una propria **schemaIDGUID** univoca.</span><span class="sxs-lookup"><span data-stu-id="fffc6-127">Every property in the schema has its own unique **schemaIDGUID**.</span></span> <span data-ttu-id="fffc6-128">Nell'esempio di codice seguente vengono usate le stringhe per specificare i GUID.</span><span class="sxs-lookup"><span data-stu-id="fffc6-128">The following code example uses strings to specify the GUIDs.</span></span> <span data-ttu-id="fffc6-129">Le stringhe GUID hanno il formato seguente, dove ogni "X" viene sostituito da una cifra esadecimale: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}.</span><span class="sxs-lookup"><span data-stu-id="fffc6-129">The GUID strings have the following format where each "X" is replaced by a hexadecimal digit: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}.</span></span>

<span data-ttu-id="fffc6-130">Vedere le pagine di riferimento dello schema Active Directory per i valori **schemaIDGUID** assegnati alle proprietà per concedere o negare l'accesso a.</span><span class="sxs-lookup"><span data-stu-id="fffc6-130">Refer to the Active Directory Schema reference pages for the **schemaIDGUID** values assigned to the properties to grant or deny access to.</span></span>

<span data-ttu-id="fffc6-131">Nell'esempio di codice seguente vengono utilizzate le interfacce [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) per eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="fffc6-131">The following code example uses the [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) interfaces to perform the following operations.</span></span>

1.  <span data-ttu-id="fffc6-132">Ottenere il descrittore di sicurezza dell'oggetto SCP.</span><span class="sxs-lookup"><span data-stu-id="fffc6-132">Obtain the security descriptor of the SCP object.</span></span>
2.  <span data-ttu-id="fffc6-133">Impostare le voci ACE appropriate nell'elenco di controllo di accesso discrezionale (DACL) del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fffc6-133">Set the appropriate ACEs in the discretionary access control list (DACL) of the security descriptor.</span></span>
3.  <span data-ttu-id="fffc6-134">Modificare il descrittore di sicurezza dell'oggetto SCP.</span><span class="sxs-lookup"><span data-stu-id="fffc6-134">Modify the security descriptor of the SCP object.</span></span>


```C++
#include <atlbase.h>

//******************************
//
//  AllowAccessToScpProperties()
//
//******************************

HRESULT AllowAccessToScpProperties(
    LPWSTR wszAccountSAM,   // Service account to allow access.
    IADs *pSCPObject)       // IADs pointer to the SCP object.
{
    HRESULT hr = E_FAIL;
    IADsAccessControlList *pACL = NULL;
    IADsSecurityDescriptor *pSD = NULL;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE1 = NULL;
    IADsAccessControlEntry *pACE2 = NULL;
    IDispatch *pDispACE = NULL;
    long lFlags = 0L;
    CComBSTR sbstrTrustee;
    CComBSTR sbstrSecurityDescriptor = L"nTSecurityDescriptor";
    VARIANT varSD;

    if(NULL == pSCPObject)
    {
        return E_INVALIDARG;
    }
    
    VariantInit(&varSD);
     
    /*
    If no service account is specified, service runs under 
    LocalSystem. Allow access to the computer account of the 
    service's host.
    */
    if (wszAccountSAM) 
    {
        sbstrTrustee = wszAccountSAM;
    }
    else
    {
        LPWSTR pwszComputerName;
        DWORD dwLen;
        
        // Get the size required for the SAM account name.
        dwLen = 0;
        GetComputerObjectNameW(NameSamCompatible, 
            NULL, &dwLen);
        
        pwszComputerName = new WCHAR[dwLen + 1];
        if(NULL == pwszComputerName)
        {
            hr = E_OUTOFMEMORY;
            goto cleanup;
        }

        /*
        Get the SAM account name of the computer object for 
        the server.
        */
        if(!GetComputerObjectNameW(NameSamCompatible,
            pwszComputerName, &dwLen))
        {
            delete pwszComputerName;
            
            hr = HRESULT_FROM_WIN32(GetLastError());
            goto cleanup;
        }

        sbstrTrustee = pwszComputerName;
        wprintf(L"GetComputerObjectName: %s\n", pwszComputerName);
        delete pwszComputerName;
    } 

    // Get the nTSecurityDescriptor.
    hr = pSCPObject->Get(sbstrSecurityDescriptor, &varSD);
    if (FAILED(hr) || (varSD.vt != VT_DISPATCH)) 
    {
        _tprintf(TEXT("Get nTSecurityDescriptor failed: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    /*
    Use the V_DISPATCH macro to get the IDispatch pointer from 
    VARIANT structure and QueryInterface for an 
    IADsSecurityDescriptor pointer.
    */
    hr = V_DISPATCH( &varSD )->QueryInterface(
        IID_IADsSecurityDescriptor,
        (void**)&pSD);
    if (FAILED(hr)) 
    {
        _tprintf(
            TEXT("Cannot get IADsSecurityDescriptor: 0x%x\n"), 
            hr);
        goto cleanup;
    } 
     
    /*
    Get an IADsAccessControlList pointer to the security 
    descriptor's DACL.
    */
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(
            IID_IADsAccessControlList,
            (void**)&pACL);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot get DACL: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Create the COM object for the first ACE.
    hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE1);
     
    // Create the COM object for the second ACE.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE2);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot create ACEs: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Set the properties of the two ACEs.
                                
    // Allow read and write access to the property.
    hr = pACE1->put_AccessMask(
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
    hr = pACE2->put_AccessMask( 
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
                                
    // Set the trustee, which is either the service account or the 
    // host computer account.
    hr = pACE1->put_Trustee( sbstrTrustee );
    hr = pACE2->put_Trustee( sbstrTrustee );
                                
    // Set the ACE type.
    hr = pACE1->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
    hr = pACE2->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
                                
    // Set AceFlags to zero because ACE is not inheritable.
    hr = pACE1->put_AceFlags( 0 );
    hr = pACE2->put_AceFlags( 0 );
     
    // Set Flags to indicate an ACE that protects a specified object.
    hr = pACE1->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
    hr = pACE2->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
     
    // Set ObjectType to the schemaIDGUID of the attribute.
    // serviceDNSName
    hr = pACE1->put_ObjectType( 
        L"{28630eb8-41d5-11d1-a9c1-0000f80367c1}"); 
    // serviceBindingInformation
    hr = pACE2->put_ObjectType( 
        L"{b7b1311c-b82e-11d0-afee-0000f80367c1}"); 
     
    /*
    Add the ACEs to the DACL. Need an IDispatch pointer for 
    each ACE to pass to the AddAce method.
    */
    hr = pACE1->QueryInterface(IID_IDispatch,(void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add first ACE: 0x%x\n"), hr);
        goto cleanup;
    }
    else 
    {
        if (pDispACE)
            pDispACE->Release();
    
        pDispACE = NULL;
    }
     
    // Repeat for the second ACE.
    hr = pACE2->QueryInterface(IID_IDispatch, (void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add second ACE: 0x%x\n"), hr);
        goto cleanup;
    }
     
    // Write the modified DACL back to the security descriptor.
    hr = pSD->put_DiscretionaryAcl(pDisp);
    if (SUCCEEDED(hr))
    {
        /*
        Write the ntSecurityDescriptor property to the 
        property cache.
        */
        hr = pSCPObject->Put(sbstrSecurityDescriptor, varSD);
        if (SUCCEEDED(hr))
        {
            // SetInfo updates the SCP object in the directory.
            hr = pSCPObject->SetInfo();
        }
    }
                                    
    cleanup:
    if (pDispACE)
        pDispACE->Release();
                        
    if (pACE1)
        pACE1->Release();
                    
    if (pACE2)
        pACE2->Release();
                    
    if (pACL)
        pACL->Release();
               
    if (pDisp)
        pDisp->Release();
            
    if (pSD)
        pSD->Release();
 
    VariantClear(&varSD);
 
    return hr;
}
```



 

 