---
description: Specifica il modo in cui la sessione multimediale arresta un oggetto nella topologia.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: Attributo MF_TOPONODE_NOSHUTDOWN_ON_REMOVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308442"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a><span data-ttu-id="0b5d0-103">MF \_ TOPONODE \_ noshutdown \_ sull' \_ attributo Remove</span><span class="sxs-lookup"><span data-stu-id="0b5d0-103">MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE attribute</span></span>

<span data-ttu-id="0b5d0-104">Specifica il modo in cui la sessione multimediale arresta un oggetto nella topologia.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-104">Specifies how the Media Session shuts down an object in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="0b5d0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0b5d0-105">Data type</span></span>

<span data-ttu-id="0b5d0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0b5d0-106">**UINT32**</span></span>

<span data-ttu-id="0b5d0-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b5d0-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b5d0-108">Remarks</span></span>

<span data-ttu-id="0b5d0-109">Questo attributo si applica ai tipi di nodo di topologia seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b5d0-109">This attribute applies to the following types of toplogy node:</span></span>

-   <span data-ttu-id="0b5d0-110">Nodi di output</span><span class="sxs-lookup"><span data-stu-id="0b5d0-110">Output nodes</span></span>
-   <span data-ttu-id="0b5d0-111">Qualsiasi nodo di trasformazione che contiene una trasformazione di Media Foundation *asincrona* (MFT).</span><span class="sxs-lookup"><span data-stu-id="0b5d0-111">Any transform node that contains an *asynchronous* Media Foundation transform (MFT).</span></span>

<span data-ttu-id="0b5d0-112">L'attributo può avere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b5d0-112">The attribute can have the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b5d0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0b5d0-113">Value</span></span></th>
<th><span data-ttu-id="0b5d0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b5d0-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b5d0-115"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="0b5d0-115"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="0b5d0-116">Quando la sessione multimediale passa a una nuova topologia o cancella la topologia corrente, non arresta l'oggetto che appartiene a questo nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-116">When the Media Session switches to a new topology or clears the current topology, it does not shut down the object that belongs to this topology node.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b5d0-117"><strong>FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="0b5d0-117"><strong>FALSE</strong></span></span></td>
<td><span data-ttu-id="0b5d0-118">Quando la sessione multimediale passa a una nuova topologia o cancella la topologia corrente, arresta l'oggetto nodo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0b5d0-118">When the Media Session switches to a new topology or clears the current topology, it shuts down the node object, as follows:</span></span>
<ul>
<li><span data-ttu-id="0b5d0-119">Nodi di output: la sessione chiama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink:: Shutdown</strong></a> sul sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-119">Output nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink::Shutdown</strong></a> on the media sink.</span></span></li>
<li><span data-ttu-id="0b5d0-120">Nodi di trasformazione: la sessione chiama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown:: Shutdown</strong></a> sulla MFT.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-120">Transform nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown::Shutdown</strong></a> on the MFT.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0b5d0-121">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-121">The default value is **TRUE**.</span></span>

<span data-ttu-id="0b5d0-122">Se l'applicazione Accoda più topologie, è consigliabile impostare questo attributo su **false**.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-122">If your application queues multiple topologies, it is a good idea to set this attribute to **FALSE**.</span></span> <span data-ttu-id="0b5d0-123">In caso contrario, gli oggetti della topologia potrebbero non essere arrestati correttamente.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-123">Otherwise, objects in the topology might not be shut down correctly.</span></span>

<span data-ttu-id="0b5d0-124">Questo attributo non si applica quando l'applicazione arresta la sessione multimediale chiamando [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="0b5d0-124">This attribute does not apply when the application shuts down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="0b5d0-125">Quando la sessione multimediale viene arrestata, arresta sempre i sink del supporto e i MFTs asincroni nella topologia corrente.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-125">When the Media Session shuts down, it always shuts down the media sinks and asynchronous MFTs in the current topology.</span></span>

<span data-ttu-id="0b5d0-126">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b5d0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b5d0-127">Requirements</span></span>



| <span data-ttu-id="0b5d0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b5d0-128">Requirement</span></span> | <span data-ttu-id="0b5d0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0b5d0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b5d0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b5d0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0b5d0-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b5d0-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0b5d0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b5d0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0b5d0-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b5d0-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0b5d0-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b5d0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b5d0-135"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b5d0-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b5d0-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b5d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b5d0-137">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b5d0-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b5d0-138">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="0b5d0-138">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="0b5d0-139">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="0b5d0-139">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b5d0-140">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="0b5d0-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0b5d0-141">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="0b5d0-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0b5d0-142">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="0b5d0-142">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




