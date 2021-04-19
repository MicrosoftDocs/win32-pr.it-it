---
description: L'interfaccia IStats fornisce i metodi usati per connettere un NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere l'oggetto NPP dalla rete. Questa interfaccia genera statistiche senza frame.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interfaccia IStats (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308167"
---
# <a name="istats-interface"></a><span data-ttu-id="98ac0-104">Interfaccia IStats</span><span class="sxs-lookup"><span data-stu-id="98ac0-104">IStats interface</span></span>

<span data-ttu-id="98ac0-105">L'interfaccia **IStats** fornisce i metodi usati per connettere un NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="98ac0-105">The **IStats** interface provides the methods you use to connect an NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="98ac0-106">Questa interfaccia genera statistiche senza frame.</span><span class="sxs-lookup"><span data-stu-id="98ac0-106">This interface generates statistics without frames.</span></span>

## <a name="members"></a><span data-ttu-id="98ac0-107">Membri</span><span class="sxs-lookup"><span data-stu-id="98ac0-107">Members</span></span>

<span data-ttu-id="98ac0-108">L'interfaccia **IStats** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="98ac0-108">The **IStats** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="98ac0-109">Gli **Istat** hanno anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="98ac0-109">**IStats** also has these types of members:</span></span>

-   [<span data-ttu-id="98ac0-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="98ac0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="98ac0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="98ac0-111">Methods</span></span>

<span data-ttu-id="98ac0-112">L'interfaccia **IStats** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="98ac0-112">The **IStats** interface has these methods.</span></span>



| <span data-ttu-id="98ac0-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="98ac0-113">Method</span></span>                                                                | <span data-ttu-id="98ac0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98ac0-114">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98ac0-115">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="98ac0-115">**Configure**</span></span>](istats-configure.md)                                 | <span data-ttu-id="98ac0-116">Configura il trigger, la corrispondenza dei criteri e le dimensioni del buffer del file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="98ac0-116">Configures the trigger, pattern match, and buffer size of the capture file.</span></span><br/>                                                                    |
| [<span data-ttu-id="98ac0-117">**Connettersi**</span><span class="sxs-lookup"><span data-stu-id="98ac0-117">**Connect**</span></span>](istats-connect.md)                                     | <span data-ttu-id="98ac0-118">Connette l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="98ac0-118">Connects the NPP to the network.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="98ac0-119">**Disconnetti**</span><span class="sxs-lookup"><span data-stu-id="98ac0-119">**Disconnect**</span></span>](istats-disconnect.md)                               | <span data-ttu-id="98ac0-120">Disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="98ac0-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="98ac0-121">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="98ac0-121">**GetControlState**</span></span>](istats-getcontrolstate.md)                     | <span data-ttu-id="98ac0-122">Recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.</span><span class="sxs-lookup"><span data-stu-id="98ac0-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                        |
| [<span data-ttu-id="98ac0-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="98ac0-123">**GetConversationStatistics**</span></span>](istats-getconversationstatistics.md) | <span data-ttu-id="98ac0-124">Recupera le informazioni sulla [*sessione*](s.md) e sulla [*stazione*](s.md) relative all'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="98ac0-124">Retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span><br/> |
| [<span data-ttu-id="98ac0-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="98ac0-125">**GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)               | <span data-ttu-id="98ac0-126">Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="98ac0-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                                |
| [<span data-ttu-id="98ac0-127">**Sospendere**</span><span class="sxs-lookup"><span data-stu-id="98ac0-127">**Pause**</span></span>](istats-pause.md)                                         | <span data-ttu-id="98ac0-128">Interrompe temporaneamente l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="98ac0-128">Temporarily stops the current capture.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="98ac0-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="98ac0-129">**QueryStations**</span></span>](istats-querystations.md)                         | <span data-ttu-id="98ac0-130">Recupera un elenco di tutti i computer che utilizzano Network Monitor per acquisire i dati in una subnet.</span><span class="sxs-lookup"><span data-stu-id="98ac0-130">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                                                  |
| [<span data-ttu-id="98ac0-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="98ac0-131">**QueryStatus**</span></span>](istats-querystatus.md)                             | <span data-ttu-id="98ac0-132">Recupera lo stato dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="98ac0-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="98ac0-133">**Riprendi**</span><span class="sxs-lookup"><span data-stu-id="98ac0-133">**Resume**</span></span>](istats-resume.md)                                       | <span data-ttu-id="98ac0-134">Riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="98ac0-134">Restarts a paused capture.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="98ac0-135">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="98ac0-135">**Start**</span></span>](istats-start.md)                                         | <span data-ttu-id="98ac0-136">Avvia l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="98ac0-136">Starts the capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="98ac0-137">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="98ac0-137">**Stop**</span></span>](istats-stop.md)                                           | <span data-ttu-id="98ac0-138">Arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="98ac0-138">Stops the current capture.</span></span><br/>                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="98ac0-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98ac0-139">Requirements</span></span>



| <span data-ttu-id="98ac0-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="98ac0-140">Requirement</span></span> | <span data-ttu-id="98ac0-141">Valore</span><span class="sxs-lookup"><span data-stu-id="98ac0-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ac0-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98ac0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="98ac0-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98ac0-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="98ac0-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98ac0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="98ac0-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98ac0-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="98ac0-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98ac0-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="98ac0-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="98ac0-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="98ac0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="98ac0-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98ac0-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98ac0-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

