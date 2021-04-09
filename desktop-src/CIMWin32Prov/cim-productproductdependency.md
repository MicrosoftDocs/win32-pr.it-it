---
description: La \_ classe CIM ProductProductDependency rappresenta un'associazione tra due prodotti, che indica che è necessario installare o assente per il funzionamento dell'altro. Questa operazione è concettualmente equivalente all' \_ associazione CIM ServiceServiceDependency.
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: Classe CIM_ProductProductDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductProductDependency
- CIM_ProductProductDependency.DependentProduct
- CIM_ProductProductDependency.RequiredProduct
- CIM_ProductProductDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 094800b3a2d50d7be4039d5850f9ac1d3f236a40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049133"
---
# <a name="cim_productproductdependency-class"></a><span data-ttu-id="6a372-104">CIM \_ ProductProductDependency (classe)</span><span class="sxs-lookup"><span data-stu-id="6a372-104">CIM\_ProductProductDependency class</span></span>

<span data-ttu-id="6a372-105">La classe **CIM \_ ProductProductDependency** rappresenta un'associazione tra due prodotti, che indica che è necessario installare o assente per il funzionamento dell'altro.</span><span class="sxs-lookup"><span data-stu-id="6a372-105">The **CIM\_ProductProductDependency** class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="6a372-106">Questa operazione è concettualmente equivalente all'associazione [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="6a372-106">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a372-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6a372-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6a372-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6a372-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6a372-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6a372-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6a372-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6a372-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a372-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a372-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{65878E68-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductProductDependency
{
  CIM_Product REF DependentProduct;
  CIM_Product REF RequiredProduct;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="6a372-112">Members</span><span class="sxs-lookup"><span data-stu-id="6a372-112">Members</span></span>

<span data-ttu-id="6a372-113">La classe **CIM \_ ProductProductDependency** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6a372-113">The **CIM\_ProductProductDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="6a372-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a372-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a372-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a372-115">Properties</span></span>

<span data-ttu-id="6a372-116">La classe **CIM \_ ProductProductDependency** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6a372-116">The **CIM\_ProductProductDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a372-117">**DependentProduct**</span><span class="sxs-lookup"><span data-stu-id="6a372-117">**DependentProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a372-118">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="6a372-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="6a372-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a372-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a372-120">Riferimento al prodotto dipendente da un altro prodotto.</span><span class="sxs-lookup"><span data-stu-id="6a372-120">Reference to the product that is dependent on another product.</span></span>

</dd> <dt>

<span data-ttu-id="6a372-121">**RequiredProduct**</span><span class="sxs-lookup"><span data-stu-id="6a372-121">**RequiredProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a372-122">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="6a372-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="6a372-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a372-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a372-124">Riferimento al prodotto richiesto.</span><span class="sxs-lookup"><span data-stu-id="6a372-124">Reference to the required product.</span></span>

</dd> <dt>

<span data-ttu-id="6a372-125">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="6a372-125">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a372-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a372-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a372-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a372-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a372-128">Natura della dipendenza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="6a372-128">Nature of the product dependency.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a372-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a372-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6a372-130">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6a372-130">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a372-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a372-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a372-132">Altro.</span><span class="sxs-lookup"><span data-stu-id="6a372-132">Other.</span></span>

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span data-ttu-id="6a372-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>Il **prodotto deve essere installato** (2)</span><span class="sxs-lookup"><span data-stu-id="6a372-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**Product Must Be Installed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a372-134">Il prodotto deve essere installato.</span><span class="sxs-lookup"><span data-stu-id="6a372-134">Product must be installed.</span></span>

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span data-ttu-id="6a372-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>Il **prodotto non deve essere installato** (3)</span><span class="sxs-lookup"><span data-stu-id="6a372-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**Product Must Not Be Installed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6a372-136">Il prodotto non deve essere installato.</span><span class="sxs-lookup"><span data-stu-id="6a372-136">Product must not be installed.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a372-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a372-137">Remarks</span></span>

<span data-ttu-id="6a372-138">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6a372-138">WMI does not implement this class.</span></span>

<span data-ttu-id="6a372-139">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6a372-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6a372-140">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6a372-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a372-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a372-141">Requirements</span></span>



| <span data-ttu-id="6a372-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a372-142">Requirement</span></span> | <span data-ttu-id="6a372-143">Valore</span><span class="sxs-lookup"><span data-stu-id="6a372-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a372-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a372-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6a372-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a372-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a372-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a372-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6a372-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a372-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a372-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a372-148">Namespace</span></span><br/>                | <span data-ttu-id="6a372-149">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6a372-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a372-150">MOF</span><span class="sxs-lookup"><span data-stu-id="6a372-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a372-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a372-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a372-152">DLL</span><span class="sxs-lookup"><span data-stu-id="6a372-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a372-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a372-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




