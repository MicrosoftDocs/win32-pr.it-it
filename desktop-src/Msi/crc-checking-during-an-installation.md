---
description: È disponibile un controllo di ridondanza ciclico (CRC) di file con Windows programma di installazione.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Controllo CRC durante un'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b80a9b1900abf6c294911803df155a4c75025f5ad5ef01609af7345b0431e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379916"
---
# <a name="crc-checking-during-an-installation"></a>Controllo CRC durante un'installazione

È disponibile un controllo di ridondanza ciclico (CRC) di file con Windows programma di installazione. Il controllo CRC è un meccanismo di controllo degli errori, simile a un checksum, che consente a un'applicazione di determinare se le informazioni in un file sono state modificate. Al termine Windows del programma di installazione, ottiene un valore CRC dai file di origine e di destinazione. Il programma di installazione controlla il CRC originale inserito nel file e lo confronta con il CRC calcolato dalla copia. Il controllo CRC ha esito negativo se il valore CRC originale è diverso da quello calcolato nella copia. Se il CRC originale è Null, non viene eseguito alcun controllo.

Il Windows installer esegue un controllo CRC su un file nei casi seguenti:

-   Se la [proprietà MSICHECKCRCS](msicheckcrcs.md) è impostata e **msidbFileAttributesChecksum** è incluso nel campo Attributi del record del file nella [tabella File](file-table.md). Il programma di installazione esegue il controllo CRC una volta dopo l'installazione, la duplicazione o lo spostamento del file.
-   Se la [proprietà MSICHECKCRCS](msicheckcrcs.md) è impostata e **msidbFileAttributesChecksum** è incluso nel campo Attributi del record del file nella tabella [File](file-table.md), il programma di installazione esegue un controllo CRC dopo l'applicazione di patch al file.
-   Se **msidbFileAttributesChecksum** è incluso nel campo Attributi del record del file nella tabella [File](file-table.md), il programma di installazione esegue un controllo CRC prima di associare le immagini.

Se il controllo ha esito negativo prima di associare un'immagine, il programma di installazione segnala i due errori seguenti nel file di log e continua l'installazione senza associare il file.



| Codice | Message                                               |
|------|-------------------------------------------------------|
| 2941 | Impossibile calcolare il CRC per il file \[ \] 2.             |
| 2942 | L'azione BindImage non è stata eseguita su \[ 2 \] file. |



 

Se il controllo ha esito negativo dopo la copia, la duplicazione o l'applicazione di patch a un file non compresso, il programma di installazione segnala l'errore seguente. Questo errore viene segnalato anche se il controllo ha esito negativo dopo la copia di un file compresso. Se il file ha l'attributo **msidbFileAttributesVital,** il file viene considerato essenziale per l'installazione e l'utente ottiene la possibilità di riprovare o annullare l'installazione. Se il file è contrassegnato come nonvitale nella colonna Attributi della tabella [File](file-table.md), l'utente può ignorare l'errore e continuare, riprovare o annullare l'installazione.



| Codice | Message                                         |
|------|-------------------------------------------------|
| 1331 | Impossibile copiare correttamente \[ il file \] 2: errore CRC. |



 

Si noti che vengono spostati solo i file non compressi. Se il controllo ha esito negativo dopo lo spostamento di un file non compresso, il programma di installazione visualizza l'errore seguente. Se il file ha **l'attributo msidbFileAttributesVital,** il file viene considerato essenziale per l'installazione e l'installazione non riesce. Se il file è contrassegnato come nonvitale nella colonna Attributi della tabella [File](file-table.md), l'utente ottiene l'opzione per annullare o ignorare l'errore e continuare l'installazione.



| Codice | Message                                         |
|------|-------------------------------------------------|
| 1332 | Impossibile spostare correttamente \[ il file \] 2: errore CRC. |



 

Se il controllo ha esito negativo dopo l'applicazione di patch a un file non compresso, il programma di installazione visualizza l'errore seguente. Se il file ha **l'attributo msidbFileAttributesVital,** il file viene considerato essenziale per l'installazione e l'installazione non riesce. Se il file è contrassegnato come nonvitale nella colonna Attributi della tabella [File](file-table.md), l'utente ottiene l'opzione per annullare o ignorare l'errore e continuare l'installazione.



| Codice | Message                                          |
|------|--------------------------------------------------|
| 1333 | Impossibile applicare correttamente la patch \[ al file \] 2: errore CRC. |



 

 

 



