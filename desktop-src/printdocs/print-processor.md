---
description: Lo spooler di stampa monitora i processi di stampa correnti e la stampante di destinazione per determinare l'ora appropriata per la stampa di un processo.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Processore di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1250c617706b8e11309ffaf151fb09820ba1acbdb9f09d5cf44086e2153f8c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718621"
---
# <a name="print-processor"></a>Processore di stampa

Lo spooler di stampa monitora i processi di stampa correnti e la stampante di destinazione per determinare l'ora appropriata per la stampa di un processo. Quando lo spooler determina che un processo deve essere stampato, chiama il processore di stampa. Il processore di stampa è un plug-in che elabora i dati del processo di stampa.

Usare le funzioni seguenti per lavorare con i processori di stampa.



| Funzione                                                           | Descrizione                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [**AddPrintProcessor**](addprintprocessor.md)                     | Installa un processore di stampa in un server specificato.                    |
| [**DeletePrintProcessor**](deleteprintprocessor.md)               | Rimuove un processore di stampa da un server specificato.                 |
| [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) | Enumera i tipi di dati supportati da un processore di stampa specificato. |
| [**EnumPrintProcessors**](enumprintprocessors.md)                 | Enumera i processori di stampa installati in un server specificato.     |
| [**GetPrintProcessorDirectory**](getprintprocessordirectory.md)   | Recupera il percorso del processore di stampa nel server specificato.  |



 

 

 



