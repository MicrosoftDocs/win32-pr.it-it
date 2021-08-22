---
description: Descrive gli aspetti virtuali di un sistema virtuale tramite un set di proprietà specifiche della virtualizzazione. CIM \_ VirtualSystemSettingData viene usato anche come classe di primo livello delle configurazioni del sistema virtuale.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData classe
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
ms.openlocfilehash: 1caed7797343eac9babd320af42fd6c9aaaffeff054211cc55bda0d437582d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068491"
---
# <a name="cim_virtualsystemsettingdata-class"></a>Classe CIM \_ VirtualSystemSettingData

Descrive gli aspetti virtuali di un sistema virtuale tramite un set di proprietà specifiche della virtualizzazione. **CIM \_ VirtualSystemSettingData viene** usato anche come classe di primo livello delle configurazioni del sistema virtuale.

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

La **classe CIM \_ VirtualSystemSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ VirtualSystemSettingData** ha queste proprietà.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per il sistema virtuale quando il software eseguito dal sistema virtuale ha esito negativo. Gli errori indirizzati da questa proprietà includono solo quelli rilevabili dalla piattaforma host, ad esempio una condizione di stato di attesa non interrompibile.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Riavvio** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Ripristinare lo snapshot** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per il sistema virtuale quando l'host viene arrestato.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Spegni** (2)


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Stato di salvataggio** (3)


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

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire sul sistema virtuale all'avvio dell'host.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Riavvia se precedentemente attivo** (3)


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

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ritardo per l'azione di avvio. Questo valore è una variante di intervallo del **tipo di dati datetime.**

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di sequenza per l'attivazione del sistema virtuale all'avvio del sistema host. Un numero inferiore indica l'attivazione precedente. Se una o più configurazioni mostrano lo stesso valore, la sequenza dipende dall'implementazione. Il valore "0" indica che la sequenza dipende dall'implementazione.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso file della directory in cui sono archiviate le informazioni sulla configurazione del sistema virtuale. Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo del file in cui sono archiviate le informazioni sulla configurazione del sistema virtuale. Il percorso relativo viene aggiunto al valore della **proprietà ConfigurationDataRoot.** Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID univoco della configurazione del sistema virtuale.

> [!Note]  
> **ConfigurationID** è diverso da **InstanceID** e viene assegnato dall'implementazione a un sistema virtuale o a una configurazione del sistema virtuale. **ConfigurationID** non è una chiave e lo stesso valore può verificarsi per più istanze.

 

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della configurazione del sistema virtuale.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo del file della directory in cui sono archiviate le informazioni di log per il sistema virtuale. Il percorso relativo viene aggiunto al valore della **proprietà ConfigurationDataRoot.** Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice contenente le note fornite dall'utente correlate al sistema virtuale.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file in cui sono archiviate le informazioni relative al ripristino del sistema virtuale. Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo della directory in cui sono archiviate le informazioni sugli snapshot del sistema virtuale. Il percorso relativo viene aggiunto al valore della **proprietà ConfigurationDataRoot.** Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo della directory in cui vengono archiviate le informazioni correlate di sospensione sul sistema virtuale. Il percorso relativo viene aggiunto al valore della **proprietà ConfigurationDataRoot.** Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo della directory in cui sono archiviati i file di scambio del sistema virtuale. Il percorso relativo viene aggiunto al valore della **proprietà ConfigurationDataRoot.** Il formato di questa proprietà è un URI basato su RFC 2079.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome univoco del sistema all'interno della piattaforma di virtualizzazione. **VirtualSystemIdentifier** non è il nome host assegnato all'istanza del sistema operativo in esecuzione nel sistema virtuale, né è un indirizzo IP o MAC assegnato a una delle porte di rete.

**VirtualSystemIdentifier** può contenere regole specifiche dell'implementazione, ad esempio modelli semplici o un'espressione regolare che può essere interpretata dall'implementazione quando si imposta **VirtualSystemIdentifier**.

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo del sistema virtuale.

> [!Note]  
> Se il tipo di sistema virtuale è sconosciuto, questo valore deve essere impostato su "DMTF:unknown".

 

Questa proprietà viene formattata usando il formato ABNF (Augmented Backus Naur Form) seguente:

vs-type = dmtf-value /other-org-value/legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;

Il valore del formato ABNF precedente è:

-   *dmtf-value*   valore della proprietà definito da DMTF e definito nella descrizione di questa proprietà.
-   *other-org-value*   è un valore di proprietà definito da un'entità aziendale diversa da DMTF e non è definito nella descrizione di questa proprietà.
-   *legacy-value*   un valore di proprietà definito da un'entità aziendale diversa da DMTF e non è definito nella descrizione di questa proprietà. Questi valori sono consentiti ma consigliati per essere deprecati nel tempo.
-   *defining-org*   un identificatore per l'entità business che definisce il tipo di sistema virtuale. Deve includere un copyright, un marchio o un nome univoco di proprietà dell'entità aziendale. Non deve essere "DMTF" e non deve contenere i due punti.
-   *org-vs-type*   un identificatore per il tipo di sistema virtuale all'interno dell'entità business di definizione. Deve essere univoco all'interno di defining-org. org-vs-type può usare qualsiasi carattere consentito per le stringhe CIM, ad eccezione dei seguenti: U0000-U001F (controlli Unicode C0), U0020 (spazio), U007F (controlli Unicode C0) o U0080-U009F (controlli Unicode C1).
-   Se è necessario strutturare il valore in segmenti, i segmenti devono essere separati da un singolo due punti.
-   I valori di questa proprietà devono essere elaborati con distinzione tra maiuscole e minuscole. Devono essere elaborati a livello di codice, anziché essere un nome visualizzato, e devono essere brevi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




