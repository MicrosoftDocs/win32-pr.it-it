---
description: Esegue uno script predefinito in un linguaggio di scripting arbitrario quando viene recapitato un evento.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: Classe ActiveScriptEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316580"
---
# <a name="activescripteventconsumer-class"></a><span data-ttu-id="1531d-103">Classe ActiveScriptEventConsumer</span><span class="sxs-lookup"><span data-stu-id="1531d-103">ActiveScriptEventConsumer class</span></span>

<span data-ttu-id="1531d-104">La classe **ActiveScriptEventConsumer** esegue uno script predefinito in un linguaggio di scripting arbitrario quando viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="1531d-104">The **ActiveScriptEventConsumer** class runs a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span> <span data-ttu-id="1531d-105">Questa classe è uno dei consumer di eventi standard forniti da WMI.</span><span class="sxs-lookup"><span data-stu-id="1531d-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="1531d-106">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="1531d-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



<span data-ttu-id="1531d-107">È possibile configurare le prestazioni di tutte le istanze di **ActiveScriptEventConsumer** in un sistema impostando i valori della proprietà [**timeout**](scriptingstandardconsumersetting.md) o **MaximumScripts** nella singola istanza di **ScriptingStandardConsumerSetting**.</span><span class="sxs-lookup"><span data-stu-id="1531d-107">You can configure the performance of all instances of **ActiveScriptEventConsumer** on a system by setting the values of either the [**Timeout**](scriptingstandardconsumersetting.md) or **MaximumScripts** property in the single instance of **ScriptingStandardConsumerSetting**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1531d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1531d-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a><span data-ttu-id="1531d-109">Members</span><span class="sxs-lookup"><span data-stu-id="1531d-109">Members</span></span>

<span data-ttu-id="1531d-110">La classe **ActiveScriptEventConsumer** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1531d-110">The **ActiveScriptEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="1531d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1531d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1531d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1531d-112">Properties</span></span>

<span data-ttu-id="1531d-113">La classe **ActiveScriptEventConsumer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1531d-113">The **ActiveScriptEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1531d-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="1531d-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1531d-115">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1531d-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1531d-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1531d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1531d-117">Matrice che rappresenta l'ID di sicurezza (SID), che identifica in modo univoco l'autore del consumer di eventi di script attivo.</span><span class="sxs-lookup"><span data-stu-id="1531d-117">Array that represents the security identifier (SID), which uniquely identifies the creator of the Active Script Event consumer.</span></span> <span data-ttu-id="1531d-118">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="1531d-118">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1531d-119">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="1531d-119">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1531d-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1531d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1531d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1531d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1531d-122">Numero, in secondi, consentito per l'esecuzione dello script.</span><span class="sxs-lookup"><span data-stu-id="1531d-122">Number, in seconds, that the script is allowed to run.</span></span> <span data-ttu-id="1531d-123">Se è 0 (zero), ovvero l'impostazione predefinita, lo script non viene terminato.</span><span class="sxs-lookup"><span data-stu-id="1531d-123">If 0 (zero), which is the default, the script is not terminated.</span></span>

</dd> <dt>

<span data-ttu-id="1531d-124">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="1531d-124">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1531d-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1531d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1531d-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1531d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1531d-127">Nome del computer a cui WMI invia gli eventi.</span><span class="sxs-lookup"><span data-stu-id="1531d-127">Name of the computer to which WMI sends events.</span></span> <span data-ttu-id="1531d-128">Per convenzione degli utenti standard Microsoft, il consumer di script non può essere eseguito in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="1531d-128">By convention of Microsoft standard consumers, the script consumer cannot be run remotely.</span></span> <span data-ttu-id="1531d-129">I consumer di terze parti possono usare questa proprietà anche.</span><span class="sxs-lookup"><span data-stu-id="1531d-129">Third-party consumers can also use this property.</span></span> <span data-ttu-id="1531d-130">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="1531d-130">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1531d-131">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="1531d-131">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1531d-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1531d-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1531d-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1531d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1531d-134">Massima coda, in byte, del consumer di eventi di script attivo.</span><span class="sxs-lookup"><span data-stu-id="1531d-134">Maximum queue, in bytes, for the Active Script Event consumer.</span></span> <span data-ttu-id="1531d-135">Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="1531d-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1531d-136">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1531d-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1531d-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1531d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1531d-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1531d-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1531d-139">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1531d-139">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1531d-140">Identificatore univoco del consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="1531d-140">Unique identifier for the event consumer.</span></span> <span data-ttu-id="1531d-141">Se si rinomina il consumer, il risultato è due consumer uguali con nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="1531d-141">If you rename the consumer, the result is two equal consumers that have different names.</span></span>

