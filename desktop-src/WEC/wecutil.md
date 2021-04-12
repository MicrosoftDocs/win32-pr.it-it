---
title: Wecutil.exe
description: Wecutil.exe è un'utilità raccolta eventi di Windows che consente a un amministratore di creare e gestire le sottoscrizioni agli eventi da origini eventi remote che supportano il protocollo di WS-Management.
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353981"
---
# <a name="wecutilexe"></a><span data-ttu-id="a4159-104">Wecutil.exe</span><span class="sxs-lookup"><span data-stu-id="a4159-104">Wecutil.exe</span></span>

<span data-ttu-id="a4159-105">Wecutil.exe è un'utilità raccolta eventi di Windows che consente a un amministratore di creare e gestire le sottoscrizioni agli eventi da origini eventi remote che supportano il protocollo di WS-Management.</span><span class="sxs-lookup"><span data-stu-id="a4159-105">Wecutil.exe is a Windows Event Collector utility that enables an administrator to create and manage subscriptions to events forwarded from remote event sources that support the WS-Management protocol.</span></span> <span data-ttu-id="a4159-106">I comandi, le opzioni e i valori di opzione non fanno distinzione tra maiuscole e minuscole per questa utilità.</span><span class="sxs-lookup"><span data-stu-id="a4159-106">Commands, options, and option values are case-insensitive for this utility.</span></span>

<span data-ttu-id="a4159-107">Se viene visualizzato un messaggio che indica che il server RPC non è disponibile o che l'interfaccia è sconosciuta, quando si tenta di eseguire wecutil, è necessario avviare il servizio raccolta eventi Windows (wecsvc).</span><span class="sxs-lookup"><span data-stu-id="a4159-107">If you receive a message that says "The RPC server is unavailable" or "The interface is unknown" when you try to run wecutil, then you need to start the Windows Event Collector service (wecsvc).</span></span> <span data-ttu-id="a4159-108">Per avviare wecsvc, a un prompt dei comandi con privilegi elevati, digitare **net start wecsvc**.</span><span class="sxs-lookup"><span data-stu-id="a4159-108">To start wecsvc, at an elevated command prompt type **net start wecsvc**.</span></span>

## <a name="list-existing-subscriptions"></a><span data-ttu-id="a4159-109">Elencare le sottoscrizioni esistenti</span><span class="sxs-lookup"><span data-stu-id="a4159-109">List existing subscriptions</span></span>

<span data-ttu-id="a4159-110">La sintassi seguente consente di elencare le sottoscrizioni di eventi remoti esistenti.</span><span class="sxs-lookup"><span data-stu-id="a4159-110">The following syntax is used to list existing remote event subscriptions.</span></span>

``` syntax
wecutil { es | enum-subscription }
```

<span data-ttu-id="a4159-111">Se si usa uno script per ottenere i nomi delle sottoscrizioni dall'output, sarà necessario ignorare i caratteri DBA UTF-8 nella prima riga dell'output.</span><span class="sxs-lookup"><span data-stu-id="a4159-111">If you use a script to get the names of the subscriptions from the output, you will need to bypass the UTF-8 BOM characters in the first line of the output.</span></span> <span data-ttu-id="a4159-112">Nello script seguente viene illustrato un esempio di come è possibile ignorare i caratteri DBA.</span><span class="sxs-lookup"><span data-stu-id="a4159-112">The following script shows an example of how you might skip the BOM characters.</span></span>

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a><span data-ttu-id="a4159-113">Ottenere la configurazione della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="a4159-113">Get subscription configuration</span></span>

<span data-ttu-id="a4159-114">La sintassi seguente consente di visualizzare i dati di configurazione della sottoscrizione di eventi remoti.</span><span class="sxs-lookup"><span data-stu-id="a4159-114">The following syntax is used to display remote event subscription configuration data.</span></span>

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a><span data-ttu-id="a4159-115">Ottenere i parametri di configurazione</span><span class="sxs-lookup"><span data-stu-id="a4159-115">Get Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4159-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**</span><span class="sxs-lookup"><span data-stu-id="a4159-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-117">Stringa che identifica in modo univoco una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-117">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a4159-118">Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-118">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>\*\*VALORE/f: \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a4159-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:\*VALUE**\*</span></span>
</dt> <dd>

<span data-ttu-id="a4159-120">Valore che specifica l'output dei dati di configurazione della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-120">A value that specifies the output of the subscription configuration data.</span></span> <span data-ttu-id="a4159-121">Il valore può essere "XML" o "conciso" e il *valore* predefinito è "conciso".</span><span class="sxs-lookup"><span data-stu-id="a4159-121">*VALUE* can be "XML" or "Terse", and the default is "Terse".</span></span> <span data-ttu-id="a4159-122">Se il *valore* è "XML", l'output viene stampato in formato "XML".</span><span class="sxs-lookup"><span data-stu-id="a4159-122">If *VALUE* is "XML", then the output is printed in "XML" format.</span></span> <span data-ttu-id="a4159-123">Se il *valore* è "conciso", l'output viene stampato in coppie nome-valore.</span><span class="sxs-lookup"><span data-stu-id="a4159-123">If *VALUE* is "Terse", then the output is printed in name-value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *valore***</span><span class="sxs-lookup"><span data-stu-id="a4159-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-125">Valore che specifica se l'output è in formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a4159-125">A value that specifies whether the output is in Unicode format.</span></span> <span data-ttu-id="a4159-126">Il *valore* può essere "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="a4159-126">*VALUE* can be "true" or "false".</span></span> <span data-ttu-id="a4159-127">Se il *valore* è "true", l'output è in formato Unicode e se *value* è "false", l'output non è in formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a4159-127">If *VALUE* is "true", then the output is in Unicode format, and if *VALUE* is "false", then the output is not in Unicode format.</span></span>

