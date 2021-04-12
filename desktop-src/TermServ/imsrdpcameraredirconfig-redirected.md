---
title: Proprietà reindirizzata IMsRdpCameraRedirConfig
description: Specifica se la fotocamera viene reindirizzata o meno.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà reindirizzata
- Servizi Desktop remoto proprietà reindirizzata, interfaccia IMsRdpCameraRedirConfig
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto, proprietà reindirizzata
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480556"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a><span data-ttu-id="cc1ed-106">Proprietà IMsRdpCameraRedirConfig:: Redirected</span><span class="sxs-lookup"><span data-stu-id="cc1ed-106">IMsRdpCameraRedirConfig::Redirected property</span></span>

<span data-ttu-id="cc1ed-107">Specifica se la fotocamera viene reindirizzata o meno.</span><span class="sxs-lookup"><span data-stu-id="cc1ed-107">Specifies whether or not the camera is redirected.</span></span>

<span data-ttu-id="cc1ed-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cc1ed-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc1ed-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc1ed-109">Syntax</span></span>

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a><span data-ttu-id="cc1ed-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cc1ed-110">Property value</span></span>

<span data-ttu-id="cc1ed-111">Valore che specifica se la fotocamera viene reindirizzata o meno.</span><span class="sxs-lookup"><span data-stu-id="cc1ed-111">A value that specifies whether or not the camera is redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc1ed-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc1ed-112">Requirements</span></span>

| <span data-ttu-id="cc1ed-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc1ed-113">Requirement</span></span> | <span data-ttu-id="cc1ed-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cc1ed-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="cc1ed-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc1ed-115">Minimum supported client</span></span>| <span data-ttu-id="cc1ed-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="cc1ed-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="cc1ed-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cc1ed-117">Type library</span></span>            | <span data-ttu-id="cc1ed-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="cc1ed-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="cc1ed-119">DLL</span><span class="sxs-lookup"><span data-stu-id="cc1ed-119">DLL</span></span>                  | <span data-ttu-id="cc1ed-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="cc1ed-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="cc1ed-121">IID</span><span class="sxs-lookup"><span data-stu-id="cc1ed-121">IID</span></span>                      | <span data-ttu-id="cc1ed-122">IID \_ IMsRdpCameraRedirConfig è definito come 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="cc1ed-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="cc1ed-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc1ed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc1ed-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="cc1ed-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>