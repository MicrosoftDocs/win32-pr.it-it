---
description: La \_ classe CIM SettingContext associa gli oggetti di configurazione a oggetti setting.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: Classe CIM_SettingContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966021"
---
# <a name="cim_settingcontext-class"></a><span data-ttu-id="f9764-103">CIM \_ SettingContext (classe)</span><span class="sxs-lookup"><span data-stu-id="f9764-103">CIM\_SettingContext class</span></span>

<span data-ttu-id="f9764-104">La classe **CIM \_ SettingContext** associa gli oggetti di configurazione a oggetti setting.</span><span class="sxs-lookup"><span data-stu-id="f9764-104">The **CIM\_SettingContext** class associates configuration objects with setting objects.</span></span> <span data-ttu-id="f9764-105">È ad esempio possibile che le impostazioni di una scheda di rete cambino in base al sito o alla rete a cui è collegato il relativo sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="f9764-105">For example, a network adapter's settings could change based on the site or network to which its hosting computer system is attached.</span></span> <span data-ttu-id="f9764-106">In tal caso, il sistema informatico avrebbe due oggetti di configurazione diversi, corrispondenti alle differenze nella configurazione di rete per i due segmenti di rete.</span><span class="sxs-lookup"><span data-stu-id="f9764-106">In which case, the computer system would have two different configuration objects, corresponding to the differences in network configuration for the two network segments.</span></span> <span data-ttu-id="f9764-107">Una configurazione aggrega un oggetto Setting per la scheda di rete quando opera su un segmento. mentre l'altra configurazione aggrega un oggetto impostazione della scheda di rete diverso, specifico di un altro segmento.</span><span class="sxs-lookup"><span data-stu-id="f9764-107">One configuration would aggregate a setting object for the network adapter when operating on one segment; whereas, the other configuration would aggregate a different network adapter setting object, specific to another segment.</span></span> <span data-ttu-id="f9764-108">Si noti che molte impostazioni computer sono indipendenti dalla configurazione di rete.</span><span class="sxs-lookup"><span data-stu-id="f9764-108">Note that many computer settings are independent of the network configuration.</span></span> <span data-ttu-id="f9764-109">Entrambe le configurazioni, ad esempio, aggregano lo stesso oggetto Setting per la risoluzione del monitoraggio del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="f9764-109">For example, both configurations would aggregate the same setting object for the computer system's monitor resolution.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9764-110">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f9764-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f9764-111">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f9764-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f9764-112">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f9764-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f9764-113">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f9764-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9764-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9764-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="f9764-115">Members</span><span class="sxs-lookup"><span data-stu-id="f9764-115">Members</span></span>

<span data-ttu-id="f9764-116">La classe **CIM \_ SettingContext** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f9764-116">The **CIM\_SettingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="f9764-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9764-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9764-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9764-118">Properties</span></span>

<span data-ttu-id="f9764-119">La classe **CIM \_ SettingContext** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f9764-119">The **CIM\_SettingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9764-120">**Contesto**</span><span class="sxs-lookup"><span data-stu-id="f9764-120">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9764-121">Tipo di dati **: \_ configurazione CIM**</span><span class="sxs-lookup"><span data-stu-id="f9764-121">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="f9764-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9764-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9764-123">Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f9764-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f9764-124">Riferimento all'oggetto di configurazione che aggrega l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="f9764-124">Reference to the configuration object that aggregates the setting.</span></span>

</dd> <dt>

<span data-ttu-id="f9764-125">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="f9764-125">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9764-126">Tipo di dati **: \_ impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="f9764-126">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="f9764-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9764-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9764-128">Riferimento a un'impostazione aggregata.</span><span class="sxs-lookup"><span data-stu-id="f9764-128">Reference to an aggregated setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9764-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9764-129">Remarks</span></span>

<span data-ttu-id="f9764-130">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f9764-130">WMI does not implement this class.</span></span>

<span data-ttu-id="f9764-131">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f9764-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f9764-132">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f9764-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9764-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9764-133">Requirements</span></span>



| <span data-ttu-id="f9764-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9764-134">Requirement</span></span> | <span data-ttu-id="f9764-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f9764-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9764-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9764-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f9764-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9764-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9764-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9764-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f9764-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9764-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9764-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9764-140">Namespace</span></span><br/>                | <span data-ttu-id="f9764-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f9764-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f9764-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f9764-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9764-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9764-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9764-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f9764-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9764-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9764-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

