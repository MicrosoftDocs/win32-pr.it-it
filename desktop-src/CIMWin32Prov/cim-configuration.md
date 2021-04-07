---
description: L' \_ oggetto di configurazione CIM consente il raggruppamento di set di parametri (definiti in \_ oggetti impostazione CIM) e le dipendenze per uno o più elementi di sistema gestiti.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: Classe CIM_Configuration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c069f5c7186d08f01b54fe02c0568dbb4ff43d26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748602"
---
# <a name="cim_configuration-class"></a><span data-ttu-id="2fbda-103">\_Classe di configurazione CIM</span><span class="sxs-lookup"><span data-stu-id="2fbda-103">CIM\_Configuration class</span></span>

<span data-ttu-id="2fbda-104">L'oggetto di **\_ configurazione CIM** consente il raggruppamento di set di parametri (definiti in oggetti [**\_ impostazione CIM**](cim-setting.md) ) e le dipendenze per uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="2fbda-104">The **CIM\_Configuration** object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span> <span data-ttu-id="2fbda-105">Questo oggetto rappresenta un determinato comportamento o uno stato funzionale desiderato per gli elementi del sistema gestito.</span><span class="sxs-lookup"><span data-stu-id="2fbda-105">This object represents a certain behavior, or a desired functional state for the managed system elements.</span></span> <span data-ttu-id="2fbda-106">Lo stato funzionale desiderato è in genere determinato da requisiti esterni, ad esempio l'ora o la località.</span><span class="sxs-lookup"><span data-stu-id="2fbda-106">The desired functional state is typically driven by external requirements, such as time or location.</span></span> <span data-ttu-id="2fbda-107">Ad esempio, per connettersi a un sistema di posta elettronica da casa, esiste una dipendenza da un modem; mentre una dipendenza da una scheda di rete esiste al lavoro.</span><span class="sxs-lookup"><span data-stu-id="2fbda-107">For example, to connect to a mail system from home, a dependency on a modem exists; whereas, a dependency on a network adapter exists at work.</span></span> <span data-ttu-id="2fbda-108">Le impostazioni per i dispositivi logici pertinenti (in questo esempio, il modem e la scheda di rete di POTS) possono essere definite e aggregate in base alla **\_ configurazione CIM**.</span><span class="sxs-lookup"><span data-stu-id="2fbda-108">Settings for the pertinent logical devices (in this example, POTS modem and network adapter) can be defined and aggregated by **CIM\_Configuration**.</span></span> <span data-ttu-id="2fbda-109">Per questo motivo, è possibile definire due configurazioni di "Connetti alla posta elettronica" raggruppando le dipendenze e gli oggetti di [**\_ Impostazioni CIM**](cim-setting.md) pertinenti.</span><span class="sxs-lookup"><span data-stu-id="2fbda-109">Therefore, two "Connect to Mail" configurations can be defined by grouping the relevant dependencies and [**CIM\_Setting**](cim-setting.md) objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fbda-110">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2fbda-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2fbda-111">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2fbda-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2fbda-112">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2fbda-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2fbda-113">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2fbda-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fbda-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fbda-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="2fbda-115">Members</span><span class="sxs-lookup"><span data-stu-id="2fbda-115">Members</span></span>

<span data-ttu-id="2fbda-116">La classe di **\_ configurazione CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2fbda-116">The **CIM\_Configuration** class has these types of members:</span></span>

-   [<span data-ttu-id="2fbda-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fbda-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fbda-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fbda-118">Properties</span></span>

<span data-ttu-id="2fbda-119">La classe di **\_ configurazione CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2fbda-119">The **CIM\_Configuration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fbda-120">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2fbda-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fbda-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2fbda-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fbda-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fbda-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fbda-123">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2fbda-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2fbda-124">Breve descrizione testuale dell'oggetto **di \_ configurazione CIM** .</span><span class="sxs-lookup"><span data-stu-id="2fbda-124">Short textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="2fbda-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2fbda-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fbda-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2fbda-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fbda-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fbda-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fbda-128">Descrizione testuale dell'oggetto **di \_ configurazione CIM** .</span><span class="sxs-lookup"><span data-stu-id="2fbda-128">Textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="2fbda-129">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2fbda-129">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fbda-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2fbda-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fbda-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fbda-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fbda-132">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2fbda-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2fbda-133">Etichetta con cui è noto l'oggetto di **\_ configurazione CIM** .</span><span class="sxs-lookup"><span data-stu-id="2fbda-133">Label by which the **CIM\_Configuration** object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fbda-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fbda-134">Remarks</span></span>

<span data-ttu-id="2fbda-135">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="2fbda-135">WMI does not implement this class.</span></span>

<span data-ttu-id="2fbda-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2fbda-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2fbda-137">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2fbda-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fbda-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fbda-138">Requirements</span></span>



| <span data-ttu-id="2fbda-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fbda-139">Requirement</span></span> | <span data-ttu-id="2fbda-140">Valore</span><span class="sxs-lookup"><span data-stu-id="2fbda-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fbda-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fbda-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2fbda-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fbda-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fbda-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fbda-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2fbda-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fbda-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fbda-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2fbda-145">Namespace</span></span><br/>                | <span data-ttu-id="2fbda-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2fbda-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2fbda-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2fbda-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fbda-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fbda-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fbda-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2fbda-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fbda-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fbda-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

