---
title: Codici di controllo file system distribuito
description: file system distribuito codici di controllo DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe054f87210c40da595dd731b263c485311729a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963213"
---
# <a name="distributed-file-system-control-codes"></a>Codici di controllo file system distribuito

Di seguito sono riportati i codici di controllo file system distribuito (DFS):

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

Il codice di controllo [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) può ottenere le stesse informazioni della funzione [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , ma può fornire prestazioni migliori in alcune configurazioni con latenze elevate per i server DFS. Non è consigliabile usare il codice di controllo **FSCTL_DFS_GET_PKT_ENTRY_STATE** , a meno che non si verifichino problemi di prestazioni.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

</dd> </dl>