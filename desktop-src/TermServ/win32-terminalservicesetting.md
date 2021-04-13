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
# <a name="win32_terminalservicesetting-class"></a><span data-ttu-id="049cc-105">Win32 \_ TerminalServiceSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="049cc-105">Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="049cc-106">La classe WMI **\_ TerminalServiceSetting Win32** rappresenta la configurazione per un server Host sessione desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="049cc-106">The **Win32\_TerminalServiceSetting** WMI class represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="049cc-107">Le impostazioni includono funzionalità quali la modalità server Host sessione Desktop remoto, le licenze, il desktop attivo, le autorizzazioni, l'eliminazione di cartelle temporanee e le directory temporanee per le sessioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-107">Settings include capabilities such as RD Session Host server mode, licensing, Active Desktop, permissions, deletion of temporary folders, and temporary directories for sessions.</span></span>

<span data-ttu-id="049cc-108">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="049cc-108">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="049cc-109">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="049cc-109">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="049cc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="049cc-110">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="049cc-111">Members</span><span class="sxs-lookup"><span data-stu-id="049cc-111">Members</span></span>

<span data-ttu-id="049cc-112">La classe **Win32 \_ TerminalServiceSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="049cc-112">The **Win32\_TerminalServiceSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="049cc-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="049cc-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="049cc-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="049cc-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="049cc-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="049cc-115">Methods</span></span>

<span data-ttu-id="049cc-116">La classe **Win32 \_ TerminalServiceSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="049cc-116">The **Win32\_TerminalServiceSetting** class has these methods.</span></span>



