---
description: La \_ classe WMI DCOMApplication Win32 rappresenta le proprietà di un'applicazione DCOM.
ms.assetid: 11856834-6774-4262-bac4-e0265d4ba7e3
ms.tgt_platform: multiple
title: Classe Win32_DCOMApplication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplication
- Win32_DCOMApplication.Caption
- Win32_DCOMApplication.Description
- Win32_DCOMApplication.InstallDate
- Win32_DCOMApplication.Name
- Win32_DCOMApplication.Status
- Win32_DCOMApplication.AppID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a90ddaab9565557b5bbc83f52d0dce82447ab15d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305275"
---
# <a name="win32_dcomapplication-class"></a><span data-ttu-id="cd0e3-103">Win32 \_ DCOMApplication (classe)</span><span class="sxs-lookup"><span data-stu-id="cd0e3-103">Win32\_DCOMApplication class</span></span>

<span data-ttu-id="cd0e3-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DCOMApplication Win32** rappresenta le proprietà di un'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-104">The **Win32\_DCOMApplication** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a DCOM application.</span></span>

<span data-ttu-id="cd0e3-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cd0e3-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0e3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd0e3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED52-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplication : Win32_COMApplication
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   AppID;
};
```

## <a name="members"></a><span data-ttu-id="cd0e3-108">Members</span><span class="sxs-lookup"><span data-stu-id="cd0e3-108">Members</span></span>

<span data-ttu-id="cd0e3-109">La classe **Win32 \_ DCOMApplication** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cd0e3-109">The **Win32\_DCOMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="cd0e3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd0e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd0e3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd0e3-111">Properties</span></span>

<span data-ttu-id="cd0e3-112">La classe **Win32 \_ DCOMApplication** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-112">The **Win32\_DCOMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd0e3-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e3-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="cd0e3-117">Identificatore univoco globale (GUID) per l'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-117">Globally unique identifier (GUID) for the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="cd0e3-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e3-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cd0e3-122">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-122">A short textual description of the object.</span></span>

<span data-ttu-id="cd0e3-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e3-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd0e3-124">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e3-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e3-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-127">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cd0e3-128">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-128">A textual description of the object.</span></span>

<span data-ttu-id="cd0e3-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e3-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd0e3-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e3-131">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-133">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cd0e3-134">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-134">Indicates when the object was installed.</span></span> <span data-ttu-id="cd0e3-135">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cd0e3-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e3-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd0e3-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e3-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e3-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-140">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-140">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd0e3-141">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-141">Label by which the object is known.</span></span> <span data-ttu-id="cd0e3-142">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-142">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cd0e3-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e3-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd0e3-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e3-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e3-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd0e3-147">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cd0e3-148">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="cd0e3-149">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cd0e3-150">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="cd0e3-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cd0e3-151">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cd0e3-152">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="cd0e3-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cd0e3-153">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cd0e3-154">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="cd0e3-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cd0e3-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e3-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cd0e3-156">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd0e3-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cd0e3-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cd0e3-158">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cd0e3-159">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="cd0e3-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd0e3-160">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cd0e3-161">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cd0e3-162">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cd0e3-163">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cd0e3-164">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cd0e3-165">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="cd0e3-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cd0e3-166">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cd0e3-167">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cd0e3-168">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="cd0e3-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="cd0e3-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cd0e3-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cd0e3-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd0e3-170">Remarks</span></span>

<span data-ttu-id="cd0e3-171">La classe **Win32 \_ DCOMApplication** è derivata da [**Win32 \_ comapplication**](win32-comapplication.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e3-171">The **Win32\_DCOMApplication** class is derived from [**Win32\_COMApplication**](win32-comapplication.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd0e3-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd0e3-172">Requirements</span></span>



| <span data-ttu-id="cd0e3-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd0e3-173">Requirement</span></span> | <span data-ttu-id="cd0e3-174">Valore</span><span class="sxs-lookup"><span data-stu-id="cd0e3-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0e3-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd0e3-175">Minimum supported client</span></span><br/> | <span data-ttu-id="cd0e3-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd0e3-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd0e3-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd0e3-177">Minimum supported server</span></span><br/> | <span data-ttu-id="cd0e3-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd0e3-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd0e3-179">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd0e3-179">Namespace</span></span><br/>                | <span data-ttu-id="cd0e3-180">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cd0e3-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd0e3-181">MOF</span><span class="sxs-lookup"><span data-stu-id="cd0e3-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd0e3-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd0e3-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd0e3-183">DLL</span><span class="sxs-lookup"><span data-stu-id="cd0e3-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd0e3-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd0e3-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd0e3-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd0e3-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0e3-186">**ComApplicazione Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="cd0e3-186">**Win32\_COMApplication**</span></span>](win32-comapplication.md)
</dt> <dt>

<span data-ttu-id="cd0e3-187">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cd0e3-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

