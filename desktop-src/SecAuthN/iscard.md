---
description: Consente di aprire e gestire una connessione a una smart card.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interfaccia scheda (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528152"
---
# <a name="iscard-interface"></a><span data-ttu-id="3dff7-103">Interfaccia scheda</span><span class="sxs-lookup"><span data-stu-id="3dff7-103">ISCard interface</span></span>

<span data-ttu-id="3dff7-104">\[L'interfaccia della **scheda** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="3dff7-104">\[The **ISCard** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3dff7-105">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="3dff7-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3dff7-106">L'interfaccia della **scheda** consente di aprire e gestire una connessione a una [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3dff7-106">The **ISCard** interface lets you open and manage a connection to a [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="3dff7-107">Ogni connessione a una scheda richiede una singola istanza corrispondente dell'interfaccia della **scheda** .</span><span class="sxs-lookup"><span data-stu-id="3dff7-107">Each connection to a card requires a single, corresponding instance of the **ISCard** interface.</span></span>

<span data-ttu-id="3dff7-108">Il gestore di [*risorse*](../secgloss/r-gly.md) della smart card deve essere disponibile ogni volta che viene creata un'istanza di una **scheda** .</span><span class="sxs-lookup"><span data-stu-id="3dff7-108">The smart card [*resource manager*](../secgloss/r-gly.md) must be available whenever an instance of **ISCard** is created.</span></span> <span data-ttu-id="3dff7-109">Se il servizio non è disponibile, la creazione dell'interfaccia avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3dff7-109">If this service is unavailable, creation of the interface will fail.</span></span>

<span data-ttu-id="3dff7-110">Nell'esempio seguente viene illustrato un utilizzo tipico dell'interfaccia della **scheda** .</span><span class="sxs-lookup"><span data-stu-id="3dff7-110">The following example shows a typical use of the **ISCard** interface.</span></span> <span data-ttu-id="3dff7-111">L' **interfaccia della scheda viene** utilizzata per connettersi alla smart card, inviare una [*transazione*](../secgloss/t-gly.md)e rilasciare la smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-111">The **ISCard** interface is used to connect to the smart card, submit a [*transaction*](../secgloss/t-gly.md), and release the smart card.</span></span>

<span data-ttu-id="3dff7-112">**Per inviare una transazione a una scheda specifica**</span><span class="sxs-lookup"><span data-stu-id="3dff7-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="3dff7-113">Creare un'interfaccia di **scheda** .</span><span class="sxs-lookup"><span data-stu-id="3dff7-113">Create an **ISCard** interface.</span></span>
2.  <span data-ttu-id="3dff7-114">Connettersi a una smart card specificando un [*lettore*](../secgloss/r-gly.md) di smart card o utilizzando un handle valido precedentemente definito.</span><span class="sxs-lookup"><span data-stu-id="3dff7-114">Attach to a smart card by specifying a smart card [*reader*](../secgloss/r-gly.md) or by using a previously established, valid handle.</span></span>
3.  <span data-ttu-id="3dff7-115">Creare comandi di transazione con [**ISCardCmd**](iscardcmd.md)e interfacce smart card [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="3dff7-115">Create transaction commands with [**ISCardCmd**](iscardcmd.md), and [**ISCardISO7816**](iscardiso7816.md) smart card interfaces.</span></span>
4.  <span data-ttu-id="3dff7-116">Utilizzare **la scheda per** inviare i comandi di transazione per l'elaborazione da parte della smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-116">Use **ISCard** to submit the transaction commands for processing by the smart card.</span></span>
5.  <span data-ttu-id="3dff7-117">Utilizzare **la scheda per** rilasciare la smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-117">Use **ISCard** to release the smart card.</span></span>
6.  <span data-ttu-id="3dff7-118">Rilasciare l'interfaccia di **scheda** .</span><span class="sxs-lookup"><span data-stu-id="3dff7-118">Release the **ISCard** interface.</span></span>

## <a name="members"></a><span data-ttu-id="3dff7-119">Membri</span><span class="sxs-lookup"><span data-stu-id="3dff7-119">Members</span></span>

<span data-ttu-id="3dff7-120">L'interfaccia della **scheda** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3dff7-120">The **ISCard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3dff7-121">La **scheda** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3dff7-121">**ISCard** also has these types of members:</span></span>

-   [<span data-ttu-id="3dff7-122">Metodi</span><span class="sxs-lookup"><span data-stu-id="3dff7-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="3dff7-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3dff7-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3dff7-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="3dff7-124">Methods</span></span>

<span data-ttu-id="3dff7-125">L'interfaccia della **scheda** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3dff7-125">The **ISCard** interface has these methods.</span></span>



| <span data-ttu-id="3dff7-126">Metodo</span><span class="sxs-lookup"><span data-stu-id="3dff7-126">Method</span></span>                                          | <span data-ttu-id="3dff7-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dff7-127">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dff7-128">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="3dff7-128">**AttachByHandle**</span></span>](iscard-attachbyhandle.md) | <span data-ttu-id="3dff7-129">Connette un oggetto a un handle di smart card aperto e configurato.</span><span class="sxs-lookup"><span data-stu-id="3dff7-129">Attaches an object to an open and configured smart card handle.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="3dff7-130">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="3dff7-130">**AttachByReader**</span></span>](iscard-attachbyreader.md) | <span data-ttu-id="3dff7-131">Apre la smart card nel lettore denominato.</span><span class="sxs-lookup"><span data-stu-id="3dff7-131">Opens the smart card in the named reader.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="3dff7-132">**Scollegare**</span><span class="sxs-lookup"><span data-stu-id="3dff7-132">**Detach**</span></span>](iscard-detach.md)                 | <span data-ttu-id="3dff7-133">Chiude la connessione aperta alla smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-133">Closes the open connection to the smart card.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="3dff7-134">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="3dff7-134">**LockSCard**</span></span>](iscard-lockscard.md)           | <span data-ttu-id="3dff7-135">Attesta l'accesso esclusivo alla smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-135">Claims exclusive access to the smart card.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="3dff7-136">**Ricollegare**</span><span class="sxs-lookup"><span data-stu-id="3dff7-136">**ReAttach**</span></span>](iscard-reattach.md)             | <span data-ttu-id="3dff7-137">Reimposta e reinizializza la smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-137">Resets and reinitializes the smart card.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="3dff7-138">**Transazione**</span><span class="sxs-lookup"><span data-stu-id="3dff7-138">**Transaction**</span></span>](iscard-transaction.md)       | <span data-ttu-id="3dff7-139">Esegue un'operazione di scrittura e lettura sull'oggetto comando della smart card ([*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="3dff7-139">Executes a write and read operation on the smart card command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span><br/> |
| [<span data-ttu-id="3dff7-140">**UnlockScard**</span><span class="sxs-lookup"><span data-stu-id="3dff7-140">**UnlockScard**</span></span>](iscard-unlockscard.md)       | <span data-ttu-id="3dff7-141">Rilascia accesso esclusivo alla smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-141">Releases exclusive access to the smart card.</span></span><br/>                                                                                                                                                                         |



 

### <a name="properties"></a><span data-ttu-id="3dff7-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3dff7-142">Properties</span></span>

<span data-ttu-id="3dff7-143">L'interfaccia della **scheda** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3dff7-143">The **ISCard** interface has these properties.</span></span>



| <span data-ttu-id="3dff7-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3dff7-144">Property</span></span>                                               | <span data-ttu-id="3dff7-145">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="3dff7-145">Access type</span></span>          | <span data-ttu-id="3dff7-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dff7-146">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dff7-147">**Atr**</span><span class="sxs-lookup"><span data-stu-id="3dff7-147">**Atr**</span></span>](iscard-get-atr.md)<br/>               | <span data-ttu-id="3dff7-148">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3dff7-148">Read-only</span></span><br/> | <span data-ttu-id="3dff7-149">Recupera la [*stringa ATR*](../secgloss/a-gly.md) della smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-149">Retrieves the [*ATR string*](../secgloss/a-gly.md) of the smart card.</span></span><br/>                                                                   |
| [<span data-ttu-id="3dff7-150">**CardHandle**</span><span class="sxs-lookup"><span data-stu-id="3dff7-150">**CardHandle**</span></span>](iscard-get-cardhandle.md)<br/> | <span data-ttu-id="3dff7-151">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3dff7-151">Read-only</span></span><br/> | <span data-ttu-id="3dff7-152">Recupera l'handle per la smart card connessa.</span><span class="sxs-lookup"><span data-stu-id="3dff7-152">Retrieves the handle for the connected smart card.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="3dff7-153">**Context**</span><span class="sxs-lookup"><span data-stu-id="3dff7-153">**Context**</span></span>](iscard-get-context.md)<br/>       | <span data-ttu-id="3dff7-154">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3dff7-154">Read-only</span></span><br/> | <span data-ttu-id="3dff7-155">Recupera l'handle di contesto corrente di [*Resource Manager*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3dff7-155">Retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span><br/>                            |
| [<span data-ttu-id="3dff7-156">**Protocollo**</span><span class="sxs-lookup"><span data-stu-id="3dff7-156">**Protocol**</span></span>](iscard-get-protocol.md)<br/>     | <span data-ttu-id="3dff7-157">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3dff7-157">Read-only</span></span><br/> | <span data-ttu-id="3dff7-158">Recupera l'identificatore del protocollo attualmente in uso nella smart card.</span><span class="sxs-lookup"><span data-stu-id="3dff7-158">Retrieves the identifier of the protocol currently in use on the smart card.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="3dff7-159">**Stato**</span><span class="sxs-lookup"><span data-stu-id="3dff7-159">**Status**</span></span>](iscard-get-status.md)<br/>         | <span data-ttu-id="3dff7-160">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3dff7-160">Read-only</span></span><br/> | <span data-ttu-id="3dff7-161">Recupera lo [*stato*](../secgloss/s-gly.md) corrente in cui si trova la [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3dff7-161">Retrieves the current [*state*](../secgloss/s-gly.md) the [*smart card*](../secgloss/s-gly.md) is in.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3dff7-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3dff7-162">Requirements</span></span>



| <span data-ttu-id="3dff7-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dff7-163">Requirement</span></span> | <span data-ttu-id="3dff7-164">Valore</span><span class="sxs-lookup"><span data-stu-id="3dff7-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dff7-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3dff7-165">Minimum supported client</span></span><br/> | <span data-ttu-id="3dff7-166">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3dff7-166">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3dff7-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3dff7-167">Minimum supported server</span></span><br/> | <span data-ttu-id="3dff7-168">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3dff7-168">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3dff7-169">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3dff7-169">End of client support</span></span><br/>    | <span data-ttu-id="3dff7-170">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3dff7-170">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3dff7-171">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="3dff7-171">End of server support</span></span><br/>    | <span data-ttu-id="3dff7-172">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3dff7-172">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3dff7-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3dff7-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dff7-174"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dff7-174"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="3dff7-175">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3dff7-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="3dff7-176"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3dff7-176"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3dff7-177">DLL</span><span class="sxs-lookup"><span data-stu-id="3dff7-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dff7-178"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dff7-178"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3dff7-179">IID</span><span class="sxs-lookup"><span data-stu-id="3dff7-179">IID</span></span><br/>                      | <span data-ttu-id="3dff7-180">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3dff7-180">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



 

 
