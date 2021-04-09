---
title: Interfaccia IVMFloppyDriveEvents (VPCCOMInterfaces. h)
description: Definisce l'interfaccia evento in uscita per l'interfaccia IVMFloppyDrive. Il client implementa questi metodi per ricevere gli eventi inviati da IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Interfaccia IVMFloppyDriveEvents Virtual PC
- Interfaccia IVMFloppyDriveEvents Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121358"
---
# <a name="ivmfloppydriveevents-interface"></a><span data-ttu-id="f2c32-106">Interfaccia IVMFloppyDriveEvents</span><span class="sxs-lookup"><span data-stu-id="f2c32-106">IVMFloppyDriveEvents interface</span></span>

<span data-ttu-id="f2c32-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2c32-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f2c32-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f2c32-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f2c32-109">Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMFloppyDrive**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c32-109">Defines the outgoing event interface for the [**IVMFloppyDrive**](ivmfloppydrive.md) interface.</span></span> <span data-ttu-id="f2c32-110">Il client implementa questi metodi per ricevere gli eventi inviati da **IVMFloppyDrive**.</span><span class="sxs-lookup"><span data-stu-id="f2c32-110">The client implements these methods to receive events sent from **IVMFloppyDrive**.</span></span>

## <a name="members"></a><span data-ttu-id="f2c32-111">Membri</span><span class="sxs-lookup"><span data-stu-id="f2c32-111">Members</span></span>

<span data-ttu-id="f2c32-112">L'interfaccia **IVMFloppyDriveEvents** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="f2c32-112">The **IVMFloppyDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f2c32-113">**IVMFloppyDriveEvents** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f2c32-113">**IVMFloppyDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="f2c32-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="f2c32-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f2c32-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="f2c32-115">Methods</span></span>

<span data-ttu-id="f2c32-116">L'interfaccia **IVMFloppyDriveEvents** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f2c32-116">The **IVMFloppyDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="f2c32-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="f2c32-117">Method</span></span>                                                      | <span data-ttu-id="f2c32-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2c32-118">Description</span></span>                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="f2c32-119">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="f2c32-119">**OnMediaEject**</span></span>](ivmfloppydriveevents-onmediaeject.md)   | <span data-ttu-id="f2c32-120">Riceve una notifica che segnala che il supporto è stato espulso dall'unità.</span><span class="sxs-lookup"><span data-stu-id="f2c32-120">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="f2c32-121">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="f2c32-121">**OnMediaInsert**</span></span>](ivmfloppydriveevents-onmediainsert.md) | <span data-ttu-id="f2c32-122">Riceve la notifica che i supporti sono stati inseriti nell'unità.</span><span class="sxs-lookup"><span data-stu-id="f2c32-122">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f2c32-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2c32-123">Requirements</span></span>



| <span data-ttu-id="f2c32-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2c32-124">Requirement</span></span> | <span data-ttu-id="f2c32-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f2c32-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c32-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2c32-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f2c32-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f2c32-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2c32-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2c32-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f2c32-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f2c32-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f2c32-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f2c32-130">End of client support</span></span><br/>    | <span data-ttu-id="f2c32-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2c32-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f2c32-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f2c32-132">Product</span></span><br/>                  | <span data-ttu-id="f2c32-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f2c32-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f2c32-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2c32-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2c32-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2c32-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f2c32-136">IID</span><span class="sxs-lookup"><span data-stu-id="f2c32-136">IID</span></span><br/>                      | <span data-ttu-id="f2c32-137">DIID \_ IVMFloppyDriveEvents è definito come a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="f2c32-137">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



 

