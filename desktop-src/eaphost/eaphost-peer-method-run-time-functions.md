---
title: Funzioni di Run-Time peer EAPHost
description: Informazioni sulle funzioni di run-time dell'API del metodo peer EAPHost. Vedere un elenco di funzioni e visualizzare altre risorse disponibili.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3134a2b118b4bce4511e79d8d9ef58708f6b1c2bd7a93ed820fc16ec073914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275024"
---
# <a name="eaphost-peer-method-run-time-functions"></a>Funzioni di Run-Time peer EAPHost

Le funzioni di run-time dell'API del metodo peer EAP sono le seguenti.



| Funzione                                                                   | Descrizione                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Avvia una nuova sessione di autenticazione nel peer EAPHost.                                                                                                                                                                    |
| [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Termina una sessione di autenticazione EAP corrente tra EAPHost e il peer.                                                                                                                                               |
| [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Consente agli sviluppatori di metodi EAP di fornire le varie proprietà di connessione e le proprietà utente supportate dal metodo . EAPHost richiama questa funzione per creare la proprietà di connessione e la proprietà utente del metodo EAP. |
| [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Ottiene l'identità per il metodo EAP che chiama .                                                                                                                                                                    |
| [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Ottiene un set di puntatori a funzione per un'implementazione del metodo peer EAP caricato.                                                                                                                                     |
| [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Ottiene una matrice di attributi EAP dal metodo EAP.                                                                                                                                                                     |
| [**EapPeerGetResponsePacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Ottiene un pacchetto di risposta dal metodo EAP.                                                                                                                                                                              |
| [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Ottiene il risultato di una sessione di autenticazione dal metodo EAP.                                                                                                                                                        |
| [**EapPeerGetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Ottiene il contesto dell'interfaccia utente dal metodo EAP.                                                                                                                                                                     |
| [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Inizializza EAPHost per il metodo peer.                                                                                                                                                                                    |
| [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Elabora un pacchetto ricevuto da EAPHost da un supplicante.                                                                                                                                                                   |
| [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Fornisce credenziali utente nuove o aggiornate al metodo EAP.                                                                                                                                                                 |
| [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Fornisce una matrice aggiornata di attributi EAP al metodo EAP.                                                                                                                                                              |
| [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Fornisce un contesto dell'interfaccia utente al metodo EAP.                                                                                                                                                                        |
| [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Arresta il metodo EAP e si prepara a scaricare la DLL corrispondente.                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di configurazione del metodo peer EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




