---
title: Binding con ADsOpenObject e IADsOpenDSObject OpenDSObject
description: La funzione ADsOpenObject e il metodo IADsOpenDSObject OpenDSObject vengono usati per l'associazione agli oggetti servizio directory quando è necessario specificare credenziali alternative e quando è necessaria la crittografia dei dati.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Binding con ADsOpenObject e IADsOpenDSObject OpenDSObject ADSI
- ADSI ADSI, uso, associazione con ADsOpenObject e IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047354"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a><span data-ttu-id="d442e-105">Binding con ADsOpenObject e IADsOpenDSObject:: OpenDSObject</span><span class="sxs-lookup"><span data-stu-id="d442e-105">Binding With ADsOpenObject and IADsOpenDSObject::OpenDSObject</span></span>

<span data-ttu-id="d442e-106">La funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) vengono usati per l'associazione agli oggetti servizio directory quando è necessario specificare credenziali alternative e quando è necessaria la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="d442e-106">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method are used to bind to directory service objects when alternate credentials must be specified and when data encryption is required.</span></span>

<span data-ttu-id="d442e-107">Quando possibile, è necessario utilizzare le credenziali del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="d442e-107">The credentials of the calling thread should be used when possible.</span></span> <span data-ttu-id="d442e-108">Tuttavia, se è necessario utilizzare le credenziali alternative, è necessario utilizzare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="d442e-108">However, if alternate credentials must be used, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method must be used.</span></span> <span data-ttu-id="d442e-109">Se vengono usate credenziali alternative, è importante non memorizzare la password nella cache.</span><span class="sxs-lookup"><span data-stu-id="d442e-109">If alternate credentials are used, it is important to not cache the password.</span></span> <span data-ttu-id="d442e-110">È possibile eseguire più operazioni di binding specificando il nome utente e la password per la prima operazione di binding e quindi specificando solo il nome utente nelle associazioni successive.</span><span class="sxs-lookup"><span data-stu-id="d442e-110">Multiple bind operations can be performed by specifying the user name and password for the first bind operation and then specifying only the user name in subsequent binds.</span></span> <span data-ttu-id="d442e-111">Il sistema configura una sessione alla prima chiamata e utilizza la stessa sessione per le successive chiamate di binding, purché vengano soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d442e-111">The system sets up a session on the first call and uses the same session on subsequent bind calls as long as the following conditions are met:</span></span>

-   <span data-ttu-id="d442e-112">Lo stesso nome utente in ogni operazione di associazione.</span><span class="sxs-lookup"><span data-stu-id="d442e-112">The same user name in each bind operation.</span></span>
-   <span data-ttu-id="d442e-113">Implementare un'associazione senza server o eseguire l'associazione allo stesso server in ogni operazione di binding.</span><span class="sxs-lookup"><span data-stu-id="d442e-113">Implement serverless binding or bind to the same server in each bind operation.</span></span>
-   <span data-ttu-id="d442e-114">Mantenere una sessione aperta mantenendo un riferimento a un oggetto da una delle operazioni di associazione.</span><span class="sxs-lookup"><span data-stu-id="d442e-114">Maintain an open session by holding on to an object reference from one of the bind operations.</span></span> <span data-ttu-id="d442e-115">La sessione viene chiusa quando viene rilasciato l'ultimo riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d442e-115">The session is closed when the last object reference is released.</span></span>

<span data-ttu-id="d442e-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) utilizzano le [interfacce SSPI (Security Support Provider Interface)](/windows/desktop/SecAuthN/sspi) di Windows NT per garantire la flessibilità nelle opzioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d442e-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) use the Windows NT [Security Support Provider Interfaces (SSPI)](/windows/desktop/SecAuthN/sspi) to allow flexibility in authentication options.</span></span> <span data-ttu-id="d442e-117">Il vantaggio principale dell'utilizzo di queste interfacce consiste nel fornire tipi diversi di autenticazione ai client Active Directory e crittografare la sessione.</span><span class="sxs-lookup"><span data-stu-id="d442e-117">The major advantage of using these interfaces is to provide different types of authentication to Active Directory clients and to encrypt the session.</span></span> <span data-ttu-id="d442e-118">Attualmente, ADSI non consente il passaggio di certificati.</span><span class="sxs-lookup"><span data-stu-id="d442e-118">Currently, ADSI does not allow certificates to be passed in.</span></span> <span data-ttu-id="d442e-119">Pertanto, è possibile utilizzare SSL per la crittografia e quindi Kerberos, NTLM o autenticazione semplice, a seconda della modalità di impostazione dei flag sul parametro *dwReserved* .</span><span class="sxs-lookup"><span data-stu-id="d442e-119">Therefore, you can use SSL for encryption and then Kerberos, NTLM, or simple authentication, depending on how the flags are set on the *dwReserved* parameter.</span></span>