</dd> <dt>

<span data-ttu-id="1531d-142">**ScriptFileName**</span><span class="sxs-lookup"><span data-stu-id="1531d-142">**ScriptFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1531d-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1531d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1531d-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1531d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1531d-145">Nome del file da cui viene letto il testo dello script, progettato come alternativa alla specifica del testo dello script nella proprietà **ScriptText** .</span><span class="sxs-lookup"><span data-stu-id="1531d-145">Name of the file from which the script text is read, intended as an alternative to specifying the text of the script in the **ScriptText** property.</span></span> <span data-ttu-id="1531d-146">Questa proprietà deve essere **null** se la proprietà **ScriptText** non è **null**.</span><span class="sxs-lookup"><span data-stu-id="1531d-146">This property must be **NULL** if the **ScriptText** property is not **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="1531d-147">Quando si specifica **ScriptFileName**, è importante proteggere il file eseguibile che si sta avviando.</span><span class="sxs-lookup"><span data-stu-id="1531d-147">When you specify the **ScriptFileName**, it is important to secure the executable that you are launching.</span></span> <span data-ttu-id="1531d-148">Se il file eseguibile non si trova in un percorso sicuro o protetto con un elenco di controllo di accesso (ACL) sicuro, chiunque può sostituire il file eseguibile con uno diverso.</span><span class="sxs-lookup"><span data-stu-id="1531d-148">If the executable is not in a secure location or secured with a strong access control list (ACL), anyone can replace the executable with a different one.</span></span> <span data-ttu-id="1531d-149">Per ulteriori informazioni sugli ACL, vedere [creazione di un descrittore di sicurezza (SD) per un nuovo oggetto in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="1531d-149">For more information about ACLs, see [Creating a Security Descriptor (SD) for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="1531d-150">**ScriptingEngine**</span><span class="sxs-lookup"><span data-stu-id="1531d-150">**ScriptingEngine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1531d-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1531d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1531d-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1531d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1531d-153">Nome del motore di script da usare, ad esempio "VBScript".</span><span class="sxs-lookup"><span data-stu-id="1531d-153">Name of the scripting engine to use, for example, "VBScript".</span></span> <span data-ttu-id="1531d-154">Questa proprietà non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="1531d-154">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1531d-155">**ScriptText**</span><span class="sxs-lookup"><span data-stu-id="1531d-155">**ScriptText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1531d-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1531d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1531d-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1531d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1531d-158">Testo dello script espresso in un linguaggio noto al motore di script.</span><span class="sxs-lookup"><span data-stu-id="1531d-158">Text of the script that is expressed in a language known to the scripting engine.</span></span> <span data-ttu-id="1531d-159">Questa proprietà deve essere **null** se la proprietà **ScriptFileName** non è **null**.</span><span class="sxs-lookup"><span data-stu-id="1531d-159">This property must be **NULL** if the **ScriptFileName** property is not **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1531d-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="1531d-160">Remarks</span></span>

<span data-ttu-id="1531d-161">Questa classe è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="1531d-161">This class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span> <span data-ttu-id="1531d-162">Si trova nello \\ spazio dei nomi della sottoscrizione radice.</span><span class="sxs-lookup"><span data-stu-id="1531d-162">It is located in the root\\subscription namespace.</span></span>

<span data-ttu-id="1531d-163">Quando il testo di uno script viene specificato nell'istanza del consumer di eventi, lo script può accedere all'istanza dell'evento nella variabile di ambiente script **TargetEvent**.</span><span class="sxs-lookup"><span data-stu-id="1531d-163">When the text of a script is specified in the event consumer instance, the script has access to the event instance in the script environment variable **TargetEvent**.</span></span>

<span data-ttu-id="1531d-164">Gli script vengono eseguiti nel contesto di sicurezza LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="1531d-164">The scripts run in the LocalSystem security context.</span></span> <span data-ttu-id="1531d-165">Come misura di sicurezza, solo un amministratore di sistema locale o un amministratore di dominio può configurare il consumer di scripting.</span><span class="sxs-lookup"><span data-stu-id="1531d-165">As a security measure, only a local system administrator or a domain administrator can configure the scripting consumer.</span></span> <span data-ttu-id="1531d-166">I diritti di accesso non vengono controllati fino alla fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1531d-166">Access rights are not checked until run time.</span></span> <span data-ttu-id="1531d-167">Dopo la configurazione del consumer, qualsiasi utente può attivare l'evento che determina l'esecuzione dello script.</span><span class="sxs-lookup"><span data-stu-id="1531d-167">After the consumer is configured, any user can trigger the event that causes the script to .</span></span>

