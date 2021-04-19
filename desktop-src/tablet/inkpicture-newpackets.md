---
description: Si verifica quando l'agente di raccolta input penna riceve un pacchetto.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: Evento InkPicture. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0b3e1df0df2ba051150550daa60772e2a068df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313928"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="d02b6-103">Evento InkPicture. NewPackets</span><span class="sxs-lookup"><span data-stu-id="d02b6-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="d02b6-104">Si verifica quando l'agente di raccolta input penna riceve un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d02b6-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02b6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d02b6-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="d02b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d02b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d02b6-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d02b6-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d02b6-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**NewInAirPackets**](inkpicture-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="d02b6-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="d02b6-109">*Tratto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d02b6-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d02b6-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="d02b6-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="d02b6-111">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d02b6-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d02b6-112">Numero di pacchetti ricevuti per un oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="d02b6-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="d02b6-113">*PacketData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d02b6-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d02b6-114">Matrice che contiene i dati selezionati per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d02b6-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="d02b6-115">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="d02b6-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d02b6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d02b6-116">Return value</span></span>

<span data-ttu-id="d02b6-117">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d02b6-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d02b6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d02b6-118">Remarks</span></span>

<span data-ttu-id="d02b6-119">I pacchetti vengono ricevuti durante la raccolta di un tratto.</span><span class="sxs-lookup"><span data-stu-id="d02b6-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="d02b6-120">Gli eventi di pacchetti si verificano rapidamente e un gestore dell'evento **NewPackets** deve avere una velocità elevata o prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="d02b6-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="d02b6-121">Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch (dispinterfaces) con ID DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="d02b6-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="d02b6-122">Questo evento deve essere usato con cautela perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se nei gestori eventi viene eseguita una quantità eccessiva di codice.</span><span class="sxs-lookup"><span data-stu-id="d02b6-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="d02b6-123">Per impostare le proprietà contenute in questa matrice, utilizzare la proprietà [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="d02b6-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="d02b6-124">La matrice restituita dal parametro *PacketData* contiene i dati per tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="d02b6-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="d02b6-125">Sebbene sia possibile modificare i dati dei pacchetti, queste modifiche non vengono mantenute o utilizzate.</span><span class="sxs-lookup"><span data-stu-id="d02b6-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d02b6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d02b6-126">Requirements</span></span>



| <span data-ttu-id="d02b6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d02b6-127">Requirement</span></span> | <span data-ttu-id="d02b6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="d02b6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d02b6-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d02b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d02b6-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d02b6-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d02b6-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d02b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d02b6-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d02b6-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d02b6-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d02b6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d02b6-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d02b6-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d02b6-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="d02b6-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d02b6-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d02b6-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d02b6-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d02b6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02b6-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d02b6-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d02b6-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="d02b6-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="d02b6-140">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="d02b6-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="d02b6-141">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="d02b6-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




