---
description: 'Evento InkPicture.NewInAirPackets: si verifica quando viene visualizzato un pacchetto in ingresso.'
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: Evento InkPicture.NewInAirPackets (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0de8f2423817bada84f83b63de1517393740db4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086559"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="88112-103">Evento InkPicture.NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="88112-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="88112-104">Si verifica quando viene visualizzato un pacchetto in aria.</span><span class="sxs-lookup"><span data-stu-id="88112-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="88112-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88112-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="88112-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="88112-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88112-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="88112-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88112-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento NewInAirPackets.**</span><span class="sxs-lookup"><span data-stu-id="88112-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="88112-109">*PacketCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="88112-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88112-110">Numero di pacchetti in aria ricevuti.</span><span class="sxs-lookup"><span data-stu-id="88112-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="88112-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="88112-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="88112-112">Matrice contenente i dati selezionati per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="88112-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="88112-113">Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="88112-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88112-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88112-114">Return value</span></span>

<span data-ttu-id="88112-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="88112-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88112-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="88112-116">Remarks</span></span>

<span data-ttu-id="88112-117">Un pacchetto in air viene creato quando un utente sposta una penna vicino al tablet e il cursore si trova all'interno della finestra dell'oggetto dell'agente di raccolta input penna oppure l'utente sposta un mouse all'interno della finestra associata dell'oggetto dell'agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="88112-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="88112-118">**Gli eventi NewInAirPackets** vengono generati rapidamente e il gestore eventi deve essere veloce o le prestazioni ne risentiranno.</span><span class="sxs-lookup"><span data-stu-id="88112-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="88112-119">Questo metodo di evento è definito nelle interfacce di solo invio **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ DISPID ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="88112-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="88112-120">**L'evento NewInAirPackets** viene generato anche in modalità di selezione o cancellazione, non solo quando si inserisce l'input penna.</span><span class="sxs-lookup"><span data-stu-id="88112-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="88112-121">A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="88112-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="88112-122">Il vantaggio di questo requisito è una maggiore libertà di innovare sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="88112-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="88112-123">Per impostare le proprietà contenute in questa matrice, usare la [**proprietà DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="88112-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="88112-124">La matrice *restituita dal parametro PacketData* contiene i dati per tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="88112-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="88112-125">Sebbene sia possibile modificare i dati del pacchetto, queste modifiche non vengono rese persistenti o utilizzate.</span><span class="sxs-lookup"><span data-stu-id="88112-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88112-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88112-126">Requirements</span></span>



| <span data-ttu-id="88112-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="88112-127">Requirement</span></span> | <span data-ttu-id="88112-128">Valore</span><span class="sxs-lookup"><span data-stu-id="88112-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88112-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88112-129">Minimum supported client</span></span><br/> | <span data-ttu-id="88112-130">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="88112-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="88112-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88112-131">Minimum supported server</span></span><br/> | <span data-ttu-id="88112-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="88112-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="88112-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88112-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="88112-134"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="88112-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88112-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="88112-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="88112-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88112-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="88112-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88112-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88112-138">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="88112-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="88112-139">**Proprietà DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="88112-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="88112-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="88112-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="88112-141">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="88112-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




