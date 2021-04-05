---
description: Gestire directory con la tabella voce di directory, gli handle di directory e i reparse point.
title: File system locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755159"
---
# <a name="local-file-systems"></a>File system locali

Un *file System* consente alle applicazioni di archiviare e recuperare file nei dispositivi di archiviazione. I file vengono inseriti in una struttura gerarchica. Il file system specifica le convenzioni di denominazione per i file e il formato per specificare il percorso di un file nella struttura ad albero.

Ogni file system è costituita da uno o più driver e librerie a collegamento dinamico che definiscono i formati di dati e le funzionalità del file system. I file System possono esistere in molti tipi diversi di dispositivi di archiviazione, tra cui dischi rigidi, jukebox, dischi ottici rimovibili, unità di backup su nastro e schede di memoria.

Per tutti i file system supportati da Windows sono disponibili i componenti di archiviazione seguenti:

-   Volumi. Un *volume* è una raccolta di directory e file.
-   Directory. Una *directory* è una raccolta gerarchica di directory e file.
-   File Un *file* è un raggruppamento logico di dati correlati.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                | Descrizione                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestione directory](directory-management.md)<br/>          | Una *directory* è una raccolta gerarchica di directory e file. L'unico vincolo sul numero di file che possono essere contenuti in una singola directory è la dimensione fisica del disco in cui si trova la directory.<br/> |
| [Gestione disco](disk-management.md)<br/>                    | Un *disco rigido* è un disco rigido all'interno di un computer che archivia e fornisce accesso relativamente rapido a grandi quantità di dati. Si tratta del tipo di archiviazione usato più di frequente con Windows. Il sistema supporta inoltre supporti rimovibili.<br/>    |
| [Gestione dei file](file-management.md)<br/>                    | Un *oggetto file* fornisce una rappresentazione di una risorsa, ovvero un dispositivo fisico o una risorsa che si trova in un dispositivo fisico, che può essere gestita dal sistema i/O.<br/>                                                            |
| [Transactional NTFS (TxF)](transactional-ntfs-portal.md)<br/> | Transactional NTFS (TxF) consente di eseguire operazioni su file su un volume file system NTFS in una transazione.<br/>                                                                                                                 |
| [Gestione dei volumi](volume-management.md)<br/>                | Il livello più elevato di organizzazione nella file system è il *volume*. Un file system risiede in un volume.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento tecnico FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))
</dt> <dt>

[Tecnologie per file System](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))
</dt> <dt>

[Riferimento tecnico per NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

