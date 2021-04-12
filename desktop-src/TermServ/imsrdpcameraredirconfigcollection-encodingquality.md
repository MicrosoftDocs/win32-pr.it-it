---
title: Proprietà EncodingQuality di IMsRdpCameraRedirConfigCollection
description: Specifica la qualità della codifica (velocità in bit).
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EncodingQuality
- Servizi Desktop remoto proprietà EncodingQuality, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà EncodingQuality
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480540"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a><span data-ttu-id="60694-106">Proprietà IMsRdpCameraRedirConfigCollection:: EncodingQuality</span><span class="sxs-lookup"><span data-stu-id="60694-106">IMsRdpCameraRedirConfigCollection::EncodingQuality property</span></span>

<span data-ttu-id="60694-107">Specifica la qualità della codifica (velocità in bit).</span><span class="sxs-lookup"><span data-stu-id="60694-107">Specifies the encoding quality (bit rate).</span></span>

<span data-ttu-id="60694-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="60694-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="60694-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60694-109">Syntax</span></span>

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a><span data-ttu-id="60694-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="60694-110">Property value</span></span>

<span data-ttu-id="60694-111">Uno dei seguenti valori di enumerazione **CameraRedirEncodingQuality** che specifica la qualità della codifica (velocità in bit).</span><span class="sxs-lookup"><span data-stu-id="60694-111">One of the following **CameraRedirEncodingQuality** enum values that specifies the encoding quality (bit rate).</span></span>

| <span data-ttu-id="60694-112">Nome del membro enum</span><span class="sxs-lookup"><span data-stu-id="60694-112">Enum member name</span></span> | <span data-ttu-id="60694-113">Valore</span><span class="sxs-lookup"><span data-stu-id="60694-113">Value</span></span> |
|-----------------|--------|
| <span data-ttu-id="60694-114">encodingQualityLow</span><span class="sxs-lookup"><span data-stu-id="60694-114">encodingQualityLow</span></span> | <span data-ttu-id="60694-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="60694-115">0x0000</span></span> |
| <span data-ttu-id="60694-116">encodingQualityMedium</span><span class="sxs-lookup"><span data-stu-id="60694-116">encodingQualityMedium</span></span> | <span data-ttu-id="60694-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="60694-117">0x0001</span></span> |
| <span data-ttu-id="60694-118">encodingQualityHigh</span><span class="sxs-lookup"><span data-stu-id="60694-118">encodingQualityHigh</span></span> | <span data-ttu-id="60694-119">0x0002</span><span class="sxs-lookup"><span data-stu-id="60694-119">0x0002</span></span> |

## <a name="requirements"></a><span data-ttu-id="60694-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60694-120">Requirements</span></span>

| <span data-ttu-id="60694-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="60694-121">Requirement</span></span> | <span data-ttu-id="60694-122">Valore</span><span class="sxs-lookup"><span data-stu-id="60694-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="60694-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60694-123">Minimum supported client</span></span>| <span data-ttu-id="60694-124">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="60694-124">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="60694-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="60694-125">Type library</span></span>            | <span data-ttu-id="60694-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="60694-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="60694-127">DLL</span><span class="sxs-lookup"><span data-stu-id="60694-127">DLL</span></span>                  | <span data-ttu-id="60694-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="60694-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="60694-129">IID</span><span class="sxs-lookup"><span data-stu-id="60694-129">IID</span></span>                      | <span data-ttu-id="60694-130">IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="60694-130">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="60694-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60694-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60694-132">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="60694-132">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>