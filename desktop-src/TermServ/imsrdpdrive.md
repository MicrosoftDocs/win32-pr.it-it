---
title: Interfaccia IMsRdpDrive
description: Contiene informazioni su un oggetto unità.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDrive Servizi Desktop remoto
- Interfaccia IMsRdpDrive Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739991"
---
# <a name="imsrdpdrive-interface"></a><span data-ttu-id="e7077-105">Interfaccia IMsRdpDrive</span><span class="sxs-lookup"><span data-stu-id="e7077-105">IMsRdpDrive interface</span></span>

<span data-ttu-id="e7077-106">Contiene informazioni su un oggetto unità.</span><span class="sxs-lookup"><span data-stu-id="e7077-106">Contains information about a drive object.</span></span>

## <a name="members"></a><span data-ttu-id="e7077-107">Membri</span><span class="sxs-lookup"><span data-stu-id="e7077-107">Members</span></span>

<span data-ttu-id="e7077-108">L'interfaccia **IMsRdpDrive** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e7077-108">The **IMsRdpDrive** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e7077-109">**IMsRdpDrive** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e7077-109">**IMsRdpDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="e7077-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7077-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7077-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7077-111">Properties</span></span>

<span data-ttu-id="e7077-112">L'interfaccia **IMsRdpDrive** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e7077-112">The **IMsRdpDrive** interface has these properties.</span></span>



| <span data-ttu-id="e7077-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7077-113">Property</span></span>                                                            | <span data-ttu-id="e7077-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e7077-114">Access type</span></span>           | <span data-ttu-id="e7077-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7077-115">Description</span></span>                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="e7077-116">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e7077-116">**Name**</span></span>](imsrdpdrive-name.md)<br/>                         | <span data-ttu-id="e7077-117">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7077-117">Read-only</span></span><br/>  | <span data-ttu-id="e7077-118">Recupera il nome dell'unità.</span><span class="sxs-lookup"><span data-stu-id="e7077-118">Retrieves the name of the drive.</span></span><br/>              |
| [<span data-ttu-id="e7077-119">**RedirectionState**</span><span class="sxs-lookup"><span data-stu-id="e7077-119">**RedirectionState**</span></span>](imsrdpdrive-redirectionstate.md)<br/> | <span data-ttu-id="e7077-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e7077-120">Read/write</span></span><br/> | <span data-ttu-id="e7077-121">Indica lo stato di reindirizzamento dell'unità.</span><span class="sxs-lookup"><span data-stu-id="e7077-121">Indicates the redirection state of the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e7077-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7077-122">Requirements</span></span>



| <span data-ttu-id="e7077-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7077-123">Requirement</span></span> | <span data-ttu-id="e7077-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e7077-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7077-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7077-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e7077-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7077-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e7077-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7077-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e7077-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7077-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e7077-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e7077-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7077-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7077-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7077-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e7077-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7077-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7077-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7077-133">IID</span><span class="sxs-lookup"><span data-stu-id="e7077-133">IID</span></span><br/>                      | <span data-ttu-id="e7077-134">IID \_ IMsRdpDrive è definito come d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="e7077-134">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="e7077-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7077-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7077-136">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="e7077-136">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="e7077-137">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="e7077-137">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

