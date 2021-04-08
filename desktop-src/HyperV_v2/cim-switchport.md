---
description: Rappresenta una porta di commutazione che invia e riceve frame di dati.
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: Classe CIM_SwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf63843fc5a246012d3af6a059c897956d6f19b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967554"
---
# <a name="cim_switchport-class"></a><span data-ttu-id="4f488-103">CIM \_ SwitchPort (classe)</span><span class="sxs-lookup"><span data-stu-id="4f488-103">CIM\_SwitchPort class</span></span>

<span data-ttu-id="4f488-104">Rappresenta una porta di commutazione che invia e riceve frame di dati.</span><span class="sxs-lookup"><span data-stu-id="4f488-104">Represents a switch port that sends and receives data frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f488-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f488-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a><span data-ttu-id="4f488-106">Members</span><span class="sxs-lookup"><span data-stu-id="4f488-106">Members</span></span>

<span data-ttu-id="4f488-107">La classe **CIM \_ SwitchPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4f488-107">The **CIM\_SwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="4f488-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f488-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f488-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f488-109">Properties</span></span>

<span data-ttu-id="4f488-110">La classe **CIM \_ SwitchPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4f488-110">The **CIM\_SwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f488-111">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="4f488-111">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f488-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f488-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f488-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f488-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f488-114">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dPort ")</span><span class="sxs-lookup"><span data-stu-id="4f488-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dPort")</span></span>
</dt> </dl>

<span data-ttu-id="4f488-115">Identificatore numerico della porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="4f488-115">The numeric identifier of the switch port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f488-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f488-116">Requirements</span></span>



| <span data-ttu-id="4f488-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f488-117">Requirement</span></span> | <span data-ttu-id="4f488-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4f488-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f488-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f488-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f488-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4f488-120">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4f488-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f488-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f488-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4f488-122">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4f488-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f488-123">Namespace</span></span><br/>                | <span data-ttu-id="4f488-124">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4f488-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4f488-125">MOF</span><span class="sxs-lookup"><span data-stu-id="4f488-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f488-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f488-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f488-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4f488-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f488-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f488-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f488-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f488-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f488-130">**\_PROTOCOLENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="4f488-130">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