</dd> </dl>

## <a name="get-subscription-runtime-status"></a><span data-ttu-id="a4159-128">Ottenere lo stato di runtime della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="a4159-128">Get subscription runtime status</span></span>

<span data-ttu-id="a4159-129">La sintassi seguente consente di visualizzare lo stato di runtime della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-129">The following syntax is used to display the subscription runtime status.</span></span>

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a><span data-ttu-id="a4159-130">Ottieni parametri di stato</span><span class="sxs-lookup"><span data-stu-id="a4159-130">Get Status Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4159-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**</span><span class="sxs-lookup"><span data-stu-id="a4159-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-132">Stringa che identifica in modo univoco una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-132">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a4159-133">Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-133">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_origine evento**</span><span class="sxs-lookup"><span data-stu-id="a4159-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-135">Valore che identifica un computer che rappresenta un'origine evento per una sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-135">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="a4159-136">Questo valore può essere il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a4159-136">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="set-subscription-configuration-information"></a><span data-ttu-id="a4159-137">Impostare le informazioni di configurazione della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="a4159-137">Set Subscription Configuration Information</span></span>

<span data-ttu-id="a4159-138">La sintassi seguente viene utilizzata per impostare i dati di configurazione della sottoscrizione modificando i parametri di sottoscrizione dalla riga di comando o utilizzando un file di configurazione XML.</span><span class="sxs-lookup"><span data-stu-id="a4159-138">The following syntax is used to set subscription configuration data by changing subscription parameters from the command line or using an XML configuration file.</span></span>

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a><span data-ttu-id="a4159-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4159-139">Remarks</span></span>

<span data-ttu-id="a4159-140">Quando si specifica un nome utente o una password non corretta nel comando **wecutil SS** , non viene segnalato alcun errore fino a quando non si visualizza lo stato di runtime della sottoscrizione usando il comando **wecutil gr** .</span><span class="sxs-lookup"><span data-stu-id="a4159-140">When an incorrect username or password is specified in the **wecutil ss** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="set-configuration-parameters"></a><span data-ttu-id="a4159-141">Imposta parametri di configurazione</span><span class="sxs-lookup"><span data-stu-id="a4159-141">Set Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4159-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**</span><span class="sxs-lookup"><span data-stu-id="a4159-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-143">Stringa che identifica in modo univoco una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-143">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a4159-144">Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-144">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *\_ file CONGIG***</span><span class="sxs-lookup"><span data-stu-id="a4159-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG\_FILE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-146">Valore che specifica il percorso del file XML che contiene le informazioni di configurazione della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-146">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="a4159-147">Il percorso può essere assoluto o relativo alla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="a4159-147">The path can be absolute or relative to the current directory.</span></span> <span data-ttu-id="a4159-148">Questo parametro può essere utilizzato solo con i parametri facoltativi/CUS e/Cup e si escludono a vicenda con tutti gli altri parametri.</span><span class="sxs-lookup"><span data-stu-id="a4159-148">This parameter can only be used with the optional /cus and /cup parameters, and is mutually exclusive with all the other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *valore***</span><span class="sxs-lookup"><span data-stu-id="a4159-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-150">Valore che determina se abilitare o disabilitare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-150">A value that determines whether to enable or disable the subscription.</span></span> <span data-ttu-id="a4159-151">Il valore può essere true o false.</span><span class="sxs-lookup"><span data-stu-id="a4159-151">VALUE can be true or false.</span></span> <span data-ttu-id="a4159-152">Il valore predefinito è true, che Abilita la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-152">The default value is true, which enables the subscription.</span></span>

