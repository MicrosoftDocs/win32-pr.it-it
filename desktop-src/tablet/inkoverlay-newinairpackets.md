---
description: 'Evento InkOverlay.NewInAirPackets: si verifica quando viene visualizzato un pacchetto in air.'
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: Evento InkOverlay.NewInAirPackets (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39e568941b1af0727ad9c8464913325409b4604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086709"
---
# <a name="inkoverlaynewinairpackets-event"></a><span data-ttu-id="011b4-103">Evento InkOverlay.NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="011b4-103">InkOverlay.NewInAirPackets event</span></span>

<span data-ttu-id="011b4-104">Si verifica quando viene visualizzato un pacchetto in aria.</span><span class="sxs-lookup"><span data-stu-id="011b4-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="011b4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="011b4-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="011b4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="011b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="011b4-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="011b4-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="011b4-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento NewInAirPackets.**](inkcollector-newinairpackets.md)</span><span class="sxs-lookup"><span data-stu-id="011b4-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="011b4-109">*PacketCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="011b4-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="011b4-110">Numero di pacchetti in aria ricevuti.</span><span class="sxs-lookup"><span data-stu-id="011b4-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="011b4-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="011b4-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="011b4-112">Matrice che contiene i dati selezionati per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="011b4-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="011b4-113">Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="011b4-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="011b4-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="011b4-114">Return value</span></span>

<span data-ttu-id="011b4-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="011b4-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="011b4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="011b4-116">Remarks</span></span>

<span data-ttu-id="011b4-117">Un pacchetto in air viene creato quando un utente sposta una penna vicino al tablet e il cursore si trova all'interno della finestra dell'oggetto dell'agente di raccolta input penna oppure l'utente sposta un mouse all'interno della finestra associata dell'oggetto dell'agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="011b4-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="011b4-118">[**Gli eventi NewInAirPackets**](inkcollector-newinairpackets.md) vengono generati rapidamente e il gestore eventi deve essere veloce o le prestazioni ne risentiranno.</span><span class="sxs-lookup"><span data-stu-id="011b4-118">[**NewInAirPackets**](inkcollector-newinairpackets.md) events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="011b4-119">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="011b4-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="011b4-120">[**L'evento NewInAirPackets**](inkcollector-newinairpackets.md) viene generato anche in modalità di selezione o cancellazione, non solo quando si inserisce l'input penna.</span><span class="sxs-lookup"><span data-stu-id="011b4-120">The [**NewInAirPackets**](inkcollector-newinairpackets.md) event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="011b4-121">A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="011b4-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="011b4-122">Il vantaggio di questo requisito è una maggiore libertà di innovare sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="011b4-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="011b4-123">Per impostare le proprietà contenute in questa matrice, usare la [**proprietà DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="011b4-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="011b4-124">La matrice *restituita dal parametro PacketData* contiene i dati per tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="011b4-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="011b4-125">Sebbene sia possibile modificare i dati del pacchetto, queste modifiche non vengono rese persistenti o utilizzate.</span><span class="sxs-lookup"><span data-stu-id="011b4-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="011b4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="011b4-126">Requirements</span></span>



| <span data-ttu-id="011b4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="011b4-127">Requirement</span></span> | <span data-ttu-id="011b4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="011b4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="011b4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="011b4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="011b4-130">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="011b4-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="011b4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="011b4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="011b4-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="011b4-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="011b4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="011b4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="011b4-134"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="011b4-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="011b4-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="011b4-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="011b4-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="011b4-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="011b4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="011b4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011b4-138">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="011b4-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="011b4-139">**Proprietà DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="011b4-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="011b4-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="011b4-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="011b4-141">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="011b4-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




