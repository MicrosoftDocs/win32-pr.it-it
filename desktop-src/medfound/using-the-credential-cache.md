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
# <a name="using-the-credential-cache"></a>Uso della cache delle credenziali

Media Foundation fornisce un'implementazione predefinita dell'interfaccia [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) . Un'applicazione che implementa l'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) può utilizzare l'oggetto della cache delle credenziali predefinito per archiviare le credenziali dell'utente.

Per creare l'oggetto cache delle credenziali predefinito, chiamare la funzione [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



Dopo la creazione della cache delle credenziali, l'applicazione può utilizzare i metodi seguenti per ottenere un oggetto credenziale, impostare le credenziali utente e specificare le opzioni di memorizzazione nella cache.

-   Per ottenere l'oggetto Credential per un URL, chiamare [**IMFNetCredentialCache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    Se le credenziali per l'URL specificato non sono presenti nella cache delle credenziali, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) crea un nuovo oggetto credenziale con valori di nome utente e password vuoti.

-   Per impostare il nome utente e la password nell'oggetto Credential, chiamare [**IMFNetCredential:: seuser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) e [**IMFNetCredential:: password**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).
-   Per impostare le opzioni di memorizzazione nella cache per l'oggetto credenziale, chiamare [**IMFNetCredentialCache:: SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    I valori dei parametri *dwOptionsFlags* sono definiti nell'enumerazione [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) . Per salvare le credenziali utente per un URL in un archivio permanente, impostare il \_ flag di salvataggio delle credenziali di MFNET \_ . Se la chiamata [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) viene completata correttamente, la chiamata successiva a [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) Cerca le credenziali nell'archivio permanente. Se viene trovata una corrispondenza, questo metodo restituisce un puntatore all'oggetto credenziale che contiene le informazioni.

    Per impostazione predefinita, le credenziali utente inviate in rete vengono crittografate. Per modificare questa impostazione in testo non crittografato, impostare il \_ \_ \_ flag Consenti testo non crittografato per le credenziali MFNET \_ .

    Per rimuovere le informazioni dal registro di sistema, chiamare [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) per ottenere l'oggetto Credential, quindi chiamare [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) e impostare *dwOptionsFlags* su MFNET \_ Credential \_ dont \_ cache.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione origine rete](network-source-authentication.md)
</dt> </dl>

 

 



