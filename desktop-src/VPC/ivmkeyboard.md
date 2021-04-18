---
title: Interfaccia IVMKeyboard (VPCCOMInterfaces. h)
description: Controlla il dispositivo della tastiera all'interno di una macchina virtuale. Il IVMKeyboard di una macchina virtuale può essere recuperato usando la proprietà della tastiera IVMVirtualMachine.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Interfaccia IVMKeyboard Virtual PC
- Interfaccia IVMKeyboard Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302560"
---
# <a name="ivmkeyboard-interface"></a><span data-ttu-id="76a27-106">Interfaccia IVMKeyboard</span><span class="sxs-lookup"><span data-stu-id="76a27-106">IVMKeyboard interface</span></span>

<span data-ttu-id="76a27-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="76a27-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="76a27-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="76a27-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="76a27-109">Controlla il dispositivo della tastiera all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76a27-109">Controls the keyboard device within a virtual machine.</span></span> <span data-ttu-id="76a27-110">Il **IVMKeyboard** di una macchina virtuale può essere recuperato usando la proprietà [**IVMVirtualMachine:: Keyboard**](ivmvirtualmachine-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="76a27-110">The **IVMKeyboard** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Keyboard**](ivmvirtualmachine-keyboard.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="76a27-111">Membri</span><span class="sxs-lookup"><span data-stu-id="76a27-111">Members</span></span>

<span data-ttu-id="76a27-112">L'interfaccia **IVMKeyboard** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="76a27-112">The **IVMKeyboard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="76a27-113">**IVMKeyboard** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="76a27-113">**IVMKeyboard** also has these types of members:</span></span>

