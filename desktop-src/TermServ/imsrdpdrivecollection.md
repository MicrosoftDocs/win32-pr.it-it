---
title: Interfaccia IMsRdpDriveCollection
description: Rappresenta una raccolta di oggetti unità.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDriveCollection Servizi Desktop remoto
- Interfaccia IMsRdpDriveCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477735"
---
# <a name="imsrdpdrivecollection-interface"></a><span data-ttu-id="ab80f-105">Interfaccia IMsRdpDriveCollection</span><span class="sxs-lookup"><span data-stu-id="ab80f-105">IMsRdpDriveCollection interface</span></span>

<span data-ttu-id="ab80f-106">Rappresenta una raccolta di oggetti unità.</span><span class="sxs-lookup"><span data-stu-id="ab80f-106">Represents a collection of drive objects.</span></span>

## <a name="members"></a><span data-ttu-id="ab80f-107">Membri</span><span class="sxs-lookup"><span data-stu-id="ab80f-107">Members</span></span>

<span data-ttu-id="ab80f-108">L'interfaccia **IMsRdpDriveCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ab80f-108">The **IMsRdpDriveCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ab80f-109">**IMsRdpDriveCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ab80f-109">**IMsRdpDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="ab80f-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ab80f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ab80f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab80f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ab80f-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ab80f-112">Methods</span></span>

<span data-ttu-id="ab80f-113">L'interfaccia **IMsRdpDriveCollection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ab80f-113">The **IMsRdpDriveCollection** interface has these methods.</span></span>



| <span data-ttu-id="ab80f-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="ab80f-114">Method</span></span>                                                     | <span data-ttu-id="ab80f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab80f-115">Description</span></span>                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="ab80f-116">**RescanDrives**</span><span class="sxs-lookup"><span data-stu-id="ab80f-116">**RescanDrives**</span></span>](imsrdpdrivecollection-rescandrives.md) | <span data-ttu-id="ab80f-117">Aggiorna l'elenco di oggetti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="ab80f-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ab80f-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab80f-118">Properties</span></span>

<span data-ttu-id="ab80f-119">L'interfaccia **IMsRdpDriveCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ab80f-119">The **IMsRdpDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="ab80f-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab80f-120">Property</span></span>                                                              | <span data-ttu-id="ab80f-121">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ab80f-121">Access type</span></span>          | <span data-ttu-id="ab80f-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab80f-122">Description</span></span>                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="ab80f-123">**DriveByIndex**</span><span class="sxs-lookup"><span data-stu-id="ab80f-123">**DriveByIndex**</span></span>](imsrdpdrivecollection-drivebyindex.md)<br/> | <span data-ttu-id="ab80f-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab80f-124">Read-only</span></span><br/> | <span data-ttu-id="ab80f-125">Recupera l'unità in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="ab80f-125">Retrieves the drive at the specified index.</span></span><br/>       |
| [<span data-ttu-id="ab80f-126">**DriveCount**</span><span class="sxs-lookup"><span data-stu-id="ab80f-126">**DriveCount**</span></span>](imsrdpdrivecollection-drivecount.md)<br/>     | <span data-ttu-id="ab80f-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab80f-127">Read-only</span></span><br/> | <span data-ttu-id="ab80f-128">Recupera il numero di oggetti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="ab80f-128">Retrieves the count of objects in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ab80f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab80f-129">Requirements</span></span>



| <span data-ttu-id="ab80f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab80f-130">Requirement</span></span> | <span data-ttu-id="ab80f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ab80f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab80f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab80f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ab80f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab80f-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ab80f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab80f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ab80f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab80f-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ab80f-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ab80f-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab80f-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab80f-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ab80f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ab80f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab80f-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab80f-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ab80f-140">IID</span><span class="sxs-lookup"><span data-stu-id="ab80f-140">IID</span></span><br/>                      | <span data-ttu-id="ab80f-141">IID \_ IMsRdpDriveCollection è definito come 7ff17599-da2c-4677-Ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="ab80f-141">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab80f-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab80f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab80f-143">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="ab80f-143">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="ab80f-144">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="ab80f-144">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

