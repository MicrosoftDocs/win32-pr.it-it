---
description: L'azione RemoveDuplicateFiles elimina i file installati dall'azione DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Azione RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7527e7bd4dc66fe4d57f8c23654f1138e781a33064fc0a4a2694987c7ccdb66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074621"
---
# <a name="removeduplicatefiles-action"></a>Azione RemoveDuplicateFiles

L'azione RemoveDuplicateFiles elimina i file installati [dall'azione DuplicateFiles.](duplicatefiles-action.md)

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione RemoveDuplicateFiles deve essere eseguita dopo [l'azione InstallValidate](installvalidate-action.md) e prima [dell'azione InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                    |
|-------|-----------------------------------------------|
| \[1\] | Identificatore del file rimosso.                   |
| \[9\] | Identificatore della directory contenente il file rimosso. |



 

## <a name="remarks"></a>Commenti

Per eliminare un file duplicato con l'azione [DuplicateFiles](duplicatefiles-action.md) usando l'azione RemoveDuplicateFiles, è necessario selezionare il componente associato alla voce del file nella tabella DuplicateFile per la rimozione.

Usare la colonna DestFolder della tabella [DuplicateFile per](duplicatefile-table.md) specificare il nome della proprietà il cui valore identifica la cartella di destinazione.

 

 



