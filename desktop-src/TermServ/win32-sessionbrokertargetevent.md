---
title: Classe Win32_SessionBrokerTargetEvent
description: Rappresenta una modifica a una destinazione di Service Broker di sessione.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerTargetEvent Servizi Desktop remoto
- Classe Win32_SessionBrokerTargetEvent Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740703"
---
# <a name="win32_sessionbrokertargetevent-class"></a><span data-ttu-id="74794-105">Win32 \_ SessionBrokerTargetEvent (classe)</span><span class="sxs-lookup"><span data-stu-id="74794-105">Win32\_SessionBrokerTargetEvent class</span></span>

<span data-ttu-id="74794-106">Rappresenta una modifica a una destinazione di Service Broker di sessione.</span><span class="sxs-lookup"><span data-stu-id="74794-106">Represents a change to a session broker target.</span></span>

<span data-ttu-id="74794-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="74794-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74794-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74794-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="74794-109">Members</span><span class="sxs-lookup"><span data-stu-id="74794-109">Members</span></span>

<span data-ttu-id="74794-110">La classe **Win32 \_ SessionBrokerTargetEvent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="74794-110">The **Win32\_SessionBrokerTargetEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="74794-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74794-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74794-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74794-112">Properties</span></span>

<span data-ttu-id="74794-113">La classe **Win32 \_ SessionBrokerTargetEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="74794-113">The **Win32\_SessionBrokerTargetEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74794-114">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="74794-114">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74794-115">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74794-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74794-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74794-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74794-117">Specifica la modifica che si è verificata.</span><span class="sxs-lookup"><span data-stu-id="74794-117">Specifies the change that occurred.</span></span> <span data-ttu-id="74794-118">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="74794-118">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="74794-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="74794-119">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="74794-120">Il tipo di modifica non è specificato.</span><span class="sxs-lookup"><span data-stu-id="74794-120">The type of change is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="74794-121">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="74794-121">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="74794-122">L'indirizzo IP esterno è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="74794-122">The external IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="74794-123">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="74794-123">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="74794-124">L'indirizzo IP interno è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="74794-124">The internal IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="74794-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="74794-125">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="74794-126">La destinazione è stata unita in join.</span><span class="sxs-lookup"><span data-stu-id="74794-126">The target was joined.</span></span>

</dd> <dt>

<span data-ttu-id="74794-127">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="74794-127">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="74794-128">La destinazione è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="74794-128">The target was removed.</span></span>

</dd> <dt>

<span data-ttu-id="74794-129">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="74794-129">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="74794-130">Lo stato della destinazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="74794-130">The state of the target has changed.</span></span>

</dd> <dt>

<span data-ttu-id="74794-131">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="74794-131">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="74794-132">La destinazione è inattiva.</span><span class="sxs-lookup"><span data-stu-id="74794-132">The target is idle.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74794-133">**Environment**</span><span class="sxs-lookup"><span data-stu-id="74794-133">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74794-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74794-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74794-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74794-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74794-136">Nome dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="74794-136">The environment name.</span></span> <span data-ttu-id="74794-137">Nel caso di una macchina virtuale (VM) destinazione, potrebbe essere il nome host della VM.</span><span class="sxs-lookup"><span data-stu-id="74794-137">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

<span data-ttu-id="74794-138">**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74794-138">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="74794-139">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="74794-139">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74794-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74794-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74794-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74794-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74794-142">Nome della farm a cui appartiene la destinazione.</span><span class="sxs-lookup"><span data-stu-id="74794-142">The name of the farm the target belongs to.</span></span>

<span data-ttu-id="74794-143">**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74794-143">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="74794-144">**GUID**</span><span class="sxs-lookup"><span data-stu-id="74794-144">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74794-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74794-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74794-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74794-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74794-147">GUID della destinazione.</span><span class="sxs-lookup"><span data-stu-id="74794-147">The GUID of the target.</span></span>

<span data-ttu-id="74794-148">**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74794-148">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="74794-149">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="74794-149">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74794-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74794-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74794-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74794-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74794-152">Nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="74794-152">The name of the plug-in.</span></span>

<span data-ttu-id="74794-153">**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74794-153">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="74794-154">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="74794-154">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74794-155">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="74794-155">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="74794-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74794-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74794-157">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="74794-157">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="74794-158">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="74794-158">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="74794-159">Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="74794-159">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="74794-160">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="74794-160">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74794-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74794-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74794-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74794-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74794-163">Nome della destinazione.</span><span class="sxs-lookup"><span data-stu-id="74794-163">The name of the target.</span></span>

<span data-ttu-id="74794-164">**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74794-164">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="74794-165">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="74794-165">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74794-166">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74794-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74794-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74794-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74794-168">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="74794-168">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="74794-169">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="74794-169">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="74794-170">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="74794-170">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="74794-171">Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="74794-171">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="74794-172">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74794-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74794-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74794-173">Requirements</span></span>



| <span data-ttu-id="74794-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="74794-174">Requirement</span></span> | <span data-ttu-id="74794-175">Valore</span><span class="sxs-lookup"><span data-stu-id="74794-175">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74794-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74794-176">Minimum supported client</span></span><br/> | <span data-ttu-id="74794-177">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="74794-177">None supported</span></span><br/>                                                              |
| <span data-ttu-id="74794-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74794-178">Minimum supported server</span></span><br/> | <span data-ttu-id="74794-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74794-179">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="74794-180">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="74794-180">Namespace</span></span><br/>                | <span data-ttu-id="74794-181">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="74794-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="74794-182">MOF</span><span class="sxs-lookup"><span data-stu-id="74794-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74794-183"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74794-183"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="74794-184">DLL</span><span class="sxs-lookup"><span data-stu-id="74794-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74794-185"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74794-185"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

