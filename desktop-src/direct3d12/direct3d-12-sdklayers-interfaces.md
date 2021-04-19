---
title: Interfacce del livello di debug
description: Le interfacce seguenti sono dichiarate in d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2020
ms.locfileid: "106299483"
---
# <a name="debug-layer-interfaces"></a><span data-ttu-id="1de54-103">Interfacce del livello di debug</span><span class="sxs-lookup"><span data-stu-id="1de54-103">Debug Layer interfaces</span></span>

<span data-ttu-id="1de54-104">Le interfacce seguenti sono definite in `d3d12sdklayers.h` .</span><span class="sxs-lookup"><span data-stu-id="1de54-104">The following interfaces are defined in `d3d12sdklayers.h`.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1de54-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1de54-105">In this section</span></span>

| <span data-ttu-id="1de54-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="1de54-106">Topic</span></span> | <span data-ttu-id="1de54-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1de54-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="1de54-108">**ID3D12Debug**</span><span class="sxs-lookup"><span data-stu-id="1de54-108">**ID3D12Debug**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | <span data-ttu-id="1de54-109">Un'interfaccia di debug controlla le impostazioni di debug e convalida lo stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="1de54-109">A debug interface controls debug settings and validates pipeline state.</span></span> <span data-ttu-id="1de54-110">Può essere utilizzato solo se il livello di debug è attivato.</span><span class="sxs-lookup"><span data-stu-id="1de54-110">It can only be used if the debug layer is turned on.</span></span> |
| [<span data-ttu-id="1de54-111">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="1de54-111">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | <span data-ttu-id="1de54-112">Aggiunge la convalida basata su GPU e la sincronizzazione della coda dei comandi dipendenti al livello di debug.</span><span class="sxs-lookup"><span data-stu-id="1de54-112">Adds GPU-based validation and Dependent Command Queue Synchronization to the debug layer.</span></span> |
| [<span data-ttu-id="1de54-113">**ID3D12Debug2**</span><span class="sxs-lookup"><span data-stu-id="1de54-113">**ID3D12Debug2**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | <span data-ttu-id="1de54-114">Aggiunge livelli configurabili di convalida GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="1de54-114">Adds configurable levels of GPU-Based Validation.</span></span> |
| [<span data-ttu-id="1de54-115">**ID3D12Debug3**</span><span class="sxs-lookup"><span data-stu-id="1de54-115">**ID3D12Debug3**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | <span data-ttu-id="1de54-116">Aggiunge alla convalida basata su GPU del livello di debug, alla sincronizzazione della coda dei comandi dipendenti e ai livelli configurabili della convalida basata su GPU.</span><span class="sxs-lookup"><span data-stu-id="1de54-116">Adds to the debug layer GPU-based validation, Dependent Command Queue Synchronization, and configurable levels of GPU-based validation.</span></span> |
| [<span data-ttu-id="1de54-117">**ID3D12DebugCommandList**</span><span class="sxs-lookup"><span data-stu-id="1de54-117">**ID3D12DebugCommandList**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | <span data-ttu-id="1de54-118">Fornisce metodi per monitorare ed eseguire il debug di un elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="1de54-118">Provides methods to monitor and debug a command list.</span></span> |
| [<span data-ttu-id="1de54-119">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="1de54-119">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | <span data-ttu-id="1de54-120">Questa interfaccia consente di modificare le impostazioni aggiuntive del livello di debug dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1de54-120">This interface enables modification of additional command list debug layer settings.</span></span> |
| [<span data-ttu-id="1de54-121">**ID3D12DebugCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="1de54-121">**ID3D12DebugCommandQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | <span data-ttu-id="1de54-122">Fornisce metodi per monitorare ed eseguire il debug di una coda di comandi.</span><span class="sxs-lookup"><span data-stu-id="1de54-122">Provides methods to monitor and debug a command queue.</span></span> |
| [<span data-ttu-id="1de54-123">**ID3D12DebugDevice**</span><span class="sxs-lookup"><span data-stu-id="1de54-123">**ID3D12DebugDevice**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | <span data-ttu-id="1de54-124">Questa interfaccia rappresenta un dispositivo grafico per il debug.</span><span class="sxs-lookup"><span data-stu-id="1de54-124">This interface represents a graphics device for debugging.</span></span> |
| [<span data-ttu-id="1de54-125">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="1de54-125">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | <span data-ttu-id="1de54-126">Specifica le impostazioni del livello di debug a livello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1de54-126">Specifies device-wide debug layer settings.</span></span> |
| [<span data-ttu-id="1de54-127">**ID3D12InfoQueue**</span><span class="sxs-lookup"><span data-stu-id="1de54-127">**ID3D12InfoQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | <span data-ttu-id="1de54-128">Un'interfaccia della coda di informazioni archivia, recupera e filtra i messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="1de54-128">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="1de54-129">La coda è costituita da una coda di messaggi, da uno stack di filtri di archiviazione facoltativo e da uno stack di filtri di recupero facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1de54-129">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> |
| [<span data-ttu-id="1de54-130">**ID3D12SharingContract**</span><span class="sxs-lookup"><span data-stu-id="1de54-130">**ID3D12SharingContract**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | <span data-ttu-id="1de54-131">Parte di un contratto tra i livelli di diagnostica D3D11On12 e gli strumenti di diagnostica grafica.</span><span class="sxs-lookup"><span data-stu-id="1de54-131">Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="1de54-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1de54-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de54-133">Configurazione dell'ambiente di programmazione Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1de54-133">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="1de54-134">Riferimento al livello di debug</span><span class="sxs-lookup"><span data-stu-id="1de54-134">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="1de54-135">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1de54-135">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>