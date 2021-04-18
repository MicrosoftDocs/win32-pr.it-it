---
description: Ottiene le dimensioni in pixel dell'immagine decodificata.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Proprietà AVDecVideoImageSize (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304250"
---
# <a name="avdecvideoimagesize-property"></a><span data-ttu-id="cc621-103">Proprietà AVDecVideoImageSize</span><span class="sxs-lookup"><span data-stu-id="cc621-103">AVDecVideoImageSize property</span></span>

<span data-ttu-id="cc621-104">Ottiene le dimensioni in pixel dell'immagine decodificata.</span><span class="sxs-lookup"><span data-stu-id="cc621-104">Gets the size of the decoded image, in pixels.</span></span>

<span data-ttu-id="cc621-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cc621-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="cc621-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cc621-106">Data type</span></span>

<span data-ttu-id="cc621-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="cc621-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cc621-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="cc621-108">Property GUID</span></span>

<span data-ttu-id="cc621-109">**Codecapis \_ AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="cc621-109">**CODECAPI\_AVDecVideoImageSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="cc621-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cc621-110">Property value</span></span>

<span data-ttu-id="cc621-111">I 16 bit alti contengono la larghezza e i 16 bit bassi contengono l'altezza.</span><span class="sxs-lookup"><span data-stu-id="cc621-111">The high 16 bits contain the width, and the low 16 bits contain the height.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc621-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc621-112">Remarks</span></span>

<span data-ttu-id="cc621-113">Il numero di canali include il canale LFE (Low Frequency Effect), se presente.</span><span class="sxs-lookup"><span data-stu-id="cc621-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc621-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc621-114">Requirements</span></span>



| <span data-ttu-id="cc621-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc621-115">Requirement</span></span> | <span data-ttu-id="cc621-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cc621-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc621-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc621-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc621-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="cc621-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cc621-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc621-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc621-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cc621-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cc621-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc621-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc621-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc621-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc621-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc621-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc621-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="cc621-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cc621-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="cc621-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




