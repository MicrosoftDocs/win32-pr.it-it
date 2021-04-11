---
title: DXCoreHardwareID
description: Rappresenta le parti dell'ID hardware PnP per un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117882"
---
# <a name="dxcorehardwareid-structure"></a><span data-ttu-id="507c6-103">Struttura DXCoreHardwareID</span><span class="sxs-lookup"><span data-stu-id="507c6-103">DXCoreHardwareID structure</span></span>

<span data-ttu-id="507c6-104">Rappresenta le parti dell'ID hardware PnP per un adapter.</span><span class="sxs-lookup"><span data-stu-id="507c6-104">Represents the PnP hardware ID parts for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="507c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="507c6-105">Syntax</span></span>

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a><span data-ttu-id="507c6-106">Members</span><span class="sxs-lookup"><span data-stu-id="507c6-106">Members</span></span>

### <a name="vendorid"></a><span data-ttu-id="507c6-107">vendorId</span><span class="sxs-lookup"><span data-stu-id="507c6-107">vendorId</span></span>

<span data-ttu-id="507c6-108">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="507c6-108">Type: **uint32_t\***</span></span>

<span data-ttu-id="507c6-109">ID PCI del fornitore dell'hardware della scheda.</span><span class="sxs-lookup"><span data-stu-id="507c6-109">The PCI ID of the adapter's hardware vendor.</span></span>

### <a name="deviceid"></a><span data-ttu-id="507c6-110">deviceId</span><span class="sxs-lookup"><span data-stu-id="507c6-110">deviceId</span></span>

<span data-ttu-id="507c6-111">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="507c6-111">Type: **uint32_t\***</span></span>

<span data-ttu-id="507c6-112">ID PCI del dispositivo hardware della scheda.</span><span class="sxs-lookup"><span data-stu-id="507c6-112">The PCI ID of the adapter's hardware device.</span></span>

### <a name="subsysid"></a><span data-ttu-id="507c6-113">subSysId</span><span class="sxs-lookup"><span data-stu-id="507c6-113">subSysId</span></span>

<span data-ttu-id="507c6-114">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="507c6-114">Type: **uint32_t\***</span></span>

<span data-ttu-id="507c6-115">ID PCI del sottosistema hardware della scheda.</span><span class="sxs-lookup"><span data-stu-id="507c6-115">The PCI ID of the adapter's hardware subsystem.</span></span>

### <a name="revision"></a><span data-ttu-id="507c6-116">revision</span><span class="sxs-lookup"><span data-stu-id="507c6-116">revision</span></span>

<span data-ttu-id="507c6-117">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="507c6-117">Type: **uint32_t\***</span></span>

<span data-ttu-id="507c6-118">ID PCI del numero di revisione della scheda.</span><span class="sxs-lookup"><span data-stu-id="507c6-118">The PCI ID of the adapter's revision number.</span></span>

## <a name="see-also"></a><span data-ttu-id="507c6-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="507c6-119">See also</span></span>

<span data-ttu-id="507c6-120">Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="507c6-120">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>