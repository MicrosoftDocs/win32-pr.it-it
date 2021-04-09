---
description: Win32 \_ PrivilegesStatus&\# 8194; La classe WMI fornisce informazioni sui privilegi necessari per completare un'operazione. Può essere restituito quando un'operazione ha esito negativo o quando è stata restituita un'istanza parzialmente compilata.
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Classe Win32_PrivilegesStatus (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab399ce08374a954b3bbc015cfee7b4d20167b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877813"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a><span data-ttu-id="ed31c-104">Classe Win32_PrivilegesStatus (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ed31c-104">Win32_PrivilegesStatus class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ed31c-105">La  [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ PrivilegesStatus** fornisce informazioni sui privilegi necessari per completare un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ed31c-105">The **Win32\_PrivilegesStatus** [WMI class](../wmisdk/retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="ed31c-106">Può essere restituito quando un'operazione ha esito negativo o quando è stata restituita un'istanza parzialmente compilata.</span><span class="sxs-lookup"><span data-stu-id="ed31c-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="ed31c-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ed31c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ed31c-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ed31c-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed31c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed31c-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a><span data-ttu-id="ed31c-110">Members</span><span class="sxs-lookup"><span data-stu-id="ed31c-110">Members</span></span>

<span data-ttu-id="ed31c-111">La classe **Win32 \_ PrivilegesStatus** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ed31c-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="ed31c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed31c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed31c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed31c-113">Properties</span></span>

<span data-ttu-id="ed31c-114">La classe **Win32 \_ PrivilegesStatus** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed31c-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed31c-115">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ed31c-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed31c-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed31c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed31c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed31c-118">Qualsiasi stringa definita dall'utente che descrive un errore o uno stato operativo.</span><span class="sxs-lookup"><span data-stu-id="ed31c-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="ed31c-119">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ed31c-119">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed31c-120">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="ed31c-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed31c-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed31c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed31c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed31c-123">Operazione che viene eseguita al momento di un errore o di un'anomalia.</span><span class="sxs-lookup"><span data-stu-id="ed31c-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="ed31c-124">In genere, Strumentazione gestione Windows (WMI) imposta questa proprietà sul nome di un'API COM per un metodo WMI come il seguente: [**IWbemServices:: CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="ed31c-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="ed31c-125">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ed31c-125">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed31c-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="ed31c-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed31c-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed31c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed31c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed31c-129">Parametri che coinvolgono un errore o una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="ed31c-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="ed31c-130">Se, ad esempio, un'applicazione tenta di recuperare una classe che non esiste, questa proprietà viene impostata sul nome della classe che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="ed31c-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="ed31c-131">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ed31c-131">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed31c-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="ed31c-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed31c-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ed31c-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed31c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-135">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT Privileges")</span><span class="sxs-lookup"><span data-stu-id="ed31c-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="ed31c-136">Elenco dei privilegi di accesso necessari mancanti per completare un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ed31c-136">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="ed31c-137">I tipi di privilegi di accesso sono disponibili con i privilegi di Windows.</span><span class="sxs-lookup"><span data-stu-id="ed31c-137">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="ed31c-138">Esempio: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="ed31c-138">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="ed31c-139">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="ed31c-139">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed31c-140">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ed31c-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed31c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-142">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT Privileges")</span><span class="sxs-lookup"><span data-stu-id="ed31c-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="ed31c-143">Elenco di tutti i privilegi necessari per eseguire un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ed31c-143">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="ed31c-144">Sono inclusi i valori della proprietà **PrivilegesNotHeld** .</span><span class="sxs-lookup"><span data-stu-id="ed31c-144">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="ed31c-145">Esempio: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="ed31c-145">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="ed31c-146">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="ed31c-146">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed31c-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ed31c-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed31c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed31c-149">Identifica il provider che causa o segnala un errore o una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="ed31c-149">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="ed31c-150">Se un provider non è necessario, questa stringa è impostata su "Windows Management".</span><span class="sxs-lookup"><span data-stu-id="ed31c-150">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="ed31c-151">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ed31c-151">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed31c-152">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="ed31c-152">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed31c-153">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed31c-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed31c-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ed31c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed31c-155">Contiene un codice di errore o informazioni per un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ed31c-155">Contains an error or information code for an operation.</span></span> <span data-ttu-id="ed31c-156">Può trattarsi di qualsiasi valore definito dal provider, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ed31c-156">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span>

<span data-ttu-id="ed31c-157">Questa proprietà viene ereditata da [**\_ \_ NotifyStatus**](../wmisdk/--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="ed31c-157">This property is inherited from [**\_\_NotifyStatus**](../wmisdk/--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed31c-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed31c-158">Remarks</span></span>

<span data-ttu-id="ed31c-159">La classe **Win32 \_ PrivilegesStatus** deriva da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ed31c-159">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed31c-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed31c-160">Requirements</span></span>



| <span data-ttu-id="ed31c-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed31c-161">Requirement</span></span> | <span data-ttu-id="ed31c-162">Valore</span><span class="sxs-lookup"><span data-stu-id="ed31c-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed31c-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed31c-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ed31c-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed31c-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed31c-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed31c-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ed31c-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed31c-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed31c-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed31c-167">Namespace</span></span><br/>                | <span data-ttu-id="ed31c-168">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ed31c-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed31c-169">MOF</span><span class="sxs-lookup"><span data-stu-id="ed31c-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed31c-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed31c-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed31c-171">DLL</span><span class="sxs-lookup"><span data-stu-id="ed31c-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed31c-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed31c-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed31c-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed31c-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed31c-174">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="ed31c-174">**\_\_ExtendedStatus**</span></span>](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
