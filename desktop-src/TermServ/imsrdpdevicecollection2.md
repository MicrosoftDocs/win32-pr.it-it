---
title: Interfaccia IMsRdpDeviceCollection2
description: Rappresenta una raccolta di oggetti dispositivo. Si tratta di un miglioramento dell'interfaccia IMsRdpDeviceCollection.
ms.assetid: df4d704c-e031-4df1-aed1-11aacf8a6992
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDeviceCollection2 Servizi Desktop remoto
- Interfaccia IMsRdpDeviceCollection2 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea35c0a66ad8bf5d291062eafb7be3ceae4ac58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301986"
---
# <a name="imsrdpdevicecollection2-interface"></a><span data-ttu-id="a0ee7-106">Interfaccia IMsRdpDeviceCollection2</span><span class="sxs-lookup"><span data-stu-id="a0ee7-106">IMsRdpDeviceCollection2 interface</span></span>

<span data-ttu-id="a0ee7-107">Rappresenta una raccolta di oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0ee7-107">Represents a collection of device objects.</span></span> <span data-ttu-id="a0ee7-108">Si tratta di un miglioramento dell'interfaccia [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a0ee7-108">This is an enhancement to the [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="a0ee7-109">Membri</span><span class="sxs-lookup"><span data-stu-id="a0ee7-109">Members</span></span>

<span data-ttu-id="a0ee7-110">L'interfaccia **IMsRdpDeviceCollection2** eredita da [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span><span class="sxs-lookup"><span data-stu-id="a0ee7-110">The **IMsRdpDeviceCollection2** interface inherits from [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span></span> <span data-ttu-id="a0ee7-111">**IMsRdpDeviceCollection2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a0ee7-111">**IMsRdpDeviceCollection2** also has these types of members:</span></span>

-   [<span data-ttu-id="a0ee7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a0ee7-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0ee7-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a0ee7-113">Methods</span></span>

<span data-ttu-id="a0ee7-114">L'interfaccia **IMsRdpDeviceCollection2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a0ee7-114">The **IMsRdpDeviceCollection2** interface has these methods.</span></span>



| <span data-ttu-id="a0ee7-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a0ee7-115">Method</span></span>                                                                         | <span data-ttu-id="a0ee7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0ee7-116">Description</span></span>                                                                                                 |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0ee7-117">**AddDeviceByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="a0ee7-117">**AddDeviceByInstanceId**</span></span>](imsrdpdevicecollection2-adddevicebyinstanceid.md) | <span data-ttu-id="a0ee7-118">Aggiunge un dispositivo non in elenco alla raccolta di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a0ee7-118">Adds an unlisted device to the device collection.</span></span><br/>                                                |
| [<span data-ttu-id="a0ee7-119">**RedirectNow**</span><span class="sxs-lookup"><span data-stu-id="a0ee7-119">**RedirectNow**</span></span>](imsrdpdevicecollection2-redirectnow.md)                     | <span data-ttu-id="a0ee7-120">Impone il reindirizzamento o la rimozione dei dispositivi selezionati o deselezionati dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="a0ee7-120">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a0ee7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0ee7-121">Requirements</span></span>



| <span data-ttu-id="a0ee7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0ee7-122">Requirement</span></span> | <span data-ttu-id="a0ee7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a0ee7-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ee7-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0ee7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ee7-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0ee7-125">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="a0ee7-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0ee7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ee7-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0ee7-127">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="a0ee7-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a0ee7-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0ee7-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0ee7-129"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="a0ee7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a0ee7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0ee7-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0ee7-131"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="a0ee7-132">IID</span><span class="sxs-lookup"><span data-stu-id="a0ee7-132">IID</span></span><br/>                      | <span data-ttu-id="a0ee7-133">IID \_ IMsRdpDeviceCollection2 è definito come e0e5d68a-f2e7-4350-ADFE-ac0e08d74de0</span><span class="sxs-lookup"><span data-stu-id="a0ee7-133">IID\_IMsRdpDeviceCollection2 is defined as e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span></span><br/> |



 

 





