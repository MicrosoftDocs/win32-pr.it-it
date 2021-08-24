---
description: L'file system NTFS associa un identificatore senza segno a 64 bit a ogni journal delle modifiche.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Utilizzo dell'identificatore del journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483c171b69bcee0faf8df9f325d4ee8ffcb6e904f6aa0cd3c720b83df326e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015069"
---
# <a name="using-the-change-journal-identifier"></a>Utilizzo dell'identificatore del journal delle modifiche

L'file system NTFS associa un identificatore senza segno a 64 bit a ogni journal delle modifiche. Il journal viene contrassegnato con questo identificatore al momento della creazione. Il file system contrassegna il journal con un nuovo identificatore in cui i record USN (Update Sequence Number) esistenti sono o possono essere inutilizzabili.

Ntfs, ad esempio, file system un journal delle modifiche con un nuovo identificatore quando un volume viene spostato da una versione di NTFS a un'altra e quindi di nuovo. Questo spostamento può verificarsi in un ambiente ad avvio doppio o quando si lavora con supporti rimovibili.

Per ottenere l'identificatore del journal delle modifiche corrente in un volume specificato, usare il codice di controllo [**FSCTL \_ QUERY \_ USN \_ JOURNAL.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) Per eseguire questa e tutte le altre operazioni del journal delle modifiche, è necessario disporre dei privilegi di amministratore di sistema. Ciò significa che è necessario essere un membro del gruppo Administrators.

Quando un amministratore elimina e rie crea di nuovo il journal delle modifiche, ad esempio quando il valore USN corrente si avvicina al valore USN massimo possibile, i valori USN iniziano di nuovo da zero. Quando il file system NTFS contrassegna un journal con un nuovo identificatore anziché creare nuovamente il journal, non reimposta l'USN su zero, ma continua dall'USN corrente. In entrambi i casi, tutti gli USN esistenti sono minori di qualsiasi USN futuro.

Quando sono necessarie informazioni su un set specifico di record, usare il codice di controllo [**\_ FSCTL QUERY \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) per ottenere l'identificatore del journal delle modifiche. Usare quindi il [**codice di controllo JOURNAL FSCTL READ \_ \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) per leggere i record del journal di interesse. Il file system NTFS restituisce solo i record validi per il journal specificato dall'identificatore.

L'applicazione necessita sia degli USN dei record che dell'identificatore per leggere il journal. Questo requisito fornisce un controllo di integrità per i casi in cui l'applicazione deve ignorare i record esistenti nel file e in cui i record sono stati scritti nelle istanze precedenti del journal per lo stesso volume.

Per ottenere i record a cui si è interessati, è necessario iniziare dal record meno recente ,ovvero con il numero USN più basso, ed eseguire l'analisi in avanti fino a individuare il primo record di interesse.

 

 
