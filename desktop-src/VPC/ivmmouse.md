---
title: Interfaccia IVMMouse (VPCCOMInterfaces. h)
description: Controlla il dispositivo mouse all'interno di una macchina virtuale.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Interfaccia IVMMouse Virtual PC
- Interfaccia IVMMouse Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874377"
---
# <a name="ivmmouse-interface"></a><span data-ttu-id="2d71d-105">Interfaccia IVMMouse</span><span class="sxs-lookup"><span data-stu-id="2d71d-105">IVMMouse interface</span></span>

<span data-ttu-id="2d71d-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2d71d-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2d71d-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2d71d-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2d71d-108">Controlla il dispositivo mouse all'interno di una macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="2d71d-108">Controls the mouse device within a virtual machine (VM).</span></span> <span data-ttu-id="2d71d-109">Il **IVMMouse** di una macchina virtuale può essere recuperato usando la proprietà [**IVMVirtualMachine:: mouse**](ivmvirtualmachine-mouse.md) .</span><span class="sxs-lookup"><span data-stu-id="2d71d-109">The **IVMMouse** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Mouse**](ivmvirtualmachine-mouse.md) property.</span></span> <span data-ttu-id="2d71d-110">Le coordinate per il dispositivo mouse possono essere rappresentate in coordinate assolute o in coordinate Delta.</span><span class="sxs-lookup"><span data-stu-id="2d71d-110">Coordinates for the mouse device can be represented either in absolute coordinates or in delta coordinates.</span></span> <span data-ttu-id="2d71d-111">Utilizzare la proprietà [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) per distinguere tra i due metodi di rappresentazione della coordinata.</span><span class="sxs-lookup"><span data-stu-id="2d71d-111">Use the [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) property to distinguish between the two methods of coordinate representation.</span></span> <span data-ttu-id="2d71d-112">Si noti che il recupero della posizione corrente del cursore e l'utilizzo delle coordinate assolute sono supportate solo se nel sistema operativo guest sono installati i componenti di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2d71d-112">Note that retrieving the current cursor position and the use of absolute coordinates are only supported if the guest operating system has the integration components installed.</span></span>

## <a name="members"></a><span data-ttu-id="2d71d-113">Membri</span><span class="sxs-lookup"><span data-stu-id="2d71d-113">Members</span></span>

<span data-ttu-id="2d71d-114">L'interfaccia **IVMMouse** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2d71d-114">The **IVMMouse** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2d71d-115">**IVMMouse** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2d71d-115">**IVMMouse** also has these types of members:</span></span>

-   [<span data-ttu-id="2d71d-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="2d71d-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d71d-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d71d-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d71d-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="2d71d-118">Methods</span></span>

<span data-ttu-id="2d71d-119">L'interfaccia **IVMMouse** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2d71d-119">The **IVMMouse** interface has these methods.</span></span>



| <span data-ttu-id="2d71d-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="2d71d-120">Method</span></span>                                  | <span data-ttu-id="2d71d-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d71d-121">Description</span></span>                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2d71d-122">**Clic**</span><span class="sxs-lookup"><span data-stu-id="2d71d-122">**Click**</span></span>](ivmmouse-click.md)         | <span data-ttu-id="2d71d-123">Simula un clic del pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="2d71d-123">Simulates a mouse button click.</span></span><br/>                                         |
| [<span data-ttu-id="2d71d-124">**GetButton**</span><span class="sxs-lookup"><span data-stu-id="2d71d-124">**GetButton**</span></span>](ivmmouse-getbutton.md) | <span data-ttu-id="2d71d-125">Recupera lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.</span><span class="sxs-lookup"><span data-stu-id="2d71d-125">Retrieves the current state (up or down) of the specified mouse button.</span></span><br/> |
| [<span data-ttu-id="2d71d-126">**Pulsante di**</span><span class="sxs-lookup"><span data-stu-id="2d71d-126">**SetButton**</span></span>](ivmmouse-setbutton.md) | <span data-ttu-id="2d71d-127">Imposta lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.</span><span class="sxs-lookup"><span data-stu-id="2d71d-127">Sets the current state (up or down) of the specified mouse button.</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="2d71d-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d71d-128">Properties</span></span>

<span data-ttu-id="2d71d-129">L'interfaccia **IVMMouse** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2d71d-129">The **IVMMouse** interface has these properties.</span></span>



| <span data-ttu-id="2d71d-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d71d-130">Property</span></span>                                                                         | <span data-ttu-id="2d71d-131">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2d71d-131">Access type</span></span>           | <span data-ttu-id="2d71d-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d71d-132">Description</span></span>                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d71d-133">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="2d71d-133">**HorizontalPosition**</span></span>](ivmmouse-horizontalposition.md)<br/>             | <span data-ttu-id="2d71d-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2d71d-134">Read/write</span></span><br/> | <span data-ttu-id="2d71d-135">Coordinata x assoluta del mouse.</span><span class="sxs-lookup"><span data-stu-id="2d71d-135">The absolute x-coordinate of the mouse.</span></span><br/>                                         |
| [<span data-ttu-id="2d71d-136">**ScrollWheelPosition**</span><span class="sxs-lookup"><span data-stu-id="2d71d-136">**ScrollWheelPosition**</span></span>](ivmmouse-scrollwheelposition.md)<br/>           | <span data-ttu-id="2d71d-137">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="2d71d-137">Write-only</span></span><br/> | <span data-ttu-id="2d71d-138">Coordinata z del mouse (solo relativa).</span><span class="sxs-lookup"><span data-stu-id="2d71d-138">The z-coordinate of the mouse (relative only).</span></span><br/>                                  |
| [<span data-ttu-id="2d71d-139">**UsingAbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="2d71d-139">**UsingAbsoluteCoordinates**</span></span>](ivmmouse-usingabsolutecoordinates.md)<br/> | <span data-ttu-id="2d71d-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2d71d-140">Read/write</span></span><br/> | <span data-ttu-id="2d71d-141">Indica se le coordinate del mouse rappresentano coordinate assolute o relative.</span><span class="sxs-lookup"><span data-stu-id="2d71d-141">Indicates whether mouse coordinates represent absolute or relative coordinates.</span></span><br/> |
| [<span data-ttu-id="2d71d-142">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="2d71d-142">**VerticalPosition**</span></span>](ivmmouse-verticalposition.md)<br/>                 | <span data-ttu-id="2d71d-143">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2d71d-143">Read/write</span></span><br/> | <span data-ttu-id="2d71d-144">Coordinata y assoluta del mouse.</span><span class="sxs-lookup"><span data-stu-id="2d71d-144">The absolute y-coordinate of the mouse.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="2d71d-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d71d-145">Requirements</span></span>



| <span data-ttu-id="2d71d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d71d-146">Requirement</span></span> | <span data-ttu-id="2d71d-147">Valore</span><span class="sxs-lookup"><span data-stu-id="2d71d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d71d-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d71d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2d71d-149">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2d71d-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d71d-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d71d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2d71d-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2d71d-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2d71d-152">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2d71d-152">End of client support</span></span><br/>    | <span data-ttu-id="2d71d-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d71d-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2d71d-154">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2d71d-154">Product</span></span><br/>                  | <span data-ttu-id="2d71d-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2d71d-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2d71d-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d71d-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d71d-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d71d-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2d71d-158">IID</span><span class="sxs-lookup"><span data-stu-id="2d71d-158">IID</span></span><br/>                      | <span data-ttu-id="2d71d-159">IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="2d71d-159">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



 

