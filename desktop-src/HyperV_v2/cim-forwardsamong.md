---
description: Rappresenta un'associazione in cui gli endpoint del protocollo dipendono da un servizio di inoltre per l'invio dei dati.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: Classe CIM_ForwardsAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b584f6472d8fbe3eb738d87652b796d9bb617f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305669"
---
# <a name="cim_forwardsamong-class"></a><span data-ttu-id="2b3c5-103">CIM \_ ForwardsAmong (classe)</span><span class="sxs-lookup"><span data-stu-id="2b3c5-103">CIM\_ForwardsAmong class</span></span>

<span data-ttu-id="2b3c5-104">Rappresenta un'associazione in cui gli endpoint del protocollo dipendono da un servizio di inoltre per l'invio dei dati.</span><span class="sxs-lookup"><span data-stu-id="2b3c5-104">Represents an association in which protocol endpoints depend on a forwarding service to forward data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b3c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b3c5-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2b3c5-106">Members</span><span class="sxs-lookup"><span data-stu-id="2b3c5-106">Members</span></span>

<span data-ttu-id="2b3c5-107">La classe **CIM \_ ForwardsAmong** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2b3c5-107">The **CIM\_ForwardsAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="2b3c5-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b3c5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b3c5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b3c5-109">Properties</span></span>

<span data-ttu-id="2b3c5-110">La classe **CIM \_ ForwardsAmong** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b3c5-110">The **CIM\_ForwardsAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b3c5-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2b3c5-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3c5-112">Tipo di dati: **CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="2b3c5-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="2b3c5-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b3c5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b3c5-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="2b3c5-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2b3c5-115">Gli endpoint del protocollo inviano e ricevono i dati inoltrati.</span><span class="sxs-lookup"><span data-stu-id="2b3c5-115">The protocol endpoints send and receive the forwarded data.</span></span>

</dd> <dt>

<span data-ttu-id="2b3c5-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="2b3c5-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b3c5-117">Tipo di dati: **CIM \_ ForwardingService**</span><span class="sxs-lookup"><span data-stu-id="2b3c5-117">Data type: **CIM\_ForwardingService**</span></span>
</dt> <dt>

<span data-ttu-id="2b3c5-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b3c5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b3c5-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="2b3c5-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2b3c5-120">Servizio di invio che invia i dati.</span><span class="sxs-lookup"><span data-stu-id="2b3c5-120">The forwarding service that forwards the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b3c5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b3c5-121">Requirements</span></span>



| <span data-ttu-id="2b3c5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b3c5-122">Requirement</span></span> | <span data-ttu-id="2b3c5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2b3c5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3c5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b3c5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2b3c5-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2b3c5-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2b3c5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b3c5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2b3c5-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2b3c5-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2b3c5-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2b3c5-128">Namespace</span></span><br/>                | <span data-ttu-id="2b3c5-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2b3c5-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2b3c5-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2b3c5-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b3c5-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b3c5-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b3c5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2b3c5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b3c5-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b3c5-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b3c5-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b3c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b3c5-135">**\_SERVICESAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="2b3c5-135">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> </dl>

 

