---
description: "L'interfaccia IEnumTime fornisce metodi di enumerazione standard COM per l'interfaccia ITTime. Il metodo ITTimeCollection:: Get \\_ EnumerationIf restituisce un puntatore a IEnumTime."
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interfaccia IEnumTime (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328734"
---
# <a name="ienumtime-interface"></a><span data-ttu-id="935f6-104">Interfaccia IEnumTime</span><span class="sxs-lookup"><span data-stu-id="935f6-104">IEnumTime interface</span></span>

<span data-ttu-id="935f6-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="935f6-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="935f6-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="935f6-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="935f6-107">L'interfaccia **IEnumTime** fornisce metodi di enumerazione standard com per l'interfaccia [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="935f6-107">The **IEnumTime** interface provides COM-standard enumeration methods for the [**ITTime**](ittime.md) interface.</span></span> <span data-ttu-id="935f6-108">Il metodo [**ITTimeCollection:: Get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) restituisce un puntatore a **IEnumTime**.</span><span class="sxs-lookup"><span data-stu-id="935f6-108">The [**ITTimeCollection::get\_EnumerationIf**](ittimecollection-get-enumerationif.md) method returns a pointer to **IEnumTime**.</span></span>

## <a name="members"></a><span data-ttu-id="935f6-109">Membri</span><span class="sxs-lookup"><span data-stu-id="935f6-109">Members</span></span>

<span data-ttu-id="935f6-110">L'interfaccia **IEnumTime** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="935f6-110">The **IEnumTime** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="935f6-111">**IEnumTime** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="935f6-111">**IEnumTime** also has these types of members:</span></span>

-   [<span data-ttu-id="935f6-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="935f6-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="935f6-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="935f6-113">Methods</span></span>

<span data-ttu-id="935f6-114">L'interfaccia **IEnumTime** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="935f6-114">The **IEnumTime** interface has these methods.</span></span>



| <span data-ttu-id="935f6-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="935f6-115">Method</span></span>                           | <span data-ttu-id="935f6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="935f6-116">Description</span></span>                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="935f6-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="935f6-117">**Clone**</span></span>](ienumtime-clone.md) | <span data-ttu-id="935f6-118">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="935f6-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="935f6-119">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="935f6-119">**Next**</span></span>](ienumtime-next.md)   | <span data-ttu-id="935f6-120">Ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="935f6-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="935f6-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="935f6-121">**Reset**</span></span>](ienumtime-reset.md) | <span data-ttu-id="935f6-122">Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="935f6-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="935f6-123">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="935f6-123">**Skip**</span></span>](ienumtime-skip.md)   | <span data-ttu-id="935f6-124">Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="935f6-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="935f6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="935f6-125">Requirements</span></span>



| <span data-ttu-id="935f6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="935f6-126">Requirement</span></span> | <span data-ttu-id="935f6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="935f6-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="935f6-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="935f6-128">TAPI version</span></span><br/> | <span data-ttu-id="935f6-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="935f6-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="935f6-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="935f6-130">Header</span></span><br/>       | <dl> <span data-ttu-id="935f6-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="935f6-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="935f6-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="935f6-132">Library</span></span><br/>      | <dl> <span data-ttu-id="935f6-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="935f6-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="935f6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="935f6-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="935f6-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="935f6-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

