---
description: L'azione InstallFiles copia i file specificati nella tabella file dalla directory di origine alla directory di destinazione.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Azione InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308685"
---
# <a name="installfiles-action"></a>Azione InstallFiles

L'azione InstallFiles copia i file specificati nella tabella file dalla directory di origine alla directory di destinazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione InstallFiles deve essere successiva all'azione [InstallValidate](installvalidate-action.md) e prima di qualsiasi azione dipendente dal file.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                      |
|-------|-------------------------------------------------|
| \[1\] | Identificatore del file installato.                   |
| \[6\] | Dimensioni del file installato in byte.                |
| \[9\] | Identificatore della directory che contiene il file installato. |



 

## <a name="remarks"></a>Commenti

L'azione InstallFiles opera sui file specificati nella [tabella file](file-table.md). Ogni file viene installato in base allo stato di installazione del componente associato del file nella [tabella dei componenti](component-table.md). Solo i file i cui componenti vengono risolti nello stato **msiInstallStatelocal** sono idonei per la copia.

L'azione InstallFiles implementa le colonne seguenti della tabella file.

-   La colonna FileName specifica il nome del file di destinazione.
-   La colonna Version specifica la versione del file.
-   La colonna attributi specifica i bit del flag dell'attributo di installazione e del file.
-   La colonna file specifica il token del file univoco.
-   La colonna Filesize specifica le dimensioni del file non compresso in byte.
-   Nella colonna lingua viene specificato l'identificatore della lingua del file.
-   Nella colonna sequenza viene specificato il numero di sequenza sui supporti.

L'azione InstallFiles implementa le colonne seguenti della tabella Component.

-   Nella \_ colonna directory viene specificato un riferimento a un elemento della [tabella di directory](directory-table.md) .
-   La colonna Component specifica un nome univoco per l'elemento Component.

Il file specificato viene copiato solo se si verifica una delle condizioni seguenti:

-   Il file non è attualmente installato nel computer locale.
-   Il file si trova nel computer locale, ma ha un numero di versione inferiore a quello del file nella [tabella file](file-table.md).
-   Il file si trova nel computer locale, ma non è presente alcun numero di versione associato.

La directory di origine per ogni file da copiare è determinata da sourceMode, che a sua volta dipende dal valore nella colonna CAB della tabella media. Per una descrizione completa della modalità di origine, vedere la [tabella media](media-table.md).

Se la directory di origine per un file da copiare si trova su un supporto rimovibile, ad esempio un disco floppy o un CD-ROM, l'azione InstallFiles verifica che il supporto di origine appropriato venga inserito prima di tentare di copiare il file. InstallFiles Cerca i supporti dello stesso tipo rimovibile con un'etichetta di [*volume*](v-gly.md) che corrisponde al valore specificato nella colonna VolumeLabel della tabella media. Se viene trovato un volume montato corrispondente, il processo di copia dei file continua. Se non viene trovata alcuna corrispondenza, una finestra di dialogo richiede all'utente di inserire i supporti appropriati. In questo caso, nella finestra di dialogo viene usato il nome del supporto trovato nella colonna DiskPrompt della tabella dei supporti come parte del prompt.

È necessario prestare attenzione perché l'azione InstallFiles può eliminare un file originale e non sostituirlo. Questo errore si verifica quando si verifica un errore nell'azione InstallFiles durante la sostituzione di un file precedente e l'utente sceglie di ignorare l'errore. Il comportamento predefinito del programma di installazione prevede l'eliminazione di un file obsoleto prima di garantire la copia corretta del nuovo file.

Per le regole di controllo delle versioni dei file usate dal programma di installazione, vedere [regole di controllo delle versioni dei file](file-versioning-rules.md).

 

 



