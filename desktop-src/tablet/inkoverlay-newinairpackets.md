---
description: Si verifica quando viene visualizzato un pacchetto in aria.
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: Evento InkOverlay. NewInAirPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ac030a2e32ecf662d811a3c91ccdc2dd3c5fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233182"
---
# <a name="inkoverlaynewinairpackets-event"></a><span data-ttu-id="7eb1a-103">Evento InkOverlay. NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="7eb1a-103">InkOverlay.NewInAirPackets event</span></span>

<span data-ttu-id="7eb1a-104">Si verifica quando viene visualizzato un pacchetto in aria.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb1a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7eb1a-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="7eb1a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7eb1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eb1a-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7eb1a-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb1a-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**NewInAirPackets**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="7eb1a-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="7eb1a-109">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7eb1a-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb1a-110">Numero di pacchetti in aria ricevuti.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="7eb1a-111">*PacketData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7eb1a-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb1a-112">Matrice che contiene i dati selezionati per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="7eb1a-113">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="7eb1a-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eb1a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7eb1a-114">Return value</span></span>

<span data-ttu-id="7eb1a-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eb1a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7eb1a-116">Remarks</span></span>

<span data-ttu-id="7eb1a-117">Viene creato un pacchetto in aria quando un utente sposta una penna accanto al tablet e il cursore si trova all'interno della finestra dell'oggetto agente di raccolta input penna oppure l'utente sposta il mouse all'interno della finestra associata dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="7eb1a-118">Gli eventi [**NewInAirPackets**](inkcollector-newinairpackets.md) vengono generati rapidamente e il gestore eventi deve essere troppo veloce o le prestazioni subiscono problemi.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-118">[**NewInAirPackets**](inkcollector-newinairpackets.md) events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="7eb1a-119">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="7eb1a-120">L'evento [**NewInAirPackets**](inkcollector-newinairpackets.md) viene generato anche in modalità selezione o cancellazione, non solo quando si inserisce input penna.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-120">The [**NewInAirPackets**](inkcollector-newinairpackets.md) event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="7eb1a-121">A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="7eb1a-122">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="7eb1a-123">Per impostare le proprietà contenute in questa matrice, utilizzare la proprietà [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="7eb1a-124">La matrice restituita dal parametro *PacketData* contiene i dati per tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="7eb1a-125">Sebbene sia possibile modificare i dati dei pacchetti, queste modifiche non vengono mantenute o utilizzate.</span><span class="sxs-lookup"><span data-stu-id="7eb1a-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7eb1a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7eb1a-126">Requirements</span></span>



| <span data-ttu-id="7eb1a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eb1a-127">Requirement</span></span> | <span data-ttu-id="7eb1a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="7eb1a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb1a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7eb1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7eb1a-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7eb1a-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7eb1a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7eb1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7eb1a-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7eb1a-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7eb1a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7eb1a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7eb1a-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7eb1a-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7eb1a-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="7eb1a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7eb1a-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eb1a-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7eb1a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7eb1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb1a-138">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="7eb1a-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="7eb1a-139">**Proprietà DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="7eb1a-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="7eb1a-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="7eb1a-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="7eb1a-141">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="7eb1a-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