<span data-ttu-id="d442e-120">Non è possibile richiedere un provider SSPI specifico in ADSI, sebbene si ottenga sempre il protocollo preferenziale più alto.</span><span class="sxs-lookup"><span data-stu-id="d442e-120">You cannot request a specific SSPI provider in ADSI, although you always get the highest preference protocol.</span></span> <span data-ttu-id="d442e-121">Nel caso di un'associazione client Windows a un computer che esegue Windows, il protocollo è Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d442e-121">In the case of a Windows client binding to a computer running Windows, the protocol is Kerberos.</span></span> <span data-ttu-id="d442e-122">Non consentire un certificato per l'autenticazione è accettabile nel caso di una pagina Web, in quanto l'autenticazione viene eseguita prima di eseguire la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="d442e-122">Not allowing a certificate for authentication is acceptable in the case of a webpage because authentication occurs prior to running the webpage.</span></span>

<span data-ttu-id="d442e-123">Sebbene le operazioni aperte consentano di specificare un utente e una password, non è consigliabile farlo.</span><span class="sxs-lookup"><span data-stu-id="d442e-123">Although Open operations allow you to specify a user and password, you should not do so.</span></span> <span data-ttu-id="d442e-124">Al contrario, non specificare alcuna credenziale e utilizzare in modo implicito le credenziali del contesto di sicurezza del chiamante.</span><span class="sxs-lookup"><span data-stu-id="d442e-124">Instead, do not specify any credentials and implicitly use the credentials of the caller's security context.</span></span> <span data-ttu-id="d442e-125">Per eseguire il binding a un oggetto directory usando le credenziali del chiamante con [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specificare **null** per nome utente e password.</span><span class="sxs-lookup"><span data-stu-id="d442e-125">To bind to a directory object using the caller's credentials with [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specify **NULL** for both user name and password.</span></span>

<span data-ttu-id="d442e-126">Infine, per eseguire il binding senza autenticazione, usare il flag **Ads \_ No \_ Authentication** .</span><span class="sxs-lookup"><span data-stu-id="d442e-126">Finally, to bind with no authentication, use the **ADS\_NO\_AUTHENTICATION** flag.</span></span> <span data-ttu-id="d442e-127">Nessuna autenticazione indica che ADSI tenta di eseguire l'associazione come utente anonimo all'oggetto di destinazione e non esegue alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d442e-127">No authentication indicates that ADSI attempts to bind as an anonymous user to the target object and performs no authentication.</span></span> <span data-ttu-id="d442e-128">Questa operazione equivale a richiedere l'associazione anonima in LDAP e indica che tutti gli utenti sono inclusi nel contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d442e-128">This is equivalent to requesting anonymous binding in LDAP and indicates that all users are included in the security context.</span></span>

<span data-ttu-id="d442e-129">Se i flag di autenticazione sono impostati su zero, ADSI esegue un binding semplice, inviato come testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="d442e-129">If the authentication flags are set to zero, ADSI performs a simple bind, sent as plaintext.</span></span>

> [!Caution]  
> <span data-ttu-id="d442e-130">Se vengono specificati un nome utente e una password senza specificare i flag di autenticazione, il nome utente e la password vengono trasmessi in rete in testo non crittografato, il che rappresenta un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d442e-130">If a user name and password are specified without specifying authentication flags, the user name and password are transmitted over the network in plaintext, which is a security risk.</span></span> <span data-ttu-id="d442e-131">Non specificare un nome utente e una password senza specificare i flag di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d442e-131">Do not specify a user name and password without specifying authentication flags.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d442e-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="d442e-132">Examples</span></span>

<span data-ttu-id="d442e-133">Nell'esempio di codice Visual Basic riportato di seguito viene illustrato come utilizzare il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="d442e-133">The following Visual Basic code example shows how to use the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span>


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



<span data-ttu-id="d442e-134">Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="d442e-134">The following C++ code example shows how to use the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



<span data-ttu-id="d442e-135">L'interfaccia [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) può essere usata anche in C++, ma Duplica la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="d442e-135">The [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface can also be used in C++, but it duplicates the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>

<span data-ttu-id="d442e-136">Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare l'interfaccia [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) per eseguire la stessa operazione di associazione come nell'esempio di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="d442e-136">The following C++ code example shows how to use the [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface to perform the same bind operation as in the code example above.</span></span>


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 