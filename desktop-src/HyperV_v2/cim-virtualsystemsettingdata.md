---
description: Vengono descritti gli aspetti virtuali di un sistema virtuale tramite un set di proprietà specifiche della virtualizzazione. CIM \_ VirtualSystemSettingData viene usato anche come classe di primo livello delle configurazioni di sistema virtuale.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: Classe CIM_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315521"
---
# <a name="cim_virtualsystemsettingdata-class"></a>CIM \_ VirtualSystemSettingData (classe)

Vengono descritti gli aspetti virtuali di un sistema virtuale tramite un set di proprietà specifiche della virtualizzazione. **CIM \_ VirtualSystemSettingData** viene utilizzato anche come classe di primo livello delle configurazioni di sistema virtuale.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Members

La classe **CIM \_ VirtualSystemSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ VirtualSystemSettingData** dispone di queste proprietà.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da intraprendere per il sistema virtuale quando il software eseguito dal sistema virtuale ha esito negativo. Gli errori risolti da questa proprietà includono solo quelli che possono essere rilevati dalla piattaforma host, ad esempio una condizione di stato di attesa non interrompibili.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Riavvia** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Ripristina snapshot** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per il sistema virtuale quando l'host viene arrestato.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Disattiva** (2)


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Salva stato** (3)


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**Arresto** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da intraprendere sul sistema virtuale quando l'host viene avviato.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Riavvia se in precedenza attivo** (3)


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**Avvio sempre** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ritardo per l'azione di avvio. Questo valore è una variante di intervallo del tipo di dati **DateTime** .

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di sequenza per l'attivazione del sistema virtuale quando viene avviato il sistema host. Un numero inferiore indica l'attivazione precedente. Se una o più configurazioni mostrano lo stesso valore, la sequenza è dipendente dall'implementazione. Il valore "0" indica che la sequenza è dipendente dall'implementazione.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file della directory in cui sono archiviate le informazioni sulla configurazione del sistema virtuale. Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo del file in cui sono archiviate le informazioni sulla configurazione del sistema virtuale. Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** . Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID univoco della configurazione del sistema virtuale.

> [!Note]  
> **ConfigurationID** è diverso da **InstanceID** e viene assegnato dall'implementazione a un sistema virtuale o a una configurazione di sistema virtuale. **ConfigurationID** non è una chiave e lo stesso valore può verificarsi per più di un'istanza.

 

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della configurazione del sistema virtuale.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo del file della directory in cui sono archiviate le informazioni sul log per il sistema virtuale. Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** . Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene le note fornite dall'utente correlate al sistema virtuale.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file in cui sono archiviate le informazioni relative al ripristino del sistema virtuale. Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo della directory in cui vengono archiviate le informazioni sugli snapshot del sistema virtuale. Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** . Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo della directory in cui vengono archiviate le informazioni correlate di sospensione relative al sistema virtuale. Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** . Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo del file della directory in cui sono archiviati i file di scambio del sistema virtuale. Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** . Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome univoco del sistema all'interno della piattaforma di virtualizzazione. **VirtualSystemIdentifier** non è il nome host assegnato all'istanza del sistema operativo in esecuzione nel sistema virtuale, né un indirizzo IP o un indirizzo MAC assegnato a una delle porte di rete.

**VirtualSystemIdentifier** può contenere regole specifiche di implementazione, ad esempio semplici modelli o un'espressione regolare che può essere interpretata dall'implementazione durante l'impostazione di **VirtualSystemIdentifier**.

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di sistema virtuale.

> [!Note]  
> Se il tipo di sistema virtuale è sconosciuto, questo valore deve essere impostato su "DMTF: Unknown".

 

Questa proprietà viene formattata usando il formato ABNF (Augmented Naur Form) seguente:

vs-Type = DMTF-value/other-org-value/legacy-value; DMTF-value = "DMTF:" define-org ":" org-vs-Type; Other-org-value = defineing-org ":" org-vs-Type;

Il valore del formato ABNF precedente è:

-   *DMTF-value*   un valore della proprietà definito da DMTF ed è definito nella descrizione di questa proprietà.
-   *other-org-value*   è un valore di proprietà definito da un'entità di business diversa da DMTF e non è definito nella descrizione di questa proprietà.
-   *valore Legacy:*   valore della proprietà definito da un'entità di business diversa da DMTF e non è definito nella descrizione di questa proprietà. Questi valori sono consentiti, ma è consigliabile deprecarli nel tempo.
-   *definizione di-org*   un identificatore per l'entità business che definisce il tipo di sistema virtuale. Deve includere un nome con copyright, un marchio o un nome univoco di proprietà dell'entità di business. Non deve essere "DMTF" e non deve contenere i due punti.
-   *org-vs-digitare*   un identificatore per il tipo di sistema virtuale all'interno dell'entità di business che definisce. Deve essere univoco all'interno di define-org. org-vs-Type può usare qualsiasi carattere consentito per le stringhe CIM, ad eccezione dei seguenti: u0000-U001F (controlli Unicode C0), U0020 (spazio), U007F (controlli C0 Unicode) o U0080-U009F (controlli Unicode C1).
-   Se è necessario strutturare il valore in segmenti, è necessario che i segmenti siano separati da un solo segno di due punti.
-   I valori di questa proprietà devono essere elaborati con distinzione tra maiuscole e minuscole. Sono progettati per essere elaborati a livello di codice, anziché essere un nome visualizzato e dovrebbero essere brevi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




