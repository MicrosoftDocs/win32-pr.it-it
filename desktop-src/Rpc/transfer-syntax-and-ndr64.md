---
title: Sintassi transfer e NDR64
description: Il protocollo di collegamento NDR, noto anche come sintassi di trasferimento, consente alle chiamate RPC di attraversare la rete.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046781"
---
# <a name="transfer-syntax-and-ndr64"></a>Sintassi transfer e NDR64

Il protocollo di collegamento NDR, noto anche come sintassi di trasferimento, consente alle chiamate RPC di attraversare la rete. Il protocollo wire definisce la rappresentazione in transito di una chiamata RPC, ad esempio l'ordine in cui i membri dati vengono sottoposti a marshalling, l'allineamento dei dati in transito, informazioni aggiuntive incluse con i dati e altri problemi. Il protocollo NDR64 è un'estensione della sintassi di trasferimento NDR basato su 32 bit, creata appositamente per consentire agli sviluppatori di utilizzare sistemi a 64 bit per ottenere prestazioni ottimizzate.

Le differenze tra il formato wire NDR e il formato wire NDR64 sono le diverse dimensioni dei puntatori in un ambiente a 64 bit, oltre ad altri problemi. Il meccanismo di NDR64 è gestito da RPC. Gli sviluppatori devono usare solo l'opzione della riga di comando per **tutti** i [**protocolli**](/windows/desktop/Midl/-protocol)MIDL per ottenere i vantaggi di NDR64 su piattaforme a 64 bit. NDR64 è disponibile solo su piattaforme a 64 bit.

 

 