---
description: Determinare se un file system supporta i file sparse chiamando la funzione GetVolumeInformation.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Operazioni su file sparse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c23d26fc1c52db32ca7674aec2fc487a826e9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307935"
---
# <a name="sparse-file-operations"></a>Operazioni su file sparse

Per determinare se un file system supporta i file sparse, chiamare la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il file supporta il flag di bit dei **\_ \_ \_ file sparse** restituito tramite il parametro *lpFileSystemFlags* .

La maggior parte delle applicazioni non è in grado di riconoscere file sparse e non creerà file sparse. Il fatto che un'applicazione legga un file sparse è trasparente per l'applicazione. Un'applicazione che conosce i file sparse deve determinare se il set di dati è adatto per essere mantenuto in un file sparse. Una volta eseguita questa determinazione, l'applicazione deve dichiarare in modo esplicito un file come di tipo sparse, usando il codice di controllo [**FSCTL \_ set \_ sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) .

Dopo che un'applicazione ha impostato un file di tipo sparse, l'applicazione può usare il [**FSCTL \_ set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) Control Code per impostare un'area del file su zero. Inoltre, l'applicazione può usare il codice di controllo degli [**\_ \_ \_ intervalli allocati per query FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) per velocizzare la ricerca di dati diversi da zero nel file sparse.

Quando si esegue un'operazione di scrittura (con una funzione o un'operazione diversa da [**FSCTL, \_ impostare \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) i cui dati sono costituiti solo da zero, gli zeri verranno scritti sul disco per l'intera durata della scrittura. Per azzerare un intervallo del file e mantenere la densità, usare **FSCTL \_ set \_ zero \_ Data**.

Un'applicazione in grado di riconoscere la sparsità può anche impostare un file esistente come sparse. Se un'applicazione imposta un file di tipo sparse, deve quindi eseguire l'analisi del file per le aree che contengono zeri e usare [**FSCTL \_ set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) per reimpostare tali aree, in modo da poter anche deallocare l'archiviazione su disco fisico. Questa conversione deve essere eseguita da un'applicazione aggiornata a riconoscimento file sparse.

Quando si esegue un'operazione di lettura da una parte azzerata di un file sparse, il sistema operativo potrebbe non essere in grado di leggere dall'unità disco rigido. Il sistema riconosce invece che la parte del file da leggere contiene zeri e restituisce un buffer pieno di zeri senza eseguire effettivamente la lettura dal disco.

Come per qualsiasi altro file, il sistema può scrivere o leggere i dati da qualsiasi posizione in un file sparse. I dati diversi da zero scritti in una porzione precedentemente azzerata del file possono comportare l'allocazione dello spazio su disco. Gli zeri scritti su dati diversi da zero (solo con [**FSCTL \_ set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) possono causare la deallocazione dello spazio su disco.

> [!Note]  
> È possibile che l'applicazione mantenga la scarsità scrivendo zeri con [**FSCTL \_ set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data).

 

Gli strumenti di deframmentazione che gestiscono i file compressi nei file system NTFS gestiranno correttamente i file sparse nei volumi file system NTFS. I file sparse di grandi dimensioni e molto frammentati possono superare la limitazione NTFS sugli extent del disco prima dell'utilizzo dello spazio disponibile. Per ulteriori informazioni, vedere l'argomento relativo all' [estensione di un file potrebbe non riuscire con l'errore "disco completo" anche se il volume dispone di spazio libero](https://support.microsoft.com/default.aspx/kb/957180).

 

 
