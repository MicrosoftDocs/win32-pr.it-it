---
description: Quando viene apportata una modifica a un file o a una directory in un volume, il Journal delle modifiche USN per tale volume viene aggiornato con una descrizione della modifica e il nome del file o della directory.
ms.assetid: 9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d
title: Journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5052ec87830a822270071a6ee00f1c3f7cffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884898"
---
# <a name="change-journals"></a>Journal delle modifiche

Un'applicazione di backup automatico è un esempio di programma che deve verificare la presenza di modifiche allo stato di un volume per eseguirne l'attività. Il metodo di forza bruta per verificare le modifiche nelle directory o nei file consiste nell'eseguire la scansione dell'intero volume. Questo approccio, tuttavia, non è spesso accettabile a causa della riduzione delle prestazioni del sistema. Un altro metodo prevede che l'applicazione registri una notifica di directory (chiamando le funzioni [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) o [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) ) per le directory di cui eseguire il backup. Questa operazione è più efficiente rispetto al primo metodo, tuttavia, richiede l'esecuzione di un'applicazione in qualsiasi momento. Inoltre, se è necessario eseguire il backup di un numero elevato di directory e file, la quantità di sovraccarico di elaborazione e memoria per tale applicazione potrebbe causare una riduzione delle prestazioni del sistema operativo.

Per evitare questi svantaggi, il file system NTFS gestisce un journal delle modifiche del numero di sequenza di aggiornamento (USN). Quando viene apportata una modifica a un file o a una directory in un volume, il Journal delle modifiche USN per tale volume viene aggiornato con una descrizione della modifica e il nome del file o della directory.

I journal delle modifiche sono necessari anche per ripristinare file system indicizzazione, ad esempio dopo un errore del computer o del volume. La possibilità di recuperare l'indicizzazione significa che il file system può evitare il processo che richiede molto tempo di reindicizzare l'intero volume in tali casi.

Negli argomenti seguenti vengono illustrati i journal delle modifiche.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                             | Descrizione                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modificare i record del Journal](change-journal-records.md)<br/>                                                                   | Quando vengono aggiunti, eliminati e modificati file, directory e altri oggetti di file system NTFS, il file system NTFS immette i record del journal delle modifiche nei flussi, uno per ogni volume del computer.<br/>                                           |
| [Utilizzo dell'identificatore del journal delle modifiche](using-the-change-journal-identifier.md)<br/>                                         | Il file system NTFS associa un identificatore a 64 bit senza segno a ogni Journal delle modifiche.<br/>                                                                                                                                                   |
| [Creazione, modifica ed eliminazione di un journal delle modifiche](creating-modifying-and-deleting-a-change-journal.md)<br/>             | Gli amministratori possono creare, eliminare e ricreare i journal delle modifiche.<br/>                                                                                                                                                                         |
| [Ottenere un handle del volume per le operazioni del journal delle modifiche](obtaining-a-volume-handle-for-change-journal-operations.md)<br/> | Per ottenere un handle per un volume da utilizzare con le operazioni del journal delle modifiche USN (Update Sequence Number), chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il parametro *lpFileName* impostato su una stringa nel formato seguente: \\ \\ . \\ *X*.<br/> |
| [Operazioni Journal delle modifiche](change-journal-operations.md)<br/>                                                             | Codici e strutture di controllo da utilizzare con il Journal delle modifiche del numero di sequenza di aggiornamento (USN) file system NTFS.<br/>                                                                                                                                |



 

 

 




