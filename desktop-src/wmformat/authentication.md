---
title: Autenticazione (Windows Media Format 11 SDK)
description: Authentication
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows Media Format SDK, autenticazione
- Windows Media Format SDK, autenticazione di rete
- ASF (Advanced Systems Format), autenticazione
- ASF (formato avanzato dei sistemi), autenticazione
- ASF (Advanced Systems Format), autenticazione di rete
- ASF (formato avanzato dei sistemi), autenticazione di rete
- autenticazione
- autenticazione di rete, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300872"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Autenticazione (Windows Media Format 11 SDK)

L'oggetto Reader può gestire le richieste di autenticazione di rete, tra cui l'autenticazione del digest e l'autenticazione NTLM. In alcuni casi l'applicazione deve fornire le credenziali dell'utente tramite un'interfaccia di callback:

-   Autenticazione del digest: l'applicazione deve implementare l'interfaccia **IWMCredentialCallback** , come descritto più avanti in questo argomento.
-   Autenticazione NTLM: il lettore risponde automaticamente con le credenziali di accesso dell'utente. Se l'utente corrente è autorizzato ad accedere al server, l'applicazione non deve eseguire alcuna operazione. Se l'utente non dispone dell'autorizzazione, l'applicazione deve implementare l'interfaccia **IWMCredentialCallback** .

    > [!Note]  
    > Windows Media Services versione 4,1 non supporta l'autenticazione NTLM tramite un server proxy. Per l'autenticazione NTLM sono necessari diversi scambi client-server nella stessa connessione e la versione 4,1 non mantiene una connessione persistente con il proxy. Windows Media Services 9 Series in Microsoft Windows Server 2003 supporta l'autenticazione NTLM tramite un server proxy, purché il proxy supporti le connessioni keep-alive.

     

Come indicato, in alcuni casi l'applicazione deve fornire le credenziali dell'utente. Questo problema si verifica tramite l'interfaccia **IWMCredentialCallback** , che ha un singolo metodo, **AcquireCredentials**. Per supportare l'autenticazione, implementare questa interfaccia nell'applicazione. L'oggetto Reader esegue una query per questa interfaccia chiamando **QueryInterface** sul puntatore [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) ricevuto dall'applicazione nel metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) . Se l'oggetto Reader deve ottenere le credenziali dell'utente, chiama il metodo **AcquireCredentials** dell'applicazione.

Se le credenziali vengono inviate in rete senza crittografia, il lettore imposta il \_ \_ flag di testo non crittografato delle credenziali WMT \_ nel parametro *pdwFlags* . Ciò consente all'applicazione di avvisare l'utente che le credenziali verranno inviate in testo normale.

In caso contrario, l'oggetto Reader crittografa automaticamente le credenziali prima di inviarle sulla rete. L'applicazione può restituirle all'oggetto Reader in testo normale. Inoltre, se l'oggetto Reader imposta il \_ \_ flag di crittografia delle credenziali WMT, significa che il lettore supporta la lettura delle credenziali crittografate dall'applicazione. In tal caso, l'applicazione può restituire le credenziali in testo normale, altrimenti crittografarle usando la funzione **CryptProtectData** , descritta nella documentazione di Platform SDK. Se l'applicazione crittografa le credenziali, deve impostare il \_ \_ flag di crittografia delle credenziali WMT nel parametro *pdwFlags* prima che il metodo restituisca.

In genere, non è necessario crittografare i dati, perché l'oggetto Reader crittografa i dati, se necessario. Tuttavia, la crittografia può essere utile se l'applicazione mantiene il nome utente e la password in memoria, perché impedisce a un utente malintenzionato di ispezionare un dump della memoria del processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




