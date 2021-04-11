---
title: Proprietà EncodeVideo di IMsRdpCameraRedirConfigCollection
description: Specifica se il flusso video è codificato con H. 264.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EncodeVideo
- Servizi Desktop remoto proprietà EncodeVideo, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà EncodeVideo
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6b2994f4db3de04f339bb242120b6c63cd2e0c7b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123288"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a><span data-ttu-id="1d585-106">Proprietà IMsRdpCameraRedirConfigCollection:: EncodeVideo</span><span class="sxs-lookup"><span data-stu-id="1d585-106">IMsRdpCameraRedirConfigCollection::EncodeVideo property</span></span>

<span data-ttu-id="1d585-107">Specifica se il flusso video è codificato con H. 264.</span><span class="sxs-lookup"><span data-stu-id="1d585-107">Specifies whether or not the video stream is H.264 encoded.</span></span>

<span data-ttu-id="1d585-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1d585-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d585-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d585-109">Syntax</span></span>

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a><span data-ttu-id="1d585-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1d585-110">Property value</span></span>

<span data-ttu-id="1d585-111">Valore che indica se il flusso video è con codifica H. 264.</span><span class="sxs-lookup"><span data-stu-id="1d585-111">A value that indicates whether or not the video stream is H.264 encoded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d585-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d585-112">Requirements</span></span>

| <span data-ttu-id="1d585-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d585-113">Requirement</span></span> | <span data-ttu-id="1d585-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1d585-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="1d585-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d585-115">Minimum supported client</span></span>| <span data-ttu-id="1d585-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="1d585-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="1d585-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1d585-117">Type library</span></span>            | <span data-ttu-id="1d585-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="1d585-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="1d585-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1d585-119">DLL</span></span>                  | <span data-ttu-id="1d585-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="1d585-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="1d585-121">IID</span><span class="sxs-lookup"><span data-stu-id="1d585-121">IID</span></span>                      | <span data-ttu-id="1d585-122">IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="1d585-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="1d585-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d585-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d585-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="1d585-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>