---
description: Specifica se il codificatore esegue la telecine inversa.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Proprietà AVEncVideoInverseTelecineEnable (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124995"
---
# <a name="avencvideoinversetelecineenable-property"></a><span data-ttu-id="bcb12-103">Proprietà AVEncVideoInverseTelecineEnable</span><span class="sxs-lookup"><span data-stu-id="bcb12-103">AVEncVideoInverseTelecineEnable property</span></span>

<span data-ttu-id="bcb12-104">Specifica se il codificatore esegue la telecine inversa.</span><span class="sxs-lookup"><span data-stu-id="bcb12-104">Specifies whether the encoder performs inverse telecine.</span></span>

<span data-ttu-id="bcb12-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bcb12-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="bcb12-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bcb12-106">Data type</span></span>

<span data-ttu-id="bcb12-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="bcb12-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bcb12-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="bcb12-108">Property GUID</span></span>

<span data-ttu-id="bcb12-109">**Codecapis \_ AVEncVideoInverseTelecineEnable**</span><span class="sxs-lookup"><span data-stu-id="bcb12-109">**CODECAPI\_AVEncVideoInverseTelecineEnable**</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb12-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcb12-110">Remarks</span></span>

<span data-ttu-id="bcb12-111">Se il valore è **Variant \_ true**, il codificatore esegue la telecine inversa.</span><span class="sxs-lookup"><span data-stu-id="bcb12-111">If the value is **VARIANT\_TRUE**, the encoder performs inverse telecine.</span></span> <span data-ttu-id="bcb12-112">Se non è necessaria la telecine inversa, impostare questa proprietà su **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="bcb12-112">If inverse telecine is not required, set this property to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="bcb12-113">Per eseguire la telecine inversa all'esterno del codificatore, impostare questa proprietà su **Variant \_ false** e impostare la proprietà [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) su eAVEncVideoOutputScan \_ SameAsInput.</span><span class="sxs-lookup"><span data-stu-id="bcb12-113">To perform inverse telecine outside of the encoder, set this property to **VARIANT\_FALSE** and set the [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) property to eAVEncVideoOutputScan\_SameAsInput.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb12-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcb12-114">Requirements</span></span>



| <span data-ttu-id="bcb12-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb12-115">Requirement</span></span> | <span data-ttu-id="bcb12-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb12-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb12-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcb12-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb12-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="bcb12-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bcb12-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcb12-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb12-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bcb12-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bcb12-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcb12-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcb12-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcb12-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb12-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcb12-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb12-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="bcb12-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bcb12-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="bcb12-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




