---
description: L'azione InstallFiles copia i file specificati nella tabella File dalla directory di origine alla directory di destinazione.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Azione InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df2a62deb253314e84e72cd84e88052f1175db7451807c3f266542e29c10c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629932"
---
# <a name="installfiles-action"></a>Azione InstallFiles

L'azione InstallFiles copia i file specificati nella tabella File dalla directory di origine alla directory di destinazione.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione InstallFiles deve essere eseguita dopo [l'azione InstallValidate](installvalidate-action.md) e prima di qualsiasi azione dipendente da file.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                      |
|-------|-------------------------------------------------|
| \[1\] | Identificatore del file installato.                   |
| \[6\] | Dimensioni del file installato in byte.                |
| \[9\] | Identificatore della directory contenente il file installato. |



 

## <a name="remarks"></a>Commenti

L'azione InstallFiles opera sui file specificati nella [tabella File](file-table.md). Ogni file viene installato in base allo stato di installazione del componente associato del file nella [tabella Componente](component-table.md). Solo i file i cui componenti vengono risolti nello stato **msiInstallStatelocal** sono idonei per la copia.

L'azione InstallFiles implementa le colonne seguenti della tabella File.

-   La colonna FileName specifica il nome del file di destinazione.
-   La colonna Versione specifica la versione del file.
-   La colonna Attributi specifica i bit del flag del file e dell'attributo di installazione.
-   La colonna File specifica il token di file univoco.
-   La colonna FileSize specifica le dimensioni in byte del file non compresso.
-   La colonna Lingua specifica l'identificatore della lingua del file.
-   La colonna Sequence specifica il numero di sequenza sul supporto.

L'azione InstallFiles implementa le colonne seguenti della tabella Component.

-   La colonna Directory \_ specifica un riferimento a un elemento della tabella [Directory.](directory-table.md)
-   La colonna Componente specifica un nome univoco per l'elemento del componente.

Il file specificato viene copiato solo se si verifica una delle condizioni seguenti:

-   Il file non è attualmente installato nel computer locale.
-   Il file si trova nel computer locale ma ha un numero di versione inferiore rispetto al file nella [tabella File](file-table.md).
-   Il file si trova nel computer locale, ma non è presente alcun numero di versione associato.

La directory di origine per ogni file da copiare è determinata da sourceMode, che a sua volta dipende dal valore nella colonna Cabinet della tabella Media. Per una descrizione completa della modalità di origine, vedere la [tabella Media](media-table.md).

Se la directory di origine per un file da copiare si trova su supporti rimovibili, ad esempio un disco floppy o un CD-ROM, l'azione InstallFiles verifica che il supporto di origine corretto venga inserito prima di tentare di copiare il file. InstallFiles cerca supporti dello stesso tipo rimovibile con un'etichetta di [*volume*](v-gly.md) corrispondente al valore specificato nella colonna VolumeLabel della tabella Media. Se viene trovato un volume montato corrispondente, il processo di copia dei file continua. Se non viene trovata alcuna corrispondenza, una finestra di dialogo richiede all'utente di inserire il supporto appropriato. In questo caso, la finestra di dialogo usa il nome del supporto disponibile nella colonna DiskPrompt della tabella Media come parte del prompt.

Prestare attenzione perché l'azione InstallFiles può eliminare un file originale e non sostituirlo. Ciò si verifica quando l'azione InstallFiles verifica un errore durante la sostituzione di un file meno recente e l'utente sceglie di ignorare l'errore. Il comportamento predefinito del programma di installazione è eliminare un file precedente prima di assicurarsi che il nuovo file venga copiato correttamente.

Per le regole di controllo delle versioni dei file usate dal programma di installazione, vedere [Regole di controllo delle versioni dei file](file-versioning-rules.md).

 

 



