---
title: Funzioni Run-Time supplicant EAPHost
description: Informazioni sulle funzioni di run-time supplicant EAPHost, ad esempio EapHostPeerBeginSession ed EapHostPeerGetResult.
ms.assetid: b1c473ba-9a12-4929-b4d0-27262117e9c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97481347535de03cb1d3c04f341f382c270f0ae89482060e9952c38cfbdc5b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785329"
---
# <a name="eaphost-supplicant-run-time-functions"></a>Funzioni Run-Time supplicant EAPHost

Le funzioni di run-time dell'API Supplicant EAP sono le seguenti.



| Funzione                                                                     | Descrizione                                                                                                                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                   | Avvia una sessione di autenticazione EAP.                                                                                                                                                                                |
| [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection)             | Arresta tutti i callback futuri a [**NotificationHandler**](/previous-versions/windows/desktop/api) forniti dal supplicant chiamante a EAPHost in una chiamata precedente a [**EapHostPeerBeginSession.**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) |
| [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)                       | Termina una sessione di autenticazione EAP corrente tra EAPHost e il supplicant chiamante.                                                                                                                          |
| [**EapHostPeerFreeEapError**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror)                   | Libera tutta la memoria specifica degli errori EAP restituita dalle API EAPHost.                                                                                                                                                        |
| [**EapHostFreeRuntimeMemory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory)                    | Rilascia lo spazio di memoria usato dalle API di run-time.                                                                                                                                                                         |
| [**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)                 | Ottiene lo stato di autenticazione EAP corrente del supplicant da EAPHost.                                                                                                                                             |
| [**EapHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity)                     | Richiede informazioni sull'identità dai metodi interni.                                                                                                                                                                |
| [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) | Ottiene una matrice di attributi di autenticazione EAP da EAPHost.                                                                                                                                                      |
| [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)                         | Ottiene il risultato dell'autenticazione per la sessione di autenticazione EAP specificata.                                                                                                                                      |
| [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket)                 | Ottiene un pacchetto da EAPHost da inviare all'autenticatore.                                                                                                                                                          |
| [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)                   | Ottiene il contesto dell'interfaccia utente per il supplicant da EAPHost usato nelle API [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) per il supplicant.                             |
| [**EapHostPeerInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize)                       | Inizializza EAPHost per il supplicant. [**EapHostInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) ed [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) devono essere chiamati come coppia.                                      |
| [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) | Trasferisce il pacchetto EAP a EAPHost dopo aver ricevuto un pacchetto EAP dal server.                                                                                                                             |
| [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) | Fornisce attributi di autenticazione EAP aggiornati a EAPHost.                                                                                                                                                           |
| [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext)                   | Fornisce un contesto dell'interfaccia utente nuovo o aggiornato al metodo peer EAP caricato in EAPHost.                                                                                                                           |
| [**EapHostPeerUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize)                   | Unitizza EapHost per il supplicant. [**EapHostInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) ed [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) devono essere chiamati come coppia.                                      |



 

 

 




