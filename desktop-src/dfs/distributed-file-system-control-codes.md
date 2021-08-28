---
title: file system distribuito di controllo
description: file system distribuito di controllo DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d0a429bdb1e203d9b89f77e951d422cf3c0cef05cd5de5de39b537bb405f6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853531"
---
# <a name="distributed-file-system-control-codes"></a>file system distribuito di controllo

Di seguito sono riportati i file system distribuito di controllo DFS:

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

Il [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) di controllo può ottenere le stesse informazioni della funzione [**NetDfsGetClientInfo,**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) ma può offrire prestazioni migliori in alcune configurazioni con latenze elevate per i server DFS. Non è consigliabile usare il codice di controllo **FSCTL_DFS_GET_PKT_ENTRY_STATE** a meno che non si siano verificati problemi di prestazioni.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

</dd> </dl>