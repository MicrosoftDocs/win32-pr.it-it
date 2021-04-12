---
description: Se un'applicazione richiede blocchi opportunistici, è necessario aprire tutti i file per cui richiede blocchi per l'input e l'output sovrapposti usando la funzione CreateFile con il flag FILE \_ \_ sovrapposto.
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Operazioni di blocco opportunistiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529137"
---
# <a name="opportunistic-lock-operations"></a><span data-ttu-id="7fbf0-103">Operazioni di blocco opportunistiche</span><span class="sxs-lookup"><span data-stu-id="7fbf0-103">Opportunistic Lock Operations</span></span>

<span data-ttu-id="7fbf0-104">Se un'applicazione richiede blocchi opportunistici, è necessario aprire tutti i file per cui richiede blocchi per l'input e l'output sovrapposti usando la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag **file \_ \_ sovrapposto** .</span><span class="sxs-lookup"><span data-stu-id="7fbf0-104">If an application requests opportunistic locks, all files for which it requests locks must be opened for overlapped (asynchronous) input and output by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_OVERLAPPED** flag.</span></span> <span data-ttu-id="7fbf0-105">Dopo l'apertura dei file per un'operazione sovrapposta, è possibile usare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con uno dei seguenti codici di controllo per lavorare con i blocchi opportunistici di tali file:</span><span class="sxs-lookup"><span data-stu-id="7fbf0-105">After the files are opened for overlapped operation, you can use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with one of the following control codes to work with those files' opportunistic locks:</span></span>

<dl>

[<span data-ttu-id="7fbf0-106">**\_ \_ chiusura ACK FSCTL \_ OPBATCH \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-106">**FSCTL\_OPBATCH\_ACK\_CLOSE\_PENDING**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[<span data-ttu-id="7fbf0-107">**FSCTL \_ blocco opportunistico \_ break \_ ACK \_ No \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-107">**FSCTL\_OPLOCK\_BREAK\_ACK\_NO\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[<span data-ttu-id="7fbf0-108">**\_conferma FSCTL \_ blocco opportunistico \_**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-108">**FSCTL\_OPLOCK\_BREAK\_ACKNOWLEDGE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[<span data-ttu-id="7fbf0-109">**notifica di FSCTL \_ blocco opportunistico \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-109">**FSCTL\_OPLOCK\_BREAK\_NOTIFY**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[<span data-ttu-id="7fbf0-110">**\_ \_ blocco opportunistico batch richieste \_ FSCTL**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-110">**FSCTL\_REQUEST\_BATCH\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[<span data-ttu-id="7fbf0-111">**\_ \_ blocco opportunistico filtro richieste \_ FSCTL**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-111">**FSCTL\_REQUEST\_FILTER\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[<span data-ttu-id="7fbf0-112">**\_blocco opportunistico richiesta \_ FSCTL**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-112">**FSCTL\_REQUEST\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[<span data-ttu-id="7fbf0-113">**FSCTL \_ richiesta \_ blocco opportunistico \_ livello \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-113">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_1**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[<span data-ttu-id="7fbf0-114">**FSCTL \_ richiesta \_ blocco opportunistico \_ livello \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7fbf0-114">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
