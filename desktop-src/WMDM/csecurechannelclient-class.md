---
title: Classe CSecureChannelClient
description: Classe CSecureChannelClient
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Gestione dispositivi multimediali, classe CSecureChannelClient
- Gestione dispositivi, classe CSecureChannelClient
- applicazioni desktop, classe CSecureChannelClient
- informazioni di riferimento sulla programmazione, classe CSecureChannelClient
- informazioni di riferimento Windows Gestione dispositivi multimediali, classe CSecureChannelClient
- Classe CSecureChannelClient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef469c1e7a73b04124850952ef0690bd18c82ecb3fc624d08df081b7b669637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585614"
---
# <a name="csecurechannelclient-class"></a>Classe CSecureChannelClient

La **classe CSecureChannelClient** è una classe helper (non un'interfaccia) che consente alle applicazioni di autenticarsi, crittografare e decrittografare i dati e creare macs.

La **classe CSecureChannelClient** espone i metodi seguenti.



| Metodo                                                            | Descrizione                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Autenticare**](/previous-versions/ms983906(v=msdn.10))         | Attiva lo scambio di certificati tra i componenti per stabilire l'attendibilità.                                              |
| [**DecryptParam**](/previous-versions/bb231586(v=vs.85))         | Decrittografa i dati ricevuti tramite un parametro.                                                                               |
| [**EncryptParam**](/previous-versions/bb231587(v=vs.85))         | Crittografa i dati inviati tramite un parametro.                                                                         |
| [**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10)) | Verifica che un canale di autenticazione sicuro sia stato stabilito correttamente. Questo metodo non viene usato dalle applicazioni. |
| [**GetAppSec**](/previous-versions/ms868498(v=msdn.10))               | Recupera i livelli di sicurezza dell'applicazione dei componenti locali e remoti.                                             |
| [**GetSessionKey**](/previous-versions/bb231590(v=vs.85))       | Recupera la chiave di sessione corrente. Questo metodo non viene usato dalle applicazioni.                                               |
| [**MACFinal**](/previous-versions/bb231591(v=vs.85))                 | Rilascia il canale MAC (Message Authentication Code) e recupera un valore MAC finale.                                   |
| [**MACInit**](/previous-versions/bb231592(v=vs.85))                   | Acquisisce un canale MAC (Message Authentication Code).                                                                     |
| [**MACUpdate**](/previous-versions/bb231593(v=vs.85))               | Aggiunge un valore a un codice mac (Message Authentication Code).                                                                      |
| [**SetCertificate**](/previous-versions/ms868504(v=msdn.10))     | Specifica il certificato e la chiave privata del client SAC (Secure Authenticated Channel).                               |
| [**SetInterface**](/previous-versions/bb231595(v=vs.85))         | Seleziona l'interfaccia usata per le comunicazioni SAC (Secure Authenticated Channel).                                         |
| [**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))       | Imposta la chiave di sessione utilizzata per comunicare con un altro componente. Questo metodo non viene usato dalle applicazioni.         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CSecureChannelServer**](csecurechannelserver-class.md)
</dt> <dt>

[**Interfaccia IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfacce per le applicazioni**](interfaces-for-applications.md)
</dt> </dl>

 

 