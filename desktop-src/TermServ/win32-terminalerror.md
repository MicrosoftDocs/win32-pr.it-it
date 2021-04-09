---
title: Classe Win32_TerminalError
description: Rappresenta un errore del terminale.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Classe Win32_TerminalError Servizi Desktop remoto
- Classe Win32_TerminalError Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119251"
---
# <a name="win32_terminalerror-class"></a><span data-ttu-id="567d8-105">Win32 \_ TerminalError (classe)</span><span class="sxs-lookup"><span data-stu-id="567d8-105">Win32\_TerminalError class</span></span>

<span data-ttu-id="567d8-106">Rappresenta un errore del terminale.</span><span class="sxs-lookup"><span data-stu-id="567d8-106">Represents a terminal error.</span></span>

<span data-ttu-id="567d8-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="567d8-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="567d8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="567d8-108">Syntax</span></span>

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="567d8-109">Members</span><span class="sxs-lookup"><span data-stu-id="567d8-109">Members</span></span>

<span data-ttu-id="567d8-110">La classe **Win32 \_ TerminalError** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="567d8-110">The **Win32\_TerminalError** class has these types of members:</span></span>

-   [<span data-ttu-id="567d8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="567d8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="567d8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="567d8-112">Properties</span></span>

<span data-ttu-id="567d8-113">La classe **Win32 \_ TerminalError** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="567d8-113">The **Win32\_TerminalError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="567d8-114">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="567d8-114">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567d8-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="567d8-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="567d8-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="567d8-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="567d8-117">Qualsiasi stringa definita dall'utente che descrive un errore o uno stato operativo.</span><span class="sxs-lookup"><span data-stu-id="567d8-117">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="567d8-118">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="567d8-118">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="567d8-119">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="567d8-119">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567d8-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="567d8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="567d8-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="567d8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="567d8-122">Operazione che viene eseguita al momento di un errore o di un'anomalia.</span><span class="sxs-lookup"><span data-stu-id="567d8-122">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="567d8-123">In genere, WMI imposta questa proprietà sul nome di un'API COM per un metodo WMI come il seguente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="567d8-123">Typically, WMI sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="567d8-124">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="567d8-124">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="567d8-125">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="567d8-125">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567d8-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="567d8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="567d8-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="567d8-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="567d8-128">Parametri che coinvolgono un errore o una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="567d8-128">Parameters involved in an error or status change.</span></span> <span data-ttu-id="567d8-129">Se, ad esempio, un'applicazione tenta di recuperare una classe che non esiste, questa proprietà viene impostata sul nome della classe che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="567d8-129">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="567d8-130">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="567d8-130">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="567d8-131">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="567d8-131">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567d8-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="567d8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="567d8-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="567d8-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="567d8-134">Identifica il provider che causa o segnala un errore o una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="567d8-134">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="567d8-135">Se un provider non è necessario, questa stringa è impostata su "Windows Management".</span><span class="sxs-lookup"><span data-stu-id="567d8-135">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="567d8-136">Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="567d8-136">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="567d8-137">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="567d8-137">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567d8-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="567d8-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="567d8-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="567d8-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="567d8-140">Contiene un codice di errore o informazioni per un'operazione.</span><span class="sxs-lookup"><span data-stu-id="567d8-140">Contains an error or information code for an operation.</span></span> <span data-ttu-id="567d8-141">Può trattarsi di qualsiasi valore definito dal provider, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="567d8-141">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="567d8-142">Questa proprietà viene ereditata da [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span><span class="sxs-lookup"><span data-stu-id="567d8-142">This property is inherited from [**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span></span>

</dd> <dt>

<span data-ttu-id="567d8-143">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="567d8-143">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="567d8-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="567d8-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="567d8-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="567d8-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="567d8-146">Nome del vizio del terminale in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="567d8-146">The name of the terminal sin which the error occurred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="567d8-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="567d8-147">Requirements</span></span>



| <span data-ttu-id="567d8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="567d8-148">Requirement</span></span> | <span data-ttu-id="567d8-149">Valore</span><span class="sxs-lookup"><span data-stu-id="567d8-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="567d8-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="567d8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="567d8-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="567d8-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="567d8-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="567d8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="567d8-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="567d8-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="567d8-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="567d8-154">Namespace</span></span><br/>                | <span data-ttu-id="567d8-155">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="567d8-155">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="567d8-156">MOF</span><span class="sxs-lookup"><span data-stu-id="567d8-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="567d8-157"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="567d8-157"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="567d8-158">DLL</span><span class="sxs-lookup"><span data-stu-id="567d8-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="567d8-159"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="567d8-159"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="567d8-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="567d8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567d8-161">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="567d8-161">**\_\_ExtendedStatus**</span></span>](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

