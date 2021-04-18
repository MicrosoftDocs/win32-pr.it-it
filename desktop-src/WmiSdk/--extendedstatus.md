---
description: Utilizzato per segnalare informazioni dettagliate sullo stato e sull'errore.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: Classe __ExtendedStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319314"
---
# <a name="__extendedstatus-class"></a><span data-ttu-id="f36dd-103">\_\_Classe ExtendedStatus</span><span class="sxs-lookup"><span data-stu-id="f36dd-103">\_\_ExtendedStatus class</span></span>

<span data-ttu-id="f36dd-104">La classe di sistema **\_ \_ ExtendedStatus** viene utilizzata per segnalare informazioni dettagliate sullo stato e sull'errore.</span><span class="sxs-lookup"><span data-stu-id="f36dd-104">The **\_\_ExtendedStatus** system class is used to report detailed status and error information.</span></span>

<span data-ttu-id="f36dd-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f36dd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f36dd-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f36dd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f36dd-107">Syntax</span></span>

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="f36dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="f36dd-108">Members</span></span>

<span data-ttu-id="f36dd-109">La classe **\_ \_ ExtendedStatus** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f36dd-109">The **\_\_ExtendedStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="f36dd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f36dd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f36dd-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f36dd-111">Properties</span></span>

<span data-ttu-id="f36dd-112">La classe **\_ \_ ExtendedStatus** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f36dd-112">The **\_\_ExtendedStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f36dd-113">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f36dd-113">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36dd-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f36dd-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f36dd-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f36dd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f36dd-116">Qualsiasi stringa definita dall'utente che descrive un errore o uno stato operativo.</span><span class="sxs-lookup"><span data-stu-id="f36dd-116">Any user-defined string that describes an error or operational status.</span></span>

</dd> <dt>

<span data-ttu-id="f36dd-117">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="f36dd-117">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36dd-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f36dd-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f36dd-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f36dd-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f36dd-120">Operazione che viene eseguita al momento di un errore o di un'anomalia.</span><span class="sxs-lookup"><span data-stu-id="f36dd-120">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="f36dd-121">In genere, Strumentazione gestione Windows (WMI) imposta questa proprietà sul nome di un'API COM per un metodo WMI come il seguente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="f36dd-121">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

</dd> <dt>

<span data-ttu-id="f36dd-122">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="f36dd-122">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36dd-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f36dd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f36dd-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f36dd-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f36dd-125">Parametri che coinvolgono un errore o una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="f36dd-125">Parameters involved in an error or status change.</span></span> <span data-ttu-id="f36dd-126">Se, ad esempio, un'applicazione tenta di recuperare una classe che non esiste, questa proprietà viene impostata sul nome della classe che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="f36dd-126">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

</dd> <dt>

<span data-ttu-id="f36dd-127">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="f36dd-127">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36dd-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f36dd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f36dd-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f36dd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f36dd-130">Identifica il provider che causa o segnala un errore o una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="f36dd-130">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="f36dd-131">Se un provider non è necessario, questa stringa è impostata su "Windows Management".</span><span class="sxs-lookup"><span data-stu-id="f36dd-131">If a provider is not involved, this string is set to "Windows Management".</span></span>

</dd> <dt>

<span data-ttu-id="f36dd-132">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="f36dd-132">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36dd-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f36dd-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f36dd-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f36dd-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f36dd-135">Contiene un codice di errore o informazioni per un'operazione.</span><span class="sxs-lookup"><span data-stu-id="f36dd-135">Contains an error or information code for an operation.</span></span> <span data-ttu-id="f36dd-136">Può trattarsi di qualsiasi valore definito dal provider, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f36dd-136">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="f36dd-137">Questa proprietà viene ereditata da [**\_ \_ NotifyStatus**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="f36dd-137">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f36dd-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="f36dd-138">Remarks</span></span>

<span data-ttu-id="f36dd-139">La classe **\_ \_ ExtendedStatus** è derivata dalla classe [**\_ \_ NotifyStatus**](--notifystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f36dd-139">The **\_\_ExtendedStatus** class is derived from the [**\_\_NotifyStatus**](--notifystatus.md) class.</span></span>

<span data-ttu-id="f36dd-140">Usare la classe **\_ \_ ExtendedStatus** per segnalare informazioni più complesse rispetto a un semplice codice di risultato.</span><span class="sxs-lookup"><span data-stu-id="f36dd-140">Use the **\_\_ExtendedStatus** class to report information that is more complex than a simple result code.</span></span> <span data-ttu-id="f36dd-141">I provider possono derivare le proprie classi da **\_ \_ ExtendedStatus** se richiedono più proprietà per descrivere gli errori.</span><span class="sxs-lookup"><span data-stu-id="f36dd-141">Providers can derive their own classes from **\_\_ExtendedStatus** if they require more properties to describe the errors.</span></span>

<span data-ttu-id="f36dd-142">La proprietà **statusCode** , ereditata dalla classe padre [**\_ \_ NotifyStatus**](--notifystatus.md) , è un Unsigned Integer che rappresenta il valore di errore o di stato.</span><span class="sxs-lookup"><span data-stu-id="f36dd-142">The **StatusCode** property, inherited from the [**\_\_NotifyStatus**](--notifystatus.md) parent class, is an unsigned integer that represents the error or status value.</span></span> <span data-ttu-id="f36dd-143">Quando le istanze di questa classe vengono restituite da un metodo da un provider dinamico, le proprietà **statusCode** e **Description** vengono impostate dal provider e le altre proprietà vengono impostate da WMI.</span><span class="sxs-lookup"><span data-stu-id="f36dd-143">When instances of this class are returned from a method by a dynamic provider, the **StatusCode** and **Description** properties are set by the provider, and the other properties are set by WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="f36dd-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="f36dd-144">Examples</span></span>

<span data-ttu-id="f36dd-145">Nell'esempio di codice seguente, tratto da [FND: How to handle Configuration Manager asincrono Errors Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example in TechNet Gallery, descrive l'uso di **\_ \_ ExtendedStatus** per recuperare le informazioni sugli errori.</span><span class="sxs-lookup"><span data-stu-id="f36dd-145">The following code sample, taken from the [FND:How to Handle Configuration Manager Asynchronous Errors by Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example on TechNet Gallery, describes using **\_\_ExtendedStatus** to retrieve error information.</span></span>


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a><span data-ttu-id="f36dd-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f36dd-146">Requirements</span></span>



| <span data-ttu-id="f36dd-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36dd-147">Requirement</span></span> | <span data-ttu-id="f36dd-148">Valore</span><span class="sxs-lookup"><span data-stu-id="f36dd-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f36dd-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f36dd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f36dd-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f36dd-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f36dd-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f36dd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f36dd-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f36dd-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f36dd-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f36dd-153">Namespace</span></span><br/>                | <span data-ttu-id="f36dd-154">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="f36dd-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f36dd-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f36dd-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36dd-156">**\_\_NotifyStatus**</span><span class="sxs-lookup"><span data-stu-id="f36dd-156">**\_\_NotifyStatus**</span></span>](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[<span data-ttu-id="f36dd-157">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f36dd-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

