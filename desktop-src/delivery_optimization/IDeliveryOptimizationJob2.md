---
title: Interfaccia IDeliveryOptimizationJob2
description: 'Altre informazioni su: interfaccia IDeliveryOptimizationJob2'
keywords:
- Interfaccia IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305008"
---
# <a name="ideliveryoptimizationjob2-interface"></a><span data-ttu-id="a5edb-104">Interfaccia IDeliveryOptimizationJob2</span><span class="sxs-lookup"><span data-stu-id="a5edb-104">IDeliveryOptimizationJob2 interface</span></span>

<span data-ttu-id="a5edb-105">IDeliveryOptimizationJob2 consente di aggiungere un singolo file al processo di download e di recuperare immediatamente il file.</span><span class="sxs-lookup"><span data-stu-id="a5edb-105">The IDeliveryOptimizationJob2 enables adding a single file to the download job, and retrieving the file immediately.</span></span> <span data-ttu-id="a5edb-106">Questa interfaccia supporta anche l'impostazione e il recupero di proprietà facoltative del processo.</span><span class="sxs-lookup"><span data-stu-id="a5edb-106">This interface also supports setting and getting optional job properties.</span></span>

## <a name="members"></a><span data-ttu-id="a5edb-107">Membri</span><span class="sxs-lookup"><span data-stu-id="a5edb-107">Members</span></span>

<span data-ttu-id="a5edb-108">L'interfaccia **IDeliveryOptimizationJob2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a5edb-108">The **IDeliveryOptimizationJob2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a5edb-109">**IDeliveryOptimizationJob2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a5edb-109">**IDeliveryOptimizationJob2** also has these types of members:</span></span>

- [<span data-ttu-id="a5edb-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a5edb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a5edb-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a5edb-111">Methods</span></span>

<span data-ttu-id="a5edb-112">L'interfaccia **IDeliveryOptimizationJob2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a5edb-112">The **IDeliveryOptimizationJob2** interface has these methods.</span></span>

| <span data-ttu-id="a5edb-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="a5edb-113">Method</span></span>                                              | <span data-ttu-id="a5edb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5edb-114">Description</span></span>                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="a5edb-115">**AddFile**</span><span class="sxs-lookup"><span data-stu-id="a5edb-115">**AddFile**</span></span>](ideliveryoptimizationjob2-addfile.md) | <span data-ttu-id="a5edb-116">Il metodo AddFile aggiunge un singolo file a un processo DO esistente.</span><span class="sxs-lookup"><span data-stu-id="a5edb-116">The AddFile method adds a single file to an existing DO job.</span></span>         |
| [<span data-ttu-id="a5edb-117">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="a5edb-117">**GetProperty**</span></span>](ideliveryoptimizationjob2-getproperty.md) | <span data-ttu-id="a5edb-118">Il metodo AddFile aggiunge un singolo file a un processo DO esistente.</span><span class="sxs-lookup"><span data-stu-id="a5edb-118">The AddFile method adds a single file to an existing DO job.</span></span> |
| [<span data-ttu-id="a5edb-119">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="a5edb-119">**SetProperty**</span></span>](ideliveryoptimizationjob2-setproperty.md) | <span data-ttu-id="a5edb-120">Questo metodo non è utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a5edb-120">This method is unused.</span></span>                                       |

## <a name="requirements"></a><span data-ttu-id="a5edb-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5edb-121">Requirements</span></span>

| <span data-ttu-id="a5edb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5edb-122">Requirement</span></span> | <span data-ttu-id="a5edb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a5edb-123">Value</span></span> |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a5edb-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5edb-124">Minimum supported client</span></span> | <span data-ttu-id="a5edb-125">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5edb-125">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="a5edb-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5edb-126">Minimum supported server</span></span> | <span data-ttu-id="a5edb-127">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5edb-127">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="a5edb-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5edb-128">Header</span></span>                   | <span data-ttu-id="a5edb-129">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="a5edb-129">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="a5edb-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a5edb-130">IDL</span></span>                      | <span data-ttu-id="a5edb-131">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="a5edb-131">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="a5edb-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5edb-132">Library</span></span>                  | <span data-ttu-id="a5edb-133">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="a5edb-133">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="a5edb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a5edb-134">DLL</span></span>                      | <span data-ttu-id="a5edb-135">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="a5edb-135">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="a5edb-136">IID</span><span class="sxs-lookup"><span data-stu-id="a5edb-136">IID</span></span>                      | <span data-ttu-id="a5edb-137">IID_IDeliveryOptimizationJob2 viene definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="a5edb-137">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |
