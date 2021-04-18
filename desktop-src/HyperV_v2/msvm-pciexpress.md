---
description: Rappresenta lo stato della porta PCI Express.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Classe Msvm_PciExpress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7534d09c9c0f3825ca462c342747caa17c8de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318318"
---
# <a name="msvm_pciexpress-class"></a><span data-ttu-id="c5e14-103">\_Classe MSVM per</span><span class="sxs-lookup"><span data-stu-id="c5e14-103">Msvm\_PciExpress class</span></span>

<span data-ttu-id="c5e14-104">Rappresenta lo stato della porta PCI Express.</span><span class="sxs-lookup"><span data-stu-id="c5e14-104">Represents the state of the PCI Express port.</span></span>

<span data-ttu-id="c5e14-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c5e14-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e14-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5e14-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a><span data-ttu-id="c5e14-107">Members</span><span class="sxs-lookup"><span data-stu-id="c5e14-107">Members</span></span>

<span data-ttu-id="c5e14-108">La **classe \_ per di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c5e14-108">The **Msvm\_PciExpress** class has these types of members:</span></span>

-   [<span data-ttu-id="c5e14-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5e14-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5e14-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5e14-110">Properties</span></span>

<span data-ttu-id="c5e14-111">La **classe \_ per di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5e14-111">The **Msvm\_PciExpress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5e14-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="c5e14-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5e14-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c5e14-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5e14-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5e14-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5e14-115">Stringa contenente il percorso dell'istanza del dispositivo che identifica il dispositivo PCI Express virtuale del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5e14-115">A string containing the device instance path that identifies the device virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="c5e14-116">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="c5e14-116">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5e14-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5e14-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5e14-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5e14-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5e14-119">Numero di funzione del dispositivo PCI Express virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5e14-119">The function number of the virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="c5e14-120">**LocationPath**</span><span class="sxs-lookup"><span data-stu-id="c5e14-120">**LocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5e14-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c5e14-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5e14-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5e14-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5e14-123">Stringa contenente il percorso del dispositivo che identifica il dispositivo PCI Express virtuale del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5e14-123">A string containing the device location path that identifies the device virtual PCI Express device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5e14-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5e14-124">Requirements</span></span>



| <span data-ttu-id="c5e14-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e14-125">Requirement</span></span> | <span data-ttu-id="c5e14-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c5e14-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e14-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5e14-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e14-128">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5e14-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c5e14-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5e14-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e14-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c5e14-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c5e14-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c5e14-131">Namespace</span></span><br/>                | <span data-ttu-id="c5e14-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c5e14-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c5e14-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c5e14-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5e14-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5e14-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5e14-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c5e14-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5e14-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5e14-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5e14-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5e14-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e14-138">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c5e14-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




