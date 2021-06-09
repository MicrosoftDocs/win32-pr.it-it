---
description: Abilita la modalità a bassa latenza in un codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826905"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="0c756-103">CODECAPI \_ AVLowLatencyMode - proprietà</span><span class="sxs-lookup"><span data-stu-id="0c756-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="0c756-104">Abilita la modalità a bassa latenza in un codec.</span><span class="sxs-lookup"><span data-stu-id="0c756-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c756-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0c756-105">Data type</span></span>

<span data-ttu-id="0c756-106">**ULONG** (**VT \_ BOOL**)</span><span class="sxs-lookup"><span data-stu-id="0c756-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0c756-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="0c756-107">Property GUID</span></span>

<span data-ttu-id="0c756-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="0c756-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="0c756-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0c756-109">Property value</span></span>

<span data-ttu-id="0c756-110">Se il valore è diverso da zero, viene abilitata la modalità a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="0c756-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="0c756-111">Se il valore è zero, la modalità a bassa latenza è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="0c756-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c756-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c756-112">Remarks</span></span>

<span data-ttu-id="0c756-113">Questa proprietà si applica sia ai codificatori che ai decodificatori.</span><span class="sxs-lookup"><span data-stu-id="0c756-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="0c756-114">La modalità a bassa latenza è utile per le comunicazioni in tempo reale o l'acquisizione in tempo reale, quando la latenza deve essere ridotta al minimo.</span><span class="sxs-lookup"><span data-stu-id="0c756-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="0c756-115">Tuttavia, la modalità a bassa latenza potrebbe anche ridurre la qualità di decodifica o codifica.</span><span class="sxs-lookup"><span data-stu-id="0c756-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="0c756-116">Il codificatore non dovrebbe aggiungere alcun ritardo del campione a causa del riordinamento dei fotogrammi nel processo di codifica e un campione di input genererà un campione di output.</span><span class="sxs-lookup"><span data-stu-id="0c756-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="0c756-117">Le sezioni/fotogrammi B possono essere presenti purché non introduca alcun ordinamento dei fotogrammi nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="0c756-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

> [!WARNING] 
> <span data-ttu-id="0c756-118">Nell'implementazione corrente il Media Foundation decodificatore H.264 usa il **tipo VT_UI4** per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c756-118">In the current implementation, the Media Foundation H.264 decoder uses the type **VT_UI4** for this property.</span></span> <span data-ttu-id="0c756-119">Tutte le altre implementazioni, incluso il codificatore H.264, usano il **tipo VT_BOOL**.</span><span class="sxs-lookup"><span data-stu-id="0c756-119">All other implementations, including the H.264 encoder, use the type **VT_BOOL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c756-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c756-120">Requirements</span></span>



| <span data-ttu-id="0c756-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c756-121">Requirement</span></span> | <span data-ttu-id="0c756-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0c756-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c756-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c756-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0c756-124">Windows 8 app \[ desktop \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0c756-124">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="0c756-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c756-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0c756-126">App desktop di Windows Server 2012 \[ \| per app UWP\]</span><span class="sxs-lookup"><span data-stu-id="0c756-126">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0c756-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c756-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c756-128"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="0c756-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c756-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c756-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c756-130">Media Foundation proprietà</span><span class="sxs-lookup"><span data-stu-id="0c756-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0c756-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0c756-131">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

