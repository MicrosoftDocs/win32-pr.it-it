---
description: TAPI risponde alle modifiche apportate ai dispositivi, ad esempio un telefono che ha avviato la suoneria o un modem che è stato rimosso mediante l'attivazione di eventi del dispositivo.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: Eventi dispositivo (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f5508e74424a13117facc1c4c370144ecd46de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751626"
---
# <a name="device-events-telephony-api"></a>Eventi dispositivo (API di telefonia)

TAPI risponde alle modifiche apportate ai dispositivi, ad esempio un telefono che ha avviato la suoneria o un modem che è stato rimosso mediante l'attivazione di eventi del dispositivo. Un'applicazione TAPI deve rispondere a un evento del dispositivo eseguendo una query per la modifica specifica che si è verificata e quindi intraprendendo un'azione appropriata. Un'applicazione può schermare gli eventi che riceveranno tramite la [notifica degli eventi](event-notification.md).

**TAPI 2. x:** Le applicazioni ricevono la notifica degli eventi del dispositivo usando il messaggio di [**riga \_ LINEDEVSTATE**](./line-linedevstate.md) . Lo stato corrente di un indirizzo viene determinato chiamando [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), che restituisce le informazioni in una struttura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) . Lo stato di un dispositivo a linee aperte specificato viene ottenuto chiamando [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), che restituisce le informazioni in una struttura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) .

**TAPI 3. x:** Le applicazioni ricevono una notifica degli [**\_ eventi di indirizzo**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) , che viene elaborata tramite l'interfaccia [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) . Il [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) può quindi essere usato per ottenere informazioni più dettagliate.

 

 
