---
description: Con Windows Installer è disponibile un controllo di ridondanza ciclico (CRC) dei file.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Verifica CRC durante un'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232682"
---
# <a name="crc-checking-during-an-installation"></a>Verifica CRC durante un'installazione

Con Windows Installer è disponibile un controllo di ridondanza ciclico (CRC) dei file. Il controllo CRC è un meccanismo di controllo degli errori, simile a un checksum, che consente a un'applicazione di determinare se le informazioni in un file sono state modificate. Al termine della copia di un file, il Windows Installer ottiene un valore CRC dai file di origine e di destinazione. Il programma di installazione controlla il CRC originale timbrato nel file e lo confronta con il CRC calcolato dalla copia. Il controllo CRC ha esito negativo se il valore CRC originale non è null ed è diverso dal CRC calcolato per la copia. Se il CRC originale è null, non viene eseguito alcun controllo.

Il Windows Installer esegue un controllo CRC su un file nei casi seguenti:

-   Se la [Proprietà MSICHECKCRCS](msicheckcrcs.md) è impostata e **msidbFileAttributesChecksum** è incluso nel campo Attributes del record del file nella [tabella file](file-table.md). Il programma di installazione esegue il controllo CRC una volta dopo l'installazione, la duplicazione o lo stato di trasferimento del file.
-   Se la [Proprietà MSICHECKCRCS](msicheckcrcs.md) è impostata e **msidbFileAttributesChecksum** è incluso nel campo Attributes del record del file nella [tabella file](file-table.md), il programma di installazione esegue un controllo CRC dopo l'applicazione di patch al file.
-   Se il **msidbFileAttributesChecksum** è incluso nel campo attributi del record del file nella [tabella file](file-table.md), il programma di installazione esegue un controllo CRC prima di associare le immagini.

Se il controllo ha esito negativo prima di associare un'immagine, il programma di installazione segnala i due errori seguenti nel file di log e continua l'installazione senza associare il file.



| Codice | Message                                               |
|------|-------------------------------------------------------|
| 2941 | Non è possibile calcolare il CRC per il file \[ 2 \] .             |
| 2942 | L'azione azione BindImage sul non è stata eseguita su \[ 2 \] file. |



 

Se il controllo ha esito negativo dopo la copia, la duplicazione o la correzione di un file non compresso, il programma di installazione segnala l'errore seguente. Questo errore viene inoltre segnalato se il controllo ha esito negativo dopo la copia di un file compresso. Se il file ha l'attributo **msidbFileAttributesVital** , il file è considerato vitale per l'installazione e l'utente ottiene l'opzione per riprovare o annullare l'installazione. Se il file è contrassegnato come non vitale nella colonna attributi della [tabella file](file-table.md), l'utente può ignorare l'errore e continuare, riprovare o annullare l'installazione.



| Codice | Message                                         |
|------|-------------------------------------------------|
| 1331 | Non è stato possibile copiare correttamente \[ 2 \] file: errore CRC. |



 

Si noti che vengono spostati solo i file non compressi. Se il controllo ha esito negativo dopo lo spostamento di un file non compresso, il programma di installazione visualizzerà il seguente errore. Se il file ha l'attributo **msidbFileAttributesVital** , il file è considerato vitale per l'installazione e l'installazione non riesce. Se il file è contrassegnato come non vitale nella colonna attributi della [tabella file](file-table.md), l'utente ottiene l'opzione per annullare o ignorare l'errore e continuare l'installazione.



| Codice | Message                                         |
|------|-------------------------------------------------|
| 1332 | Non è stato possibile spostare correttamente \[ 2 \] file: errore CRC. |



 

Se il controllo ha esito negativo dopo la correzione di un file non compresso, il programma di installazione visualizzerà il seguente errore. Se il file ha l'attributo **msidbFileAttributesVital** , il file è considerato vitale per l'installazione e l'installazione non riesce. Se il file è contrassegnato come non vitale nella colonna attributi della [tabella file](file-table.md), l'utente ottiene l'opzione per annullare o ignorare l'errore e continuare l'installazione.



| Codice | Message                                          |
|------|--------------------------------------------------|
| 1333 | Non è stato possibile correggere correttamente la patch \[ 2 \] file: errore CRC. |



 

 

 



