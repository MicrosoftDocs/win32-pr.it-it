---
title: Classe Win32_TSClientSetting
description: Definisce le impostazioni di configurazione per la \_ classe terminale Win32 correlate ai criteri di connessione.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSClientSetting Servizi Desktop remoto
- Classe Win32_TSClientSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204f38570e1e023ca070ed1845e4574d9570b8ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121207"
---
# <a name="win32_tsclientsetting-class"></a>Win32 \_ TSClientSetting (classe)

La classe WMI **Win32 \_ TSClientSetting** definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) correlate ai criteri di connessione.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico. Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSClientSetting** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSClientSetting** presenta questi metodi.



| Metodo                                                                   | Descrizione                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionSettings**](win32-tsclientsetting-connectionsettings.md)   | Imposta le proprietà **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon** e **DefaultToClientPrinter** di questa classe.<br/>                      |
| [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md)                 | Non supportata.<br/> **Windows 7 e Windows Server 2008 R2:** Imposta la proprietà **AllowDwm** .<br/>                                               |
| [**SetClientProperty**](win32-tsclientsetting-setclientproperty.md)     | Imposta la proprietà **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** o **WindowsPrinterMapping** .<br/> |
| [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md)             | Imposta la proprietà **ColorDepth** .<br/>                                                                                                                 |
| [**SetColorDepthPolicy**](win32-tsclientsetting-setcolordepthpolicy.md) | Imposta la proprietà **ColorDepthPolicy** .<br/>                                                                                                           |
| [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md)           | Imposta la proprietà **MaxMonitors** .<br/>                                                                                                                |
| [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md)     | Imposta la proprietà **MaxXResolution** .<br/>                                                                                                             |
| [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md)     | Imposta la proprietà **MaxYResolution** .<br/>                                                                                                             |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSClientSetting** dispone di queste proprietà.

<dl> <dt>

**AdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se abilitare la grafica RemoteFX avanzata per RemoteApp.

**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2012 R2 e Windows 8.1.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

I grafici avanzati sono disabilitati.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

I grafici avanzati sono abilitati.

</dd> </dl>

</dd> <dt>

**AllowDwm**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà non è disponibile.

* * Windows 7 e Windows Server 2008 R2: * *

Specifica se abilitare o disabilitare la composizione del desktop remoto. Lo zero disabilita la composizione del desktop remoto e un valore diverso da zero lo Abilita.

Usare il metodo [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) per modificare questa proprietà.

</dd> <dt>

**AudioCaptureRedir**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se consentire il reindirizzamento dell'acquisizione audio.

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**AudioMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il mapping audio è disabilitato o abilitato.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Il mapping audio è abilitato.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Il mapping audio è disabilitato.

</dd> </dl>

</dd> <dt>

**AVC444ModePreferred**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se è preferibile la modalità AVC444.

**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 10 o Windows Server 2016.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa a una riga) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ClipboardMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il mapping degli Appunti è disabilitato o abilitato.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Il mapping degli Appunti è abilitato.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Il mapping degli Appunti è disabilitato.

</dd> </dl>

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la profondità del colore. Per i valori possibili, vedere il metodo [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) .

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span id="32_bit"></span><span id="32_BIT"></span>**bit 32** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ColorDepthPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se eseguire l'override dell'impostazione del colore massimo dell'utente.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Non eseguire l'override dei criteri dell'utente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Eseguire l'override dei criteri dell'utente.

</dd> </dl>

</dd> <dt>

**COMPortMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il mapping delle porte COM è disabilitato o abilitato.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Il mapping della porta COM è abilitato.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Il mapping della porta COM è disabilitato.

</dd> </dl>

</dd> <dt>

**ConnectClientDrivesAtLogon**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se le unità del client verranno connesse automaticamente durante il processo di accesso.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le unità non verranno connesse automaticamente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le unità verranno connesse automaticamente.

</dd> </dl>

</dd> <dt>

**ConnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Il criterio utilizzato dal server per recuperare le impostazioni di connessione utente.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)


</dt> <dd>

Le impostazioni di connessione dell'utente sono attive.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)


</dt> <dd>

Le impostazioni di connessione dell'utente vengono sostituite dal server.

</dd> </dl>

</dd> <dt>

**ConnectPrinterAtLogon**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se tutte le stampanti locali mappate del client verranno connesse automaticamente durante il processo di accesso.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le stampanti locali non verranno connesse automaticamente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le stampanti locali verranno connesse automaticamente.

</dd> </dl>

</dd> <dt>

**DefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se i processi di stampa verranno inviati automaticamente alla stampante locale del client.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

I processi di stampa non devono essere inviati automaticamente alla stampante locale del client.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

I processi di stampa devono essere inviati automaticamente alla stampante locale del client.

</dd> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DriveMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il mapping delle unità è disabilitato o abilitato.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Il mapping delle unità è abilitato.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Il mapping delle unità è disabilitato.

</dd> </dl>

</dd> <dt>

