---
description: Relazione che indica che due o più dispositivi sono connessi tra loro.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: Classe CIM_DeviceConnection (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308357"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a><span data-ttu-id="9ff76-103">Classe CIM_DeviceConnection (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="9ff76-103">CIM_DeviceConnection class (Hyper-V management)</span></span>

<span data-ttu-id="9ff76-104">Relazione che indica che due o più dispositivi sono connessi tra loro.</span><span class="sxs-lookup"><span data-stu-id="9ff76-104">A relationship that indicates that two or more devices are connected together.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff76-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ff76-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a><span data-ttu-id="9ff76-106">Members</span><span class="sxs-lookup"><span data-stu-id="9ff76-106">Members</span></span>

<span data-ttu-id="9ff76-107">La classe **CIM \_ DeviceConnection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9ff76-107">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="9ff76-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9ff76-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ff76-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9ff76-109">Properties</span></span>

<span data-ttu-id="9ff76-110">La classe **CIM \_ DeviceConnection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9ff76-110">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ff76-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9ff76-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff76-112">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="9ff76-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9ff76-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ff76-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff76-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="9ff76-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9ff76-115">Un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ff76-115">A device.</span></span>

</dd> <dt>

<span data-ttu-id="9ff76-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="9ff76-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff76-117">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="9ff76-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9ff76-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ff76-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff76-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="9ff76-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9ff76-120">Un secondo dispositivo connesso all'altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ff76-120">A second device that is connected to the other device.</span></span>

</dd> <dt>

<span data-ttu-id="9ff76-121">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="9ff76-121">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff76-122">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ff76-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ff76-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ff76-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff76-124">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Associazione porta bus DMTF \| 001,3 "), **punito** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="9ff76-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.3"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="9ff76-125">Quando sono possibili più larghezze di dati del bus e della connessione, la proprietà NegotiatedDataWidth definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="9ff76-125">When several bus and connection data widths are possible, the NegotiatedDataWidth property defines the one that is in use between the Devices.</span></span> <span data-ttu-id="9ff76-126">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="9ff76-126">Data width is specified in bits.</span></span> <span data-ttu-id="9ff76-127">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o non sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="9ff76-127">If data width is not negotiated, or if this information is not available or not important to Device management, the property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9ff76-128">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="9ff76-128">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff76-129">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ff76-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ff76-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9ff76-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff76-131">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Associazione porta bus DMTF \| 001,2 "), **punito** (" bit/secondo ")</span><span class="sxs-lookup"><span data-stu-id="9ff76-131">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.2"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="9ff76-132">Quando sono possibili più velocità di connessione e bus, questa proprietà definisce la velocità in uso tra i dispositivi, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="9ff76-132">When several bus and connection speeds are possible, this property defines the speed that is in use between the devices, in bits per second.</span></span> <span data-ttu-id="9ff76-133">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o non sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su "0".</span><span class="sxs-lookup"><span data-stu-id="9ff76-133">If connection or bus speeds are not negotiated, or if this information is not available, or not important to device management, the property should be set to "0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ff76-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ff76-134">Requirements</span></span>



| <span data-ttu-id="9ff76-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ff76-135">Requirement</span></span> | <span data-ttu-id="9ff76-136">Valore</span><span class="sxs-lookup"><span data-stu-id="9ff76-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff76-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ff76-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff76-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9ff76-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9ff76-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ff76-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff76-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ff76-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9ff76-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9ff76-141">Namespace</span></span><br/>                | <span data-ttu-id="9ff76-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9ff76-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9ff76-143">MOF</span><span class="sxs-lookup"><span data-stu-id="9ff76-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ff76-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ff76-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ff76-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff76-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff76-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9ff76-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9ff76-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ff76-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff76-148">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="9ff76-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

