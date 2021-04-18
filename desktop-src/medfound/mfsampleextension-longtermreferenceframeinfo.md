---
description: Specifica le informazioni del frame di riferimento a lungo termine (LTR) e viene restituito nell'esempio di output.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: Attributo MFSampleExtension_LongTermReferenceFrameInfo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320813"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a><span data-ttu-id="fc5a6-103">\_Attributo LongTermReferenceFrameInfo di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="fc5a6-103">MFSampleExtension\_LongTermReferenceFrameInfo attribute</span></span>

<span data-ttu-id="fc5a6-104">Specifica le informazioni del frame di riferimento a lungo termine (LTR) e viene restituito nell'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="fc5a6-104">Specifies Long Term Reference (LTR) frame info and is returned on the output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="fc5a6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fc5a6-105">Data type</span></span>

<span data-ttu-id="fc5a6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fc5a6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fc5a6-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc5a6-107">Remarks</span></span>

<span data-ttu-id="fc5a6-108">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="fc5a6-108">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="fc5a6-109">I codificatori devono restituire questo attributo nell'esempio di output quando l'applicazione controlla i frame LTR, che è specificato da [codecapi \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="fc5a6-109">Encoders shall return this attribute on the output sample when the application controls LTR frames, which is specified by [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

<span data-ttu-id="fc5a6-110">MFSampleExtension \_ LongTermReferenceFrameInfo restituisce fino a due campi.</span><span class="sxs-lookup"><span data-stu-id="fc5a6-110">MFSampleExtension\_LongTermReferenceFrameInfo returns up to two fields.</span></span>

<span data-ttu-id="fc5a6-111">Il primo campo, BITS \[ 0.. 15 \] , è *LongTermFrameIdx* associato al frame di output se è contrassegnato come frame ltr.</span><span class="sxs-lookup"><span data-stu-id="fc5a6-111">The first field, bits\[0..15\], is *LongTermFrameIdx* associated with the output frame if it is marked as a LTR frame.</span></span> <span data-ttu-id="fc5a6-112">Il primo valore è 0xFFFF, se questo frame di output è un frame di riferimento a breve termine o un frame non di riferimento.</span><span class="sxs-lookup"><span data-stu-id="fc5a6-112">The first value is 0xffff, if this output frame is a short term reference frame or a non-reference frame.</span></span>

<span data-ttu-id="fc5a6-113">Il secondo campo, BITS \[ 16.31 \] , è una bitmap costituita da *MaxNumLTRFrames* molti bit che indicano i frame LTR usati per codificare questo frame di output, a partire dal bit 16.</span><span class="sxs-lookup"><span data-stu-id="fc5a6-113">The second field, bits\[16..31\], is a bitmap consisting of *MaxNumLTRFrames* many bits that indicate which LTR frame(s) were used for encoding this output frame, starting from bit 16.</span></span> <span data-ttu-id="fc5a6-114">Il resto dei bit deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="fc5a6-114">The rest of bits shall be set to 0.</span></span> <span data-ttu-id="fc5a6-115">Il secondo valore è 0 se il frame di output non è codificato con frame LTR.</span><span class="sxs-lookup"><span data-stu-id="fc5a6-115">The second value is 0 if this output frame is not encoded using any LTR frames.</span></span> <span data-ttu-id="fc5a6-116">*MaxNumLTRFrames* è il numero massimo di fotogrammi LTR impostati tramite [codecapis \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="fc5a6-116">*MaxNumLTRFrames* is the maximum number of LTR frames set through [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5a6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc5a6-117">Requirements</span></span>



| <span data-ttu-id="fc5a6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc5a6-118">Requirement</span></span> | <span data-ttu-id="fc5a6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fc5a6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5a6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc5a6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fc5a6-121">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fc5a6-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="fc5a6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc5a6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fc5a6-123">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fc5a6-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fc5a6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc5a6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc5a6-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc5a6-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc5a6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc5a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5a6-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fc5a6-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




