---
description: Rappresenta un gruppo di controller che controllano l'operazione e la funzione dei dispositivi che avviano i protocolli.
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: Classe CIM_ProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27372bc57ad36f37689d75b3963ec0c4b1106956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305659"
---
# <a name="cim_protocolcontroller-class"></a><span data-ttu-id="cd183-103">CIM \_ ProtocolController (classe)</span><span class="sxs-lookup"><span data-stu-id="cd183-103">CIM\_ProtocolController class</span></span>

<span data-ttu-id="cd183-104">Rappresenta un gruppo di controller che controllano l'operazione e la funzione dei dispositivi che avviano i protocolli.</span><span class="sxs-lookup"><span data-stu-id="cd183-104">Represents a group of controllers that control the operation and function of devices that initiate protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd183-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd183-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a><span data-ttu-id="cd183-106">Members</span><span class="sxs-lookup"><span data-stu-id="cd183-106">Members</span></span>

<span data-ttu-id="cd183-107">La classe **CIM \_ ProtocolController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cd183-107">The **CIM\_ProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="cd183-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd183-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd183-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd183-109">Properties</span></span>

<span data-ttu-id="cd183-110">La classe **CIM \_ ProtocolController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd183-110">The **CIM\_ProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd183-111">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="cd183-111">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd183-112">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd183-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd183-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd183-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd183-114">Numero massimo di unità che possono essere controllate o accessibili tramite il controller di protocollo.</span><span class="sxs-lookup"><span data-stu-id="cd183-114">The maximum number of units that can be controlled by or accessed through the protocol controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd183-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd183-115">Requirements</span></span>



| <span data-ttu-id="cd183-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd183-116">Requirement</span></span> | <span data-ttu-id="cd183-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cd183-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd183-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd183-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd183-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd183-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cd183-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd183-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd183-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd183-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cd183-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd183-122">Namespace</span></span><br/>                | <span data-ttu-id="cd183-123">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cd183-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd183-124">MOF</span><span class="sxs-lookup"><span data-stu-id="cd183-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd183-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd183-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd183-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cd183-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd183-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd183-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd183-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd183-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd183-129">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="cd183-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




