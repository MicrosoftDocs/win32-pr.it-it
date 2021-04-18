---
description: Rappresenta un'associazione generica tra due elementi gestiti che rappresentano aspetti diversi della stessa entità sottostante.
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: Classe CIM_LogicalIdentity (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305663"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a><span data-ttu-id="ef115-103">Classe CIM_LogicalIdentity (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ef115-103">CIM_LogicalIdentity class (Hyper-V management)</span></span>

<span data-ttu-id="ef115-104">Rappresenta un'associazione generica tra due elementi gestiti che rappresentano aspetti diversi della stessa entità sottostante.</span><span class="sxs-lookup"><span data-stu-id="ef115-104">Represents a generic association between two managed elements that represent different aspects of the same underlying entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef115-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef115-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a><span data-ttu-id="ef115-106">Members</span><span class="sxs-lookup"><span data-stu-id="ef115-106">Members</span></span>

<span data-ttu-id="ef115-107">La classe **CIM \_ LogicalIdentity** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ef115-107">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="ef115-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef115-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef115-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef115-109">Properties</span></span>

<span data-ttu-id="ef115-110">La classe **CIM \_ LogicalIdentity** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ef115-110">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef115-111">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="ef115-111">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef115-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="ef115-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="ef115-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ef115-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef115-114">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ef115-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ef115-115">Secondo aspetto nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="ef115-115">The second aspect in the association.</span></span>

</dd> <dt>

<span data-ttu-id="ef115-116">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="ef115-116">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef115-117">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="ef115-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="ef115-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ef115-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef115-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ef115-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ef115-120">Primo aspetto nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="ef115-120">The first aspect in the association.</span></span> <span data-ttu-id="ef115-121">L'utilizzo del sistema nel nome della proprietà non limita l'ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="ef115-121">The use of System in the property name does not limit the scope of the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef115-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef115-122">Requirements</span></span>



| <span data-ttu-id="ef115-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef115-123">Requirement</span></span> | <span data-ttu-id="ef115-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ef115-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef115-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef115-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef115-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ef115-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ef115-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef115-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef115-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ef115-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ef115-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ef115-129">Namespace</span></span><br/>                | <span data-ttu-id="ef115-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef115-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ef115-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ef115-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef115-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef115-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef115-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ef115-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef115-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef115-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

