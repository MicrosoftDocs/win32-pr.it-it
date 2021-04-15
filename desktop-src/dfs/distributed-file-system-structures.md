---
description: Di seguito sono riportate le strutture file system distribuito DFS
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Strutture di file system distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483772"
---
# <a name="distributed-file-system-structures"></a>Strutture di file system distribuito

Di seguito sono riportate le strutture file system distribuito (DFS):

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Buffer di input utilizzato con il codice di controllo [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dd> <dt>

[Struttura _DFS_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Contiene il nome di una radice file system distribuito (DFS) o di un collegamento.

</dd> <dt>

[Struttura _DFS_INFO_2](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Contiene informazioni su una radice o un collegamento file system distribuito (DFS). Questa struttura contiene il nome, lo stato e il numero di destinazioni DFS per la radice o il collegamento.

</dd> <dt>

[Struttura _DFS_INFO_3](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Contiene informazioni su una radice o un collegamento file system distribuito (DFS). Questa struttura contiene il nome, lo stato, il numero di destinazioni DFS e le informazioni su ogni destinazione della radice o del collegamento.

</dd> <dt>

[Struttura _DFS_INFO_4](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Contiene informazioni su una radice o un collegamento file system distribuito (DFS). Questa struttura contiene il nome, lo stato, il **GUID**, il timeout, il numero di destinazioni e le informazioni su ogni destinazione della radice o del collegamento.

</dd> <dt>

[Struttura _DFS_INFO_5](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Contiene informazioni su una radice o un collegamento file system distribuito (DFS). Questa struttura contiene le proprietà nome, stato, **GUID**, timeout, spazio dei nomi/radice/collegamento, dimensione metadati e numero di destinazioni per la radice o il collegamento.

</dd> <dt>

[Struttura _DFS_INFO_6](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Contiene informazioni su una radice o un collegamento file system distribuito (DFS). Questa struttura contiene le proprietà nome, stato, **GUID**, timeout, spazio dei nomi/radice/collegamento, dimensione metadati, numero di destinazioni e informazioni su ogni destinazione della radice o del collegamento.

</dd> <dt>

[Struttura _DFS_INFO_7](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Contiene informazioni su uno spazio dei nomi DFS. Questa struttura contiene il **GUID** della versione per i metadati per lo spazio dei nomi.

</dd> <dt>

[Struttura _DFS_INFO_8](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Contiene il nome, lo stato, il **GUID**, il timeout, i flag delle proprietà, le dimensioni dei metadati, le informazioni di destinazione DFS e il descrittore di sicurezza del punto di analisi del collegamento per una radice o un collegamento.

</dd> <dt>

[Struttura _DFS_INFO_9](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Contiene il nome, lo stato, il **GUID**, il timeout, i flag delle proprietà, le dimensioni dei metadati, le informazioni di destinazione DFS, il descrittore di sicurezza del reparse point del collegamento e un elenco di destinazioni DFS per un collegamento o una radice.

</dd> <dt>

[Struttura _DFS_INFO_50](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Contiene la versione dei metadati DFS e le funzionalità di uno spazio dei nomi DFS esistente.

</dd> <dt>

[Struttura _DFS_INFO_100](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Contiene un commento associato a una radice file system distribuito (DFS) o a un collegamento.

</dd> <dt>

[Struttura _DFS_INFO_101](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Descrive lo stato di archiviazione in una radice DFS, un collegamento, una destinazione radice o una destinazione del collegamento.

</dd> <dt>

[Struttura _DFS_INFO_102](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Contiene un valore di timeout da associare a una radice file system distribuito (DFS) o a un collegamento in una radice DFS denominata.

</dd> <dt>

[Struttura _DFS_INFO_103](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Contiene proprietà che impostano comportamenti specifici per un collegamento o una radice DFS.

</dd> <dt>

[Struttura _DFS_INFO_104](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Contiene la priorità di una destinazione radice DFS o di una destinazione del collegamento.

</dd> <dt>

[Struttura _DFS_INFO_105](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Contiene informazioni su un collegamento o una radice DFS, inclusi il commento, lo stato, il timeout e i comportamenti DFS specificati dai flag della proprietà.

</dd> <dt>

[Struttura _DFS_INFO_106](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Contiene lo stato di archiviazione e la priorità per una destinazione radice DFS o una destinazione del collegamento. Questa struttura viene utilizzata solo con la funzione [**NetDfsSetInfo**](netdfssetinfo.md) .

</dd> <dt>

[Struttura _DFS_INFO_107](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Contiene informazioni su un collegamento o una radice DFS, inclusi il commento, lo stato, il timeout, i flag di proprietà e il descrittore di sicurezza del punto di analisi del collegamento.

</dd> <dt>

[Struttura _DFS_INFO_150](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Contiene il descrittore di sicurezza per il punto di analisi di un collegamento DFS.

</dd> <dt>

[Struttura _DFS_INFO_200](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Contiene il nome di uno spazio dei nomi di file system distribuito basato su dominio (DFS).

</dd> <dt>

[Struttura _DFS_INFO_300](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Contiene il nome e il tipo (basati su dominio o autonomo) di uno spazio dei nomi DFS.

</dd> <dt>

[Struttura _DFS_STORAGE_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Contiene informazioni su una radice DFS o una destinazione del collegamento in uno spazio dei nomi DFS o dalla cache gestita dal client DFS.

</dd> <dt>

[Struttura _DFS_STORAGE_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Contiene informazioni su una destinazione DFS, inclusi il nome del server di destinazione DFS e il nome della condivisione, nonché lo stato e la priorità della destinazione.

</dd> <dt>

[Struttura _DFS_SUPPORTED_NAMESPACE_VERSION_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Contiene informazioni sulla versione per uno spazio dei nomi DFS.

</dd> <dt>

[Struttura _DFS_TARGET_PRIORITY](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Contiene la classe di priorità e il rango di una specifica destinazione DFS.

</dd> </dl>
