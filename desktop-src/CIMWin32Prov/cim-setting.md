---
description: La \_ classe di impostazioni CIM rappresenta i parametri operativi e correlati alla configurazione per uno o più elementi di sistema gestiti.
ms.assetid: 57c46b00-96c4-4df1-82ad-01f7b4f75ced
ms.tgt_platform: multiple
title: Classe CIM_Setting (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1081bd93c95dfa90b6a4dfa6a87339e8e3172a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877665"
---
# <a name="cim_setting-class-cimwin32-wmi-providers"></a><span data-ttu-id="c6dd4-103">Classe CIM_Setting (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c6dd4-103">CIM_Setting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c6dd4-104">La classe di **\_ Impostazioni CIM** rappresenta i parametri operativi e correlati alla configurazione per uno o più elementi di sistema gestiti.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-104">The **CIM\_Setting** class represents configuration-related and operational parameters for one or more managed system elements.</span></span> <span data-ttu-id="c6dd4-105">A un elemento del sistema gestito possono essere associati più oggetti setting.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-105">A managed system element can have multiple setting objects associated with it.</span></span> <span data-ttu-id="c6dd4-106">I valori operativi correnti per i parametri di un elemento vengono riflessi dalle proprietà nell'elemento stesso o dalle proprietà nelle relative associazioni.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-106">The current operational values for an element's parameters are reflected by properties in the element itself or by properties in its associations.</span></span> <span data-ttu-id="c6dd4-107">Queste proprietà non devono necessariamente corrispondere ai valori presenti nell'oggetto Setting.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-107">These properties do not have to be the same values present in the setting object.</span></span> <span data-ttu-id="c6dd4-108">Un modem, ad esempio, può avere un valore di velocità in baud di 56 kilobyte al secondo, ma deve essere operativo a 19,2 kilobyte al secondo.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-108">For example, a modem may have a setting baud rate of 56 kilobytes per second, but be operating at 19.2 kilobytes per second.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6dd4-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c6dd4-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c6dd4-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c6dd4-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c6dd4-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6dd4-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6dd4-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C572-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="c6dd4-114">Members</span><span class="sxs-lookup"><span data-stu-id="c6dd4-114">Members</span></span>

<span data-ttu-id="c6dd4-115">La classe di **\_ Impostazioni CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c6dd4-115">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="c6dd4-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6dd4-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6dd4-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6dd4-117">Properties</span></span>

<span data-ttu-id="c6dd4-118">La classe di **\_ Impostazioni CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-118">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6dd4-119">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c6dd4-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6dd4-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6dd4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6dd4-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6dd4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6dd4-122">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c6dd4-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c6dd4-123">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-123">Short textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="c6dd4-124">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c6dd4-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6dd4-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6dd4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6dd4-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6dd4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6dd4-127">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-127">Textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="c6dd4-128">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="c6dd4-128">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6dd4-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6dd4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6dd4-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6dd4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6dd4-131">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c6dd4-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c6dd4-132">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-132">Identifier by which the current object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6dd4-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6dd4-133">Remarks</span></span>

<span data-ttu-id="c6dd4-134">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-134">WMI does not implement this class.</span></span> <span data-ttu-id="c6dd4-135">Per le classi WMI derivate dall' **\_ impostazione CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c6dd4-135">For WMI classes derived from **CIM\_Setting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c6dd4-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c6dd4-137">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c6dd4-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6dd4-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6dd4-138">Requirements</span></span>



| <span data-ttu-id="c6dd4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6dd4-139">Requirement</span></span> | <span data-ttu-id="c6dd4-140">Valore</span><span class="sxs-lookup"><span data-stu-id="c6dd4-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6dd4-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6dd4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c6dd4-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6dd4-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6dd4-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6dd4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c6dd4-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6dd4-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6dd4-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c6dd4-145">Namespace</span></span><br/>                | <span data-ttu-id="c6dd4-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c6dd4-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6dd4-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c6dd4-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6dd4-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6dd4-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6dd4-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c6dd4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6dd4-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6dd4-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

