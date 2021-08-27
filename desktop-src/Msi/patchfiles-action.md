---
description: L'azione PatchFiles esegue una query nella tabella Patch per determinare le patch da applicare. L'azione PatchFiles esegue anche l'applicazione di patch per byte dei file.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Azione PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6186f150df1871e424b1dc6e4f466d148a1ce2ed51ffd9cd8170a1221e2f0b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082671"
---
# <a name="patchfiles-action"></a>Azione PatchFiles

L'azione PatchFiles esegue una query [nella tabella Patch](patch-table.md) per determinare le patch da applicare. L'azione PatchFiles esegue anche l'applicazione di patch per byte dei file.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

Se il file da applicare a patch non è installato, l'azione PatchFiles deve essere eseguita dopo l'azione [InstallFiles](installfiles-action.md) che installa il file. I file installati in precedenza possono essere patchati in qualsiasi punto della sequenza di azione. [L'azione DuplicateFiles](duplicatefiles-action.md) deve essere eseguita dopo l'azione PatchFiles per impedire la duplicazione della versione senza patch del file.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                    |
|-------|-----------------------------------------------|
| \[1\] | Identificatore del file con patch.                   |
| \[2\] | Identificatore della directory contenente il file con patch. |
| \[3\] | Dimensioni della patch in byte.                       |



 

 

 



