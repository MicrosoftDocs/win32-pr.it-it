---
description: Specifica il formato di input corrente per il decodificatore.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Proprietà AVDecCommonInputFormat (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482284"
---
# <a name="avdeccommoninputformat-property"></a><span data-ttu-id="c07f7-103">Proprietà AVDecCommonInputFormat</span><span class="sxs-lookup"><span data-stu-id="c07f7-103">AVDecCommonInputFormat property</span></span>

<span data-ttu-id="c07f7-104">Specifica il formato di input corrente per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="c07f7-104">Specifies the current input format for the decoder.</span></span>

<span data-ttu-id="c07f7-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c07f7-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="c07f7-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c07f7-106">Data type</span></span>

<span data-ttu-id="c07f7-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="c07f7-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c07f7-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="c07f7-108">Property GUID</span></span>

<span data-ttu-id="c07f7-109">**Codecapis \_ AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="c07f7-109">**CODECAPI\_AVDecCommonInputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="c07f7-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c07f7-110">Property value</span></span>

<span data-ttu-id="c07f7-111">Il valore di questa proprietà è un **BSTR** che contiene la rappresentazione di stringa di un GUID.</span><span class="sxs-lookup"><span data-stu-id="c07f7-111">The value of this property is a **BSTR** that contains the string representation of a GUID.</span></span> <span data-ttu-id="c07f7-112">Sono definiti i seguenti GUID.</span><span class="sxs-lookup"><span data-stu-id="c07f7-112">The following GUIDs are defined.</span></span>



| <span data-ttu-id="c07f7-113">**GUID**</span><span class="sxs-lookup"><span data-stu-id="c07f7-113">**GUID**</span></span>                                            | <span data-ttu-id="c07f7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c07f7-114">Description</span></span>                                    |
|-----------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="c07f7-115">**\_GUID AVDecAudioInputAAC di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-115">**CODECAPI\_GUID\_AVDecAudioInputAAC**</span></span>              | <span data-ttu-id="c07f7-116">Codifica audio avanzata (AAC)</span><span class="sxs-lookup"><span data-stu-id="c07f7-116">Advanced Audio Coding (AAC)</span></span>                    |
| <span data-ttu-id="c07f7-117">**\_GUID AVDecAudioInputDolbyDigitalPlus di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-117">**CODECAPI\_GUID\_AVDecAudioInputDolbyDigitalPlus**</span></span> | <span data-ttu-id="c07f7-118">Audio Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="c07f7-118">Dolby Digital Plus audio</span></span>                       |
| <span data-ttu-id="c07f7-119">**\_GUID AVDecAudioInputDolby di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-119">**CODECAPI\_GUID\_AVDecAudioInputDolby**</span></span>            | <span data-ttu-id="c07f7-120">Audio Dolby</span><span class="sxs-lookup"><span data-stu-id="c07f7-120">Dolby audio</span></span>                                    |
| <span data-ttu-id="c07f7-121">**\_GUID AVDecAudioInputDTS di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-121">**CODECAPI\_GUID\_AVDecAudioInputDTS**</span></span>              | <span data-ttu-id="c07f7-122">Audio DTS</span><span class="sxs-lookup"><span data-stu-id="c07f7-122">DTS audio</span></span>                                      |
| <span data-ttu-id="c07f7-123">**\_GUID AVDecAudioInputHEAAC di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-123">**CODECAPI\_GUID\_AVDecAudioInputHEAAC**</span></span>            | <span data-ttu-id="c07f7-124">High-Efficiency codifica audio avanzata (HE-AAC)</span><span class="sxs-lookup"><span data-stu-id="c07f7-124">High-Efficiency Advanced Audio Coding (HE-AAC)</span></span> |
| <span data-ttu-id="c07f7-125">**\_GUID AVDecAudioInputMPEG di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-125">**CODECAPI\_GUID\_AVDecAudioInputMPEG**</span></span>             | <span data-ttu-id="c07f7-126">Audio MPEG</span><span class="sxs-lookup"><span data-stu-id="c07f7-126">MPEG audio</span></span>                                     |
| <span data-ttu-id="c07f7-127">**\_GUID AVDecAudioInputPCM di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-127">**CODECAPI\_GUID\_AVDecAudioInputPCM**</span></span>              | <span data-ttu-id="c07f7-128">Audio PCM</span><span class="sxs-lookup"><span data-stu-id="c07f7-128">PCM audio</span></span>                                      |
| <span data-ttu-id="c07f7-129">**\_GUID AVDecAudioInputWMA di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-129">**CODECAPI\_GUID\_AVDecAudioInputWMA**</span></span>              | <span data-ttu-id="c07f7-130">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="c07f7-130">Windows Media Audio</span></span>                            |
| <span data-ttu-id="c07f7-131">**\_GUID AVDecAudioInputWMAPro di CODEcapi \_**</span><span class="sxs-lookup"><span data-stu-id="c07f7-131">**CODECAPI\_GUID\_AVDecAudioInputWMAPro**</span></span>           | <span data-ttu-id="c07f7-132">Windows Media Audio 9 Professional (WMA Pro)</span><span class="sxs-lookup"><span data-stu-id="c07f7-132">Windows Media Audio 9 Professional (WMA Pro)</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="c07f7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c07f7-133">Requirements</span></span>



| <span data-ttu-id="c07f7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c07f7-134">Requirement</span></span> | <span data-ttu-id="c07f7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c07f7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c07f7-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c07f7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c07f7-137">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="c07f7-137">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c07f7-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c07f7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c07f7-139">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c07f7-139">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c07f7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c07f7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c07f7-141"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="c07f7-141"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c07f7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c07f7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07f7-143">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="c07f7-143">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c07f7-144">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c07f7-144">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




