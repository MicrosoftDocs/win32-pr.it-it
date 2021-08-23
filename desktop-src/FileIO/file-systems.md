---
description: Gestire le directory con la tabella delle voci di directory, gli handle di directory e i reparse point.
title: File system locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa77c1029ce4dc19529b148dde1798084acf91afcf6e4435adf8fb2ab266f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696231"
---
# <a name="local-file-systems"></a>File system locali

Un *file system* consente alle applicazioni di archiviare e recuperare file nei dispositivi di archiviazione. I file vengono inseriti in una struttura gerarchica. L file system specifica le convenzioni di denominazione per i file e il formato per specificare il percorso di un file nella struttura ad albero.

Ogni file system è costituita da uno o più driver e librerie a collegamento dinamico che definiscono i formati di dati e le funzionalità del file system. I file system possono essere presenti in molti tipi diversi di dispositivi di archiviazione, tra cui dischi rigidi, jukebox, dischi ottici rimovibili, unità di backup su nastro e schede di memoria.

Tutti i file system supportati da Windows i componenti di archiviazione seguenti:

-   Volumi. Un *volume* è una raccolta di directory e file.
-   Directory. Una *directory* è una raccolta gerarchica di directory e file.
-   File Un *file* è un raggruppamento logico di dati correlati.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                | Descrizione                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestione directory](directory-management.md)<br/>          | Una *directory* è una raccolta gerarchica di directory e file. L'unico vincolo al numero di file che possono essere contenuti in una singola directory è la dimensione fisica del disco in cui si trova la directory.<br/> |
| [Gestione disco](disk-management.md)<br/>                    | Un *disco rigido è* un disco rigido all'interno di un computer che archivia e fornisce un accesso relativamente rapido a grandi quantità di dati. È il tipo di archiviazione più usato con Windows. Il sistema supporta anche supporti rimovibili.<br/>    |
| [Gestione dei file](file-management.md)<br/>                    | Un *oggetto file* fornisce una rappresentazione di una risorsa (un dispositivo fisico o una risorsa che si trova in un dispositivo fisico) che può essere gestita dal sistema di I/O.<br/>                                                            |
| [NTFS transazionale (TxF)](transactional-ntfs-portal.md)<br/> | Ntfs transazionale (TxF) consente di eseguire operazioni su file in un volume file system NTFS in una transazione.<br/>                                                                                                                 |
| [Gestione dei volumi](volume-management.md)<br/>                | Il livello più alto di organizzazione nel file system è il *volume*. Un file system risiede in un volume.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento tecniche su FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))
</dt> <dt>

[Tecnologie dei file system](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))
</dt> <dt>

[Informazioni di riferimento tecniche su NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

