---
description: L'API di scripting per WMI contiene flag, valori comuni e codici di errore.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Esecuzione di script di costanti API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309899"
---
# <a name="scripting-api-constants"></a><span data-ttu-id="47c35-103">Esecuzione di script di costanti API</span><span class="sxs-lookup"><span data-stu-id="47c35-103">Scripting API Constants</span></span>

<span data-ttu-id="47c35-104">WMI usa diversi tipi di costanti nel parametro *iFlags* delle chiamate al metodo nell'API di [Scripting per WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-104">WMI uses several types of constants in the *iflags* parameter of method calls in the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="47c35-105">Visual Basic applicazioni possono includere la libreria dei tipi per l'API di scripting, wbemdisp. tlb.</span><span class="sxs-lookup"><span data-stu-id="47c35-105">Visual Basic applications can include the type library for the scripting API, Wbemdisp.tlb.</span></span> <span data-ttu-id="47c35-106">Gli script non sono in grado di accedere alle costanti nella libreria dei tipi, a meno che non utilizzino i <REFERENCE> tag o del <OBJECT> formato di file XML WSH (Windows script host), come descritto in [utilizzo della libreria dei tipi di scripting WMI](using-the-wmi-scripting-type-library.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-106">Scripts are unable to access constants in the type library unless they use the <REFERENCE> or <OBJECT> tags from the Windows Script Host (WSH) XML file format as described in [Using the WMI Scripting Type Library](using-the-wmi-scripting-type-library.md).</span></span> <span data-ttu-id="47c35-107">In caso contrario, uno script deve usare il valore della costante.</span><span class="sxs-lookup"><span data-stu-id="47c35-107">Otherwise, a script must use the value of the constant.</span></span>

## <a name="constants"></a><span data-ttu-id="47c35-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="47c35-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="47c35-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-110">Definire i livelli di autenticazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="47c35-110">Define the security authentication levels.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-112">Definire il modo in cui viene eseguita un'operazione di scrittura in una classe o in un'istanza.</span><span class="sxs-lookup"><span data-stu-id="47c35-112">Define how a write operation to a class or an instance is carried out.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-114">Definire i tipi CIM validi di un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="47c35-114">Define the valid CIM types of a property value.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-116">Definire le impostazioni per il confronto degli oggetti e usate da [**SWbemObject. \_ CompareTo**](swbemobject-compareto-.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-116">Define the settings for object comparison and are used by [**SWbemObject.CompareTo\_**](swbemobject-compareto-.md).</span></span>

</dd> <dt>

<span data-ttu-id="47c35-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-118">Definisce un flag di sicurezza usato come parametro nelle chiamate al metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) in caso di errore di una connessione a WMI in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="47c35-118">Defines a security flag that is used as a parameter in calls to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method when a connection to WMI on a remote machine is failing.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-120">Definire gli errori che possono essere restituiti dall' [API di scripting per](scripting-api-for-wmi.md) le chiamate WMI.</span><span class="sxs-lookup"><span data-stu-id="47c35-120">Define the errors that may be returned by [Scripting API for WMI](scripting-api-for-wmi.md) calls.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-122">Definisce le costanti utilizzate da [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)e [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-122">Defines constants that are used by [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md), and [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>

</dd> <dt>

<span data-ttu-id="47c35-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-124">Definire i livelli di rappresentazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="47c35-124">Define the security impersonation levels.</span></span> <span data-ttu-id="47c35-125">Queste costanti vengono usate con [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-125">These constants are used with [**SWbemSecurity**](swbemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="47c35-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-127">Definire i formati di testo oggetto validi che devono essere usati da [**SWbemObjectEx. \_ gettext**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-127">Define the valid object text formats to be used by [**SWbemObjectEx.GetText\_**](swbemobjectex-gettext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="47c35-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-129">Definire i privilegi.</span><span class="sxs-lookup"><span data-stu-id="47c35-129">Define privileges.</span></span> <span data-ttu-id="47c35-130">Queste costanti vengono usate con [**SWbemSecurity**](swbemsecurity.md) per concedere i privilegi necessari per alcune operazioni.</span><span class="sxs-lookup"><span data-stu-id="47c35-130">These constants are used with [**SWbemSecurity**](swbemsecurity.md) to grant the privileges required for some operations.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-132">Definire la profondità dell'enumerazione o della query, che determina il numero di oggetti restituiti da una chiamata.</span><span class="sxs-lookup"><span data-stu-id="47c35-132">Define the depth of enumeration or query, which determines how many objects are returned by a call.</span></span>

</dd> <dt>

<span data-ttu-id="47c35-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span><span class="sxs-lookup"><span data-stu-id="47c35-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-134">Definisce il contenuto del testo dell'oggetto generato e viene usato da [**SWbemObject. \_ GetObjectText**](swbemobject-getobjecttext-.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-134">Defines the content of generated object text and is used by [**SWbemObject.GetObjectText\_**](swbemobject-getobjecttext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="47c35-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span><span class="sxs-lookup"><span data-stu-id="47c35-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span></span>
</dt> <dd>

<span data-ttu-id="47c35-136">Definisce le costanti di timeout.</span><span class="sxs-lookup"><span data-stu-id="47c35-136">Defines the time-out constants.</span></span> <span data-ttu-id="47c35-137">Questa costante viene utilizzata da [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md).</span><span class="sxs-lookup"><span data-stu-id="47c35-137">This constant is used by [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md).</span></span>

</dd> </dl>

## <a name="combining-flags"></a><span data-ttu-id="47c35-138">Combinazione di flag</span><span class="sxs-lookup"><span data-stu-id="47c35-138">Combining Flags</span></span>

<span data-ttu-id="47c35-139">È possibile combinare i flag per influenzare più di un aspetto della chiamata API.</span><span class="sxs-lookup"><span data-stu-id="47c35-139">You can combine flags to affect more than one aspect of the API call.</span></span>

<span data-ttu-id="47c35-140">Per creare, ad esempio, una chiamata [*semisincrono*](gloss-s.md) , il parametro *iFlags* in una chiamata [**SWbemServices.Exe\_ CQuery**](swbemservices-execquery.md) deve contenere due flag: **WbemFlagReturnImmediately** e **WbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="47c35-140">For example, to create a [*semisynchronous*](gloss-s.md) call, the *iFlags* parameter in an [**SWbemServices.ExecQuery\_**](swbemservices-execquery.md) call must contain two flags: **WbemFlagReturnImmediately** and **WbemFlagForwardOnly**.</span></span> <span data-ttu-id="47c35-141">Il valore di **WbemFlagReturnImmediately** è 16 e il valore di **WbemFlagForwardOnly** è 32.</span><span class="sxs-lookup"><span data-stu-id="47c35-141">The value of **WbemFlagReturnImmediately** is 16 and the value of **WbemFlagForwardOnly** is 32.</span></span> <span data-ttu-id="47c35-142">Poiché non è possibile accedere alle costanti in base al nome, i valori di questi flag vengono combinati, producendo un valore *iFlags* pari a 48.</span><span class="sxs-lookup"><span data-stu-id="47c35-142">Because the constants cannot be accessed by name, the values of these flags are combined, producing an *iFlags* value of 48.</span></span>

<span data-ttu-id="47c35-143">Nell'esempio di script seguente viene illustrata la chiamata a.</span><span class="sxs-lookup"><span data-stu-id="47c35-143">The following script example shows the call.</span></span>


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



<span data-ttu-id="47c35-144">Non tutti i flag possono essere combinati poiché molti si escludono a vicenda e possono produrre risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="47c35-144">Not all flags can be combined since many are mutually exclusive and may produce unpredictable results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47c35-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47c35-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47c35-146">API di scripting per WMI</span><span class="sxs-lookup"><span data-stu-id="47c35-146">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 



