---
title: Proprietà ParentInstanceId di IMsRdpCameraRedirConfig
description: Ottiene l'ID dell'istanza del dispositivo padre della fotocamera.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ParentInstanceId
- Servizi Desktop remoto proprietà ParentInstanceId, interfaccia IMsRdpCameraRedirConfig
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto, proprietà ParentInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303654"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a><span data-ttu-id="fc662-106">IMsRdpCameraRedirConfig::P proprietà arentInstanceId</span><span class="sxs-lookup"><span data-stu-id="fc662-106">IMsRdpCameraRedirConfig::ParentInstanceId property</span></span>

<span data-ttu-id="fc662-107">Ottiene l'ID dell'istanza del dispositivo padre della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="fc662-107">Gets the parent device instance ID of the camera.</span></span>

<span data-ttu-id="fc662-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fc662-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc662-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc662-109">Syntax</span></span>

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a><span data-ttu-id="fc662-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fc662-110">Property value</span></span>

<span data-ttu-id="fc662-111">ID dell'istanza del dispositivo padre della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="fc662-111">The parent device instance ID of the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc662-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc662-112">Requirements</span></span>

| <span data-ttu-id="fc662-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc662-113">Requirement</span></span> | <span data-ttu-id="fc662-114">Valore</span><span class="sxs-lookup"><span data-stu-id="fc662-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="fc662-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc662-115">Minimum supported client</span></span>| <span data-ttu-id="fc662-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="fc662-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="fc662-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fc662-117">Type library</span></span>            | <span data-ttu-id="fc662-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fc662-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="fc662-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fc662-119">DLL</span></span>                  | <span data-ttu-id="fc662-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fc662-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="fc662-121">IID</span><span class="sxs-lookup"><span data-stu-id="fc662-121">IID</span></span>                      | <span data-ttu-id="fc662-122">IID \_ IMsRdpCameraRedirConfig è definito come 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="fc662-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="fc662-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc662-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc662-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="fc662-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>