> [!Note]  
> <span data-ttu-id="a4159-153">Quando si disabilita una sottoscrizione avviata dall'agente di raccolta, l'origine evento diventa inattiva invece che disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a4159-153">When you disable a collector initiated subscription, the event source becomes inactive instead of disabled.</span></span> <span data-ttu-id="a4159-154">In una sottoscrizione avviata dall'agente di raccolta è possibile disabilitare un'origine evento indipendente dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-154">In a collector initiated subscription, you can disable an event source independent of the subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="a4159-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Descrizione***</span><span class="sxs-lookup"><span data-stu-id="a4159-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-156">Valore che specifica una descrizione per la sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-156">A value that specifies a description for the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *data e \_ ora***</span><span class="sxs-lookup"><span data-stu-id="a4159-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE\_TIME***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-158">Valore che specifica l'ora di scadenza della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-158">A value that specifies the subscription expiration time.</span></span> <span data-ttu-id="a4159-159">*Data di scadenza \_ TIME* è un valore specificato nel formato di data e ora standard XML o ISO8601: "aaaa-mm-ggThh: mm: SS \[ . sss \] \[ Z \] " dove "T" è il separatore dell'ora e "Z" indica l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="a4159-159">*DATE\_TIME* is a value specified in standard XML or ISO8601 date-time format: "yyyy-MM-ddThh:mm:ss\[.sss\]\[Z\]" where "T" is the time separator and "Z" indicates UTC time.</span></span> <span data-ttu-id="a4159-160">Se, ad esempio, *data e \_ ora* è "2007-01-12T01:20:00", l'ora di scadenza della sottoscrizione è il 12 gennaio 2007, 01:20.</span><span class="sxs-lookup"><span data-stu-id="a4159-160">For example, if *DATE\_TIME* is "2007-01-12T01:20:00", then the subscription expiration time is January 12th, 2007, 01:20.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/URI: *URI***</span><span class="sxs-lookup"><span data-stu-id="a4159-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-162">Valore che specifica il tipo di eventi utilizzati dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-162">A value that specifies the type of events consumed by the subscription.</span></span> <span data-ttu-id="a4159-163">L'indirizzo del computer di origine evento insieme all'URI (Uniform Resource Identifier) identifica in modo univoco l'origine degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-163">The address of the event source computer along with the uniform resource identifier (URI) uniquely identifies the source of the events.</span></span> <span data-ttu-id="a4159-164">La stringa URI è utilizzata per tutti gli indirizzi di origine evento nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-164">The URI string is used for all event source addresses in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *\_ modalità di configurazione***</span><span class="sxs-lookup"><span data-stu-id="a4159-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *CONFIGURATION\_MODE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-166">Valore che specifica la modalità di configurazione della sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-166">A value that specifies the configuration mode of the event subscription.</span></span> <span data-ttu-id="a4159-167">*Configurazione \_ di La modalità* può essere una delle seguenti stringhe: "Normal", "Custom", "MinLatency" o "MinBandwidth".</span><span class="sxs-lookup"><span data-stu-id="a4159-167">*CONFIGURATION\_MODE* can be one of the following strings: "Normal", "Custom", "MinLatency", or "MinBandwidth".</span></span> <span data-ttu-id="a4159-168">L'enumerazione della [**\_ modalità di \_ configurazione \_ della sottoscrizione EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) definisce le modalità di configurazione.</span><span class="sxs-lookup"><span data-stu-id="a4159-168">The [**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) enumeration defines the configuration modes.</span></span> <span data-ttu-id="a4159-169">È possibile specificare i parametri/DM,/DMI,/Hi e/DMLT solo se la modalità di configurazione è impostata su Custom.</span><span class="sxs-lookup"><span data-stu-id="a4159-169">The /dm, /dmi, /hi, and /dmlt parameters can only be specified if the configuration mode is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *query***</span><span class="sxs-lookup"><span data-stu-id="a4159-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-171">Valore che specifica la stringa di query per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-171">A value that specifies the query string for the subscription.</span></span> <span data-ttu-id="a4159-172">Il formato di questa stringa può essere diverso per i diversi valori URI e si applica a tutte le origini eventi nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-172">The format of this string can be different for different URI values and applies to all event sources in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *dialetto***</span><span class="sxs-lookup"><span data-stu-id="a4159-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-174">Valore che specifica il dialetto utilizzato dalla stringa di query.</span><span class="sxs-lookup"><span data-stu-id="a4159-174">A value that specifies the dialect the query string uses.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF: *Format***</span><span class="sxs-lookup"><span data-stu-id="a4159-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-176">Valore che specifica il formato degli eventi restituiti.</span><span class="sxs-lookup"><span data-stu-id="a4159-176">A value that specifies the format of the returned events.</span></span> <span data-ttu-id="a4159-177">*Format* può essere "Events" o "informazioni sulla".</span><span class="sxs-lookup"><span data-stu-id="a4159-177">*FORMAT* can be "Events" or "RenderedText".</span></span> <span data-ttu-id="a4159-178">Quando il valore è "informazioni sulla", gli eventi vengono restituiti con le stringhe localizzate, ad esempio le stringhe di descrizione evento, associate agli eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-178">When the value is "RenderedText", the events are returned with the localized strings (such as event description strings) attached to the events.</span></span> <span data-ttu-id="a4159-179">Il valore predefinito di *Format* è "informazioni sulla".</span><span class="sxs-lookup"><span data-stu-id="a4159-179">The default value of *FORMAT* is "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="a4159-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *impostazioni locali***</span><span class="sxs-lookup"><span data-stu-id="a4159-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-181">Valore che specifica le impostazioni locali per il recapito delle stringhe localizzate nel formato di testo di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="a4159-181">A value that specifies the locale for delivery of the localized strings in rendered text format.</span></span> <span data-ttu-id="a4159-182">Le *impostazioni locali* sono un identificatore di lingua/paese, ad esempio, "en-US".</span><span class="sxs-lookup"><span data-stu-id="a4159-182">*LOCALE* is a language/country culture identifier, for example, "EN-us".</span></span> <span data-ttu-id="a4159-183">Questo parametro è valido solo quando il parametro/CF è impostato su "informazioni sulla".</span><span class="sxs-lookup"><span data-stu-id="a4159-183">This parameter is only valid when the /cf parameter is set to "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="a4159-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/Ree: \[ *valore*\]**</span><span class="sxs-lookup"><span data-stu-id="a4159-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree:\[*VALUE*\]**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-185">Valore che specifica gli eventi da recapitare per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-185">A value that specifies which events are to be delivered for the subscription.</span></span> <span data-ttu-id="a4159-186">Il *valore* può essere true o false.</span><span class="sxs-lookup"><span data-stu-id="a4159-186">*VALUE* can be true or false.</span></span> <span data-ttu-id="a4159-187">Quando *value* è true, tutti gli eventi esistenti vengono letti dalle origini eventi della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-187">When *VALUE* is true, all existing events are read from the subscription event sources.</span></span> <span data-ttu-id="a4159-188">Quando *value* è false, vengono recapitati solo gli eventi future (in arrivo).</span><span class="sxs-lookup"><span data-stu-id="a4159-188">When *VALUE* is false, only future (arriving) events are delivered.</span></span> <span data-ttu-id="a4159-189">Il valore predefinito è true se/Ree viene specificato senza un valore e il valore predefinito è false se/Ree non è specificato.</span><span class="sxs-lookup"><span data-stu-id="a4159-189">The default is true when /ree is specified without a value, and the default is false if /ree is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF: *nomefile***</span><span class="sxs-lookup"><span data-stu-id="a4159-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-191">Valore che specifica il registro eventi locale utilizzato per archiviare gli eventi ricevuti dalla sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a4159-191">A value that specifies the local event log that is used to store events received from the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN: *server di pubblicazione***</span><span class="sxs-lookup"><span data-stu-id="a4159-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-193">Valore che specifica il nome dell'autore di eventi (provider).</span><span class="sxs-lookup"><span data-stu-id="a4159-193">A value that specifies the event publisher (provider) name.</span></span> <span data-ttu-id="a4159-194">Deve essere un server di pubblicazione che possiede o importa il log specificato dal parametro/LF.</span><span class="sxs-lookup"><span data-stu-id="a4159-194">It must be a publisher which owns or imports the log specified by the /lf parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM: *modalità***</span><span class="sxs-lookup"><span data-stu-id="a4159-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-196">Valore che specifica la modalità di recapito della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-196">A value that specifies the subscription delivery mode.</span></span> <span data-ttu-id="a4159-197">La *modalità* può essere push o pull.</span><span class="sxs-lookup"><span data-stu-id="a4159-197">*MODE* can be either push or pull.</span></span> <span data-ttu-id="a4159-198">Questa opzione è valida solo se il parametro/cm è impostato su Custom.</span><span class="sxs-lookup"><span data-stu-id="a4159-198">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI: *numero***</span><span class="sxs-lookup"><span data-stu-id="a4159-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-200">Valore che specifica il numero massimo di elementi per il recapito in batch nella sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a4159-200">A value that specifies the maximum number of items for batched delivery in the event subscription.</span></span> <span data-ttu-id="a4159-201">Questa opzione è valida solo se il parametro/cm è impostato su Custom.</span><span class="sxs-lookup"><span data-stu-id="a4159-201">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/DMLT: *MS***</span><span class="sxs-lookup"><span data-stu-id="a4159-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-203">Valore che specifica la latenza massima consentita per la distribuzione di un batch di eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-203">A value that specifies the maximum latency allowed in delivering a batch of events.</span></span> <span data-ttu-id="a4159-204">MS è il numero di millisecondi consentiti.</span><span class="sxs-lookup"><span data-stu-id="a4159-204">MS is the number of milliseconds allowed.</span></span> <span data-ttu-id="a4159-205">Questo parametro è valido solo se il parametro/cm è impostato su Custom.</span><span class="sxs-lookup"><span data-stu-id="a4159-205">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/Hi: *MS***</span><span class="sxs-lookup"><span data-stu-id="a4159-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-207">Valore che specifica l'intervallo di heartbeat per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-207">A value that specifies the heartbeat interval for the subscription.</span></span> <span data-ttu-id="a4159-208">*MS* è il numero di millisecondi utilizzati nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="a4159-208">*MS* is the number of milliseconds used in the interval.</span></span> <span data-ttu-id="a4159-209">Questo parametro è valido solo se il parametro/cm è impostato su Custom.</span><span class="sxs-lookup"><span data-stu-id="a4159-209">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *TRANSportaname***</span><span class="sxs-lookup"><span data-stu-id="a4159-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-211">Valore che specifica il nome del trasporto utilizzato per la connessione al computer di origine dell'evento remoto.</span><span class="sxs-lookup"><span data-stu-id="a4159-211">A value that specifies the name of the transport used to connect to the remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ESA: *\_ origine evento***</span><span class="sxs-lookup"><span data-stu-id="a4159-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *EVENT\_SOURCE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-213">Valore che specifica l'indirizzo di un computer di origine evento.</span><span class="sxs-lookup"><span data-stu-id="a4159-213">A value that specifies the address of an event source computer.</span></span> <span data-ttu-id="a4159-214">*Evento \_ SOURCE* è una stringa che identifica un computer di origine evento utilizzando il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a4159-214">*EVENT\_SOURCE* is a string that identifies an event source computer using the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span> <span data-ttu-id="a4159-215">Questo parametro può essere utilizzato con i parametri/ESE,/AES,/res o/un e/up.</span><span class="sxs-lookup"><span data-stu-id="a4159-215">This parameter can be used with the /ese, /aes, /res, or /un and /up parameters.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ESE: *valore***</span><span class="sxs-lookup"><span data-stu-id="a4159-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-217">Valore che determina se abilitare o disabilitare un'origine evento.</span><span class="sxs-lookup"><span data-stu-id="a4159-217">A value that determines whether to enable or disable an event source.</span></span> <span data-ttu-id="a4159-218">Il *valore* può essere true o false.</span><span class="sxs-lookup"><span data-stu-id="a4159-218">*VALUE* can be true or false.</span></span> <span data-ttu-id="a4159-219">Il valore predefinito è true, che Abilita l'origine evento.</span><span class="sxs-lookup"><span data-stu-id="a4159-219">The default value is true, which enables the event source.</span></span> <span data-ttu-id="a4159-220">Questo parametro viene usato solo se viene usato il parametro/ESA.</span><span class="sxs-lookup"><span data-stu-id="a4159-220">This parameter is only used if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span><span class="sxs-lookup"><span data-stu-id="a4159-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-222">Valore che aggiunge l'origine evento specificata dal parametro/ESA se l'origine evento non fa già parte della sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-222">A value that adds the event source specified by the /esa parameter if the event source is not already part of the event subscription.</span></span> <span data-ttu-id="a4159-223">Se il computer specificato dal parametro/ESA fa già parte della sottoscrizione, viene visualizzato un errore.</span><span class="sxs-lookup"><span data-stu-id="a4159-223">If the computer specified by the /esa parameter is already a part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="a4159-224">Questo parametro è consentito solo se viene usato il parametro/ESA.</span><span class="sxs-lookup"><span data-stu-id="a4159-224">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-225"><span id="_res"></span><span id="_RES"></span>**/res**</span><span class="sxs-lookup"><span data-stu-id="a4159-225"><span id="_res"></span><span id="_RES"></span>**/res**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-226">Valore che rimuove l'origine evento specificata dal parametro/ESA se l'origine evento fa già parte della sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-226">A value that removes the event source specified by the /esa parameter if the event source is already part of the event subscription.</span></span> <span data-ttu-id="a4159-227">Se il computer specificato dal parametro/ESA non fa parte della sottoscrizione, viene visualizzato un errore.</span><span class="sxs-lookup"><span data-stu-id="a4159-227">If the computer specified by the /esa parameter is not part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="a4159-228">Questo parametro è consentito solo se viene usato il parametro/ESA.</span><span class="sxs-lookup"><span data-stu-id="a4159-228">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *nomeutente***</span><span class="sxs-lookup"><span data-stu-id="a4159-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-230">Valore che specifica il nome utente utilizzato nelle credenziali per la connessione all'origine evento specificata nel parametro/ESA.</span><span class="sxs-lookup"><span data-stu-id="a4159-230">A value that specifies the user name used in the credentials to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="a4159-231">Questo parametro è consentito solo se viene usato il parametro/ESA.</span><span class="sxs-lookup"><span data-stu-id="a4159-231">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *password***</span><span class="sxs-lookup"><span data-stu-id="a4159-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-233">Valore che specifica la password per il nome utente specificato nel parametro/un.</span><span class="sxs-lookup"><span data-stu-id="a4159-233">A value that specifies the password for the user name specified in the /un parameter.</span></span> <span data-ttu-id="a4159-234">Le credenziali relative al nome utente e alla password vengono usate per connettersi all'origine evento specificata nel parametro/ESA.</span><span class="sxs-lookup"><span data-stu-id="a4159-234">The user name and password credentials are used to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="a4159-235">Questo parametro è consentito solo se viene usato il parametro/un.</span><span class="sxs-lookup"><span data-stu-id="a4159-235">This parameter is allowed only if the /un parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *TRANSPORTPORT***</span><span class="sxs-lookup"><span data-stu-id="a4159-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-237">Valore che specifica il numero di porta utilizzato dal trasporto quando ci si connette a un computer di origine evento remoto.</span><span class="sxs-lookup"><span data-stu-id="a4159-237">A value that specifies the port number used by the transport when connecting to a remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN: *nome***</span><span class="sxs-lookup"><span data-stu-id="a4159-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-239">Valore che specifica il nome DNS del computer locale.</span><span class="sxs-lookup"><span data-stu-id="a4159-239">A value that specifies the DNS name of the local computer.</span></span> <span data-ttu-id="a4159-240">Questo nome viene utilizzato dalle origini eventi Remote per eseguire il push degli eventi e deve essere utilizzato solo per le sottoscrizioni push.</span><span class="sxs-lookup"><span data-stu-id="a4159-240">This name is used by remote event sources to push back events and must be used for push subscriptions only.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT: *tipo***</span><span class="sxs-lookup"><span data-stu-id="a4159-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-242">Valore che specifica il tipo di credenziale utilizzato per l'accesso alle origini eventi remote.</span><span class="sxs-lookup"><span data-stu-id="a4159-242">A value that specifies the credential type used for accessing remote event sources.</span></span> <span data-ttu-id="a4159-243">*Type* può essere "default", "Negotiate", "digest", "Basic" o "LocalMachine".</span><span class="sxs-lookup"><span data-stu-id="a4159-243">*TYPE* can be "default", "negotiate", "digest", "basic", or "localmachine".</span></span> <span data-ttu-id="a4159-244">Il valore predefinito è "default".</span><span class="sxs-lookup"><span data-stu-id="a4159-244">The default is "default".</span></span> <span data-ttu-id="a4159-245">Questi valori sono definiti nell'enumerazione [**del \_ \_ \_ tipo di credenziali della sottoscrizione EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .</span><span class="sxs-lookup"><span data-stu-id="a4159-245">These values are defined in the [**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nomeutente***</span><span class="sxs-lookup"><span data-stu-id="a4159-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-247">Valore che imposta le credenziali utente condivise utilizzate per le origini eventi che non dispongono di credenziali utente personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a4159-247">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span>

