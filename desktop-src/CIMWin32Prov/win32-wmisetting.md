---
description: La classe \_ WMI singleton Win32 WMISetting contiene i parametri operativi per il servizio WMI. Questa classe può avere una sola istanza, che esiste sempre per ogni Windows sistema e non può essere eliminata. Non è possibile creare istanze aggiuntive.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting classe
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
ms.openlocfilehash: 39c976a6a8b4c25fbc42561b7d0a8db52b9029f679ad72993f931efa596d2d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079575"
---
# <a name="win32_wmisetting-class"></a>Classe WMISetting Win32 \_

La **classe WMI singleton \_ Win32 WMISetting** [contiene](../wmisdk/retrieving-a-class.md) i parametri operativi per il servizio WMI. Questa classe può avere una sola istanza, che esiste sempre per ogni Windows sistema e non può essere eliminata. Non è possibile creare istanze aggiuntive.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

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

La **classe \_ WMISetting Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ WMISetting Win32** ha queste proprietà.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Spazio dei nomi predefinito script \| Microsoft \\ \\ \\ \\ WBEM \\ \\ \| Win32Registry Software")
</dt> </dl>

Spazio dei nomi dello script predefinito. Questa proprietà contiene lo spazio dei nomi utilizzato dalle chiamate dall'API di scripting per WMI se non ne viene specificato nessuno dal chiamante.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ Spazio \_ dei nomi predefinito** per lo scripting \\  \\ **Microsoft** \\ **WBEM** del \\ **software \|** LOCAL MACHINE    

Esempio: root \\ cimv2

Per uno script di esempio che usa questa proprietà, vedere la sezione Osservazioni.

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM scripting Enable for \\ \\ \| ASP")
</dt> </dl>

Se **True,** lo scripting WMI può essere usato nelle Active Server (ASP). Questa proprietà è valida solo nei sistemi che eseguono versioni non Windows supportate. Per i sistemi Windows supportati, lo scripting WMI è sempre consentito in ASP.

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Autorecover MOFs")
</dt> </dl>

Elenco di nomi di file MOF completi usati per inizializzare o ripristinare il repository WMI. L'elenco determina l'ordine in cui vengono compilati i file MOF.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Autorecover MOFs**    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")
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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Backup Interval \| Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")
</dt> </dl>

Non supportata. Eseguire invece manualmente il backup del repository WMI.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funzioni ora Win32API \| \| GetTimeZoneInformation")
</dt> </dl>

Data e ora dell'ultimo backup eseguito.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \| Build")
</dt> </dl>

Informazioni sulla versione per il servizio WMI attualmente installato.

Periodo di tempo trascorso tra i backup del database WMI.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| Build**

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Repository \| Directory")
</dt> </dl>

Percorso della directory che contiene il repository WMI.

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Max DB \| Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Dimensioni massime del repository WMI.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")
</dt> </dl>

Non supportata.

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")
</dt> </dl>

Se **True,** il sottosistema di eventi WMI deve essere abilitato.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")
</dt> </dl>

Se **True,** WMI crea un heap preallocato con le dimensioni del **valore LastStartupHeapPreallocation** quando WMI viene inizializzato.

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM High Threshold On Client \| Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")
</dt> </dl>

Velocità massima con cui gli oggetti creati dal provider possono essere recapitati ai client. Per supportare i differenziali di velocità tra provider e client, WMI contiene gli oggetti nelle code prima di recapitarli ai consumer. Per una maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider. Se la memoria utilizzata dagli oggetti non ritirati raggiunge **LowThresholdOnObjects,** WMI rallenta l'aggiunta di nuovi oggetti nella coda. Se gli eventi non registrati continuano ad accumularsi e viene raggiunta l'attesa massima per il recapito degli eventi in **MaxWaitOnClientObjects** mentre la memoria usata è pari al valore in **HighThresholdOnClientObjects,** WMI non accetta più oggetti dai provider e restituisce **WBEM \_ E OUT OF \_ \_ \_ MEMORY** ai client.

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM High Threshold On \| Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")
</dt> </dl>

