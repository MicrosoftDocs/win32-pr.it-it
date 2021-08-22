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
ms.openlocfilehash: acf7ef4b4207f72cbaee61c0aaad8b2279419682bdddbeb4373c36c6868b8fce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557834"
---
# <a name="activescripteventconsumer-class"></a>Classe ActiveScriptEventConsumer

La **classe ActiveScriptEventConsumer** esegue uno script predefinito in un linguaggio di scripting arbitrario quando viene recapitato un evento. Questa classe è uno dei consumer di eventi standard forniti da WMI. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



È possibile configurare le prestazioni di tutte le istanze di **ActiveScriptEventConsumer** in un sistema impostando i valori della proprietà [**Timeout**](scriptingstandardconsumersetting.md) o **MaximumScripts** nella singola istanza di **ScriptingStandardConsumerSetting**.

## <a name="syntax"></a>Sintassi

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

## <a name="members"></a>Members

La **classe ActiveScriptEventConsumer** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe ActiveScriptEventConsumer** ha queste proprietà.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che rappresenta l'identificatore di sicurezza (SID), che identifica in modo univoco l'autore del consumer di eventi di script attivo. Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero, in secondi, di esecuzione dello script. Se 0 (zero), che è il valore predefinito, lo script non viene terminato.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer a cui WMI invia gli eventi. Per convenzione dei consumer standard Microsoft, il consumer di script non può essere eseguito in modalità remota. Anche i consumer di terze parti possono usare questa proprietà. Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coda massima, in byte, per il consumer di eventi script attivo. Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Identificatore univoco per il consumer di eventi. Se si rinomina il consumer, il risultato sarà due consumer uguali con nomi diversi.

</dd> <dt>

**ScriptFileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del file da cui viene letto il testo dello script, inteso come alternativa alla specifica del testo dello script nella **proprietà ScriptText.** Questa proprietà deve essere **NULL** se la **proprietà ScriptText** non è **NULL.**

> [!Note]  
> Quando si specifica **ScriptFileName**, è importante proteggere il file eseguibile che si sta avviando. Se l'eseguibile non si trova in una posizione sicura o è protetto con un elenco di controllo di accesso sicuro ( ACL), chiunque può sostituire il file eseguibile con un altro. Per altre informazioni sugli ACL, vedere Creazione di un descrittore di sicurezza [(SD) per un nuovo oggetto in C++.](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

 

</dd> <dt>

**ScriptingEngine**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del motore di scripting da usare, ad esempio "VBScript". Questa proprietà non può essere **NULL.**

</dd> <dt>

**ScriptText**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Testo dello script espresso in un linguaggio noto al motore di scripting. Questa proprietà deve essere **NULL** se la **proprietà ScriptFileName** non è **NULL.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe è derivata dalla [**\_ \_ classe astratta EventConsumer.**](--eventconsumer.md) Si trova nello spazio dei nomi della \\ sottoscrizione radice.

Quando il testo di uno script viene specificato nell'istanza del consumer di eventi, lo script ha accesso all'istanza dell'evento nella variabile di ambiente **script TargetEvent**.

Gli script vengono eseguiti nel contesto di sicurezza LocalSystem. Come misura di sicurezza, solo un amministratore di sistema locale o un amministratore di dominio può configurare il consumer di scripting. I diritti di accesso non vengono controllati fino alla fase di esecuzione. Dopo la configurazione del consumer, qualsiasi utente può attivare l'evento che causa l'esecuzione dello script su .

Il mancato caricamento del motore di scripting o l'analisi e la convalida dello script sono considerati un errore. Anche i codici di errore restituiti dallo script e la terminazione dello script tramite un timeout vengono considerati errori.

**ScriptText o** **ScriptFileName** non deve essere **NULL.** Se entrambe le proprietà **sono NULL** o **non NULL,** viene generato un errore.

Quando WMI viene eseguito come servizio, gli script eseguiti da **ActiveScriptEventConsumer** non generano l'output dello schermo. Gli script che **usano MsgBox** vengono eseguiti, ma non visualizzano informazioni sullo schermo. L'esecuzione del servizio WMI come file eseguibile non è supportata, ma WMI consente agli script che usano la funzione **MsgBox** di visualizzare l'output o accettare l'input dell'utente. Nessuno dei metodi forniti dall'oggetto [WScript](/previous-versions//at5ydy31(v=vs.85)) può essere usato perché **ActiveScriptEventConsumer** non usa Windows Script Host (WSH).

## <a name="examples"></a>Esempio

L'esempio di PowerShell Create [Permanent WMI Event registration](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) to monitor files in TechNet Gallery usa **ActiveScriptEventConsumer** come parte di uno script complesso per configurare una registrazione eventi WMI permanente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Sottoscrizione \\ radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi consumer standard](standard-consumer-classes.md)
</dt> <dt>

[Esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[Creazione di un consumer logico](creating-a-logical-consumer.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)
</dt> </dl>

 

