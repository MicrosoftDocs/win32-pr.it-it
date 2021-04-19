---
description: L'azione RemoveFiles rimuove i file precedentemente installati dall'azione InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Azione RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314780"
---
# <a name="removefiles-action"></a>Azione RemoveFiles

L'azione RemoveFiles rimuove i file precedentemente installati dall'azione [InstallFiles](installfiles-action.md) . Ognuno di questi file è gestito da un collegamento a una voce nella tabella dei [componenti](component-table.md) . Solo i file con componenti risolti nello stato *msiInstallStateAbsent* o *msiInstallStateLocal* se il componente è installato localmente, vengono rimossi.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione [InstallValidate](installvalidate-action.md) deve essere chiamata prima di chiamare RemoveFiles. Se viene usata un'azione [InstallFiles](installfiles-action.md) , deve essere visualizzata dopo RemoveFiles.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                    |
|-------|-----------------------------------------------|
| \[1\] | Identificatore del file rimosso.                   |
| \[9\] | Identificatore della directory che contiene il file rimosso. |



 

## <a name="remarks"></a>Commenti

La tabella [RemoveFile](removefile-table.md) può essere omessa dal database del programma di installazione se non sono presenti file esterni da rimuovere.

L'azione RemoveFiles può anche rimuovere i file specificati dall'autore che non sono installati dall'azione InstallFiles. Questi file sono specificati nella tabella [RemoveFile](removefile-table.md) . Ognuno di questi file è gestito da un collegamento a una voce nella tabella dei [componenti](component-table.md) . Se il file è presente nella directory specificata, i file i cui componenti vengono risolti in uno stato di azione attivo (ovvero non in stato disattivato o null) vengono rimossi. La rimozione dei file specificati nella tabella RemoveFile viene tentata quando il componente collegato viene installato per la prima volta, durante una reinstallazione e nuovamente quando il componente collegato viene rimosso.

L'azione RemoveFiles consente inoltre di rimuovere le cartelle. Se il valore nella colonna FileName della tabella RemoveFile è null, viene rimossa una cartella vuota.

Quando si rimuovono i file installati in precedenza, l'azione RemoveFiles esegue una query sugli stessi campi nelle stesse tabelle di quelli sottoposti a query dall'azione [InstallFiles](installfiles-action.md) , con l'eccezione che la [tabella supporti](media-table.md) non viene utilizzata dall'azione RemoveFiles.

Il nome del file di destinazione può essere specificato nel testo localizzato nella colonna FileName della tabella RemoveFile.

 

 



