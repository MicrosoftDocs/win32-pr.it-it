---
description: L'azione DuplicateFiles duplica i file installati dall'azione InstallFiles. I file duplicati possono essere copiati nella stessa directory con un nome diverso o in una directory diversa con il nome originale.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Azione DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7969440aed4361ad264baa0d30a9c1d16f0ca673c72a2a7c3c1326e5d393ffc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637713"
---
# <a name="duplicatefiles-action"></a>Azione DuplicateFiles

L'azione DuplicateFiles duplica i file installati [dall'azione InstallFiles.](installfiles-action.md) I file duplicati possono essere copiati nella stessa directory con un nome diverso o in una directory diversa con il nome originale.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione DuplicateFiles deve essere eseguita dopo [l'azione InstallFiles](installfiles-action.md). L'azione DuplicateFiles deve essere eseguita anche dopo [l'azione PatchFiles](patchfiles-action.md) per impedire la duplicazione della versione senza patch del file.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                       |
|-------|--------------------------------------------------|
| \[1\] | Identificatore del file duplicato.                   |
| \[6\] | Dimensioni del file duplicato.                         |
| \[9\] | Identificatore della directory contenente il file duplicato. |



 

## <a name="remarks"></a>Commenti

L'azione DuplicateFiles elabora una voce di tabella [DuplicateFile](duplicatefile-table.md) solo se il componente collegato a tale voce viene installato in locale. Per altre informazioni, vedere [Tabella dei componenti](component-table.md).

La stringa nel campo DestFolder è un nome di proprietà il cui valore deve essere risolto in un percorso completo. Questa proprietà può essere una delle voci di directory nella tabella [Directory,](directory-table.md) qualsiasi proprietà di cartella predefinita ([**CommonFilesFolder**](commonfilesfolder.md), ad esempio) o una proprietà impostata da qualsiasi voce nella [tabella AppSearch.](appsearch-table.md) Se la **proprietà DestFolder** non restituisce un percorso valido, l'azione DuplicateFiles non esegue alcuna operazione per tale voce.

Se il nome del file di destinazione nella colonna DestName della tabella DuplicateFile viene lasciato vuoto, il nome del file di destinazione sarà lo stesso del nome del file originale.

I file installati dall'azione DuplicateFiles vengono rimossi [dall'azione RemoveDuplicateFiles](removeduplicatefiles-action.md) quando appropriato.

 

 



