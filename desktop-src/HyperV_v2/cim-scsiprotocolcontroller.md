---
description: Rappresenta un controller di protocollo che gestisce un'interfaccia SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: Classe CIM_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307769"
---
# <a name="cim_scsiprotocolcontroller-class"></a><span data-ttu-id="1111b-103">CIM \_ SCSIProtocolController (classe)</span><span class="sxs-lookup"><span data-stu-id="1111b-103">CIM\_SCSIProtocolController class</span></span>

<span data-ttu-id="1111b-104">Rappresenta un controller di protocollo che gestisce un'interfaccia SCSI.</span><span class="sxs-lookup"><span data-stu-id="1111b-104">Represents a protocol controller that manages a SCSI interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1111b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1111b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="1111b-106">Members</span><span class="sxs-lookup"><span data-stu-id="1111b-106">Members</span></span>

<span data-ttu-id="1111b-107">La classe **CIM \_ SCSIProtocolController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1111b-107">The **CIM\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="1111b-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1111b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1111b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1111b-109">Properties</span></span>

<span data-ttu-id="1111b-110">La classe **CIM \_ SCSIProtocolController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1111b-110">The **CIM\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1111b-111">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="1111b-111">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1111b-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1111b-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1111b-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1111b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1111b-114">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Nome**","**CIM \_ SCSIProtocolController**.**OtherNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="1111b-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="1111b-115">Formato della proprietà **Name** del **\_ SCSIProtocolController CIM**.</span><span class="sxs-lookup"><span data-stu-id="1111b-115">The format of the **Name** property of the **CIM\_SCSIProtocolController**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1111b-116">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="1111b-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1111b-117">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="1111b-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

<span data-ttu-id="1111b-118">**Porta FC WWN** (2)</span><span class="sxs-lookup"><span data-stu-id="1111b-118">**FC Port WWN** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

<span data-ttu-id="1111b-119">**nome iSCSI** (3)</span><span class="sxs-lookup"><span data-stu-id="1111b-119">**iSCSI Name** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1111b-120">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="1111b-120">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1111b-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1111b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1111b-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1111b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1111b-123">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Nome**","**CIM \_ SCSIProtocolController**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="1111b-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="1111b-124">Descrizione della proprietà **NameFormat** quando **NameFormat** è impostato su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="1111b-124">A description of the **NameFormat** property when **NameFormat** is set to "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1111b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1111b-125">Requirements</span></span>



| <span data-ttu-id="1111b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1111b-126">Requirement</span></span> | <span data-ttu-id="1111b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1111b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1111b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1111b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1111b-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1111b-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1111b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1111b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1111b-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1111b-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1111b-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1111b-132">Namespace</span></span><br/>                | <span data-ttu-id="1111b-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1111b-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1111b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1111b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1111b-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1111b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1111b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1111b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1111b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1111b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1111b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1111b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1111b-139">**\_PROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="1111b-139">**CIM\_ProtocolController**</span></span>](cim-protocolcontroller.md)
</dt> </dl>

 

