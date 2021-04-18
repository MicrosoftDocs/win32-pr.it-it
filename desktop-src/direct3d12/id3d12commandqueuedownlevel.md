---
title: Interfaccia ID3D12CommandQueueDownlevel
description: Fornisce un meccanismo di presentazione specifico di Windows 7.
keywords:
- Interfaccia ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322163"
---
# <a name="id3d12commandqueuedownlevel-interface"></a><span data-ttu-id="47a30-104">Interfaccia ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="47a30-104">ID3D12CommandQueueDownlevel interface</span></span>

<span data-ttu-id="47a30-105">È possibile accedere a questa interfaccia tramite **QueryInterface** da una [coda di comandi Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) quando si usa [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="47a30-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 command queue](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="47a30-106">Fornisce un meccanismo di presentazione specifico di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="47a30-106">It provides a Windows-7-specific present mechanism.</span></span>

### <a name="methods"></a><span data-ttu-id="47a30-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="47a30-107">Methods</span></span>

<span data-ttu-id="47a30-108">L'interfaccia **ID3D12CommandQueueDownlevel** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="47a30-108">The **ID3D12CommandQueueDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="47a30-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="47a30-109">Method</span></span> | <span data-ttu-id="47a30-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47a30-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="47a30-111">**Presente**</span><span class="sxs-lookup"><span data-stu-id="47a30-111">**Present**</span></span>](id3d12commandqueuedownlevel-present.md) | <span data-ttu-id="47a30-112">Copia il contenuto da una risorsa Texture2D di D3D12 in una finestra.</span><span class="sxs-lookup"><span data-stu-id="47a30-112">Copies contents from a D3D12 Texture2D resource into a window.</span></span> |

## <a name="requirements"></a><span data-ttu-id="47a30-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47a30-113">Requirements</span></span>

| <span data-ttu-id="47a30-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="47a30-114">Requirement</span></span> | <span data-ttu-id="47a30-115">Valore</span><span class="sxs-lookup"><span data-stu-id="47a30-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="47a30-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47a30-116">Header</span></span> | <span data-ttu-id="47a30-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="47a30-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="47a30-118">DLL</span><span class="sxs-lookup"><span data-stu-id="47a30-118">DLL</span></span>    | <span data-ttu-id="47a30-119">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="47a30-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="47a30-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47a30-120">See also</span></span>
* [<span data-ttu-id="47a30-121">Interfacce Direct3D 12 su Windows 7</span><span class="sxs-lookup"><span data-stu-id="47a30-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="47a30-122">Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="47a30-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="47a30-123">Direct3D 12 in Windows 7</span><span class="sxs-lookup"><span data-stu-id="47a30-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