**EncodeImageQuality**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica la qualità dell'immagine per l'esperienza RDP.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

**Lossless** (1)


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

**alta** (2)


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

**media** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se il server Host sessione Desktop remoto utilizza il renderer della grafica hardware come adattatore predefinito.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LPTPortMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il mapping delle porte LPT è disabilitato o abilitato.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Il mapping della porta LPT è abilitato.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Il mapping della porta LPT è disabilitato.

</dd> </dl>

</dd> <dt>

**MaxMonitors**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di monitoraggi supportati dal server. Usare il metodo [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) per modificare questa proprietà.

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

</dd> <dt>

**MaxXResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Risoluzione X massima supportata dal server. Usare il metodo [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) per modificare questa proprietà.

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

</dd> <dt>

**MaxYResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La risoluzione Y massima supportata dal server. Usare il metodo [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) per modificare questa proprietà.

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PNPRedirection**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se consentire il reindirizzamento Plug and Play.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Consentire il reindirizzamento del Plug and Play.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Non consentire il reindirizzamento del Plug and Play.

</dd> </dl>

</dd> <dt>

**PolicyAdvancedRemoteAppGraphics**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **AdvancedRemoteAppGraphics** è configurata dal server o da criteri di gruppo.

**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2012 R2 e Windows 8.1.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceAllowDwm**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà non è disponibile.

* * Windows 7 e Windows Server 2008 R2: * *

Indica se la proprietà **AllowDwm** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceAudioCaptureRedir**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **AudioCaptureRedir** è configurata dal server o da criteri di gruppo.

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceAudioMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **AudioMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceAvc444ModePreferred**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il modo in cui la proprietà **AVC444ModePreferredis** è configurata.

**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 10 o Windows Server 2016.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceClipboardMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **ClipboardMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **ColorDepth** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceColorDepthPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **ColorDepthPolicy** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceCOMPortMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **COMPortMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceDefaultToClientPrinter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **DefaultToClientPrinter** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceDriveMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **DriveMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceEncodeImageQuality**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la modalità di configurazione di **EncodeImageQualityi** .

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceHardwareGraphicsAdapter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la modalità di configurazione di **HardwareGraphicsAdapter** .

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceLPTPortMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **LPTPortMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceMaxMonitors**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **MaxMonitors** è configurata in base al server, ai criteri di gruppo o al valore predefinito.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

</dd> <dt>

**PolicySourceMaxResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le proprietà **MaxXResolution** e **MaxYResolution** sono configurate dal server, dai criteri di gruppo o dal valore predefinito.

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourcePNPRedirection**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **PNPRedirection** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceRemoteSessionProfile**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la modalità di configurazione di **RemoteSessionProfile** .

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceSelectNetworkDetect**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il modo in cui la proprietà **SelectNetworkDetect** è configurata.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceSelectTransport**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il modo in cui la proprietà **SelectTransport** è configurata.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceVideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **VideoPlaybackRedir** è configurata dal server o da criteri di gruppo.

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

</dd> <dt>

**PolicySourceWindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **WindowsPrinterMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**RemoteSessionProfile**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica il profilo per l'esperienza RDP.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

<span id="scale"></span><span id="SCALE"></span>

**scala** (1)


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

**esperienza** (2)


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

**larghezza di banda** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**SelectNetworkDetect**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se viene utilizzato il rilevamento di rete.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

utilizzato in fase di connessione e in stato stabile.

</dd> <dt>

1
</dt> <dd>

disabilitato al momento della connessione

</dd> <dt>

2
</dt> <dd>

disabilitato in stato stazionario

</dd> <dt>

3
</dt> <dd>

disabilitato in fase di connessione e in stato stabile.

</dd> </dl>

</dd> <dt>

**SelectTransport**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica i protocolli di trasporto che possono essere utilizzati per l'accesso RDP al server.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.

<dt>

0
</dt> <dd>

Usare sia UDP che TCP.

</dd> <dt>

1
</dt> <dd>

Utilizzare solo TCP.

</dd> <dt>

2
</dt> <dd>

Utilizzare UDP o TCP.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Errore")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Errore di predazione")


</dt> <dd></dd> <dt>



 ("Avvio")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> <dt>

**Terminale**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del terminale.

Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**VideoPlaybackRedir**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se consentire il reindirizzamento della riproduzione video.

**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**WindowsPrinterMapping**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il mapping della stampante è disabilitato o abilitato per la finestra del client.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Il mapping della stampante è abilitato.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Il mapping della stampante è disabilitato.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

Tenere presente che una stazione della finestra associata alla sessione della console non può accedere ai metodi e alle proprietà di questa classe. Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà **TerminalName** , i metodi di questo oggetto restituiranno **WBEM \_ E \_ non \_ supportati**. Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto per aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.

Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore di sei.

Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Terminale Win32**](win32-terminal.md)
</dt> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> <dt>

[**\_Impostazione CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

