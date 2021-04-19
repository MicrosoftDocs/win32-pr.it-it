---
description: L'interfaccia ITTime è un'interfaccia specifica del provider per un oggetto BLOB di conferenza SDP (Session Descriptor Protocol).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Interfaccia ITTime (sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326760"
---
# <a name="ittime-interface"></a><span data-ttu-id="16e22-103">Interfaccia ITTime</span><span class="sxs-lookup"><span data-stu-id="16e22-103">ITTime interface</span></span>

<span data-ttu-id="16e22-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="16e22-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="16e22-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="16e22-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="16e22-106">L'interfaccia **ITTime** è un'interfaccia specifica del provider per un oggetto BLOB di conferenza SDP (Session Descriptor Protocol).</span><span class="sxs-lookup"><span data-stu-id="16e22-106">The **ITTime** interface is a provider-specific interface for a Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="16e22-107">Consente di accedere a un set di tempi di attivazione per la sessione.</span><span class="sxs-lookup"><span data-stu-id="16e22-107">It provides access to a set of activation times for the session.</span></span> <span data-ttu-id="16e22-108">I metodi [**IEnumTime:: Next**](ienumtime-next.md) e [**ITTimeCollection:: create**](ittimecollection-create.md) creano l'interfaccia **ITTime** .</span><span class="sxs-lookup"><span data-stu-id="16e22-108">The [**IEnumTime::Next**](ienumtime-next.md) and [**ITTimeCollection::Create**](ittimecollection-create.md) methods create the **ITTime** interface.</span></span>

## <a name="members"></a><span data-ttu-id="16e22-109">Membri</span><span class="sxs-lookup"><span data-stu-id="16e22-109">Members</span></span>

<span data-ttu-id="16e22-110">L'interfaccia **ITTime** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="16e22-110">The **ITTime** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="16e22-111">**ITTime** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="16e22-111">**ITTime** also has these types of members:</span></span>

-   [<span data-ttu-id="16e22-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="16e22-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16e22-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="16e22-113">Methods</span></span>

<span data-ttu-id="16e22-114">L'interfaccia **ITTime** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="16e22-114">The **ITTime** interface has these methods.</span></span>



| <span data-ttu-id="16e22-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="16e22-115">Method</span></span>                                         | <span data-ttu-id="16e22-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16e22-116">Description</span></span>                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="16e22-117">**ottenere \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="16e22-117">**get\_StartTime**</span></span>](ittime-get-starttime.md) | <span data-ttu-id="16e22-118">Ottiene il valore dell'ora di inizio (NTP) a 32 bit (Network Time Protocol).</span><span class="sxs-lookup"><span data-stu-id="16e22-118">Gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span><br/> |
| [<span data-ttu-id="16e22-119">**ottenere \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="16e22-119">**get\_StopTime**</span></span>](ittime-get-stoptime.md)   | <span data-ttu-id="16e22-120">Ottiene il valore dell'ora di fine NTP.</span><span class="sxs-lookup"><span data-stu-id="16e22-120">Gets the NTP ending time value.</span></span><br/>                                  |
| [<span data-ttu-id="16e22-121">**Inserisci \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="16e22-121">**put\_StartTime**</span></span>](ittime-put-starttime.md) | <span data-ttu-id="16e22-122">Imposta il valore dell'ora di inizio NTP a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="16e22-122">Sets the 32-bit NTP starting time value.</span></span><br/>                         |
| [<span data-ttu-id="16e22-123">**Inserisci \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="16e22-123">**put\_StopTime**</span></span>](ittime-put-stoptime.md)   | <span data-ttu-id="16e22-124">Imposta il valore dell'ora di fine NTP.</span><span class="sxs-lookup"><span data-stu-id="16e22-124">Sets the NTP ending time value.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="16e22-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16e22-125">Requirements</span></span>



| <span data-ttu-id="16e22-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e22-126">Requirement</span></span> | <span data-ttu-id="16e22-127">Valore</span><span class="sxs-lookup"><span data-stu-id="16e22-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16e22-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="16e22-128">TAPI version</span></span><br/> | <span data-ttu-id="16e22-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="16e22-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="16e22-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16e22-130">Header</span></span><br/>       | <dl> <span data-ttu-id="16e22-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="16e22-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="16e22-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="16e22-132">Library</span></span><br/>      | <dl> <span data-ttu-id="16e22-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16e22-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="16e22-134">DLL</span><span class="sxs-lookup"><span data-stu-id="16e22-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="16e22-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16e22-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

