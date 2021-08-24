---
title: Win32_TerminalServiceSetting classe
description: Rappresenta la configurazione per un Desktop remoto host sessione Desktop remoto.
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceSetting classe Servizi Desktop remoto
- Win32_TerminalServiceSetting classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: 5a4d7aefdd3f0a684c91fda3ab73d17de32327f34e8d20d5a7f844ea07e21906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769891"
---
# <a name="win32_terminalservicesetting-class"></a>Classe TerminalServiceSetting Win32 \_

La **classe WMI \_ Win32 TerminalServiceSetting** rappresenta la configurazione per un server Desktop remoto Host sessione Desktop remoto. Impostazioni funzionalità quali la modalità server Host sessione Desktop remoto, le licenze, Active Desktop, le autorizzazioni, l'eliminazione di cartelle temporanee e le directory temporanee per le sessioni.

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

La **classe \_ TerminalServiceSetting Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ TerminalServiceSetting Win32** include questi metodi.



| Metodo                                                                                                                | Descrizione                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDirectConnectLicenseServer**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | Configura un nuovo server licenze nell'organizzazione.<br/>                                                                                                                  |
| [**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | Aggiunge il server licenze specificato alla fine dell'elenco di server licenze specificati.<br/>                                                                                  |
| [**CanAccessLicenseServer**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | Determina se al server Host sessione Desktop remoto è consentito richiedere Servizi Desktop remoto licenze CAL (Client Access License) da un server licenze Desktop remoto servizi Desktop remoto.<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | Imposta il tipo di licenza del Desktop remoto licenze.<br/>                                                                                                       |
| [**CreateWinstation**](createwinstation-win32-terminalservicesetting.md)                                             | Crea un nuovo stack di listener in base alla combinazione univoca del nome del listener e della scheda di interfaccia di rete.<br/>                                                                              |
| [**DeleteDirectConnectLicenseServer**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | Elimina il server licenze specificato dall'organizzazione.<br/>                                                                                                           |
| [**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | Rimuove tutti i server licenze dall'elenco dei server licenze specificati.<br/>                                                                                             |
| [**FindLicenseServers**](findlicenseservers-win32-terminalservicesetting.md)                                         | Enumera tutti i server Desktop remoto licenze e il metodo di individuazione.<br/>                                                                                   |
| [**GetDomain**](getdomain-win32-terminalservicesetting.md)                                                           | Recupera il nome del dominio di cui è membro il server Host sessione Desktop remoto.<br/>                                                                                    |
| [**GetGracePeriodDays**](getgraceperioddays-win32-terminalservicesetting.md)                                         | Recupera il numero di giorni rimanenti nel periodo di tolleranza di Licenze Desktop remoto per un server Host sessione Desktop remoto.<br/>                                                     |
| [**GetRegisteredLicenseServerList**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | Ottiene l'elenco dei server licenze registrati.<br/>                                                                                                                        |
| [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Recupera l'elenco di server licenze specificati.<br/>                                                                                                                    |
| [**GetTSLanaIds**](gettslanaids-win32-terminalservicesetting.md)                                                     | Ottiene gli ID e le descrizioni delle schede Servizi Desktop remoto di rete.<br/>                                                                                          |
| [**GetTStoLSConnectivityStatus**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | Determina lo stato di connettività tra Servizi Desktop remoto e un server licenze.<br/>                                                                            |
| [**GetWinstationDriverNames**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | Recupera un elenco di nomi di driver Winstation.<br/>                                                                                                                        |
| [**PingLicenseServer**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Esegue il ping del server licenze per determinare se si tratta di un server licenze valido.<br/>                                                                                         |
| [**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | Rimuove il server licenze specificato dall'elenco dei server licenze specificati.<br/>                                                                                        |
| [**SetAllowTSConnections**](win32-terminalservicesetting-setallowtsconnections.md)                                   | Imposta la **proprietà AllowTSConnections.**<br/>                                                                                                                           |
| [**SetDisableForcibleLogoff**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | Imposta la **proprietà DisableForcibleLogoff.**<br/>                                                                                                                        |
| [**SetFallbackPrintDriverType**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | Imposta la **proprietà FallbackPrintDriverType.**<br/>                                                                                                                      |
| [**SetHomeDirectory**](win32-terminalservicesetting-sethomedirectory.md)                                             | Imposta la **proprietà HomeDirectory.**<br/>                                                                                                                                |
| [**SetPolicyPropertyName**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | Imposta una delle proprietà seguenti: **DeleteTempFolders** o **UseTempFolders**.<br/>                                                                                  |
| [**SetPrimaryLicenseServer**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.<br/>                                                                          |
| [**SetProfilePath**](win32-terminalservicesetting-setprofilepath.md)                                                 | Imposta la **proprietà ProfilePath.**<br/>                                                                                                                                  |
| [**SetSingleSession**](win32-terminalservicesetting-setsinglesession.md)                                             | Imposta la **proprietà SingleSession.**<br/>                                                                                                                                |
| [**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Aggiorna l'elenco dei server licenze specificati, sostituendo eventuali server licenze specificati esistenti.<br/>                                                                    |
| [**SetTimeZoneRedirection**](win32-terminalservicesetting-settimezoneredirection.md)                                 | Imposta la **proprietà TimeZoneRedirection.**<br/>                                                                                                                          |
| [**UpdateDirectConnectLicenseServer**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | Aggiorna l'elenco dei server licenze di individuazione.<br/>                                                                                                                      |



 

### <a name="properties"></a>Proprietà

La **classe \_ TerminalServiceSetting Win32** ha queste proprietà.

<dl> <dt>

**ActiveDesktop**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se la Active Desktop è consentita in ogni sessione utente.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (0)


</dt> <dd>

Active Desktop non è consentito in ogni sessione utente.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (1)


</dt> <dd>

Active Desktop è consentito in ogni sessione utente.

</dd> </dl>

</dd> <dt>

**AllowTSConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se sono consentite Servizi Desktop remoto nuove connessioni.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Non sono consentite nuove connessioni.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Sono consentite nuove connessioni.

</dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa di una riga) dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DeleteTempFolders**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se le directory temporanee vengono eliminate all'uscita.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

L'eliminazione di directory temporanee è disabilitata.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

L'eliminazione di directory temporanee è abilitata.

</dd> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **DEPRECATO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è disponibile.

**Windows Server 2008:** Enumera l'elenco dei server licenze.

</dd> <dt>

**DisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Determina se un amministratore connesso alla console di può essere disconnesso forzatamente.

<dt>

0
</dt> <dd>

L'amministratore può essere disconnesso forzatamente.

</dd> <dt>

1
</dt> <dd>

Non è possibile disconnettersi forzatamente dall'amministratore.

</dd> </dl>

</dd> <dt>

**EnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se consentire ai client Desktop remoto di riconnettersi automaticamente alle sessioni in un server Host sessione Desktop remoto se il collegamento di rete viene temporaneamente perso.

<dt>

0 (0x0)
</dt> <dd>

La riconnessione automatica è disabilitata.

</dd> <dt>

1 (0x1)
</dt> <dd>

La riconnessione automatica è abilitata.

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**EnableDFSS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se la pianificazione dinamica delle condivisioni equa (DFSS) è abilitata o disabilitata. Può essere uno dei valori seguenti.

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se la pianificazione della condivisione equa dei dischi è abilitata.

<dt>

0 (0x0)
</dt> <dd>

La pianificazione della condivisione equa dei dischi è disabilitata.

</dd> <dt>

1 (0x1)
</dt> <dd>

La pianificazione della condivisione equa dei dischi è abilitata.

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**EnableNetworkFSS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se la pianificazione della condivisione equa di rete è abilitata.

<dt>

0 (0x0)
</dt> <dd>

La pianificazione della condivisione equa di rete è disabilitata.

</dd> <dt>

1 (0x1)
</dt> <dd>

La pianificazione della condivisione equa di rete è abilitata.

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**EnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se l'Desktop remoto MSI è abilitata o disabilitata.

<dt>

0 (0x0)
</dt> <dd>

Disabled

</dd> <dt>

1 (0x1)
</dt> <dd>

Attivato

</dd> </dl>

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**FallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il driver della stampante in cui eseguire il fallback.

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Nessun dirvers di fallback=0** (0)


</dt> <dd>

Nessun driver di fallback.

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Ipotesi migliore=1** (1)


</dt> <dd>

L'ipotesi migliore.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Ipotesi migliore, se non viene trovata alcuna corrispondenza fallback a PCL=2** (2)


</dt> <dd>

L'ipotesi migliore. Se non viene trovata alcuna corrispondenza, eseguire il fallback Hewlett-Packard Printer Control Language (PCL).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Ipotesi migliore, se non viene trovata alcuna corrispondenza fallback a PS=3** (3)


</dt> <dd>

L'ipotesi migliore. Se non viene trovata alcuna corrispondenza, eseguire il fallback a Postscript (PS).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**L'ipotesi migliore è che, se non viene trovata alcuna corrispondenza, vengono visualizzati sia i driver PCL che i driver PS=4** (4)


</dt> <dd>

L'ipotesi migliore. Se non viene trovata alcuna corrispondenza, visualizzare i driver PS e PCL.

</dd> </dl>

</dd> <dt>

**GetCapabilitiesID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID funzionalità per il provider.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Directory radice del computer.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**mappingstring**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LicensingDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione della modalità di gestione delle licenze.

</dd> <dt>

**LicensingName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della modalità di gestione delle licenze.

</dd> <dt>

**LicensingType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di licenza per la modalità server specificata.

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)


</dt> <dd>

Server Host sessione Desktop remoto personale.

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Desktop remoto per l'amministrazione** (1)


</dt> <dd>

Desktop remoto per Amministrazione.

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

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurato** (4)


</dt> <dd>

Non configurata.

</dd> </dl>

</dd> <dt>

**LimitedUserSessions**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se la funzionalità per limitare il numero di sessioni attive e inattive consentite in un server Host sessione Desktop remoto è abilitata. Ad esempio, è possibile impostare **LimitedUserSessions** per garantire la conformità delle licenze per una particolare applicazione installata nel server Host sessione Desktop remoto. In caso contrario, è possibile limitare il numero massimo di sessioni in un server Host sessione Desktop remoto in una farm con carico bilanciato in modo che il server non venga sovraccaricato in caso di errore di un altro server nella farm.

> [!Note]
>
> La sessione utilizzata per connettersi al server per scopi amministrativi non è interessata da **LimitedUserSessions**.
>
> In un host sessione Desktop remoto server farm, se un utente supera il limite di sessione, la sessione verrà indirizzata a un altro server dal bilanciamento del carico di Gestore connessione Desktop remoto. Se il server è un server autonomo, l'utente non sarà in grado di connettersi.
>
> A causa della sessione usata per connettersi al server a scopo amministrativo e della tempistica di imposizione del numero di sessioni durante il ciclo di accesso, è consigliabile impostare **LimitedUserSessions** su un valore leggermente inferiore rispetto al limite fisico per il numero di sessioni in un server.
>
> La **proprietà LimitedUserSessions** è valida solo se è installato il servizio ruolo Host sessione Desktop remoto.

 

<dt>

0
</dt> <dd>

Caratteristica disabilitata.

</dd> <dt>

1 o versione successiva
</dt> <dd>

Un valore maggiore o uguale a uno rappresenta il numero massimo di sessioni (attive e inattive) consentite nel server Host sessione Desktop remoto.

</dd> </dl>

</dd> <dt>

**Accessi**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se sono consentite nuove sessioni. Questa impostazione non influisce sulle impostazioni esistenti.

<dt>

0
</dt> <dd>

Sono consentite nuove sessioni.

</dd> <dt>

1
</dt> <dd>

Le nuove sessioni non sono consentite.

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NetworkFSSCatchAllWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica il peso predefinito della condivisione equa di rete per il traffico di rete catch-all. I valori validi sono da 1 a 9.

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**NetworkFSSLocalSystemWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica il peso predefinito della condivisione equa di rete per i processi del sistema locale. I valori validi sono da 1 a 9.

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**NetworkFSSUserSessionWeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica il peso predefinito della condivisione equa di rete per una sessione utente. I valori validi sono da 1 a 9.

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**PolicySourceAllowTSConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà AllowTSConnections** è configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se i server licenze restituiti dal [**metodo GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) sono configurati dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà DeleteTempFolders** è configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **DEPRECATO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà non è disponibile.

**Windows Server 2008:** Indica se la **proprietà DirectConnectLicenseServers è** configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà non è supportata.

**Windows Server 2008:** Determina se la **proprietà DisableForcibleLogoff** è configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **EnableAutomaticReconnection** è configurata dal server o da Criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**PolicySourceEnableDFSS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **EnableDFSS** è configurata dal server o da Criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**PolicySourceEnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **EnableRemoteDesktopMSI** è configurata dal server o da Criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows Server 2008:** Questa proprietà non è disponibile prima Windows Server 2008 R2.

</dd> <dt>

**PolicySourceFallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **FallbackPrintDriverType** è configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **HomeDirectory** è configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **LicensingType** è configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **ProfilePath** è configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà RedirectSmartCards è** configurata dal server o da Criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**PolicySourceSingleSession**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **SingleSession** è configurata dal server o da Criteri di gruppo.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **TimeZoneRedirection** è configurata dal server o da Criteri di gruppo.

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

**PolicySourceUseRDPrintDriver**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **UseRDPrintDriver** è configurata dal server o dai criteri di gruppo.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**PolicySourceUseTempFolders**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà UseTempFolders** è configurata dal server o da Criteri di gruppo.

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

**Tipi di licenza possibili**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Desktop remoto for Administration", "Per Device", "Per User", "Not Configured")
</dt> </dl>

Maschera di bit che specifica i tipi di licenza disponibili. Può essere una combinazione di uno o più dei valori seguenti.

<dt>

1 (0x1)
</dt> <dd>

Sono supportate le licenze del server Host sessione Desktop remoto personali.

</dd> <dt>

2 (0x2)
</dt> <dd>

Desktop remoto licenze sono supportate.

</dd> <dt>

4 (0x4)
</dt> <dd>

Le licenze per dispositivo sono supportate.

</dd> <dt>

8 (0x8)
</dt> <dd>

Sono supportate le licenze per utente.

</dd> </dl>

</dd> <dt>

**ProfilePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del profilo per il computer.

</dd> <dt>

**RedirectSmartCards**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se il reindirizzamento smart card dispositivi è consentito in una sessione remota.

<dt>

0 (0x0)
</dt> <dd>

Il reindirizzamento dei dispositivi smart card non è consentito.

</dd> <dt>

1 (0x1)
</dt> <dd>

Il reindirizzamento dei dispositivi smart card è consentito.

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del server Host sessione Desktop remoto le cui proprietà sono di interesse.

</dd> <dt>

**SessionBrokerDrainMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Modalità di accesso utente di Gestore connessione Desktop remoto.

<dt>

0
</dt> <dd>

Consentire tutte le connessioni.

</dd> <dt>

1
</dt> <dd>

Consentire le riconnessioni, ma impedire nuovi accessi fino al riavvio del server.

</dd> <dt>

2
</dt> <dd>

Consentire le riconnessioni, ma impedire nuovi accessi.

</dd> </dl>

</dd> <dt>

**SingleSession**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se una o più sessioni Servizi Desktop remoto sono consentite per utente.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

È consentita più di una sessione per utente.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

È consentita una sola sessione per utente.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati nonoperational includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono in linea, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalServerMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità operativa del server Host sessione Desktop remoto del Servizi Desktop remoto remoto. Questa modalità controlla i criteri di licenza applicabili, nonché se le funzionalità di compatibilità delle applicazioni sono abilitate.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il computer client può reindirizzare le impostazioni del fuso orario alla Servizi Desktop remoto sessione.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se il Easy Print di Desktopo remoto driver della stampante viene usato per primo per installare tutte le stampanti client.

<dt>

0
</dt> <dd>

Il server Host sessione Desktop remoto tenta di trovare un driver della stampante appropriato per installare la stampante client. Se il server Host sessione Desktop remoto non dispone di un driver della stampante corrispondente alla stampante client, il server tenta di usare il driver Easy Print di Desktopo remoto per installare la stampante client.

</dd> <dt>

1
</dt> <dd>

Il server Host sessione Desktop remoto tenta prima di tutto di usare Easy Print di Desktopo remoto driver della stampante per installare tutte le stampanti client. Se per qualsiasi motivo non è Easy Print di Desktopo remoto possibile usare il driver della stampante, viene usato un driver della stampante nel server Host sessione Desktop remoto corrispondente alla stampante client.

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è disponibile.

</dd> <dt>

**Userpermission**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se ogni sessione utente ha una sicurezza ristretta o meno rigida.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

La sicurezza è stretta.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

La sicurezza è più rilassata.

</dd> </dl>

</dd> <dt>

**UseTempFolders**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se le directory temporanee vengono create ed eliminate per sessione.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Le directory temporanee non vengono create ed eliminate per ogni sessione. Ne viene creata una per la prima sessione e non viene mai eliminata.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Le directory temporanee vengono create ed eliminate per ogni sessione.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

**Win32 \_ TerminalServiceSetting** è associato a [**\_ TerminalService Win32**](win32-terminalservice.md) come proprietà **Setting** dell'associazione [**\_ TerminalServiceToSetting Win32.**](win32-terminalservicetosetting.md)

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) è associato al [**\_ terminale Win32**](win32-terminal.md) come **proprietà Setting** dell'associazione [**\_ TerminalTerminalSetting Win32.**](win32-terminalterminalsetting.md)

Per connettersi allo spazio dei \\ nomi TerminalServices CIMV2 radice, il livello di autenticazione \\ deve includere la privacy dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione **di RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con valore sei.

Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dt>

[**Terminale Win32 \_**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_Terminale Win32TerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dt>

[**Impostazione \_ CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

