---
description: L' \_ associazione CIM ElementConfiguration mette in correlazione un \_ oggetto di configurazione CIM a uno o più elementi di sistema gestiti. L' \_ oggetto di configurazione CIM rappresenta un determinato comportamento o uno stato funzionale desiderato per il MANAGEDSYSTEMELEMENT CIM associato \_ .
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: Classe CIM_ElementConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049208"
---
# <a name="cim_elementconfiguration-class"></a><span data-ttu-id="492c7-104">CIM \_ ElementConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="492c7-104">CIM\_ElementConfiguration class</span></span>

<span data-ttu-id="492c7-105">L'associazione **CIM \_ ElementConfiguration** mette in correlazione un oggetto di [**\_ configurazione CIM**](cim-configuration.md) a uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="492c7-105">The **CIM\_ElementConfiguration** association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="492c7-106">L'oggetto di **\_ configurazione CIM** rappresenta un determinato comportamento o uno stato funzionale desiderato per il [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associato.</span><span class="sxs-lookup"><span data-stu-id="492c7-106">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="492c7-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="492c7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="492c7-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="492c7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="492c7-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="492c7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="492c7-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="492c7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="492c7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="492c7-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="492c7-112">Members</span><span class="sxs-lookup"><span data-stu-id="492c7-112">Members</span></span>

<span data-ttu-id="492c7-113">La classe **CIM \_ ElementConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="492c7-113">The **CIM\_ElementConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="492c7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="492c7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="492c7-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="492c7-115">Properties</span></span>

<span data-ttu-id="492c7-116">La classe **CIM \_ ElementConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="492c7-116">The **CIM\_ElementConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="492c7-117">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="492c7-117">**Configuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="492c7-118">Tipo di dati **: \_ configurazione CIM**</span><span class="sxs-lookup"><span data-stu-id="492c7-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="492c7-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="492c7-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="492c7-120">Riferimento all'oggetto [**di \_ configurazione CIM**](cim-configuration.md) che raggruppa le impostazioni e le dipendenze associate all'elemento del sistema gestito.</span><span class="sxs-lookup"><span data-stu-id="492c7-120">Reference to the [**CIM\_Configuration**](cim-configuration.md) object that groups the settings and dependencies associated with the managed system element.</span></span>

</dd> <dt>

<span data-ttu-id="492c7-121">**elemento**</span><span class="sxs-lookup"><span data-stu-id="492c7-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="492c7-122">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="492c7-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="492c7-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="492c7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="492c7-124">Riferimento all'elemento del sistema gestito.</span><span class="sxs-lookup"><span data-stu-id="492c7-124">Reference to the managed system element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="492c7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="492c7-125">Remarks</span></span>

<span data-ttu-id="492c7-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="492c7-126">WMI does not implement this class.</span></span>

<span data-ttu-id="492c7-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="492c7-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="492c7-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="492c7-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="492c7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="492c7-129">Requirements</span></span>



| <span data-ttu-id="492c7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="492c7-130">Requirement</span></span> | <span data-ttu-id="492c7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="492c7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="492c7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="492c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="492c7-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="492c7-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="492c7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="492c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="492c7-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="492c7-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="492c7-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="492c7-136">Namespace</span></span><br/>                | <span data-ttu-id="492c7-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="492c7-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="492c7-138">MOF</span><span class="sxs-lookup"><span data-stu-id="492c7-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="492c7-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="492c7-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="492c7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="492c7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="492c7-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="492c7-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




