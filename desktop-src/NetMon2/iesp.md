---
description: L'interfaccia IESP fornisce i metodi che connettono l'oggetto NPP alla rete, acquisisce il traffico di rete in un file di acquisizione, recupera le statistiche e disconnette l'oggetto NPP dalla rete.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interfaccia IESP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128918"
---
# <a name="iesp-interface"></a><span data-ttu-id="ea771-103">Interfaccia IESP</span><span class="sxs-lookup"><span data-stu-id="ea771-103">IESP interface</span></span>

<span data-ttu-id="ea771-104">L'interfaccia **IESP** fornisce i metodi che connettono l'oggetto NPP alla rete, acquisisce il traffico di rete in un file di acquisizione, recupera le statistiche e disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="ea771-104">The **IESP** interface provides the methods that connect the NPP to the network, capture network traffic to a capture file, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="ea771-105">Questa interfaccia viene utilizzata principalmente quando è necessario raccogliere le [*statistiche delle conversazioni*](c.md) di rete in un formato di file ESP proprietario.</span><span class="sxs-lookup"><span data-stu-id="ea771-105">This interface is used primarily when you need to collect network [*conversation statistics*](c.md) in a proprietary ESP file format.</span></span>

## <a name="members"></a><span data-ttu-id="ea771-106">Membri</span><span class="sxs-lookup"><span data-stu-id="ea771-106">Members</span></span>

<span data-ttu-id="ea771-107">L'interfaccia **IESP** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ea771-107">The **IESP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ea771-108">**IESP** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ea771-108">**IESP** also has these types of members:</span></span>

-   [<span data-ttu-id="ea771-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ea771-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ea771-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ea771-110">Methods</span></span>

<span data-ttu-id="ea771-111">L'interfaccia **IESP** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ea771-111">The **IESP** interface has these methods.</span></span>



| <span data-ttu-id="ea771-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="ea771-112">Method</span></span>                                          | <span data-ttu-id="ea771-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea771-113">Description</span></span>                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea771-114">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="ea771-114">**Configure**</span></span>](iesp-configure.md)             | <span data-ttu-id="ea771-115">Invia le informazioni di configurazione per un'acquisizione</span><span class="sxs-lookup"><span data-stu-id="ea771-115">Submits configuration information for a capture</span></span><br/>                                                                         |
| [<span data-ttu-id="ea771-116">**Connettersi**</span><span class="sxs-lookup"><span data-stu-id="ea771-116">**Connect**</span></span>](iesp-connect.md)                 | <span data-ttu-id="ea771-117">Connette l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="ea771-117">Connects the NPP to the network.</span></span><br/>                                                                                        |
| [<span data-ttu-id="ea771-118">**Disconnetti**</span><span class="sxs-lookup"><span data-stu-id="ea771-118">**Disconnect**</span></span>](iesp-disconnect.md)           | <span data-ttu-id="ea771-119">Disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="ea771-119">Disconnects the NPP from the network.</span></span><br/>                                                                                   |
| [<span data-ttu-id="ea771-120">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="ea771-120">**GetControlState**</span></span>](iesp-getcontrolstate.md) | <span data-ttu-id="ea771-121">Recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.</span><span class="sxs-lookup"><span data-stu-id="ea771-121">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/> |
| [<span data-ttu-id="ea771-122">**Sospendere**</span><span class="sxs-lookup"><span data-stu-id="ea771-122">**Pause**</span></span>](iesp-pause.md)                     | <span data-ttu-id="ea771-123">Interrompe temporaneamente l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="ea771-123">Temporarily stops the current capture.</span></span><br/>                                                                                  |
| [<span data-ttu-id="ea771-124">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="ea771-124">**QueryStations**</span></span>](iesp-querystations.md)     | <span data-ttu-id="ea771-125">Recupera un elenco di tutti i computer che utilizzano Network Monitor per acquisire i dati in una subnet.</span><span class="sxs-lookup"><span data-stu-id="ea771-125">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                           |
| [<span data-ttu-id="ea771-126">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="ea771-126">**QueryStatus**</span></span>](iesp-querystatus.md)         | <span data-ttu-id="ea771-127">Recupera lo stato dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="ea771-127">Retrieves the status of the NPP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="ea771-128">**Riprendi**</span><span class="sxs-lookup"><span data-stu-id="ea771-128">**Resume**</span></span>](iesp-resume.md)                   | <span data-ttu-id="ea771-129">Riprende un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="ea771-129">Resumes a paused capture.</span></span><br/>                                                                                               |
| [<span data-ttu-id="ea771-130">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="ea771-130">**Start**</span></span>](iesp-start.md)                     | <span data-ttu-id="ea771-131">Avvia l'acquisizione e crea il file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="ea771-131">Starts the capture and creates the capture file.</span></span><br/>                                                                        |
| [<span data-ttu-id="ea771-132">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="ea771-132">**Stop**</span></span>](iesp-stop.md)                       | <span data-ttu-id="ea771-133">Arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="ea771-133">Stops the current capture.</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="ea771-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea771-134">Requirements</span></span>



| <span data-ttu-id="ea771-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea771-135">Requirement</span></span> | <span data-ttu-id="ea771-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ea771-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea771-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea771-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ea771-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea771-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ea771-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea771-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ea771-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea771-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ea771-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea771-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea771-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea771-142"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ea771-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ea771-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea771-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea771-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

