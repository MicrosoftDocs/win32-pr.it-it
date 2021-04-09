---
description: La \_ classe WMI WMISetting singleton Win32 contiene i parametri operativi per il servizio WMI. Questa classe può avere una sola istanza, che esiste sempre per ogni sistema Windows e non può essere eliminata. Non è possibile creare istanze aggiuntive.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Classe Win32_WMISetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877326"
---
# <a name="win32_wmisetting-class"></a>Win32 \_ WMISetting (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ WMISetting singleton Win32** contiene i parametri operativi per il servizio WMI. Questa classe può avere una sola istanza, che esiste sempre per ogni sistema Windows e non può essere eliminata. Non è possibile creare istanze aggiuntive.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ WMISetting** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ WMISetting** dispone di queste proprietà.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| Default Namespace")
</dt> </dl>

Spazio dei nomi dello script predefinito. Questa proprietà contiene lo spazio dei nomi utilizzato dalle chiamate dall'API di scripting per WMI se non ne è stato specificato alcuno dal chiamante.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **scripting \| default namespace**    

Esempio: radice \\ CIMV2

Per uno script di esempio che usa questa proprietà, vedere la sezione Osservazioni.

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| Enable for ASP")
</dt> </dl>

Se **true**, lo scripting WMI può essere utilizzato in Active Server Pages (ASP). Questa proprietà è valida solo nei sistemi che eseguono versioni non supportate di Windows. Per i sistemi Windows supportati, lo scripting WMI è sempre consentito in ASP.

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| autocover file MOF")
</dt> </dl>

Elenco dei nomi di file MOF completi utilizzati per inizializzare o ripristinare il repository WMI. L'elenco determina l'ordine in cui vengono compilati i file MOF.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| autocover file MOF**    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")
</dt> </dl>

Non supportata.

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

**Non avviare** (0)


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

**Avvio automatico** (1)


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

**Avvio al riavvio** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**BackupInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| backup Interval Threshold"), [**unità**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Non supportata. Eseguire invece il backup manuale del repository WMI.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Functions \| GetTimeZoneInformation")
</dt> </dl>

Data e ora in cui è stato eseguito l'ultimo backup.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Build")
</dt> </dl>

Informazioni sulla versione per il servizio WMI attualmente installato.

Lunghezza del tempo che trascorre tra i backup del database WMI.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| Build**

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| repository directory")
</dt> </dl>

Percorso della directory che contiene il repository WMI.

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB Size"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Dimensioni massime del repository WMI.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")
</dt> </dl>

Non supportata.

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")
</dt> </dl>

Se **true**, il sottosistema di eventi WMI deve essere abilitato.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")
</dt> </dl>

Se **true**, WMI crea un heap preallocato con la dimensione del valore **LastStartupHeapPreallocation** quando WMI viene inizializzato.

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| alta soglia per oggetti client"), [**unità**](../wmisdk/standard-qualifiers.md) ("oggetti al secondo")
</dt> </dl>

Frequenza massima con cui è possibile recapitare gli oggetti creati dal provider ai client. Per gestire le differenze di velocità tra provider e client, WMI include gli oggetti nelle code prima di distribuirli ai consumer. Per maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider. Se la memoria utilizzata dagli oggetti non raccolti raggiunge **LowThresholdOnObjects**, WMI rallenta l'aggiunta di nuovi oggetti nella coda. Se gli eventi non raccolti continuano ad accumularsi e viene raggiunta la quantità massima di tempo di attesa per il recapito di eventi in **MaxWaitOnClientObjects** mentre la memoria usata è in corrispondenza del valore di **HighThresholdOnClientObjects**, WMI non accetta più oggetti dai provider e restituisce **WBEM \_ e \_ \_ \_ memoria insufficiente** ai client.

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| alta soglia per gli eventi"), [**unità**](../wmisdk/standard-qualifiers.md) ("eventi al secondo")
</dt> </dl>

Frequenza massima con cui gli eventi devono essere recapitati ai client. Per gestire le differenze di velocità tra provider e client, WMI Accoda gli eventi prima di distribuirli agli utenti. Per maggiore efficienza, i consumer devono raccogliere gli eventi a un ritmo corrispondente al provider. Se la memoria utilizzata dagli eventi non raccolti raggiunge **LowThresholdOnObjects**, WMI rallenta l'aggiunta di nuovi eventi alla coda. Se gli eventi non raccolti continuano ad accumularsi e viene raggiunta la quantità massima di tempo di attesa per il recapito di eventi in **MaxWaitOnEvents** mentre la memoria usata è in corrispondenza del valore di **HighThresholdOnEvents**, WMI non accetta più eventi dai provider e restituisce **WBEM \_ e \_ \_ \_ memoria insufficiente** ai client.

