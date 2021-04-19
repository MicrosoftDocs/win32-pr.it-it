---
description: Lo spooler di stampa monitora i processi di stampa correnti e la stampante di destinazione per determinare il momento appropriato per la stampa di un processo.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Processore di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311812"
---
# <a name="print-processor"></a>Processore di stampa

Lo spooler di stampa monitora i processi di stampa correnti e la stampante di destinazione per determinare il momento appropriato per la stampa di un processo. Quando lo spooler stabilisce che è necessario stampare un processo, viene chiamato il processore di stampa. Il processore di stampa è un plug-in che elabora i dati del processo di stampa.

Usare le funzioni seguenti per lavorare con i processori di stampa.



| Funzione                                                           | Descrizione                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [**AddPrintProcessor**](addprintprocessor.md)                     | Installa un processore di stampa in un server specificato.                    |
| [**DeletePrintProcessor**](deleteprintprocessor.md)               | Rimuove un processore di stampanti da un server specificato.                 |
| [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) | Enumera i tipi di dati supportati da un processore di stampa specificato. |
| [**EnumPrintProcessors**](enumprintprocessors.md)                 | Enumera i processori di stampa installati in un server specificato.     |
| [**GetPrintProcessorDirectory**](getprintprocessordirectory.md)   | Recupera il percorso per il processore di stampa nel server specificato.  |



 

 

 



