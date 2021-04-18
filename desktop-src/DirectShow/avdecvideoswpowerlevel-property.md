---
description: Specifica il livello di risparmio energia di un decodificatore video.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Proprietà AVDecVideoSWPowerLevel (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304167"
---
# <a name="avdecvideoswpowerlevel-property"></a><span data-ttu-id="d9031-103">Proprietà AVDecVideoSWPowerLevel</span><span class="sxs-lookup"><span data-stu-id="d9031-103">AVDecVideoSWPowerLevel property</span></span>

<span data-ttu-id="d9031-104">Specifica il livello di risparmio energia di un decodificatore video.</span><span class="sxs-lookup"><span data-stu-id="d9031-104">Specifies the power-saving level of a video decoder.</span></span>

<span data-ttu-id="d9031-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d9031-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9031-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d9031-106">Data type</span></span>

<span data-ttu-id="d9031-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d9031-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d9031-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="d9031-108">Property GUID</span></span>

<span data-ttu-id="d9031-109">**Codecapis \_ AVDecVideoSWPowerLevel**</span><span class="sxs-lookup"><span data-stu-id="d9031-109">**CODECAPI\_AVDecVideoSWPowerLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="d9031-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d9031-110">Property value</span></span>

<span data-ttu-id="d9031-111">L'intervallo dei valori possibili è \[ 0.. 100 \] , inclusivo, con il significato seguente.</span><span class="sxs-lookup"><span data-stu-id="d9031-111">The range of possible values is \[0..100\], inclusive, with the following meaning.</span></span>



| <span data-ttu-id="d9031-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d9031-112">Value</span></span> | <span data-ttu-id="d9031-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9031-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="d9031-114">0</span><span class="sxs-lookup"><span data-stu-id="d9031-114">0</span></span>     | <span data-ttu-id="d9031-115">Ottimizza per la durata della batteria.</span><span class="sxs-lookup"><span data-stu-id="d9031-115">Optimize for battery life.</span></span>  |
| <span data-ttu-id="d9031-116">100</span><span class="sxs-lookup"><span data-stu-id="d9031-116">100</span></span>   | <span data-ttu-id="d9031-117">Ottimizza per la qualità del video.</span><span class="sxs-lookup"><span data-stu-id="d9031-117">Optimize for video quality.</span></span> |



 

<span data-ttu-id="d9031-118">L'enumerazione [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) definisce alcune costanti specifiche all'interno di questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="d9031-118">The [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) enumeration defines some specific constants within this range.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9031-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9031-119">Remarks</span></span>

<span data-ttu-id="d9031-120">È possibile impostare questa proprietà durante la riproduzione per modificare il livello di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="d9031-120">You can set this property during playback to change the pwoer-saving level.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9031-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9031-121">Requirements</span></span>



| <span data-ttu-id="d9031-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9031-122">Requirement</span></span> | <span data-ttu-id="d9031-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d9031-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9031-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9031-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d9031-125">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="d9031-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d9031-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9031-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d9031-127">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d9031-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d9031-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9031-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9031-129"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9031-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9031-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9031-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9031-131">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="d9031-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d9031-132">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d9031-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




