---
description: arresta il servizio.
ms.assetid: 0f9a015d-b895-496a-a4c6-2737c0742746
title: Metodo StartService della classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f76fa9e5069c2a9e19b83a8ab83136879c6657e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319515"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="75cc3-103">Metodo StartService della classe MSVM \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="75cc3-103">StartService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="75cc3-104">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="75cc3-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="75cc3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75cc3-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="75cc3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75cc3-106">Parameters</span></span>

<span data-ttu-id="75cc3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="75cc3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75cc3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75cc3-108">Return value</span></span>

<span data-ttu-id="75cc3-109">Restituisce 0 se ha esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="75cc3-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="75cc3-110">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="75cc3-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75cc3-111">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="75cc3-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="75cc3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75cc3-112">Requirements</span></span>



| <span data-ttu-id="75cc3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="75cc3-113">Requirement</span></span> | <span data-ttu-id="75cc3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="75cc3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75cc3-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75cc3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="75cc3-116">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="75cc3-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="75cc3-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75cc3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="75cc3-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="75cc3-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="75cc3-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="75cc3-119">Namespace</span></span><br/>                | <span data-ttu-id="75cc3-120">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="75cc3-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="75cc3-121">MOF</span><span class="sxs-lookup"><span data-stu-id="75cc3-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75cc3-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75cc3-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75cc3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="75cc3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75cc3-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75cc3-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75cc3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75cc3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75cc3-126">**\_CollectionManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="75cc3-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




