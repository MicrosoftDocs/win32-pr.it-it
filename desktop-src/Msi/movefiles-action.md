---
description: L'azione MoveFiles individua i file esistenti nel computer dell'utente e sposta o copia tali file in un nuovo percorso.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Azione MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8581cd19569109c0f7697b5dfebf33e91b33da9ba84d15caf424242e4e21ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945036"
---
# <a name="movefiles-action"></a>Azione MoveFiles

L'azione MoveFiles individua i file esistenti nel computer dell'utente e sposta o copia tali file in un nuovo percorso. L'azione MoveFiles esegue una query sulla tabella [MoveFile](movefile-table.md) e sposta i file specificati se il componente collegato alle voci viene specificato per l'installazione in locale o viene eseguito dall'origine.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione MoveFiles deve essere eseguita dopo [l'azione InstallValidate](installvalidate-action.md) e prima [dell'azione InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                  |
|-------|---------------------------------------------|
| \[1\] | Identificatore del file spostato.                   |
| \[6\] | Dimensioni del file installato in byte.            |
| \[9\] | Identificatore della directory contenente il file spostato. |



 

## <a name="remarks"></a>Commenti

La tabella MoveFiles contiene una colonna denominata "options" che specifica i file di origine da spostare o copiare. Un file di origine spostato viene eliminato dopo che è stato copiato in un nuovo percorso. Per la sintassi esatta, vedere la [tabella MoveFile](movefile-table.md).

Le colonne SourceFolder e DestFolder della tabella MoveFile sono nomi di proprietà i cui valori devono essere risolti in percorsi completi. Queste proprietà possono essere una qualsiasi delle voci di directory nella tabella [Directory,](directory-table.md) qualsiasi proprietà di cartella predefinita (ad esempio [**FavoritesFolder)**](favoritesfolder.md)o una proprietà impostata da qualsiasi voce nella [tabella AppSearch.](appsearch-table.md) Queste proprietà possono contenere un percorso completo contenente il nome file di un file specifico. Ad esempio, è possibile creare la tabella AppSearch per cercare un determinato file e impostare una proprietà sul percorso completo del file. In questo esempio la colonna SourceName nella tabella MoveFile può essere lasciata vuota per indicare che il valore nella proprietà SourceFolder contiene un percorso di file completo. Il punto e virgola è il delimitatore di elenco per trasformazioni, origini e patch e non deve essere usato nei nomi di file o nei percorsi.

L'azione MoveFiles non agisce sulle voci nella tabella MoveFile in cui la proprietà SourceFolder o DestFolder non restituisce un percorso completo.

L'azione MoveFiles tenta di spostare o copiare tutti i file nella directory di origine che corrispondono al nome specificato nella colonna SourceName della tabella MoveFiles. Il nome nella colonna SourceName può includere \* o ? caratteri jolly che consentono di spostare o copiare un gruppo di file. Ad esempio, la colonna SourceName può contenere una voce ".xls" e l'azione MoveFiles sposta o copia ogni cartella di lavoro di Microsoft Excel dalla directory di origine \* alla destinazione.

Il nome da assegnare al file di destinazione può essere specificato nella colonna DestName della tabella MoveFile. Il nome del file di destinazione mantiene il nome del file di origine se questa colonna viene lasciata vuota.

Se viene immesso un carattere jolly " " nella colonna SourceName della tabella MoveFile e viene specificato un nome di file di destinazione nella colonna DestName, tutti i file spostati o copiati mantengono i nomi nelle \* origini. [](movefile-table.md)

I file spostati o copiati dall'azione MoveFiles non vengono eliminati quando il prodotto viene disinstallato.

 

 



