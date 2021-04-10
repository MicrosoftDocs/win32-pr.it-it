---
description: Associa una porta seriale a un controller seriale.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Classe Msvm_SerialPortOnSerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879694"
---
# <a name="msvm_serialportonserialcontroller-class"></a><span data-ttu-id="9da45-103">\_Classe MSVM SerialPortOnSerialController</span><span class="sxs-lookup"><span data-stu-id="9da45-103">Msvm\_SerialPortOnSerialController class</span></span>

<span data-ttu-id="9da45-104">Associa una porta seriale a un controller seriale.</span><span class="sxs-lookup"><span data-stu-id="9da45-104">Associates a serial port with a serial controller.</span></span>

<span data-ttu-id="9da45-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9da45-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da45-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9da45-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9da45-107">Members</span><span class="sxs-lookup"><span data-stu-id="9da45-107">Members</span></span>

<span data-ttu-id="9da45-108">La **classe \_ SerialPortOnSerialController di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9da45-108">The **Msvm\_SerialPortOnSerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="9da45-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9da45-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9da45-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9da45-110">Properties</span></span>

<span data-ttu-id="9da45-111">La **classe \_ SerialPortOnSerialController di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9da45-111">The **Msvm\_SerialPortOnSerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9da45-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9da45-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9da45-113">Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="9da45-113">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="9da45-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9da45-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9da45-115">Controller seriale a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="9da45-115">The serial controller to which the port is connected.</span></span> <span data-ttu-id="9da45-116">Questa proprietà viene ereditata da [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="9da45-116">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> <dt>

<span data-ttu-id="9da45-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="9da45-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9da45-118">Tipo di dati: **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9da45-118">Data type: **[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="9da45-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9da45-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9da45-120">Porta del controller seriale.</span><span class="sxs-lookup"><span data-stu-id="9da45-120">The port of the serial controller.</span></span> <span data-ttu-id="9da45-121">Questa proprietà viene ereditata da [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="9da45-121">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9da45-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="9da45-122">Remarks</span></span>

<span data-ttu-id="9da45-123">L'accesso alla **classe \_ SerialPortOnSerialController di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="9da45-123">Access to the **Msvm\_SerialPortOnSerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9da45-124">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9da45-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9da45-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9da45-125">Requirements</span></span>



| <span data-ttu-id="9da45-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9da45-126">Requirement</span></span> | <span data-ttu-id="9da45-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9da45-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da45-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9da45-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9da45-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9da45-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9da45-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9da45-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9da45-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9da45-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9da45-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9da45-132">Namespace</span></span><br/>                | <span data-ttu-id="9da45-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9da45-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9da45-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9da45-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9da45-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9da45-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9da45-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9da45-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9da45-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9da45-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9da45-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9da45-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da45-139">**\_PORTONDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9da45-139">**CIM\_PortOnDevice**</span></span>](cim-portondevice.md)
</dt> <dt>

[<span data-ttu-id="9da45-140">**\_PORTONDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9da45-140">**CIM\_PortOnDevice**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[<span data-ttu-id="9da45-141">Classi di dispositivi seriali</span><span class="sxs-lookup"><span data-stu-id="9da45-141">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