> [!Note]  
> <span data-ttu-id="a4159-248">Se questo parametro viene utilizzato con l'opzione/c, le impostazioni relative a nome utente e password per le singole origini eventi del file di configurazione verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="a4159-248">If this parameter is used with the /c option, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="a4159-249">Se si desidera utilizzare credenziali diverse per un'origine evento specifica, è possibile eseguire l'override di questo valore specificando i parametri/un e/up per un'origine evento specifica nella riga di comando di un altro comando set-Subscription.</span><span class="sxs-lookup"><span data-stu-id="a4159-249">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="a4159-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *password***</span><span class="sxs-lookup"><span data-stu-id="a4159-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-251">Valore che imposta la password utente per le credenziali utente condivise.</span><span class="sxs-lookup"><span data-stu-id="a4159-251">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="a4159-252">Quando la *password* è impostata su \* (asterisco), la password viene letta dalla console.</span><span class="sxs-lookup"><span data-stu-id="a4159-252">When *PASSWORD* is set to \* (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="a4159-253">Questa opzione è valida solo quando viene specificato il parametro/CUN.</span><span class="sxs-lookup"><span data-stu-id="a4159-253">This option is only valid when the /cun parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA: *identificazione personale***</span><span class="sxs-lookup"><span data-stu-id="a4159-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *THUMBPRINTS***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-255">Valore che imposta l'elenco di stampe Thumb del certificato dell'autorità emittente, in un elenco delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="a4159-255">A value that sets the list of issuer certificate thumb prints, in a comma-separated list.</span></span>

