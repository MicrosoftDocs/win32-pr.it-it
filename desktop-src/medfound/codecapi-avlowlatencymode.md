---
description: Abilita la modalità a bassa latenza in un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Proprietà CODECAPI_AVLowLatencyMode (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305481"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="bc0f3-103">Proprietà AVLowLatencyMode di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="bc0f3-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="bc0f3-104">Abilita la modalità a bassa latenza in un codec.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="bc0f3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bc0f3-105">Data type</span></span>

<span data-ttu-id="bc0f3-106">**ULONG** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="bc0f3-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bc0f3-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="bc0f3-107">Property GUID</span></span>

<span data-ttu-id="bc0f3-108">**Codecapis \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="bc0f3-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="bc0f3-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bc0f3-109">Property value</span></span>

<span data-ttu-id="bc0f3-110">Se il valore è diverso da zero, è abilitata la modalità a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="bc0f3-111">Se il valore è zero, la modalità a bassa latenza è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc0f3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc0f3-112">Remarks</span></span>

<span data-ttu-id="bc0f3-113">Questa proprietà si applica a codificatori e decodificatori.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="bc0f3-114">La modalità a bassa latenza è utile per le comunicazioni in tempo reale o Live Capture, quando la latenza deve essere ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="bc0f3-115">Tuttavia, la modalità a bassa latenza può ridurre anche la decodifica o la qualità della codifica.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="bc0f3-116">Si prevede che il codificatore non aggiunga alcun ritardo di esempio a causa del riordino dei frame nel processo di codifica e un esempio di input produrrà un esempio di output.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="bc0f3-117">Le sezioni e i frame B possono essere presenti a condizione che non introducano un nuovo ordinamento del frame nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="bc0f3-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0f3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc0f3-118">Requirements</span></span>



| <span data-ttu-id="bc0f3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc0f3-119">Requirement</span></span> | <span data-ttu-id="bc0f3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bc0f3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0f3-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc0f3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bc0f3-122">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bc0f3-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="bc0f3-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc0f3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bc0f3-124">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="bc0f3-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bc0f3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc0f3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc0f3-126"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc0f3-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc0f3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc0f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0f3-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bc0f3-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bc0f3-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="bc0f3-129">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

