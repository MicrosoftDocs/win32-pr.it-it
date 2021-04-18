---
description: "L'interfaccia IEnumParticipant fornisce metodi di enumerazione standard COM per l'interfaccia ITParticipant. Il metodo ITParticipantControl:: EnumerateParticipants restituisce un puntatore a IEnumParticipant."
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interfaccia IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330747"
---
# <a name="ienumparticipant-interface"></a><span data-ttu-id="daf8b-104">Interfaccia IEnumParticipant</span><span class="sxs-lookup"><span data-stu-id="daf8b-104">IEnumParticipant interface</span></span>

<span data-ttu-id="daf8b-105">\[**IEnumParticipant** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="daf8b-105">\[**IEnumParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="daf8b-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="daf8b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="daf8b-107">L'interfaccia **IEnumParticipant** fornisce metodi di enumerazione standard com per l'interfaccia [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="daf8b-107">The **IEnumParticipant** interface provides COM-standard enumeration methods for the [**ITParticipant**](itparticipant.md) interface.</span></span> <span data-ttu-id="daf8b-108">Il metodo [**ITParticipantControl:: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) restituisce un puntatore a **IEnumParticipant**.</span><span class="sxs-lookup"><span data-stu-id="daf8b-108">The [**ITParticipantControl::EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method returns a pointer to **IEnumParticipant**.</span></span>

<span data-ttu-id="daf8b-109">L'interfaccia **IEnumParticipant** è nascosta per Visual Basic e linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="daf8b-109">The **IEnumParticipant** interface is hidden from Visual Basic and scripting languages.</span></span>

## <a name="members"></a><span data-ttu-id="daf8b-110">Membri</span><span class="sxs-lookup"><span data-stu-id="daf8b-110">Members</span></span>

<span data-ttu-id="daf8b-111">L'interfaccia **IEnumParticipant** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="daf8b-111">The **IEnumParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="daf8b-112">**IEnumParticipant** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="daf8b-112">**IEnumParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="daf8b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="daf8b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="daf8b-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="daf8b-114">Methods</span></span>

<span data-ttu-id="daf8b-115">L'interfaccia **IEnumParticipant** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="daf8b-115">The **IEnumParticipant** interface has these methods.</span></span>



| <span data-ttu-id="daf8b-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="daf8b-116">Method</span></span>                                  | <span data-ttu-id="daf8b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="daf8b-117">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="daf8b-118">**Clone**</span><span class="sxs-lookup"><span data-stu-id="daf8b-118">**Clone**</span></span>](ienumparticipant-clone.md) | <span data-ttu-id="daf8b-119">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="daf8b-119">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="daf8b-120">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="daf8b-120">**Next**</span></span>](ienumparticipant-next.md)   | <span data-ttu-id="daf8b-121">Ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="daf8b-121">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="daf8b-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="daf8b-122">**Reset**</span></span>](ienumparticipant-reset.md) | <span data-ttu-id="daf8b-123">Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="daf8b-123">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="daf8b-124">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="daf8b-124">**Skip**</span></span>](ienumparticipant-skip.md)   | <span data-ttu-id="daf8b-125">Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="daf8b-125">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="daf8b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="daf8b-126">Requirements</span></span>



| <span data-ttu-id="daf8b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="daf8b-127">Requirement</span></span> | <span data-ttu-id="daf8b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="daf8b-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="daf8b-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="daf8b-129">TAPI version</span></span><br/> | <span data-ttu-id="daf8b-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="daf8b-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="daf8b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="daf8b-131">Header</span></span><br/>       | <dl> <span data-ttu-id="daf8b-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="daf8b-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="daf8b-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="daf8b-133">Library</span></span><br/>      | <dl> <span data-ttu-id="daf8b-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="daf8b-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="daf8b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="daf8b-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="daf8b-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daf8b-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="daf8b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="daf8b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf8b-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="daf8b-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

