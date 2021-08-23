---
title: Spazio dei nomi
description: Uno spazio dei nomi è un contesto in cui i nomi di tutti gli oggetti devono essere risolvibili in modo inequivocabile.
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce9119b49cde888cb51f65e6e6b677fb364d640e1b78fe48c739b7c1206936d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692201"
---
# <a name="namespace"></a>Spazio dei nomi

Uno spazio dei nomi è un contesto in cui i nomi di tutti gli oggetti devono essere risolvibili in modo inequivocabile. Ad esempio, Internet è un singolo spazio dei nomi DNS, all'interno del quale tutti i dispositivi di rete con un nome DNS possono essere risolti in un indirizzo specifico (ad esempio, si risolve `www.microsoft.com` in 207.46.131.13).

## <a name="flat-namespace"></a>Spazio dei nomi flat

Uno spazio dei nomi può essere flat o gerarchico. Uno spazio dei nomi flat non viene ridimensionato bene perché può aumentare solo in modo così grande prima che tutti i nomi disponibili siano usati. Quando un nome viene usato più di una volta in uno spazio dei nomi, lo spazio dei nomi viola il requisito risolvibile in modo non ambiguo.

## <a name="hierarchical-namespace"></a>Spazio dei nomi gerarchico

Uno spazio dei nomi gerarchico è suddiviso in aree diverse, che possono essere ritenute come spazi dei nomi secondari. Ogni area è il proprio sotto-spazio dei nomi all'interno dello spazio dei nomi complessivo. Pertanto, ogni oggetto deve avere un nome univoco solo all'interno del relativo spazio dei nomi secondario per avere un nome risolvibile in modo non ambiguo all'interno della gerarchia dello spazio dei nomi. Gli spazi dei nomi gerarchici possono quindi essere ridimensionati in reti di dimensioni estremamente grandi quando si aggiungono altri oggetti allo spazio dei nomi complessivo. È quindi necessario trovare nomi univoci all'interno solo dello spazio dei nomi secondario a cui &mdash; appartengono.

Tutti gli spazi dei nomi DNS sono gerarchici. Gli spazi dei nomi secondari nello spazio dei nomi gerarchico DNS sono denominati *domini*. Il nome univoco di un computer all'interno di un dominio è denominato *nome distinto relativo*. I computer con lo stesso nome distinto relativo possono esistere in diversi sottonodi (domini) della gerarchia degli spazi dei nomi perché possono essere risolti completamente in un oggetto univoco all'interno dell'intera gerarchia DNS, usando un nome di dominio completo (FQDN). Ad esempio, è possibile avere un server denominato *server1* nel dominio *widgets.microsoft.com* (lo spazio dei nomi *widgets.microsoft.com)* e *server1* nello spazio dei nomi *gadgets.widgets.microsoft.com.* Poiché si tratta di spazi dei nomi secondari diversi nello spazio dei nomi gerarchico, possono essere risolti in fqdn diversi server1.widgets.microsoft.com &mdash;  e *server1.gadgets.widgets.microsoft.com*.
