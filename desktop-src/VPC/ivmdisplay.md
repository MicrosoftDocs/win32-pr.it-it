---
title: Interfaccia IVMDisplay (VPCCOMInterfaces. h)
description: Controlla le impostazioni di visualizzazione di una macchina virtuale. L'interfaccia IVMDisplay per una macchina virtuale può essere recuperata usando la proprietà di visualizzazione IVMVirtualMachine.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Interfaccia IVMDisplay Virtual PC
- Interfaccia IVMDisplay Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964599"
---
# <a name="ivmdisplay-interface"></a><span data-ttu-id="2798a-106">Interfaccia IVMDisplay</span><span class="sxs-lookup"><span data-stu-id="2798a-106">IVMDisplay interface</span></span>

<span data-ttu-id="2798a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2798a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2798a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2798a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2798a-109">Controlla le impostazioni di visualizzazione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2798a-109">Controls the display settings of a virtual machine.</span></span> <span data-ttu-id="2798a-110">È possibile recuperare l'interfaccia **IVMDisplay** per una macchina virtuale utilizzando la proprietà [**IVMVirtualMachine::D di riproduzione**](ivmvirtualmachine-display.md) .</span><span class="sxs-lookup"><span data-stu-id="2798a-110">The **IVMDisplay** interface for a virtual machine can be retrieved using the [**IVMVirtualMachine::Display**](ivmvirtualmachine-display.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="2798a-111">Membri</span><span class="sxs-lookup"><span data-stu-id="2798a-111">Members</span></span>

<span data-ttu-id="2798a-112">L'interfaccia **IVMDisplay** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2798a-112">The **IVMDisplay** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2798a-113">**IVMDisplay** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2798a-113">**IVMDisplay** also has these types of members:</span></span>

-   [<span data-ttu-id="2798a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="2798a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2798a-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2798a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2798a-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="2798a-116">Methods</span></span>

<span data-ttu-id="2798a-117">L'interfaccia **IVMDisplay** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2798a-117">The **IVMDisplay** interface has these methods.</span></span>



| <span data-ttu-id="2798a-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="2798a-118">Method</span></span>                                                       | <span data-ttu-id="2798a-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2798a-119">Description</span></span>                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2798a-120">**\_GenerateThumbnail**</span><span class="sxs-lookup"><span data-stu-id="2798a-120">**\_GenerateThumbnail**</span></span>](ivmdisplay--generatethumbnail.md) | <span data-ttu-id="2798a-121">Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2798a-121">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="2798a-122">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="2798a-122">**SetDimensions**</span></span>](ivmdisplay-setdimensions.md)            | <span data-ttu-id="2798a-123">Imposta l'altezza e la larghezza della visualizzazione della macchina virtuale, in pixel.</span><span class="sxs-lookup"><span data-stu-id="2798a-123">Sets the height and width of the virtual machine's display, in pixels.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="2798a-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2798a-124">Properties</span></span>

<span data-ttu-id="2798a-125">L'interfaccia **IVMDisplay** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2798a-125">The **IVMDisplay** interface has these properties.</span></span>



| <span data-ttu-id="2798a-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2798a-126">Property</span></span>                                             | <span data-ttu-id="2798a-127">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2798a-127">Access type</span></span>          | <span data-ttu-id="2798a-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2798a-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2798a-129">**CanResize**</span><span class="sxs-lookup"><span data-stu-id="2798a-129">**CanResize**</span></span>](ivmdisplay-canresize.md)<br/> | <span data-ttu-id="2798a-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2798a-130">Read-only</span></span><br/> | <span data-ttu-id="2798a-131">Indica se il Guest consente le modifiche di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="2798a-131">Indicates whether the Guest allows resolution changes.</span></span><br/>                             |
| [<span data-ttu-id="2798a-132">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="2798a-132">**Height**</span></span>](ivmdisplay-height.md)<br/>       | <span data-ttu-id="2798a-133">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2798a-133">Read-only</span></span><br/> | <span data-ttu-id="2798a-134">Altezza, in pixel, della visualizzazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2798a-134">The height of the virtual machine's display, in pixels.</span></span><br/>                            |
| [<span data-ttu-id="2798a-135">**Anteprima**</span><span class="sxs-lookup"><span data-stu-id="2798a-135">**Thumbnail**</span></span>](ivmdisplay-thumbnail.md)<br/> | <span data-ttu-id="2798a-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2798a-136">Read-only</span></span><br/> | <span data-ttu-id="2798a-137">Matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2798a-137">An array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="2798a-138">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="2798a-138">**VideoMode**</span></span>](ivmdisplay-videomode.md)<br/> | <span data-ttu-id="2798a-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2798a-139">Read-only</span></span><br/> | <span data-ttu-id="2798a-140">Modalità video corrente (testo, VGA, SVGA e così via).</span><span class="sxs-lookup"><span data-stu-id="2798a-140">The current video mode (Text, VGA, SVGA, and so on).</span></span><br/>                               |
| [<span data-ttu-id="2798a-141">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="2798a-141">**Width**</span></span>](ivmdisplay-width.md)<br/>         | <span data-ttu-id="2798a-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2798a-142">Read-only</span></span><br/> | <span data-ttu-id="2798a-143">Larghezza, in pixel, dello schermo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2798a-143">The width of the virtual machine's display, in pixels.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="2798a-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2798a-144">Requirements</span></span>



| <span data-ttu-id="2798a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="2798a-145">Requirement</span></span> | <span data-ttu-id="2798a-146">Valore</span><span class="sxs-lookup"><span data-stu-id="2798a-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2798a-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2798a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="2798a-148">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2798a-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2798a-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2798a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="2798a-150">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2798a-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2798a-151">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2798a-151">End of client support</span></span><br/>    | <span data-ttu-id="2798a-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2798a-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2798a-153">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2798a-153">Product</span></span><br/>                  | <span data-ttu-id="2798a-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2798a-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2798a-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2798a-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="2798a-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2798a-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2798a-157">IID</span><span class="sxs-lookup"><span data-stu-id="2798a-157">IID</span></span><br/>                      | <span data-ttu-id="2798a-158">IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="2798a-158">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



 

