---
title: Classe CSecureChannelServer
description: Classe CSecureChannelServer
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Gestione dispositivi, classe CSecureChannelServer
- Gestione dispositivi, classe CSecureChannelServer
- provider di servizi, classe CSecureChannelServer
- Guida di riferimento alla programmazione, classe CSecureChannelServer
- informazioni di riferimento su Windows Media Gestione dispositivi, classe CSecureChannelServer
- Classe CSecureChannelServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727879"
---
# <a name="csecurechannelserver-class"></a>Classe CSecureChannelServer

La classe **CSecureChannelServer** è una classe helper (non un'interfaccia) che consente a un provider di servizi o a un provider di contenuti protetto di autenticare un'applicazione usando l'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) , di crittografare e decrittografare i dati e di creare firme Mac. Il processo di autenticazione richiede che l'applicazione crei un oggetto **CSecureChannelClient** e che il provider di servizi crei un oggetto **CSecureChannelServer** . Le classi **CSecureChannelClient** e **CSecureChannelServer** sono dichiarate nella libreria a collegamento statico, mssachlp. lib. Tutti i metodi di Windows Media Gestione dispositivi, provider di servizi e interfacce del provider di contenuti protetti possono restituire WMDM \_ E \_ NOTCERTIFIED per indicare che il chiamante non è stato autenticato correttamente.

La classe **CSecureChannelServer** espone i metodi seguenti.



| Metodo                                                            | Descrizione                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**DecryptParam**](/previous-versions/bb231598(v=vs.85))         | Decrittografa i dati contenuti in un parametro.                                                 |
| [**EncryptParam**](/previous-versions/ms868509(v=msdn.10))         | Crittografa i dati contenuti in un parametro.                                                 |
| [**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) | Verifica che sia stato stabilito correttamente un canale di autenticazione protetto.            |
| [**GetAppSec**](/previous-versions/bb231601(v=vs.85))               | Recupera i livelli di sicurezza dell'applicazione dei componenti locali e remoti.               |
| [**GetSessionKey**](/previous-versions/bb231602(v=vs.85))       | Recupera la chiave della sessione corrente.                                                          |
| [**MACFinal**](/previous-versions/ms868513(v=msdn.10))                 | Rilascia il canale MAC (Message Authentication Code) e recupera un valore MAC finale.     |
| [**MACInit**](/previous-versions/ms868514(v=msdn.10))                   | Acquisisce un canale MAC (Message Authentication Code).                                       |
| [**MACUpdate**](/previous-versions/ms868515(v=msdn.10))               | Aggiorna il valore del codice MAC (Message Authentication Code) con un valore di parametro.                 |
| [**SACAuth**](/previous-versions/ms868516(v=msdn.10))                   | Stabilisce un canale autenticato sicuro tra i componenti.                              |
| [**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))   | Segnala i protocolli supportati da un componente.                                             |
| [**SetCertificate**](/previous-versions/ms868518(v=msdn.10))     | Specifica il certificato e la chiave privata del server SAC (Secure Authenticated Channel). |
| [**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))       | Imposta la chiave della sessione utilizzata per comunicare con un altro componente.                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CSecureChannelClient**](csecurechannelclient-class.md)
</dt> <dt>

[**Interfaccia IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfacce per i provider di servizi**](interfaces-for-service-providers.md)
</dt> <dt>

[**Uso di canali con autenticazione sicura**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 