---
description: Un'applicazione legge e scrive in un file usando le funzioni ReadFile, ReadFileEx, WriteFile e WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lettura e scrittura nei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315931"
---
# <a name="reading-from-and-writing-to-files"></a>Lettura e scrittura nei file

Un'applicazione legge e scrive in un file usando le funzioni [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) . Queste funzioni richiedono un handle per un file da aprire rispettivamente per la lettura e la scrittura. Leggono e scrivono un numero specificato di byte nella posizione indicata dal puntatore del file. I dati vengono letti e scritti esattamente come specificato; le funzioni non formattano i dati.

Quando il puntatore del file raggiunge la fine di un file e l'applicazione tenta di leggere dal file, non si verifica alcun errore, ma non viene letto alcun byte. Pertanto, la lettura di zero byte senza errori indica che l'applicazione ha raggiunto la fine del file. La scrittura di zero byte non esegue alcuna operazione.

Per ulteriori informazioni, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                                           | Descrizione                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Posizionamento di un puntatore di file](positioning-a-file-pointer.md)<br/>                                                                         | Windows utilizza un puntatore di file per tenere traccia dei byte letti o scritti.<br/>                                                       |
| [Lettura o scrittura nei file utilizzando uno schema di Scatter-Gather](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | Descrive uno schema di raccolta a dispersione per la lettura o la scrittura di blocchi di dati non contigui in un'unica operazione.<br/>                   |
| [Scaricamento di System-Buffered dati di I/O su disco](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | Windows archivia i dati nelle operazioni di lettura e scrittura dei file nei buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco.<br/> |
| [Troncamento o estensione di file](truncating-or-extending-files.md)<br/>                                                                   | Un'applicazione può troncare o estendere un file chiamando [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).<br/>                             |



 

 

 