> [!Note]  
> <span data-ttu-id="a4159-256">Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a4159-256">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="a4159-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/As: *consentito***</span><span class="sxs-lookup"><span data-stu-id="a4159-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ALLOWED***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-258">Valore che imposta un elenco delimitato da virgole di stringa che specifica i nomi DNS dei computer non di dominio a cui è consentito avviare le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a4159-258">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are allowed to initiate subscriptions.</span></span> <span data-ttu-id="a4159-259">I nomi possono essere specificati utilizzando caratteri jolly, ad esempio " \* . mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="a4159-259">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="a4159-260">Per impostazione predefinita, tale elenco è vuoto.</span><span class="sxs-lookup"><span data-stu-id="a4159-260">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="a4159-261">Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a4159-261">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="a4159-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS: *negato***</span><span class="sxs-lookup"><span data-stu-id="a4159-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-263">Valore che imposta un elenco delimitato da virgole di stringa che specifica i nomi DNS dei computer non di dominio che non sono autorizzati ad avviare le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a4159-263">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are not allowed to initiate subscriptions.</span></span> <span data-ttu-id="a4159-264">I nomi possono essere specificati utilizzando caratteri jolly, ad esempio " \* . mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="a4159-264">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="a4159-265">Per impostazione predefinita, tale elenco è vuoto.</span><span class="sxs-lookup"><span data-stu-id="a4159-265">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="a4159-266">Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a4159-266">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="a4159-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC: *SDDL***</span><span class="sxs-lookup"><span data-stu-id="a4159-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-268">Valore che imposta una stringa, in formato SDDL, che specifica quali computer del dominio sono consentiti o meno per avviare le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a4159-268">A value that sets a string, in SDDL format, that specifies which domain computers are allowed or not allowed to initiate subscriptions.</span></span> <span data-ttu-id="a4159-269">Il valore predefinito è consentire a tutti i computer del dominio di avviare le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a4159-269">The default is to allow all domain computers to initiate subscriptions.</span></span>

