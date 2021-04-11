---
description: Di seguito sono elencati i qualificatori utilizzati per definire le classi del provider di visualizzazione.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Qualificatori specifici del provider di visualizzazione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232903"
---
# <a name="qualifiers-specific-to-the-view-provider"></a>Qualificatori specifici del provider di visualizzazione

Di seguito sono elencati i qualificatori utilizzati per definire le classi del provider di visualizzazione.

> [!Note]  
> La classe del provider di visualizzazione supporta solo i nomi NetBIOS quando si utilizzano riferimenti remoti. Se si usa un indirizzo IP o un nome DNS in un riferimento remoto, la connessione ha esito negativo con un errore 0x800706ba.

 

<dt>

<span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Diretto**
</dt> <dd>

Tipo di dati: **Boolean**

Utilizzato con le proprietà di associazione di visualizzazione per impedire il mapping dei riferimenti di associazione a un riferimento alla visualizzazione.

Nell'esempio seguente viene definita la proprietà **GroupComponent** come riferimento di associazione di cui non è stato eseguito il mapping nel riferimento alla vista.


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**
</dt> <dd>

Tipo di dati: **Boolean**

Valore predefinito per una proprietà della classe di visualizzazione basata su una proprietà della classe di origine con un valore predefinito diverso. La classe di origine sottostante è implicita nella visualizzazione.

Ad esempio, la classe di origine [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) ha una proprietà [booleana](boolean.md) **RunRepeatedly** che indica se il processo deve essere eseguito periodicamente o solo una volta. Il valore predefinito di **RunRepeatedly** non è true per **\_ ScheduledJob Win32**, ma è true per la classe di visualizzazione.


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**
</dt> <dd>

Tipo di dati: **String**

Definisce la modalità di Unione delle istanze della classe di origine nelle classi di visualizzazione join. Nell'esempio seguente viene illustrato come utilizzare il qualificatore **JoinOn** per unire due classi di origine.


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Metodo di origine da eseguire per il metodo di visualizzazione. Per una sintassi simile, vedere [qualificatore PropertySources](propertysources-qualifier.md). La firma del metodo deve corrispondere esattamente alla firma della classe di origine. Copiare la firma del metodo dal file MOF che definisce la classe di origine. Nell'esempio seguente viene definito un metodo del metodo [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) di [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



Questo qualificatore è valido solo quando viene utilizzato con le viste Union.

</dd> <dt>

<span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)
</dt> <dd>

Tipo di dati: **String**

Query WQL per filtrare le istanze dopo che sono state aggiunte a una classe join.

</dd> <dt>

<span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Proprietà di origine da cui una proprietà della classe di visualizzazione Ottiene i dati.

</dd> <dt>

<span id="Union"></span><span id="union"></span><span id="UNION"></span>**Unione**
</dt> <dd>

Tipo di dati: **Boolean**

Indica se si sta definendo una classe Union. Le viste Unione contengono istanze basate sull'Unione delle istanze di origine. È ad esempio possibile dichiarare quanto segue:


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Set di query di WMI Query Language (WQL) che definiscono le istanze e le proprietà di origine utilizzate in una classe di visualizzazione specifica. La corrispondenza posizionale di tutti i qualificatori di matrice è importante.

</dd> <dt>

<span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Spazi dei nomi in cui si trovano le istanze di origine.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

