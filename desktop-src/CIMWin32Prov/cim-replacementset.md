---
description: La \_ classe CIM ReplacementSet aggrega gli elementi fisici che devono essere sostituiti insieme.
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: Classe CIM_ReplacementSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: defc63628e494465d7a31d8adcea758e538c4c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126129"
---
# <a name="cim_replacementset-class"></a><span data-ttu-id="c87bf-103">CIM \_ ReplacementSet (classe)</span><span class="sxs-lookup"><span data-stu-id="c87bf-103">CIM\_ReplacementSet class</span></span>

<span data-ttu-id="c87bf-104">La classe **CIM \_ ReplacementSet** aggrega gli elementi fisici che devono essere sostituiti insieme.</span><span class="sxs-lookup"><span data-stu-id="c87bf-104">The **CIM\_ReplacementSet** class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="c87bf-105">Ad esempio, quando si sostituisce una scheda di memoria, è possibile rimuovere e sostituire anche i chip di memoria del componente.</span><span class="sxs-lookup"><span data-stu-id="c87bf-105">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="c87bf-106">In alternativa, è possibile usare questa associazione per sostituire o aggiornare un set di chip di memoria.</span><span class="sxs-lookup"><span data-stu-id="c87bf-106">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c87bf-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c87bf-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c87bf-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c87bf-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c87bf-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c87bf-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c87bf-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c87bf-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c87bf-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c87bf-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="c87bf-112">Members</span><span class="sxs-lookup"><span data-stu-id="c87bf-112">Members</span></span>

<span data-ttu-id="c87bf-113">La classe **CIM \_ ReplacementSet** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c87bf-113">The **CIM\_ReplacementSet** class has these types of members:</span></span>

-   [<span data-ttu-id="c87bf-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c87bf-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c87bf-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c87bf-115">Properties</span></span>

<span data-ttu-id="c87bf-116">La classe **CIM \_ ReplacementSet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c87bf-116">The **CIM\_ReplacementSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c87bf-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c87bf-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87bf-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c87bf-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c87bf-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c87bf-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c87bf-120">Stringa in formato libero che specifica le informazioni correlate a questa classe.</span><span class="sxs-lookup"><span data-stu-id="c87bf-120">Free-form string that specifies information related to this class.</span></span> <span data-ttu-id="c87bf-121">Lo scopo del set, o informazioni correlate alla modalità di sostituzione degli elementi dei componenti, può essere incluso in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c87bf-121">The purpose of the set, or information related to how the component elements are replaced, can be included in this property.</span></span>

</dd> <dt>

<span data-ttu-id="c87bf-122">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c87bf-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c87bf-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c87bf-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c87bf-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c87bf-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c87bf-125">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c87bf-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c87bf-126">Stringa in formato libero che definisce un'etichetta per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c87bf-126">Free-form string that defines a label for this property.</span></span> <span data-ttu-id="c87bf-127">Questa proprietà è la chiave per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c87bf-127">This property is the key for the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c87bf-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="c87bf-128">Remarks</span></span>

<span data-ttu-id="c87bf-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c87bf-129">WMI does not implement this class.</span></span>

<span data-ttu-id="c87bf-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c87bf-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c87bf-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c87bf-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c87bf-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c87bf-132">Requirements</span></span>



| <span data-ttu-id="c87bf-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c87bf-133">Requirement</span></span> | <span data-ttu-id="c87bf-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c87bf-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c87bf-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c87bf-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c87bf-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c87bf-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c87bf-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c87bf-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c87bf-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c87bf-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c87bf-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c87bf-139">Namespace</span></span><br/>                | <span data-ttu-id="c87bf-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c87bf-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c87bf-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c87bf-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c87bf-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c87bf-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c87bf-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c87bf-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c87bf-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c87bf-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

