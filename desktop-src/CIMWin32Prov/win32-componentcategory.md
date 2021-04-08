---
description: La \_ classe WMI ComponentCategory Win32 rappresenta una categoria di componenti.
ms.assetid: 9c6fc856-8300-4fa5-ae1c-a7d6476f5c51
ms.tgt_platform: multiple
title: Classe Win32_ComponentCategory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComponentCategory
- Win32_ComponentCategory.Caption
- Win32_ComponentCategory.Description
- Win32_ComponentCategory.InstallDate
- Win32_ComponentCategory.Status
- Win32_ComponentCategory.CategoryId
- Win32_ComponentCategory.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730abf9058f5068def4a01f0d7e7601b9c69e53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966266"
---
# <a name="win32_componentcategory-class"></a><span data-ttu-id="57996-103">Win32 \_ ComponentCategory (classe)</span><span class="sxs-lookup"><span data-stu-id="57996-103">Win32\_ComponentCategory class</span></span>

<span data-ttu-id="57996-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComponentCategory Win32** rappresenta una categoria di componenti.</span><span class="sxs-lookup"><span data-stu-id="57996-104">The **Win32\_ComponentCategory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a component category.</span></span> <span data-ttu-id="57996-105">Le categorie di componenti sono gruppi di classi Component Object Model (COM) con un set di funzionalità definito condiviso tra di essi.</span><span class="sxs-lookup"><span data-stu-id="57996-105">Component categories are groups of Component Object Model (COM) classes with a defined functionality set shared between them.</span></span> <span data-ttu-id="57996-106">Un client che utilizza queste interfacce interroga il registro di sistema per il titolo della categoria e l'identificatore univoco denominato **CategoryID**, creato da un identificatore univoco globale (Guid).</span><span class="sxs-lookup"><span data-stu-id="57996-106">A client using these interfaces queries the registry for the category title and unique identifier called **CategoryID**, which is created from a globally unique identifier (GUID).</span></span>

<span data-ttu-id="57996-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="57996-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="57996-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="57996-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="57996-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57996-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED5A-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComponentCategory : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CategoryId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="57996-110">Members</span><span class="sxs-lookup"><span data-stu-id="57996-110">Members</span></span>

<span data-ttu-id="57996-111">La classe **Win32 \_ ComponentCategory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="57996-111">The **Win32\_ComponentCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="57996-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57996-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57996-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57996-113">Properties</span></span>

<span data-ttu-id="57996-114">La classe **Win32 \_ ComponentCategory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="57996-114">The **Win32\_ComponentCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57996-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="57996-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57996-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57996-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57996-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57996-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57996-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="57996-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="57996-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57996-119">A short textual description of the object.</span></span>

<span data-ttu-id="57996-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57996-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57996-121">**CategoryId**</span><span class="sxs-lookup"><span data-stu-id="57996-121">**CategoryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57996-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57996-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57996-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57996-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57996-124">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| categorie di componenti \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| CATID")</span><span class="sxs-lookup"><span data-stu-id="57996-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|catid")</span></span>
</dt> </dl>

<span data-ttu-id="57996-125">GUID per questa categoria di componenti.</span><span class="sxs-lookup"><span data-stu-id="57996-125">GUID for this component category.</span></span>

</dd> <dt>

<span data-ttu-id="57996-126">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="57996-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57996-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57996-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57996-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57996-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57996-129">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="57996-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="57996-130">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57996-130">A textual description of the object.</span></span>

<span data-ttu-id="57996-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57996-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57996-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="57996-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57996-133">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="57996-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="57996-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57996-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57996-135">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="57996-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="57996-136">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="57996-136">Indicates when the object was installed.</span></span> <span data-ttu-id="57996-137">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="57996-137">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="57996-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57996-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57996-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="57996-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57996-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57996-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57996-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57996-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57996-142">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Component Categories \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| szDescription")</span><span class="sxs-lookup"><span data-stu-id="57996-142">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|szDescription")</span></span>
</dt> </dl>

<span data-ttu-id="57996-143">La proprietà Name indica un nome descrittivo di questa categoria di componenti.</span><span class="sxs-lookup"><span data-stu-id="57996-143">The Name property indicates a descriptive name of this component category.</span></span>

</dd> <dt>

<span data-ttu-id="57996-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="57996-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57996-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57996-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57996-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57996-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57996-147">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="57996-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="57996-148">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57996-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="57996-149">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="57996-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="57996-150">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="57996-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="57996-151">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="57996-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="57996-152">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="57996-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="57996-153">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="57996-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="57996-154">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="57996-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="57996-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57996-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="57996-156">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="57996-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="57996-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="57996-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="57996-158">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="57996-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="57996-159">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="57996-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="57996-160">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="57996-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="57996-161">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="57996-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="57996-162">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="57996-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="57996-163">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="57996-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="57996-164">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="57996-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="57996-165">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="57996-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="57996-166">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="57996-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="57996-167">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="57996-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="57996-168">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="57996-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="57996-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="57996-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="57996-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="57996-170">Remarks</span></span>

<span data-ttu-id="57996-171">La classe **Win32 \_ ComponentCategory** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="57996-171">The **Win32\_ComponentCategory** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57996-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57996-172">Requirements</span></span>



| <span data-ttu-id="57996-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="57996-173">Requirement</span></span> | <span data-ttu-id="57996-174">Valore</span><span class="sxs-lookup"><span data-stu-id="57996-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57996-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57996-175">Minimum supported client</span></span><br/> | <span data-ttu-id="57996-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57996-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57996-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57996-177">Minimum supported server</span></span><br/> | <span data-ttu-id="57996-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57996-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57996-179">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="57996-179">Namespace</span></span><br/>                | <span data-ttu-id="57996-180">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="57996-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57996-181">MOF</span><span class="sxs-lookup"><span data-stu-id="57996-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57996-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57996-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57996-183">DLL</span><span class="sxs-lookup"><span data-stu-id="57996-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57996-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57996-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57996-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57996-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57996-186">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="57996-186">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="57996-187">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="57996-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