Frequenza massima con cui gli eventi devono essere recapitati ai client. Per supportare differenze di velocità tra provider e client, WMI accoda gli eventi prima di recapitarli ai consumer. Per una maggiore efficienza, i consumer devono raccogliere gli eventi a un ritmo corrispondente al provider. Se la memoria utilizzata dagli eventi non registrati raggiunge **LowThresholdOnObjects,** WMI rallenta l'aggiunta di nuovi eventi nella coda. Se gli eventi non registrati continuano ad accumularsi e viene raggiunta l'attesa massima per il recapito degli eventi in **MaxWaitOnEvents** mentre la memoria usata è al valore in **HighThresholdOnEvents,** WMI non accetta più eventi dai provider e restituisce **WBEM \_ E OUT OF \_ \_ \_ MEMORY** ai client.

> [!Note]  
> La limitazione viene eseguita solo per i consumer di eventi permanenti, pertanto i consumer temporanei non devono aspettarsi la limitazione quando viene eseguito il backup degli eventi nella coda di eventi interna WMI.

 

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM High Threshold On Client Objects \| (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM Installation \| Directory")
</dt> </dl>

Percorso della directory in cui è stato installato il software WMI. Il percorso predefinito è \\ System32 \\ Wbem.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| Installation Directory**

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Unità**](../wmisdk/standard-qualifiers.md) ("byte")
</dt> </dl>

Dimensione dell'heap preallocato creato da WMI durante l'inizializzazione.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Logging \| Directory")
</dt> </dl>

Percorso della directory che contiene il percorso dei file di registro di sistema WMI.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging Directory**

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Logging")
</dt> </dl>

Abilitazione della registrazione degli eventi e del livello di dettaglio della registrazione utilizzato.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging**

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Disattivato** (0)


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**Registrazione degli errori** (1)


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

**Registrazione errori dettagliati** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LowThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CiMOM Low Threshold On Client \| Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")
</dt> </dl>

Frequenza con cui WMI inizia a rallentare la creazione di nuovi oggetti creati per i client. Per supportare i differenziali di velocità tra provider e client, WMI contiene gli oggetti nelle code prima di recapitarli ai consumer. Per una maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider. Se la frequenza delle richieste di oggetti raggiunge **LowThresholdOnClientObjects,** WMI rallenta gradualmente la creazione di nuovi oggetti in modo che corrisponda alla frequenza d'uso del client. Questo rallentamento inizia quando la frequenza con cui vengono creati gli oggetti supera il valore di questa proprietà. Vedere **HighThresholdOnClientObjects.**

Questa proprietà riflette il valore del Registro di sistema.

