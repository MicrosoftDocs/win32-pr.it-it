---
description: La \_ tabella SummaryInformation è una tabella speciale utilizzata con il flusso di informazioni di riepilogo. È possibile ottenere o impostare il flusso di informazioni di riepilogo di un database di Windows Installer esportando o importando un file di archivio di testo denominato \_ SummaryInformation. IDT.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311114"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

La \_ tabella SummaryInformation è una tabella speciale utilizzata con il [flusso di informazioni di riepilogo](summary-information-stream.md). È possibile ottenere o impostare il flusso di informazioni di riepilogo di un database di Windows Installer esportando o importando un [file di archivio di testo](text-archive-files.md) denominato \_ SummaryInformation. IDT.

Il file con estensione IDT di una \_ tabella SummaryInformation esportata presenta il formato seguente.

-   La prima riga contiene i nomi delle colonne di tabella separati da tabulazioni: PropertyId e value. Per un elenco delle proprietà e dei rispettivi ID (PID), vedere l'argomento relativo al [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md) .
-   La seconda riga contiene le definizioni di colonna separate da tabulazioni. Le definizioni di colonna vengono specificate in modo analogo al formato del file di [Archivio](archive-file-format.md)Basic. IDT. La colonna PropertyId può essere un valore short integer non nullable. La colonna valore può essere una stringa localizzabile non nullable di 255 caratteri.
-   La terza riga è il nome della tabella e il nome della colonna chiave primaria separati da tabulazioni: \_ SummaryInformation e PropertyId.
-   Le righe rimanenti nel file rappresentano il PID e il valore associato, separati da tabulazioni. La data e l'ora in \_ SummaryInformation sono nel formato: aaaa/mm/gg hh:: mm:: SS. Ad esempio, 1999/03/22 15:25:45.

Di seguito è riportato un esempio del [flusso di informazioni di riepilogo](summary-information-stream.md) di un database in formato IDT.

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

Quando si utilizza [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o il metodo [Import](database-import.md) dell'oggetto di [**database**](database-object.md) per importare una tabella di archivio di testo denominata \_ SummaryInformation in un database del programma di installazione, è necessario scrivere il flusso "05SummaryInformation" nel database.

 

 



