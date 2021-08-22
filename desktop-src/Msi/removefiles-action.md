---
description: L'azione RemoveFiles rimuove i file installati in precedenza dall'azione InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Azione RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50e23a7d2eb3c9bb23575d83d000b053f0de06907541777e43b5476f8c722ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626451"
---
# <a name="removefiles-action"></a>Azione RemoveFiles

L'azione RemoveFiles rimuove i file installati in precedenza [dall'azione InstallFiles.](installfiles-action.md) Ognuno di questi file è reciso da un collegamento a una voce nella [tabella](component-table.md) Componente. Vengono rimossi solo i file con componenti risolti nello stato *msiInstallStateAbsent* o *msiInstallStateLocal* se il componente è installato in locale.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

[L'azione InstallValidate](installvalidate-action.md) deve essere chiamata prima di chiamare RemoveFiles. Se si [usa un'azione InstallFiles,](installfiles-action.md) deve essere visualizzata dopo RemoveFiles.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                    |
|-------|-----------------------------------------------|
| \[1\] | Identificatore del file rimosso.                   |
| \[9\] | Identificatore della directory contenente il file rimosso. |



 

## <a name="remarks"></a>Commenti

La [tabella RemoveFile](removefile-table.md) può essere omessa dal database del programma di installazione se non sono presenti file esterni da rimuovere.

L'azione RemoveFiles può anche rimuovere i file specificati dall'autore che non vengono installati dall'azione InstallFiles. Questi file vengono specificati nella [tabella RemoveFile.](removefile-table.md) Ognuno di questi file è reciso da un collegamento a una voce nella [tabella](component-table.md) Componente. Se il file esiste nella directory specificata, i file i cui componenti vengono risolti in uno stato Azione attivo, ovvero non nello stato Disattivato o Null, vengono rimossi. La rimozione dei file specificati nella tabella RemoveFile viene tentata quando il componente collegato viene installato per la prima volta, durante una reinstallazione e di nuovo quando il componente collegato viene rimosso.

L'azione RemoveFiles può anche rimuovere le cartelle. Se il valore nella colonna FileName della tabella RemoveFile è Null, viene rimossa una cartella vuota.

Quando si rimuovono file installati in precedenza, l'azione RemoveFiles esegue una query negli stessi campi nelle stesse tabelle di quelle su cui viene eseguita una query tramite l'azione [InstallFiles,](installfiles-action.md) ad eccezione del fatto che la tabella [Media](media-table.md) non viene usata dall'azione RemoveFiles.

Il nome del file di destinazione può essere specificato nel testo localizzato nella colonna FileName della tabella RemoveFile.

 

 



