---
description: Fornisce i metodi necessari per supportare gli utenti delle altre interfacce COM per smart card.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interfaccia ISCardTypeConv (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881682"
---
# <a name="iscardtypeconv-interface"></a><span data-ttu-id="2b64d-103">Interfaccia ISCardTypeConv</span><span class="sxs-lookup"><span data-stu-id="2b64d-103">ISCardTypeConv interface</span></span>

<span data-ttu-id="2b64d-104">\[L'interfaccia **ISCardTypeConv** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2b64d-104">\[The **ISCardTypeConv** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2b64d-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2b64d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2b64d-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2b64d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2b64d-107">L'interfaccia **ISCardTypeConv** fornisce i metodi necessari per supportare gli utenti delle altre interfacce com per [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2b64d-107">The **ISCardTypeConv** interface provides the methods needed to support the users of the other [*smart card*](../secgloss/s-gly.md) COM interfaces.</span></span> <span data-ttu-id="2b64d-108">Questa interfaccia viene fornita solo per compatibilità con le versioni precedenti e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b64d-108">This interface is provided for backward compatibility only and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="2b64d-109">Membri</span><span class="sxs-lookup"><span data-stu-id="2b64d-109">Members</span></span>

<span data-ttu-id="2b64d-110">L'interfaccia **ISCardTypeConv** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2b64d-110">The **ISCardTypeConv** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2b64d-111">**ISCardTypeConv** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2b64d-111">**ISCardTypeConv** also has these types of members:</span></span>

-   [<span data-ttu-id="2b64d-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2b64d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2b64d-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="2b64d-113">Methods</span></span>

<span data-ttu-id="2b64d-114">L'interfaccia **ISCardTypeConv** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2b64d-114">The **ISCardTypeConv** interface has these methods.</span></span>



| <span data-ttu-id="2b64d-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="2b64d-115">Method</span></span>                                                                              | <span data-ttu-id="2b64d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b64d-116">Description</span></span>                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b64d-117">**ConvertByteArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="2b64d-117">**ConvertByteArrayToByteBuffer**</span></span>](iscardtypeconv-convertbytearraytobytebuffer.md) | <span data-ttu-id="2b64d-118">Converte una matrice di byte C/C++ tipica in un buffer universale di byte (oggetto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="2b64d-118">Converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span><br/>                                   |
| [<span data-ttu-id="2b64d-119">**ConvertByteBufferToByteArray**</span><span class="sxs-lookup"><span data-stu-id="2b64d-119">**ConvertByteBufferToByteArray**</span></span>](iscardtypeconv-convertbytebuffertobytearray.md) | <span data-ttu-id="2b64d-120">Converte una matrice di byte mappata in un buffer universale di byte (oggetto **IStream** ) in una matrice di byte C/C++ tipica.</span><span class="sxs-lookup"><span data-stu-id="2b64d-120">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span><br/>          |
| [<span data-ttu-id="2b64d-121">**ConvertByteBufferToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="2b64d-121">**ConvertByteBufferToSafeArray**</span></span>](iscardtypeconv-convertbytebuffertosafearray.md) | <span data-ttu-id="2b64d-122">Converte una matrice di byte mappata in un buffer universale di byte (oggetto **IStream** ) in un SAFEARRAY di unsigned char (byte).</span><span class="sxs-lookup"><span data-stu-id="2b64d-122">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span><br/> |
| [<span data-ttu-id="2b64d-123">**ConvertSafeArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="2b64d-123">**ConvertSafeArrayToByteBuffer**</span></span>](iscardtypeconv-convertsafearraytobytebuffer.md) | <span data-ttu-id="2b64d-124">Converte una matrice di byte definita come SAFEARRAY in un buffer universale di byte (oggetto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="2b64d-124">Converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span><br/>                          |
| [<span data-ttu-id="2b64d-125">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="2b64d-125">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)                           | <span data-ttu-id="2b64d-126">Crea una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="2b64d-126">Creates an array of bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="2b64d-127">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="2b64d-127">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)                         | <span data-ttu-id="2b64d-128">Crea un buffer universale di byte mappato in un oggetto **IStream** ([**IByteBuffer**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="2b64d-128">Creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span><br/>                  |
| [<span data-ttu-id="2b64d-129">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="2b64d-129">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)                           | <span data-ttu-id="2b64d-130">Crea un SAFEARRAY di automazione di caratteri non firmati (byte).</span><span class="sxs-lookup"><span data-stu-id="2b64d-130">Creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span><br/>                                                              |
| [<span data-ttu-id="2b64d-131">**FreeIStreamMemoryPtr**</span><span class="sxs-lookup"><span data-stu-id="2b64d-131">**FreeIStreamMemoryPtr**</span></span>](iscardtypeconv-freeistreammemoryptr.md)                 | <span data-ttu-id="2b64d-132">Libera un puntatore di memoria per il blocco di memoria HGLOBAL gestito da un'interfaccia com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2b64d-132">Frees a memory pointer to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span><br/>                                  |
| [<span data-ttu-id="2b64d-133">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="2b64d-133">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)                     | <span data-ttu-id="2b64d-134">Acquisisce un puntatore di byte al blocco di memoria HGLOBAL gestito dall'interfaccia com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2b64d-134">Acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span><br/>                        |
| [<span data-ttu-id="2b64d-135">**SizeOfIStream**</span><span class="sxs-lookup"><span data-stu-id="2b64d-135">**SizeOfIStream**</span></span>](iscardtypeconv-sizeofistream.md)                               | <span data-ttu-id="2b64d-136">Determina la dimensione (numero di byte) di un'interfaccia com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2b64d-136">Determines the size (number of bytes) of an **IStream** COM interface.</span></span><br/>                                                       |



 

## <a name="requirements"></a><span data-ttu-id="2b64d-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b64d-137">Requirements</span></span>



| <span data-ttu-id="2b64d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b64d-138">Requirement</span></span> | <span data-ttu-id="2b64d-139">Valore</span><span class="sxs-lookup"><span data-stu-id="2b64d-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b64d-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b64d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2b64d-141">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2b64d-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2b64d-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b64d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2b64d-143">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2b64d-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b64d-144">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2b64d-144">End of client support</span></span><br/>    | <span data-ttu-id="2b64d-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b64d-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2b64d-146">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2b64d-146">End of server support</span></span><br/>    | <span data-ttu-id="2b64d-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b64d-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2b64d-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b64d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b64d-149"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b64d-149"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b64d-150">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2b64d-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b64d-151"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2b64d-151"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2b64d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="2b64d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b64d-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b64d-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b64d-154">IID</span><span class="sxs-lookup"><span data-stu-id="2b64d-154">IID</span></span><br/>                      | <span data-ttu-id="2b64d-155">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2b64d-155">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



 

 
