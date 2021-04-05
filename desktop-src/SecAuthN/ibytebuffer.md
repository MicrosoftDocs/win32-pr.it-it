---
description: Viene fornita l'interfaccia IByteBuffer per la lettura, la scrittura e la gestione di oggetti flusso. Questo oggetto è essenzialmente un wrapper per l'oggetto IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interfaccia IByteBuffer (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968294"
---
# <a name="ibytebuffer-interface"></a><span data-ttu-id="28540-104">Interfaccia IByteBuffer</span><span class="sxs-lookup"><span data-stu-id="28540-104">IByteBuffer interface</span></span>

<span data-ttu-id="28540-105">\[L'interfaccia **IByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="28540-105">\[The **IByteBuffer** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="28540-106">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="28540-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="28540-107">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="28540-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="28540-108">Viene fornita l'interfaccia **IByteBuffer** per la lettura, la scrittura e la gestione di oggetti flusso.</span><span class="sxs-lookup"><span data-stu-id="28540-108">The **IByteBuffer** interface is provided to read, write and manage stream objects.</span></span> <span data-ttu-id="28540-109">Questo oggetto è essenzialmente un wrapper per l'oggetto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="28540-109">This object essentially is a wrapper for the **IStream** object.</span></span>

## <a name="members"></a><span data-ttu-id="28540-110">Membri</span><span class="sxs-lookup"><span data-stu-id="28540-110">Members</span></span>

<span data-ttu-id="28540-111">L'interfaccia **IByteBuffer** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="28540-111">The **IByteBuffer** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="28540-112">**IByteBuffer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="28540-112">**IByteBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="28540-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="28540-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="28540-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="28540-114">Methods</span></span>

<span data-ttu-id="28540-115">L'interfaccia **IByteBuffer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="28540-115">The **IByteBuffer** interface has these methods.</span></span>



| <span data-ttu-id="28540-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="28540-116">Method</span></span>                                           | <span data-ttu-id="28540-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28540-117">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28540-118">**Clone**</span><span class="sxs-lookup"><span data-stu-id="28540-118">**Clone**</span></span>](ibytebuffer-clone.md)               | <span data-ttu-id="28540-119">Clona un oggetto **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="28540-119">Clones an **IByteBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="28540-120">**Commit**</span><span class="sxs-lookup"><span data-stu-id="28540-120">**Commit**</span></span>](ibytebuffer-commit.md)             | <span data-ttu-id="28540-121">Viene eseguito il commit di una [*transazione*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="28540-121">Commits a [*transaction*](/windows/desktop/SecGloss/t-gly).</span></span><br/> |
| [<span data-ttu-id="28540-122">**CopyTo**</span><span class="sxs-lookup"><span data-stu-id="28540-122">**CopyTo**</span></span>](ibytebuffer-copyto.md)             | <span data-ttu-id="28540-123">Copia i byte in un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="28540-123">Copies bytes to another object.</span></span><br/>                                                                |
| [<span data-ttu-id="28540-124">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="28540-124">**Initialize**</span></span>](ibytebuffer-initialize.md)     | <span data-ttu-id="28540-125">Inizializza l'oggetto **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="28540-125">Initializes the **IByteBuffer** object.</span></span><br/>                                                        |
| [<span data-ttu-id="28540-126">**LockRegion**</span><span class="sxs-lookup"><span data-stu-id="28540-126">**LockRegion**</span></span>](ibytebuffer-lockregion.md)     | <span data-ttu-id="28540-127">Limita l'accesso a un intervallo di byte.</span><span class="sxs-lookup"><span data-stu-id="28540-127">Restricts access to a range of bytes.</span></span><br/>                                                          |
| [<span data-ttu-id="28540-128">**Lettura**</span><span class="sxs-lookup"><span data-stu-id="28540-128">**Read**</span></span>](ibytebuffer-read.md)                 | <span data-ttu-id="28540-129">Legge i byte in memoria.</span><span class="sxs-lookup"><span data-stu-id="28540-129">Reads bytes into memory.</span></span><br/>                                                                       |
| [<span data-ttu-id="28540-130">**Ripristinare**</span><span class="sxs-lookup"><span data-stu-id="28540-130">**Revert**</span></span>](ibytebuffer-revert.md)             | <span data-ttu-id="28540-131">Elimina le modifiche apportate dall'ultima chiamata al [**commit**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="28540-131">Discards changes since the last [**Commit**](ibytebuffer-commit.md) call.</span></span><br/>                     |
| [<span data-ttu-id="28540-132">**Seek**</span><span class="sxs-lookup"><span data-stu-id="28540-132">**Seek**</span></span>](ibytebuffer-seek.md)                 | <span data-ttu-id="28540-133">Modifica il puntatore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="28540-133">Changes the seek pointer.</span></span><br/>                                                                      |
| [<span data-ttu-id="28540-134">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="28540-134">**SetSize**</span></span>](ibytebuffer-setsize.md)           | <span data-ttu-id="28540-135">Modifica la dimensione dell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="28540-135">Changes the size of the stream object.</span></span><br/>                                                         |
| [<span data-ttu-id="28540-136">**Stat**</span><span class="sxs-lookup"><span data-stu-id="28540-136">**Stat**</span></span>](ibytebuffer-stat.md)                 | <span data-ttu-id="28540-137">Recupera le informazioni statistiche su un flusso.</span><span class="sxs-lookup"><span data-stu-id="28540-137">Retrieves statistical information about a stream.</span></span><br/>                                              |
| [<span data-ttu-id="28540-138">**UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="28540-138">**UnlockRegion**</span></span>](ibytebuffer-unlockregion.md) | <span data-ttu-id="28540-139">Rimuove la restrizione di accesso precedentemente impostata da [**LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="28540-139">Removes access restriction previously set by [**LockRegion**](ibytebuffer-lockregion.md).</span></span><br/>     |
| [<span data-ttu-id="28540-140">**Scrittura**</span><span class="sxs-lookup"><span data-stu-id="28540-140">**Write**</span></span>](ibytebuffer-write.md)               | <span data-ttu-id="28540-141">Scrive i byte nel flusso.</span><span class="sxs-lookup"><span data-stu-id="28540-141">Writes bytes to the stream.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="28540-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28540-142">Requirements</span></span>



| <span data-ttu-id="28540-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="28540-143">Requirement</span></span> | <span data-ttu-id="28540-144">Valore</span><span class="sxs-lookup"><span data-stu-id="28540-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28540-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28540-145">Minimum supported client</span></span><br/> | <span data-ttu-id="28540-146">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="28540-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="28540-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28540-147">Minimum supported server</span></span><br/> | <span data-ttu-id="28540-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28540-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28540-149">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="28540-149">End of client support</span></span><br/>    | <span data-ttu-id="28540-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="28540-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="28540-151">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="28540-151">End of server support</span></span><br/>    | <span data-ttu-id="28540-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28540-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="28540-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28540-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="28540-154"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="28540-154"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="28540-155">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="28540-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="28540-156"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="28540-156"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="28540-157">DLL</span><span class="sxs-lookup"><span data-stu-id="28540-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28540-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28540-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="28540-159">IID</span><span class="sxs-lookup"><span data-stu-id="28540-159">IID</span></span><br/>                      | <span data-ttu-id="28540-160">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="28540-160">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

