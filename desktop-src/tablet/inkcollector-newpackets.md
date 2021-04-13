---
description: Si verifica quando l'agente di raccolta input penna riceve un pacchetto.
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Evento InkCollector. NewPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b03e1a561a61c9b291bca8e59f990dc12b4e2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342811"
---
# <a name="inkcollectornewpackets-event"></a><span data-ttu-id="b6af7-103">Evento InkCollector. NewPackets</span><span class="sxs-lookup"><span data-stu-id="b6af7-103">InkCollector.NewPackets event</span></span>

<span data-ttu-id="b6af7-104">Si verifica quando l'agente di raccolta input penna riceve un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="b6af7-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6af7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6af7-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="b6af7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6af7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6af7-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6af7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6af7-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**NewInAirPackets**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="b6af7-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="b6af7-109">*Tratto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6af7-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6af7-110">Specifica l'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="b6af7-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="b6af7-111">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6af7-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6af7-112">Numero di pacchetti ricevuti per un oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="b6af7-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="b6af7-113">*PacketData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b6af7-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6af7-114">Quando termina, questo metodo contiene una matrice che contiene i dati selezionati per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="b6af7-114">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="b6af7-115">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="b6af7-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6af7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6af7-116">Return value</span></span>

<span data-ttu-id="b6af7-117">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b6af7-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6af7-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6af7-118">Remarks</span></span>

<span data-ttu-id="b6af7-119">I pacchetti vengono ricevuti durante la raccolta di un tratto.</span><span class="sxs-lookup"><span data-stu-id="b6af7-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="b6af7-120">Gli eventi di pacchetti si verificano rapidamente e un gestore dell'evento **NewPackets** deve avere una velocità elevata o prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="b6af7-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="b6af7-121">Il metodo dell'evento TThis è definito nelle \_ \_ interfacce di solo invio IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (DISPINTERFACES) con ID DISPID \_ ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="b6af7-121">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="b6af7-122">Questo evento deve essere usato con cautela perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se nei gestori eventi viene eseguita una quantità eccessiva di codice.</span><span class="sxs-lookup"><span data-stu-id="b6af7-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="b6af7-123">Per impostare le proprietà contenute in questa matrice, utilizzare la proprietà [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="b6af7-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="b6af7-124">La matrice restituita dal parametro *PacketData* contiene i dati per tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6af7-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="b6af7-125">Sebbene sia possibile modificare i dati dei pacchetti, queste modifiche non vengono mantenute o utilizzate.</span><span class="sxs-lookup"><span data-stu-id="b6af7-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6af7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6af7-126">Requirements</span></span>



| <span data-ttu-id="b6af7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6af7-127">Requirement</span></span> | <span data-ttu-id="b6af7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b6af7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6af7-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6af7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b6af7-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b6af7-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b6af7-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6af7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b6af7-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b6af7-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b6af7-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6af7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6af7-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b6af7-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b6af7-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6af7-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6af7-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6af7-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b6af7-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6af7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6af7-138">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="b6af7-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="b6af7-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="b6af7-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="b6af7-140">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="b6af7-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="b6af7-141">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="b6af7-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




