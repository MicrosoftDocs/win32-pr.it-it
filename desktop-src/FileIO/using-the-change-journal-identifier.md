---
description: Il file system NTFS associa un identificatore a 64 bit senza segno a ogni Journal delle modifiche.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Utilizzo dell'identificatore del journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692acf98403e45b6bdafd3cd4791a64dd1beb532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309527"
---
# <a name="using-the-change-journal-identifier"></a>Utilizzo dell'identificatore del journal delle modifiche

Il file system NTFS associa un identificatore a 64 bit senza segno a ogni Journal delle modifiche. Il journal viene contrassegnato con questo identificatore quando viene creato. Il file system timbra il Journal con un nuovo identificatore in cui i record del numero di sequenza di aggiornamento (USN) esistenti sono o possono essere inutilizzabili.

Il file system NTFS, ad esempio, consente di contrassegnare un journal delle modifiche con un nuovo identificatore quando un volume viene spostato da una versione di NTFS a un'altra e quindi viceversa. Tale spostamento può verificarsi in un ambiente a doppio avvio o quando si utilizza un supporto rimovibile.

Per ottenere l'identificatore del journal delle modifiche corrente in un volume specificato, usare il codice di controllo del [**\_ \_ \_ journal USN della query FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) . Per eseguire questa operazione e tutte le altre operazioni Journal delle modifiche, è necessario disporre dei privilegi di amministratore di sistema. Ovvero, è necessario essere un membro del gruppo Administrators.

Quando un amministratore Elimina e ricrea il Journal delle modifiche, ad esempio quando il valore USN corrente si avvicina al valore USN massimo possibile, i valori USN iniziano di nuovo da zero. Quando NTFS file system timbra un journal con un nuovo identificatore anziché ricreare il Journal, non reimposta l'USN su zero, ma continua dall'USN corrente. In entrambi i casi, tutti i USNs esistenti sono inferiori a qualsiasi USNs futura.

Quando sono necessarie informazioni su un set specifico di record, usare il codice di controllo del [**\_ \_ \_ journal USN della query FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) per ottenere l'identificatore del journal delle modifiche. Usare quindi il codice di controllo [**\_ \_ \_ journal USN FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) per leggere i record del journal di interesse. Il file system NTFS restituisce solo i record validi per il Journal specificato dall'identificatore.

Per leggere il Journal, l'applicazione richiede sia il USNs dei record che l'identificatore. Questo requisito fornisce un controllo di integrità nei casi in cui l'applicazione deve ignorare i record esistenti nel file e in cui i record sono stati scritti nelle istanze precedenti del journal per lo stesso volume.

Per ottenere i record a cui si è interessati, è necessario iniziare dal record meno recente, ovvero con l'USN più basso, ed eseguire l'analisi in futuro fino a individuare il primo record di interesse.

 

 
