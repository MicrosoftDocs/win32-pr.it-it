---
description: Esistono tre funzioni principali per lo stato della stazione che devono controllare le luci di attesa dei messaggi, l'inoltro e la non disturbo.
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: Controllo stato stazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e136450dbda8cec260a460f49ce8d45b65d1b58ec588ccbcc435c5e3a2b1cd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861934"
---
# <a name="station-status-control"></a>Controllo stato stazione

Sono disponibili tre funzioni principali per lo stato della stazione che necessitano di controllo: Message Waiting lights (Luci di attesa messaggi), Forwarding (Inoltro) e Do Not Disturb (Non disturbare). Forwarding e Do Not Disturb sono controllabili tramite la funzione [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) esistente (specifica dell'indirizzo) ed è possibile eseguire query usando [**lineGetAddressStatus.**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) Il bit LINEDEVSTATUSFLAGS \_ MSGWAIT nel membro **dwDevStatusFlags** di [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) indica lo stato del messaggio in attesa sul dispositivo e viene inviato un messaggio LINEDEVSTATE \_ MSGWAITON o LINEDEVSTATE MSGWAITOFF per indicare quando lo stato \_ cambia. La [**funzione lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) consente di controllare la luce di attesa del messaggio senza dover implementare un dispositivo telefonico TAPI solo a tale scopo. Il bit LINEFEATURE \_ SETDEVSTATUS (nel membro **dwLineFeatures** di [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) e **LINEDEVSTATUS**) indica quando può essere chiamato e il membro **dwSettableDevStatus** di **LINEDEVCAPS** consente all'applicazione di rilevare quali impostazioni di stato del dispositivo possono essere controllate dall'applicazione. Oltre a consentire il controllo della funzionalità di attesa dei messaggi, consente anche di impostare lo stato Connesso, In servizio e Bloccato del dispositivo, nella misura in cui sono supportati dal commutatore o da altro hardware. Le chiamate a questa funzione comportano l'invio di messaggi [**\_ LINEDEVSTATE**](line-linedevstate.md) appropriati per riflettere il nuovo stato.

 

 



