---
description: L'interfaccia ITMediaCollection consente di accedere al set di informazioni sui supporti in una descrizione della conferenza SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interfaccia ITMediaCollection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324238"
---
# <a name="itmediacollection-interface"></a><span data-ttu-id="6a97f-103">Interfaccia ITMediaCollection</span><span class="sxs-lookup"><span data-stu-id="6a97f-103">ITMediaCollection interface</span></span>

<span data-ttu-id="6a97f-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6a97f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6a97f-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="6a97f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6a97f-106">L'interfaccia **ITMediaCollection** consente di accedere al set di informazioni sui supporti in una descrizione della conferenza SDP (RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="6a97f-106">The **ITMediaCollection** interface provides access to the set of media information in an SDP (RFC 2327) conference description.</span></span> <span data-ttu-id="6a97f-107">Ogni descrizione del supporto in SDP è descritta da un'interfaccia [**ITmedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="6a97f-107">Each Media description in the SDP is described by an [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="6a97f-108">**ITMediaCollection** consente la manipolazione del set di informazioni **ITMEDIA** per il SDP, tra cui:</span><span class="sxs-lookup"><span data-stu-id="6a97f-108">**ITMediaCollection** allows manipulation of the set of **ITMedia** information for the SDP, including:</span></span>

-   <span data-ttu-id="6a97f-109">Consente l'accesso ai file multimediali in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="6a97f-109">Allows media access by index.</span></span>
-   <span data-ttu-id="6a97f-110">Consente la creazione e l'eliminazione di supporti.</span><span class="sxs-lookup"><span data-stu-id="6a97f-110">Enables creation and deletion of media.</span></span>

<span data-ttu-id="6a97f-111">Il metodo [**ITSdp:: Get \_ mediacollection**](itsdp-get-mediacollection.md) crea l'interfaccia **ITMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="6a97f-111">The [**ITSdp::get\_MediaCollection**](itsdp-get-mediacollection.md) method creates the **ITMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="6a97f-112">Membri</span><span class="sxs-lookup"><span data-stu-id="6a97f-112">Members</span></span>

<span data-ttu-id="6a97f-113">L'interfaccia **ITMediaCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="6a97f-113">The **ITMediaCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6a97f-114">**ITMediaCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6a97f-114">**ITMediaCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="6a97f-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="6a97f-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a97f-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="6a97f-116">Methods</span></span>

<span data-ttu-id="6a97f-117">L'interfaccia **ITMediaCollection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6a97f-117">The **ITMediaCollection** interface has these methods.</span></span>



| <span data-ttu-id="6a97f-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="6a97f-118">Method</span></span>                                                            | <span data-ttu-id="6a97f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a97f-119">Description</span></span>                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="6a97f-120">**Creare**</span><span class="sxs-lookup"><span data-stu-id="6a97f-120">**Create**</span></span>](itmediacollection-create.md)                        | <span data-ttu-id="6a97f-121">Crea un nuovo supporto con le proprietà predefinite e lo restituisce.</span><span class="sxs-lookup"><span data-stu-id="6a97f-121">Creates a new media with default properties and returns it.</span></span><br/> |
| [<span data-ttu-id="6a97f-122">**Delete**</span><span class="sxs-lookup"><span data-stu-id="6a97f-122">**Delete**</span></span>](itmediacollection-delete.md)                        | <span data-ttu-id="6a97f-123">Elimina i supporti corrispondenti all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="6a97f-123">Deletes the media corresponding to the specified index.</span></span><br/>     |
| [<span data-ttu-id="6a97f-124">**ottenere \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="6a97f-124">**get\_\_NewEnum**</span></span>](itmediacollection-get--newenum.md)          | <span data-ttu-id="6a97f-125">Restituisce un enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="6a97f-125">Returns an enumerator for the collection.</span></span><br/>                   |
| [<span data-ttu-id="6a97f-126">**Ottieni \_ conteggio**</span><span class="sxs-lookup"><span data-stu-id="6a97f-126">**get\_Count**</span></span>](itmediacollection-get-count.md)                 | <span data-ttu-id="6a97f-127">Ottiene il numero di supporti nella sessione.</span><span class="sxs-lookup"><span data-stu-id="6a97f-127">Gets the number of media in the session.</span></span><br/>                    |
| [<span data-ttu-id="6a97f-128">**ottenere \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="6a97f-128">**get\_EnumerationIf**</span></span>](itmediacollection-get-enumerationif.md) | <span data-ttu-id="6a97f-129">Ottiene il puntatore all'interfaccia di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="6a97f-129">Gets pointer to enumeration interface.</span></span><br/>                      |
| [<span data-ttu-id="6a97f-130">**Ottieni \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="6a97f-130">**get\_Item**</span></span>](itmediacollection-get-item.md)                   | <span data-ttu-id="6a97f-131">Restituisce il supporto corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="6a97f-131">Returns the media corresponding to the specified index.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="6a97f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a97f-132">Requirements</span></span>



| <span data-ttu-id="6a97f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a97f-133">Requirement</span></span> | <span data-ttu-id="6a97f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="6a97f-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a97f-135">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="6a97f-135">TAPI version</span></span><br/> | <span data-ttu-id="6a97f-136">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6a97f-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6a97f-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a97f-137">Header</span></span><br/>       | <dl> <span data-ttu-id="6a97f-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a97f-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a97f-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a97f-139">Library</span></span><br/>      | <dl> <span data-ttu-id="6a97f-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a97f-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6a97f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6a97f-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="6a97f-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a97f-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

