---
description: Win32 \_ PowerManagementEvent &\# 32; La classe WMI rappresenta gli eventi di risparmio energia risultanti da modifiche dello stato di alimentazione.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Win32_PowerManagementEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 536963be51d665b03af77bb81c7592b44d2a6eb5ddc449bfa82896dd7f7da9b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064421"
---
# <a name="win32_powermanagementevent-class"></a>Classe PowerManagementEvent Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 PowerManagementEvent** rappresenta gli eventi di risparmio energia risultanti da modifiche dello stato di alimentazione. Queste modifiche di stato sono associate ai protocolli di gestione Advanced Power Management (APM) o Advanced Configuration and Power Interface (ACPI).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a>Members

La **classe \_ PowerManagementEvent Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Win32 PowerManagementEvent** ha queste proprietà.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Eventi di risparmio energia Win32API") \|
</dt> </dl>

Tipo di modifica nello stato di alimentazione del sistema.

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Immissione di Suspend** (4)


</dt> <dd>

Mentre è sospeso, il computer sembra essere spento; tuttavia può essere "rimovito" in risposta a vari eventi, incluso l'input dell'utente, ad esempio lo spostamento del mouse o la pressione di un tasto sulla tastiera. Mentre il computer è sospeso, il consumo di energia viene ridotto a uno dei diversi livelli a seconda della modalità di utilizzo del sistema. Minore è il livello di consumo di energia, maggiore è il tempo necessario al sistema per tornare allo stato di lavoro. Quando il computer entra nello stato di sospensione, il desktop viene bloccato ed è necessario premere CTRL+ALT+CANC e specificare un nome utente e una password validi per riprendere le operazioni

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Riprendi dalla sospensione** (7)


</dt> <dd>

Indica che è stato inviato un messaggio Resume from Suspend, che consente al computer di tornare allo stato di alimentazione normale.

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Modifica stato alimentazione** (10)


</dt> <dd>

Indica una modifica dello stato di alimentazione del computer, ad esempio un passaggio dall'alimentazione a batteria all'alimentatore o da ca a un alimentatore ininterrotta. Il sistema trasmette questo evento anche quando l'autonomia della batteria scende sotto la soglia specificata dall'utente o se lo stato di carica della batteria cambia di una percentuale specificata.

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Evento OEM** (11)


</dt> <dd>

Indica che un BIOS Advanced Power Management (APM) ha inviato un evento OEM. Il valore dell'evento verrà acquisito nella **proprietà OEMEventCode.** Poiché alcune implementazioni del BIOS APM non forniscono notifiche degli eventi OEM, questo evento potrebbe non essere mai trasmesso in alcuni computer. APM è uno schema di risparmio energia legacy. Sebbene sia ancora supportato, APM è stato in gran parte sostituito da ACPI (Advanced Configuration and Power Interface).

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Riprendi** automatico (18)


</dt> <dd>

Indica che il computer è stato in risposta a un evento. Se il sistema rileva l'attività dell'utente, ad esempio un clic del mouse, verrà trasmesso il messaggio ResumeSuspend, in modo che le applicazioni sappiano che possono riprendere l'interattività completa con l'utente.

</dd> </dl>

</dd> <dt>

**OEMEventCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Eventi di risparmio energia Win32API") \|
</dt> </dl>

Stato di alimentazione del sistema definito dall'OEM (Original Equipment Manufacturer) quando la proprietà **EventType** di questa classe è impostata su 11 (evento OEM); In caso contrario, questa proprietà è impostata su **NULL.** Gli eventi OEM vengono generati quando un BIOS APM segnala un evento OEM APM. I codici evento OEM sono nell'intervallo 0x0200h - 0x02FFh.

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](../wmisdk/--event.md). Per altre informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere [Costanti di sicurezza WMI.](../wmisdk/wmi-security-constants.md)

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Times).

Questa proprietà viene ereditata [**\_ \_ dall'evento**](../wmisdk/--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Win32 PowerManagementEvent** è derivata da [**\_ \_ ExtrinsicEvent.**](../wmisdk/--extrinsicevent.md)

Le modifiche dello stato di alimentazione spesso indicano che si è verificato un problema con un computer o con un altro dispositivo gestito. Se un server passa improvvisamente dall'alimentazione CA a un alimentatore ininterrotta, questa modifica può indicare che si è verificato un problema elettrico di qualche tipo, con il computer stesso o con il sistema elettrico nella stanza in cui è conservato il computer.

Gli amministratori devono monitorare queste modifiche nello stato dell'alimentazione e ricevere immediatamente una notifica di tali modifiche. In questo modo, gli utenti possono intervenire prima che il dispositivo perda completamente l'alimentazione. I sistemi di alimentazione ininterrotti, ad esempio, possono essere eseguiti solo per 15 minuti circa prima dell'arresto.

La **classe \_ PowerManagementEvent Win32** può essere usata per monitorare le modifiche dello stato di alimentazione in un computer. Queste modifiche possono includere il passaggio da una fonte di alimentazione a un'altra e una modifica dello stato di alimentazione del computer (ad esempio, l'ingresso o l'uscita dalla modalità di sospensione).

La classe **\_ Win32 PowerManagementEvent** ha solo due proprietà: EventType, usato per indicare il tipo di evento di modifica dell'alimentazione che si è verificato, e OEMEventType, che viene usato da alcuni produttori di apparecchiature originali per definire eventi di modifica dell'alimentazione aggiuntivi.

Per altre informazioni sulla risposta Windows eventi di risparmio energia, vedere l'articolo Monitorare e rispondere Windows [power events con PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) in Hey! Scripting Guy! .

## <a name="examples"></a>Esempio

Il codice VBScript seguente monitora le modifiche apportate allo stato di alimentazione in un computer.


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> <dt>

[Monitoraggio delle modifiche nello stato di alimentazione del computer](/previous-versions/tn-archive/ee176537(v=technet.10))
</dt> </dl>

 

 
