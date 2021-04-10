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
# <a name="distributed-file-system-control-codes"></a><span data-ttu-id="68f59-103">Codici di controllo file system distribuito</span><span class="sxs-lookup"><span data-stu-id="68f59-103">Distributed File System Control Codes</span></span>

<span data-ttu-id="68f59-104">Di seguito sono riportati i codici di controllo file system distribuito (DFS):</span><span class="sxs-lookup"><span data-stu-id="68f59-104">The following are the Distributed File System (DFS) control codes:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="68f59-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="68f59-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="68f59-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span><span class="sxs-lookup"><span data-stu-id="68f59-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span></span>](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

<span data-ttu-id="68f59-107">Il codice di controllo [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) può ottenere le stesse informazioni della funzione [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , ma può fornire prestazioni migliori in alcune configurazioni con latenze elevate per i server DFS.</span><span class="sxs-lookup"><span data-stu-id="68f59-107">The [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="68f59-108">Non è consigliabile usare il codice di controllo **FSCTL_DFS_GET_PKT_ENTRY_STATE** , a meno che non si verifichino problemi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="68f59-108">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="68f59-109">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="68f59-109">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span>

</dd> </dl>