> [!Note]  
> La limitazione viene eseguita solo per i consumer di eventi permanenti, quindi i consumer temporanei non dovrebbero prevedere la limitazione quando viene eseguito il backup degli eventi nella coda degli eventi interni WMI.

 

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold per oggetti client (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Installation Directory")
</dt> </dl>

Percorso della directory in cui è stato installato il software WMI. Il percorso predefinito è \\ system32 \\ WBEM.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Directory di installazione del software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \|**

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**unità**](../wmisdk/standard-qualifiers.md) ("byte")
</dt> </dl>

Dimensioni dell'heap pre-allocato creato da WMI durante l'inizializzazione.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging directory")
</dt> </dl>

Percorso della directory che contiene il percorso dei file di registro di sistema WMI.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging directory**

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging")
</dt> </dl>

Abilitazione della registrazione degli eventi e del livello di dettaglio della registrazione usata.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging**

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Disattivato** (0)


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**Registrazione degli errori** (1)


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

**Registrazione dettagliata degli errori** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LowThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| bassa soglia per oggetti client"), [**unità**](../wmisdk/standard-qualifiers.md) ("oggetti al secondo")
</dt> </dl>

Frequenza con cui WMI inizia a rallentare la creazione di nuovi oggetti creati per i client. Per gestire le differenze di velocità tra provider e client, WMI include gli oggetti nelle code prima di distribuirli ai consumer. Per maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider. Se il numero di richieste per gli oggetti raggiunge **LowThresholdOnClientObjects**, WMI rallenta gradualmente la creazione di nuovi oggetti in modo che corrispondano alla frequenza di utilizzo del client. Questo rallentamento inizia quando la velocità con cui vengono creati gli oggetti supera il valore di questa proprietà. Vedere **HighThresholdOnClientObjects**.

Questa proprietà riflette il valore del registro di sistema.

