---
description: Sono disponibili tre funzioni principali per lo stato della stazione che necessitano di controllare i messaggi di avviso, l'invio e l'inattività.
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: Controllo stato stazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f6ddd1b1ce6df1ad2f3dc61e891ed6952a7f05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311874"
---
# <a name="station-status-control"></a>Controllo stato stazione

Sono disponibili tre funzioni principali per lo stato della stazione che necessitano di controllo: le luci in attesa del messaggio, l'invio e non interferiscono. L'invio e la mancata risoluzione dei disturbi sono controllabili tramite la funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) esistente (specifica dell'indirizzo) e sottoposta a query utilizzando [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). Il \_ bit LINEDEVSTATUSFLAGS MSGWAIT nel membro **DwDevStatusFlags** di [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) indica lo stato della luce in attesa del messaggio sul dispositivo e viene inviato un messaggio LINEDEVSTATE MSGWAITON \_ o LINEDEVSTATE MSGWAITOFF \_ per indicare quando lo stato cambia. La funzione [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) consente il controllo della luce in attesa del messaggio senza che sia necessario implementare un dispositivo telefonico TAPI solo a tale scopo. Il \_ bit LINEFEATURE SETDEVSTATUS (nel membro **DwLineFeatures** di [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) e **LINEDEVSTATUS**) indica quando può essere chiamato e il membro **dwSettableDevStatus** di **LINEDEVCAPS** consente all'applicazione di rilevare le impostazioni dello stato del dispositivo che possono essere controllate dall'applicazione. Oltre a consentire il controllo della funzionalità di attesa dei messaggi, è anche possibile impostare lo stato connesso, inservizio e bloccato del dispositivo, in modo che siano supportati dal Commuter o da un altro hardware. Le chiamate a questa funzione comportano l'invio di messaggi [**\_ LINEDEVSTATE di riga**](line-linedevstate.md) appropriati per riflettere il nuovo stato.

 

 