**CHIAVE \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM High Threshold On Client Objects \| (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CiMOM Low Threshold On \| Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")
</dt> </dl>

Frequenza con cui WMI inizia a rallentare il recapito di nuovi eventi. Per supportare differenze di velocità tra provider e client, WMI accoda gli eventi prima di recapitarli ai consumer. Per una maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider. Se la coda diventa fuori controllo, WMI rallenta il recapito degli eventi gradualmente per allinearsi alla frequenza del client. Questo rallentamento inizia quando la frequenza con cui vengono generati gli eventi supera il valore di questa proprietà. Vedere **HighThresholdOnEvents.**

> [!Note]  
> La limitazione viene eseguita solo per i consumer di eventi permanenti, pertanto i consumer temporanei non devono aspettarsi la limitazione quando viene eseguito il backup degli eventi nella coda di eventi interna WMI.

 

Questa proprietà riflette il valore del Registro di sistema.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM High Threshold on Client Objects \| {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Log File Max \| Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Dimensioni massime dei file di log generati dal servizio WMI.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| Log File Max Size**

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Max Wait On \| Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Tempo di attesa per l'utilizzo da parte del client di un oggetto appena creato prima che venga eliminato e venga restituito un valore di errore. Questa proprietà interagisce con le proprietà **LowThresholdOnClientObjects** e **HighThresholdOnClientObjects** per rallentare, ovvero rallentare, il recapito di oggetti ai consumer quando il consumer riceve gli oggetti troppo lentamente.

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Max Wait On \| Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("millisecondi")
</dt> </dl>

Periodo di tempo per cui un evento inviato a un client viene accodato prima di essere eliminato. Questa proprietà interagisce0 con **LowThresholdOnEvents** e **HighThresholdOnEvents** per rallentare il recapito di oggetti ai consumer quando il consumer riceve gli oggetti troppo lentamente.

Questa proprietà riflette il valore del Registro di sistema.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max Wait On Events (ms)**    

</dd> <dt>

**MofSelfInstallDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \| MOF Self-Install Directory")
</dt> </dl>

Percorso della directory per le applicazioni che installano file MOF nel repository WMI. WMI compila automaticamente tutti i file MOF inseriti in questa directory e, a seconda dell'esito positivo, sposta il file MOF in una sottodirectory con etichetta good o bad. Se è incluso il comando \# [pragma autorecover,](../wmisdk/pragma-autorecover.md) il nome file completo viene aggiunto all'elenco **AutorecoverMofs** usato durante l'inizializzazione o il ripristino del repository da parte di WMI. L'elenco determina l'ordine in cui vengono compilati i file MOF.

Questa proprietà riflette il valore nella chiave del Registro di sistema.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self=Install Directory**

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ WMISetting Win32** deriva dall'impostazione [**CIM \_**](cim-setting.md). In un computer può esistere una sola istanza di questa classe.

Conoscere la configurazione di WMI in un computer può essere molto utile quando si esegue il debug di script o si risoluzione dei problemi relativi al servizio WMI stesso. Ad esempio, molti script WMI vengono scritti presupponendo che root cimv2 sia lo spazio dei nomi \\ predefinito nel computer di destinazione. Di conseguenza, i writer di script che devono accedere a una classe in "CIMv2 radice" spesso non riescono a includere lo spazio dei nomi nel moniker GetObject, come illustrato nell'esempio di codice \\ seguente:

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

Se \\ cimv2 radice non è lo spazio dei nomi predefinito nel computer di destinazione, questo script avrà esito negativo. Per evitare questo problema, la radice dello spazio dei nomi cimv2 deve essere inclusa nel moniker, come illustrato \\ nell'esempio di codice seguente:

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

Se lo spazio dei nomi predefinito nel computer di destinazione è diverso da quello assunto da uno script, lo script avrà esito negativo. Inoltre, all'utente verrà visualizzato il messaggio di errore un po' fuorviante "Classe non valida". In realtà, l'errore non è dovuto al fatto che la classe non è valida, ma perché non è possibile trovare la classe nello spazio dei nomi predefinito. Si tratta di un problema difficile da risolvere, perché è probabile che si anighino i possibili problemi con la classe anziché con lo spazio dei nomi specificato (o, in questo caso, non è stato).

È possibile usare la **classe \_ WMISetting Win32** per determinare come è stato configurato WMI in un computer. I dettagli di configurazione, ad esempio lo spazio dei nomi predefinito o il numero di build WMI, possono essere utili per la risoluzione dei problemi relativi agli script. Queste impostazioni forniscono anche importanti informazioni amministrative, ad esempio come, o anche se, gli errori WMI vengono registrati in un computer e quali provider WMI verranno ricaricati automaticamente se è necessario ricompilare il repository WMI.

## <a name="examples"></a>Esempio

L'esempio di [codice Modify WMI Impostazioni](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript in TechNet Gallery usa la classe **\_ WMISetting Win32** per configurare l'intervallo di backup WMI e il livello di registrazione.

[L'esempio](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) di codice VBScript Elenca lo spazio dei nomi predefinito in TechNet Gallery usa la classe **\_ WMISetting Win32** per recuperare e visualizzare l'impostazione corrente "Spazio dei nomi predefinito per lo scripting" WMI.

L'esempio di codice VBScript Modify [the Default WMI Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) in TechNet Gallery usa la proprietà **ASPScriptDefaultNamespace** per impostare l'impostazione WMI "Default namespace for scripting" su "root \\ cimv2".

L'esempio di codice [List All the WMI Impostazioni](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.

[L'esempio di codice](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript Elenca informazioni sulle impostazioni WMI usa diverse proprietà in **\_ WMISetting Win32** per restituire un elenco di impostazioni WMI configurate in un computer.

[L'esempio di codice Python](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) Elenca informazioni sulle impostazioni WMI usa diverse proprietà in **\_ WMISetting Win32** per restituire un elenco di impostazioni WMI configurate in un computer.

[L'esempio di codice List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX usa diverse proprietà in **\_ WMISetting Win32** per restituire un elenco di impostazioni WMI configurate in un computer.

Nell'esempio di codice VBScript seguente viene illustrato come ottenere la versione di WMI in esecuzione nel computer locale. "Win32 \_ WMISetting=@" indica la singola istanza della classe. Per altre informazioni, vedere Versioni di WMI.


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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dt>

[Classi di gestione dei servizi WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