**Chiave \_ di Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold per oggetti client (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| soglia bassa per gli eventi"), [**unità**](../wmisdk/standard-qualifiers.md) ("eventi al secondo")
</dt> </dl>

Frequenza con cui WMI inizia a rallentare il recapito di nuovi eventi. Per gestire le differenze di velocità tra provider e client, WMI Accoda gli eventi prima di distribuirli agli utenti. Per maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider. Se la coda cresce fuori controllo, le limitazioni di WMI rallentano, ovvero il recapito degli eventi gradualmente per allinearsi alla velocità del client. Questo rallentamento inizia quando la frequenza con cui vengono generati gli eventi supera il valore di questa proprietà. Vedere **HighThresholdOnEvents**.

> [!Note]  
> La limitazione viene eseguita solo per i consumer di eventi permanenti, quindi i consumer temporanei non dovrebbero prevedere la limitazione quando viene eseguito il backup degli eventi nella coda degli eventi interni WMI.

 

Questa proprietà riflette il valore del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold per gli oggetti client {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| log file di dimensioni massime"), [**unità**](../wmisdk/standard-qualifiers.md) ("byte")
</dt> </dl>

Dimensioni massime dei file di log generati dal servizio WMI.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ \_** \\  \\  \\ **\| \| Dimensioni massime del file di log** del software del computer locale Microsoft WBEM CIMOM

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max wait on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Quantità di tempo in cui un oggetto appena creato resta in attesa di essere utilizzato dal client prima che venga eliminato e viene restituito un valore di errore. Questa proprietà interagisce con le proprietà **LowThresholdOnClientObjects** e **HighThresholdOnClientObjects** per limitare, rallentare, il recapito di oggetti ai consumer quando il consumer riceve gli oggetti troppo lentamente.

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max wait on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Quantità di tempo per cui un evento inviato a un client viene accodato prima di essere eliminato. Questa proprietà interacts0 con **LowThresholdOnEvents** e **HighThresholdOnEvents** per limitare il rallentamento, ovvero il recapito di oggetti ai consumer quando il consumer riceve gli oggetti troppo lentamente.

Questa proprietà riflette il valore del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max Wait for Events (MS)**    

</dd> <dt>

**MofSelfInstallDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install directory")
</dt> </dl>

Percorso della directory per le applicazioni che installano i file MOF nel repository WMI. WMI compila automaticamente tutti i file MOF presenti in questa directory e, a seconda del suo esito positivo, sposta il file MOF in una sottodirectory contrassegnata come valida o non valida. Se il \# comando [pragma autocover](../wmisdk/pragma-autorecover.md) è incluso, il nome file completo viene aggiunto all'elenco **AutoRecoverMofs** usato durante l'inizializzazione o il recupero del repository WMI. L'elenco determina l'ordine in cui vengono compilate file MOF.

Questa proprietà riflette il valore nella chiave del registro di sistema.

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = install directory**

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ WMISetting** deriva dall' [**\_ impostazione CIM**](cim-setting.md). In un computer può esistere una sola istanza di questa classe.

Sapere come WMI è configurato in un computer può essere molto utile quando si esegue il debug di script o si risolvono problemi con il servizio WMI stesso. Molti script WMI, ad esempio, vengono scritti nel presupposto che root \\ CIMV2 sia lo spazio dei nomi predefinito nel computer di destinazione. Di conseguenza, gli autori di script che devono accedere a una classe in "root \\ CIMv2" spesso non riescono a includere lo spazio dei nomi nel moniker GetObject, come illustrato nell'esempio di codice seguente:

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

Se il \\ CIMV2 radice non è lo spazio dei nomi predefinito nel computer di destinazione, lo script avrà esito negativo. Per evitare che ciò accada, è necessario includere il CIMV2 radice dello spazio dei nomi \\ nel moniker, come illustrato nell'esempio di codice seguente:

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

Se lo spazio dei nomi predefinito nel computer di destinazione è diverso dallo spazio dei nomi utilizzato da uno script, lo script avrà esito negativo. A questo proposito, all'utente viene visualizzato il messaggio di errore "classe non valida". In realtà, l'errore non è dovuto al fatto che la classe non è valida, ma perché non è possibile trovare la classe nello spazio dei nomi predefinito. Si tratta di un problema difficile da risolvere, perché è probabile che si verifichino possibili problemi con la classe piuttosto che problemi con lo spazio dei nomi (o, in questo caso, non è stato specificato).

È possibile utilizzare la classe **Win32 \_ WMISetting** per determinare la modalità di configurazione di WMI in un computer. I dettagli di configurazione come lo spazio dei nomi predefinito o il numero di build WMI possono essere utili per la risoluzione dei problemi relativi agli script. Queste impostazioni forniscono inoltre informazioni amministrative importanti, ad esempio come, o anche se, gli errori WMI vengono registrati in un computer e quali provider WMI verranno ricaricati automaticamente se è necessario ricompilare il repository WMI.

## <a name="examples"></a>Esempio

Nell'esempio relativo alla [modifica delle impostazioni WMI](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) per il codice VBScript della raccolta TechNet viene utilizzata la classe **Win32 \_ WMISetting** per configurare l'intervallo di backup e il livello di registrazione di WMI.

L'esempio di codice VBScript [dello spazio dei nomi predefinito](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) nella raccolta TechNet usa la classe **Win32 \_ WMISetting** per recuperare e visualizzare l'impostazione WMI corrente "spazio dei nomi predefinito per lo scripting".

Nell'esempio relativo alla [modifica del codice VBScript dello spazio dei nomi WMI predefinito](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) nella raccolta TechNet viene utilizzata la proprietà **ASPScriptDefaultNamespace** per impostare l'impostazione "spazio dei nomi predefinito per lo script" di WMI su "root \\ cimv2".

L' [elenco di tutti gli](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) esempi di codice VBSCript delle impostazioni WMI usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.

L' [elenco di informazioni sull'impostazione WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) di esempio codice JavaScript usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.

L'elenco di esempi di codice Python per [informazioni sull'impostazione WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.

L' [elenco WMI setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.

Nell'esempio di codice VBScript riportato di seguito viene illustrato come ottenere la versione di WMI in esecuzione nel computer locale. "Win32 \_ WMISetting = @" indica la singola istanza della classe. Per ulteriori informazioni, vedere versioni WMI.


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> <dt>

[Classi di gestione del servizio WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