<span data-ttu-id="1531d-168">Il mancato caricamento del motore di scripting o l'analisi e la convalida dello script viene considerato un errore.</span><span class="sxs-lookup"><span data-stu-id="1531d-168">Failure to load the scripting engine or parse and validate the script is considered a failure.</span></span> <span data-ttu-id="1531d-169">Vengono considerati anche errori i codici restituiti dallo script e il termine dello script tramite un timeout.</span><span class="sxs-lookup"><span data-stu-id="1531d-169">Error return codes from the script and terminating the script by using a time-out are also considered failures.</span></span>

<span data-ttu-id="1531d-170">**ScriptText** o **ScriptFileName** non devono essere **null**.</span><span class="sxs-lookup"><span data-stu-id="1531d-170">Either **ScriptText** or **ScriptFileName** must be not **NULL**.</span></span> <span data-ttu-id="1531d-171">Se entrambe le proprietà sono **null** o Not **null**, viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="1531d-171">If both properties are **NULL** or not **NULL**, an error is generated.</span></span>

<span data-ttu-id="1531d-172">Quando WMI viene eseguito come servizio, gli script eseguiti da **ActiveScriptEventConsumer** non generano l'output dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1531d-172">When WMI is run as a service, scripts run by **ActiveScriptEventConsumer** do not generate screen output.</span></span> <span data-ttu-id="1531d-173">Gli script che usano **MsgBox** vengono eseguiti, ma non visualizzano informazioni sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="1531d-173">Scripts that use **MsgBox** do run, but they do not display information on the screen.</span></span> <span data-ttu-id="1531d-174">L'esecuzione del servizio WMI come file eseguibile non è supportata, ma WMI consente agli script che utilizzano la funzione **MsgBox** di visualizzare l'output o accettare l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1531d-174">Running the WMI service as an executable file is not supported, but WMI allows scripts that use the **MsgBox** function to display output or accept user input.</span></span> <span data-ttu-id="1531d-175">Nessuno dei metodi forniti dall'oggetto [WScript](/previous-versions//at5ydy31(v=vs.85)) può essere usato perché **ActiveScriptEventConsumer** non usa Windows script host (WSH).</span><span class="sxs-lookup"><span data-stu-id="1531d-175">None of the methods provided by the [WScript](/previous-versions//at5ydy31(v=vs.85)) object can be used because **ActiveScriptEventConsumer** does not use Windows Script Host (WSH).</span></span>

## <a name="examples"></a><span data-ttu-id="1531d-176">Esempio</span><span class="sxs-lookup"><span data-stu-id="1531d-176">Examples</span></span>

<span data-ttu-id="1531d-177">Nell'esempio di PowerShell [per la creazione di una registrazione di eventi WMI permanenti per il monitoraggio dei file](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) nella raccolta TechNet viene usato **ActiveScriptEventConsumer** come parte di uno script complesso per configurare la registrazione di un evento WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="1531d-177">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **ActiveScriptEventConsumer** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1531d-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1531d-178">Requirements</span></span>



| <span data-ttu-id="1531d-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="1531d-179">Requirement</span></span> | <span data-ttu-id="1531d-180">Valore</span><span class="sxs-lookup"><span data-stu-id="1531d-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1531d-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1531d-181">Minimum supported client</span></span><br/> | <span data-ttu-id="1531d-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1531d-182">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1531d-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1531d-183">Minimum supported server</span></span><br/> | <span data-ttu-id="1531d-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1531d-184">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1531d-185">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1531d-185">Namespace</span></span><br/>                | <span data-ttu-id="1531d-186">\\Sottoscrizione radice</span><span class="sxs-lookup"><span data-stu-id="1531d-186">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="1531d-187">MOF</span><span class="sxs-lookup"><span data-stu-id="1531d-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1531d-188"><dt>Scrcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1531d-188"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="1531d-189">DLL</span><span class="sxs-lookup"><span data-stu-id="1531d-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1531d-190"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1531d-190"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1531d-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1531d-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1531d-192">Classi consumer standard</span><span class="sxs-lookup"><span data-stu-id="1531d-192">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="1531d-193">Esecuzione di uno script basato su un evento</span><span class="sxs-lookup"><span data-stu-id="1531d-193">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="1531d-194">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="1531d-194">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="1531d-195">Creazione di un consumer logico</span><span class="sxs-lookup"><span data-stu-id="1531d-195">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="1531d-196">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="1531d-196">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="1531d-197">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="1531d-197">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md)
</dt> </dl>

 

