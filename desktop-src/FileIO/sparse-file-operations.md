---
description: Determinare se file system supporta file sparse chiamando la funzione GetVolumeInformation.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Operazioni su file di tipo sparse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9835d550a414c047e578eb90fc9b55afbefb760d31d8333a290f00da7162f839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015109"
---
# <a name="sparse-file-operations"></a>Operazioni su file di tipo sparse

Per determinare se un file system supporta file sparse, chiamare la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il flag di bit **FILE \_ SUPPORTS \_ SPARSE \_ FILES** restituito tramite il parametro *lpFileSystemFlags.*

La maggior parte delle applicazioni non è a conoscenza dei file sparse e non crea file sparse. Il fatto che un'applicazione leggono un file sparse è trasparente per l'applicazione. Un'applicazione che è in grado di riconoscere i file di tipo sparse deve determinare se il relativo set di dati è adatto per essere mantenuto in un file sparse. Dopo la determinazione, l'applicazione deve dichiarare in modo esplicito un file come sparse, usando il codice di controllo [**FSCTL \_ SET \_ SPARSE.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)

Dopo che un'applicazione ha impostato un file come sparse, l'applicazione può usare il codice di controllo [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) per impostare un'area del file su zero. Inoltre, l'applicazione può usare il codice di controllo [**FSCTL \_ QUERY \_ ALLOCATED \_ RANGES**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) per velocizzare le ricerche di dati diversi da zero nel file sparse.

Quando si esegue un'operazione di scrittura (con una funzione o un'operazione diversa da [**FSCTL \_ SET \_ ZERO \_ DATA)**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)i cui dati sono costituiti solo da zero, sul disco verranno scritti zeri per l'intera lunghezza della scrittura. Per azzerare un intervallo del file e mantenere la sparsezza, usare **FSCTL \_ SET \_ ZERO \_ DATA**.

Un'applicazione in grado di riconoscere il tipo di dati di tipo sparse può anche impostare un file esistente come sparse. Se un'applicazione imposta un file esistente come sparse, deve quindi analizzare il file per cercare le aree che contengono zeri e usare [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) per reimpostare tali aree, deallocando eventualmente una parte dello spazio di archiviazione su disco fisico. Questa conversione deve essere eseguita da un'applicazione aggiornata al riconoscimento di file sparse.

Quando si esegue un'operazione di lettura da una parte azzerato di un file sparse, il sistema operativo potrebbe non leggere dall'unità disco rigido. Al contrario, il sistema riconosce che la parte del file da leggere contiene zeri e restituisce un buffer pieno di zeri senza effettivamente leggere dal disco.

Come per qualsiasi altro file, il sistema può scrivere o leggere dati da qualsiasi posizione in un file sparse. La scrittura di dati diversi da zero in una parte del file azzerato in precedenza può comportare l'allocazione di spazio su disco. La scrittura di zeri su dati diversi da zero (solo con [**FSCTL \_ SET \_ ZERO \_ DATA)**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)può comportare una deallocazione dello spazio su disco.

> [!Note]  
> È l'applicazione a gestire la sparsezza scrivendo zeri con [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data).

 

Gli strumenti di deframmentazione che gestiscono i file compressi nei file system NTFS gestiranno correttamente i file sparse nei volumi FILE SYSTEM NTFS. I file sparse di grandi dimensioni e altamente frammentati possono superare la limitazione NTFS sugli extent del disco prima che venga usato lo spazio disponibile. Per altre informazioni, vedere L'estensione di un file potrebbe non riuscire con [l'errore "Disco pieno" anche se il volume ha spazio libero.](https://support.microsoft.com/default.aspx/kb/957180)

 

 
