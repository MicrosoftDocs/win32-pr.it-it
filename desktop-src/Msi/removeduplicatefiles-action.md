---
description: L'azione RemoveDuplicateFiles Elimina i file installati dall'azione DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Azione RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751122"
---
# <a name="removeduplicatefiles-action"></a>Azione RemoveDuplicateFiles

L'azione RemoveDuplicateFiles Elimina i file installati dall'azione [DuplicateFiles](duplicatefiles-action.md) .

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RemoveDuplicateFiles deve essere eseguita dopo l'azione [InstallValidate](installvalidate-action.md) e prima dell'azione [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                    |
|-------|-----------------------------------------------|
| \[1\] | Identificatore del file rimosso.                   |
| \[9\] | Identificatore della directory che contiene il file rimosso. |



 

## <a name="remarks"></a>Commenti

Per eliminare un file duplicato con l' [azione DuplicateFiles](duplicatefiles-action.md) usando l'azione RemoveDuplicateFiles, è necessario selezionare per la rimozione il componente associato alla voce del file nella tabella DuplicateFile.

Utilizzare la colonna DestFolder della [tabella DuplicateFile](duplicatefile-table.md) per specificare il nome della proprietà il cui valore identifica la cartella di destinazione.

 

 



