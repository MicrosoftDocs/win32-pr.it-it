---
description: "È possibile fare riferimento a cluster da due diverse prospettive: all'interno del file e nel volume."
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Cluster ed extent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312940"
---
# <a name="clusters-and-extents"></a>Cluster ed extent

È possibile fare riferimento a cluster da due diverse prospettive: all'interno del file e nel volume. Qualsiasi cluster in un file ha un *numero di cluster virtuale* (VCN), ovvero il relativo offset rispetto all'inizio del file. Ad esempio, una ricerca a due volte la dimensione di un cluster, seguita da un'operazione di lettura, restituirà i dati a partire dalla terza VCN. Un *numero di cluster logico* (LCN) descrive l'offset di un cluster da un punto arbitrario all'interno del volume. LCNs deve essere trattato solo come numeri ordinali o relativi. Non esiste un mapping garantito dei cluster logici ai settori di unità disco rigido fisico.

Un *extent* è un'esecuzione di cluster contigui. Si supponga, ad esempio, che un file costituito da 30 cluster venga registrato in due extent. Il primo extent può essere costituito da cinque cluster contigui, l'altro dei 25 cluster rimanenti.

Non esiste alcuna garanzia di alcuna relazione sul disco di qualsiasi extent con qualsiasi altro extent. Il primo extent, ad esempio, può essere a una LCN superiore rispetto a un extent successivo.

 

 



