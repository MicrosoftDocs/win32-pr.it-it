---
description: La definizione di interfaccia seguente viene fornita come standard che può essere seguita durante lo sviluppo di un provider di servizi per smart card.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Interfaccia ISCardFileAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882902"
---
# <a name="iscardfileaccess-interface"></a><span data-ttu-id="33b42-103">Interfaccia ISCardFileAccess</span><span class="sxs-lookup"><span data-stu-id="33b42-103">ISCardFileAccess interface</span></span>

<span data-ttu-id="33b42-104">\[L'interfaccia **ISCardFileAccess** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="33b42-104">\[The **ISCardFileAccess** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="33b42-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="33b42-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="33b42-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="33b42-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="33b42-107">La definizione di interfaccia seguente viene fornita come standard che può essere seguita durante lo sviluppo di un [*provider di servizi*](../secgloss/c-gly.md)per [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="33b42-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="33b42-108">L'interfaccia **ISCardFileAccess** può essere usata per implementare un'interfaccia di alto livello per una file System basata su schede con una scheda sottostante file System basata sulla struttura definita in ISO/IEC 7816-4.</span><span class="sxs-lookup"><span data-stu-id="33b42-108">The **ISCardFileAccess** interface can be used to implement a high-level interface to a card-based file system with an underlying card file system based on the structure defined in ISO/IEC 7816-4.</span></span> <span data-ttu-id="33b42-109">Sono possibili altre implementazioni, ma questo dovrebbe essere il più comune.</span><span class="sxs-lookup"><span data-stu-id="33b42-109">Other implementations are possible, but this is expected to be the most common.</span></span>

<span data-ttu-id="33b42-110">L'interfaccia **ISCardFileAccess** può essere utilizzata per esporre file System entità in modo molto familiare agli sviluppatori di applicazioni nell'ambiente del computer.</span><span class="sxs-lookup"><span data-stu-id="33b42-110">The **ISCardFileAccess** interface can be used to expose file system entities in a manner very familiar to application developers in the PC environment.</span></span> <span data-ttu-id="33b42-111">Fornisce meccanismi per l'individuazione di file specifici e l'esecuzione di operazioni comuni, ad esempio la selezione, la lettura, la scrittura, la creazione e l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="33b42-111">It provides mechanisms for locating specific files and performing common operations such as selecting, reading, writing, creating and deleting.</span></span> <span data-ttu-id="33b42-112">Incapsula e maschera gran parte dei dettagli di basso livello necessari per eseguire queste operazioni a livello di scheda.</span><span class="sxs-lookup"><span data-stu-id="33b42-112">It encapsulates and masks much of the low-level detail involved in performing these operations at the card level.</span></span>

<span data-ttu-id="33b42-113">Di seguito è riportato un utilizzo tipico dell'interfaccia **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="33b42-113">Following is a typical use of the **ISCardFileAccess** interface.</span></span> <span data-ttu-id="33b42-114">In questo caso, l'interfaccia **ISCardFileAccess** viene utilizzata per selezionare, aprire e scrivere in un file.</span><span class="sxs-lookup"><span data-stu-id="33b42-114">In this case, the **ISCardFileAccess** interface is used to select, open, and write to a file.</span></span>

<span data-ttu-id="33b42-115">**Per scrivere in un file**</span><span class="sxs-lookup"><span data-stu-id="33b42-115">**To write to a file**</span></span>

1.  <span data-ttu-id="33b42-116">Chiamare [**ISCardManage:: CreateFileAccess**](iscardmanage-createfileaccess.md) per creare un'interfaccia **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="33b42-116">Call [**ISCardManage::CreateFileAccess**](iscardmanage-createfileaccess.md) to create an **ISCardFileAccess** interface.</span></span>
2.  <span data-ttu-id="33b42-117">Chiamare [**Open**](iscardfileaccess-open.md) per selezionare e aprire il file.</span><span class="sxs-lookup"><span data-stu-id="33b42-117">Call [**Open**](iscardfileaccess-open.md) to select and open the file.</span></span>
3.  <span data-ttu-id="33b42-118">Chiamata [**Write**](iscardfileaccess-write.md).</span><span class="sxs-lookup"><span data-stu-id="33b42-118">Call [**Write**](iscardfileaccess-write.md).</span></span>
4.  <span data-ttu-id="33b42-119">[**Chiusura**](iscardfileaccess-close.md)della chiamata.</span><span class="sxs-lookup"><span data-stu-id="33b42-119">Call [**Close**](iscardfileaccess-close.md).</span></span>
5.  <span data-ttu-id="33b42-120">Rilasciare l'interfaccia **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="33b42-120">Release the **ISCardFileAccess** interface.</span></span>

## <a name="members"></a><span data-ttu-id="33b42-121">Membri</span><span class="sxs-lookup"><span data-stu-id="33b42-121">Members</span></span>

<span data-ttu-id="33b42-122">L'interfaccia **ISCardFileAccess** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="33b42-122">The **ISCardFileAccess** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="33b42-123">**ISCardFileAccess** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="33b42-123">**ISCardFileAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="33b42-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="33b42-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="33b42-125">Metodi</span><span class="sxs-lookup"><span data-stu-id="33b42-125">Methods</span></span>

<span data-ttu-id="33b42-126">L'interfaccia **ISCardFileAccess** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="33b42-126">The **ISCardFileAccess** interface has these methods.</span></span>



| <span data-ttu-id="33b42-127">Metodo</span><span class="sxs-lookup"><span data-stu-id="33b42-127">Method</span></span>                                                              | <span data-ttu-id="33b42-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33b42-128">Description</span></span>                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33b42-129">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="33b42-129">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)                     | <span data-ttu-id="33b42-130">Imposta la directory della smart card corrente sulla nuova directory specificata.</span><span class="sxs-lookup"><span data-stu-id="33b42-130">Changes the current smart card directory to the new specified directory.</span></span><br/>                                                          |
| [<span data-ttu-id="33b42-131">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="33b42-131">**Close**</span></span>](iscardfileaccess-close.md)                             | <span data-ttu-id="33b42-132">Chiude il file specificato.</span><span class="sxs-lookup"><span data-stu-id="33b42-132">Closes the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="33b42-133">**Creare**</span><span class="sxs-lookup"><span data-stu-id="33b42-133">**Create**</span></span>](iscardfileaccess-create.md)                           | <span data-ttu-id="33b42-134">Crea un file in una posizione specificata all'interno del file system ICC.</span><span class="sxs-lookup"><span data-stu-id="33b42-134">Creates a file at a given location within the ICC file system.</span></span><br/>                                                                    |
| [<span data-ttu-id="33b42-135">**Delete**</span><span class="sxs-lookup"><span data-stu-id="33b42-135">**Delete**</span></span>](iscardfileaccess-delete.md)                           | <span data-ttu-id="33b42-136">Elimina un file specificato.</span><span class="sxs-lookup"><span data-stu-id="33b42-136">Deletes a specified file.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="33b42-137">**Directory**</span><span class="sxs-lookup"><span data-stu-id="33b42-137">**Directory**</span></span>](iscardfileaccess-directory.md)                     | <span data-ttu-id="33b42-138">Recupera un elenco di file.</span><span class="sxs-lookup"><span data-stu-id="33b42-138">Retrieves a list of files.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="33b42-139">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="33b42-139">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)             | <span data-ttu-id="33b42-140">Restituisce un percorso assoluto della directory attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="33b42-140">Returns an absolute path to the currently selected directory.</span></span><br/>                                                                     |
| [<span data-ttu-id="33b42-141">**GetFileCapabilities**</span><span class="sxs-lookup"><span data-stu-id="33b42-141">**GetFileCapabilities**</span></span>](iscardfileaccess-getfilecapabilities.md) | <span data-ttu-id="33b42-142">Recupera le funzionalità del file.</span><span class="sxs-lookup"><span data-stu-id="33b42-142">Retrieves file capabilities.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="33b42-143">**GetProperties**</span><span class="sxs-lookup"><span data-stu-id="33b42-143">**GetProperties**</span></span>](iscardfileaccess-getproperties.md)             | <span data-ttu-id="33b42-144">Recupera i dati primitivi a cui fanno riferimento i tag per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="33b42-144">Retrieves the primitive data referred by tags for the specified object.</span></span><br/>                                                           |
| [<span data-ttu-id="33b42-145">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="33b42-145">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)                   | <span data-ttu-id="33b42-146">Rende il file specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="33b42-146">Makes the specified file not valid.</span></span><br/>                                                                                               |
| [<span data-ttu-id="33b42-147">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="33b42-147">**Open**</span></span>](iscardfileaccess-open.md)                               | <span data-ttu-id="33b42-148">Apre il file specificato per un ulteriore utilizzo.</span><span class="sxs-lookup"><span data-stu-id="33b42-148">Opens the specified file for further use.</span></span><br/>                                                                                         |
| [<span data-ttu-id="33b42-149">**Lettura**</span><span class="sxs-lookup"><span data-stu-id="33b42-149">**Read**</span></span>](iscardfileaccess-read.md)                               | <span data-ttu-id="33b42-150">Legge e restituisce i dati specificati da un file specificato.</span><span class="sxs-lookup"><span data-stu-id="33b42-150">Reads and returns the specified data from a given file.</span></span><br/>                                                                           |
| [<span data-ttu-id="33b42-151">**Riabilitare**</span><span class="sxs-lookup"><span data-stu-id="33b42-151">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)               | <span data-ttu-id="33b42-152">Rende un file (EF o DF), che in precedenza non è stato reso valido tramite il comando Invalidate, accessibile dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="33b42-152">Makes a file (EF or DF), which has been previously made not valid by using the Invalidate command, accessible by the application.</span></span><br/> |
| [<span data-ttu-id="33b42-153">**Seek**</span><span class="sxs-lookup"><span data-stu-id="33b42-153">**Seek**</span></span>](iscardfileaccess-seek.md)                               | <span data-ttu-id="33b42-154">Seleziona l'oggetto da cui verrà eseguita l'autorizzazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="33b42-154">Selects the object from which read/write permission will be done.</span></span><br/>                                                                 |
| [<span data-ttu-id="33b42-155">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="33b42-155">**SetProperties**</span></span>](iscardfileaccess-setproperties.md)             | <span data-ttu-id="33b42-156">Imposta i dati primitivi a cui fanno riferimento i tag per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="33b42-156">Sets the primitive data referred by tags for the specified object.</span></span><br/>                                                                |
| [<span data-ttu-id="33b42-157">**Scrittura**</span><span class="sxs-lookup"><span data-stu-id="33b42-157">**Write**</span></span>](iscardfileaccess-write.md)                             | <span data-ttu-id="33b42-158">Scrive i dati in un file aperto corrente.</span><span class="sxs-lookup"><span data-stu-id="33b42-158">Writes data to a current opened file.</span></span><br/>                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="33b42-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33b42-159">Requirements</span></span>



| <span data-ttu-id="33b42-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="33b42-160">Requirement</span></span> | <span data-ttu-id="33b42-161">Valore</span><span class="sxs-lookup"><span data-stu-id="33b42-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="33b42-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33b42-162">Minimum supported client</span></span><br/> | <span data-ttu-id="33b42-163">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="33b42-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="33b42-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33b42-164">Minimum supported server</span></span><br/> | <span data-ttu-id="33b42-165">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33b42-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="33b42-166">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="33b42-166">End of client support</span></span><br/>    | <span data-ttu-id="33b42-167">Windows XP</span><span class="sxs-lookup"><span data-stu-id="33b42-167">Windows XP</span></span><br/>                                |
| <span data-ttu-id="33b42-168">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="33b42-168">End of server support</span></span><br/>    | <span data-ttu-id="33b42-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="33b42-169">Windows Server 2003</span></span><br/>                       |



 

 
