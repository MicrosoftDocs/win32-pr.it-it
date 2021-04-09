---
description: Abilita o Disabilita la modalità di generazione di anteprime in un decodificatore video.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Proprietà AVDecVideoThumbnailGenerationMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965825"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a><span data-ttu-id="1f698-103">Proprietà AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="1f698-103">AVDecVideoThumbnailGenerationMode property</span></span>

<span data-ttu-id="1f698-104">Abilita o Disabilita la modalità di generazione di anteprime in un decodificatore video.</span><span class="sxs-lookup"><span data-stu-id="1f698-104">Enables or disables thumbnail generation mode in a video decoder.</span></span>

<span data-ttu-id="1f698-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1f698-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="1f698-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1f698-106">Data type</span></span>

<span data-ttu-id="1f698-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="1f698-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1f698-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="1f698-108">Property GUID</span></span>

<span data-ttu-id="1f698-109">**Codecapis \_ AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="1f698-109">**CODECAPI\_AVDecVideoThumbnailGenerationMode**</span></span>

## <a name="remarks"></a><span data-ttu-id="1f698-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f698-110">Remarks</span></span>

<span data-ttu-id="1f698-111">Se il valore è **Variant \_ true**, il decodificatore usa un'impostazione ottimizzata per generare rapidamente immagini di anteprima.</span><span class="sxs-lookup"><span data-stu-id="1f698-111">If the value is **VARIANT\_TRUE**, the decoder uses a setting that is optimized to generate thumbnail images quickly.</span></span> <span data-ttu-id="1f698-112">(Ad esempio, potrebbe ignorare i frame B o P). In caso contrario, se il valore è **Variant \_ false**, il decodificatore utilizza le impostazioni di decodifica normali.</span><span class="sxs-lookup"><span data-stu-id="1f698-112">(For example, it might skip B or P frames.) Otherwise, if the value is **VARIANT\_FALSE**, the decoder uses its normal decoding settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f698-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f698-113">Requirements</span></span>



| <span data-ttu-id="1f698-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f698-114">Requirement</span></span> | <span data-ttu-id="1f698-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1f698-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f698-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f698-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1f698-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="1f698-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1f698-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f698-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1f698-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1f698-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1f698-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f698-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f698-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f698-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f698-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f698-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f698-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="1f698-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="1f698-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="1f698-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




