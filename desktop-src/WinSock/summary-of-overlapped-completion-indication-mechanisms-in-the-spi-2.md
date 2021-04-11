---
description: Riepilogo dei meccanismi di indicazione di completamento sovrapposti in Windows Sockets (Winsock) SPI.
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Riepilogo dei meccanismi di indicazione di completamento sovrapposti in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129115"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a><span data-ttu-id="e1807-103">Riepilogo dei meccanismi di indicazione di completamento sovrapposti in SPI</span><span class="sxs-lookup"><span data-stu-id="e1807-103">Summary of Overlapped Completion Indication Mechanisms in the SPI</span></span>

<span data-ttu-id="e1807-104">Nella tabella seguente viene riepilogata la semantica di completamento per un socket sovrapposto, che mostra le varie combinazioni di *lpOverlapped*, **hEvent** e *il lpCompletionRoutine*.</span><span class="sxs-lookup"><span data-stu-id="e1807-104">The following table summarizes the completion semantics for an overlapped socket, showing the various combination of *lpOverlapped*, **hEvent**, and *lpCompletionRoutine*.</span></span>



| <span data-ttu-id="e1807-105">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="e1807-105">*lpOverlapped*</span></span> | <span data-ttu-id="e1807-106">**hEvent**</span><span class="sxs-lookup"><span data-stu-id="e1807-106">**hEvent**</span></span>     | <span data-ttu-id="e1807-107">*Il lpCompletionRoutine*</span><span class="sxs-lookup"><span data-stu-id="e1807-107">*lpCompletionRoutine*</span></span> | <span data-ttu-id="e1807-108">Indicazione di completamento</span><span class="sxs-lookup"><span data-stu-id="e1807-108">Completion indication</span></span>                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1807-109">NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-109">NULL</span></span>           | <span data-ttu-id="e1807-110">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="e1807-110">Not applicable</span></span> | <span data-ttu-id="e1807-111">Ignorato</span><span class="sxs-lookup"><span data-stu-id="e1807-111">Ignored</span></span>               | <span data-ttu-id="e1807-112">L'operazione viene completata in modo sincrono, ovvero si comporta come se fosse un socket non sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="e1807-112">Operation completes synchronously, that is, it behaves as if it were a nonoverlapped socket.</span></span>                                                                                                                                 |
| <span data-ttu-id="e1807-113">NOT NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-113">not NULL</span></span>       | <span data-ttu-id="e1807-114">NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-114">NULL</span></span>           | <span data-ttu-id="e1807-115">NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-115">NULL</span></span>                  | <span data-ttu-id="e1807-116">L'operazione è stata completata, ma non è disponibile alcun meccanismo di completamento supportato da Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="e1807-116">Operation completes overlapped, but there is no Windows Sockets 2-supported completion mechanism.</span></span> <span data-ttu-id="e1807-117">Il meccanismo della porta di completamento (se supportato) può essere usato in questo caso, altrimenti non sarà presente alcuna notifica di completamento.</span><span class="sxs-lookup"><span data-stu-id="e1807-117">The completion port mechanism (if supported) may be used in this case, otherwise there will be no completion notification.</span></span> |
| <span data-ttu-id="e1807-118">NOT NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-118">not NULL</span></span>       | <span data-ttu-id="e1807-119">NOT NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-119">not NULL</span></span>       | <span data-ttu-id="e1807-120">NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-120">NULL</span></span>                  | <span data-ttu-id="e1807-121">L'operazione è stata completata e viene eseguita la notifica tramite un oggetto evento di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="e1807-121">Operation completes overlapped, notification by signaling event object.</span></span>                                                                                                                                                      |
| <span data-ttu-id="e1807-122">NOT NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-122">not NULL</span></span>       | <span data-ttu-id="e1807-123">Ignorato</span><span class="sxs-lookup"><span data-stu-id="e1807-123">Ignored</span></span>        | <span data-ttu-id="e1807-124">NOT NULL</span><span class="sxs-lookup"><span data-stu-id="e1807-124">not NULL</span></span>              | <span data-ttu-id="e1807-125">Il completamento dell'operazione è sovrapposto, notifica pianificando la routine di completamento.</span><span class="sxs-lookup"><span data-stu-id="e1807-125">Operation completes overlapped, notification by scheduling completion routine.</span></span>                                                                                                                                               |



 

 

 



