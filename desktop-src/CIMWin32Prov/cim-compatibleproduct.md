---
description: La \_ classe CIM CompatibleProduct rappresenta un'associazione tra i prodotti che indica se due prodotti a cui viene fatto riferimento sono interoperativi, ad esempio se possono essere installati insieme o se uno può essere il contenitore fisico per l'altro e così via.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: Classe CIM_CompatibleProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94969b1f2e45a27e402e132a0b9593de413a653b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877982"
---
# <a name="cim_compatibleproduct-class"></a><span data-ttu-id="dde33-103">CIM \_ CompatibleProduct (classe)</span><span class="sxs-lookup"><span data-stu-id="dde33-103">CIM\_CompatibleProduct class</span></span>

<span data-ttu-id="dde33-104">La classe **CIM \_ CompatibleProduct** rappresenta un'associazione tra i prodotti che indica se due prodotti a cui viene fatto riferimento sono interoperativi, ad esempio se possono essere installati insieme o se uno può essere il contenitore fisico per l'altro e così via.</span><span class="sxs-lookup"><span data-stu-id="dde33-104">The **CIM\_CompatibleProduct** class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dde33-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="dde33-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dde33-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dde33-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dde33-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dde33-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dde33-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="dde33-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde33-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dde33-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="dde33-110">Members</span><span class="sxs-lookup"><span data-stu-id="dde33-110">Members</span></span>

<span data-ttu-id="dde33-111">La classe **CIM \_ CompatibleProduct** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dde33-111">The **CIM\_CompatibleProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="dde33-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dde33-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dde33-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dde33-113">Properties</span></span>

<span data-ttu-id="dde33-114">La classe **CIM \_ CompatibleProduct** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dde33-114">The **CIM\_CompatibleProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dde33-115">**CompatibilityDescription**</span><span class="sxs-lookup"><span data-stu-id="dde33-115">**CompatibilityDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde33-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dde33-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dde33-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dde33-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dde33-118">Stringa in formato libero che definisce la modalità di interoperabilità e compatibilità dei due prodotti a cui viene fatto riferimento e se sono presenti limitazioni di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="dde33-118">Free-form string that defines how the two referenced products are interoperable, compatible, and whether there are compatibility limitations.</span></span>

</dd> <dt>

<span data-ttu-id="dde33-119">**CompatibleProduct**</span><span class="sxs-lookup"><span data-stu-id="dde33-119">**CompatibleProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde33-120">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="dde33-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="dde33-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dde33-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dde33-122">Riferimento al prodotto compatibile.</span><span class="sxs-lookup"><span data-stu-id="dde33-122">Reference to the compatible product.</span></span>

</dd> <dt>

<span data-ttu-id="dde33-123">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="dde33-123">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde33-124">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="dde33-124">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="dde33-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dde33-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dde33-126">Riferimento al prodotto per il quale sono definite offerte compatibili.</span><span class="sxs-lookup"><span data-stu-id="dde33-126">Reference to the product for which compatible offerings are defined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dde33-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="dde33-127">Remarks</span></span>

<span data-ttu-id="dde33-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="dde33-128">WMI does not implement this class.</span></span>

<span data-ttu-id="dde33-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="dde33-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dde33-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="dde33-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde33-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dde33-131">Requirements</span></span>



| <span data-ttu-id="dde33-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="dde33-132">Requirement</span></span> | <span data-ttu-id="dde33-133">Valore</span><span class="sxs-lookup"><span data-stu-id="dde33-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dde33-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dde33-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dde33-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dde33-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dde33-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dde33-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dde33-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dde33-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dde33-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dde33-138">Namespace</span></span><br/>                | <span data-ttu-id="dde33-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="dde33-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dde33-140">MOF</span><span class="sxs-lookup"><span data-stu-id="dde33-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dde33-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dde33-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dde33-142">DLL</span><span class="sxs-lookup"><span data-stu-id="dde33-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dde33-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dde33-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




