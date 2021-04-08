---
description: L'azione PatchFiles esegue una query sulla tabella patch per individuare le patch da applicare. L'azione PatchFiles esegue anche l'applicazione di patch per byte dei file.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Azione PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881857"
---
# <a name="patchfiles-action"></a>Azione PatchFiles

L'azione PatchFiles esegue una query sulla [tabella patch](patch-table.md) per individuare le patch da applicare. L'azione PatchFiles esegue anche l'applicazione di patch per byte dei file.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Se il file di cui eseguire la patch non è installato, l'azione PatchFiles deve provenire dopo l' [azione InstallFiles](installfiles-action.md) che installa il file. I file installati in precedenza possono essere corretti in qualsiasi punto della sequenza di azione. L' [azione DuplicateFiles](duplicatefiles-action.md) deve essere successiva all'azione PatchFiles per impedire la duplicazione della versione senza patch del file.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                    |
|-------|-----------------------------------------------|
| \[1\] | Identificatore del file con patch.                   |
| \[2\] | Identificatore della directory contenente il file con patch. |
| \[3\] | Dimensioni in byte della patch.                       |



 

 

 



