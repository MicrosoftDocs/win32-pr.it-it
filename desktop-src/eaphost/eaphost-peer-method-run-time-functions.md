---
title: Funzioni di Run-Time del metodo peer EAPHost
description: Informazioni sulle funzioni di runtime dell'API del metodo peer EAPHost. Vedere un elenco di funzioni e visualizzare altre risorse disponibili.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfde4adc8d509fcd5d67f9a33bd0617d605716db
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872954"
---
# <a name="eaphost-peer-method-run-time-functions"></a>Funzioni di Run-Time del metodo peer EAPHost

Di seguito sono riportate le funzioni di Runtime API del metodo peer EAP.



| Funzione                                                                   | Descrizione                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Avvia una nuova sessione di autenticazione nell'EAPHost peer.                                                                                                                                                                    |
| [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Termina una sessione di autenticazione EAP corrente tra EAPHost e il peer.                                                                                                                                               |
| [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Consente agli sviluppatori di metodi EAP di fornire le varie proprietà di connessione e le proprietà utente supportate dal metodo. EAPHost richiama questa funzione per creare la proprietà di connessione e la proprietà utente del metodo EAP. |
| [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Ottiene l'identità per il metodo EAP che sta chiamando.                                                                                                                                                                    |
| [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Ottiene un set di puntatori a funzione per un'implementazione del metodo peer EAP caricato.                                                                                                                                     |
| [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Ottiene una matrice di attributi EAP dal metodo EAP.                                                                                                                                                                     |
| [**EapPeerGetResponsePacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Ottiene un pacchetto di risposta dal metodo EAP.                                                                                                                                                                              |
| [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Ottiene il risultato di una sessione di autenticazione dal metodo EAP.                                                                                                                                                        |
| [**EapPeerGetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Ottiene il contesto dell'interfaccia utente dal metodo EAP.                                                                                                                                                                     |
| [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Inizializza EAPHost per il metodo peer.                                                                                                                                                                                    |
| [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Elabora un pacchetto ricevuto da EAPHost da un supplicant.                                                                                                                                                                   |
| [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Fornisce credenziali utente nuove o aggiornate al metodo EAP.                                                                                                                                                                 |
| [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Fornisce una matrice aggiornata di attributi EAP al metodo EAP.                                                                                                                                                              |
| [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Fornisce un contesto dell'interfaccia utente al metodo EAP.                                                                                                                                                                        |
| [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Arresta il metodo EAP e prepara per scaricare la DLL corrispondente.                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di configurazione del metodo peer EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




