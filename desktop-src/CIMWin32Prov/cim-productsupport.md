---
description: La \_ classe CIM ProductSupport rappresenta un'associazione tra il prodotto e il supporto dell'accesso che comunica come si ottiene il supporto per il prodotto.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: Classe CIM_ProductSupport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304587"
---
# <a name="cim_productsupport-class"></a><span data-ttu-id="26321-103">CIM \_ ProductSupport (classe)</span><span class="sxs-lookup"><span data-stu-id="26321-103">CIM\_ProductSupport class</span></span>

<span data-ttu-id="26321-104">La classe **CIM \_ ProductSupport** rappresenta un'associazione tra il prodotto e il supporto dell'accesso che comunica come si ottiene il supporto per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="26321-104">The **CIM\_ProductSupport** class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="26321-105">Sono disponibili vari tipi di supporto per un prodotto; lo stesso oggetto di supporto può fornire assistenza per più prodotti.</span><span class="sxs-lookup"><span data-stu-id="26321-105">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26321-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="26321-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="26321-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="26321-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="26321-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="26321-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="26321-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="26321-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="26321-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26321-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a><span data-ttu-id="26321-111">Members</span><span class="sxs-lookup"><span data-stu-id="26321-111">Members</span></span>

<span data-ttu-id="26321-112">La classe **CIM \_ ProductSupport** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="26321-112">The **CIM\_ProductSupport** class has these types of members:</span></span>

-   [<span data-ttu-id="26321-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26321-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26321-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26321-114">Properties</span></span>

<span data-ttu-id="26321-115">La classe **CIM \_ ProductSupport** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="26321-115">The **CIM\_ProductSupport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26321-116">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="26321-116">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26321-117">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="26321-117">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="26321-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26321-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26321-119">Riferimento al prodotto.</span><span class="sxs-lookup"><span data-stu-id="26321-119">Reference to the product.</span></span>

</dd> <dt>

<span data-ttu-id="26321-120">**Supporto**</span><span class="sxs-lookup"><span data-stu-id="26321-120">**Support**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26321-121">Tipo di dati: **CIM \_ SupportAccess**</span><span class="sxs-lookup"><span data-stu-id="26321-121">Data type: **CIM\_SupportAccess**</span></span>
</dt> <dt>

<span data-ttu-id="26321-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26321-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26321-123">Riferimento al supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="26321-123">Reference to the product support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26321-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="26321-124">Remarks</span></span>

<span data-ttu-id="26321-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="26321-125">WMI does not implement this class.</span></span>

<span data-ttu-id="26321-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="26321-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="26321-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="26321-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="26321-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26321-128">Requirements</span></span>



| <span data-ttu-id="26321-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="26321-129">Requirement</span></span> | <span data-ttu-id="26321-130">Valore</span><span class="sxs-lookup"><span data-stu-id="26321-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26321-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26321-131">Minimum supported client</span></span><br/> | <span data-ttu-id="26321-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26321-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26321-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26321-133">Minimum supported server</span></span><br/> | <span data-ttu-id="26321-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26321-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26321-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26321-135">Namespace</span></span><br/>                | <span data-ttu-id="26321-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="26321-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26321-137">MOF</span><span class="sxs-lookup"><span data-stu-id="26321-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26321-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26321-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26321-139">DLL</span><span class="sxs-lookup"><span data-stu-id="26321-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26321-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26321-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




