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
# <a name="activescripteventconsumer-class"></a>Classe ActiveScriptEventConsumer

La classe **ActiveScriptEventConsumer** esegue uno script predefinito in un linguaggio di scripting arbitrario quando viene recapitato un evento. Questa classe è uno dei consumer di eventi standard forniti da WMI. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



È possibile configurare le prestazioni di tutte le istanze di **ActiveScriptEventConsumer** in un sistema impostando i valori della proprietà [**timeout**](scriptingstandardconsumersetting.md) o **MaximumScripts** nella singola istanza di **ScriptingStandardConsumerSetting**.

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

La classe **ActiveScriptEventConsumer** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **ActiveScriptEventConsumer** dispone di queste proprietà.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che rappresenta l'ID di sicurezza (SID), che identifica in modo univoco l'autore del consumer di eventi di script attivo. Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero, in secondi, consentito per l'esecuzione dello script. Se è 0 (zero), ovvero l'impostazione predefinita, lo script non viene terminato.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer a cui WMI invia gli eventi. Per convenzione degli utenti standard Microsoft, il consumer di script non può essere eseguito in modalità remota. I consumer di terze parti possono usare questa proprietà anche. Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Massima coda, in byte, del consumer di eventi di script attivo. Questa proprietà viene ereditata da [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Identificatore univoco del consumer di eventi. Se si rinomina il consumer, il risultato è due consumer uguali con nomi diversi.

</dd> <dt>

**ScriptFileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del file da cui viene letto il testo dello script, progettato come alternativa alla specifica del testo dello script nella proprietà **ScriptText** . Questa proprietà deve essere **null** se la proprietà **ScriptText** non è **null**.

> [!Note]  
> Quando si specifica **ScriptFileName**, è importante proteggere il file eseguibile che si sta avviando. Se il file eseguibile non si trova in un percorso sicuro o protetto con un elenco di controllo di accesso (ACL) sicuro, chiunque può sostituire il file eseguibile con uno diverso. Per ulteriori informazioni sugli ACL, vedere [creazione di un descrittore di sicurezza (SD) per un nuovo oggetto in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**ScriptingEngine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del motore di script da usare, ad esempio "VBScript". Questa proprietà non può essere **null**.

</dd> <dt>

**ScriptText**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Testo dello script espresso in un linguaggio noto al motore di script. Questa proprietà deve essere **null** se la proprietà **ScriptFileName** non è **null**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa classe è derivata dalla classe astratta [**\_ \_ EventConsumer**](--eventconsumer.md) . Si trova nello \\ spazio dei nomi della sottoscrizione radice.

Quando il testo di uno script viene specificato nell'istanza del consumer di eventi, lo script può accedere all'istanza dell'evento nella variabile di ambiente script **TargetEvent**.

Gli script vengono eseguiti nel contesto di sicurezza LocalSystem. Come misura di sicurezza, solo un amministratore di sistema locale o un amministratore di dominio può configurare il consumer di scripting. I diritti di accesso non vengono controllati fino alla fase di esecuzione. Dopo la configurazione del consumer, qualsiasi utente può attivare l'evento che determina l'esecuzione dello script.

Il mancato caricamento del motore di scripting o l'analisi e la convalida dello script viene considerato un errore. Vengono considerati anche errori i codici restituiti dallo script e il termine dello script tramite un timeout.

**ScriptText** o **ScriptFileName** non devono essere **null**. Se entrambe le proprietà sono **null** o Not **null**, viene generato un errore.

Quando WMI viene eseguito come servizio, gli script eseguiti da **ActiveScriptEventConsumer** non generano l'output dello schermo. Gli script che usano **MsgBox** vengono eseguiti, ma non visualizzano informazioni sullo schermo. L'esecuzione del servizio WMI come file eseguibile non è supportata, ma WMI consente agli script che utilizzano la funzione **MsgBox** di visualizzare l'output o accettare l'input dell'utente. Nessuno dei metodi forniti dall'oggetto [WScript](/previous-versions//at5ydy31(v=vs.85)) può essere usato perché **ActiveScriptEventConsumer** non usa Windows script host (WSH).

## <a name="examples"></a>Esempio

Nell'esempio di PowerShell [per la creazione di una registrazione di eventi WMI permanenti per il monitoraggio dei file](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) nella raccolta TechNet viene usato **ActiveScriptEventConsumer** come parte di uno script complesso per configurare la registrazione di un evento WMI permanente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | \\Sottoscrizione radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons. mof</dt> </dl> |
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

 

