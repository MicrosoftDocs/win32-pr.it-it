---
title: Interfaccia IDODownload
description: Utilizzato per avviare e gestire un download.
keywords:
- Interfaccia IDODownload
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337646"
---
# <a name="idodownload-interface"></a><span data-ttu-id="69a58-104">Interfaccia IDODownload</span><span class="sxs-lookup"><span data-stu-id="69a58-104">IDODownload interface</span></span>

<span data-ttu-id="69a58-105">L'interfaccia **IDODownload** viene utilizzata per avviare e gestire un download.</span><span class="sxs-lookup"><span data-stu-id="69a58-105">The **IDODownload** interface is used to start and manage a download.</span></span>

## <a name="methods"></a><span data-ttu-id="69a58-106">Metodi</span><span class="sxs-lookup"><span data-stu-id="69a58-106">Methods</span></span>

<span data-ttu-id="69a58-107">L'interfaccia **IDODownload** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="69a58-107">The **IDODownload** interface has these methods.</span></span>

| <span data-ttu-id="69a58-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="69a58-108">Method</span></span> | <span data-ttu-id="69a58-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69a58-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="69a58-110">IDODownload:: Abort</span><span class="sxs-lookup"><span data-stu-id="69a58-110">IDODownload::Abort</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="69a58-111">Interrompe il download.</span><span class="sxs-lookup"><span data-stu-id="69a58-111">Aborts the download.</span></span> |
| [<span data-ttu-id="69a58-112">IDODownload:: Finalize</span><span class="sxs-lookup"><span data-stu-id="69a58-112">IDODownload::Finalize</span></span>](./nf-do-idodownload-finalize.md) | <span data-ttu-id="69a58-113">Completa il download.</span><span class="sxs-lookup"><span data-stu-id="69a58-113">Finalizes the download.</span></span> |
| [<span data-ttu-id="69a58-114">IDODownload:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="69a58-114">IDODownload::GetProperty</span></span>](./nf-do-idodownload-getproperty.md) | <span data-ttu-id="69a58-115">Recupera un puntatore a un **Variant** che contiene una specifica proprietà di download.</span><span class="sxs-lookup"><span data-stu-id="69a58-115">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span> |
| [<span data-ttu-id="69a58-116">IDODownload:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="69a58-116">IDODownload::GetStatus</span></span>](./nf-do-idodownload-getstatus.md) | <span data-ttu-id="69a58-117">Recupera un puntatore a una struttura **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download.</span><span class="sxs-lookup"><span data-stu-id="69a58-117">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span> |
| [<span data-ttu-id="69a58-118">IDODownload::P ause</span><span class="sxs-lookup"><span data-stu-id="69a58-118">IDODownload::Pause</span></span>](./nf-do-idodownload-pause.md) | <span data-ttu-id="69a58-119">Sospende il download.</span><span class="sxs-lookup"><span data-stu-id="69a58-119">Pauses the download.</span></span> |
| [<span data-ttu-id="69a58-120">IDODownload:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="69a58-120">IDODownload::SetProperty</span></span>](./nf-do-idodownload-setproperty.md) | <span data-ttu-id="69a58-121">Imposta una proprietà di download.</span><span class="sxs-lookup"><span data-stu-id="69a58-121">Sets a download property.</span></span> |
| [<span data-ttu-id="69a58-122">IDODownload:: Start</span><span class="sxs-lookup"><span data-stu-id="69a58-122">IDODownload::Start</span></span>](./nf-do-idodownload-start.md) | <span data-ttu-id="69a58-123">Avvia o riprende un download.</span><span class="sxs-lookup"><span data-stu-id="69a58-123">Starts or resumes a download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="69a58-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69a58-124">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="69a58-125">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="69a58-125">**Minimum supported client**</span></span> | <span data-ttu-id="69a58-126">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="69a58-126">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="69a58-127">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="69a58-127">**Minimum supported server**</span></span> | <span data-ttu-id="69a58-128">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="69a58-128">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="69a58-129">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="69a58-129">**Header**</span></span> | <span data-ttu-id="69a58-130">Do. h</span><span class="sxs-lookup"><span data-stu-id="69a58-130">Do.h</span></span> |