-   [<span data-ttu-id="76a27-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="76a27-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="76a27-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76a27-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="76a27-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="76a27-116">Methods</span></span>

<span data-ttu-id="76a27-117">L'interfaccia **IVMKeyboard** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="76a27-117">The **IVMKeyboard** interface has these methods.</span></span>



| <span data-ttu-id="76a27-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="76a27-118">Method</span></span>                                                       | <span data-ttu-id="76a27-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76a27-119">Description</span></span>                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="76a27-120">**IsPressed**</span><span class="sxs-lookup"><span data-stu-id="76a27-120">**IsPressed**</span></span>](ivmkeyboard-ispressed.md)                   | <span data-ttu-id="76a27-121">Determina se il tasto specificato è inattivo.</span><span class="sxs-lookup"><span data-stu-id="76a27-121">Determines whether the specified key is down.</span></span><br/>                      |
| [<span data-ttu-id="76a27-122">**PressAndReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="76a27-122">**PressAndReleaseKey**</span></span>](ivmkeyboard-pressandreleasekey.md) | <span data-ttu-id="76a27-123">Simula un tasto premuto e quindi rilasciato.</span><span class="sxs-lookup"><span data-stu-id="76a27-123">Simulates a key being pressed down and then released.</span></span><br/>              |
| [<span data-ttu-id="76a27-124">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="76a27-124">**PressKey**</span></span>](ivmkeyboard-presskey.md)                     | <span data-ttu-id="76a27-125">Simula un tasto premuto.</span><span class="sxs-lookup"><span data-stu-id="76a27-125">Simulates a key being pressed down.</span></span><br/>                                |
| [<span data-ttu-id="76a27-126">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="76a27-126">**ReleaseKey**</span></span>](ivmkeyboard-releasekey.md)                 | <span data-ttu-id="76a27-127">Simula una chiave rilasciata.</span><span class="sxs-lookup"><span data-stu-id="76a27-127">Simulates a key being released.</span></span><br/>                                    |
| [<span data-ttu-id="76a27-128">**TypeAsciiText**</span><span class="sxs-lookup"><span data-stu-id="76a27-128">**TypeAsciiText**</span></span>](ivmkeyboard-typeasciitext.md)           | <span data-ttu-id="76a27-129">Simula una serie di chiavi ASCII digitate nel guest.</span><span class="sxs-lookup"><span data-stu-id="76a27-129">Simulates a series of ASCII keys being typed into the guest.</span></span><br/>       |
| [<span data-ttu-id="76a27-130">**TypeKeySequence**</span><span class="sxs-lookup"><span data-stu-id="76a27-130">**TypeKeySequence**</span></span>](ivmkeyboard-typekeysequence.md)       | <span data-ttu-id="76a27-131">Simula un elenco delimitato da virgole di chiavi digitate nel guest.</span><span class="sxs-lookup"><span data-stu-id="76a27-131">Simulates a comma-delimited list of keys being typed in the guest.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="76a27-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76a27-132">Properties</span></span>

<span data-ttu-id="76a27-133">L'interfaccia **IVMKeyboard** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="76a27-133">The **IVMKeyboard** interface has these properties.</span></span>



| <span data-ttu-id="76a27-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76a27-134">Property</span></span>                                                                | <span data-ttu-id="76a27-135">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="76a27-135">Access type</span></span>           | <span data-ttu-id="76a27-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76a27-136">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76a27-137">**HasExclusiveAccess**</span><span class="sxs-lookup"><span data-stu-id="76a27-137">**HasExclusiveAccess**</span></span>](ivmkeyboard-hasexclusiveaccess.md)<br/> | <span data-ttu-id="76a27-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="76a27-138">Read/write</span></span><br/> | <span data-ttu-id="76a27-139">Indica se l'oggetto dispone del controllo esclusivo sul dispositivo della tastiera della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76a27-139">Indicates whether this object has exclusive control over the virtual machine's keyboard device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76a27-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="76a27-140">Remarks</span></span>

<span data-ttu-id="76a27-141">Le chiavi possono essere digitate nella macchina virtuale in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="76a27-141">Keys can be typed into the virtual machine in several ways.</span></span> <span data-ttu-id="76a27-142">Per digitare una normale sequenza ASCII di caratteri, usare il metodo [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) .</span><span class="sxs-lookup"><span data-stu-id="76a27-142">To type a normal ASCII sequence of characters, use the [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) method.</span></span> <span data-ttu-id="76a27-143">Se è necessaria una maggiore flessibilità, **IVMKeyboard** dispone di diversi metodi progettati per essere utilizzati con i codici chiave elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="76a27-143">If greater flexibility is required, **IVMKeyboard** has several methods that are designed to be used with the key codes in the following list.</span></span> <span data-ttu-id="76a27-144">Il metodo [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) può accettare una stringa delimitata da virgole di codici chiave, che verrà premuta e rilasciata nell'ordine, all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76a27-144">The [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) method can accept a comma-delimited string of key codes, which will be pressed and released, in order, within the virtual machine.</span></span> <span data-ttu-id="76a27-145">Oltre a questi codici chiave, è possibile usare le parole chiave su e giù per forzare la pressione di una chiave solo o rilasciarla.</span><span class="sxs-lookup"><span data-stu-id="76a27-145">In addition to these key codes, the keywords UP and DOWN can be used to force a key to only be pressed, or only be released.</span></span> <span data-ttu-id="76a27-146">Le parole chiave UP e DOWN si applicano solo al codice chiave che segue direttamente la parola chiave.</span><span class="sxs-lookup"><span data-stu-id="76a27-146">The UP and DOWN keywords only apply to the key code directly following the keyword.</span></span>

<span data-ttu-id="76a27-147">Per evitare che più script, applicazioni o utenti tentino simultaneamente di accedere allo stesso dispositivo della tastiera, impostare la proprietà [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="76a27-147">To avoid multiple scripts, applications, or users from simultaneously attempting to access the same keyboard device, set the [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) property to **TRUE**.</span></span> <span data-ttu-id="76a27-148">Se l'accesso esclusivo viene acquisito da un processo, eventuali tentativi da parte di altri processi di inviare input al dispositivo della tastiera verranno ignorati fino a quando non viene rilasciato l'accesso esclusivo.</span><span class="sxs-lookup"><span data-stu-id="76a27-148">If exclusive access is acquired by one process, any attempts by other processes to send input to the keyboard device will be ignored until exclusive access has been released.</span></span>

## <a name="requirements"></a><span data-ttu-id="76a27-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76a27-149">Requirements</span></span>



| <span data-ttu-id="76a27-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="76a27-150">Requirement</span></span> | <span data-ttu-id="76a27-151">Valore</span><span class="sxs-lookup"><span data-stu-id="76a27-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76a27-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76a27-152">Minimum supported client</span></span><br/> | <span data-ttu-id="76a27-153">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76a27-153">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76a27-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76a27-154">Minimum supported server</span></span><br/> | <span data-ttu-id="76a27-155">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="76a27-155">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="76a27-156">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="76a27-156">End of client support</span></span><br/>    | <span data-ttu-id="76a27-157">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76a27-157">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="76a27-158">Prodotto</span><span class="sxs-lookup"><span data-stu-id="76a27-158">Product</span></span><br/>                  | <span data-ttu-id="76a27-159">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="76a27-159">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="76a27-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76a27-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="76a27-161"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="76a27-161"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="76a27-162">IID</span><span class="sxs-lookup"><span data-stu-id="76a27-162">IID</span></span><br/>                      | <span data-ttu-id="76a27-163">IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="76a27-163">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="76a27-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76a27-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76a27-165">Interfacce Virtual PC Windows</span><span class="sxs-lookup"><span data-stu-id="76a27-165">Windows Virtual PC Interfaces</span></span>](virtual-pc-interfaces.md)
</dt> <dt>

[<span data-ttu-id="76a27-166">Sequenze di chiavi</span><span class="sxs-lookup"><span data-stu-id="76a27-166">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

