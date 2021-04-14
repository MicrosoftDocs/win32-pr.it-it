---
title: Interfaccia IVMDVDDriveEvents (VPCCOMInterfaces. h)
description: Definisce l'interfaccia evento in uscita per l'interfaccia IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Interfaccia IVMDVDDriveEvents Virtual PC
- Interfaccia IVMDVDDriveEvents Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479012"
---
# <a name="ivmdvddriveevents-interface"></a><span data-ttu-id="00971-105">Interfaccia IVMDVDDriveEvents</span><span class="sxs-lookup"><span data-stu-id="00971-105">IVMDVDDriveEvents interface</span></span>

<span data-ttu-id="00971-106">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="00971-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="00971-107">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="00971-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="00971-108">Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="00971-108">Defines the outgoing event interface for the [**IVMDVDDrive**](ivmdvddrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="00971-109">Membri</span><span class="sxs-lookup"><span data-stu-id="00971-109">Members</span></span>

<span data-ttu-id="00971-110">L'interfaccia **IVMDVDDriveEvents** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="00971-110">The **IVMDVDDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="00971-111">**IVMDVDDriveEvents** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="00971-111">**IVMDVDDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="00971-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="00971-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="00971-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="00971-113">Methods</span></span>

<span data-ttu-id="00971-114">L'interfaccia **IVMDVDDriveEvents** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="00971-114">The **IVMDVDDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="00971-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="00971-115">Method</span></span>                                                   | <span data-ttu-id="00971-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00971-116">Description</span></span>                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="00971-117">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="00971-117">**OnMediaEject**</span></span>](ivmdvddriveevents-onmediaeject.md)   | <span data-ttu-id="00971-118">Riceve una notifica che segnala che il supporto è stato espulso dall'unità.</span><span class="sxs-lookup"><span data-stu-id="00971-118">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="00971-119">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="00971-119">**OnMediaInsert**</span></span>](ivmdvddriveevents-onmediainsert.md) | <span data-ttu-id="00971-120">Riceve la notifica che i supporti sono stati inseriti nell'unità.</span><span class="sxs-lookup"><span data-stu-id="00971-120">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="00971-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00971-121">Requirements</span></span>



| <span data-ttu-id="00971-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="00971-122">Requirement</span></span> | <span data-ttu-id="00971-123">Valore</span><span class="sxs-lookup"><span data-stu-id="00971-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="00971-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00971-124">Minimum supported client</span></span><br/> | <span data-ttu-id="00971-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="00971-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00971-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00971-126">Minimum supported server</span></span><br/> | <span data-ttu-id="00971-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="00971-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="00971-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="00971-128">End of client support</span></span><br/>    | <span data-ttu-id="00971-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="00971-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="00971-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="00971-130">Product</span></span><br/>                  | <span data-ttu-id="00971-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="00971-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="00971-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00971-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="00971-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="00971-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="00971-134">IID</span><span class="sxs-lookup"><span data-stu-id="00971-134">IID</span></span><br/>                      | <span data-ttu-id="00971-135">DIID \_ IVMDVDDriveEvents è definito come c2a7d8e9-E76C-4EB8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="00971-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



 