| <span data-ttu-id="049cc-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="049cc-117">Method</span></span>                                                                                                                | <span data-ttu-id="049cc-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="049cc-118">Description</span></span>                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="049cc-119">**AddDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="049cc-119">**AddDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | <span data-ttu-id="049cc-120">Configura un nuovo server licenze nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="049cc-120">Configures a new license server in the enterprise.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="049cc-121">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="049cc-121">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | <span data-ttu-id="049cc-122">Aggiunge il server licenze specificato alla fine dell'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="049cc-122">Adds the given license server to the end of the list of specified license servers.</span></span><br/>                                                                                  |
| [<span data-ttu-id="049cc-123">**CanAccessLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="049cc-123">**CanAccessLicenseServer**</span></span>](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | <span data-ttu-id="049cc-124">Determina se il server Host sessione Desktop remoto è autorizzato a richiedere le licenze CAL (Client Access License) di Servizi Desktop remoto da un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-124">Determines whether the RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="049cc-125">**ChangeMode**</span><span class="sxs-lookup"><span data-stu-id="049cc-125">**ChangeMode**</span></span>](win32-terminalservicesetting-changemode.md)                                                         | <span data-ttu-id="049cc-126">Imposta il tipo di licenza del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-126">Sets the licensing type of the Remote Desktop license server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="049cc-127">**CreateWinstation**</span><span class="sxs-lookup"><span data-stu-id="049cc-127">**CreateWinstation**</span></span>](createwinstation-win32-terminalservicesetting.md)                                             | <span data-ttu-id="049cc-128">Crea un nuovo stack del listener in base alla combinazione univoca di nome del listener e NIC.</span><span class="sxs-lookup"><span data-stu-id="049cc-128">Creates a new listener stack based on the unique combination of listener name and NIC.</span></span><br/>                                                                              |
| [<span data-ttu-id="049cc-129">**DeleteDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="049cc-129">**DeleteDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | <span data-ttu-id="049cc-130">Elimina il server licenze specificato dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="049cc-130">Deletes the specified license server from the enterprise.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="049cc-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="049cc-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | <span data-ttu-id="049cc-132">Rimuove tutti i server licenze dall'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="049cc-132">Removes all license servers from the list of specified license servers.</span></span><br/>                                                                                             |
| [<span data-ttu-id="049cc-133">**FindLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="049cc-133">**FindLicenseServers**</span></span>](findlicenseservers-win32-terminalservicesetting.md)                                         | <span data-ttu-id="049cc-134">Enumera tutti i server licenze Desktop remoto e il metodo di individuazione.</span><span class="sxs-lookup"><span data-stu-id="049cc-134">Enumerates all of the Remote Desktop license servers and the method of discovery.</span></span><br/>                                                                                   |
| [<span data-ttu-id="049cc-135">**GetDomain**</span><span class="sxs-lookup"><span data-stu-id="049cc-135">**GetDomain**</span></span>](getdomain-win32-terminalservicesetting.md)                                                           | <span data-ttu-id="049cc-136">Recupera il nome del dominio di cui è membro il server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-136">Retrieves the name of the domain that the RD Session Host server is a member of.</span></span><br/>                                                                                    |
| [<span data-ttu-id="049cc-137">**GetGracePeriodDays**</span><span class="sxs-lookup"><span data-stu-id="049cc-137">**GetGracePeriodDays**</span></span>](getgraceperioddays-win32-terminalservicesetting.md)                                         | <span data-ttu-id="049cc-138">Recupera il numero di giorni rimanenti nel periodo di tolleranza di gestione licenze Desktop remoto per un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-138">Retrieves the number of days that are remaining in the RD Licensing grace period for an RD Session Host server.</span></span><br/>                                                     |
| [<span data-ttu-id="049cc-139">**GetRegisteredLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="049cc-139">**GetRegisteredLicenseServerList**</span></span>](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | <span data-ttu-id="049cc-140">Ottiene l'elenco dei server licenze registrati.</span><span class="sxs-lookup"><span data-stu-id="049cc-140">Gets the list of registered license servers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="049cc-141">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="049cc-141">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="049cc-142">Recupera l'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="049cc-142">Retrieves the list of specified license servers.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="049cc-143">**GetTSLanaIds**</span><span class="sxs-lookup"><span data-stu-id="049cc-143">**GetTSLanaIds**</span></span>](gettslanaids-win32-terminalservicesetting.md)                                                     | <span data-ttu-id="049cc-144">Ottiene gli ID e le descrizioni delle schede di rete Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-144">Gets the IDs and descriptions of Remote Desktop Services network adapters.</span></span><br/>                                                                                          |
| [<span data-ttu-id="049cc-145">**GetTStoLSConnectivityStatus**</span><span class="sxs-lookup"><span data-stu-id="049cc-145">**GetTStoLSConnectivityStatus**</span></span>](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | <span data-ttu-id="049cc-146">Determina lo stato di connettività tra Servizi Desktop remoto e un server licenze.</span><span class="sxs-lookup"><span data-stu-id="049cc-146">Determines the connectivity status between Remote Desktop Services and a license server.</span></span><br/>                                                                            |
| [<span data-ttu-id="049cc-147">**GetWinstationDriverNames**</span><span class="sxs-lookup"><span data-stu-id="049cc-147">**GetWinstationDriverNames**</span></span>](getwinstationdrivernames-win32-terminalservicesetting.md)                             | <span data-ttu-id="049cc-148">Recupera un elenco di nomi di driver WinStation.</span><span class="sxs-lookup"><span data-stu-id="049cc-148">Retrieves a list of Winstation driver names.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="049cc-149">**PingLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="049cc-149">**PingLicenseServer**</span></span>](pinglicenseserver-win32-terminalservicesetting.md)                                           | <span data-ttu-id="049cc-150">Effettua il ping del server licenze per determinare se si tratta di un server licenze valido.</span><span class="sxs-lookup"><span data-stu-id="049cc-150">Pings the license server to determine whether it is a valid license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="049cc-151">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="049cc-151">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | <span data-ttu-id="049cc-152">Rimuove il server licenze specificato dall'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="049cc-152">Removes the given license server from the list of specified license servers.</span></span><br/>                                                                                        |
| [<span data-ttu-id="049cc-153">**SetAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="049cc-153">**SetAllowTSConnections**</span></span>](win32-terminalservicesetting-setallowtsconnections.md)                                   | <span data-ttu-id="049cc-154">Imposta la proprietà **AllowTSConnections** .</span><span class="sxs-lookup"><span data-stu-id="049cc-154">Sets the **AllowTSConnections** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="049cc-155">**SetDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="049cc-155">**SetDisableForcibleLogoff**</span></span>](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | <span data-ttu-id="049cc-156">Imposta la proprietà **DisableForcibleLogoff** .</span><span class="sxs-lookup"><span data-stu-id="049cc-156">Sets the **DisableForcibleLogoff** property.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="049cc-157">**SetFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="049cc-157">**SetFallbackPrintDriverType**</span></span>](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | <span data-ttu-id="049cc-158">Imposta la proprietà **FallbackPrintDriverType** .</span><span class="sxs-lookup"><span data-stu-id="049cc-158">Sets the **FallbackPrintDriverType** property.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="049cc-159">**SetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="049cc-159">**SetHomeDirectory**</span></span>](win32-terminalservicesetting-sethomedirectory.md)                                             | <span data-ttu-id="049cc-160">Imposta la proprietà **HomeDirectory** .</span><span class="sxs-lookup"><span data-stu-id="049cc-160">Sets the **HomeDirectory** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="049cc-161">**SetPolicyPropertyName**</span><span class="sxs-lookup"><span data-stu-id="049cc-161">**SetPolicyPropertyName**</span></span>](win32-terminalservicesetting-setpolicypropertyname.md)                                   | <span data-ttu-id="049cc-162">Imposta una delle proprietà seguenti: **DeleteTempFolders** o **UseTempFolders**.</span><span class="sxs-lookup"><span data-stu-id="049cc-162">Sets one of the following properties: **DeleteTempFolders** or **UseTempFolders**.</span></span><br/>                                                                                  |
| [<span data-ttu-id="049cc-163">**SetPrimaryLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="049cc-163">**SetPrimaryLicenseServer**</span></span>](setprimarylicenseserver-win32-terminalservicesetting.md)                               | <span data-ttu-id="049cc-164">Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="049cc-164">Sets the given license server as the first entry in the list of specified license servers.</span></span><br/>                                                                          |
| [<span data-ttu-id="049cc-165">**SetProfilePath**</span><span class="sxs-lookup"><span data-stu-id="049cc-165">**SetProfilePath**</span></span>](win32-terminalservicesetting-setprofilepath.md)                                                 | <span data-ttu-id="049cc-166">Imposta la proprietà **propath** .</span><span class="sxs-lookup"><span data-stu-id="049cc-166">Sets the **ProfilePath** property.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="049cc-167">**SetSingleSession**</span><span class="sxs-lookup"><span data-stu-id="049cc-167">**SetSingleSession**</span></span>](win32-terminalservicesetting-setsinglesession.md)                                             | <span data-ttu-id="049cc-168">Imposta la proprietà **SingleSession** .</span><span class="sxs-lookup"><span data-stu-id="049cc-168">Sets the **SingleSession** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="049cc-169">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="049cc-169">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="049cc-170">Aggiorna l'elenco dei server licenze specificati, sostituendo i server licenze esistenti specificati.</span><span class="sxs-lookup"><span data-stu-id="049cc-170">Updates the list of specified license servers, replacing any existing specified license servers.</span></span><br/>                                                                    |
| [<span data-ttu-id="049cc-171">**SetTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="049cc-171">**SetTimeZoneRedirection**</span></span>](win32-terminalservicesetting-settimezoneredirection.md)                                 | <span data-ttu-id="049cc-172">Imposta la proprietà **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="049cc-172">Sets the **TimeZoneRedirection** property.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="049cc-173">**UpdateDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="049cc-173">**UpdateDirectConnectLicenseServer**</span></span>](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | <span data-ttu-id="049cc-174">Aggiorna l'elenco dei server licenze di individuazione.</span><span class="sxs-lookup"><span data-stu-id="049cc-174">Updates the list of discovery license servers.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="049cc-175">Proprietà</span><span class="sxs-lookup"><span data-stu-id="049cc-175">Properties</span></span>

<span data-ttu-id="049cc-176">La classe **Win32 \_ TerminalServiceSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="049cc-176">The **Win32\_TerminalServiceSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="049cc-177">**ActiveDesktop**</span><span class="sxs-lookup"><span data-stu-id="049cc-177">**ActiveDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-178">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-179">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-180">Specifica se il desktop attivo è consentito in ogni sessione utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-180">Specifies whether Active Desktop is allowed in each user session.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="049cc-181"><span id="TRUE"></span><span id="true"></span>**True** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-181"><span id="TRUE"></span><span id="true"></span>**TRUE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-182">Il desktop attivo non è consentito in ogni sessione utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-182">Active Desktop is not allowed in each user session.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="049cc-183"><span id="FALSE"></span><span id="false"></span>**False** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-183"><span id="FALSE"></span><span id="false"></span>**FALSE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-184">Active Desktop è consentito in ogni sessione utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-184">Active Desktop is allowed in each user session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-185">**AllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="049cc-185">**AllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-186">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-188">Specifica se sono consentite nuove connessioni Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-188">Specifies whether new Remote Desktop Services connections are allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="049cc-189"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-189"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-190">Non sono consentite nuove connessioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-190">New connections are not allowed.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="049cc-191"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-191"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-192">Sono consentite nuove connessioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-192">New connections are allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-193">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="049cc-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049cc-196">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="049cc-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="049cc-197">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="049cc-197">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="049cc-198">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="049cc-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="049cc-199">**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="049cc-199">**DeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-200">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-202">Specifica se le directory temporanee vengono eliminate all'uscita.</span><span class="sxs-lookup"><span data-stu-id="049cc-202">Specifies whether temporary directories are deleted on exit.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="049cc-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-204">L'eliminazione di directory temporanee è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-204">Deletion of temporary directories is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="049cc-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-206">L'eliminazione delle directory temporanee è abilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-206">Deletion of temporary directories is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-207">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="049cc-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-210">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="049cc-210">Description of the object.</span></span>

<span data-ttu-id="049cc-211">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="049cc-211">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="049cc-212">**DirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="049cc-212">**DirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049cc-215">Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="049cc-215">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="049cc-216">Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-216">This property is not available.</span></span>

<span data-ttu-id="049cc-217">**Windows Server 2008:** Enumera l'elenco dei server licenze.</span><span class="sxs-lookup"><span data-stu-id="049cc-217">**Windows Server 2008:** Enumerates the list of license servers.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-218">**DisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="049cc-218">**DisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-219">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-221">Determina se un amministratore che è connesso alla console di può essere disconnesso forzatamente.</span><span class="sxs-lookup"><span data-stu-id="049cc-221">Determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span data-ttu-id="049cc-222">0</span><span class="sxs-lookup"><span data-stu-id="049cc-222">0</span></span>
</dt> <dd>

<span data-ttu-id="049cc-223">L'amministratore può essere disconnesso in modo forzato.</span><span class="sxs-lookup"><span data-stu-id="049cc-223">Administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-224">1</span><span class="sxs-lookup"><span data-stu-id="049cc-224">1</span></span>
</dt> <dd>

<span data-ttu-id="049cc-225">Impossibile disconnettere forzatamente l'amministratore.</span><span class="sxs-lookup"><span data-stu-id="049cc-225">Administrator cannot be forcibly logged off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-226">**EnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="049cc-226">**EnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-227">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-228">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-229">Specifica se consentire ai client di connessione Desktop remoto di riconnettersi automaticamente alle sessioni in un server Host sessione Desktop remoto se il collegamento di rete è temporaneamente perduto.</span><span class="sxs-lookup"><span data-stu-id="049cc-229">Specifies whether to allow Remote Desktop connection clients to automatically reconnect to sessions on an RD Session Host server if the network link is temporarily lost.</span></span>

<dt>

<span data-ttu-id="049cc-230">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-230">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-231">La riconnessione automatica è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-231">Automatic reconnection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-232">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-232">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-233">La riconnessione automatica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-233">Automatic reconnection is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="049cc-234">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-234">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-235">**EnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="049cc-235">**EnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-236">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-237">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-238">Indica se la pianificazione dinamica della condivisione equa (DFSS) è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-238">Indicates whether dynamic fair-share scheduling (DFSS) is enabled or disabled.</span></span> <span data-ttu-id="049cc-239">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="049cc-239">This can be one of the following values.</span></span>

<span data-ttu-id="049cc-240">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="049cc-240">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="049cc-241">0</span><span class="sxs-lookup"><span data-stu-id="049cc-241">0</span></span>
</dt> <dd>

<span data-ttu-id="049cc-242">DFSS è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="049cc-242">DFSS is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-243">1</span><span class="sxs-lookup"><span data-stu-id="049cc-243">1</span></span>
</dt> <dd>

<span data-ttu-id="049cc-244">DFSS è abilitato.</span><span class="sxs-lookup"><span data-stu-id="049cc-244">DFSS is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-245">**EnableDiskFSS**</span><span class="sxs-lookup"><span data-stu-id="049cc-245">**EnableDiskFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-246">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-247">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-247">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-248">Specifica se è abilitata la pianificazione delle condivisioni corrette del disco.</span><span class="sxs-lookup"><span data-stu-id="049cc-248">Specifies if disk fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="049cc-249">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-249">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-250">La pianificazione delle condivisioni corrette del disco è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-250">Disk fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-251">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-251">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-252">La pianificazione delle condivisioni corrette del disco è abilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-252">Disk fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="049cc-253">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-253">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-254">**EnableNetworkFSS**</span><span class="sxs-lookup"><span data-stu-id="049cc-254">**EnableNetworkFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-255">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-256">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-256">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-257">Specifica se è abilitata la pianificazione della condivisione di rete equa.</span><span class="sxs-lookup"><span data-stu-id="049cc-257">Specifies if network fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="049cc-258">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-258">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-259">La pianificazione della condivisione equa della rete è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-259">Network fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-260">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-260">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-261">La pianificazione della condivisione equa della rete è abilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-261">Network fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="049cc-262">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-262">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-263">**EnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="049cc-263">**EnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-264">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-265">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-266">Indica se il Desktop remoto MSI è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="049cc-266">Indicates whether the Remote Desktop MSI is enabled or disabled.</span></span>

<dt>

<span data-ttu-id="049cc-267">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-267">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-268">Disabled</span><span class="sxs-lookup"><span data-stu-id="049cc-268">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="049cc-269">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-269">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-270">Abilitato</span><span class="sxs-lookup"><span data-stu-id="049cc-270">Enabled</span></span>

</dd> </dl>

<span data-ttu-id="049cc-271">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="049cc-271">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-272">**FallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="049cc-272">**FallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-273">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-275">Specifica il driver della stampante a cui eseguire il fallback.</span><span class="sxs-lookup"><span data-stu-id="049cc-275">Specifies which printer driver to fallback to.</span></span>

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span data-ttu-id="049cc-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Nessun dirvers di fallback = 0** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No fallback dirvers=0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-277">Nessun driver di fallback.</span><span class="sxs-lookup"><span data-stu-id="049cc-277">No fallback drivers.</span></span>

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span data-ttu-id="049cc-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Migliore indovinare = 1** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Best guess=1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-279">Migliore ipotesi.</span><span class="sxs-lookup"><span data-stu-id="049cc-279">Best guess.</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span data-ttu-id="049cc-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Migliore ipotesi, se non viene trovata alcuna corrispondenza con fallback a PCL = 2** (2)</span><span class="sxs-lookup"><span data-stu-id="049cc-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Best guess, if no match is found fallback to PCL=2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-281">Migliore ipotesi.</span><span class="sxs-lookup"><span data-stu-id="049cc-281">Best guess.</span></span> <span data-ttu-id="049cc-282">Se non viene trovata alcuna corrispondenza, eseguire il fallback a Hewlett-Packard PCL (Printer Control Language).</span><span class="sxs-lookup"><span data-stu-id="049cc-282">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span data-ttu-id="049cc-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Migliore ipotesi, se non viene trovata alcuna corrispondenza per il fallback a PS = 3** (3)</span><span class="sxs-lookup"><span data-stu-id="049cc-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Best guess, if no match is found fallback to PS=3** (3)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-284">Migliore ipotesi.</span><span class="sxs-lookup"><span data-stu-id="049cc-284">Best guess.</span></span> <span data-ttu-id="049cc-285">Se non viene trovata alcuna corrispondenza, eseguire il fallback a PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="049cc-285">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span data-ttu-id="049cc-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Se non viene trovata alcuna corrispondenza, è consigliabile visualizzare sia i driver PCL che i driver PS = 4** (4)</span><span class="sxs-lookup"><span data-stu-id="049cc-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Best guess, if no match is found show both PCL and PS drivers=4** (4)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-287">Migliore ipotesi.</span><span class="sxs-lookup"><span data-stu-id="049cc-287">Best guess.</span></span> <span data-ttu-id="049cc-288">Se non viene trovata alcuna corrispondenza, visualizzare i driver PS e PCL.</span><span class="sxs-lookup"><span data-stu-id="049cc-288">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-289">**GetCapabilitiesID**</span><span class="sxs-lookup"><span data-stu-id="049cc-289">**GetCapabilitiesID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-290">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-292">ID funzionalità per il provider.</span><span class="sxs-lookup"><span data-stu-id="049cc-292">Capabilities ID for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-293">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="049cc-293">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-296">Directory radice del computer.</span><span class="sxs-lookup"><span data-stu-id="049cc-296">The root directory for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="049cc-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-298">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="049cc-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049cc-300">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="049cc-300">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="049cc-301">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="049cc-301">The date the object was installed.</span></span> <span data-ttu-id="049cc-302">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="049cc-302">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="049cc-303">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="049cc-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="049cc-304">**LicensingDescription**</span><span class="sxs-lookup"><span data-stu-id="049cc-304">**LicensingDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-307">Breve descrizione della modalità di gestione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="049cc-307">A brief description of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-308">**Gestione licenze**</span><span class="sxs-lookup"><span data-stu-id="049cc-308">**LicensingName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-311">Nome della modalità di gestione licenze.</span><span class="sxs-lookup"><span data-stu-id="049cc-311">The name of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-312">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="049cc-312">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-313">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-315">Tipo di licenza per la modalità server specificata.</span><span class="sxs-lookup"><span data-stu-id="049cc-315">The licensing type for the specified server mode.</span></span>

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span data-ttu-id="049cc-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Terminal Server personale** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-317">Server Host sessione Desktop remoto personale.</span><span class="sxs-lookup"><span data-stu-id="049cc-317">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span data-ttu-id="049cc-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Desktop remoto per l'amministrazione** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remote Desktop for Administration** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-319">Desktop remoto per l'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="049cc-319">Remote Desktop for Administration.</span></span>

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="049cc-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="049cc-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per Device** (2)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-321">Per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="049cc-321">Per Device.</span></span> <span data-ttu-id="049cc-322">Valido per i server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-322">Valid for application servers.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="049cc-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (3)</span><span class="sxs-lookup"><span data-stu-id="049cc-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (3)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-324">Per utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-324">Per User.</span></span> <span data-ttu-id="049cc-325">Valido per i server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-325">Valid for application servers.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="049cc-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (4)</span><span class="sxs-lookup"><span data-stu-id="049cc-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (4)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-327">Non configurato.</span><span class="sxs-lookup"><span data-stu-id="049cc-327">Not Configured.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-328">**LimitedUserSessions**</span><span class="sxs-lookup"><span data-stu-id="049cc-328">**LimitedUserSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-329">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-330">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-330">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-331">Indica se la funzionalità per limitare il numero di sessioni attive e inattive consentite in un server Host sessione Desktop remoto è abilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-331">Indicates whether the feature to limit the number of both active and inactive sessions that are allowed on an RD Session Host server is enabled.</span></span> <span data-ttu-id="049cc-332">Ad esempio, è possibile impostare **LimitedUserSessions** per garantire la conformità delle licenze per una particolare applicazione installata nel server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-332">For example, you may want to set **LimitedUserSessions** to guarantee license compliance for a particular application that is installed on the RD Session Host server.</span></span> <span data-ttu-id="049cc-333">In alternativa, è possibile limitare il numero massimo di sessioni in un server Host sessione Desktop remoto in una farm con carico bilanciato in modo che il server non venga sottoposta a overload in caso di errore di un altro server nella farm.</span><span class="sxs-lookup"><span data-stu-id="049cc-333">Or, you may want to limit the maximum number of sessions on an RD Session Host server in a load-balanced farm so that the server will not be overloaded if another server in the farm fails.</span></span>

> [!Note]
>
> <span data-ttu-id="049cc-334">La sessione utilizzata per la connessione al server per scopi amministrativi non è influenzata da **LimitedUserSessions**.</span><span class="sxs-lookup"><span data-stu-id="049cc-334">The session that is used to connect to the server for administrative purposes is not affected by **LimitedUserSessions**.</span></span>
>
> <span data-ttu-id="049cc-335">In un host sessione Desktop remoto server farm, se un utente supera il limite di sessione, la sessione verrà indirizzata a un altro server tramite il bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-335">In an RD Session Host server farm, if a user exceeds the session limit, the session will be directed to another server by RD Connection Broker load balancing.</span></span> <span data-ttu-id="049cc-336">Se il server è un server autonomo, l'utente non sarà in grado di connettersi.</span><span class="sxs-lookup"><span data-stu-id="049cc-336">If the server is a stand-alone server, the user will not be able to connect.</span></span>
>
> <span data-ttu-id="049cc-337">A causa della sessione utilizzata per la connessione al server per scopi amministrativi e la tempistica dell'applicazione del numero di sessioni durante il ciclo di accesso, è consigliabile impostare **LimitedUserSessions** su un valore leggermente inferiore rispetto al limite fisico per il numero di sessioni in un server.</span><span class="sxs-lookup"><span data-stu-id="049cc-337">Because of the session that is used to connect to the server for administrative purposes, and the timing of the enforcement of the number of sessions during the logon cycle, it is recommended that you set **LimitedUserSessions** to a value that is slightly lower that the physical limit for the number of sessions on a server.</span></span>
>
> <span data-ttu-id="049cc-338">La proprietà **LimitedUserSessions** è valida solo se è installato il servizio ruolo Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-338">The **LimitedUserSessions** property is only valid if the RD Session Host role service is installed.</span></span>

 

<dt>

<span data-ttu-id="049cc-339">0</span><span class="sxs-lookup"><span data-stu-id="049cc-339">0</span></span>
</dt> <dd>

<span data-ttu-id="049cc-340">Caratteristica disabilitata.</span><span class="sxs-lookup"><span data-stu-id="049cc-340">The feature is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-341">1 o superiore</span><span class="sxs-lookup"><span data-stu-id="049cc-341">1 or greater</span></span>
</dt> <dd>

<span data-ttu-id="049cc-342">Un valore di uno o più rappresenta il numero massimo di sessioni (attive e inattive) consentite nel server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-342">A value of one or greater represents the maximum number of sessions (both active and inactive) that are allowed on the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-343">**Accessi**</span><span class="sxs-lookup"><span data-stu-id="049cc-343">**Logons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-344">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-345">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-345">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-346">Specifica se sono consentite nuove sessioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-346">Specifies whether new sessions are allowed.</span></span> <span data-ttu-id="049cc-347">Questa impostazione non influisce sulle impostazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="049cc-347">This setting does not affect existing settings.</span></span>

<dt>

<span data-ttu-id="049cc-348">0</span><span class="sxs-lookup"><span data-stu-id="049cc-348">0</span></span>
</dt> <dd>

<span data-ttu-id="049cc-349">Sono consentite nuove sessioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-349">New sessions are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-350">1</span><span class="sxs-lookup"><span data-stu-id="049cc-350">1</span></span>
</dt> <dd>

<span data-ttu-id="049cc-351">Non sono consentite nuove sessioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-351">New sessions are not allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-352">**Nome**</span><span class="sxs-lookup"><span data-stu-id="049cc-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-355">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="049cc-355">The name of the object.</span></span>

<span data-ttu-id="049cc-356">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="049cc-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="049cc-357">**NetworkFSSCatchAllWeight**</span><span class="sxs-lookup"><span data-stu-id="049cc-357">**NetworkFSSCatchAllWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-358">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-359">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-359">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-360">Specifica il peso della condivisione equa della rete predefinita per il traffico di rete catch-all.</span><span class="sxs-lookup"><span data-stu-id="049cc-360">Specifies the default network fair share weight for catch-all network traffic.</span></span> <span data-ttu-id="049cc-361">I valori validi sono compresi tra 1 e 9.</span><span class="sxs-lookup"><span data-stu-id="049cc-361">Valid values are 1 to 9.</span></span>

<span data-ttu-id="049cc-362">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-362">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-363">**NetworkFSSLocalSystemWeight**</span><span class="sxs-lookup"><span data-stu-id="049cc-363">**NetworkFSSLocalSystemWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-364">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-365">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-365">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-366">Specifica il peso della condivisione equa della rete predefinito per i processi di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="049cc-366">Specifies the default network fair share weight for a local system processes.</span></span> <span data-ttu-id="049cc-367">I valori validi sono compresi tra 1 e 9.</span><span class="sxs-lookup"><span data-stu-id="049cc-367">Valid values are 1 to 9.</span></span>

<span data-ttu-id="049cc-368">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-368">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-369">**NetworkFSSUserSessionWeight**</span><span class="sxs-lookup"><span data-stu-id="049cc-369">**NetworkFSSUserSessionWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-370">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-371">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-371">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-372">Specifica il peso della condivisione equa di rete predefinito per una sessione utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-372">Specifies the default network fair share weight for a user session.</span></span> <span data-ttu-id="049cc-373">I valori validi sono compresi tra 1 e 9.</span><span class="sxs-lookup"><span data-stu-id="049cc-373">Valid values are 1 to 9.</span></span>

<span data-ttu-id="049cc-374">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-374">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-375">**PolicySourceAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="049cc-375">**PolicySourceAllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-376">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-378">Indica se la proprietà **AllowTSConnections** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-378">Indicates whether the **AllowTSConnections** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-379">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-379">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-380">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-380">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-381">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-381">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-382">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-382">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-383">**PolicySourceConfiguredLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="049cc-383">**PolicySourceConfiguredLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-384">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-384">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-386">Indica se i server licenze restituiti dal metodo [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) sono configurati dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-386">Indicates whether the license servers returned by the [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) method are configured by the server or by group policy.</span></span>

<span data-ttu-id="049cc-387">**Windows Server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-387">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="049cc-388">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-388">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-389">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-389">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-390">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-390">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-391">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-391">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-392">**PolicySourceDeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="049cc-392">**PolicySourceDeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-393">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-395">Indica se la proprietà **DeleteTempFolders** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-395">Indicates whether the **DeleteTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-396">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-396">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-397">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-397">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-398">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-398">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-399">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-399">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-400">**PolicySourceDirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="049cc-400">**PolicySourceDirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-401">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-401">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049cc-403">Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="049cc-403">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="049cc-404">Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-404">This property is not available.</span></span>

<span data-ttu-id="049cc-405">**Windows Server 2008:** Indica se la proprietà **DirectConnectLicenseServers** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-405">**Windows Server 2008:** Indicates whether the **DirectConnectLicenseServers** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-406">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-406">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-407">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-407">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-408">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-408">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-409">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-409">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-410">**PolicySourceDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="049cc-410">**PolicySourceDisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-411">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-413">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="049cc-413">This property is not supported.</span></span>

<span data-ttu-id="049cc-414">**Windows Server 2008:** Determina se la proprietà **DisableForcibleLogoff** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-414">**Windows Server 2008:** Determines whether the **DisableForcibleLogoff** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-415">0</span><span class="sxs-lookup"><span data-stu-id="049cc-415">0</span></span>
</dt> <dd>

<span data-ttu-id="049cc-416">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-416">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-417">1</span><span class="sxs-lookup"><span data-stu-id="049cc-417">1</span></span>
</dt> <dd>

<span data-ttu-id="049cc-418">Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-418">Group Policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-419">**PolicySourceEnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="049cc-419">**PolicySourceEnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-420">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-422">Indica se la proprietà **EnableAutomaticReconnection** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-422">Indicates whether the **EnableAutomaticReconnection** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="049cc-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-424">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-426">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-426">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="049cc-427">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-427">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-428">**PolicySourceEnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="049cc-428">**PolicySourceEnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-429">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-431">Indica se la proprietà **EnableDFSS** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-431">Indicates whether the **EnableDFSS** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-432">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-432">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-433">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-433">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-434">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-434">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-435">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-435">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="049cc-436">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="049cc-436">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-437">**PolicySourceEnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="049cc-437">**PolicySourceEnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-438">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-440">Indica se la proprietà **EnableRemoteDesktopMSI** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-440">Indicates whether the **EnableRemoteDesktopMSI** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="049cc-441">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-441">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-442">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-442">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-443">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-443">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-444">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-444">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="049cc-445">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="049cc-445">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-446">**PolicySourceFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="049cc-446">**PolicySourceFallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-447">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-447">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-449">Indica se la proprietà **FallbackPrintDriverType** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-449">Indicates whether the **FallbackPrintDriverType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-450">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-450">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-451">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-451">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-452">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-452">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-453">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-453">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-454">**PolicySourceHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="049cc-454">**PolicySourceHomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-455">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-455">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-456">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-457">Indica se la proprietà **HomeDirectory** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-457">Indicates whether the **HomeDirectory** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-458">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-458">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-459">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-459">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-460">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-460">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-461">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-461">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-462">**PolicySourceLicensingType**</span><span class="sxs-lookup"><span data-stu-id="049cc-462">**PolicySourceLicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-463">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-464">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-465">Indica se la proprietà **LicensingType** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-465">Indicates whether the **LicensingType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-466">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-466">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-467">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-467">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-468">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-468">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-469">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-469">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-470">**PolicySourceProfilePath**</span><span class="sxs-lookup"><span data-stu-id="049cc-470">**PolicySourceProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-471">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-473">Indica se la **Proprietà** Profiler è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-473">Indicates whether the **ProfilePath** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-474">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-474">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-475">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-475">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-476">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-476">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-477">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-477">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-478">**PolicySourceRedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="049cc-478">**PolicySourceRedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-479">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-479">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-480">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-481">Indica se la proprietà **RedirectSmartCards** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-481">Indicates whether the **RedirectSmartCards** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="049cc-482">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-482">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-483">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-483">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-484">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-484">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-485">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-485">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="049cc-486">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-486">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-487">**PolicySourceSingleSession**</span><span class="sxs-lookup"><span data-stu-id="049cc-487">**PolicySourceSingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-488">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-489">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-490">Indica se la proprietà **SingleSession** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-490">Indicates whether the property **SingleSession** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-491">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-491">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-492">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-492">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-493">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-493">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-494">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-494">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-495">**PolicySourceTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="049cc-495">**PolicySourceTimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-496">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-497">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-498">Indica se la proprietà **TimeZoneRedirection** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-498">Indicates whether the property **TimeZoneRedirection** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-499">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-499">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-500">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-500">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-501">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-501">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-502">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-502">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-503">**PolicySourceUseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="049cc-503">**PolicySourceUseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-504">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-505">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-506">Indica se la proprietà **UseRDEasyPrintDriver** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-506">Indicates whether the **UseRDEasyPrintDriver** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="049cc-507">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-507">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-508">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-508">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-509">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-509">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-510">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-510">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="049cc-511">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-511">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-512">**PolicySourceUseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="049cc-512">**PolicySourceUseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-513">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-514">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-515">Indica se la proprietà **UseTempFolders** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="049cc-515">Indicates whether the **UseTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="049cc-516">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-516">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-517">Server</span><span class="sxs-lookup"><span data-stu-id="049cc-517">Server</span></span>

</dd> <dt>

<span data-ttu-id="049cc-518">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-518">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-519">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="049cc-519">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-520">**PossibleLicensingTypes**</span><span class="sxs-lookup"><span data-stu-id="049cc-520">**PossibleLicensingTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-521">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-522">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049cc-523">Qualificatori: [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Desktop remoto per l'amministrazione", "per dispositivo", "per utente", "non configurato")</span><span class="sxs-lookup"><span data-stu-id="049cc-523">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Remote Desktop for Administration", "Per Device", "Per User", "Not Configured")</span></span>
</dt> </dl>

<span data-ttu-id="049cc-524">Maschera di maschera che specifica i tipi di licenza disponibili.</span><span class="sxs-lookup"><span data-stu-id="049cc-524">A bitmask that specifies the licensing types that are available.</span></span> <span data-ttu-id="049cc-525">Può trattarsi di una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="049cc-525">This can be a combination of one or more of the following values.</span></span>

<dt>

<span data-ttu-id="049cc-526">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-526">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-527">Sono supportate le licenze server Host sessione Desktop remoto personali.</span><span class="sxs-lookup"><span data-stu-id="049cc-527">Personal RD Session Host server licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-528">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="049cc-528">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-529">Sono supportate le licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-529">Remote Desktop licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-530">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="049cc-530">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-531">Sono supportate le licenze per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="049cc-531">Per device licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-532">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="049cc-532">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-533">Sono supportate le licenze per utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-533">Per user licenses are supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-534">**PercorsoProfilo**</span><span class="sxs-lookup"><span data-stu-id="049cc-534">**ProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-535">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-536">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-537">Percorso del profilo per il computer.</span><span class="sxs-lookup"><span data-stu-id="049cc-537">Profile path for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-538">**RedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="049cc-538">**RedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-539">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-540">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-540">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-541">Specifica se il reindirizzamento dei dispositivi Smart Card è consentito in una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="049cc-541">Specifies if redirection of smart card devices is allowed in a remote session.</span></span>

<dt>

<span data-ttu-id="049cc-542">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="049cc-542">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-543">Il reindirizzamento dei dispositivi con smart card non è consentito.</span><span class="sxs-lookup"><span data-stu-id="049cc-543">Smart card device redirection is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-544">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="049cc-544">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="049cc-545">Il reindirizzamento dei dispositivi con smart card è consentito.</span><span class="sxs-lookup"><span data-stu-id="049cc-545">Smart card device redirection is allowed.</span></span>

</dd> </dl>

<span data-ttu-id="049cc-546">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-546">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-547">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="049cc-547">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-548">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-549">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049cc-550">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="049cc-550">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="049cc-551">Nome del server Host sessione Desktop remoto le cui proprietà sono di interesse.</span><span class="sxs-lookup"><span data-stu-id="049cc-551">Name of the RD Session Host server whose properties are of interest.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-552">**SessionBrokerDrainMode**</span><span class="sxs-lookup"><span data-stu-id="049cc-552">**SessionBrokerDrainMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-553">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-553">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-554">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-555">Modalità di accesso utente di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-555">The RD Connection Broker user logon mode.</span></span>

<dt>

<span data-ttu-id="049cc-556">0</span><span class="sxs-lookup"><span data-stu-id="049cc-556">0</span></span>
</dt> <dd>

<span data-ttu-id="049cc-557">Consenti tutte le connessioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-557">Allow all connections.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-558">1</span><span class="sxs-lookup"><span data-stu-id="049cc-558">1</span></span>
</dt> <dd>

<span data-ttu-id="049cc-559">Consente la riconnessione, ma impedisce nuovi accessi fino a quando il server non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="049cc-559">Allow reconnections, but prevent new logons until the server is restarted.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-560">2</span><span class="sxs-lookup"><span data-stu-id="049cc-560">2</span></span>
</dt> <dd>

<span data-ttu-id="049cc-561">Consente la riconnessione, ma impedisce nuovi accessi.</span><span class="sxs-lookup"><span data-stu-id="049cc-561">Allow reconnections, but prevent new logons.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-562">**SingleSession**</span><span class="sxs-lookup"><span data-stu-id="049cc-562">**SingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-563">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-564">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-565">Specifica se sono consentite una o più sessioni di Servizi Desktop remoto per utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-565">Specifies whether one or more Remote Desktop Services sessions are allowed per user.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="049cc-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-567">Sono consentite più sessioni per utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-567">More than one session is allowed per user.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="049cc-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-569">È consentita una sola sessione per utente.</span><span class="sxs-lookup"><span data-stu-id="049cc-569">Only one session is allowed per user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-570">**Status**</span><span class="sxs-lookup"><span data-stu-id="049cc-570">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-571">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="049cc-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-572">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049cc-573">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="049cc-573">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="049cc-574">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="049cc-574">Current status of the object.</span></span> <span data-ttu-id="049cc-575">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="049cc-575">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="049cc-576">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="049cc-576">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="049cc-577">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="049cc-577">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="049cc-578">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="049cc-578">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="049cc-579">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="049cc-579">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="049cc-580">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="049cc-580">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="049cc-581">("OK")</span><span class="sxs-lookup"><span data-stu-id="049cc-581">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="049cc-582">("Errore")</span><span class="sxs-lookup"><span data-stu-id="049cc-582">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="049cc-583">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="049cc-583">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="049cc-584">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="049cc-584">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="049cc-585">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="049cc-585">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="049cc-586">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="049cc-586">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="049cc-587">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="049cc-587">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="049cc-588">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="049cc-588">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-589">**TerminalServerMode**</span><span class="sxs-lookup"><span data-stu-id="049cc-589">**TerminalServerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-590">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-591">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-592">Modalità operativa del server Host sessione Desktop remoto del servizio Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-592">The RD Session Host server operating mode of the Remote Desktop Services service.</span></span> <span data-ttu-id="049cc-593">Questa modalità controlla i criteri di licenza applicabili, nonché se le funzionalità di compatibilità delle applicazioni sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="049cc-593">This mode controls the licensing policies that are applicable as well as whether application-compatibility features are enabled.</span></span>

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span data-ttu-id="049cc-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-595">Il server funziona come server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="049cc-595">The server operates as an application server.</span></span>

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span data-ttu-id="049cc-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-597">La sessione viene amministrata in remoto.</span><span class="sxs-lookup"><span data-stu-id="049cc-597">The session is administered remotely.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-598">**TimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="049cc-598">**TimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-599">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-599">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-600">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-600">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-601">Specifica se il computer client può reindirizzare le impostazioni del fuso orario al Servizi Desktop remoto sessione.</span><span class="sxs-lookup"><span data-stu-id="049cc-601">Specifies whether the client computer can redirect its time zone settings to the Remote Desktop Services session.</span></span>

<dt>

<span data-ttu-id="049cc-602">0</span><span class="sxs-lookup"><span data-stu-id="049cc-602">0</span></span>
</dt> <dd>

<span data-ttu-id="049cc-603">Il reindirizzamento è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="049cc-603">Redirection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-604">1</span><span class="sxs-lookup"><span data-stu-id="049cc-604">1</span></span>
</dt> <dd>

<span data-ttu-id="049cc-605">Il reindirizzamento è abilitato.</span><span class="sxs-lookup"><span data-stu-id="049cc-605">Redirection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-606">**UseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="049cc-606">**UseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-607">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-607">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-608">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-608">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-609">Specifica se il driver della stampante Easy Print di Desktopo remoto viene usato per prima per installare tutte le stampanti client.</span><span class="sxs-lookup"><span data-stu-id="049cc-609">Specifies whether the Remote Desktop Easy Print printer driver is used first to install all client printers.</span></span>

<dt>

<span data-ttu-id="049cc-610">0</span><span class="sxs-lookup"><span data-stu-id="049cc-610">0</span></span>
</dt> <dd>

<span data-ttu-id="049cc-611">Il server Host sessione Desktop remoto tenta di trovare un driver della stampante adatto per installare la stampante client.</span><span class="sxs-lookup"><span data-stu-id="049cc-611">The RD Session Host server tries to find a suitable printer driver to install the client printer.</span></span> <span data-ttu-id="049cc-612">Se il server Host sessione Desktop remoto non dispone di un driver della stampante corrispondente alla stampante client, il server tenterà di utilizzare il driver Easy Print di Desktopo remoto per installare la stampante client.</span><span class="sxs-lookup"><span data-stu-id="049cc-612">If the RD Session Host server does not have a printer driver that matches the client printer, the server tries to use the Remote Desktop Easy Print driver to install the client printer.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-613">1</span><span class="sxs-lookup"><span data-stu-id="049cc-613">1</span></span>
</dt> <dd>

<span data-ttu-id="049cc-614">Il server Host sessione Desktop remoto tenta innanzitutto di utilizzare il driver della stampante Easy Print di Desktopo remoto per installare tutte le stampanti client.</span><span class="sxs-lookup"><span data-stu-id="049cc-614">The RD Session Host server first tries to use the Remote Desktop Easy Print printer driver to install all client printers.</span></span> <span data-ttu-id="049cc-615">Se per qualsiasi motivo non è possibile usare il driver della stampante Easy Print di Desktopo remoto, viene usato un driver della stampante nel server Host sessione Desktop remoto che corrisponde alla stampante client.</span><span class="sxs-lookup"><span data-stu-id="049cc-615">If for any reason the Remote Desktop Easy Print printer driver cannot be used, a printer driver on the RD Session Host server that matches the client printer is used.</span></span>

</dd> </dl>

<span data-ttu-id="049cc-616">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-616">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="049cc-617">**UserPermission**</span><span class="sxs-lookup"><span data-stu-id="049cc-617">**UserPermission**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-618">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-618">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-619">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="049cc-619">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="049cc-620">Specifica se ogni sessione utente presenta una sicurezza rigida o flessibile.</span><span class="sxs-lookup"><span data-stu-id="049cc-620">Specifies if each user session has tight or relaxed security.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="049cc-621"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-621"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-622">La sicurezza è strettamente.</span><span class="sxs-lookup"><span data-stu-id="049cc-622">Security is tight.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="049cc-623"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-623"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-624">La sicurezza è rilassata.</span><span class="sxs-lookup"><span data-stu-id="049cc-624">Security is relaxed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="049cc-625">**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="049cc-625">**UseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049cc-626">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049cc-626">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049cc-627">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="049cc-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049cc-628">Specifica se le directory temporanee vengono create ed eliminate in base alla singola sessione.</span><span class="sxs-lookup"><span data-stu-id="049cc-628">Specifies whether temporary directories are created and deleted on a per-session basis.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="049cc-629"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="049cc-629"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-630">Le directory temporanee non vengono create ed eliminate per ogni sessione.</span><span class="sxs-lookup"><span data-stu-id="049cc-630">Temporary directories are not created and deleted for each session.</span></span> <span data-ttu-id="049cc-631">Una viene creata per la prima sessione e non viene mai eliminata.</span><span class="sxs-lookup"><span data-stu-id="049cc-631">One is created for the first session and never deleted.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="049cc-632"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="049cc-632"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="049cc-633">Le directory temporanee vengono create ed eliminate per ogni sessione.</span><span class="sxs-lookup"><span data-stu-id="049cc-633">Temporary directories are created and deleted for each session.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="049cc-634">Commenti</span><span class="sxs-lookup"><span data-stu-id="049cc-634">Remarks</span></span>

<span data-ttu-id="049cc-635">**Win32 \_ TerminalServiceSetting** è associato a [**Win32 \_ TerminalService**](win32-terminalservice.md) come proprietà **Setting** dell'associazione [**\_ TerminalServiceToSetting di Win32**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="049cc-635">**Win32\_TerminalServiceSetting** is associated to [**Win32\_TerminalService**](win32-terminalservice.md) as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="049cc-636">[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) è associato al [**\_ terminale Win32**](win32-terminal.md) come proprietà **Setting** dell'associazione [**\_ TerminalTerminalSetting di Win32**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="049cc-636">[**Win32\_TerminalSetting**](win32-terminalsetting.md) is associated to [**Win32\_Terminal**](win32-terminal.md) as the **Setting** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="049cc-637">Per connettersi allo \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="049cc-637">To connect to the Root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="049cc-638">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="049cc-638">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="049cc-639">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore di sei.</span><span class="sxs-lookup"><span data-stu-id="049cc-639">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="049cc-640">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="049cc-640">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="049cc-641">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="049cc-641">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="049cc-642">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="049cc-642">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="049cc-643">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="049cc-643">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="049cc-644">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="049cc-644">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="049cc-645">Requisiti</span><span class="sxs-lookup"><span data-stu-id="049cc-645">Requirements</span></span>



| <span data-ttu-id="049cc-646">Requisito</span><span class="sxs-lookup"><span data-stu-id="049cc-646">Requirement</span></span> | <span data-ttu-id="049cc-647">Valore</span><span class="sxs-lookup"><span data-stu-id="049cc-647">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="049cc-648">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="049cc-648">Minimum supported client</span></span><br/> | <span data-ttu-id="049cc-649">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="049cc-649">None supported</span></span><br/>                                                               |
| <span data-ttu-id="049cc-650">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="049cc-650">Minimum supported server</span></span><br/> | <span data-ttu-id="049cc-651">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="049cc-651">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="049cc-652">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="049cc-652">Namespace</span></span><br/>                | <span data-ttu-id="049cc-653">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="049cc-653">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="049cc-654">MOF</span><span class="sxs-lookup"><span data-stu-id="049cc-654">MOF</span></span><br/>                      | <dl> <span data-ttu-id="049cc-655"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="049cc-655"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="049cc-656">DLL</span><span class="sxs-lookup"><span data-stu-id="049cc-656">DLL</span></span><br/>                      | <dl> <span data-ttu-id="049cc-657"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="049cc-657"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="049cc-658">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="049cc-658">See also</span></span>

<dl> <dt>

[<span data-ttu-id="049cc-659">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="049cc-659">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="049cc-660">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="049cc-660">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="049cc-661">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="049cc-661">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="049cc-662">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="049cc-662">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="049cc-663">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="049cc-663">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dt>

[<span data-ttu-id="049cc-664">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="049cc-664">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

