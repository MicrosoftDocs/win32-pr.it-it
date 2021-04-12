---
title: Proprietà DeviceExists di IMsRdpCameraRedirConfig
description: Specifica se il dispositivo della fotocamera è attualmente esistente (ovvero la fotocamera è connessa).
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DeviceExists
- Servizi Desktop remoto proprietà DeviceExists, interfaccia IMsRdpCameraRedirConfig
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto, proprietà DeviceExists
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480564"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a><span data-ttu-id="2979a-106">IMsRdpCameraRedirConfig::D Proprietà eviceExists</span><span class="sxs-lookup"><span data-stu-id="2979a-106">IMsRdpCameraRedirConfig::DeviceExists property</span></span>

<span data-ttu-id="2979a-107">Specifica se il dispositivo della fotocamera è attualmente esistente (ovvero la fotocamera è connessa).</span><span class="sxs-lookup"><span data-stu-id="2979a-107">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>

<span data-ttu-id="2979a-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2979a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2979a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2979a-109">Syntax</span></span>

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a><span data-ttu-id="2979a-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2979a-110">Property value</span></span>

<span data-ttu-id="2979a-111">Valore che indica se il dispositivo della fotocamera è attualmente esistente (ovvero la fotocamera è connessa).</span><span class="sxs-lookup"><span data-stu-id="2979a-111">A value that indicates whether or not the camera device currently exists (that is, the camera is connected).</span></span>

## <a name="requirements"></a><span data-ttu-id="2979a-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2979a-112">Requirements</span></span>

| <span data-ttu-id="2979a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2979a-113">Requirement</span></span> | <span data-ttu-id="2979a-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2979a-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="2979a-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2979a-115">Minimum supported client</span></span>| <span data-ttu-id="2979a-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="2979a-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="2979a-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2979a-117">Type library</span></span>            | <span data-ttu-id="2979a-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="2979a-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="2979a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="2979a-119">DLL</span></span>                  | <span data-ttu-id="2979a-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="2979a-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="2979a-121">IID</span><span class="sxs-lookup"><span data-stu-id="2979a-121">IID</span></span>                      | <span data-ttu-id="2979a-122">IID \_ IMsRdpCameraRedirConfig è definito come 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="2979a-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="2979a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2979a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2979a-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="2979a-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>