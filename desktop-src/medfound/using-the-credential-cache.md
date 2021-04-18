---
description: Uso della cache delle credenziali
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Uso della cache delle credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308987"
---
# <a name="using-the-credential-cache"></a><span data-ttu-id="4add0-103">Uso della cache delle credenziali</span><span class="sxs-lookup"><span data-stu-id="4add0-103">Using the Credential Cache</span></span>

<span data-ttu-id="4add0-104">Media Foundation fornisce un'implementazione predefinita dell'interfaccia [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="4add0-104">Media Foundation provides a default implementation of the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface.</span></span> <span data-ttu-id="4add0-105">Un'applicazione che implementa l'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) può utilizzare l'oggetto della cache delle credenziali predefinito per archiviare le credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4add0-105">An application that implements the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface can use the default credential cache object to store the user's credentials.</span></span>

<span data-ttu-id="4add0-106">Per creare l'oggetto cache delle credenziali predefinito, chiamare la funzione [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="4add0-106">To create the default credential cache object, call the [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) function.</span></span>


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



<span data-ttu-id="4add0-107">Dopo la creazione della cache delle credenziali, l'applicazione può utilizzare i metodi seguenti per ottenere un oggetto credenziale, impostare le credenziali utente e specificare le opzioni di memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="4add0-107">After the credential cache is created, the application can use the following methods to get a credential object, set user credentials, and specify the caching options.</span></span>

-   <span data-ttu-id="4add0-108">Per ottenere l'oggetto Credential per un URL, chiamare [**IMFNetCredentialCache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="4add0-108">To get the credential object for a URL, call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span>

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    <span data-ttu-id="4add0-109">Se le credenziali per l'URL specificato non sono presenti nella cache delle credenziali, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) crea un nuovo oggetto credenziale con valori di nome utente e password vuoti.</span><span class="sxs-lookup"><span data-stu-id="4add0-109">If the credentials for the specified URL do not exist in the credential cache, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) creates a new credential object with empty user name and password values.</span></span>

-   <span data-ttu-id="4add0-110">Per impostare il nome utente e la password nell'oggetto Credential, chiamare [**IMFNetCredential:: seuser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) e [**IMFNetCredential:: password**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span><span class="sxs-lookup"><span data-stu-id="4add0-110">To set the user name and password on the credential object, call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span></span>
-   <span data-ttu-id="4add0-111">Per impostare le opzioni di memorizzazione nella cache per l'oggetto credenziale, chiamare [**IMFNetCredentialCache:: SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span><span class="sxs-lookup"><span data-stu-id="4add0-111">To set the caching options on the credential object, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span></span>

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    <span data-ttu-id="4add0-112">I valori dei parametri *dwOptionsFlags* sono definiti nell'enumerazione [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) .</span><span class="sxs-lookup"><span data-stu-id="4add0-112">The *dwOptionsFlags* parameter values are defined in the [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) enumeration.</span></span> <span data-ttu-id="4add0-113">Per salvare le credenziali utente per un URL in un archivio permanente, impostare il \_ flag di salvataggio delle credenziali di MFNET \_ .</span><span class="sxs-lookup"><span data-stu-id="4add0-113">To save user credentials for a URL in a persistent storage, set the MFNET\_CREDENTIAL\_SAVE flag.</span></span> <span data-ttu-id="4add0-114">Se la chiamata [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) viene completata correttamente, la chiamata successiva a [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) Cerca le credenziali nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="4add0-114">If the [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) call completes successfully, then the subsequent call to [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) searches for the credentials in the persistent storage.</span></span> <span data-ttu-id="4add0-115">Se viene trovata una corrispondenza, questo metodo restituisce un puntatore all'oggetto credenziale che contiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="4add0-115">If a match is found, this method returns a pointer to the credential object that contains the information.</span></span>

    <span data-ttu-id="4add0-116">Per impostazione predefinita, le credenziali utente inviate in rete vengono crittografate.</span><span class="sxs-lookup"><span data-stu-id="4add0-116">By default, user credentials sent over the network are encrypted.</span></span> <span data-ttu-id="4add0-117">Per modificare questa impostazione in testo non crittografato, impostare il \_ \_ \_ flag Consenti testo non crittografato per le credenziali MFNET \_ .</span><span class="sxs-lookup"><span data-stu-id="4add0-117">To change this to clear text, set the MFNET\_CREDENTIAL\_ALLOW\_CLEAR\_TEXT flag.</span></span>

    <span data-ttu-id="4add0-118">Per rimuovere le informazioni dal registro di sistema, chiamare [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) per ottenere l'oggetto Credential, quindi chiamare [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) e impostare *dwOptionsFlags* su MFNET \_ Credential \_ dont \_ cache.</span><span class="sxs-lookup"><span data-stu-id="4add0-118">To remove information from the registry, call [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) to get the credential object, and then call [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) and set *dwOptionsFlags* to MFNET\_CREDENTIAL\_DONT\_CACHE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4add0-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4add0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4add0-120">Autenticazione origine rete</span><span class="sxs-lookup"><span data-stu-id="4add0-120">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



