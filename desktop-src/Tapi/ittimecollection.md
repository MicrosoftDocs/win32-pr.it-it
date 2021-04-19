---
description: L'interfaccia ITTimeCollection è un'interfaccia specifica del provider per l'oggetto BLOB della conferenza SDP (Session Descriptor Protocol).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interfaccia ITTimeCollection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326746"
---
# <a name="ittimecollection-interface"></a><span data-ttu-id="3e0dd-103">Interfaccia ITTimeCollection</span><span class="sxs-lookup"><span data-stu-id="3e0dd-103">ITTimeCollection interface</span></span>

<span data-ttu-id="3e0dd-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3e0dd-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3e0dd-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="3e0dd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3e0dd-106">L'interfaccia **ITTimeCollection** è un'interfaccia specifica del provider per l'oggetto BLOB della conferenza SDP (Session Descriptor Protocol).</span><span class="sxs-lookup"><span data-stu-id="3e0dd-106">The **ITTimeCollection** interface is a provider-specific interface for the Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="3e0dd-107">Questa interfaccia consente l'accesso alle interfacce [**ITTime**](ittime.md) in base all'indice e consente inoltre la creazione e l'eliminazione di componenti temporali.</span><span class="sxs-lookup"><span data-stu-id="3e0dd-107">This interface allows access to [**ITTime**](ittime.md) interfaces by index, and also enable the creation and deletion of time components.</span></span> <span data-ttu-id="3e0dd-108">Il metodo [**ITSdp:: Get \_ TimeCollection**](itsdp-get-timecollection.md) crea l'interfaccia **ITTimeCollection** .</span><span class="sxs-lookup"><span data-stu-id="3e0dd-108">The [**ITSdp::get\_TimeCollection**](itsdp-get-timecollection.md) method creates the **ITTimeCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="3e0dd-109">Membri</span><span class="sxs-lookup"><span data-stu-id="3e0dd-109">Members</span></span>

<span data-ttu-id="3e0dd-110">L'interfaccia **ITTimeCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3e0dd-110">The **ITTimeCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3e0dd-111">**ITTimeCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3e0dd-111">**ITTimeCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="3e0dd-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="3e0dd-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e0dd-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="3e0dd-113">Methods</span></span>

<span data-ttu-id="3e0dd-114">L'interfaccia **ITTimeCollection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3e0dd-114">The **ITTimeCollection** interface has these methods.</span></span>



| <span data-ttu-id="3e0dd-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="3e0dd-115">Method</span></span>                                                           | <span data-ttu-id="3e0dd-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e0dd-116">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e0dd-117">**Creare**</span><span class="sxs-lookup"><span data-stu-id="3e0dd-117">**Create**</span></span>](ittimecollection-create.md)                        | <span data-ttu-id="3e0dd-118">Crea un componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="3e0dd-118">Creates an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="3e0dd-119">**Delete**</span><span class="sxs-lookup"><span data-stu-id="3e0dd-119">**Delete**</span></span>](ittimecollection-delete.md)                        | <span data-ttu-id="3e0dd-120">Elimina un componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="3e0dd-120">Deletes an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="3e0dd-121">**ottenere \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="3e0dd-121">**get\_\_NewEnum**</span></span>](ittimecollection-get--newenum.md)          | <span data-ttu-id="3e0dd-122">Restituisce un enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e0dd-122">Returns an enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="3e0dd-123">**Ottieni \_ conteggio**</span><span class="sxs-lookup"><span data-stu-id="3e0dd-123">**get\_Count**</span></span>](ittimecollection-get-count.md)                 | <span data-ttu-id="3e0dd-124">Ottiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e0dd-124">Gets number of items in collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="3e0dd-125">**ottenere \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="3e0dd-125">**get\_EnumerationIf**</span></span>](ittimecollection-get-enumerationif.md) | <span data-ttu-id="3e0dd-126">Restituisce l'interfaccia di enumerazione [**IEnumTime**](ienumtime.md) che enumera [**ITTime**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="3e0dd-126">Returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span><br/> |
| [<span data-ttu-id="3e0dd-127">**Ottieni \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="3e0dd-127">**get\_Item**</span></span>](ittimecollection-get-item.md)                   | <span data-ttu-id="3e0dd-128">Dato un indice, restituisce un elemento nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e0dd-128">Given an index, returns an item in the collection.</span></span><br/>                                                         |



 

## <a name="requirements"></a><span data-ttu-id="3e0dd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e0dd-129">Requirements</span></span>



| <span data-ttu-id="3e0dd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e0dd-130">Requirement</span></span> | <span data-ttu-id="3e0dd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3e0dd-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e0dd-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="3e0dd-132">TAPI version</span></span><br/> | <span data-ttu-id="3e0dd-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3e0dd-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3e0dd-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e0dd-134">Header</span></span><br/>       | <dl> <span data-ttu-id="3e0dd-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e0dd-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e0dd-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e0dd-136">Library</span></span><br/>      | <dl> <span data-ttu-id="3e0dd-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e0dd-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3e0dd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3e0dd-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="3e0dd-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e0dd-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

