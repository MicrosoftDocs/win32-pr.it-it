---
description: "Evento InkCollector.NewPackets: si verifica quando l'agente di raccolta input penna riceve un pacchetto."
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Evento InkCollector.NewPackets (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bab9d13dd2f33689700ef4a9aee2ed5059403e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110119"
---
# <a name="inkcollectornewpackets-event"></a><span data-ttu-id="5ee21-103">Evento InkCollector.NewPackets</span><span class="sxs-lookup"><span data-stu-id="5ee21-103">InkCollector.NewPackets event</span></span>

<span data-ttu-id="5ee21-104">Si verifica quando l'agente di raccolta input penna riceve un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5ee21-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee21-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ee21-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="5ee21-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ee21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ee21-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5ee21-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee21-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento NewInAirPackets.**](inkcollector-newinairpackets.md)</span><span class="sxs-lookup"><span data-stu-id="5ee21-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="5ee21-109">*Tratto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5ee21-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee21-110">Specifica [**l'oggetto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="5ee21-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="5ee21-111">*PacketCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5ee21-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee21-112">Numero di pacchetti ricevuti per un [**oggetto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="5ee21-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="5ee21-113">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5ee21-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee21-114">Quando questo metodo viene restituito, contiene una matrice che contiene i dati selezionati per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5ee21-114">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="5ee21-115">Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM.](using-the-com-library.md)</span><span class="sxs-lookup"><span data-stu-id="5ee21-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ee21-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ee21-116">Return value</span></span>

<span data-ttu-id="5ee21-117">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5ee21-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ee21-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ee21-118">Remarks</span></span>

<span data-ttu-id="5ee21-119">I pacchetti vengono ricevuti durante la raccolta di un tratto.</span><span class="sxs-lookup"><span data-stu-id="5ee21-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="5ee21-120">Gli eventi di pacchetto si verificano rapidamente e un gestore eventi **NewPackets** deve essere veloce o le prestazioni ne risentiranno.</span><span class="sxs-lookup"><span data-stu-id="5ee21-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="5ee21-121">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICENewPackets.</span><span class="sxs-lookup"><span data-stu-id="5ee21-121">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="5ee21-122">Questo evento deve essere usato con attenzione perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se viene eseguita una quantità troppo grande di codice nei gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="5ee21-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="5ee21-123">Per impostare le proprietà contenute in questa matrice, usare la [**proprietà DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="5ee21-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="5ee21-124">La matrice restituita *dal parametro PacketData* contiene i dati per tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ee21-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="5ee21-125">Anche se è possibile modificare i dati del pacchetto, queste modifiche non vengono rese persistenti o usate.</span><span class="sxs-lookup"><span data-stu-id="5ee21-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ee21-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ee21-126">Requirements</span></span>



| <span data-ttu-id="5ee21-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee21-127">Requirement</span></span> | <span data-ttu-id="5ee21-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5ee21-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee21-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ee21-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ee21-130">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="5ee21-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ee21-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ee21-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ee21-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ee21-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5ee21-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ee21-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ee21-134"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ee21-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ee21-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ee21-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ee21-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ee21-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5ee21-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ee21-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee21-138">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="5ee21-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="5ee21-139">**Evento NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="5ee21-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="5ee21-140">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="5ee21-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="5ee21-141">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="5ee21-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