> [!Note]  
> <span data-ttu-id="a4159-270">Questa opzione è specifica solo per le sottoscrizioni avviate dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a4159-270">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> </dl>

## <a name="create-a-new-subscription"></a><span data-ttu-id="a4159-271">Creare una nuova sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="a4159-271">Create a New Subscription</span></span>

<span data-ttu-id="a4159-272">La sintassi seguente consente di creare una sottoscrizione di eventi per gli eventi in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="a4159-272">The following syntax is used to create an event subscription for events on a remote computer.</span></span>

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a><span data-ttu-id="a4159-273">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4159-273">Remarks</span></span>

<span data-ttu-id="a4159-274">Quando si specifica un nome utente o una password non corretta nel comando **wecutil CS** , non viene segnalato alcun errore fino a quando non si visualizza lo stato di runtime della sottoscrizione usando il comando **wecutil gr** .</span><span class="sxs-lookup"><span data-stu-id="a4159-274">When an incorrect username or password is specified in the **wecutil cs** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="creation-parameters"></a><span data-ttu-id="a4159-275">Parametri di creazione</span><span class="sxs-lookup"><span data-stu-id="a4159-275">Creation Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4159-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**FILE di configurazione \_**</span><span class="sxs-lookup"><span data-stu-id="a4159-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**CONFIGURATION\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-277">Valore che specifica il percorso del file XML che contiene le informazioni di configurazione della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-277">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="a4159-278">Il percorso può essere assoluto o relativo alla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="a4159-278">The path can be absolute or relative to the current directory.</span></span>

