---
description: La \_ tabella SummaryInformation è una tabella speciale usata con il flusso di informazioni di riepilogo. È possibile ottenere o impostare il flusso di informazioni di riepilogo di un database Windows Installer esportando o importando un file di archivio di testo denominato \_ SummaryInformation.idt.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3824ceb9b3ad12338d84dfeea016a3c7e4404c274543cc691dc6ea0fb121bd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805737"
---
# <a name="_summaryinformation"></a>\_Informazioni di riepilogo

La \_ tabella SummaryInformation è una tabella speciale usata con il flusso [di informazioni di riepilogo.](summary-information-stream.md) È possibile ottenere o impostare il flusso di informazioni di riepilogo di un database Windows Installer esportando o importando un [file](text-archive-files.md) di archivio di testo denominato \_ SummaryInformation.idt.

Il file con estensione idt di una tabella \_ SummaryInformation esportata ha il formato seguente.

-   La prima riga contiene i nomi delle colonne della tabella separati da tabulazioni: PropertyId e Value. Per un elenco delle proprietà e dei relativi ID (PID), vedere l'argomento [Summary Information Stream Property Set (Set](summary-information-stream-property-set.md) di proprietà del flusso di informazioni di riepilogo).
-   La seconda riga contiene le definizioni di colonna separate da tabulazioni. Le definizioni di colonna vengono specificate come nel formato di file di archivio IDT [di base.](archive-file-format.md) La colonna PropertyId può essere un valore short integer non nullable. La colonna Value può essere una stringa localizzabile non nullable di 255 caratteri.
-   La terza riga è il nome della tabella e il nome della colonna chiave primaria separati da tabulazioni: \_ SummaryInformation e PropertyId.
-   Le righe rimanenti nel file rappresentano il PID e il valore associato, separati da tabulazioni. Data e ora in \_ SummaryInformation sono nel formato: AAAA/MM/GG hh::mm::ss. Ad esempio, 22/03/1999 15:25:45.

Di seguito è riportato un esempio del [flusso di informazioni di](summary-information-stream.md) riepilogo di un database in formato .idt.

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

Quando si usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o il metodo [Import](database-import.md) dell'oggetto [**Database**](database-object.md) per importare una tabella di archivio di testo denominata SummaryInformation in un database del programma di installazione, si scrive il flusso \_ "05SummaryInformation" nel database.

 

 



