---
description: TAPI risponde alle modifiche del dispositivo, ad esempio un telefono che ha iniziato a circolare o un modem che è stato rimosso generando eventi del dispositivo.
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: Eventi del dispositivo (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59252bddee9697ac453e8e6883c8724e4bc2b22a8a6fb245855bd493821808b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867417"
---
# <a name="device-events-telephony-api"></a>Eventi del dispositivo (API di telefonia)

TAPI risponde alle modifiche del dispositivo, ad esempio un telefono che ha iniziato a circolare o un modem che è stato rimosso generando eventi del dispositivo. Un'applicazione TAPI deve rispondere a un evento del dispositivo cercando la modifica specifica che si è verificata e quindi esegue l'azione appropriata. Un'applicazione può cercare gli eventi che riceverà usando la [notifica degli eventi](event-notification.md).

**TAPI 2.x:** Le applicazioni ricevono la notifica degli eventi del dispositivo usando [**il \_ messaggio LINE LINEDEVSTATE.**](./line-linedevstate.md) Lo stato corrente di un indirizzo viene determinato chiamando [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), che restituisce le informazioni in una [**struttura LINEADDRESSSTATUS.**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) Lo stato di un dispositivo open line specificato viene ottenuto chiamando [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), che restituisce le informazioni in una [**struttura LINEDEVSTATUS.**](/windows/win32/api/tapi/ns-tapi-linedevstatus)

**TAPI 3.x:** Le applicazioni ricevono [**una notifica ADDRESS \_ EVENT,**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) che viene elaborata usando [**l'interfaccia ITAddressEvent.**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) può quindi essere usato per acquisire informazioni più dettagliate.

 

 
