---
description: Implementazione di IMFNetCredentialManager
ms.assetid: 3eb2afec-195c-4d8d-8e08-7e6ec7c572f8
title: Implementazione di IMFNetCredentialManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c026f2c12b2ff248032a56d9c48a0e0e1576c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307517"
---
# <a name="implementing-imfnetcredentialmanager"></a><span data-ttu-id="7b33a-103">Implementazione di IMFNetCredentialManager</span><span class="sxs-lookup"><span data-stu-id="7b33a-103">Implementing IMFNetCredentialManager</span></span>

<span data-ttu-id="7b33a-104">Nel metodo [**IMFNetCredentialManager:: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b33a-104">In the [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method, do the following.</span></span>

1.  <span data-ttu-id="7b33a-105">Se non si dispone già di un puntatore [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , chiamare [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) per creare l'oggetto cache delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="7b33a-105">If you do not have an [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) pointer already, call [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) to create the credential cache object.</span></span> <span data-ttu-id="7b33a-106">Archiviare questo puntatore.</span><span class="sxs-lookup"><span data-stu-id="7b33a-106">Store this pointer.</span></span>
2.  <span data-ttu-id="7b33a-107">Chiamare [**IMFNetCredentialCache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="7b33a-107">Call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span> <span data-ttu-id="7b33a-108">Impostare i flag nel parametro *dwAuthenticationFlags* come segue:</span><span class="sxs-lookup"><span data-stu-id="7b33a-108">Set the flags in the *dwAuthenticationFlags* parameter as follows:</span></span>
    -   <span data-ttu-id="7b33a-109">Se il membro **hrOp** della struttura [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) è uguale a **NS \_ E \_ proxy \_ AccessDenied**, impostare il flag del **\_ \_ proxy di autenticazione MFNET** .</span><span class="sxs-lookup"><span data-stu-id="7b33a-109">If the **hrOp** member of the [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) structure equals **NS\_E\_PROXY\_ACCESSDENIED**, set the **MFNET\_AUTHENTICATION\_PROXY** flag.</span></span>
    -   <span data-ttu-id="7b33a-110">Se **fClearTextPackage** è **true**, impostare il flag di **\_ \_ \_ testo non crittografato di autenticazione di MFNET** .</span><span class="sxs-lookup"><span data-stu-id="7b33a-110">If **fClearTextPackage** is **TRUE**, set the **MFNET\_AUTHENTICATION\_CLEAR\_TEXT** flag.</span></span>
    -   <span data-ttu-id="7b33a-111">Se **fAllowLoggedOnUser** è **true**, impostare il flag dell' **\_ \_ \_ \_ utente connesso per l'autenticazione di MFNET** .</span><span class="sxs-lookup"><span data-stu-id="7b33a-111">If **fAllowLoggedOnUser** is **TRUE**, set the **MFNET\_AUTHENTICATION\_LOGGED\_ON\_USER** flag.</span></span>
3.  <span data-ttu-id="7b33a-112">Il metodo [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) restituisce un puntatore [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) ed eventualmente il flag require \_ prompt.</span><span class="sxs-lookup"><span data-stu-id="7b33a-112">The [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) method returns an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer and possibly the REQUIRE\_PROMPT flag.</span></span> <span data-ttu-id="7b33a-113">Archiviare il puntatore **IMFNetCredential** .</span><span class="sxs-lookup"><span data-stu-id="7b33a-113">Store the **IMFNetCredential** pointer.</span></span>
4.  <span data-ttu-id="7b33a-114">Se [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) non restituisce il flag **Richiedi \_ richiesta** , l'operazione è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="7b33a-114">If [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) does not return the **REQUIRE\_PROMPT** flag, you are done.</span></span> <span data-ttu-id="7b33a-115">Andare al passaggio 9.</span><span class="sxs-lookup"><span data-stu-id="7b33a-115">Skip to step 9.</span></span>
5.  <span data-ttu-id="7b33a-116">In caso contrario, se [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) restituisce il flag **Richiedi \_ richiesta** , è necessario richiedere all'utente il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="7b33a-116">Otherwise, if [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) returns the **REQUIRE\_PROMPT** flag, you must prompt the user for his or her user name and password.</span></span>
6.  <span data-ttu-id="7b33a-117">Se **fClearTextPackage** è **false**, crittografare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7b33a-117">If **fClearTextPackage** is **FALSE**, encrypt the credentials.</span></span>
7.  <span data-ttu-id="7b33a-118">Chiamare [**IMFNetCredential:: seuser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) e [**IMFNetCredential:: sepassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) per impostare il nome e la password dell'utente nell'oggetto credentials.</span><span class="sxs-lookup"><span data-stu-id="7b33a-118">Call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) to set the user's name and password on the credentials object.</span></span>
8.  <span data-ttu-id="7b33a-119">Facoltativamente, chiamare [**IMFNetCredentialCache:: SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) per aggiornare l'oggetto cache delle credenziali con le preferenze dell'utente per l'archiviazione e l'invio delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="7b33a-119">Optionally, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) to update the credential cache object with the user's preferences for storing and sending credentials.</span></span>
9.  <span data-ttu-id="7b33a-120">Richiamare il callback [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) chiamando [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="7b33a-120">Invoke the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>

<span data-ttu-id="7b33a-121">Nel metodo [**IMFNetCredentialManager:: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) restituire il puntatore [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) ottenuto nel metodo [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) .</span><span class="sxs-lookup"><span data-stu-id="7b33a-121">In the [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method, return the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer obtained in the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span>

<span data-ttu-id="7b33a-122">Nel metodo [**IMFNetCredentialManager:: Sebuonissimo**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) passare i parametri di input direttamente al metodo [**IMFNetCredentialCache::**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) SetValue.</span><span class="sxs-lookup"><span data-stu-id="7b33a-122">In the [**IMFNetCredentialManager::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) method, pass the input parameters directly to the [**IMFNetCredentialCache::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) method.</span></span> <span data-ttu-id="7b33a-123">Viene inviata una notifica alla cache delle credenziali se le credenziali sono state accettate dal server.</span><span class="sxs-lookup"><span data-stu-id="7b33a-123">This notifies the credential cache whether the credentials were accepted by the server.</span></span>

<span data-ttu-id="7b33a-124">Se è necessario richiedere all'utente (passaggio 5) o crittografare le credenziali (passaggio 6), è necessario eseguire questa operazione in un thread della coda di lavoro, in modo da non bloccare la pipeline Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7b33a-124">If you need to prompt the user (step 5) or encrypt the credentials (step 6), you should do so on a work-queue thread, so that you do not block the Microsoft Media Foundation pipeline.</span></span> <span data-ttu-id="7b33a-125">Chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , quindi eseguire i passaggi rimanenti all'interno del callback della coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7b33a-125">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) and then perform the remaining steps inside the work-queue callback.</span></span>

> [!Note]  
> <span data-ttu-id="7b33a-126">Tenere presente che [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) potrebbe essere richiamato durante la creazione dell'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="7b33a-126">Be aware that [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) might be invoked while the network source is being created.</span></span> <span data-ttu-id="7b33a-127">Se pertanto si crea l'origine di rete chiamando il metodo [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) sincrono, il thread chiamante potrebbe bloccarsi mentre le credenziali vengono acquisite.</span><span class="sxs-lookup"><span data-stu-id="7b33a-127">Therefore, if you create the network source by calling the synchronous [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method, your calling thread might block while the credentials are acquired.</span></span> <span data-ttu-id="7b33a-128">È quindi consigliabile usare invece il metodo asincrono [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="7b33a-128">Therefore, it is recommended to use the asynchronous [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method instead.</span></span>

 

## <a name="example"></a><span data-ttu-id="7b33a-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="7b33a-129">Example</span></span>

<span data-ttu-id="7b33a-130">In questo esempio viene illustrato un tipo di comportamento che può essere fornito da un gestore di credenziali.</span><span class="sxs-lookup"><span data-stu-id="7b33a-130">This example shows one type of behavior that a credential manager could provide.</span></span>

<span data-ttu-id="7b33a-131">Ecco una dichiarazione della classe che implementa [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span><span class="sxs-lookup"><span data-stu-id="7b33a-131">Here is a declaration of the class that implements [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span></span>


```C++
class CCredentialManager : public IMFNetCredentialManager, IMFAsyncCallback 
{
    long                    m_cRef;
    IMFNetCredentialCache   *m_pCredentialCache;

public:
    CCredentialManager () : m_cRef(1), m_pCredentialCache(NULL)
    { 
    }
    ~CCredentialManager()
    {
        SafeRelease(&m_pCredentialCache);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCredentialManager, IMFNetCredentialManager),
            QITABENT(CCredentialManager, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP BeginGetCredentials(
        MFNetCredentialManagerGetParam* pParam,
        IMFAsyncCallback* pCallback,
        IUnknown* pState
        );

    STDMETHODIMP EndGetCredentials(
        IMFAsyncResult* pResult, 
        IMFNetCredential** ppCred);

    STDMETHODIMP SetGood(IMFNetCredential* pCred, BOOL fGood)
    {
        if (!pCred)
        {
            return E_POINTER;
        }

        return m_pCredentialCache->SetGood(pCred, fGood);
    }


    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



<span data-ttu-id="7b33a-132">Per tenere traccia dello stato dell'operazione [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) , la classe usa l'oggetto helper seguente:</span><span class="sxs-lookup"><span data-stu-id="7b33a-132">To track the state of the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) operation, the class uses the following helper object:</span></span>


```C++
// Holds state information for the GetCredentials operation, so that work can 
// be moved to a work-queue thread.

struct CredentialOp : public IUnknown
{
    long                m_cRef;
    IMFNetCredential    *m_pCredential;
    DWORD               m_dwFlags;

    CredentialOp(IMFNetCredential *pCredential) 
        : m_cRef(1), m_dwFlags(0), m_pCredential(pCredential)
    {
        m_pCredential->AddRef();
    }

    ~CredentialOp()
    {
        SafeRelease(&m_pCredential);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CredentialOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



<span data-ttu-id="7b33a-133">Il metodo [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) crea la cache delle credenziali e ottiene un puntatore [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="7b33a-133">The [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method creates the credential cache and gets an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer.</span></span> <span data-ttu-id="7b33a-134">Se l'utente deve essere richiesto, indicato dal flag **Richiedi \_ richiesta** , il metodo chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) per accodare un nuovo elemento di lavoro:</span><span class="sxs-lookup"><span data-stu-id="7b33a-134">If the user must be prompted (indicated by the **REQUIRE\_PROMPT** flag), the method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item:</span></span>


```C++
STDMETHODIMP CCredentialManager::BeginGetCredentials(
    MFNetCredentialManagerGetParam* pParam,
    IMFAsyncCallback* pCallback,
    IUnknown* pState
    )
{
    if (!pParam || !pCallback)
    {
        return E_POINTER;
    }

    DWORD dwAuthenticationFlags = 0;
    DWORD dwRequirementFlags = 0;

    if (pParam->hrOp == NS_E_PROXY_ACCESSDENIED)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_PROXY;
    }

    if (pParam->fAllowLoggedOnUser)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_LOGGED_ON_USER;
    }

    if (pParam->fClearTextPackage)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_CLEAR_TEXT;
    }

    IMFNetCredential *pCredential =  NULL;
    IMFAsyncResult* pResult = NULL;

    HRESULT hr = S_OK;

    if (m_pCredentialCache == NULL)
    {
        hr = MFCreateCredentialCache(&m_pCredentialCache);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    hr = m_pCredentialCache->GetCredential(
        pParam->pszUrl, 
        pParam->pszRealm, 
        dwAuthenticationFlags, 
        &pCredential, 
        &dwRequirementFlags
        );

    if (FAILED(hr))
    {
        goto done;
    }

    if( ( dwRequirementFlags & REQUIRE_PROMPT ) == 0 )
    {
        // The credential is good to use. Prompting the user is not required.
        hr = S_OK;
        goto done;
    }

    // The credential requires prompting the user. 
    CredentialOp *pOp = new (std::nothrow) CredentialOp(pCredential);

    if (pOp == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Set flags. Use these to inform the user if the credentials will
    // be sent in plaintext or saved in the credential cache.

    if (pParam->fClearTextPackage)
    {
        // Notify the user that credentials will be sent in plaintext.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT;
    }

    if(dwRequirementFlags & REQUIRE_SAVE_SELECTED )
    {
        // Credentials will be saved in the cache by default.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_SAVE;
    }

    // NOTE: The application should enable to user to deselect these two flags;
    // for example, through check boxes in the prompt dialog.


    // Now queue the work item.

    hr = MFCreateAsyncResult(pOp, pCallback, pState, &pResult);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION, this, pResult);

done:
    SafeRelease(&pResult);
    SafeRelease(&pCredential);
    SafeRelease(&pOp);
    return hr;
}
```



<span data-ttu-id="7b33a-135">Il thread della coda di lavoro chiama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), che richiede all'utente e quindi chiama [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) per richiamare il puntatore di callback fornito in [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span><span class="sxs-lookup"><span data-stu-id="7b33a-135">The work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), which prompts the user and then calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the callback pointer that was provided in [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span></span>


```C++
STDMETHODIMP CCredentialManager::Invoke(IMFAsyncResult* pResult)
{
    IUnknown *pState = NULL;
    IMFAsyncResult *pGetCredentialsResult = NULL;
    IUnknown *pOpState = NULL;

    CredentialOp *pOp = NULL;   // not AddRef'd

    HRESULT hr = pResult->GetState(&pState);

    if (SUCCEEDED(hr))
    {
        hr = pState->QueryInterface(IID_PPV_ARGS(&pGetCredentialsResult));
    }

    if (SUCCEEDED(hr))
    {
        hr = pGetCredentialsResult->GetObject(&pOpState);
    }

    if (SUCCEEDED(hr))
    {
        pOp = static_cast<CredentialOp*>(pOpState);

        // Display a dialog for the user to enter user name and password.
        hr = PromptUserCredentials(pOp);
    }

    if (SUCCEEDED(hr) && m_pCredentialCache)
    {
        // Update with options set by the user.
        hr = m_pCredentialCache->SetUserOptions(
            pOp->m_pCredential, 
            pOp->m_dwFlags
            );
    }

    if (pGetCredentialsResult)
    {
        pGetCredentialsResult->SetStatus(hr);
        MFInvokeCallback(pGetCredentialsResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pGetCredentialsResult);
    SafeRelease(&pOpState);
    return S_OK;
}
```



<span data-ttu-id="7b33a-136">Il metodo [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) completa l'operazione restituendo il puntatore [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) al chiamante.</span><span class="sxs-lookup"><span data-stu-id="7b33a-136">The [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method completes the operation by returning the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer to the caller.</span></span>


```C++
STDMETHODIMP CCredentialManager::EndGetCredentials(
    IMFAsyncResult* pResult, 
    IMFNetCredential** ppCred
    )
{
    if (!pResult || !ppCred)
    {
        return E_POINTER;
    }

    *ppCred = NULL;

    IUnknown *pUnk = NULL;

    // Check the result of the asynchronous operation.
    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        // The operation failed.
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    CredentialOp *pOp = static_cast<CredentialOp*>(pUnk);

    *ppCred = pOp->m_pCredential;
    pOp->m_pCredential = NULL;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7b33a-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b33a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b33a-138">Autenticazione origine rete</span><span class="sxs-lookup"><span data-stu-id="7b33a-138">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



