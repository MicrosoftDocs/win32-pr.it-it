---
description: Abilita o Disabilita l'uguaglianza di sonorità in un decoder audio o in un processore di segnali digitali (DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: Proprietà AVDSPLoudnessEqualization (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965821"
---
# <a name="avdsploudnessequalization-property"></a><span data-ttu-id="832f4-103">Proprietà AVDSPLoudnessEqualization</span><span class="sxs-lookup"><span data-stu-id="832f4-103">AVDSPLoudnessEqualization property</span></span>

<span data-ttu-id="832f4-104">Abilita o Disabilita l'uguaglianza di sonorità in un decoder audio o in un processore di segnali digitali (DSP).</span><span class="sxs-lookup"><span data-stu-id="832f4-104">Enables or disables loudness equalization in an audio decoder or digital signal processor (DSP).</span></span>

<span data-ttu-id="832f4-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="832f4-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="832f4-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="832f4-106">Data type</span></span>

<span data-ttu-id="832f4-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="832f4-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="832f4-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="832f4-108">Property GUID</span></span>

<span data-ttu-id="832f4-109">**Codecapis \_ AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="832f4-109">**CODECAPI\_AVDSPLoudnessEqualization**</span></span>

## <a name="property-value"></a><span data-ttu-id="832f4-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="832f4-110">Property value</span></span>

<span data-ttu-id="832f4-111">Il valore di questa proprietà è un membro dell'enumerazione [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) .</span><span class="sxs-lookup"><span data-stu-id="832f4-111">The value of this property is a member of the [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="832f4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="832f4-112">Remarks</span></span>

<span data-ttu-id="832f4-113">L'uguaglianza di sonorità è un processo DSP che mantiene un livello di volume coerente quando viene modificato il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="832f4-113">Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="832f4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="832f4-114">Requirements</span></span>



| <span data-ttu-id="832f4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="832f4-115">Requirement</span></span> | <span data-ttu-id="832f4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="832f4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="832f4-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="832f4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="832f4-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="832f4-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="832f4-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="832f4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="832f4-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="832f4-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="832f4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="832f4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="832f4-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="832f4-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="832f4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="832f4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="832f4-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="832f4-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="832f4-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="832f4-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




