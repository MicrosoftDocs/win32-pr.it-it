---
description: Di seguito sono riportate le file system distribuito DFS
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: file system distribuito strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1561a4586cc03304c6aa1c1e323eb42fd09766df0cc3c7210636367337873a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541282"
---
# <a name="distributed-file-system-structures"></a>file system distribuito strutture

Di seguito sono riportate le file system distribuito (DFS) seguenti:

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Buffer di input usato con il [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) di controllo
</dd> <dt>

[_DFS_INFO_1 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Contiene il nome di un file system distribuito radice (DFS) o di un collegamento.

</dd> <dt>

[_DFS_INFO_2 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Contiene informazioni su una radice file system distribuito (DFS) o un collegamento. Questa struttura contiene il nome, lo stato e il numero di destinazioni DFS per la radice o il collegamento.

</dd> <dt>

[_DFS_INFO_3 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Contiene informazioni su una radice file system distribuito (DFS) o un collegamento. Questa struttura contiene il nome, lo stato, il numero di destinazioni DFS e le informazioni su ogni destinazione della radice o del collegamento.

</dd> <dt>

[_DFS_INFO_4 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Contiene informazioni su una radice file system distribuito (DFS) o un collegamento. Questa struttura contiene il nome, lo stato, **il GUID,** il timeout, il numero di destinazioni e le informazioni su ogni destinazione della radice o del collegamento.

</dd> <dt>

[_DFS_INFO_5 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Contiene informazioni su una radice file system distribuito (DFS) o un collegamento. Questa struttura contiene il nome, lo stato, **il GUID,** il timeout, le proprietà dello spazio dei nomi/radice/collegamento, le dimensioni dei metadati e il numero di destinazioni per la radice o il collegamento.

</dd> <dt>

[_DFS_INFO_6 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Contiene informazioni su una radice file system distribuito (DFS) o un collegamento. Questa struttura contiene il nome, lo stato, **il GUID,** il timeout, le proprietà dello spazio dei nomi/radice/collegamento, le dimensioni dei metadati, il numero di destinazioni e le informazioni su ogni destinazione della radice o del collegamento.

</dd> <dt>

[_DFS_INFO_7 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Contiene informazioni su uno spazio dei nomi DFS. Questa struttura contiene il GUID della **versione per** i metadati per lo spazio dei nomi.

</dd> <dt>

[_DFS_INFO_8 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Contiene il nome, lo stato, **il GUID,** il timeout, i flag di proprietà, le dimensioni dei metadati, le informazioni sulla destinazione DFS e il descrittore di sicurezza del reparse point di collegamento per una radice o un collegamento.

</dd> <dt>

[_DFS_INFO_9 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Contiene il nome, lo stato, **il GUID,** il timeout, i flag di proprietà, le dimensioni dei metadati, le informazioni sulla destinazione DFS, il descrittore di sicurezza del reparse point di collegamento e un elenco di destinazioni DFS per una radice o un collegamento.

</dd> <dt>

[_DFS_INFO_50 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Contiene la versione dei metadati DFS e le funzionalità di uno spazio dei nomi DFS esistente.

</dd> <dt>

[_DFS_INFO_100 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Contiene un commento associato a una radice file system distribuito (DFS) o a un collegamento.

</dd> <dt>

[_DFS_INFO_101 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Descrive lo stato di archiviazione in una radice DFS, un collegamento, una destinazione radice o una destinazione di collegamento.

</dd> <dt>

[_DFS_INFO_102 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Contiene un valore di timeout da associare a una radice file system distribuito (DFS) o a un collegamento in una radice DFS denominata.

</dd> <dt>

[_DFS_INFO_103 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Contiene proprietà che impostano comportamenti specifici per una radice o un collegamento DFS.

</dd> <dt>

[_DFS_INFO_104 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Contiene la priorità di una destinazione radice DFS o di una destinazione di collegamento.

</dd> <dt>

[_DFS_INFO_105 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Contiene informazioni su una radice o un collegamento DFS, inclusi commenti, stato, timeout e comportamenti DFS specificati dai flag di proprietà.

</dd> <dt>

[_DFS_INFO_106 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Contiene lo stato di archiviazione e la priorità per una destinazione radice DFS o una destinazione di collegamento. Questa struttura può essere utilizzata solo con la [**funzione NetDfsSetInfo.**](netdfssetinfo.md)

</dd> <dt>

[_DFS_INFO_107 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Contiene informazioni su una radice o un collegamento DFS, inclusi il commento, lo stato, il timeout, i flag di proprietà e il descrittore di sicurezza del reparse point di collegamento.

</dd> <dt>

[_DFS_INFO_150 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Contiene il descrittore di sicurezza per il reparse point di un collegamento DFS.

</dd> <dt>

[_DFS_INFO_200 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Contiene il nome di uno spazio dei nomi file system distribuito (DFS) basato su dominio.

</dd> <dt>

[_DFS_INFO_300 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Contiene il nome e il tipo (basato su dominio o autonomo) di uno spazio dei nomi DFS.

</dd> <dt>

[_DFS_STORAGE_INFO struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Contiene informazioni su una radice DFS o una destinazione di collegamento in uno spazio dei nomi DFS o dalla cache gestita dal client DFS.

</dd> <dt>

[_DFS_STORAGE_INFO_1 struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Contiene informazioni su una destinazione DFS, inclusi il nome del server di destinazione DFS e il nome della condivisione, nonché lo stato e la priorità della destinazione.

</dd> <dt>

[_DFS_SUPPORTED_NAMESPACE_VERSION_INFO struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Contiene informazioni sulla versione per uno spazio dei nomi DFS.

</dd> <dt>

[_DFS_TARGET_PRIORITY struttura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Contiene la classe di priorità e la classificazione di una destinazione DFS specifica.

</dd> </dl>
