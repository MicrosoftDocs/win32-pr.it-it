---
title: Classe CSecureChannelServer
description: Classe CSecureChannelServer
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Gestione dispositivi multimediali, classe CSecureChannelServer
- Gestione dispositivi, classe CSecureChannelServer
- provider di servizi,classe CSecureChannelServer
- informazioni di riferimento sulla programmazione, classe CSecureChannelServer
- informazioni di riferimento Windows Gestione dispositivi multimediali, classe CSecureChannelServer
- Classe CSecureChannelServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87627fcdee6da42927ab88411dd579225dc38f025ae73bf9f4fe787c0c5e44bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585485"
---
# <a name="csecurechannelserver-class"></a>Classe CSecureChannelServer

La **classe CSecureChannelServer** è una classe helper (non un'interfaccia) che consente a un provider di servizi o a un provider di contenuto protetto di autenticare un'applicazione usando l'interfaccia [**IComponentAuthenticate,**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) crittografare e decrittografare i dati e creare firme MAC. Il processo di autenticazione richiede che l'applicazione crei un **oggetto CSecureChannelClient** e che il provider di servizi crei un **oggetto CSecureChannelServer.** Le **classi CSecureChannelClient** **e CSecureChannelServer** vengono dichiarate nella libreria a collegamento statico Mssachlp.lib. Tutti i metodi di Windows Gestione dispositivi multimediali, il provider di servizi e le interfacce del provider di contenuti protetti possono restituire WMDM E NOTCERTIFIED per indicare che il chiamante non è stato \_ \_ autenticato correttamente.

La **classe CSecureChannelServer** espone i metodi seguenti.



| Metodo                                                            | Descrizione                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**DecryptParam**](/previous-versions/bb231598(v=vs.85))         | Decrittografa i dati contenuti in un parametro .                                                 |
| [**EncryptParam**](/previous-versions/ms868509(v=msdn.10))         | Crittografa i dati contenuti in un parametro.                                                 |
| [**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) | Verifica che un canale di autenticazione sicuro sia stato stabilito correttamente.            |
| [**GetAppSec**](/previous-versions/bb231601(v=vs.85))               | Recupera i livelli di sicurezza dell'applicazione dei componenti locali e remoti.               |
| [**GetSessionKey**](/previous-versions/bb231602(v=vs.85))       | Recupera la chiave di sessione corrente.                                                          |
| [**MACFinal**](/previous-versions/ms868513(v=msdn.10))                 | Rilascia il canale MAC (Message Authentication Code) e recupera un valore MAC finale.     |
| [**MACInit**](/previous-versions/ms868514(v=msdn.10))                   | Acquisisce un canale MAC (Message Authentication Code).                                       |
| [**MACUpdate**](/previous-versions/ms868515(v=msdn.10))               | Aggiorna il valore mac (Message Authentication Code) con un valore di parametro.                 |
| [**SACAuth**](/previous-versions/ms868516(v=msdn.10))                   | Stabilisce un canale autenticato sicuro tra i componenti.                              |
| [**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))   | Segnala i protocolli supportati da un componente.                                             |
| [**SetCertificate**](/previous-versions/ms868518(v=msdn.10))     | Specifica il certificato e la chiave privata del server SAC (Secure Authenticated Channel). |
| [**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))       | Imposta la chiave di sessione utilizzata per comunicare con un altro componente.                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CSecureChannelClient**](csecurechannelclient-class.md)
</dt> <dt>

[**Interfaccia IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfacce per i provider di servizi**](interfaces-for-service-providers.md)
</dt> <dt>

[**Uso di canali autenticati sicuri**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 