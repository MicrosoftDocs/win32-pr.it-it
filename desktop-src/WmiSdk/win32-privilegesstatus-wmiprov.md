---
description: Win32 \_ PrivilegesStatus &\# 8194; La classe WMI fornisce informazioni sui privilegi necessari per completare un'operazione. Può essere restituito quando un'operazione ha esito negativo o quando è stata restituita un'istanza parzialmente compilata.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Classe Win32_PrivilegesStatus (WMI)
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
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 658803be4e70849531bf52e7368e4e9cbcc2f0a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233977"
---
# <a name="win32_privilegesstatus-class-wmi"></a><span data-ttu-id="32e34-104">Classe Win32_PrivilegesStatus (WMI)</span><span class="sxs-lookup"><span data-stu-id="32e34-104">Win32_PrivilegesStatus class (WMI)</span></span>

<span data-ttu-id="32e34-105">La [classe WMI](retrieving-a-class.md) **Win32 \_ PrivilegesStatus** fornisce informazioni sui privilegi necessari per completare un'operazione.   </span><span class="sxs-lookup"><span data-stu-id="32e34-105">The **Win32\_PrivilegesStatus**   [WMI class](retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="32e34-106">Può essere restituito quando un'operazione ha esito negativo o quando è stata restituita un'istanza parzialmente compilata.</span><span class="sxs-lookup"><span data-stu-id="32e34-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="32e34-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="32e34-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="32e34-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="32e34-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e34-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32e34-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
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

## <a name="members"></a><span data-ttu-id="32e34-110">Members</span><span class="sxs-lookup"><span data-stu-id="32e34-110">Members</span></span>

<span data-ttu-id="32e34-111">La classe **Win32 \_ PrivilegesStatus** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="32e34-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="32e34-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32e34-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32e34-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32e34-113">Properties</span></span>

<span data-ttu-id="32e34-114">La classe **Win32 \_ PrivilegesStatus** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="32e34-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32e34-115">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="32e34-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e34-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32e34-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32e34-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32e34-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32e34-118">Qualsiasi stringa definita dall'utente che descrive un errore o uno stato operativo.</span><span class="sxs-lookup"><span data-stu-id="32e34-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="32e34-119">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="32e34-119">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="32e34-120">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="32e34-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e34-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32e34-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32e34-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32e34-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32e34-123">Operazione che viene eseguita al momento di un errore o di un'anomalia.</span><span class="sxs-lookup"><span data-stu-id="32e34-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="32e34-124">In genere, Strumentazione gestione Windows (WMI) imposta questa proprietà sul nome di un'API COM per un metodo WMI come il seguente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="32e34-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="32e34-125">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="32e34-125">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="32e34-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="32e34-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e34-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32e34-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32e34-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32e34-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32e34-129">Parametri che coinvolgono un errore o una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="32e34-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="32e34-130">Se, ad esempio, un'applicazione tenta di recuperare una classe che non esiste, questa proprietà viene impostata sul nome della classe che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="32e34-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="32e34-131">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="32e34-131">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="32e34-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="32e34-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e34-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="32e34-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="32e34-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32e34-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32e34-135">Elenco dei privilegi di accesso necessari mancanti per completare un'operazione.</span><span class="sxs-lookup"><span data-stu-id="32e34-135">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="32e34-136">I tipi di privilegi di accesso sono disponibili con i privilegi di Windows.</span><span class="sxs-lookup"><span data-stu-id="32e34-136">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="32e34-137">Esempio: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="32e34-137">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="32e34-138">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="32e34-138">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e34-139">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="32e34-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="32e34-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32e34-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32e34-141">Elenco di tutti i privilegi necessari per eseguire un'operazione.</span><span class="sxs-lookup"><span data-stu-id="32e34-141">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="32e34-142">Sono inclusi i valori della proprietà **PrivilegesNotHeld** .</span><span class="sxs-lookup"><span data-stu-id="32e34-142">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="32e34-143">Esempio: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="32e34-143">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="32e34-144">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="32e34-144">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e34-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32e34-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32e34-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32e34-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32e34-147">Identifica il provider che causa o segnala un errore o una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="32e34-147">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="32e34-148">Se un provider non è necessario, questa stringa è impostata su "Windows Management".</span><span class="sxs-lookup"><span data-stu-id="32e34-148">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="32e34-149">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="32e34-149">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="32e34-150">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="32e34-150">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e34-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32e34-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32e34-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32e34-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32e34-153">Contiene un codice di errore o informazioni per un'operazione.</span><span class="sxs-lookup"><span data-stu-id="32e34-153">Contains an error or information code for an operation.</span></span> <span data-ttu-id="32e34-154">Può trattarsi di qualsiasi valore definito dal provider, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="32e34-154">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="32e34-155">Questa proprietà viene ereditata da [**\_ \_ NotifyStatus**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="32e34-155">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32e34-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="32e34-156">Remarks</span></span>

<span data-ttu-id="32e34-157">La classe **Win32 \_ PrivilegesStatus** deriva da [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="32e34-157">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32e34-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32e34-158">Requirements</span></span>



| <span data-ttu-id="32e34-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e34-159">Requirement</span></span> | <span data-ttu-id="32e34-160">Valore</span><span class="sxs-lookup"><span data-stu-id="32e34-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32e34-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32e34-161">Minimum supported client</span></span><br/> | <span data-ttu-id="32e34-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32e34-162">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="32e34-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32e34-163">Minimum supported server</span></span><br/> | <span data-ttu-id="32e34-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32e34-164">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="32e34-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="32e34-165">Namespace</span></span><br/>                | <span data-ttu-id="32e34-166">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="32e34-166">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="32e34-167">MOF</span><span class="sxs-lookup"><span data-stu-id="32e34-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32e34-168"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32e34-168"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e34-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32e34-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e34-170">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="32e34-170">**\_\_ExtendedStatus**</span></span>](--extendedstatus.md)
</dt> </dl>

 

 




