---
title: Proprietà BySymbolicLink di IMsRdpCameraRedirConfigCollection
description: Restituisce un oggetto IMsRdpCameraRedirConfig dalla raccolta che corrisponde al collegamento simbolico specificato dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BySymbolicLink
- Servizi Desktop remoto proprietà BySymbolicLink, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà BySymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303650"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a><span data-ttu-id="aca18-106">IMsRdpCameraRedirConfigCollection::. Proprietà BySymbolicLink</span><span class="sxs-lookup"><span data-stu-id="aca18-106">IMsRdpCameraRedirConfigCollection::.BySymbolicLink property</span></span>

<span data-ttu-id="aca18-107">Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde al collegamento simbolico specificato dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="aca18-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="aca18-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="aca18-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca18-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aca18-109">Syntax</span></span>

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="aca18-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aca18-110">Property value</span></span>

<span data-ttu-id="aca18-111">Oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) che corrisponde al collegamento simbolico specificato.</span><span class="sxs-lookup"><span data-stu-id="aca18-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified symbolic link.</span></span>

## <a name="requirements"></a><span data-ttu-id="aca18-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aca18-112">Requirements</span></span>

| <span data-ttu-id="aca18-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aca18-113">Requirement</span></span> | <span data-ttu-id="aca18-114">Valore</span><span class="sxs-lookup"><span data-stu-id="aca18-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="aca18-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aca18-115">Minimum supported client</span></span>| <span data-ttu-id="aca18-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="aca18-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="aca18-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="aca18-117">Type library</span></span>            | <span data-ttu-id="aca18-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="aca18-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="aca18-119">DLL</span><span class="sxs-lookup"><span data-stu-id="aca18-119">DLL</span></span>                  | <span data-ttu-id="aca18-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="aca18-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="aca18-121">IID</span><span class="sxs-lookup"><span data-stu-id="aca18-121">IID</span></span>                      | <span data-ttu-id="aca18-122">IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="aca18-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="aca18-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aca18-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca18-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="aca18-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>