<span data-ttu-id="a4159-279">Il codice XML seguente è un esempio di file di configurazione della sottoscrizione che crea una sottoscrizione avviata dall'agente di raccolta per l'invio di eventi dal registro eventi dell'applicazione di un computer remoto al log ForwardedEvents.</span><span class="sxs-lookup"><span data-stu-id="a4159-279">The following XML is an example of a subscription configuration file that creates a collector initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



<span data-ttu-id="a4159-280">Il codice XML seguente è un esempio di file di configurazione della sottoscrizione che consente di creare una sottoscrizione avviata dall'origine per l'invio di eventi dal registro eventi dell'applicazione di un computer remoto al log ForwardedEvents.</span><span class="sxs-lookup"><span data-stu-id="a4159-280">The following XML is an example of a subscription configuration file that creates a source initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> <span data-ttu-id="a4159-281">Quando si crea una sottoscrizione avviata dall'origine, se **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** / **IssuerCAList**, **AllowedSubjectList** e **DeniedSubjectList** sono tutti vuoti, viene fornito un valore predefinito per **AllowedSourceDomainComputers** -"O:NSG: NSD: (a;; GA;;;D C) (A;; GA;;; NS) ".</span><span class="sxs-lookup"><span data-stu-id="a4159-281">When creating a source initiated subscription, if **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers**/**IssuerCAList**, **AllowedSubjectList**, and **DeniedSubjectList** are all empty, then a default will be provided for **AllowedSourceDomainComputers** - "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)".</span></span> <span data-ttu-id="a4159-282">Questa impostazione predefinita SDDL concede i membri del gruppo di dominio computer del dominio, nonché il gruppo di servizi di rete locale (per il server d'invio locale), la possibilità di generare eventi per questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-282">This SDDL default grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="a4159-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nomeutente***</span><span class="sxs-lookup"><span data-stu-id="a4159-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-284">Valore che imposta le credenziali utente condivise utilizzate per le origini eventi che non dispongono di credenziali utente personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a4159-284">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span> <span data-ttu-id="a4159-285">Questo valore si applica solo alle sottoscrizioni avviate dall'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="a4159-285">This value applies to collector initiated subscriptions only.</span></span>

> [!Note]  
> <span data-ttu-id="a4159-286">Se si specifica questo parametro, le impostazioni relative a nome utente e password per le singole origini eventi del file di configurazione verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="a4159-286">If this parameter is specified, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="a4159-287">Se si desidera utilizzare credenziali diverse per un'origine evento specifica, è possibile eseguire l'override di questo valore specificando i parametri/un e/up per un'origine evento specifica nella riga di comando di un altro comando set-Subscription.</span><span class="sxs-lookup"><span data-stu-id="a4159-287">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="a4159-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *password***</span><span class="sxs-lookup"><span data-stu-id="a4159-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-289">Valore che imposta la password utente per le credenziali utente condivise.</span><span class="sxs-lookup"><span data-stu-id="a4159-289">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="a4159-290">Quando la *password* è impostata su " \* " (asterisco), la password viene letta dalla console.</span><span class="sxs-lookup"><span data-stu-id="a4159-290">When *PASSWORD* is set to "\*" (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="a4159-291">Questa opzione è valida solo quando viene specificato il parametro/CUN.</span><span class="sxs-lookup"><span data-stu-id="a4159-291">This option is only valid when the /cun parameter is specified.</span></span>

</dd> </dl>

## <a name="delete-a-subscription"></a><span data-ttu-id="a4159-292">Eliminare una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="a4159-292">Delete a Subscription</span></span>

<span data-ttu-id="a4159-293">La sintassi seguente consente di eliminare una sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-293">The following syntax is used to delete an event subscription.</span></span>

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a><span data-ttu-id="a4159-294">Parametri di eliminazione</span><span class="sxs-lookup"><span data-stu-id="a4159-294">Deletion Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4159-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**</span><span class="sxs-lookup"><span data-stu-id="a4159-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-296">Stringa che identifica in modo univoco una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-296">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a4159-297">Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-297">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="a4159-298">La sottoscrizione identificata in questo parametro verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="a4159-298">The subscription identified in this parameter will be deleted.</span></span>

</dd> </dl>

## <a name="retry-a-subscription"></a><span data-ttu-id="a4159-299">Ritentare una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="a4159-299">Retry a subscription</span></span>

<span data-ttu-id="a4159-300">La sintassi seguente consente di ritentare una sottoscrizione inattiva tentando di riattivare tutte o origini eventi specificate stabilendo una connessione a ogni origine evento e inviando una richiesta di sottoscrizione remota all'origine evento.</span><span class="sxs-lookup"><span data-stu-id="a4159-300">The following syntax is used to retry an inactive subscription by attempting to reactivate all or specified event sources by establishing a connection to each event source and sending a remote subscription request to the event source.</span></span> <span data-ttu-id="a4159-301">Le origini evento disabilitate non vengono ritentate.</span><span class="sxs-lookup"><span data-stu-id="a4159-301">Disabled event sources are not retried.</span></span>

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a><span data-ttu-id="a4159-302">Parametri di ripetizione dei tentativi</span><span class="sxs-lookup"><span data-stu-id="a4159-302">Retry Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4159-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ID sottoscrizione**</span><span class="sxs-lookup"><span data-stu-id="a4159-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-304">Stringa che identifica in modo univoco una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-304">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="a4159-305">Questo identificatore viene specificato nell'elemento **SubscriptionId** nel file di configurazione XML utilizzato per creare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a4159-305">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="a4159-306">Verrà eseguito un nuovo tentativo di sottoscrizione identificata in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a4159-306">The subscription identified in this parameter will be retried.</span></span>

</dd> <dt>

<span data-ttu-id="a4159-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_origine evento**</span><span class="sxs-lookup"><span data-stu-id="a4159-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a4159-308">Valore che identifica un computer che rappresenta un'origine evento per una sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="a4159-308">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="a4159-309">Questo valore può essere il nome di dominio completo per il computer, il nome NetBIOS o l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a4159-309">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a><span data-ttu-id="a4159-310">Configurare il servizio raccolta eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="a4159-310">Configure the Windows Event Collector Service</span></span>

<span data-ttu-id="a4159-311">La sintassi seguente viene utilizzata per configurare il servizio raccolta eventi di Windows per garantire che le sottoscrizioni di eventi possano essere create e sostenute attraverso il riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="a4159-311">The following syntax is used to configure the Windows Event Collector service to ensure event subscriptions can be created and sustained through computer restarts.</span></span> <span data-ttu-id="a4159-312">Sono incluse le procedure seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4159-312">This includes the following procedure:</span></span>

<span data-ttu-id="a4159-313">**Per configurare il servizio raccolta eventi di Windows**</span><span class="sxs-lookup"><span data-stu-id="a4159-313">**To configure the Windows Event Collector service**</span></span>

1.  <span data-ttu-id="a4159-314">Attivare il canale ForwardedEvents se è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a4159-314">Enable the ForwardedEvents channel if it is disabled.</span></span>
2.  <span data-ttu-id="a4159-315">Ritardare l'avvio del servizio raccolta eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="a4159-315">Delay the start of the Windows Event Collector service.</span></span>
3.  <span data-ttu-id="a4159-316">Se non è in esecuzione, avviare il servizio Raccolta eventi Windows.</span><span class="sxs-lookup"><span data-stu-id="a4159-316">Start the Windows Event Collector service if it is not running.</span></span>

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a><span data-ttu-id="a4159-317">Configurare i parametri dell'agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="a4159-317">Configure Event Collector Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4159-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *valore***</span><span class="sxs-lookup"><span data-stu-id="a4159-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="a4159-319">Valore che determina se il comando di configurazione rapida richiederà una conferma.</span><span class="sxs-lookup"><span data-stu-id="a4159-319">A value that determines whether the quick-config command will prompt for confirmation.</span></span> <span data-ttu-id="a4159-320">Il valore può essere true o false.</span><span class="sxs-lookup"><span data-stu-id="a4159-320">VALUE can be true or false.</span></span> <span data-ttu-id="a4159-321">Se il valore è true, il comando richiederà una conferma.</span><span class="sxs-lookup"><span data-stu-id="a4159-321">If VALUE is true, then the command will prompt for confirmation.</span></span> <span data-ttu-id="a4159-322">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="a4159-322">The default value is false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4159-323">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4159-323">Requirements</span></span>



| <span data-ttu-id="a4159-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4159-324">Requirement</span></span> | <span data-ttu-id="a4159-325">Valore</span><span class="sxs-lookup"><span data-stu-id="a4159-325">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a4159-326">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4159-326">Minimum supported client</span></span><br/> | <span data-ttu-id="a4159-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4159-327">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a4159-328">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4159-328">Minimum supported server</span></span><br/> | <span data-ttu-id="a4159-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4159-329">Windows Server 2008</span></span><br/> |



 

 





