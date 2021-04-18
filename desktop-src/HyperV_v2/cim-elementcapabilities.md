---
description: Rappresenta un'associazione tra un elemento gestito e le relative funzionalità.
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: Classe CIM_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308345"
---
# <a name="cim_elementcapabilities-class"></a><span data-ttu-id="48851-103">CIM \_ ElementCapabilities (classe)</span><span class="sxs-lookup"><span data-stu-id="48851-103">CIM\_ElementCapabilities class</span></span>

<span data-ttu-id="48851-104">Rappresenta un'associazione tra un elemento gestito e le relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="48851-104">Represents an association between a managed element and its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="48851-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48851-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="48851-106">Members</span><span class="sxs-lookup"><span data-stu-id="48851-106">Members</span></span>

<span data-ttu-id="48851-107">La classe **CIM \_ ElementCapabilities** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="48851-107">The **CIM\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="48851-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48851-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48851-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48851-109">Properties</span></span>

<span data-ttu-id="48851-110">La classe **CIM \_ ElementCapabilities** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="48851-110">The **CIM\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48851-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="48851-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-112">Tipo di dati **: \_ funzionalità CIM**</span><span class="sxs-lookup"><span data-stu-id="48851-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="48851-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48851-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-114">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="48851-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="48851-115">Funzionalità associate all'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="48851-115">The capabilities associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="48851-116">**Caratteristiche**</span><span class="sxs-lookup"><span data-stu-id="48851-116">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-117">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48851-117">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48851-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48851-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48851-119">Set di informazioni descrittive sulle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="48851-119">A set of descriptive information about the capabilities.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="48851-120">**Impostazione predefinita** (2)</span><span class="sxs-lookup"><span data-stu-id="48851-120">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

<span data-ttu-id="48851-121">**Corrente** (3)</span><span class="sxs-lookup"><span data-stu-id="48851-121">**Current** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="48851-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="48851-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="48851-123">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="48851-123">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48851-124">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="48851-124">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-125">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="48851-125">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="48851-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48851-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-127">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="48851-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="48851-128">Elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="48851-128">The managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48851-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48851-129">Requirements</span></span>



| <span data-ttu-id="48851-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="48851-130">Requirement</span></span> | <span data-ttu-id="48851-131">Valore</span><span class="sxs-lookup"><span data-stu-id="48851-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48851-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48851-132">Minimum supported client</span></span><br/> | <span data-ttu-id="48851-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="48851-133">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="48851-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48851-134">Minimum supported server</span></span><br/> | <span data-ttu-id="48851-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48851-135">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="48851-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="48851-136">Namespace</span></span><br/>                | <span data-ttu-id="48851-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="48851-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="48851-138">MOF</span><span class="sxs-lookup"><span data-stu-id="48851-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48851-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48851-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48851-140">DLL</span><span class="sxs-lookup"><span data-stu-id="48851-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48851-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48851-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

