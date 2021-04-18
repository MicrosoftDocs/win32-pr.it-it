---
title: Spazio dei nomi
description: Uno spazio dei nomi è un contesto in cui i nomi di tutti gli oggetti devono essere risolvibili in modo non ambiguo.
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb79ba44bfaab1ea50dd89961503176dc8fbd1a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322011"
---
# <a name="namespace"></a>Spazio dei nomi

Uno spazio dei nomi è un contesto in cui i nomi di tutti gli oggetti devono essere risolvibili in modo non ambiguo. Ad esempio, Internet è un singolo spazio dei nomi DNS, all'interno del quale è possibile risolvere tutti i dispositivi di rete con un nome DNS in un indirizzo specifico (ad esempio, si `www.microsoft.com` risolve in 207.46.131.13).

## <a name="flat-namespace"></a>Spazio dei nomi flat

Uno spazio dei nomi può essere semplice o gerarchico. Uno spazio dei nomi flat non è scalabile correttamente perché può raggiungere dimensioni elevate prima che tutti i nomi disponibili siano utilizzati. Quando un nome viene usato più di una volta in uno spazio dei nomi, lo spazio dei nomi viola il requisito non ambiguamente risolvibile.

## <a name="hierarchical-namespace"></a>Spazio dei nomi gerarchico

Uno spazio dei nomi gerarchico è suddiviso in aree diverse, che possono essere considerate come spazi dei nomi secondari. Ogni area è il proprio spazio dei nomi secondario nello spazio dei nomi globale. Ogni oggetto deve pertanto avere un nome univoco solo all'interno dello spazio dei nomi secondario per avere un nome risolvibile in modo non ambiguo all'interno della gerarchia dello spazio dei nomi. Gli spazi dei nomi gerarchici, quindi, possono essere ridimensionati a reti estremamente grandi &mdash; quando si aggiungono più oggetti allo spazio dei nomi globale, è necessario trovare nomi univoci solo all'interno dello spazio dei nomi secondario a cui appartengono.

Tutti gli spazi dei nomi DNS sono gerarchici. Gli spazi dei nomi secondari nello spazio dei nomi gerarchico DNS sono denominati *domini*. Il nome univoco di un computer all'interno di un dominio viene definito *nome distinto relativo*. I computer con lo stesso nome distinto relativo possono esistere in sottospazi dei nomi (domini) diversi della gerarchia dello spazio dei nomi perché possono essere risolti completamente in un oggetto univoco all'interno dell'intera gerarchia DNS, usando un nome di dominio completo (FQDN). Ad esempio, è possibile avere un server denominato *Server1* nel dominio *widgets.Microsoft.com* (lo spazio dei nomi *widgets.Microsoft.com* ) e *Server1* nello spazio dei nomi *gadgets.widgets.Microsoft.com* . Poiché si trovano in spazi dei nomi secondari diversi nello spazio dei nomi gerarchico, possono essere risolti in FQDN diversi &mdash; *server1.widgets.microsoft.com* e *Server1.gadgets.widgets.Microsoft.com*.
