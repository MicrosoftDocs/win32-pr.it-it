---
description: "È possibile fare riferimento ai cluster da due prospettive diverse: all'interno del file e del volume."
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Cluster ed extent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce987dc5c8afea842d6c92196474f88d17c36d2011995a2d760b83bfc1e5a644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533841"
---
# <a name="clusters-and-extents"></a>Cluster ed extent

È possibile fare riferimento ai cluster da due prospettive diverse: all'interno del file e del volume. Qualsiasi cluster in un file ha un *numero di cluster* virtuale (VCN), che è l'offset relativo dall'inizio del file. Ad esempio, una ricerca di due volte le dimensioni di un cluster, seguita da una lettura, restituirà i dati a partire dal terzo VCN. Un *numero di cluster logico* (LCN) descrive l'offset di un cluster da un punto arbitrario all'interno del volume. Le reti LCN devono essere considerate solo numeri ordinali o relativi. Non è garantito il mapping dei cluster logici ai settori delle unità disco rigido fisiche.

Un *extent* è un'esecuzione di cluster contigui. Si supponga, ad esempio, che un file costituito da 30 cluster sia registrato in due extent. Il primo extent può essere costituito da cinque cluster contigui, l'altro dei 25 cluster rimanenti.

Non c'è alcuna garanzia di alcuna relazione sul disco in alcun altro ambito. Ad esempio, il primo extent può essere a un LCN superiore rispetto a un extent successivo.

 

 



