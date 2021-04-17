---
title: Classe CSecureChannelClient
description: Classe CSecureChannelClient
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Gestione dispositivi, classe CSecureChannelClient
- Gestione dispositivi, classe CSecureChannelClient
- applicazioni desktop, classe CSecureChannelClient
- Guida di riferimento alla programmazione, classe CSecureChannelClient
- informazioni di riferimento su Windows Media Gestione dispositivi, classe CSecureChannelClient
- Classe CSecureChannelClient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299916"
---
# <a name="csecurechannelclient-class"></a>Classe CSecureChannelClient

La classe **CSecureChannelClient** è una classe helper (non un'interfaccia) che consente alle applicazioni di autenticarsi, crittografare e decrittografare i dati e creare i computer Mac.

La classe **CSecureChannelClient** espone i metodi seguenti.



| Metodo                                                            | Descrizione                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Autenticare**](/previous-versions/ms983906(v=msdn.10))         | Attiva lo scambio di certificati tra i componenti per stabilire una relazione di trust.                                              |
| [**DecryptParam**](/previous-versions/bb231586(v=vs.85))         | Consente di decrittografare i dati ricevuti tramite un parametro.                                                                               |
| [**EncryptParam**](/previous-versions/bb231587(v=vs.85))         | Crittografa i dati inviati tramite un parametro.                                                                         |
| [**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10)) | Verifica che sia stato stabilito correttamente un canale di autenticazione protetto. Questo metodo non viene utilizzato dalle applicazioni. |
| [**GetAppSec**](/previous-versions/ms868498(v=msdn.10))               | Recupera i livelli di sicurezza dell'applicazione dei componenti locali e remoti.                                             |
| [**GetSessionKey**](/previous-versions/bb231590(v=vs.85))       | Recupera la chiave della sessione corrente. Questo metodo non viene utilizzato dalle applicazioni.                                               |
| [**MACFinal**](/previous-versions/bb231591(v=vs.85))                 | Rilascia il canale MAC (Message Authentication Code) e recupera un valore MAC finale.                                   |
| [**MACInit**](/previous-versions/bb231592(v=vs.85))                   | Acquisisce un canale MAC (Message Authentication Code).                                                                     |
| [**MACUpdate**](/previous-versions/bb231593(v=vs.85))               | Aggiunge un valore a un codice MAC (Message Authentication Code).                                                                      |
| [**SetCertificate**](/previous-versions/ms868504(v=msdn.10))     | Specifica il certificato e la chiave privata del client del canale autenticato sicuro (SAC).                               |
| [**SetInterface**](/previous-versions/bb231595(v=vs.85))         | Seleziona l'interfaccia utilizzata per le comunicazioni del canale autenticato (SAC) sicuro.                                         |
| [**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))       | Imposta la chiave della sessione utilizzata per comunicare con un altro componente. Questo metodo non viene utilizzato dalle applicazioni.         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CSecureChannelServer**](csecurechannelserver-class.md)
</dt> <dt>

[**Interfaccia IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfacce per le applicazioni**](interfaces-for-applications.md)
</dt> </dl>

 

 