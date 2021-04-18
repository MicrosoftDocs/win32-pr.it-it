---
description: L' \_ associazione CIM ProductSoftwareFeatures identifica le funzionalità software per un determinato prodotto.
ms.assetid: cd6190f8-d86e-44c8-b506-48016a7c22e1
ms.tgt_platform: multiple
title: Classe CIM_ProductSoftwareFeatures
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSoftwareFeatures
- CIM_ProductSoftwareFeatures.Component
- CIM_ProductSoftwareFeatures.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d891d9465688d92c016217cecd8324588026535
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304588"
---
# <a name="cim_productsoftwarefeatures-class"></a><span data-ttu-id="9e6ff-103">CIM \_ ProductSoftwareFeatures (classe)</span><span class="sxs-lookup"><span data-stu-id="9e6ff-103">CIM\_ProductSoftwareFeatures class</span></span>

<span data-ttu-id="9e6ff-104">L'associazione **CIM \_ ProductSoftwareFeatures** identifica le funzionalità software per un determinato prodotto.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-104">The **CIM\_ProductSoftwareFeatures** association identifies the software features for a particular product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e6ff-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9e6ff-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9e6ff-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9e6ff-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9e6ff-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6ff-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e6ff-109">Syntax</span></span>

``` syntax
[UUID("{7C39D12A-DB2B-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_ProductSoftwareFeatures
{
  CIM_SoftwareFeature REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="9e6ff-110">Members</span><span class="sxs-lookup"><span data-stu-id="9e6ff-110">Members</span></span>

<span data-ttu-id="9e6ff-111">La classe **CIM \_ ProductSoftwareFeatures** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9e6ff-111">The **CIM\_ProductSoftwareFeatures** class has these types of members:</span></span>

-   [<span data-ttu-id="9e6ff-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e6ff-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e6ff-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e6ff-113">Properties</span></span>

<span data-ttu-id="9e6ff-114">La classe **CIM \_ ProductSoftwareFeatures** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-114">The **CIM\_ProductSoftwareFeatures** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e6ff-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="9e6ff-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6ff-116">Tipo di dati: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="9e6ff-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="9e6ff-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e6ff-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6ff-118">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e6ff-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e6ff-119">Riferimento al componente.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-119">Reference to the component.</span></span>

</dd> <dt>

<span data-ttu-id="9e6ff-120">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="9e6ff-120">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6ff-121">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="9e6ff-121">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="9e6ff-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e6ff-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6ff-123">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e6ff-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e6ff-124">Riferimento al prodotto.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-124">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e6ff-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e6ff-125">Remarks</span></span>

<span data-ttu-id="9e6ff-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-126">WMI does not implement this class.</span></span> <span data-ttu-id="9e6ff-127">Per le classi WMI derivate da **CIM \_ ProductSoftwareFeatures**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9e6ff-127">For WMI classes derived from **CIM\_ProductSoftwareFeatures**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9e6ff-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9e6ff-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e6ff-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e6ff-130">Requirements</span></span>



| <span data-ttu-id="9e6ff-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e6ff-131">Requirement</span></span> | <span data-ttu-id="9e6ff-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9e6ff-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6ff-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e6ff-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6ff-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e6ff-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e6ff-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e6ff-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6ff-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e6ff-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e6ff-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e6ff-137">Namespace</span></span><br/>                | <span data-ttu-id="9e6ff-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9e6ff-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e6ff-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9e6ff-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e6ff-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e6ff-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e6ff-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9e6ff-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e6ff-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e6ff-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

