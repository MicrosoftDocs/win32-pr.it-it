---
title: Interfaccia IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di porte seriali all'interno della macchina virtuale. Per ottenere un oggetto IVMSerialPortCollection, usare la proprietà IVMVirtualMachine SerialPorts.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Interfaccia IVMSerialPortCollection Virtual PC
- Interfaccia IVMSerialPortCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741738"
---
# <a name="ivmserialportcollection-interface"></a><span data-ttu-id="784c4-106">Interfaccia IVMSerialPortCollection</span><span class="sxs-lookup"><span data-stu-id="784c4-106">IVMSerialPortCollection interface</span></span>

<span data-ttu-id="784c4-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="784c4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="784c4-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="784c4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="784c4-109">Definisce la raccolta di porte seriali all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="784c4-109">Defines the collection of serial ports within the virtual machine.</span></span> <span data-ttu-id="784c4-110">Per ottenere un oggetto **IVMSerialPortCollection** , usare la proprietà [**IVMVirtualMachine:: Serialports**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="784c4-110">To obtain an **IVMSerialPortCollection** object, use the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="784c4-111">Membri</span><span class="sxs-lookup"><span data-stu-id="784c4-111">Members</span></span>

<span data-ttu-id="784c4-112">L'interfaccia **IVMSerialPortCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="784c4-112">The **IVMSerialPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="784c4-113">**IVMSerialPortCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="784c4-113">**IVMSerialPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="784c4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="784c4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="784c4-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="784c4-115">Properties</span></span>

<span data-ttu-id="784c4-116">L'interfaccia **IVMSerialPortCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="784c4-116">The **IVMSerialPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="784c4-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="784c4-117">Property</span></span>                                                         | <span data-ttu-id="784c4-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="784c4-118">Access type</span></span>          | <span data-ttu-id="784c4-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="784c4-119">Description</span></span>                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="784c4-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="784c4-120">**\_NewEnum**</span></span>](ivmserialportcollection--newenum.md)<br/> | <span data-ttu-id="784c4-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="784c4-121">Read-only</span></span><br/> | <span data-ttu-id="784c4-122">Enumeratore per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="784c4-122">An enumerator for the collection.</span></span><br/>                               |
| [<span data-ttu-id="784c4-123">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="784c4-123">**Count**</span></span>](ivmserialportcollection-count.md)<br/>        | <span data-ttu-id="784c4-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="784c4-124">Read-only</span></span><br/> | <span data-ttu-id="784c4-125">Numero di porte seriali in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="784c4-125">The number of serial ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="784c4-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="784c4-126">**Item**</span></span>](ivmserialportcollection-item.md)<br/>          | <span data-ttu-id="784c4-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="784c4-127">Read-only</span></span><br/> | <span data-ttu-id="784c4-128">Oggetto porta seriale che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="784c4-128">The serial port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="784c4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="784c4-129">Requirements</span></span>



| <span data-ttu-id="784c4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="784c4-130">Requirement</span></span> | <span data-ttu-id="784c4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="784c4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="784c4-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="784c4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="784c4-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="784c4-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="784c4-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="784c4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="784c4-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="784c4-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="784c4-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="784c4-136">End of client support</span></span><br/>    | <span data-ttu-id="784c4-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="784c4-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="784c4-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="784c4-138">Product</span></span><br/>                  | <span data-ttu-id="784c4-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="784c4-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="784c4-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="784c4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="784c4-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="784c4-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="784c4-142">IID</span><span class="sxs-lookup"><span data-stu-id="784c4-142">IID</span></span><br/>                      | <span data-ttu-id="784c4-143">IID \_ IVMSerialPortCollection è definito come dd3c6175-1F04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="784c4-143">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="784c4-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="784c4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="784c4-145">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="784c4-145">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="784c4-146">**IVMVirtualMachine:: SerialPorts**</span><span class="sxs-lookup"><span data-stu-id="784c4-146">**IVMVirtualMachine::SerialPorts**</span></span>](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

