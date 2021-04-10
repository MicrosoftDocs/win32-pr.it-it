---
description: L' \_ associazione CIM ActsAsSpare indica gli elementi che possono essere sostituiti o sostituiti da altri elementi aggregati. Una funzione di riserva può essere operata nella \# modalità &0034; hot standby&\# 0034; come specificato per elemento per elemento.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: Classe CIM_ActsAsSpare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 975c6317a78789938ea9d34e062d84fe3435498a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966237"
---
# <a name="cim_actsasspare-class"></a><span data-ttu-id="acaa0-104">CIM \_ ActsAsSpare (classe)</span><span class="sxs-lookup"><span data-stu-id="acaa0-104">CIM\_ActsAsSpare class</span></span>

<span data-ttu-id="acaa0-105">L'associazione **CIM \_ ActsAsSpare** indica gli elementi che possono essere sostituiti o sostituiti da altri elementi aggregati.</span><span class="sxs-lookup"><span data-stu-id="acaa0-105">The **CIM\_ActsAsSpare** association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="acaa0-106">Una scorta può funzionare in modalità "hot-standby", come specificato in base a un elemento.</span><span class="sxs-lookup"><span data-stu-id="acaa0-106">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="acaa0-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="acaa0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="acaa0-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="acaa0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="acaa0-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="acaa0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="acaa0-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="acaa0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="acaa0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acaa0-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a><span data-ttu-id="acaa0-112">Members</span><span class="sxs-lookup"><span data-stu-id="acaa0-112">Members</span></span>

<span data-ttu-id="acaa0-113">La classe **CIM \_ ActsAsSpare** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="acaa0-113">The **CIM\_ActsAsSpare** class has these types of members:</span></span>

-   [<span data-ttu-id="acaa0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acaa0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acaa0-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acaa0-115">Properties</span></span>

<span data-ttu-id="acaa0-116">La classe **CIM \_ ActsAsSpare** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="acaa0-116">The **CIM\_ActsAsSpare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="acaa0-117">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="acaa0-117">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acaa0-118">Tipo di dati: **CIM \_ SpareGroup**</span><span class="sxs-lookup"><span data-stu-id="acaa0-118">Data type: **CIM\_SpareGroup**</span></span>
</dt> <dt>

<span data-ttu-id="acaa0-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acaa0-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acaa0-120">Riferimento alla proprietà del **gruppo** che rappresenta la classe [**CIM \_ SpareGroup**](cim-sparegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="acaa0-120">Reference to the **Group** property that represents the [**CIM\_SpareGroup**](cim-sparegroup.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="acaa0-121">**HotStandby**</span><span class="sxs-lookup"><span data-stu-id="acaa0-121">**HotStandby**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acaa0-122">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="acaa0-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="acaa0-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acaa0-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acaa0-124">Se **true**, la riserva funziona come hot standby.</span><span class="sxs-lookup"><span data-stu-id="acaa0-124">If **TRUE**, the spare is operating as a hot standby.</span></span>

</dd> <dt>

<span data-ttu-id="acaa0-125">**Ricambio**</span><span class="sxs-lookup"><span data-stu-id="acaa0-125">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acaa0-126">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="acaa0-126">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="acaa0-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acaa0-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acaa0-128">Riferimento a un elemento del sistema gestito che funge da riserva e che partecipa al gruppo di riserva.</span><span class="sxs-lookup"><span data-stu-id="acaa0-128">Reference to a managed system element acting as a spare and participating in the spare group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acaa0-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="acaa0-129">Remarks</span></span>

<span data-ttu-id="acaa0-130">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="acaa0-130">WMI does not implement this class.</span></span>

<span data-ttu-id="acaa0-131">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="acaa0-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="acaa0-132">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="acaa0-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="acaa0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acaa0-133">Requirements</span></span>



| <span data-ttu-id="acaa0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="acaa0-134">Requirement</span></span> | <span data-ttu-id="acaa0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="acaa0-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acaa0-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acaa0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="acaa0-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acaa0-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="acaa0-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acaa0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="acaa0-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acaa0-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="acaa0-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="acaa0-140">Namespace</span></span><br/>                | <span data-ttu-id="acaa0-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="acaa0-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="acaa0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="acaa0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acaa0-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acaa0-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="acaa0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="acaa0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acaa0-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acaa0-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acaa0-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acaa0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acaa0-147">Classi CIM</span><span class="sxs-lookup"><span data-stu-id="acaa0-147">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

