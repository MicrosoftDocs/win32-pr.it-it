---
description: Gestisce i dispositivi assegnabili in un computer host.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319523"
---
# <a name="msvm_assignabledeviceservice-class"></a><span data-ttu-id="294d1-103">\_Classe MSVM AssignableDeviceService</span><span class="sxs-lookup"><span data-stu-id="294d1-103">Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="294d1-104">Gestisce i dispositivi assegnabili in un computer host.</span><span class="sxs-lookup"><span data-stu-id="294d1-104">Manages the assignable devices on a host computer system.</span></span>

<span data-ttu-id="294d1-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="294d1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="294d1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="294d1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="294d1-107">Members</span><span class="sxs-lookup"><span data-stu-id="294d1-107">Members</span></span>

<span data-ttu-id="294d1-108">La **classe \_ AssignableDeviceService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="294d1-108">The **Msvm\_AssignableDeviceService** class has these types of members:</span></span>

-   [<span data-ttu-id="294d1-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="294d1-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="294d1-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="294d1-110">Methods</span></span>

<span data-ttu-id="294d1-111">La **classe \_ AssignableDeviceService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="294d1-111">The **Msvm\_AssignableDeviceService** class has these methods.</span></span>



| <span data-ttu-id="294d1-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="294d1-112">Method</span></span>                                                                                    | <span data-ttu-id="294d1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="294d1-113">Description</span></span>                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="294d1-114">**DismountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="294d1-114">**DismountAssignableDevice**</span></span>](msvm-assignabledeviceservice-dismountassignabledevice.md) | <span data-ttu-id="294d1-115">Smonta il dispositivo PCI specificato in modo che possa essere assegnato.</span><span class="sxs-lookup"><span data-stu-id="294d1-115">Dismounts the specified PCI device so that it can be assigned.</span></span><br/>                      |
| [<span data-ttu-id="294d1-116">**MountAssignableDevice**</span><span class="sxs-lookup"><span data-stu-id="294d1-116">**MountAssignableDevice**</span></span>](msvm-assignabledeviceservice-mountassignabledevice.md)       | <span data-ttu-id="294d1-117">Monta il dispositivo PCI specificato in modo che possa essere utilizzato dal computer host.</span><span class="sxs-lookup"><span data-stu-id="294d1-117">Mounts the specified PCI device so that it can be used by the host computer system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="294d1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="294d1-118">Requirements</span></span>



| <span data-ttu-id="294d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="294d1-119">Requirement</span></span> | <span data-ttu-id="294d1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="294d1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="294d1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="294d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="294d1-122">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="294d1-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="294d1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="294d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="294d1-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="294d1-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="294d1-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="294d1-125">Namespace</span></span><br/>                | <span data-ttu-id="294d1-126">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="294d1-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="294d1-127">MOF</span><span class="sxs-lookup"><span data-stu-id="294d1-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="294d1-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="294d1-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="294d1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="294d1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="294d1-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="294d1-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="294d1-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="294d1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="294d1-132">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="294d1-132">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




