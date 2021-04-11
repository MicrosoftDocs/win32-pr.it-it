---
description: Win32 \_ PowerManagementEvent &\# 32; Classe WMI che rappresenta gli eventi di risparmio energia derivanti da modifiche allo stato di alimentazione.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Classe Win32_PowerManagementEvent
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
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126840"
---
# <a name="win32_powermanagementevent-class"></a>Win32 \_ PowerManagementEvent (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PowerManagementEvent Win32** rappresenta eventi di risparmio energia derivanti da modifiche allo stato di alimentazione. Queste modifiche di stato sono associate a Advanced Power Management (APM) o ai protocolli di gestione del sistema ACPI (Advanced Configuration and Power Interface).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

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

La classe **Win32 \_ PowerManagementEvent** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PowerManagementEvent** dispone di queste proprietà.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("eventi di risparmio \| energia Win32API")
</dt> </dl>

Tipo di modifica nello stato di alimentazione del sistema.

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Immissione della sospensione** (4)


</dt> <dd>

Durante la sospensione, il computer sembra spento; Tuttavia, può essere riattivato in risposta a vari eventi, incluso l'input dell'utente, ad esempio lo spostamento del mouse o la pressione di un tasto sulla tastiera. Quando il computer viene sospeso, il consumo di energia viene ridotto a uno dei diversi livelli, a seconda della modalità di utilizzo del sistema. Minore è il livello di consumo energetico, maggiore è il tempo necessario al sistema per tornare allo stato di lavoro. Quando il computer entra nello stato Suspend, il desktop è bloccato ed è necessario premere CTRL + ALT + CANC e specificare un nome utente e una password validi per riprendere le operazioni

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Riprendi da Sospendi** (7)


</dt> <dd>

Indica che è stato inviato un messaggio di ripresa da Suspend, che consente al computer di tornare allo stato di alimentazione normale.

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Modifica dello stato di alimentazione** (10)


</dt> <dd>

Indica una modifica dello stato di alimentazione del computer, ad esempio un passaggio dall'alimentazione a batteria ad AC o da AC a un alimentatore di continuità. Il sistema trasmette questo evento anche quando l'autonomia della batteria scende sotto la soglia specificata dall'utente o se lo stato di carica della batteria cambia di una percentuale specificata.

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Evento OEM** (11)


</dt> <dd>

Indica che un BIOS di Advanced Power Management (APM) ha inviato un evento OEM. Il valore dell'evento verrà acquisito nella proprietà **OEMEventCode** . Poiché alcune implementazioni del BIOS APM non forniscono notifiche degli eventi OEM, questo evento potrebbe non essere mai trasmesso in alcuni computer. APM è uno schema di risparmio energia legacy. Anche se ancora supportata, APM è stato ampiamente sostituito da ACPI (Advanced Configuration and Power Interface).

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Riprendi automaticamente** (18)


</dt> <dd>

Indica che il computer è stato riattivato in risposta a un evento. Se il sistema rileva l'attività dell'utente (ad esempio un clic del mouse), il messaggio ResumeSuspend verrà trasmesso, consentendo alle applicazioni di tenere presente che è possibile riprendere l'interattività completa con l'utente.

</dd> </dl>

</dd> <dt>

**OEMEventCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("eventi di risparmio \| energia Win32API")
</dt> </dl>

Stato di alimentazione del sistema definito dall'OEM (Original Equipment Manufacturer) quando la proprietà **eventType** di questa classe è impostata su 11 (evento OEM); in caso contrario, questa proprietà è impostata su **null**. Gli eventi OEM vengono generati quando un BIOS APM segnala un evento APM OEM. I codici evento OEM sono compresi nell'intervallo 0x0200h-0x02FFh.

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](../wmisdk/--event.md). Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Time).

Questa proprietà viene ereditata dall' [**\_ \_ evento**](../wmisdk/--event.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PowerManagementEvent** deriva da [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).

Le modifiche allo stato di alimentazione spesso indicano che si è verificato un problema con un computer o con un altro dispositivo gestito. Se un server passa improvvisamente dall'alimentazione AC a un alimentatore di continuità, questa modifica può indicare che si è verificato un problema elettrico, sia con il computer che con il sistema elettrico nella stanza in cui viene mantenuto il computer.

Gli amministratori devono monitorare queste modifiche nello stato di alimentazione e ricevere immediatamente notifiche relative a tali modifiche. In questo modo è possibile intervenire prima che il dispositivo perda completamente l'energia. (È possibile, ad esempio, che i sistemi di continuità elettrica continuino a essere eseguiti solo 15 minuti prima di essere arrestati).

La classe **Win32 \_ PowerManagementEvent** può essere usata per monitorare le modifiche dello stato di alimentazione in un computer. Queste modifiche possono includere un passaggio da una fonte di alimentazione a un'altra e una modifica dello stato di alimentazione del computer (ad esempio, immissione o uscita dalla modalità di sospensione).

La classe **Win32 \_ PowerManagementEvent** dispone solo di due proprietà: EventType, usata per indicare il tipo di evento di modifica di risparmio energia che si è verificato e OEMEventType, usato da alcuni produttori di apparecchiature originali per definire eventi di modifica del risparmio di energia aggiuntivi.

Per ulteriori informazioni sulla risposta agli eventi di alimentazione di Windows, vedere l'articolo [monitorare e rispondere agli eventi di Power Windows con PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) in Scripting Guy! .

## <a name="examples"></a>Esempio

Il codice VBScript seguente monitora le modifiche allo stato di alimentazione in un computer.


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> <dt>

[Monitoraggio delle modifiche allo stato di alimentazione del computer](/previous-versions/tn-archive/ee176537(v=technet.10))
</dt> </dl>

 

 
