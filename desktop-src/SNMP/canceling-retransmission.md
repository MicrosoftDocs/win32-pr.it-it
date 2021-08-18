---
title: Annullamento della ritrasmissione
description: Se non viene inviata alcuna risposta a una richiesta di comunicazione entro il periodo di timeout specificato per un'entità di destinazione e se vengono specificate ritrasmissioni per l'entità, l'implementazione di Microsoft WinSNMP ritrasmette la richiesta.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80770fc741357255adaa8b6bd15ab0e03b9148c37abf5fc631155d74b6d1f3a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009758"
---
# <a name="canceling-retransmission"></a>Annullamento della ritrasmissione

Se non viene inviata alcuna risposta a una richiesta di comunicazione entro il periodo di timeout specificato per un'entità di destinazione e se vengono specificate ritrasmissioni per l'entità, l'implementazione di Microsoft WinSNMP ritrasmette la richiesta. Una chiamata alla funzione [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) può annullare questo ciclo di ritrasmissione e rilasciare strutture di dati interne associate alla richiesta di messaggio.

Si noti che un'entità di destinazione può ricevere un messaggio SNMP annullato da una chiamata alla [**funzione SnmpCancelMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) È anche possibile che un'entità di destinazione possa rispondere a un messaggio SNMP annullato. Ciò è dovuto al fatto che l'accodamento delle transazioni si verifica a più livelli. Tuttavia, dopo che un messaggio è stato annullato da una chiamata a [**SnmpCancelMsg,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)l'implementazione di Microsoft WinSNMP non ritrasmetterà il messaggio, invierà una PDU di risposta o invierà una notifica di timeout all'applicazione per tale messaggio.

 

 




