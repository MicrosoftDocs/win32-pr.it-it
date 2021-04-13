---
title: Classe Win32_TerminalServiceSetting
description: Rappresenta la configurazione per un server Host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341113"
---
# <a name="win32_terminalservicesetting-class"></a>Win32 \_ TerminalServiceSetting (classe)

La classe WMI **\_ TerminalServiceSetting Win32** rappresenta la configurazione per un server Host sessione desktop remoto (host sessione Desktop remoto). Le impostazioni includono funzionalità quali la modalità server Host sessione Desktop remoto, le licenze, il desktop attivo, le autorizzazioni, l'eliminazione di cartelle temporanee e le directory temporanee per le sessioni.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico. Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TerminalServiceSetting** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TerminalServiceSetting** presenta questi metodi.



| Metodo                                                                                                                | Descrizione                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDirectConnectLicenseServer**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | Configura un nuovo server licenze nell'azienda.<br/>                                                                                                                  |
| [**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | Aggiunge il server licenze specificato alla fine dell'elenco dei server licenze specificati.<br/>                                                                                  |
| [**CanAccessLicenseServer**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | Determina se il server Host sessione Desktop remoto è autorizzato a richiedere le licenze CAL (Client Access License) di Servizi Desktop remoto da un server licenze Desktop remoto.<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | Imposta il tipo di licenza del server licenze Desktop remoto.<br/>                                                                                                       |
| [**CreateWinstation**](createwinstation-win32-terminalservicesetting.md)                                             | Crea un nuovo stack del listener in base alla combinazione univoca di nome del listener e NIC.<br/>                                                                              |
| [**DeleteDirectConnectLicenseServer**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | Elimina il server licenze specificato dall'organizzazione.<br/>                                                                                                           |
| [**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | Rimuove tutti i server licenze dall'elenco dei server licenze specificati.<br/>                                                                                             |
| [**FindLicenseServers**](findlicenseservers-win32-terminalservicesetting.md)                                         | Enumera tutti i server licenze Desktop remoto e il metodo di individuazione.<br/>                                                                                   |
| [**GetDomain**](getdomain-win32-terminalservicesetting.md)                                                           | Recupera il nome del dominio di cui è membro il server Host sessione Desktop remoto.<br/>                                                                                    |
| [**GetGracePeriodDays**](getgraceperioddays-win32-terminalservicesetting.md)                                         | Recupera il numero di giorni rimanenti nel periodo di tolleranza di gestione licenze Desktop remoto per un server Host sessione Desktop remoto.<br/>                                                     |
| [**GetRegisteredLicenseServerList**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | Ottiene l'elenco dei server licenze registrati.<br/>                                                                                                                        |
| [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Recupera l'elenco dei server licenze specificati.<br/>                                                                                                                    |
| [**GetTSLanaIds**](gettslanaids-win32-terminalservicesetting.md)                                                     | Ottiene gli ID e le descrizioni delle schede di rete Servizi Desktop remoto.<br/>                                                                                          |
| [**GetTStoLSConnectivityStatus**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | Determina lo stato di connettività tra Servizi Desktop remoto e un server licenze.<br/>                                                                            |
| [**GetWinstationDriverNames**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | Recupera un elenco di nomi di driver WinStation.<br/>                                                                                                                        |
| [**PingLicenseServer**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Effettua il ping del server licenze per determinare se si tratta di un server licenze valido.<br/>                                                                                         |
| [**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | Rimuove il server licenze specificato dall'elenco dei server licenze specificati.<br/>                                                                                        |
| [**SetAllowTSConnections**](win32-terminalservicesetting-setallowtsconnections.md)                                   | Imposta la proprietà **AllowTSConnections** .<br/>                                                                                                                           |
| [**SetDisableForcibleLogoff**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | Imposta la proprietà **DisableForcibleLogoff** .<br/>                                                                                                                        |
| [**SetFallbackPrintDriverType**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | Imposta la proprietà **FallbackPrintDriverType** .<br/>                                                                                                                      |
| [**SetHomeDirectory**](win32-terminalservicesetting-sethomedirectory.md)                                             | Imposta la proprietà **HomeDirectory** .<br/>                                                                                                                                |
| [**SetPolicyPropertyName**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | Imposta una delle proprietà seguenti: **DeleteTempFolders** o **UseTempFolders**.<br/>                                                                                  |
| [**SetPrimaryLicenseServer**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.<br/>                                                                          |
| [**SetProfilePath**](win32-terminalservicesetting-setprofilepath.md)                                                 | Imposta la proprietà **propath** .<br/>                                                                                                                                  |
| [**SetSingleSession**](win32-terminalservicesetting-setsinglesession.md)                                             | Imposta la proprietà **SingleSession** .<br/>                                                                                                                                |
| [**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Aggiorna l'elenco dei server licenze specificati, sostituendo i server licenze esistenti specificati.<br/>                                                                    |
| [**SetTimeZoneRedirection**](win32-terminalservicesetting-settimezoneredirection.md)                                 | Imposta la proprietà **TimeZoneRedirection** .<br/>                                                                                                                          |
| [**UpdateDirectConnectLicenseServer**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | Aggiorna l'elenco dei server licenze di individuazione.<br/>                                                                                                                      |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TerminalServiceSetting** dispone di queste proprietà.

<dl> <dt>

**ActiveDesktop**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se il desktop attivo è consentito in ogni sessione utente.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (0)


</dt> <dd>

Il desktop attivo non è consentito in ogni sessione utente.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (1)


</dt> <dd>

Active Desktop è consentito in ogni sessione utente.

</dd> </dl>

</dd> <dt>

**AllowTSConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se sono consentite nuove connessioni Servizi Desktop remoto.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Non sono consentite nuove connessioni.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Sono consentite nuove connessioni.

</dd> </dl>

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

**DeleteTempFolders**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se le directory temporanee vengono eliminate all'uscita.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

L'eliminazione di directory temporanee è disabilitata.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

L'eliminazione delle directory temporanee è abilitata.

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

**DirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è disponibile.

**Windows Server 2008:** Enumera l'elenco dei server licenze.

</dd> <dt>

**DisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Determina se un amministratore che è connesso alla console di può essere disconnesso forzatamente.

<dt>

0
</dt> <dd>

L'amministratore può essere disconnesso in modo forzato.

</dd> <dt>

1
</dt> <dd>

Impossibile disconnettere forzatamente l'amministratore.

</dd> </dl>

</dd> <dt>

**EnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se consentire ai client di connessione Desktop remoto di riconnettersi automaticamente alle sessioni in un server Host sessione Desktop remoto se il collegamento di rete è temporaneamente perduto.

<dt>

0 (0x0)
</dt> <dd>

La riconnessione automatica è disabilitata.

</dd> <dt>

1 (0x1)
</dt> <dd>

La riconnessione automatica è abilitata.

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**EnableDFSS**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se la pianificazione dinamica della condivisione equa (DFSS) è abilitata o disabilitata. Può corrispondere a uno dei valori seguenti.

**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.

<dt>

0
</dt> <dd>

DFSS è disabilitato.

</dd> <dt>

1
</dt> <dd>

DFSS è abilitato.

</dd> </dl>

</dd> <dt>

**EnableDiskFSS**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se è abilitata la pianificazione delle condivisioni corrette del disco.

<dt>

0 (0x0)
</dt> <dd>

La pianificazione delle condivisioni corrette del disco è disabilitata.

</dd> <dt>

1 (0x1)
</dt> <dd>

La pianificazione delle condivisioni corrette del disco è abilitata.

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**EnableNetworkFSS**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se è abilitata la pianificazione della condivisione di rete equa.

<dt>

0 (0x0)
</dt> <dd>

La pianificazione della condivisione equa della rete è disabilitata.

</dd> <dt>

1 (0x1)
</dt> <dd>

La pianificazione della condivisione equa della rete è abilitata.

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**EnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il Desktop remoto MSI è abilitato o disabilitato.

<dt>

0 (0x0)
</dt> <dd>

Disabled

</dd> <dt>

1 (0x1)
</dt> <dd>

Abilitato

</dd> </dl>

**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.

</dd> <dt>

**FallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il driver della stampante a cui eseguire il fallback.

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Nessun dirvers di fallback = 0** (0)


</dt> <dd>

Nessun driver di fallback.

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Migliore indovinare = 1** (1)


</dt> <dd>

Migliore ipotesi.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Migliore ipotesi, se non viene trovata alcuna corrispondenza con fallback a PCL = 2** (2)


</dt> <dd>

Migliore ipotesi. Se non viene trovata alcuna corrispondenza, eseguire il fallback a Hewlett-Packard PCL (Printer Control Language).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Migliore ipotesi, se non viene trovata alcuna corrispondenza per il fallback a PS = 3** (3)


</dt> <dd>

Migliore ipotesi. Se non viene trovata alcuna corrispondenza, eseguire il fallback a PostScript (PS).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Se non viene trovata alcuna corrispondenza, è consigliabile visualizzare sia i driver PCL che i driver PS = 4** (4)


</dt> <dd>

Migliore ipotesi. Se non viene trovata alcuna corrispondenza, visualizzare i driver PS e PCL.

</dd> </dl>

</dd> <dt>

**GetCapabilitiesID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID funzionalità per il provider.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Directory radice del computer.

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

**LicensingDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione della modalità di gestione delle licenze.

</dd> <dt>

**Gestione licenze**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della modalità di gestione licenze.

</dd> <dt>

**LicensingType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di licenza per la modalità server specificata.

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Terminal Server personale** (0)


</dt> <dd>

Server Host sessione Desktop remoto personale.

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Desktop remoto per l'amministrazione** (1)


</dt> <dd>

Desktop remoto per l'amministrazione.

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per dispositivo** (2)


</dt> <dd>

Per dispositivo. Valido per i server applicazioni.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (3)


</dt> <dd>

Per utente. Valido per i server applicazioni.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (4)


</dt> <dd>

Non configurato.

</dd> </dl>

</dd> <dt>

**LimitedUserSessions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se la funzionalità per limitare il numero di sessioni attive e inattive consentite in un server Host sessione Desktop remoto è abilitata. Ad esempio, è possibile impostare **LimitedUserSessions** per garantire la conformità delle licenze per una particolare applicazione installata nel server Host sessione Desktop remoto. In alternativa, è possibile limitare il numero massimo di sessioni in un server Host sessione Desktop remoto in una farm con carico bilanciato in modo che il server non venga sottoposta a overload in caso di errore di un altro server nella farm.

> [!Note]
>
> La sessione utilizzata per la connessione al server per scopi amministrativi non è influenzata da **LimitedUserSessions**.
>
> In un host sessione Desktop remoto server farm, se un utente supera il limite di sessione, la sessione verrà indirizzata a un altro server tramite il bilanciamento del carico di gestore connessione Desktop remoto. Se il server è un server autonomo, l'utente non sarà in grado di connettersi.
>
> A causa della sessione utilizzata per la connessione al server per scopi amministrativi e la tempistica dell'applicazione del numero di sessioni durante il ciclo di accesso, è consigliabile impostare **LimitedUserSessions** su un valore leggermente inferiore rispetto al limite fisico per il numero di sessioni in un server.
>
> La proprietà **LimitedUserSessions** è valida solo se è installato il servizio ruolo Host sessione Desktop remoto.

 

<dt>

0
</dt> <dd>

Caratteristica disabilitata.

</dd> <dt>

1 o superiore
</dt> <dd>

Un valore di uno o più rappresenta il numero massimo di sessioni (attive e inattive) consentite nel server Host sessione Desktop remoto.

</dd> </dl>

</dd> <dt>

**Accessi**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se sono consentite nuove sessioni. Questa impostazione non influisce sulle impostazioni esistenti.

<dt>

0
</dt> <dd>

Sono consentite nuove sessioni.

</dd> <dt>

1
</dt> <dd>

Non sono consentite nuove sessioni.

</dd> </dl>

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

**NetworkFSSCatchAllWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica il peso della condivisione equa della rete predefinita per il traffico di rete catch-all. I valori validi sono compresi tra 1 e 9.

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**NetworkFSSLocalSystemWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica il peso della condivisione equa della rete predefinito per i processi di sistema locale. I valori validi sono compresi tra 1 e 9.

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**NetworkFSSUserSessionWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica il peso della condivisione equa di rete predefinito per una sessione utente. I valori validi sono compresi tra 1 e 9.

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**PolicySourceAllowTSConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **AllowTSConnections** è configurata dal server o da criteri di gruppo.

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

**PolicySourceConfiguredLicenseServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se i server licenze restituiti dal metodo [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) sono configurati dal server o da criteri di gruppo.

**Windows Server 2008:** Questa proprietà non è disponibile.

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

**PolicySourceDeleteTempFolders**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **DeleteTempFolders** è configurata dal server o da criteri di gruppo.

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

**PolicySourceDirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è disponibile.

**Windows Server 2008:** Indica se la proprietà **DirectConnectLicenseServers** è configurata dal server o da criteri di gruppo.

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

**PolicySourceDisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà non è supportata.

**Windows Server 2008:** Determina se la proprietà **DisableForcibleLogoff** è configurata dal server o da criteri di gruppo.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo.

</dd> </dl>

</dd> <dt>

**PolicySourceEnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **EnableAutomaticReconnection** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**PolicySourceEnableDFSS**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **EnableDFSS** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.

</dd> <dt>

**PolicySourceEnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **EnableRemoteDesktopMSI** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.

</dd> <dt>

**PolicySourceFallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **FallbackPrintDriverType** è configurata dal server o da criteri di gruppo.

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

**PolicySourceHomeDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **HomeDirectory** è configurata dal server o da criteri di gruppo.

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

**PolicySourceLicensingType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **LicensingType** è configurata dal server o da criteri di gruppo.

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

**PolicySourceProfilePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **Proprietà** Profiler è configurata dal server o da criteri di gruppo.

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

**PolicySourceRedirectSmartCards**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **RedirectSmartCards** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**PolicySourceSingleSession**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **SingleSession** è configurata dal server o da criteri di gruppo.

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

**PolicySourceTimeZoneRedirection**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **TimeZoneRedirection** è configurata dal server o da criteri di gruppo.

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

**PolicySourceUseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **UseRDEasyPrintDriver** è configurata dal server o da criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**PolicySourceUseTempFolders**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **UseTempFolders** è configurata dal server o da criteri di gruppo.

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

**PossibleLicensingTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Desktop remoto per l'amministrazione", "per dispositivo", "per utente", "non configurato")
</dt> </dl>

Maschera di maschera che specifica i tipi di licenza disponibili. Può trattarsi di una combinazione di uno o più dei valori seguenti.

<dt>

1 (0x1)
</dt> <dd>

Sono supportate le licenze server Host sessione Desktop remoto personali.

</dd> <dt>

2 (0x2)
</dt> <dd>

Sono supportate le licenze Desktop remoto.

</dd> <dt>

4 (0x4)
</dt> <dd>

Sono supportate le licenze per dispositivo.

</dd> <dt>

8 (0x8)
</dt> <dd>

Sono supportate le licenze per utente.

</dd> </dl>

</dd> <dt>

**PercorsoProfilo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del profilo per il computer.

</dd> <dt>

**RedirectSmartCards**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se il reindirizzamento dei dispositivi Smart Card è consentito in una sessione remota.

<dt>

0 (0x0)
</dt> <dd>

Il reindirizzamento dei dispositivi con smart card non è consentito.

</dd> <dt>

1 (0x1)
</dt> <dd>

Il reindirizzamento dei dispositivi con smart card è consentito.

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del server Host sessione Desktop remoto le cui proprietà sono di interesse.

</dd> <dt>

**SessionBrokerDrainMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Modalità di accesso utente di gestore connessione Desktop remoto.

<dt>

0
</dt> <dd>

Consenti tutte le connessioni.

</dd> <dt>

1
</dt> <dd>

Consente la riconnessione, ma impedisce nuovi accessi fino a quando il server non viene riavviato.

</dd> <dt>

2
</dt> <dd>

Consente la riconnessione, ma impedisce nuovi accessi.

</dd> </dl>

</dd> <dt>

**SingleSession**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se sono consentite una o più sessioni di Servizi Desktop remoto per utente.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

Sono consentite più sessioni per utente.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

È consentita una sola sessione per utente.

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

**TerminalServerMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità operativa del server Host sessione Desktop remoto del servizio Servizi Desktop remoto. Questa modalità controlla i criteri di licenza applicabili, nonché se le funzionalità di compatibilità delle applicazioni sono abilitate.

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)


</dt> <dd>

Il server funziona come server applicazioni.

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)


</dt> <dd>

La sessione viene amministrata in remoto.

</dd> </dl>

</dd> <dt>

**TimeZoneRedirection**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il computer client può reindirizzare le impostazioni del fuso orario al Servizi Desktop remoto sessione.

<dt>

0
</dt> <dd>

Il reindirizzamento è disabilitato.

</dd> <dt>

1
</dt> <dd>

Il reindirizzamento è abilitato.

</dd> </dl>

</dd> <dt>

**UseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se il driver della stampante Easy Print di Desktopo remoto viene usato per prima per installare tutte le stampanti client.

<dt>

0
</dt> <dd>

Il server Host sessione Desktop remoto tenta di trovare un driver della stampante adatto per installare la stampante client. Se il server Host sessione Desktop remoto non dispone di un driver della stampante corrispondente alla stampante client, il server tenterà di utilizzare il driver Easy Print di Desktopo remoto per installare la stampante client.

</dd> <dt>

1
</dt> <dd>

Il server Host sessione Desktop remoto tenta innanzitutto di utilizzare il driver della stampante Easy Print di Desktopo remoto per installare tutte le stampanti client. Se per qualsiasi motivo non è possibile usare il driver della stampante Easy Print di Desktopo remoto, viene usato un driver della stampante nel server Host sessione Desktop remoto che corrisponde alla stampante client.

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**UserPermission**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se ogni sessione utente presenta una sicurezza rigida o flessibile.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La sicurezza è strettamente.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La sicurezza è rilassata.

</dd> </dl>

</dd> <dt>

**UseTempFolders**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se le directory temporanee vengono create ed eliminate in base alla singola sessione.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Le directory temporanee non vengono create ed eliminate per ogni sessione. Una viene creata per la prima sessione e non viene mai eliminata.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Le directory temporanee vengono create ed eliminate per ogni sessione.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

**Win32 \_ TerminalServiceSetting** è associato a [**Win32 \_ TerminalService**](win32-terminalservice.md) come proprietà **Setting** dell'associazione [**\_ TerminalServiceToSetting di Win32**](win32-terminalservicetosetting.md) .

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) è associato al [**\_ terminale Win32**](win32-terminal.md) come proprietà **Setting** dell'associazione [**\_ TerminalTerminalSetting di Win32**](win32-terminalterminalsetting.md) .

Per connettersi allo \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore di sei.

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
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> <dt>

[**\_Terminale Win32**](win32-terminal.md)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_TerminalTerminalSetting Win32**](win32-terminalterminalsetting.md)
</dt> <dt>

[**\_Impostazione CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

