---
description: Al termine di un processo con l'oggetto di mapping dei file, è necessario eliminare tutte le visualizzazioni di file nello spazio degli indirizzi utilizzando la funzione UnmapViewOfFile per ogni visualizzazione file.
ms.assetid: d62d068c-9b1d-4dbf-8b21-31a636a41456
title: Chiusura di un oggetto di mapping dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab35152bd90d401ca7f30a7497d1f0b06263539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881509"
---
# <a name="closing-a-file-mapping-object"></a>Chiusura di un oggetto di mapping dei file

Al termine di un processo con l'oggetto di mapping dei file, è necessario eliminare tutte le visualizzazioni di file nello spazio degli indirizzi utilizzando la funzione [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) per ogni visualizzazione file.

L'annullamento del mapping di una visualizzazione mappata di un file invalida l'intervallo occupato dalla vista nello spazio degli indirizzi del processo e rende disponibile l'intervallo per altre allocazioni. Rimuove la voce di working set per ogni pagina virtuale non mappata che faceva parte della working set del processo e riduce le working set dimensioni del processo. Decrementa anche il numero di condivisioni della pagina fisica corrispondente.

Le pagine modificate nella visualizzazione senza mapping non vengono scritte su disco fino a quando il conteggio delle condivisioni non raggiunge lo zero o, in altre parole, fino a quando non viene eseguito il mapping o l'eliminazione dei set di lavoro di tutti i processi che condividono le pagine. Anche in questo caso, le pagine modificate vengono scritte "pigramente" su disco; in altre termini, le modifiche possono essere memorizzate nella cache e scritte su disco in un secondo momento. Per ridurre al minimo il rischio di perdita di dati in caso di interruzione dell'alimentazione o di un arresto anomalo del sistema, le applicazioni devono svuotare in modo esplicito le pagine modificate utilizzando la funzione [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) .

Quando ogni processo termina utilizzando l'oggetto di mapping dei file e dispone di tutte le visualizzazioni senza mapping, è necessario chiudere l'handle dell'oggetto mapping di file e il file su disco chiamando [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle). Queste chiamate a **CloseHandle** hanno esito positivo anche quando sono presenti visualizzazioni di file ancora aperte. Tuttavia, lasciare le visualizzazioni di file mappate causa perdite di memoria.

 

 
