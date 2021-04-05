---
title: Classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Descrive un criterio di autorizzazione della connessione Desktop remoto (RD \ 160; LIMITE). RD \ 160; I tappi vengono usati per determinare se un utente è autorizzato a connettersi al server gateway gateway di Desktop remoto (Gateway Desktop remoto).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873689"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="bc275-106">Win32 \_ TSGatewayConnectionAuthorizationPolicy (classe)</span><span class="sxs-lookup"><span data-stu-id="bc275-106">Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="bc275-107">Descrive un criterio di autorizzazione della connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-107">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="bc275-108">I tappi desktop remoto vengono usati per determinare se un utente è autorizzato a connettersi al server gateway di Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="bc275-108">RD CAPs are used to determine whether a user is allowed to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc275-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc275-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a><span data-ttu-id="bc275-110">Members</span><span class="sxs-lookup"><span data-stu-id="bc275-110">Members</span></span>

<span data-ttu-id="bc275-111">La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bc275-111">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="bc275-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc275-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc275-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc275-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc275-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="bc275-114">Methods</span></span>

<span data-ttu-id="bc275-115">La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bc275-115">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="bc275-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="bc275-116">Method</span></span>                                                                                                                | <span data-ttu-id="bc275-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc275-117">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc275-118">**AddComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="bc275-118">**AddComputerGroupNames**</span></span>](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="bc275-119">Aggiunge i nomi dei gruppi di computer specificati alla proprietà **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="bc275-119">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span><br/>                                                                                      |
| [<span data-ttu-id="bc275-120">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="bc275-120">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="bc275-121">Aggiunge i nomi dei gruppi di utenti specificati alla proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="bc275-121">Adds the specified user group names to the **UserGroupNames** property.</span></span><br/>                                                                                              |
| [<span data-ttu-id="bc275-122">**Creare**</span><span class="sxs-lookup"><span data-stu-id="bc275-122">**Create**</span></span>](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="bc275-123">Crea un CAP RD.</span><span class="sxs-lookup"><span data-stu-id="bc275-123">Creates an RD CAP.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="bc275-124">**Delete**</span><span class="sxs-lookup"><span data-stu-id="bc275-124">**Delete**</span></span>](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="bc275-125">Elimina il CAP di RD corrente.</span><span class="sxs-lookup"><span data-stu-id="bc275-125">Deletes the current RD CAP.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="bc275-126">**DisableClipboard**</span><span class="sxs-lookup"><span data-stu-id="bc275-126">**DisableClipboard**</span></span>](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | <span data-ttu-id="bc275-127">Imposta la proprietà **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="bc275-127">Sets the **ClipboardDisabled** property.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="bc275-128">**DisableDiskDrives**</span><span class="sxs-lookup"><span data-stu-id="bc275-128">**DisableDiskDrives**</span></span>](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="bc275-129">Imposta la proprietà **DiskDrivesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="bc275-129">Sets the **DiskDrivesDisabled** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="bc275-130">**DisablePlugAndPlayDevices**</span><span class="sxs-lookup"><span data-stu-id="bc275-130">**DisablePlugAndPlayDevices**</span></span>](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | <span data-ttu-id="bc275-131">Imposta la proprietà **PlugAndPlayDevicesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="bc275-131">Sets the **PlugAndPlayDevicesDisabled** property.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="bc275-132">**DisablePrinters**</span><span class="sxs-lookup"><span data-stu-id="bc275-132">**DisablePrinters**</span></span>](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | <span data-ttu-id="bc275-133">Imposta la proprietà **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="bc275-133">Sets the **PrintersDisabled** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="bc275-134">**DisableSerialPorts**</span><span class="sxs-lookup"><span data-stu-id="bc275-134">**DisableSerialPorts**</span></span>](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="bc275-135">Imposta la proprietà **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="bc275-135">Sets the **SerialPortsDisabled** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="bc275-136">**EnableAllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="bc275-136">**EnableAllowOnlySDRServers**</span></span>](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | <span data-ttu-id="bc275-137">Usato per impostare o disabilitare la proprietà **AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="bc275-137">Used to toggle the **AllowOnlySDRServers** property</span></span><br/> <span data-ttu-id="bc275-138">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="bc275-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                  |
| [<span data-ttu-id="bc275-139">**MoveDown**</span><span class="sxs-lookup"><span data-stu-id="bc275-139">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | <span data-ttu-id="bc275-140">Sposta l'estremità corrente di una posizione verso il basso nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="bc275-140">Moves the current RD CAP one position down in the list.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="bc275-141">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="bc275-141">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="bc275-142">Sposta il CAP di RD corrente di una posizione verso l'alto nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="bc275-142">Moves the current RD CAP one position up in the list.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="bc275-143">**RemoveComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="bc275-143">**RemoveComputerGroupNames**</span></span>](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="bc275-144">Rimuove i nomi dei gruppi di computer specificati dalla proprietà **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="bc275-144">Removes the specified computer group names from the **ComputerGroupNames** property.</span></span><br/>                                                                                 |
| [<span data-ttu-id="bc275-145">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="bc275-145">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | <span data-ttu-id="bc275-146">Rimuove i nomi dei gruppi di utenti specificati dalla proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="bc275-146">Removes specified user group names from the **UserGroupNames** property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="bc275-147">**SetComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="bc275-147">**SetComputerGroupNames**</span></span>](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="bc275-148">Imposta la proprietà **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="bc275-148">Sets the **ComputerGroupNames** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="bc275-149">**SetCookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="bc275-149">**SetCookieAuthenticationAllowed**</span></span>](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | <span data-ttu-id="bc275-150">Imposta la proprietà **CookieAuthenticationAllowed** .</span><span class="sxs-lookup"><span data-stu-id="bc275-150">Sets the **CookieAuthenticationAllowed** property.</span></span><br/> <span data-ttu-id="bc275-151">**Windows Server 2008:** Questo metodo non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc275-151">**Windows Server 2008:** This method is not available.</span></span><br/>                                                 |
| [<span data-ttu-id="bc275-152">**SetDeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="bc275-152">**SetDeviceRedirectionType**</span></span>](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="bc275-153">Imposta la proprietà **DeviceRedirectionType** .</span><span class="sxs-lookup"><span data-stu-id="bc275-153">Sets the **DeviceRedirectionType** property.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="bc275-154">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="bc275-154">**SetEnabled**</span></span>](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | <span data-ttu-id="bc275-155">Abilita o Disabilita il criterio di autorizzazione connessioni Desktop remoto corrente.</span><span class="sxs-lookup"><span data-stu-id="bc275-155">Enables or disables the current RD CAP.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="bc275-156">**SetIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="bc275-156">**SetIdleTimeout**</span></span>](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | <span data-ttu-id="bc275-157">Imposta la proprietà **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="bc275-157">Sets the **IdleTimeout** property.</span></span><br/> <span data-ttu-id="bc275-158">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="bc275-158">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                   |
| [<span data-ttu-id="bc275-159">**SetName**</span><span class="sxs-lookup"><span data-stu-id="bc275-159">**SetName**</span></span>](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | <span data-ttu-id="bc275-160">Imposta un nuovo nome per il CAP di desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-160">Sets a new name for this RD CAP.</span></span> <span data-ttu-id="bc275-161">Questo metodo assicura che i nomi siano univoci.</span><span class="sxs-lookup"><span data-stu-id="bc275-161">This method ensures that names will be unique.</span></span><br/>                                                                                      |
| [<span data-ttu-id="bc275-162">**SetPasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="bc275-162">**SetPasswordAllowed**</span></span>](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="bc275-163">Imposta la proprietà **PasswordAllowed** .</span><span class="sxs-lookup"><span data-stu-id="bc275-163">Sets the **PasswordAllowed** property.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="bc275-164">**SetSecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="bc275-164">**SetSecureIdAllowed**</span></span>](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="bc275-165">Imposta la proprietà **SecureIdAllowed** .</span><span class="sxs-lookup"><span data-stu-id="bc275-165">Sets the **SecureIdAllowed** property.</span></span><br/> <span data-ttu-id="bc275-166">**Windows Server 2008:** Questo metodo è riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="bc275-166">**Windows Server 2008:** This method is reserved for future use.</span></span><br/>                                                   |
| [<span data-ttu-id="bc275-167">**SetSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="bc275-167">**SetSessionTimeout**</span></span>](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="bc275-168">Imposta le proprietà **SessionTimeout** e **SessionTimeoutAction** .</span><span class="sxs-lookup"><span data-stu-id="bc275-168">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span><br/> <span data-ttu-id="bc275-169">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="bc275-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/> |
| [<span data-ttu-id="bc275-170">**SetSmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="bc275-170">**SetSmartcardAllowed**</span></span>](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | <span data-ttu-id="bc275-171">Imposta la proprietà **SmartcardAllowed** .</span><span class="sxs-lookup"><span data-stu-id="bc275-171">Sets the **SmartcardAllowed** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="bc275-172">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="bc275-172">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="bc275-173">Imposta la proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="bc275-173">Sets the **UserGroupNames** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="bc275-174">**Aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="bc275-174">**Update**</span></span>](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="bc275-175">Aggiorna l'estremità del desktop remoto corrente.</span><span class="sxs-lookup"><span data-stu-id="bc275-175">Updates the current RD CAP.</span></span><br/>                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="bc275-176">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bc275-176">Properties</span></span>

<span data-ttu-id="bc275-177">La classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc275-177">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc275-178">**AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="bc275-178">**AllowOnlySDRServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-179">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-181">Indica se le connessioni sono consentite solo per i server RDS (Secure Device Reindirizzamento).</span><span class="sxs-lookup"><span data-stu-id="bc275-181">Indicates whether connections allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="bc275-182">Questa proprietà può essere impostata tramite il metodo [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .</span><span class="sxs-lookup"><span data-stu-id="bc275-182">This property can be set using the [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) method.</span></span>

<span data-ttu-id="bc275-183">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="bc275-183">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-184">**ClipboardDisabled**</span><span class="sxs-lookup"><span data-stu-id="bc275-184">**ClipboardDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-185">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-187">Indica se il reindirizzamento degli appunti verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bc275-187">Indicates if clipboard redirection will be disabled.</span></span> <span data-ttu-id="bc275-188">Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".</span><span class="sxs-lookup"><span data-stu-id="bc275-188">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="bc275-189">**ComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="bc275-189">**ComputerGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc275-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-192">Elenco di nomi di gruppi di computer separati da punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="bc275-192">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="bc275-193">Questo valore può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-193">This value can be empty.</span></span> <span data-ttu-id="bc275-194">I nomi sono nel formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="bc275-194">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="bc275-195">Se viene specificato un valore, il computer client deve appartenere a uno di questi gruppi di computer in modo che l'utente acceda al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-195">If a value is specified, then the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-196">**CookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="bc275-196">**CookieAuthenticationAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-197">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-199">Indica se l'autenticazione del cookie può essere utilizzata per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-199">Indicates if cookie authentication can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="bc275-200">Questa proprietà può essere impostata tramite il metodo [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="bc275-200">This property can be set by using the [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="bc275-201">**Windows Server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc275-201">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-202">**DeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="bc275-202">**DeviceRedirectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-203">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc275-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-205">Specifica i dispositivi che verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="bc275-205">Specifies which devices will be redirected.</span></span>

<dt>

<span data-ttu-id="bc275-206">0</span><span class="sxs-lookup"><span data-stu-id="bc275-206">0</span></span>
</dt> <dd>

<span data-ttu-id="bc275-207">Verranno reindirizzati tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="bc275-207">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-208">1</span><span class="sxs-lookup"><span data-stu-id="bc275-208">1</span></span>
</dt> <dd>

<span data-ttu-id="bc275-209">Non verrà reindirizzato alcun dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc275-209">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-210">2</span><span class="sxs-lookup"><span data-stu-id="bc275-210">2</span></span>
</dt> <dd>

<span data-ttu-id="bc275-211">I dispositivi specificati non verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="bc275-211">Specified devices will not be redirected.</span></span> <span data-ttu-id="bc275-212">Le proprietà **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controllano i dispositivi che non verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="bc275-212">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc275-213">**DiskDrivesDisabled**</span><span class="sxs-lookup"><span data-stu-id="bc275-213">**DiskDrivesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-214">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-216">Indica se il reindirizzamento dell'unità disco verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bc275-216">Indicates if disk drive redirection will be disabled.</span></span> <span data-ttu-id="bc275-217">Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".</span><span class="sxs-lookup"><span data-stu-id="bc275-217">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="bc275-218">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="bc275-218">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-219">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-221">Indica se il CAP RD verrà utilizzato per valutare l'autorizzazione di un utente.</span><span class="sxs-lookup"><span data-stu-id="bc275-221">Indicates whether this RD CAP will be used to evaluate a user for authorization.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-222">**HasNapAttributes**</span><span class="sxs-lookup"><span data-stu-id="bc275-222">**HasNapAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-223">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-225">Indica se il CAP RD utilizza gli attributi di protezione accesso alla rete (NAP).</span><span class="sxs-lookup"><span data-stu-id="bc275-225">Indicates if the RD CAP uses Network Access Protection (NAP) attributes.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-226">**IdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="bc275-226">**IdleTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-227">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc275-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-229">Valore del timeout di inattività, espresso in minuti.</span><span class="sxs-lookup"><span data-stu-id="bc275-229">The idle timeout value, in minutes.</span></span> <span data-ttu-id="bc275-230">Il valore 0 indica che non esiste alcun timeout.</span><span class="sxs-lookup"><span data-stu-id="bc275-230">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="bc275-231">Questa proprietà può essere impostata tramite il metodo [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="bc275-231">This property can be set by using the [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="bc275-232">**Windows Server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc275-232">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-233">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bc275-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-234">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc275-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc275-236">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc275-236">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc275-237">Nome del CAP di desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-237">Name of the RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-238">**Ordine**</span><span class="sxs-lookup"><span data-stu-id="bc275-238">**Order**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-239">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc275-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-241">Ordine di valutazione del CAP di desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-241">Evaluation order of the RD CAP.</span></span> <span data-ttu-id="bc275-242">Il primo CAP RD valutato ha un valore pari a "1".</span><span class="sxs-lookup"><span data-stu-id="bc275-242">The first RD CAP evaluated has a value of "1".</span></span> <span data-ttu-id="bc275-243">È possibile modificare la proprietà **Order** quando vengono chiamati i metodi [**create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)o [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="bc275-243">The **Order** property can be changed when the [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md), or [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-244">**PasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="bc275-244">**PasswordAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-245">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-247">Indica se è possibile utilizzare una password per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-247">Indicates if a password can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="bc275-248">Questa proprietà può essere modificata tramite il metodo [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="bc275-248">This property can be changed by using the [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-249">**PlugAndPlayDevicesDisabled**</span><span class="sxs-lookup"><span data-stu-id="bc275-249">**PlugAndPlayDevicesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-250">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-252">Indica se il reindirizzamento dei dispositivi Plug and Play sarà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bc275-252">Indicates if redirection of Plug and Play devices will be disabled.</span></span> <span data-ttu-id="bc275-253">Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".</span><span class="sxs-lookup"><span data-stu-id="bc275-253">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="bc275-254">**PrintersDisabled**</span><span class="sxs-lookup"><span data-stu-id="bc275-254">**PrintersDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-255">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-257">Indica se il reindirizzamento della stampante verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bc275-257">Indicates if printer redirection will be disabled.</span></span> <span data-ttu-id="bc275-258">Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".</span><span class="sxs-lookup"><span data-stu-id="bc275-258">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="bc275-259">**SecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="bc275-259">**SecureIdAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-260">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-260">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-262">Indica se è possibile utilizzare un identificatore sicuro per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-262">Indicates if a secure identifier can be used to connect to the RD Gateway server.</span></span>

<span data-ttu-id="bc275-263">**Windows Server 2008:** Questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="bc275-263">**Windows Server 2008:** This property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-264">**SerialPortsDisabled**</span><span class="sxs-lookup"><span data-stu-id="bc275-264">**SerialPortsDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-265">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-267">Indica se il reindirizzamento della porta seriale verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bc275-267">Indicates if serial port redirection will be disabled.</span></span> <span data-ttu-id="bc275-268">Questa proprietà ha effetto solo se il valore della proprietà **DeviceRedirectionType** è "2".</span><span class="sxs-lookup"><span data-stu-id="bc275-268">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="bc275-269">**SessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="bc275-269">**SessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-270">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc275-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-272">Valore di timeout della sessione, espresso in minuti.</span><span class="sxs-lookup"><span data-stu-id="bc275-272">The session timeout value, in minutes.</span></span> <span data-ttu-id="bc275-273">Il valore 0 indica che non esiste alcun timeout.</span><span class="sxs-lookup"><span data-stu-id="bc275-273">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="bc275-274">Questa proprietà può essere impostata tramite il metodo [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="bc275-274">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="bc275-275">**Windows Server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc275-275">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-276">**SessionTimeoutAction**</span><span class="sxs-lookup"><span data-stu-id="bc275-276">**SessionTimeoutAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-277">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc275-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-279">Specifica l'azione da intraprendere in caso di timeout di sessione.</span><span class="sxs-lookup"><span data-stu-id="bc275-279">Specifies the action to be taken in the case of a session timeout.</span></span> <span data-ttu-id="bc275-280">Questa proprietà può essere impostata tramite il metodo [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="bc275-280">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="bc275-281">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc275-281">This can be one of the following values.</span></span>

<span data-ttu-id="bc275-282">**Windows Server 2008:** Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc275-282">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="bc275-283">0</span><span class="sxs-lookup"><span data-stu-id="bc275-283">0</span></span>
</dt> <dd>

<span data-ttu-id="bc275-284">Disconnettere la sessione.</span><span class="sxs-lookup"><span data-stu-id="bc275-284">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-285">1</span><span class="sxs-lookup"><span data-stu-id="bc275-285">1</span></span>
</dt> <dd>

<span data-ttu-id="bc275-286">Tentativo di autorizzare nuovamente la sessione.</span><span class="sxs-lookup"><span data-stu-id="bc275-286">Attempt to re-authorize the session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc275-287">**SmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="bc275-287">**SmartcardAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-288">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bc275-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-290">Indica se è possibile utilizzare una smart card per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-290">Indicates if a smart card can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="bc275-291">Questa proprietà può essere modificata tramite il metodo [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="bc275-291">This property can be changed by using the [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="bc275-292">**UserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="bc275-292">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc275-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bc275-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc275-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bc275-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc275-295">Elenco di nomi di gruppi di utenti separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="bc275-295">List of semicolon-separated user group names.</span></span> <span data-ttu-id="bc275-296">I nomi sono nel formato *dominio \\ nomegruppoutenti*.</span><span class="sxs-lookup"><span data-stu-id="bc275-296">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="bc275-297">Se l'utente appartiene a uno di questi gruppi di utenti, l'utente sarà autorizzato ad accedere al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bc275-297">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc275-298">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc275-298">Remarks</span></span>

<span data-ttu-id="bc275-299">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="bc275-299">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="bc275-300">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bc275-300">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bc275-301">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bc275-301">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bc275-302">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bc275-302">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bc275-303">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bc275-303">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc275-304">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc275-304">Requirements</span></span>



| <span data-ttu-id="bc275-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc275-305">Requirement</span></span> | <span data-ttu-id="bc275-306">Valore</span><span class="sxs-lookup"><span data-stu-id="bc275-306">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc275-307">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc275-307">Minimum supported client</span></span><br/> | <span data-ttu-id="bc275-308">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bc275-308">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bc275-309">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc275-309">Minimum supported server</span></span><br/> | <span data-ttu-id="bc275-310">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc275-310">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bc275-311">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc275-311">Namespace</span></span><br/>                | <span data-ttu-id="bc275-312">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bc275-312">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bc275-313">MOF</span><span class="sxs-lookup"><span data-stu-id="bc275-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc275-314"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc275-314"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc275-315">DLL</span><span class="sxs-lookup"><span data-stu-id="bc275-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc275-316"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc275-316"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bc275-317">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc275-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc275-318">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="bc275-318">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="bc275-319">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="bc275-319">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="bc275-320">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="bc275-320">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="bc275-321">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="bc275-321">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="bc275-322">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="bc275-322">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="bc275-323">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="bc275-323">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

