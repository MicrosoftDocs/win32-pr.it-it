---
description: Rappresenta il servizio VSS Guest. Viene utilizzato per eseguire query sulle informazioni del cluster guest dall'host Hyper-V.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Classe Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342771"
---
# <a name="msvm_vssservice-class"></a><span data-ttu-id="8fb72-104">\_Classe MSVM VssService</span><span class="sxs-lookup"><span data-stu-id="8fb72-104">Msvm\_VssService class</span></span>

<span data-ttu-id="8fb72-105">Rappresenta il servizio VSS Guest.</span><span class="sxs-lookup"><span data-stu-id="8fb72-105">Represents the guest VSS service.</span></span> <span data-ttu-id="8fb72-106">Viene utilizzato per eseguire query sulle informazioni del cluster guest dall'host Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8fb72-106">It is used for querying guest cluster information from the Hyper-V host.</span></span>

<span data-ttu-id="8fb72-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8fb72-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb72-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fb72-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a><span data-ttu-id="8fb72-109">Members</span><span class="sxs-lookup"><span data-stu-id="8fb72-109">Members</span></span>

<span data-ttu-id="8fb72-110">La **classe \_ VssService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8fb72-110">The **Msvm\_VssService** class has these types of members:</span></span>

-   [<span data-ttu-id="8fb72-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="8fb72-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8fb72-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="8fb72-112">Methods</span></span>

<span data-ttu-id="8fb72-113">La **classe \_ VssService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8fb72-113">The **Msvm\_VssService** class has these methods.</span></span>



| <span data-ttu-id="8fb72-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="8fb72-114">Method</span></span>                                                                               | <span data-ttu-id="8fb72-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fb72-115">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="8fb72-116">**QueryGuestClusterInformation**</span><span class="sxs-lookup"><span data-stu-id="8fb72-116">**QueryGuestClusterInformation**</span></span>](msvm-vssservice-queryguestclusterinformation.md) | <span data-ttu-id="8fb72-117">Esecuzione di query sulle informazioni del cluster dall'host Hyper-V al Guest.</span><span class="sxs-lookup"><span data-stu-id="8fb72-117">Querying cluster information from the Hyper-V host to the guest.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8fb72-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fb72-118">Requirements</span></span>



| <span data-ttu-id="8fb72-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb72-119">Requirement</span></span> | <span data-ttu-id="8fb72-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb72-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb72-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fb72-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb72-122">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8fb72-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8fb72-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fb72-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb72-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8fb72-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8fb72-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8fb72-125">Namespace</span></span><br/>                | <span data-ttu-id="8fb72-126">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8fb72-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8fb72-127">MOF</span><span class="sxs-lookup"><span data-stu-id="8fb72-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fb72-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fb72-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fb72-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8fb72-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fb72-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8fb72-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8fb72-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fb72-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb72-132">**\_GuestService MSVM**</span><span class="sxs-lookup"><span data-stu-id="8fb72-132">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




