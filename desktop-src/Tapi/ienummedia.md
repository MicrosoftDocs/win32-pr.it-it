---
description: "L'interfaccia IEnumMedia fornisce metodi di enumerazione standard COM per l'interfaccia ITMedia. Il metodo ITMediaCollection:: Get \\_ EnumerationIf restituisce un puntatore a IEnumMedia."
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interfaccia IEnumMedia (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333145"
---
# <a name="ienummedia-interface"></a><span data-ttu-id="63a33-104">Interfaccia IEnumMedia</span><span class="sxs-lookup"><span data-stu-id="63a33-104">IEnumMedia interface</span></span>

<span data-ttu-id="63a33-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63a33-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="63a33-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="63a33-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="63a33-107">L'interfaccia **IEnumMedia** fornisce metodi di enumerazione standard com per l'interfaccia [**ITmedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="63a33-107">The **IEnumMedia** interface provides COM-standard enumeration methods for the [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="63a33-108">Il metodo [**ITMediaCollection:: Get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) restituisce un puntatore a **IEnumMedia**.</span><span class="sxs-lookup"><span data-stu-id="63a33-108">The [**ITMediaCollection::get\_EnumerationIf**](itmediacollection-get-enumerationif.md) method returns a pointer to **IEnumMedia**.</span></span>

## <a name="members"></a><span data-ttu-id="63a33-109">Membri</span><span class="sxs-lookup"><span data-stu-id="63a33-109">Members</span></span>

<span data-ttu-id="63a33-110">L'interfaccia **IEnumMedia** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="63a33-110">The **IEnumMedia** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="63a33-111">**IEnumMedia** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="63a33-111">**IEnumMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="63a33-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="63a33-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="63a33-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="63a33-113">Methods</span></span>

<span data-ttu-id="63a33-114">L'interfaccia **IEnumMedia** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="63a33-114">The **IEnumMedia** interface has these methods.</span></span>



| <span data-ttu-id="63a33-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="63a33-115">Method</span></span>                            | <span data-ttu-id="63a33-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63a33-116">Description</span></span>                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63a33-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="63a33-117">**Clone**</span></span>](ienummedia-clone.md) | <span data-ttu-id="63a33-118">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="63a33-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="63a33-119">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="63a33-119">**Next**</span></span>](ienummedia-next.md)   | <span data-ttu-id="63a33-120">Ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="63a33-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="63a33-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="63a33-121">**Reset**</span></span>](ienummedia-reset.md) | <span data-ttu-id="63a33-122">Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="63a33-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="63a33-123">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="63a33-123">**Skip**</span></span>](ienummedia-skip.md)   | <span data-ttu-id="63a33-124">Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="63a33-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="63a33-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63a33-125">Requirements</span></span>



| <span data-ttu-id="63a33-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="63a33-126">Requirement</span></span> | <span data-ttu-id="63a33-127">Valore</span><span class="sxs-lookup"><span data-stu-id="63a33-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63a33-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="63a33-128">TAPI version</span></span><br/> | <span data-ttu-id="63a33-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="63a33-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="63a33-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63a33-130">Header</span></span><br/>       | <dl> <span data-ttu-id="63a33-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="63a33-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="63a33-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="63a33-132">Library</span></span><br/>      | <dl> <span data-ttu-id="63a33-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63a33-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="63a33-134">DLL</span><span class="sxs-lookup"><span data-stu-id="63a33-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="63a33-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63a33-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

