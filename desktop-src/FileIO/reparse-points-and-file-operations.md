---
description: Descrive il modo in cui i reparse point abilitano il comportamento file system che si riparte dal comportamento che la maggior parte degli sviluppatori Windows prevede
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Reparse point e operazioni su file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232978"
---
# <a name="reparse-points-and-file-operations"></a>Reparse point e operazioni su file

I *reparse point* abilitano file System comportamento che si riferisce dal comportamento che la maggior parte degli sviluppatori Windows può essere abituato, pertanto tenere presente questi comportamenti quando si scrivono applicazioni che modificano i file è fondamentale per applicazioni affidabili e affidabili progettate per accedere ai file System che supportano i reparse point. L'ambito di queste considerazioni dipende dall'implementazione specifica e dal comportamento del filtro file system associato di un determinato punto di analisi, che può essere definito dall'utente. Per ulteriori informazioni, vedere [reparse point](reparse-points.md).

Si considerino gli esempi seguenti relativi alle implementazioni del reparse point NTFS, che includono le cartelle montate, i file collegati e il server di archiviazione remota Microsoft:

-   Quando si esegue il backup di file con i reparse point, le applicazioni di backup che usano [flussi di file](file-streams.md) devono specificare i **\_ \_ dati di analisi del backup** nella struttura dell' [**\_ \_ ID del flusso Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) .
-   Per le applicazioni che utilizzano la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) è necessario specificare il flag di **file \_ \_ Open \_ reparse \_ Point** quando si apre il file se si tratta di un reparse point. Per ulteriori informazioni, vedere [creazione e apertura di file](creating-and-opening-files.md).
-   Il processo di [deframmentazione dei file](defragmenting-files.md) richiede una gestione speciale per i reparse point.
-   Le applicazioni di rilevamento del virus devono cercare i reparse point che indicano i file collegati.
-   La maggior parte delle applicazioni deve eseguire azioni speciali per i file spostati nell'archiviazione a lungo termine, se solo per notificare all'utente che il recupero del file potrebbe richiedere tempo.
-   La funzione [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) consente di aprire il file o il reparse point, a seconda dell'uso del flag di **file \_ \_ Open \_ reparse \_ Point** .
-   I collegamenti simbolici, come reparse point, presentano alcune [considerazioni di programmazione](symbolic-link-programming-considerations.md) specifiche.
-   Le attività di gestione del volume per la lettura dei record del journal delle modifiche USN (Update Sequence Number) richiedono una gestione speciale per i reparse point quando si usa il [**\_ record USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e si leggono le strutture [**\_ \_ \_ dei dati journal USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Determinare se una directory è una cartella montata](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[Creazione di cartelle montate](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[Effetti dei collegamenti simbolici sulle funzioni di file System](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
