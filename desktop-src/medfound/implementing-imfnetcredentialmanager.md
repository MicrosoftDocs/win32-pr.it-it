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
# <a name="implementing-imfnetcredentialmanager"></a>Implementazione di IMFNetCredentialManager

Nel metodo [**IMFNetCredentialManager:: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) eseguire le operazioni seguenti.

1.  Se non si dispone già di un puntatore [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , chiamare [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) per creare l'oggetto cache delle credenziali. Archiviare questo puntatore.
2.  Chiamare [**IMFNetCredentialCache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential). Impostare i flag nel parametro *dwAuthenticationFlags* come segue:
    -   Se il membro **hrOp** della struttura [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) è uguale a **NS \_ E \_ proxy \_ AccessDenied**, impostare il flag del **\_ \_ proxy di autenticazione MFNET** .
    -   Se **fClearTextPackage** è **true**, impostare il flag di **\_ \_ \_ testo non crittografato di autenticazione di MFNET** .
    -   Se **fAllowLoggedOnUser** è **true**, impostare il flag dell' **\_ \_ \_ \_ utente connesso per l'autenticazione di MFNET** .
3.  Il metodo [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) restituisce un puntatore [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) ed eventualmente il flag require \_ prompt. Archiviare il puntatore **IMFNetCredential** .
4.  Se [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) non restituisce il flag **Richiedi \_ richiesta** , l'operazione è stata eseguita. Andare al passaggio 9.
5.  In caso contrario, se [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) restituisce il flag **Richiedi \_ richiesta** , è necessario richiedere all'utente il nome utente e la password.
6.  Se **fClearTextPackage** è **false**, crittografare le credenziali.
7.  Chiamare [**IMFNetCredential:: seuser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) e [**IMFNetCredential:: sepassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) per impostare il nome e la password dell'utente nell'oggetto credentials.
8.  Facoltativamente, chiamare [**IMFNetCredentialCache:: SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) per aggiornare l'oggetto cache delle credenziali con le preferenze dell'utente per l'archiviazione e l'invio delle credenziali.
9.  Richiamare il callback [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) chiamando [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).

Nel metodo [**IMFNetCredentialManager:: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) restituire il puntatore [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) ottenuto nel metodo [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) .

Nel metodo [**IMFNetCredentialManager:: Sebuonissimo**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) passare i parametri di input direttamente al metodo [**IMFNetCredentialCache::**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) SetValue. Viene inviata una notifica alla cache delle credenziali se le credenziali sono state accettate dal server.

Se è necessario richiedere all'utente (passaggio 5) o crittografare le credenziali (passaggio 6), è necessario eseguire questa operazione in un thread della coda di lavoro, in modo da non bloccare la pipeline Microsoft Media Foundation. Chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , quindi eseguire i passaggi rimanenti all'interno del callback della coda di lavoro.

> [!Note]  
> Tenere presente che [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) potrebbe essere richiamato durante la creazione dell'origine di rete. Se pertanto si crea l'origine di rete chiamando il metodo [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) sincrono, il thread chiamante potrebbe bloccarsi mentre le credenziali vengono acquisite. È quindi consigliabile usare invece il metodo asincrono [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .

 

## <a name="example"></a>Esempio

In questo esempio viene illustrato un tipo di comportamento che può essere fornito da un gestore di credenziali.

Ecco una dichiarazione della classe che implementa [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).


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



Per tenere traccia dello stato dell'operazione [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) , la classe usa l'oggetto helper seguente:


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



Il metodo [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) crea la cache delle credenziali e ottiene un puntatore [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) . Se l'utente deve essere richiesto, indicato dal flag **Richiedi \_ richiesta** , il metodo chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) per accodare un nuovo elemento di lavoro:


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



Il thread della coda di lavoro chiama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), che richiede all'utente e quindi chiama [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) per richiamare il puntatore di callback fornito in [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).


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



Il metodo [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) completa l'operazione restituendo il puntatore [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) al chiamante.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione origine rete](network-source-authentication.md)
</dt> </dl>

 

 



