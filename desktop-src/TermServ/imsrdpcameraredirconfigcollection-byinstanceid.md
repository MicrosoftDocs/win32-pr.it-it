---
title: Proprietà ByInstanceId di IMsRdpCameraRedirConfigCollection
description: Restituisce un oggetto IMsRdpCameraRedirConfig dalla raccolta che corrisponde all'ID istanza specificato.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ByInstanceId
- Servizi Desktop remoto proprietà ByInstanceId, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà ByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480525"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a><span data-ttu-id="69193-106">Proprietà IMsRdpCameraRedirConfigCollection:: ByInstanceId</span><span class="sxs-lookup"><span data-stu-id="69193-106">IMsRdpCameraRedirConfigCollection::ByInstanceId property</span></span>

<span data-ttu-id="69193-107">Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde all'ID istanza specificato.</span><span class="sxs-lookup"><span data-stu-id="69193-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>

<span data-ttu-id="69193-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="69193-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="69193-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69193-109">Syntax</span></span>

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="69193-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="69193-110">Property value</span></span>

<span data-ttu-id="69193-111">Oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) che corrisponde all'ID istanza specificato.</span><span class="sxs-lookup"><span data-stu-id="69193-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified instance ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="69193-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69193-112">Requirements</span></span>

| <span data-ttu-id="69193-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="69193-113">Requirement</span></span> | <span data-ttu-id="69193-114">Valore</span><span class="sxs-lookup"><span data-stu-id="69193-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="69193-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69193-115">Minimum supported client</span></span>| <span data-ttu-id="69193-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="69193-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="69193-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="69193-117">Type library</span></span>            | <span data-ttu-id="69193-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="69193-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="69193-119">DLL</span><span class="sxs-lookup"><span data-stu-id="69193-119">DLL</span></span>                  | <span data-ttu-id="69193-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="69193-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="69193-121">IID</span><span class="sxs-lookup"><span data-stu-id="69193-121">IID</span></span>                      | <span data-ttu-id="69193-122">IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="69193-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="69193-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69193-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69193-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="69193-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>