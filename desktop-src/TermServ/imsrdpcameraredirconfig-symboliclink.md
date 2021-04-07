---
title: Proprietà SymbolicLink di IMsRdpCameraRedirConfig
description: Ottiene il collegamento simbolico dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SymbolicLink
- Servizi Desktop remoto proprietà SymbolicLink, interfaccia IMsRdpCameraRedirConfig
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto, proprietà SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "103875886"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a><span data-ttu-id="570d5-106">Proprietà IMsRdpCameraRedirConfig:: SymbolicLink</span><span class="sxs-lookup"><span data-stu-id="570d5-106">IMsRdpCameraRedirConfig::SymbolicLink property</span></span>

<span data-ttu-id="570d5-107">Ottiene il collegamento simbolico dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="570d5-107">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="570d5-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="570d5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="570d5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="570d5-109">Syntax</span></span>

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a><span data-ttu-id="570d5-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="570d5-110">Property value</span></span>

<span data-ttu-id="570d5-111">Collegamento simbolico dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="570d5-111">The symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="570d5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="570d5-112">Requirements</span></span>

| <span data-ttu-id="570d5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="570d5-113">Requirement</span></span> | <span data-ttu-id="570d5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="570d5-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="570d5-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="570d5-115">Minimum supported client</span></span>| <span data-ttu-id="570d5-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="570d5-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="570d5-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="570d5-117">Type library</span></span>            | <span data-ttu-id="570d5-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="570d5-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="570d5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="570d5-119">DLL</span></span>                  | <span data-ttu-id="570d5-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="570d5-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="570d5-121">IID</span><span class="sxs-lookup"><span data-stu-id="570d5-121">IID</span></span>                      | <span data-ttu-id="570d5-122">IID \_ IMsRdpCameraRedirConfig è definito come 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="570d5-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="570d5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="570d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="570d5-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="570d5-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>