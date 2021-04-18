---
description: L'interfaccia IDelaydC fornisce i metodi usati per connettersi alla rete, acquisire il traffico di rete in un file di acquisizione, recuperare le statistiche e disconnettersi dalla rete.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interfaccia IDelaydC (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308660"
---
# <a name="idelaydc-interface"></a><span data-ttu-id="01bab-103">Interfaccia IDelaydC</span><span class="sxs-lookup"><span data-stu-id="01bab-103">IDelaydC interface</span></span>

<span data-ttu-id="01bab-104">L'interfaccia **IDelaydC** fornisce i metodi usati per connettersi alla rete, acquisire il traffico di rete in un file di acquisizione, recuperare le statistiche e disconnettersi dalla rete.</span><span class="sxs-lookup"><span data-stu-id="01bab-104">The **IDelaydC** interface provides the methods used to connect to the network, capture network traffic to a capture file, retrieve statistics, and disconnect from the network.</span></span>

<span data-ttu-id="01bab-105">Questa interfaccia acquisisce i frame dal flusso di dati di rete e quindi copia i frame in un file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="01bab-105">This interface captures frames from the network data stream and then copies the frames to a capture file.</span></span> <span data-ttu-id="01bab-106">Questa interfaccia viene utilizzata dalle applicazioni Network Monitor e NPP.</span><span class="sxs-lookup"><span data-stu-id="01bab-106">This interface is used by Network Monitor and NPP applications.</span></span> <span data-ttu-id="01bab-107">Per ricevere i dati di rete, la scheda di interfaccia di rete di destinazione deve supportare la modalità promiscua.</span><span class="sxs-lookup"><span data-stu-id="01bab-107">To receive the network data, the targeted NIC must support promiscuous mode.</span></span>

## <a name="members"></a><span data-ttu-id="01bab-108">Membri</span><span class="sxs-lookup"><span data-stu-id="01bab-108">Members</span></span>

<span data-ttu-id="01bab-109">L'interfaccia **IDelaydC** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="01bab-109">The **IDelaydC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01bab-110">**IDelaydC** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="01bab-110">**IDelaydC** also has these types of members:</span></span>

-   [<span data-ttu-id="01bab-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="01bab-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="01bab-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="01bab-112">Methods</span></span>

<span data-ttu-id="01bab-113">L'interfaccia **IDelaydC** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="01bab-113">The **IDelaydC** interface has these methods.</span></span>



| <span data-ttu-id="01bab-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="01bab-114">Method</span></span>                                                                  | <span data-ttu-id="01bab-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01bab-115">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01bab-116">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="01bab-116">**Configure**</span></span>](idelaydc-configure.md)                                 | <span data-ttu-id="01bab-117">Invia le informazioni di configurazione usate per un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="01bab-117">Submits configuration information used for a capture.</span></span><br/>                                                                                        |
| [<span data-ttu-id="01bab-118">**Connettersi**</span><span class="sxs-lookup"><span data-stu-id="01bab-118">**Connect**</span></span>](idelaydc-connect.md)                                     | <span data-ttu-id="01bab-119">Connette l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="01bab-119">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="01bab-120">**Disconnetti**</span><span class="sxs-lookup"><span data-stu-id="01bab-120">**Disconnect**</span></span>](idelaydc-disconnect.md)                               | <span data-ttu-id="01bab-121">Disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="01bab-121">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="01bab-122">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="01bab-122">**GetControlState**</span></span>](idelaydc-getcontrolstate.md)                     | <span data-ttu-id="01bab-123">Recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.</span><span class="sxs-lookup"><span data-stu-id="01bab-123">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="01bab-124">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="01bab-124">**GetConversationStatistics**</span></span>](idelaydc-getconversationstatistics.md) | <span data-ttu-id="01bab-125">Recupera le informazioni sulla [*sessione*](s.md) e [*sulla stazione*](s.md) per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="01bab-125">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="01bab-126">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="01bab-126">**GetTotalStatistics**</span></span>](idelaydc-gettotalstatistics.md)               | <span data-ttu-id="01bab-127">Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="01bab-127">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="01bab-128">**Sospendere**</span><span class="sxs-lookup"><span data-stu-id="01bab-128">**Pause**</span></span>](idelaydc-pause.md)                                         | <span data-ttu-id="01bab-129">Interrompe temporaneamente l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="01bab-129">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="01bab-130">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="01bab-130">**QueryStations**</span></span>](idelaydc-querystations.md)                         | <span data-ttu-id="01bab-131">Recupera un elenco di tutti i computer che utilizzano Network Monitor per acquisire i dati in una subnet.</span><span class="sxs-lookup"><span data-stu-id="01bab-131">Retrieves a list of all computers that use Network Monitor to capture data on a subnet.</span></span><br/>                                                      |
| [<span data-ttu-id="01bab-132">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="01bab-132">**QueryStatus**</span></span>](idelaydc-querystatus.md)                             | <span data-ttu-id="01bab-133">Recupera lo stato dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="01bab-133">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="01bab-134">**Riprendi**</span><span class="sxs-lookup"><span data-stu-id="01bab-134">**Resume**</span></span>](idelaydc-resume.md)                                       | <span data-ttu-id="01bab-135">Riprende un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="01bab-135">Resumes a paused capture.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="01bab-136">**Avvio**</span><span class="sxs-lookup"><span data-stu-id="01bab-136">**Start**</span></span>](idelaydc-start.md)                                         | <span data-ttu-id="01bab-137">Avvia un'acquisizione e crea il [*file di acquisizione*](c.md).</span><span class="sxs-lookup"><span data-stu-id="01bab-137">Starts a capture and creates the [*capture file*](c.md).</span></span><br/>                                                           |
| [<span data-ttu-id="01bab-138">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="01bab-138">**Stop**</span></span>](idelaydc-stop.md)                                           | <span data-ttu-id="01bab-139">Arresta l'acquisizione corrente e chiude il [*file di acquisizione*](c.md).</span><span class="sxs-lookup"><span data-stu-id="01bab-139">Stops the current capture and closes the [*capture file*](c.md).</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="01bab-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01bab-140">Requirements</span></span>



| <span data-ttu-id="01bab-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="01bab-141">Requirement</span></span> | <span data-ttu-id="01bab-142">Valore</span><span class="sxs-lookup"><span data-stu-id="01bab-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01bab-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01bab-143">Minimum supported client</span></span><br/> | <span data-ttu-id="01bab-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01bab-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="01bab-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01bab-145">Minimum supported server</span></span><br/> | <span data-ttu-id="01bab-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01bab-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="01bab-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01bab-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="01bab-148"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="01bab-148"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="01bab-149">DLL</span><span class="sxs-lookup"><span data-stu-id="01bab-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01bab-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01bab-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

