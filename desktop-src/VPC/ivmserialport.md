---
title: Interfaccia IVMSerialPort (VPCCOMInterfaces. h)
description: Definisce una porta seriale all'interno di una macchina virtuale.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Interfaccia IVMSerialPort Virtual PC
- Interfaccia IVMSerialPort Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518394"
---
# <a name="ivmserialport-interface"></a><span data-ttu-id="c82c2-105">Interfaccia IVMSerialPort</span><span class="sxs-lookup"><span data-stu-id="c82c2-105">IVMSerialPort interface</span></span>

<span data-ttu-id="c82c2-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c82c2-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c82c2-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c82c2-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c82c2-108">Definisce una porta seriale all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c82c2-108">Defines a serial port inside a virtual machine.</span></span> <span data-ttu-id="c82c2-109">Questa interfaccia consente di configurare le porte seriali all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c82c2-109">This interface allows you to configure serial ports inside a virtual machine.</span></span> <span data-ttu-id="c82c2-110">È possibile recuperare un oggetto **IVMSerialPort** dall'oggetto [**IVMSerialPortCollection**](ivmserialportcollection.md) restituito dalla proprietà [**IVMVirtualMachine:: Serialports**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="c82c2-110">You can retrieve an **IVMSerialPort** object from the [**IVMSerialPortCollection**](ivmserialportcollection.md) object returned from the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="c82c2-111">Membri</span><span class="sxs-lookup"><span data-stu-id="c82c2-111">Members</span></span>

<span data-ttu-id="c82c2-112">L'interfaccia **IVMSerialPort** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c82c2-112">The **IVMSerialPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c82c2-113">**IVMSerialPort** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c82c2-113">**IVMSerialPort** also has these types of members:</span></span>

-   [<span data-ttu-id="c82c2-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="c82c2-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c82c2-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c82c2-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c82c2-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="c82c2-116">Methods</span></span>

<span data-ttu-id="c82c2-117">L'interfaccia **IVMSerialPort** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c82c2-117">The **IVMSerialPort** interface has these methods.</span></span>



| <span data-ttu-id="c82c2-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="c82c2-118">Method</span></span>                                       | <span data-ttu-id="c82c2-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c82c2-119">Description</span></span>                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="c82c2-120">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="c82c2-120">**\_ID**</span></span>](ivmserialport--id.md)            | <span data-ttu-id="c82c2-121">Recupera l'identificatore interno della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="c82c2-121">Retrieves the internal identifier of the serial port.</span></span><br/> |
| [<span data-ttu-id="c82c2-122">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="c82c2-122">**Configure**</span></span>](ivmserialport-configure.md) | <span data-ttu-id="c82c2-123">Configura la porta seriale.</span><span class="sxs-lookup"><span data-stu-id="c82c2-123">Configures the serial port.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="c82c2-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c82c2-124">Properties</span></span>

<span data-ttu-id="c82c2-125">L'interfaccia **IVMSerialPort** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c82c2-125">The **IVMSerialPort** interface has these properties.</span></span>



| <span data-ttu-id="c82c2-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c82c2-126">Property</span></span>                                                                  | <span data-ttu-id="c82c2-127">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="c82c2-127">Access type</span></span>          | <span data-ttu-id="c82c2-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c82c2-128">Description</span></span>                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c82c2-129">**ConnectImmediately**</span><span class="sxs-lookup"><span data-stu-id="c82c2-129">**ConnectImmediately**</span></span>](ivmserialport-connectimmediately.md)<br/> | <span data-ttu-id="c82c2-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c82c2-130">Read-only</span></span><br/> | <span data-ttu-id="c82c2-131">Indica se la porta seriale deve essere aperta senza attendere la ricezione di un comando del modem.</span><span class="sxs-lookup"><span data-stu-id="c82c2-131">Indicates whether the serial port should be opened without waiting for a modem command to be received.</span></span><br/> |
| [<span data-ttu-id="c82c2-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c82c2-132">**Name**</span></span>](ivmserialport-name.md)<br/>                             | <span data-ttu-id="c82c2-133">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c82c2-133">Read-only</span></span><br/> | <span data-ttu-id="c82c2-134">Nome della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="c82c2-134">The name of the serial port.</span></span><br/>                                                                           |
| [<span data-ttu-id="c82c2-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c82c2-135">**Type**</span></span>](ivmserialport-type.md)<br/>                             | <span data-ttu-id="c82c2-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c82c2-136">Read-only</span></span><br/> | <span data-ttu-id="c82c2-137">Tipo della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="c82c2-137">The type of the serial port.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="c82c2-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c82c2-138">Requirements</span></span>



| <span data-ttu-id="c82c2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c82c2-139">Requirement</span></span> | <span data-ttu-id="c82c2-140">Valore</span><span class="sxs-lookup"><span data-stu-id="c82c2-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c82c2-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c82c2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c82c2-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c82c2-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c82c2-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c82c2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c82c2-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c82c2-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c82c2-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c82c2-145">End of client support</span></span><br/>    | <span data-ttu-id="c82c2-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c82c2-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c82c2-147">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c82c2-147">Product</span></span><br/>                  | <span data-ttu-id="c82c2-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c82c2-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c82c2-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c82c2-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c82c2-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c82c2-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c82c2-151">IID</span><span class="sxs-lookup"><span data-stu-id="c82c2-151">IID</span></span><br/>                      | <span data-ttu-id="c82c2-152">IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="c82c2-152">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



 

