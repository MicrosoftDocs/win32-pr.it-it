---
description: Si verifica quando viene visualizzato un pacchetto in aria.
ms.assetid: e8eacdec-0381-435f-b453-24dca1c507c9
title: Evento InkCollector. NewInAirPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d942aa474b5cb53d01f5ce83d2bd3ec28d521c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314925"
---
# <a name="inkcollectornewinairpackets-event"></a><span data-ttu-id="58e67-103">Evento InkCollector. NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="58e67-103">InkCollector.NewInAirPackets event</span></span>

<span data-ttu-id="58e67-104">Si verifica quando viene visualizzato un pacchetto in aria.</span><span class="sxs-lookup"><span data-stu-id="58e67-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e67-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58e67-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="58e67-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58e67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e67-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e67-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e67-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **NewInAirPackets** .</span><span class="sxs-lookup"><span data-stu-id="58e67-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="58e67-109">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e67-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e67-110">Numero di pacchetti in aria ricevuti.</span><span class="sxs-lookup"><span data-stu-id="58e67-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="58e67-111">*PacketData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="58e67-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="58e67-112">Quando termina, questo metodo contiene una matrice che contiene i dati selezionati per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="58e67-112">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="58e67-113">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="58e67-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e67-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58e67-114">Return value</span></span>

<span data-ttu-id="58e67-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="58e67-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e67-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="58e67-116">Remarks</span></span>

<span data-ttu-id="58e67-117">Viene creato un pacchetto in aria quando un utente sposta una penna accanto al tablet e il cursore si trova all'interno della finestra dell'oggetto agente di raccolta input penna oppure l'utente sposta il mouse all'interno della finestra associata dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="58e67-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="58e67-118">Gli eventi **NewInAirPackets** vengono generati rapidamente e il gestore eventi deve essere troppo veloce o le prestazioni subiscono problemi.</span><span class="sxs-lookup"><span data-stu-id="58e67-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="58e67-119">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="58e67-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="58e67-120">L'evento **NewInAirPackets** viene generato anche in modalità selezione o cancellazione, non solo quando si inserisce input penna.</span><span class="sxs-lookup"><span data-stu-id="58e67-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="58e67-121">A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="58e67-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="58e67-122">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="58e67-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="58e67-123">Per impostare le proprietà contenute in questa matrice, utilizzare la proprietà [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="58e67-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="58e67-124">La matrice restituita dal parametro *PacketData* contiene i dati per tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="58e67-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="58e67-125">Sebbene sia possibile modificare i dati dei pacchetti, queste modifiche non vengono mantenute o utilizzate.</span><span class="sxs-lookup"><span data-stu-id="58e67-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58e67-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58e67-126">Requirements</span></span>



| <span data-ttu-id="58e67-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e67-127">Requirement</span></span> | <span data-ttu-id="58e67-128">Valore</span><span class="sxs-lookup"><span data-stu-id="58e67-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e67-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58e67-129">Minimum supported client</span></span><br/> | <span data-ttu-id="58e67-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="58e67-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="58e67-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58e67-131">Minimum supported server</span></span><br/> | <span data-ttu-id="58e67-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="58e67-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="58e67-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58e67-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e67-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="58e67-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="58e67-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="58e67-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="58e67-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e67-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="58e67-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58e67-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e67-138">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="58e67-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="58e67-139">**Proprietà DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="58e67-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="58e67-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="58e67-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="58e67-141">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="58e67-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




