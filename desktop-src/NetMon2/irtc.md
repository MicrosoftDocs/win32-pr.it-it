---
description: L'interfaccia IRTC fornisce i metodi usati per connettere l'oggetto NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere l'oggetto NPP dalla rete.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interfaccia IRTC (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967136"
---
# <a name="irtc-interface"></a><span data-ttu-id="032bd-103">Interfaccia IRTC</span><span class="sxs-lookup"><span data-stu-id="032bd-103">IRTC interface</span></span>

<span data-ttu-id="032bd-104">L'interfaccia **IRTC** fornisce i metodi usati per connettere l'oggetto NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="032bd-104">The **IRTC** interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="032bd-105">**IRTC** ottiene un'interfaccia per i punti di ingresso solo locali, necessari per attivare l'acquisizione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="032bd-105">**IRTC** gets an interface to local-only entry points, which are necessary to engage in real-time capture.</span></span> <span data-ttu-id="032bd-106">Questa interfaccia include un metodo che invia un callback a NPP.</span><span class="sxs-lookup"><span data-stu-id="032bd-106">This interface includes a method that hands off a callback to the NPP.</span></span>

## <a name="members"></a><span data-ttu-id="032bd-107">Membri</span><span class="sxs-lookup"><span data-stu-id="032bd-107">Members</span></span>

<span data-ttu-id="032bd-108">L'interfaccia **IRTC** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="032bd-108">The **IRTC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="032bd-109">**IRTC** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="032bd-109">**IRTC** also has these types of members:</span></span>

-   [<span data-ttu-id="032bd-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="032bd-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="032bd-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="032bd-111">Methods</span></span>

<span data-ttu-id="032bd-112">L'interfaccia **IRTC** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="032bd-112">The **IRTC** interface has these methods.</span></span>



| <span data-ttu-id="032bd-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="032bd-113">Method</span></span>                                                              | <span data-ttu-id="032bd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="032bd-114">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="032bd-115">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="032bd-115">**Configure**</span></span>](irtc-configure.md)                                 | <span data-ttu-id="032bd-116">Imposta il trigger, la corrispondenza dei criteri e le dimensioni del buffer dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="032bd-116">Sets the trigger, pattern match, and buffer size of the capture.</span></span><br/>                                                                             |
| [<span data-ttu-id="032bd-117">**Connettersi**</span><span class="sxs-lookup"><span data-stu-id="032bd-117">**Connect**</span></span>](irtc-connect.md)                                     | <span data-ttu-id="032bd-118">Connette l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="032bd-118">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="032bd-119">**Disconnetti**</span><span class="sxs-lookup"><span data-stu-id="032bd-119">**Disconnect**</span></span>](irtc-disconnect.md)                               | <span data-ttu-id="032bd-120">Disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="032bd-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="032bd-121">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="032bd-121">**GetControlState**</span></span>](irtc-getcontrolstate.md)                     | <span data-ttu-id="032bd-122">Recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.</span><span class="sxs-lookup"><span data-stu-id="032bd-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="032bd-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="032bd-123">**GetConversationStatistics**</span></span>](irtc-getconversationstatistics.md) | <span data-ttu-id="032bd-124">Recupera le informazioni sulla [*sessione*](s.md) e [*sulla stazione*](s.md) per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="032bd-124">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="032bd-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="032bd-125">**GetTotalStatistics**</span></span>](irtc-gettotalstatistics.md)               | <span data-ttu-id="032bd-126">Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="032bd-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="032bd-127">**Sospendere**</span><span class="sxs-lookup"><span data-stu-id="032bd-127">**Pause**</span></span>](irtc-pause.md)                                         | <span data-ttu-id="032bd-128">Interrompe temporaneamente l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="032bd-128">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="032bd-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="032bd-129">**QueryStations**</span></span>](irtc-querystations.md)                         | <span data-ttu-id="032bd-130">Recupera un elenco di tutti i computer in una subnet che utilizzano Network Monitor per acquisire i dati di rete.</span><span class="sxs-lookup"><span data-stu-id="032bd-130">Retrieves a list of all computers on a subnet that are using Network Monitor to capture network data.</span></span><br/>                                        |
| [<span data-ttu-id="032bd-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="032bd-131">**QueryStatus**</span></span>](irtc-querystatus.md)                             | <span data-ttu-id="032bd-132">Recupera lo stato dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="032bd-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="032bd-133">**Riprendi**</span><span class="sxs-lookup"><span data-stu-id="032bd-133">**Resume**</span></span>](irtc-resume.md)                                       | <span data-ttu-id="032bd-134">Riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="032bd-134">Restarts a paused capture.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="032bd-135">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="032bd-135">**Start**</span></span>](irtc-start.md)                                         | <span data-ttu-id="032bd-136">Avvia un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="032bd-136">Starts a capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="032bd-137">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="032bd-137">**Stop**</span></span>](irtc-stop.md)                                           | <span data-ttu-id="032bd-138">Arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="032bd-138">Stops the current capture.</span></span><br/>                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="032bd-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="032bd-139">Requirements</span></span>



| <span data-ttu-id="032bd-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="032bd-140">Requirement</span></span> | <span data-ttu-id="032bd-141">Valore</span><span class="sxs-lookup"><span data-stu-id="032bd-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="032bd-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="032bd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="032bd-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="032bd-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="032bd-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="032bd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="032bd-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="032bd-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="032bd-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="032bd-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="032bd-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="032bd-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="032bd-148">DLL</span><span class="sxs-lookup"><span data-stu-id="032bd-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="032bd-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="032bd-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

