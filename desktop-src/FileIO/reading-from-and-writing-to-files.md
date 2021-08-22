---
description: Un'applicazione legge e scrive in un file usando le funzioni ReadFile, ReadFileEx, WriteFile e WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lettura e scrittura nei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b88de3510a681839a9592bed4755de6249f79db117d94985ddb00320381b92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533321"
---
# <a name="reading-from-and-writing-to-files"></a>Lettura e scrittura nei file

Un'applicazione legge e scrive in un file usando le funzioni [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) . Queste funzioni richiedono, rispettivamente, l'apertura di un handle a un file per la lettura e la scrittura. Leggono e scrivono un numero specificato di byte nella posizione indicata dal puntatore del file. I dati vengono letti e scritti esattamente come specificato. Le funzioni non formattano i dati.

Quando il puntatore del file raggiunge la fine di un file e l'applicazione tenta di leggere dal file, non si verifica alcun errore, ma non vengono letti byte. Pertanto, la lettura di zero byte senza errori indica che l'applicazione ha raggiunto la fine del file. La scrittura di zero byte non esegue alcuna operazione.

Per ulteriori informazioni, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                                           | Descrizione                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Posizionamento di un puntatore di file](positioning-a-file-pointer.md)<br/>                                                                         | Windows usa un puntatore di file per tenere traccia dei byte letti o scritti.<br/>                                                       |
| [Lettura o scrittura in file con uno schema Scatter-Gather scrittura](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | Descrive uno schema di raccolta a dispersione per la lettura o la scrittura di blocchi di dati non contigui in un'unica operazione.<br/>                   |
| [Scaricamento System-Buffered I/O su disco](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | Windows i dati in operazioni di lettura e scrittura di file in buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco.<br/> |
| [Troncamento o estensione di file](truncating-or-extending-files.md)<br/>                                                                   | Un'applicazione può troncare o estendere un file chiamando [**SetEndOfFile.**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                             |



 

 

 




