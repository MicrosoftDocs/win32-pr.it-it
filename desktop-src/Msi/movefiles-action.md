---
description: L'azione MoveFiles individua i file esistenti nel computer dell'utente e li sposta o li copia in una nuova posizione.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Azione MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885509"
---
# <a name="movefiles-action"></a>Azione MoveFiles

L'azione MoveFiles individua i file esistenti nel computer dell'utente e li sposta o li copia in una nuova posizione. L'azione MoveFiles esegue una query sulla [tabella MoveFile](movefile-table.md) e sposta i file specificati se il componente collegato alle voci è specificato per l'installazione locale o viene eseguito dall'origine.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione MoveFiles deve essere successiva all'azione [InstallValidate](installvalidate-action.md) e prima dell'azione [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                  |
|-------|---------------------------------------------|
| \[1\] | Identificatore del file spostato.                   |
| \[6\] | Dimensioni del file installato in byte.            |
| \[9\] | Identificatore della directory che contiene il file spostato. |



 

## <a name="remarks"></a>Commenti

La tabella MoveFiles contiene una colonna denominata "Options" che specifica i file di origine da spostare o copiare. Un file di origine spostato viene eliminato dopo essere stato copiato in un nuovo percorso. Per la sintassi esatta, vedere la [tabella MoveFile](movefile-table.md).

Le colonne SourceFolder e DestFolder della tabella MoveFile sono nomi di proprietà i cui valori sono previsti per la risoluzione nei percorsi completi. Queste proprietà possono essere qualsiasi voce di directory nella tabella di [directory](directory-table.md) , qualsiasi proprietà di cartella predefinita (ad esempio,[**FavoritesFolder**](favoritesfolder.md)) o una proprietà impostata da qualsiasi voce nella tabella [AppSearch](appsearch-table.md) . Queste proprietà possono contenere un percorso completo contenente il nome file di un file specifico. Ad esempio, è possibile creare la tabella AppSearch per cercare un file specifico e impostare una proprietà sul percorso completo di tale file. In questo esempio, la colonna SourceName nella tabella MoveFile può essere lasciata vuota per indicare che il valore nella proprietà SourceFolder contiene un percorso file completo. Il punto e virgola è il delimitatore di elenco per le trasformazioni, le origini e le patch e non deve essere usato nei nomi file o nei percorsi.

L'azione MoveFiles non agisce sulle voci della tabella MoveFile in cui la proprietà SourceFolder o DestFolder non restituisce un percorso completo.

L'azione MoveFiles tenta di spostare o copiare tutti i file nella directory di origine che corrispondono al nome specificato nella colonna SourceName della tabella MoveFiles. Il nome nella colonna SourceName può includere \* o? caratteri jolly che consentono lo spostamento o la copia di un gruppo di file. La colonna SourceName, ad esempio, può contenere una voce " \* . xls" e l'azione MoveFiles sposta o copia ogni cartella di lavoro di Microsoft Excel dalla directory di origine alla destinazione.

Il nome da assegnare al file di destinazione può essere specificato nella colonna destName della tabella MoveFile. Il nome del file di destinazione mantiene il nome del file di origine se questa colonna viene lasciata vuota.

Se un \* carattere jolly "" viene immesso nella colonna SourceName della [tabella MoveFile](movefile-table.md) e nella colonna destName viene specificato un nome file di destinazione, tutti i file spostati o copiati manterranno i nomi nelle origini.

I file che vengono spostati o copiati dall'azione MoveFiles non vengono eliminati quando il prodotto viene disinstallato.

 

 



