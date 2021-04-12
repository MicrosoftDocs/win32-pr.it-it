---
description: La classe singleton ScriptingStandardConsumerSetting fornisce dati di registrazione comuni a tutte le istanze della classe consumer standard ActiveScriptEventConsumer.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Classe ScriptingStandardConsumerSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226823"
---
# <a name="scriptingstandardconsumersetting-class"></a>Classe ScriptingStandardConsumerSetting

La classe singleton **ScriptingStandardConsumerSetting** fornisce dati di registrazione comuni a tutte le istanze della classe consumer standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) . Un'istanza di **ActiveScriptEventConsumer** usa le proprietà **MaximumScripts** e **timeout** . Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a>Members

La classe **ScriptingStandardConsumerSetting** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **ScriptingStandardConsumerSetting** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](standard-qualifiers.md) (64)
</dt> </dl>

Una breve descrizione di un oggetto a una stringa di riga. Contiene la stringa **ScriptingStandardConsumerSetting** perché si tratta di una classe singleton.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale di un oggetto.

</dd> <dt>

**MaximumScripts**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Numero massimo di script eseguiti prima che un consumer avvii una nuova istanza. Per eliminare le perdite di memoria dagli script, arrestare regolarmente il consumer. Il valore predefinito è 300.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](standard-qualifiers.md) (256)
</dt> </dl>

Identificatore per l'oggetto Setting.

</dd> <dt>

**Timeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**unità**](standard-qualifiers.md) ("minuti")
</dt> </dl>

Numero massimo di minuti prima che un consumer avvii una nuova istanza. Se è 0 (zero), la proprietà **MaximumScripts** controlla la durata del consumer. L'intervallo valido per il **timeout** è compreso tra 0 e 71.000 e il valore predefinito è 0 (zero).

</dd> </dl>

## <a name="remarks"></a>Commenti

La singola istanza della classe **ScriptingStandardConsumerSetting** risiede nello \\ spazio dei nomi CIMV2 radice.

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

[**\_Impostazione CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[Classi consumer standard](standard-consumer-classes.md)
</dt> <dt>

[Esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Creazione di un consumer logico](creating-a-logical-consumer.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

