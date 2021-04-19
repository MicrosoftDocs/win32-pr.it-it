---
description: L'interfaccia ITMedia è una rappresentazione di supporti in un protocollo SDP (Session Descriptor Protocol), vedere RFC 2327.
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interfaccia ITMedia (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329447"
---
# <a name="itmedia-interface"></a><span data-ttu-id="64fff-103">Interfaccia ITMedia</span><span class="sxs-lookup"><span data-stu-id="64fff-103">ITMedia interface</span></span>

<span data-ttu-id="64fff-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="64fff-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="64fff-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="64fff-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="64fff-106">L'interfaccia **ITmedia** è una rappresentazione di supporti in un protocollo SDP (Session Descriptor Protocol), vedere RFC 2327.</span><span class="sxs-lookup"><span data-stu-id="64fff-106">The **ITMedia** interface is a representation of media in a Session Descriptor Protocol (SDP, see RFC 2327).</span></span> <span data-ttu-id="64fff-107">Questa interfaccia Esporta i metodi per ottenere e impostare le proprietà dei supporti di base, ad esempio Type.</span><span class="sxs-lookup"><span data-stu-id="64fff-107">This interface exports methods to get and set basic media properties, such as type.</span></span> <span data-ttu-id="64fff-108">I metodi [**ITMediaCollection:: Get \_ Item**](itmediacollection-get-item.md) e [**ITMediaCollection:: create**](itmediacollection-create.md) creano l'interfaccia **ITmedia** .</span><span class="sxs-lookup"><span data-stu-id="64fff-108">The [**ITMediaCollection::get\_Item**](itmediacollection-get-item.md) and [**ITMediaCollection::Create**](itmediacollection-create.md) methods create the **ITMedia** interface.</span></span>

## <a name="members"></a><span data-ttu-id="64fff-109">Membri</span><span class="sxs-lookup"><span data-stu-id="64fff-109">Members</span></span>

<span data-ttu-id="64fff-110">L'interfaccia **ITmedia** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="64fff-110">The **ITMedia** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="64fff-111">**ITmedia** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="64fff-111">**ITMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="64fff-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="64fff-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="64fff-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="64fff-113">Methods</span></span>

<span data-ttu-id="64fff-114">L'interfaccia **ITmedia** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="64fff-114">The **ITMedia** interface has these methods.</span></span>



| <span data-ttu-id="64fff-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="64fff-115">Method</span></span>                                                          | <span data-ttu-id="64fff-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64fff-116">Description</span></span>                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64fff-117">**ottenere \_ codiciformato**</span><span class="sxs-lookup"><span data-stu-id="64fff-117">**get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)             | <span data-ttu-id="64fff-118">Ottiene l'elenco dei codici di formato del payload multimediale.</span><span class="sxs-lookup"><span data-stu-id="64fff-118">Gets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="64fff-119">**ottenere \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="64fff-119">**get\_MediaName**</span></span>](itmedia-get-medianame.md)                 | <span data-ttu-id="64fff-120">Ottiene il nome del supporto.</span><span class="sxs-lookup"><span data-stu-id="64fff-120">Gets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="64fff-121">**ottenere \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="64fff-121">**get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)               | <span data-ttu-id="64fff-122">Ottiene il titolo del supporto.</span><span class="sxs-lookup"><span data-stu-id="64fff-122">Gets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="64fff-123">**ottenere \_ NumPorts**</span><span class="sxs-lookup"><span data-stu-id="64fff-123">**get\_NumPorts**</span></span>](itmedia-get-numports.md)                   | <span data-ttu-id="64fff-124">Ottiene il numero di porte necessarie per la sessione.</span><span class="sxs-lookup"><span data-stu-id="64fff-124">Gets the number of ports needed for the session.</span></span><br/>                                      |
| [<span data-ttu-id="64fff-125">**ottenere \_ presenta**</span><span class="sxs-lookup"><span data-stu-id="64fff-125">**get\_StartPort**</span></span>](itmedia-get-startport.md)                 | <span data-ttu-id="64fff-126">Ottiene il valore della porta a 16 bit per la prima porta.</span><span class="sxs-lookup"><span data-stu-id="64fff-126">Gets the 16-bit port value for the first port.</span></span><br/>                                        |
| [<span data-ttu-id="64fff-127">**ottenere \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="64fff-127">**get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md) | <span data-ttu-id="64fff-128">Ottiene il protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="64fff-128">Gets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="64fff-129">**Inserisci \_ codiciformato**</span><span class="sxs-lookup"><span data-stu-id="64fff-129">**put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)             | <span data-ttu-id="64fff-130">Imposta l'elenco dei codici di formato del payload multimediale.</span><span class="sxs-lookup"><span data-stu-id="64fff-130">Sets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="64fff-131">**Inserisci \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="64fff-131">**put\_MediaName**</span></span>](itmedia-put-medianame.md)                 | <span data-ttu-id="64fff-132">Imposta il nome del supporto.</span><span class="sxs-lookup"><span data-stu-id="64fff-132">Sets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="64fff-133">**Inserisci \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="64fff-133">**put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)               | <span data-ttu-id="64fff-134">Imposta il titolo del supporto.</span><span class="sxs-lookup"><span data-stu-id="64fff-134">Sets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="64fff-135">**Inserisci \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="64fff-135">**put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md) | <span data-ttu-id="64fff-136">Imposta il protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="64fff-136">Sets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="64fff-137">**SetPortInfo**</span><span class="sxs-lookup"><span data-stu-id="64fff-137">**SetPortInfo**</span></span>](itmedia-setportinfo.md)                      | <span data-ttu-id="64fff-138">Imposta il valore della porta a 16 bit per la prima porta e il numero di porte necessarie per la sessione.</span><span class="sxs-lookup"><span data-stu-id="64fff-138">Sets the 16-bit port value for the first port and number of ports needed for session.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="64fff-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64fff-139">Requirements</span></span>



| <span data-ttu-id="64fff-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="64fff-140">Requirement</span></span> | <span data-ttu-id="64fff-141">Valore</span><span class="sxs-lookup"><span data-stu-id="64fff-141">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64fff-142">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="64fff-142">TAPI version</span></span><br/> | <span data-ttu-id="64fff-143">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="64fff-143">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="64fff-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64fff-144">Header</span></span><br/>       | <dl> <span data-ttu-id="64fff-145"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="64fff-145"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="64fff-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="64fff-146">Library</span></span><br/>      | <dl> <span data-ttu-id="64fff-147"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64fff-147"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="64fff-148">DLL</span><span class="sxs-lookup"><span data-stu-id="64fff-148">DLL</span></span><br/>          | <dl> <span data-ttu-id="64fff-149"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64fff-149"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64fff-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64fff-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64fff-151">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="64fff-151">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="64fff-152">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="64fff-152">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="64fff-153">**ITSDP**</span><span class="sxs-lookup"><span data-stu-id="64fff-153">**ITSDP**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="64fff-154">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="64fff-154">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

