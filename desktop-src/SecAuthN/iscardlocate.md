---
description: L'interfaccia ISCardLocate fornisce servizi per l'individuazione di una smart card in base al nome.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interfaccia ISCardLocate (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313734"
---
# <a name="iscardlocate-interface"></a><span data-ttu-id="2a235-103">Interfaccia ISCardLocate</span><span class="sxs-lookup"><span data-stu-id="2a235-103">ISCardLocate interface</span></span>

<span data-ttu-id="2a235-104">\[L'interfaccia **ISCardLocate** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2a235-104">\[The **ISCardLocate** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2a235-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2a235-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2a235-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2a235-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2a235-107">L'interfaccia **ISCardLocate** fornisce servizi per l'individuazione di una [*Smart Card*](../secgloss/s-gly.md) in base al nome.</span><span class="sxs-lookup"><span data-stu-id="2a235-107">The **ISCardLocate** interface provides services for locating a [*smart card*](../secgloss/s-gly.md) by its name.</span></span>

<span data-ttu-id="2a235-108">Questa interfaccia può visualizzare l' [*interfaccia utente*](../secgloss/u-gly.md) della smart card, se necessaria.</span><span class="sxs-lookup"><span data-stu-id="2a235-108">This interface can display the smart card [*user interface*](../secgloss/u-gly.md) if it is required.</span></span>

<span data-ttu-id="2a235-109">Nello scenario seguente viene illustrato un utilizzo tipico dell'interfaccia **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="2a235-109">The following scenario shows a typical use of the **ISCardLocate** interface.</span></span> <span data-ttu-id="2a235-110">L'interfaccia **ISCardLocate** viene utilizzata per compilare un' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="2a235-110">The **ISCardLocate** interface is used to build an [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

<span data-ttu-id="2a235-111">**Per individuare una scheda specifica usando il nome**</span><span class="sxs-lookup"><span data-stu-id="2a235-111">**To locate a specific card using its name**</span></span>

1.  <span data-ttu-id="2a235-112">Creare un'interfaccia **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="2a235-112">Create an **ISCardLocate** interface.</span></span>
2.  <span data-ttu-id="2a235-113">Chiamare [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) per cercare il nome di una smart card.</span><span class="sxs-lookup"><span data-stu-id="2a235-113">Call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to search for a smart card name.</span></span>
3.  <span data-ttu-id="2a235-114">Chiamare [**FindCard**](iscardlocate-findcard.md) per cercare la smart card.</span><span class="sxs-lookup"><span data-stu-id="2a235-114">Call [**FindCard**](iscardlocate-findcard.md) to search for the smart card.</span></span>
4.  <span data-ttu-id="2a235-115">Interpretare i risultati.</span><span class="sxs-lookup"><span data-stu-id="2a235-115">Interpret the results.</span></span>
5.  <span data-ttu-id="2a235-116">Rilasciare l'interfaccia **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="2a235-116">Release the **ISCardLocate** interface.</span></span>

## <a name="members"></a><span data-ttu-id="2a235-117">Membri</span><span class="sxs-lookup"><span data-stu-id="2a235-117">Members</span></span>

<span data-ttu-id="2a235-118">L'interfaccia **ISCardLocate** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2a235-118">The **ISCardLocate** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2a235-119">**ISCardLocate** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a235-119">**ISCardLocate** also has these types of members:</span></span>

-   [<span data-ttu-id="2a235-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a235-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2a235-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a235-121">Methods</span></span>

<span data-ttu-id="2a235-122">L'interfaccia **ISCardLocate** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2a235-122">The **ISCardLocate** interface has these methods.</span></span>



| <span data-ttu-id="2a235-123">Metodo</span><span class="sxs-lookup"><span data-stu-id="2a235-123">Method</span></span>                                                                  | <span data-ttu-id="2a235-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a235-124">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="2a235-125">**ConfigureCardGuidSearch**</span><span class="sxs-lookup"><span data-stu-id="2a235-125">**ConfigureCardGuidSearch**</span></span>                                             | <span data-ttu-id="2a235-126">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="2a235-126">Reserved for future use.</span></span><br/>                                        |
| [<span data-ttu-id="2a235-127">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="2a235-127">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md) | <span data-ttu-id="2a235-128">Specifica il nome della scheda da utilizzare nella ricerca.</span><span class="sxs-lookup"><span data-stu-id="2a235-128">Specifies the card name to be used in the search.</span></span><br/>               |
| [<span data-ttu-id="2a235-129">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="2a235-129">**FindCard**</span></span>](iscardlocate-findcard.md)                               | <span data-ttu-id="2a235-130">Cerca la smart card e apre una connessione valida.</span><span class="sxs-lookup"><span data-stu-id="2a235-130">Searches for the smart card and opens a valid connection to it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2a235-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a235-131">Requirements</span></span>



| <span data-ttu-id="2a235-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a235-132">Requirement</span></span> | <span data-ttu-id="2a235-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2a235-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a235-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a235-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2a235-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2a235-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2a235-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a235-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2a235-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a235-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a235-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2a235-138">End of client support</span></span><br/>    | <span data-ttu-id="2a235-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2a235-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2a235-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2a235-140">End of server support</span></span><br/>    | <span data-ttu-id="2a235-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a235-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2a235-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a235-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a235-143"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a235-143"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a235-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2a235-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="2a235-145"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2a235-145"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2a235-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2a235-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a235-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a235-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2a235-148">IID</span><span class="sxs-lookup"><span data-stu-id="2a235-148">IID</span></span><br/>                      | <span data-ttu-id="2a235-149">IID \_ ISCardLocate è definito come 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2a235-149">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



 

 
