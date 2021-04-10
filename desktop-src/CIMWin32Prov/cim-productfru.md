---
description: La \_ classe CIM ProductFRU rappresenta un'associazione tra il prodotto e un'unità sostituibile sul campo (FRU), che fornisce informazioni sui componenti del prodotto che sono stati o sono stati sostituiti.
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: Classe CIM_ProductFRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126306"
---
# <a name="cim_productfru-class"></a><span data-ttu-id="af703-103">CIM \_ ProductFRU (classe)</span><span class="sxs-lookup"><span data-stu-id="af703-103">CIM\_ProductFRU class</span></span>

<span data-ttu-id="af703-104">La classe **CIM \_ ProductFRU** rappresenta un'associazione tra il prodotto e un'unità sostituibile sul campo (FRU), che fornisce informazioni sui componenti del prodotto che sono stati o sono stati sostituiti.</span><span class="sxs-lookup"><span data-stu-id="af703-104">The **CIM\_ProductFRU** class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af703-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="af703-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="af703-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="af703-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="af703-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="af703-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="af703-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="af703-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af703-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af703-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="af703-110">Members</span><span class="sxs-lookup"><span data-stu-id="af703-110">Members</span></span>

<span data-ttu-id="af703-111">La classe **CIM \_ ProductFRU** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af703-111">The **CIM\_ProductFRU** class has these types of members:</span></span>

-   [<span data-ttu-id="af703-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af703-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af703-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af703-113">Properties</span></span>

<span data-ttu-id="af703-114">La classe **CIM \_ ProductFRU** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af703-114">The **CIM\_ProductFRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af703-115">**FRU**</span><span class="sxs-lookup"><span data-stu-id="af703-115">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af703-116">Tipo di dati **: \_ FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="af703-116">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="af703-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af703-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af703-118">Riferimento alla FRU.</span><span class="sxs-lookup"><span data-stu-id="af703-118">Reference to the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="af703-119">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="af703-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af703-120">Tipo di dati **: \_ prodotto CIM**</span><span class="sxs-lookup"><span data-stu-id="af703-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="af703-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af703-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af703-122">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="af703-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="af703-123">Riferimento al prodotto a cui viene applicata la FRU.</span><span class="sxs-lookup"><span data-stu-id="af703-123">Reference to the product to which the FRU is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af703-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="af703-124">Remarks</span></span>

<span data-ttu-id="af703-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="af703-125">WMI does not implement this class.</span></span>

<span data-ttu-id="af703-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="af703-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="af703-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="af703-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="af703-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af703-128">Requirements</span></span>



| <span data-ttu-id="af703-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="af703-129">Requirement</span></span> | <span data-ttu-id="af703-130">Valore</span><span class="sxs-lookup"><span data-stu-id="af703-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af703-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af703-131">Minimum supported client</span></span><br/> | <span data-ttu-id="af703-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af703-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af703-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af703-133">Minimum supported server</span></span><br/> | <span data-ttu-id="af703-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af703-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af703-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af703-135">Namespace</span></span><br/>                | <span data-ttu-id="af703-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="af703-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af703-137">MOF</span><span class="sxs-lookup"><span data-stu-id="af703-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af703-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af703-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af703-139">DLL</span><span class="sxs-lookup"><span data-stu-id="af703-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af703-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af703-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

