---
description: Gli autori devono eseguire la convalida in ogni modulo unione nuovo o modificato prima di tentare di unire il modulo in un database di installazione per la prima volta.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Convalida dei moduli unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5a226f72e35ce4ee76599444e86ef80bd71a8866ca80eef2a5da04a87fb79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995800"
---
# <a name="validating-merge-modules"></a>Convalida dei moduli unione

Gli autori devono eseguire la convalida in ogni modulo unione nuovo o modificato prima di tentare di unire il modulo in un database di installazione per la prima volta. La convalida dei moduli di [](package-validation.md) merge funziona come la convalida dei pacchetti, ma usa un set diverso di analizzatori di coerenza [interna](internal-consistency-evaluators-ices.md) specifici per i moduli di merge. Per altre informazioni su queste ICE del modulo di merge, vedere [Merge Module ICE Reference](merge-module-ice-reference.md).

Le ICE del modulo unione vengono archiviate nel file con estensione cub del modulo unione Mergemod.cub. L'installazione dello strumento Orca o msival2 fornisce anche i file Logo.cub, Darice.cub e Mergemod.cub.

Per altre informazioni, vedere [Informazioni di riferimento su ICE del modulo di merge](merge-module-ice-reference.md).

 

 



