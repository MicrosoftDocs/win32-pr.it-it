---
description: Descrive come i reparse point consentono file system comportamento che si discosta dal comportamento previsto Windows sviluppatori.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Reparse Point e operazioni su file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d18b42c2bc51617e185c2d8f13fde15952ad83d2c2c635d312d589677ee8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015179"
---
# <a name="reparse-points-and-file-operations"></a>Reparse Point e operazioni su file

I *reparse* point consentono un comportamento file system che si discosta dal comportamento a cui la maggior parte degli sviluppatori Windows può essere abituata, pertanto essere consapevoli di questi comportamenti quando scrivono applicazioni che modificano i file è fondamentale per applicazioni affidabili e affidabili destinate ad accedere ai file system che supportano i reparse point. L'entità di queste considerazioni dipenderà dall'implementazione specifica e dal comportamento file system filtro associato di un particolare reparse point, che può essere definito dall'utente. Per altre informazioni, vedere [Reparse Points](reparse-points.md).

Si considerino gli esempi seguenti relativi alle implementazioni dei reparse point NTFS, che includono cartelle montate, file collegati e Microsoft Remote Archiviazione Server:

-   Le applicazioni di backup che usano [flussi di file](file-streams.md) devono specificare BACKUP **\_ REPARSE \_ DATA** nella struttura [**\_ DELL'ID \_ FLUSSO WIN32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) quando si esegue il backup di file con reparse point.
-   Le applicazioni che usano [**la funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) devono specificare il flag **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT** all'apertura del file se si tratta di un reparse point. Per altre informazioni, vedere [Creazione e apertura di file](creating-and-opening-files.md).
-   Il processo di [deframmentazione dei file](defragmenting-files.md) richiede una gestione speciale per i reparse point.
-   Le applicazioni di rilevamento virus devono cercare reparse point che indicano i file collegati.
-   La maggior parte delle applicazioni deve eseguire azioni speciali per i file spostati nell'archiviazione a lungo termine, se non altro per notificare all'utente che potrebbe essere necessario del tempo per recuperare il file.
-   La [**funzione OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) aprirà il file o il reparse point, a seconda dell'uso del flag **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT.**
-   I collegamenti simbolici, come reparse point, hanno alcune considerazioni [di programmazione](symbolic-link-programming-considerations.md) specifiche.
-   Le attività di gestione dei volumi per la lettura dei record del journal delle modifiche USN (Update Sequence Number) richiedono una gestione speciale per i reparse point quando si usano le strutture [**USN \_ RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e [**READ \_ USN \_ JOURNAL \_ DATA.**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Determinare se una directory è una cartella montata](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[Creazione di cartelle montate](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[Effetti di collegamento simbolico sulle funzioni dei file system](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
