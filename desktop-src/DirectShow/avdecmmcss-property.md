---
description: Specifica la classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per il thread di decodifica.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Proprietà AVDecMmcss (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332709"
---
# <a name="avdecmmcss-property"></a><span data-ttu-id="fe111-103">Proprietà AVDecMmcss</span><span class="sxs-lookup"><span data-stu-id="fe111-103">AVDecMmcss property</span></span>

<span data-ttu-id="fe111-104">Specifica la classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per il thread di decodifica.</span><span class="sxs-lookup"><span data-stu-id="fe111-104">Specifies the Multimedia Class Scheduler Service (MMCSS) class for the decoding thread.</span></span>

<span data-ttu-id="fe111-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fe111-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe111-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fe111-106">Data type</span></span>

<span data-ttu-id="fe111-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="fe111-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fe111-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="fe111-108">Property GUID</span></span>

<span data-ttu-id="fe111-109">**Codecapis \_ AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="fe111-109">**CODECAPI\_AVDecMmcssClass**</span></span>

## <a name="property-value"></a><span data-ttu-id="fe111-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fe111-110">Property value</span></span>

<span data-ttu-id="fe111-111">Il valore di questa proprietà è il nome della classe MMCSS.</span><span class="sxs-lookup"><span data-stu-id="fe111-111">The value of this property is the name of the MMCSS class.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe111-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe111-112">Remarks</span></span>

<span data-ttu-id="fe111-113">MMCSS consente alle applicazioni di garantire che l'elaborazione con distinzione del tempo abbia l'accesso in ordine di priorità alle risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="fe111-113">MMCSS enables applications to ensure that time-sensitive processing has prioritized access to CPU resources.</span></span> <span data-ttu-id="fe111-114">Funziona elevando i thread registrati a priorità dei thread più elevate, diminuendo periodicamente le priorità per produrre tempo per altri processi.</span><span class="sxs-lookup"><span data-stu-id="fe111-114">It works by elevating registered threads to higher thread priorities while periodically decreasing their priorities to yield time to other processes.</span></span>

<span data-ttu-id="fe111-115">Il valore consigliato per i decodificatori audio è "audio" e il valore consigliato per i decodificatori video è "Playback".</span><span class="sxs-lookup"><span data-stu-id="fe111-115">The recommended value for audio decoders is "Audio," and the recommended value for video decoders is "Playback."</span></span>

<span data-ttu-id="fe111-116">Se il servizio MMCSS non è disponibile o la classe MMCSS specificata non esiste, l'impostazione della proprietà non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="fe111-116">If the MMCSS service is not available or the specified MMCSS class does not exist, setting the property has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe111-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe111-117">Requirements</span></span>



| <span data-ttu-id="fe111-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe111-118">Requirement</span></span> | <span data-ttu-id="fe111-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fe111-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe111-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe111-120">Header</span></span><br/> | <dl> <span data-ttu-id="fe111-121"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe111-121"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe111-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe111-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe111-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="fe111-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fe111-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fe111-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




