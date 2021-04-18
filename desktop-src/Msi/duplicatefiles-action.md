---
description: L'azione DuplicateFiles duplica i file installati dall'azione InstallFiles. I file duplicati possono essere copiati nella stessa directory con un nome diverso o in una directory diversa con il nome originale.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Azione DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313353"
---
# <a name="duplicatefiles-action"></a>Azione DuplicateFiles

L'azione DuplicateFiles duplica i file installati dall'azione [InstallFiles](installfiles-action.md) . I file duplicati possono essere copiati nella stessa directory con un nome diverso o in una directory diversa con il nome originale.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione DuplicateFiles deve essere successiva all' [azione InstallFiles](installfiles-action.md). L'azione DuplicateFiles deve anche essere successiva all' [azione PatchFiles](patchfiles-action.md) per impedire la duplicazione della versione senza patch del file.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                       |
|-------|--------------------------------------------------|
| \[1\] | Identificatore del file duplicato.                   |
| \[6\] | Dimensioni del file duplicato.                         |
| \[9\] | Identificatore della directory che contiene il file duplicato. |



 

## <a name="remarks"></a>Commenti

L'azione DuplicateFiles elabora una voce di [tabella DuplicateFile](duplicatefile-table.md) solo se il componente collegato a tale voce viene installato localmente. Per altre informazioni, vedere [tabella dei componenti](component-table.md).

La stringa nel campo DestFolder è un nome di proprietà il cui valore è previsto per la risoluzione in un percorso completo. Questa proprietà può essere qualsiasi voce di directory della tabella di [directory](directory-table.md) , qualsiasi proprietà di cartella predefinita ([**CommonFilesFolder**](commonfilesfolder.md), ad esempio) o una proprietà impostata da qualsiasi voce nella tabella [AppSearch](appsearch-table.md) . Se la proprietà **DestFolder** non restituisce un percorso valido, l'azione DuplicateFiles non esegue alcuna operazione per tale voce.

Se il nome del file di destinazione nella colonna destName della tabella DuplicateFile viene lasciato vuoto, il nome del file di destinazione sarà uguale al nome del file originale.

I file installati dall'azione DuplicateFiles vengono rimossi dall'azione [RemoveDuplicateFiles](removeduplicatefiles-action.md) quando appropriato.

 

 



