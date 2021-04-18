---
description: L'interfaccia ISCardDatabase fornisce i metodi per l'esecuzione delle operazioni di database di gestione risorse smart card.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interfaccia ISCardDatabase (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307234"
---
# <a name="iscarddatabase-interface"></a><span data-ttu-id="a9640-103">Interfaccia ISCardDatabase</span><span class="sxs-lookup"><span data-stu-id="a9640-103">ISCardDatabase interface</span></span>

<span data-ttu-id="a9640-104">\[L'interfaccia **ISCardDatabase** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a9640-104">\[The **ISCardDatabase** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a9640-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a9640-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a9640-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a9640-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a9640-107">L'interfaccia **ISCardDatabase** fornisce i metodi per l'esecuzione delle operazioni [*di database di gestione risorse*](../secgloss/r-gly.md) [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a9640-107">The **ISCardDatabase** interface provides the methods for performing the [*smart card*](../secgloss/s-gly.md) [*resource manager's*](../secgloss/r-gly.md) database operations.</span></span> <span data-ttu-id="a9640-108">Queste operazioni includono l'elenco di smart card, [*lettori*](../secgloss/r-gly.md)e gruppi di lettori noti, oltre a recuperare le interfacce supportate da una smart card e dal relativo [*provider di servizi primario*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a9640-108">These operations include listing known smart cards, [*readers*](../secgloss/r-gly.md), and reader groups, plus retrieving the interfaces supported by a smart card and its [*primary service provider*](../secgloss/p-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="a9640-109">L'identificatore del provider di servizi primario è un GUID COM che può essere utilizzato per creare un'istanza di e utilizzare gli oggetti COM per una scheda specifica.</span><span class="sxs-lookup"><span data-stu-id="a9640-109">The identifier of the primary service provider is a COM GUID that can be used to instantiate and use the COM objects for a specific card.</span></span>

 

<span data-ttu-id="a9640-110">Nell'esempio seguente viene illustrato un utilizzo tipico dell'interfaccia **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="a9640-110">The following example shows a typical use of the **ISCardDatabase** interface.</span></span> <span data-ttu-id="a9640-111">In questo caso, l'interfaccia **ISCardDatabase** viene utilizzata per elencare tutte le smart card note.</span><span class="sxs-lookup"><span data-stu-id="a9640-111">In this case, the **ISCardDatabase** interface is used to list all the known smart cards.</span></span>

<span data-ttu-id="a9640-112">**Per inviare una transazione a una scheda specifica**</span><span class="sxs-lookup"><span data-stu-id="a9640-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="a9640-113">Creare un'interfaccia **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="a9640-113">Create an **ISCardDatabase** interface.</span></span>
2.  <span data-ttu-id="a9640-114">Chiamare [**ListCards**](iscarddatabase-listcards.md) per recuperare tutte le smart card note in base a una [*stringa ATR*](../secgloss/a-gly.md) o alle relative interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="a9640-114">Call [**ListCards**](iscarddatabase-listcards.md) to retrieve all the known smart cards based on an [*ATR string*](../secgloss/a-gly.md) or their supported interfaces.</span></span>
3.  <span data-ttu-id="a9640-115">Rilasciare l'interfaccia **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="a9640-115">Release the **ISCardDatabase** interface.</span></span>

## <a name="members"></a><span data-ttu-id="a9640-116">Membri</span><span class="sxs-lookup"><span data-stu-id="a9640-116">Members</span></span>

<span data-ttu-id="a9640-117">L'interfaccia **ISCardDatabase** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a9640-117">The **ISCardDatabase** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a9640-118">**ISCardDatabase** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a9640-118">**ISCardDatabase** also has these types of members:</span></span>

-   [<span data-ttu-id="a9640-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="a9640-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9640-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="a9640-120">Methods</span></span>

<span data-ttu-id="a9640-121">L'interfaccia **ISCardDatabase** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a9640-121">The **ISCardDatabase** interface has these methods.</span></span>



| <span data-ttu-id="a9640-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="a9640-122">Method</span></span>                                                          | <span data-ttu-id="a9640-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9640-123">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9640-124">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="a9640-124">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)   | <span data-ttu-id="a9640-125">Recupera l'identificatore del [*provider di servizi primario*](../secgloss/p-gly.md) per una smart card specifica.</span><span class="sxs-lookup"><span data-stu-id="a9640-125">Retrieves the identifier of the [*primary service provider*](../secgloss/p-gly.md) for a specific smart card.</span></span><br/> |
| [<span data-ttu-id="a9640-126">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a9640-126">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md) | <span data-ttu-id="a9640-127">Recupera gli identificatori di interfaccia (GUID) di tutte le interfacce supportate da una smart card specifica.</span><span class="sxs-lookup"><span data-stu-id="a9640-127">Retrieves the interface identifiers (GUIDs) of all the interfaces supported by a specific smart card.</span></span><br/>                                                                                 |
| [<span data-ttu-id="a9640-128">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="a9640-128">**ListCards**</span></span>](iscarddatabase-listcards.md)                   | <span data-ttu-id="a9640-129">Recupera tutti i nomi delle smart card che corrispondono a un set specifico di identificatori di interfaccia (GUID) o una [*stringa ATR*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a9640-129">Retrieves all the smart card names that match a specific set of interface identifiers (GUIDs) or an [*ATR string*](../secgloss/a-gly.md).</span></span><br/> |
| [<span data-ttu-id="a9640-130">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="a9640-130">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)     | <span data-ttu-id="a9640-131">Recupera i nomi dei [*gruppi di Reader*](../secgloss/r-gly.md) a cui il gestore di risorse è a conoscenza.</span><span class="sxs-lookup"><span data-stu-id="a9640-131">Retrieves the names of the [*reader groups*](../secgloss/r-gly.md) that the resource manager has knowledge of.</span></span><br/>                        |
| [<span data-ttu-id="a9640-132">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="a9640-132">**ListReaders**</span></span>](iscarddatabase-listreaders.md)               | <span data-ttu-id="a9640-133">Recuperare i nomi dei [*lettori*](../secgloss/r-gly.md) di cui il gestore di risorse è a conoscenza.</span><span class="sxs-lookup"><span data-stu-id="a9640-133">Retrieve the names of the [*readers*](../secgloss/r-gly.md) of which the resource manager has knowledge.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="a9640-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9640-134">Requirements</span></span>



| <span data-ttu-id="a9640-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9640-135">Requirement</span></span> | <span data-ttu-id="a9640-136">Valore</span><span class="sxs-lookup"><span data-stu-id="a9640-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9640-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9640-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a9640-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a9640-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a9640-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9640-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a9640-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9640-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9640-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a9640-141">End of client support</span></span><br/>    | <span data-ttu-id="a9640-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9640-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a9640-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a9640-143">End of server support</span></span><br/>    | <span data-ttu-id="a9640-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9640-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a9640-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9640-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9640-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9640-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9640-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a9640-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="a9640-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a9640-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a9640-149">DLL</span><span class="sxs-lookup"><span data-stu-id="a9640-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9640-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9640-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9640-151">IID</span><span class="sxs-lookup"><span data-stu-id="a9640-151">IID</span></span><br/>                      | <span data-ttu-id="a9640-152">IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a9640-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



 

 
