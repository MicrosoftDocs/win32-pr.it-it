---
description: Si verifica quando viene visualizzato un pacchetto in aria.
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: Evento InkPicture. NewInAirPackets (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0331eb4e855e2051cd8b2b6d7b312d7f32e76096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313929"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="da00f-103">Evento InkPicture. NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="da00f-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="da00f-104">Si verifica quando viene visualizzato un pacchetto in aria.</span><span class="sxs-lookup"><span data-stu-id="da00f-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="da00f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da00f-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="da00f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da00f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da00f-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da00f-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da00f-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **NewInAirPackets** .</span><span class="sxs-lookup"><span data-stu-id="da00f-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="da00f-109">*PacketCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da00f-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da00f-110">Numero di pacchetti in aria ricevuti.</span><span class="sxs-lookup"><span data-stu-id="da00f-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="da00f-111">*PacketData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="da00f-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da00f-112">Matrice che contiene i dati selezionati per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="da00f-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="da00f-113">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="da00f-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da00f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da00f-114">Return value</span></span>

<span data-ttu-id="da00f-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="da00f-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da00f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="da00f-116">Remarks</span></span>

<span data-ttu-id="da00f-117">Viene creato un pacchetto in aria quando un utente sposta una penna accanto al tablet e il cursore si trova all'interno della finestra dell'oggetto agente di raccolta input penna oppure l'utente sposta il mouse all'interno della finestra associata dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="da00f-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="da00f-118">Gli eventi **NewInAirPackets** vengono generati rapidamente e il gestore eventi deve essere troppo veloce o le prestazioni subiscono problemi.</span><span class="sxs-lookup"><span data-stu-id="da00f-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="da00f-119">Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch (dispinterfaces) con ID DISPID \_ ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="da00f-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="da00f-120">L'evento **NewInAirPackets** viene generato anche in modalità selezione o cancellazione, non solo quando si inserisce input penna.</span><span class="sxs-lookup"><span data-stu-id="da00f-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="da00f-121">A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="da00f-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="da00f-122">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="da00f-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="da00f-123">Per impostare le proprietà contenute in questa matrice, utilizzare la proprietà [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) dell'oggetto agente di raccolta input penna.</span><span class="sxs-lookup"><span data-stu-id="da00f-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="da00f-124">La matrice restituita dal parametro *PacketData* contiene i dati per tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="da00f-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="da00f-125">Sebbene sia possibile modificare i dati dei pacchetti, queste modifiche non vengono mantenute o utilizzate.</span><span class="sxs-lookup"><span data-stu-id="da00f-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da00f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da00f-126">Requirements</span></span>



| <span data-ttu-id="da00f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="da00f-127">Requirement</span></span> | <span data-ttu-id="da00f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="da00f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da00f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da00f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="da00f-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="da00f-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="da00f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da00f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="da00f-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="da00f-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="da00f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da00f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="da00f-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="da00f-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="da00f-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="da00f-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="da00f-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da00f-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="da00f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da00f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da00f-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="da00f-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="da00f-139">**Proprietà DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="da00f-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="da00f-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="da00f-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="da00f-141">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="da00f-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




