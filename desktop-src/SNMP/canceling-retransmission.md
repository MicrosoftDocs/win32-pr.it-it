---
title: Annullamento della ritrasmissione
description: Se non è presente alcuna risposta a una richiesta di comunicazione entro il periodo di timeout specificato per un'entità di destinazione e se vengono specificate ritrasmissioni per l'entità, l'implementazione di Microsoft WinSNMP ritrasmette la richiesta.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044708"
---
# <a name="canceling-retransmission"></a>Annullamento della ritrasmissione

Se non è presente alcuna risposta a una richiesta di comunicazione entro il periodo di timeout specificato per un'entità di destinazione e se vengono specificate ritrasmissioni per l'entità, l'implementazione di Microsoft WinSNMP ritrasmette la richiesta. Una chiamata alla funzione [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) può annullare questo ciclo di ritrasmissione e rilasciare le strutture di dati interne associate alla richiesta del messaggio.

Si noti che è possibile che un'entità di destinazione riceva un messaggio SNMP che è stato annullato da una chiamata alla funzione [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) . È inoltre possibile che un'entità di destinazione possa rispondere a un messaggio SNMP annullato. Questo perché l'accodamento delle transazioni avviene a più livelli. Tuttavia, dopo che un messaggio è stato annullato da una chiamata a [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), l'implementazione di Microsoft WinSNMP non ritrasmette il messaggio, invierà una risposta PDU o invierà una notifica di timeout all'applicazione per quel messaggio.

 

 




