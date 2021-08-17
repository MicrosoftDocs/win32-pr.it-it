---
title: Sintassi di trasferimento e NDR64
description: Il protocollo di collegamento NDR, detto anche sintassi di trasferimento, consente alle chiamate RPC di attraversare la rete.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433e68689ec4c960adbb43ddc19ec3e9e37765db57cfe6bf87c86c096720b771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011229"
---
# <a name="transfer-syntax-and-ndr64"></a>Sintassi di trasferimento e NDR64

Il protocollo di collegamento NDR, detto anche sintassi di trasferimento, consente alle chiamate RPC di attraversare la rete. Il protocollo wire definisce la rappresentazione cablata di una chiamata RPC, ad esempio l'ordine in cui viene effettuato il marshalling dei membri dati, l'allineamento dei dati in transito, informazioni aggiuntive incluse con i dati e altri problemi. Il protocollo NDR64 è un'estensione della sintassi di trasferimento NDR basata su 32 bit, creata in modo specifico per consentire agli sviluppatori che hanno come destinazione sistemi a 64 bit di ottenere prestazioni ottimizzate.

Le differenze tra il formato di collegamento NDR e il formato di collegamento NDR64 risolve le diverse dimensioni dei puntatori in un ambiente a 64 bit, nonché altri problemi. I meccanismi di NDR64 vengono gestiti da RPC. Gli sviluppatori devono usare solo l'opzione della riga di comando [**/protocol**](/windows/desktop/Midl/-protocol)all **MIDL** per ottenere i vantaggi di NDR64 su piattaforme a 64 bit. NDR64 è disponibile solo nelle piattaforme a 64 bit.

 

 