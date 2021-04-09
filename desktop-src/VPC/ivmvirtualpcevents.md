---
title: Interfaccia IVMVirtualPCEvents (VPCCOMInterfaces. h)
description: Definisce l'interfaccia evento in uscita per l'interfaccia IVMVirtualPC.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Interfaccia IVMVirtualPCEvents Virtual PC
- Interfaccia IVMVirtualPCEvents Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048605"
---
# <a name="ivmvirtualpcevents-interface"></a><span data-ttu-id="4186b-105">Interfaccia IVMVirtualPCEvents</span><span class="sxs-lookup"><span data-stu-id="4186b-105">IVMVirtualPCEvents interface</span></span>

<span data-ttu-id="4186b-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4186b-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4186b-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4186b-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4186b-108">Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMVirtualPC**](ivmvirtualpc.md) .</span><span class="sxs-lookup"><span data-stu-id="4186b-108">Defines the outgoing event interface for the [**IVMVirtualPC**](ivmvirtualpc.md) interface.</span></span> <span data-ttu-id="4186b-109">Il client implementa questi metodi per ricevere gli eventi inviati da [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="4186b-109">The client implements these methods to receive events sent from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="members"></a><span data-ttu-id="4186b-110">Membri</span><span class="sxs-lookup"><span data-stu-id="4186b-110">Members</span></span>

<span data-ttu-id="4186b-111">L'interfaccia **IVMVirtualPCEvents** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4186b-111">The **IVMVirtualPCEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4186b-112">**IVMVirtualPCEvents** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4186b-112">**IVMVirtualPCEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="4186b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="4186b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4186b-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="4186b-114">Methods</span></span>

<span data-ttu-id="4186b-115">L'interfaccia **IVMVirtualPCEvents** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4186b-115">The **IVMVirtualPCEvents** interface has these methods.</span></span>



| <span data-ttu-id="4186b-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="4186b-116">Method</span></span>                                                        | <span data-ttu-id="4186b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4186b-117">Description</span></span>                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="4186b-118">**OnEventLogged**</span><span class="sxs-lookup"><span data-stu-id="4186b-118">**OnEventLogged**</span></span>](ivmvirtualpcevents-oneventlogged.md)     | <span data-ttu-id="4186b-119">Riceve la notifica che Windows Virtual PC registra un evento.</span><span class="sxs-lookup"><span data-stu-id="4186b-119">Receives notification that Windows Virtual PC logs an event.</span></span><br/>      |
| [<span data-ttu-id="4186b-120">**OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="4186b-120">**OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md) | <span data-ttu-id="4186b-121">Riceve una notifica che lo stato di una macchina virtuale è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="4186b-121">Receives notification that a virtual machine's state has changed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4186b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4186b-122">Requirements</span></span>



| <span data-ttu-id="4186b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4186b-123">Requirement</span></span> | <span data-ttu-id="4186b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4186b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4186b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4186b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4186b-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4186b-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4186b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4186b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4186b-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4186b-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4186b-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4186b-129">End of client support</span></span><br/>    | <span data-ttu-id="4186b-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4186b-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4186b-131">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4186b-131">Product</span></span><br/>                  | <span data-ttu-id="4186b-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4186b-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4186b-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4186b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4186b-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4186b-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4186b-135">IID</span><span class="sxs-lookup"><span data-stu-id="4186b-135">IID</span></span><br/>                      | <span data-ttu-id="4186b-136">DIID \_ IVMVirtualPCEvents è definito come efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="4186b-136">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



 

