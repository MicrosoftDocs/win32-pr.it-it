---
title: Autenticazione (Windows Media Format 11 SDK)
description: Autenticazione
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows Media Format SDK, autenticazione
- Windows Media Format SDK, autenticazione di rete
- Advanced Systems Format (ASF), autenticazione
- ASF (Advanced Systems Format), autenticazione
- Advanced Systems Format (ASF), autenticazione di rete
- ASF (Advanced Systems Format), autenticazione di rete
- autenticazione
- autenticazione di rete, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee276bc2800ad7f2d5fa94f00e282dc7d4f5402396d69eb7e3b240fd4303f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007121"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Autenticazione (Windows Media Format 11 SDK)

L'oggetto lettore può gestire i problemi di autenticazione di rete, tra cui l'autenticazione del digest e l'autenticazione NTLM. In alcuni casi l'applicazione deve fornire le credenziali dell'utente tramite un'interfaccia di callback:

-   Autenticazione del digest: l'applicazione deve implementare **l'interfaccia IWMCredentialCallback,** come descritto più avanti in questo argomento.
-   Autenticazione NTLM: il lettore risponde automaticamente con le credenziali di accesso dell'utente. Se l'utente corrente è autorizzato ad accedere al server, l'applicazione non deve eseguire alcun'operazione. Se l'utente non dispone dell'autorizzazione, l'applicazione deve implementare **l'interfaccia IWMCredentialCallback.**

    > [!Note]  
    > Servizi Windows Media versione 4.1 non supporta l'autenticazione NTLM tramite un server proxy. L'autenticazione NTLM richiede diversi scambi client-server nella stessa connessione e la versione 4.1 non mantiene una connessione permanente con il proxy. Servizi Windows Media serie 9 in Microsoft Windows Server 2003 supporta l'autenticazione NTLM tramite un server proxy, purché il proxy supporti le connessioni keep-alive.

     

Come si è fatto presente, in alcuni casi l'applicazione deve fornire le credenziali dell'utente. Ciò si verifica tramite **l'interfaccia IWMCredentialCallback,** che ha un singolo metodo, **AcquireCredentials**. Per supportare l'autenticazione, implementare questa interfaccia nell'applicazione. L'oggetto lettore esegue una query per questa interfaccia chiamando **QueryInterface** sul puntatore [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) ricevuto dall'applicazione nel metodo [**IWMReader::Open.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) Se l'oggetto lettore deve ottenere le credenziali dell'utente, chiama il metodo **AcquireCredentials** dell'applicazione.

Se le credenziali verranno inviate in rete senza crittografia, il lettore imposta il flag WMT \_ CREDENTIAL CLEAR TEXT nel parametro \_ \_ *pdwFlags.* In questo modo l'applicazione può avvisare l'utente che le proprie credenziali verranno inviate in testo normale.

In caso contrario, l'oggetto lettore crittografa automaticamente le credenziali prima di inviarle in rete. L'applicazione può restituirli all'oggetto lettore in testo normale. Inoltre, se l'oggetto reader imposta il flag WMT CREDENTIAL ENCRYPT, significa che il lettore supporta il recupero di credenziali \_ \_ crittografate dall'applicazione. In tal caso, l'applicazione può restituire le credenziali in testo normale oppure crittografarle usando la funzione **CryptProtectData,** descritta nella documentazione di Platform SDK. Se l'applicazione crittografa le credenziali, deve impostare il flag WMT CREDENTIAL ENCRYPT nel \_ \_ parametro *pdwFlags* prima che il metodo venga restituito.

In genere, non è necessario crittografare i dati, perché l'oggetto lettore crittografa i dati, se necessario. Tuttavia, la crittografia potrebbe essere utile se l'applicazione mantiene il nome utente e la password in memoria, perché impedisce a un utente malintenzionato di esaminare un dump della memoria del processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




