---
title: Proprietà ByIndex di IMsRdpCameraRedirConfigCollection
description: Restituisce un oggetto IMsRdpCameraRedirConfig in base al relativo indice nella raccolta.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ByIndex
- Servizi Desktop remoto proprietà ByIndex, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà ByIndex
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303646"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a><span data-ttu-id="80bf5-106">Proprietà IMsRdpCameraRedirConfigCollection:: ByIndex</span><span class="sxs-lookup"><span data-stu-id="80bf5-106">IMsRdpCameraRedirConfigCollection::ByIndex property</span></span>

<span data-ttu-id="80bf5-107">Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) in base al relativo indice nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="80bf5-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>

<span data-ttu-id="80bf5-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="80bf5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80bf5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80bf5-109">Syntax</span></span>

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="80bf5-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="80bf5-110">Property value</span></span>

<span data-ttu-id="80bf5-111">Oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="80bf5-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified index.</span></span>

## <a name="requirements"></a><span data-ttu-id="80bf5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80bf5-112">Requirements</span></span>

| <span data-ttu-id="80bf5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="80bf5-113">Requirement</span></span> | <span data-ttu-id="80bf5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="80bf5-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="80bf5-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80bf5-115">Minimum supported client</span></span>| <span data-ttu-id="80bf5-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="80bf5-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="80bf5-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="80bf5-117">Type library</span></span>            | <span data-ttu-id="80bf5-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="80bf5-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="80bf5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="80bf5-119">DLL</span></span>                  | <span data-ttu-id="80bf5-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="80bf5-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="80bf5-121">IID</span><span class="sxs-lookup"><span data-stu-id="80bf5-121">IID</span></span>                      | <span data-ttu-id="80bf5-122">IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="80bf5-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="80bf5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80bf5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80bf5-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="80bf5-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>