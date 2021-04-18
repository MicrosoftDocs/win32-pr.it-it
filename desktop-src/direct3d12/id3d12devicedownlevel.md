---
title: Interfaccia ID3D12DeviceDownlevel
description: Fornisce una query delle statistiche di memoria specifica di Windows 7.
keywords:
- Interfaccia ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322162"
---
# <a name="id3d12devicedownlevel-interface"></a><span data-ttu-id="904f7-104">Interfaccia ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="904f7-104">ID3D12DeviceDownlevel interface</span></span>

<span data-ttu-id="904f7-105">È possibile accedere a questa interfaccia tramite **QueryInterface** da un [dispositivo Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) quando si usa [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="904f7-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="904f7-106">Fornisce una query delle statistiche di memoria specifiche di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="904f7-106">It provides a Windows-7-specific memory statistics query.</span></span>

### <a name="methods"></a><span data-ttu-id="904f7-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="904f7-107">Methods</span></span>

<span data-ttu-id="904f7-108">L'interfaccia **ID3D12DeviceDownlevel** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="904f7-108">The **ID3D12DeviceDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="904f7-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="904f7-109">Method</span></span> | <span data-ttu-id="904f7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="904f7-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="904f7-111">**QueryVideoMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="904f7-111">**QueryVideoMemoryInfo**</span></span>](id3d12devicedownlevel-queryvideomemoryinfo.md) | <span data-ttu-id="904f7-112">Fornisce le statistiche sulla memoria in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="904f7-112">Provides memory statistics on Windows 7.</span></span> |

## <a name="requirements"></a><span data-ttu-id="904f7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="904f7-113">Requirements</span></span>

| <span data-ttu-id="904f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="904f7-114">Requirement</span></span> | <span data-ttu-id="904f7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="904f7-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="904f7-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="904f7-116">Header</span></span> | <span data-ttu-id="904f7-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="904f7-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="904f7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="904f7-118">DLL</span></span>    | <span data-ttu-id="904f7-119">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="904f7-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="904f7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="904f7-120">See also</span></span>
* [<span data-ttu-id="904f7-121">Interfacce Direct3D 12 su Windows 7</span><span class="sxs-lookup"><span data-stu-id="904f7-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="904f7-122">Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="904f7-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="904f7-123">Direct3D 12 in Windows 7</span><span class="sxs-lookup"><span data-stu-id="904f7-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
