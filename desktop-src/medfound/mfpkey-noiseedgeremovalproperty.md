---
description: Specifica se il codec deve tentare di rilevare i bordi del frame disturbati e di rimuoverli.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: Proprietà MFPKEY_NOISEEDGEREMOVAL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227002"
---
# <a name="mfpkey_noiseedgeremoval-property"></a><span data-ttu-id="b84b7-103">\_Proprietà NOISEEDGEREMOVAL di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="b84b7-103">MFPKEY\_NOISEEDGEREMOVAL Property</span></span>

<span data-ttu-id="b84b7-104">Specifica se il codec deve tentare di rilevare i bordi del frame disturbati e di rimuoverli.</span><span class="sxs-lookup"><span data-stu-id="b84b7-104">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b84b7-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b84b7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b84b7-106">g \_ wszWMVCNoiseEdgeRemoval</span><span class="sxs-lookup"><span data-stu-id="b84b7-106">g\_wszWMVCNoiseEdgeRemoval</span></span>

## <a name="data-type"></a><span data-ttu-id="b84b7-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b84b7-107">Data Type</span></span>

<span data-ttu-id="b84b7-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="b84b7-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="b84b7-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b84b7-109">Default Value</span></span>

<span data-ttu-id="b84b7-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="b84b7-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="b84b7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b84b7-111">Remarks</span></span>

<span data-ttu-id="b84b7-112">Il bordo di un frame fastidioso è in genere costituito dai dati VBI (Vertical Blanking Interval) di un frame della televisione broadcast.</span><span class="sxs-lookup"><span data-stu-id="b84b7-112">A noisy frame edge is usually the vertical blanking interval (VBI) data from a frame of broadcast television.</span></span> <span data-ttu-id="b84b7-113">Il VBI è costituito dalle prime 21 righe di analisi del fotogramma televisivo.</span><span class="sxs-lookup"><span data-stu-id="b84b7-113">The VBI is the first 21 scan lines of the television frame.</span></span> <span data-ttu-id="b84b7-114">Queste righe di analisi non contengono dati video, ovvero contengono dati sulla trasmissione.</span><span class="sxs-lookup"><span data-stu-id="b84b7-114">These scan lines do not contain video data—they contain data about the broadcast.</span></span> <span data-ttu-id="b84b7-115">Quando un segnale TV viene registrato da una scheda di acquisizione, il VBI viene in genere rimosso dal frame.</span><span class="sxs-lookup"><span data-stu-id="b84b7-115">When a television signal is recorded by a capture card, the VBI is usually removed from the frame.</span></span> <span data-ttu-id="b84b7-116">Il rilevamento e la correzione dei bordi rumorosi eseguiti dal codec possono correggere solo un bordo con tre o meno righe di disturbo.</span><span class="sxs-lookup"><span data-stu-id="b84b7-116">The noisy edge detection and correction performed by the codec can only correct an edge that has three or fewer lines of noise.</span></span> <span data-ttu-id="b84b7-117">Se il video acquisito contiene più di tre linee rumorose, si verifica un problema con l'hardware usato per acquisire il video.</span><span class="sxs-lookup"><span data-stu-id="b84b7-117">If captured video contains more than three noisy lines, there is a problem with the hardware used to capture the video.</span></span>

<span data-ttu-id="b84b7-118">Se il codec è impostato in modo da rimuovere i bordi rumorosi, le linee adiacenti al bordo rumoroso vengono duplicate per riempire il frame.</span><span class="sxs-lookup"><span data-stu-id="b84b7-118">If the codec is set to remove noisy edges, it duplicates lines adjacent to the noisy edge to fill in the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="b84b7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b84b7-119">Requirements</span></span>



| <span data-ttu-id="b84b7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b84b7-120">Requirement</span></span> | <span data-ttu-id="b84b7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b84b7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b84b7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b84b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b84b7-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b84b7-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b84b7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b84b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b84b7-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b84b7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b84b7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b84b7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b84b7-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b84b7-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b84b7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b84b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84b7-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b84b7-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




