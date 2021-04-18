---
description: Specifica il numero di fotogrammi dopo il frame corrente che il codec valuterà prima di codificare il frame corrente.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: Proprietà MFPKEY_LOOKAHEAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310627"
---
# <a name="mfpkey_lookahead-property"></a><span data-ttu-id="7f2e5-103">\_Proprietà lookahead di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="7f2e5-103">MFPKEY\_LOOKAHEAD Property</span></span>

<span data-ttu-id="7f2e5-104">Specifica il numero di fotogrammi dopo il frame corrente che il codec valuterà prima di codificare il frame corrente.</span><span class="sxs-lookup"><span data-stu-id="7f2e5-104">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7f2e5-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7f2e5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7f2e5-106">g \_ wszWMVCLookAhead</span><span class="sxs-lookup"><span data-stu-id="7f2e5-106">g\_wszWMVCLookAhead</span></span>

## <a name="data-type"></a><span data-ttu-id="7f2e5-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7f2e5-107">Data Type</span></span>

<span data-ttu-id="7f2e5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7f2e5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="7f2e5-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="7f2e5-109">Default Value</span></span>

<span data-ttu-id="7f2e5-110">0</span><span class="sxs-lookup"><span data-stu-id="7f2e5-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2e5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f2e5-111">Remarks</span></span>

<span data-ttu-id="7f2e5-112">Quando il codec USA lookahead, può codificare il video in modo più efficiente.</span><span class="sxs-lookup"><span data-stu-id="7f2e5-112">When the codec uses lookahead, it can encode the video more efficiently.</span></span>

<span data-ttu-id="7f2e5-113">L'oggetto writer di Windows Media Format SDK prevede che il codec Codifichi immediatamente ogni campione.</span><span class="sxs-lookup"><span data-stu-id="7f2e5-113">The writer object of the Windows Media Format SDK expects the codec to encode each sample immediately.</span></span> <span data-ttu-id="7f2e5-114">Di conseguenza, questa funzionalità non funziona correttamente nel software che utilizza l'oggetto writer (incluso Windows Media Encoder e Windows Media Player).</span><span class="sxs-lookup"><span data-stu-id="7f2e5-114">As a result, this feature does not work properly in software that uses the writer object (including Windows Media Encoder and Windows Media Player).</span></span> <span data-ttu-id="7f2e5-115">Tutte le estensioni di unità dati associate ai frame video verranno collegate al frame di output errato.</span><span class="sxs-lookup"><span data-stu-id="7f2e5-115">Any data unit extensions associated with video frames will be attached to the wrong output frame.</span></span> <span data-ttu-id="7f2e5-116">Il numero di frame in base ai quali le estensioni dell'unità dati vengono posizionate in modo non corrispondente è uguale al numero di frame di lookahead utilizzati.</span><span class="sxs-lookup"><span data-stu-id="7f2e5-116">The number of frames by which the data unit extensions are misplaced is equal to the number of frames of lookahead that are used.</span></span>

<span data-ttu-id="7f2e5-117">I valori lookahead validi sono compresi tra 0 e 16 frame.</span><span class="sxs-lookup"><span data-stu-id="7f2e5-117">Valid lookahead values range from 0 to 16 frames.</span></span> <span data-ttu-id="7f2e5-118">Il valore consigliato è 16.</span><span class="sxs-lookup"><span data-stu-id="7f2e5-118">The recommended value is 16.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2e5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f2e5-119">Requirements</span></span>



| <span data-ttu-id="7f2e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f2e5-120">Requirement</span></span> | <span data-ttu-id="7f2e5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7f2e5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2e5-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f2e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7f2e5-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f2e5-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7f2e5-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f2e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7f2e5-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f2e5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f2e5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f2e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f2e5-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f2e5-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f2e5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f2e5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2e5-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f2e5-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




