---
description: La \_ classe CIM StatisticalInformation è una classe radice per la raccolta arbitraria di dati statistici o metriche applicabili a uno o più elementi di sistema gestiti.
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: Classe CIM_StatisticalInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6eda3e2463c880a58c4e23a6d09dcab99417ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878302"
---
# <a name="cim_statisticalinformation-class"></a><span data-ttu-id="1acb8-103">CIM \_ StatisticalInformation (classe)</span><span class="sxs-lookup"><span data-stu-id="1acb8-103">CIM\_StatisticalInformation class</span></span>

<span data-ttu-id="1acb8-104">La classe **CIM \_ StatisticalInformation** è una classe radice per la raccolta arbitraria di dati statistici o metriche applicabili a uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="1acb8-104">The **CIM\_StatisticalInformation** class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1acb8-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="1acb8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1acb8-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1acb8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1acb8-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1acb8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1acb8-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1acb8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1acb8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1acb8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="1acb8-110">Members</span><span class="sxs-lookup"><span data-stu-id="1acb8-110">Members</span></span>

<span data-ttu-id="1acb8-111">La classe **CIM \_ StatisticalInformation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1acb8-111">The **CIM\_StatisticalInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="1acb8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1acb8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1acb8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1acb8-113">Properties</span></span>

<span data-ttu-id="1acb8-114">La classe **CIM \_ StatisticalInformation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1acb8-114">The **CIM\_StatisticalInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1acb8-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1acb8-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acb8-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1acb8-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1acb8-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acb8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1acb8-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1acb8-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1acb8-119">Breve descrizione testuale per la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="1acb8-119">Short textual description for the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="1acb8-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1acb8-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acb8-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1acb8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1acb8-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acb8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acb8-123">Descrizione testuale della statistica o della metrica.</span><span class="sxs-lookup"><span data-stu-id="1acb8-123">Textual description of the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="1acb8-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1acb8-124">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acb8-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1acb8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1acb8-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acb8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1acb8-127">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1acb8-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1acb8-128">Etichetta con la quale è nota la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="1acb8-128">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="1acb8-129">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="1acb8-129">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1acb8-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="1acb8-130">Remarks</span></span>

<span data-ttu-id="1acb8-131">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="1acb8-131">WMI does not implement this class.</span></span> <span data-ttu-id="1acb8-132">Per le classi WMI derivate da **CIM \_ StatisticalInformation**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1acb8-132">For WMI classes derived from **CIM\_StatisticalInformation**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1acb8-133">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="1acb8-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1acb8-134">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1acb8-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1acb8-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1acb8-135">Requirements</span></span>



| <span data-ttu-id="1acb8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1acb8-136">Requirement</span></span> | <span data-ttu-id="1acb8-137">Valore</span><span class="sxs-lookup"><span data-stu-id="1acb8-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1acb8-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1acb8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1acb8-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1acb8-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1acb8-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1acb8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1acb8-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1acb8-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1acb8-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1acb8-142">Namespace</span></span><br/>                | <span data-ttu-id="1acb8-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1acb8-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1acb8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="1acb8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1acb8-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1acb8-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1acb8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1acb8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1acb8-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1acb8-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

