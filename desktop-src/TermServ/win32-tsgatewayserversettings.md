---
title: Classe Win32_TSGatewayServerSettings
description: Fornisce metodi e proprietà per visualizzare e configurare le impostazioni del server Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478814"
---
# <a name="win32_tsgatewayserversettings-class"></a><span data-ttu-id="fe3a4-105">Win32 \_ TSGatewayServerSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="fe3a4-105">Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="fe3a4-106">Fornisce metodi e proprietà per visualizzare e configurare le impostazioni del server Desktop remoto Gateway (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="fe3a4-106">Provides methods and properties to view and configure Remote Desktop Gateway (RD Gateway) server settings.</span></span> <span data-ttu-id="fe3a4-107">Un amministratore può utilizzare questa classe per configurare un set di protocolli, il set di eventi che verranno scritti nel registro eventi e il numero massimo di connessioni tramite Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-107">An administrator can use this class to configure a set of protocols, the set of events that will be written to the event log, and the maximum number of connections through RD Gateway.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3a4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe3a4-108">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a><span data-ttu-id="fe3a4-109">Members</span><span class="sxs-lookup"><span data-stu-id="fe3a4-109">Members</span></span>

<span data-ttu-id="fe3a4-110">La classe **Win32 \_ TSGatewayServerSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fe3a4-110">The **Win32\_TSGatewayServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="fe3a4-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe3a4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fe3a4-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe3a4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fe3a4-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe3a4-113">Methods</span></span>

<span data-ttu-id="fe3a4-114">La classe **Win32 \_ TSGatewayServerSettings** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-114">The **Win32\_TSGatewayServerSettings** class has these methods.</span></span>



| <span data-ttu-id="fe3a4-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="fe3a4-115">Method</span></span>                                                                                                                                             | <span data-ttu-id="fe3a4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe3a4-116">Description</span></span>                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe3a4-117">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-117">**Configure**</span></span>](configure-win32-tsgatewayserversettings.md)                                                                                       | <span data-ttu-id="fe3a4-118">Configura le impostazioni RPC e IIS richieste dal servizio Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-118">Configures the IIS and RPC settings required by the RD Gateway service.</span></span><br/> <span data-ttu-id="fe3a4-119">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-119">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                               |
| [<span data-ttu-id="fe3a4-120">**EnableCentralCAP**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-120">**EnableCentralCAP**</span></span>](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="fe3a4-121">Abilita o Disabilita la proprietà **CentralCAPEnabled** , che controlla se vengono utilizzati i server di criteri di autorizzazione connessione Desktop remoto centrale (CAP) per controllare i criteri di autorizzazione della connessione per il server.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-121">Enables or disables the **CentralCAPEnabled** property, which controls whether central Remote Desktop connection authorization policy (RD CAP) servers are used for controlling connection authorization policies for this server.</span></span><br/>                    |
| [<span data-ttu-id="fe3a4-122">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-122">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="fe3a4-123">Abilita o Disabilita la registrazione del tipo di evento specificato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-123">Enables or disables logging of the specified event type.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="fe3a4-124">**EnableOnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-124">**EnableOnlyConsentCapableClients**</span></span>](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | <span data-ttu-id="fe3a4-125">Imposta la proprietà **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="fe3a4-125">Sets the **OnlyConsentCapableClients** property.</span></span><br/> <span data-ttu-id="fe3a4-126">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-126">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="fe3a4-127">**EnableRequestSOH**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-127">**EnableRequestSOH**</span></span>](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | <span data-ttu-id="fe3a4-128">Questo metodo non è supportato a partire da Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-128">This method is not supported starting with Windows Server 2016.</span></span><br/> <span data-ttu-id="fe3a4-129">**Windows server 2012 R2, Windows server 2012, Windows server 2008 R2 e Windows server 2008:** Abilita o Disabilita le richieste per un rapporto di integrità (SoH).</span><span class="sxs-lookup"><span data-stu-id="fe3a4-129">**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:** Enables or disables requests for a Statement of Health (SoH).</span></span><br/> <br/> |
| [<span data-ttu-id="fe3a4-130">**EnableTransport**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-130">**EnableTransport**</span></span>](enabletransport-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="fe3a4-131">Abilita o Disabilita il trasporto specificato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-131">Enables or disables the specified transport.</span></span><br/> <span data-ttu-id="fe3a4-132">**Windows server 2008 R2 e Windows server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-132">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="fe3a4-133">**EnumAuthenticationPlugins**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-133">**EnumAuthenticationPlugins**</span></span>](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | <span data-ttu-id="fe3a4-134">Enumera tutti i plug-in di autenticazione registrati.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-134">Enumerates all registered authentication plug-ins.</span></span><br/> <span data-ttu-id="fe3a4-135">**Windows Server 2008:** Questo metodo non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-135">**Windows Server 2008:** This method is not available.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="fe3a4-136">**EnumAuthorizationPlugins**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-136">**EnumAuthorizationPlugins**</span></span>](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="fe3a4-137">Enumera tutti i plug-in di autorizzazione registrati.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-137">Enumerates all registered authorization plug-ins.</span></span><br/> <span data-ttu-id="fe3a4-138">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="fe3a4-139">**GetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-139">**GetIPAndPort**</span></span>](getipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="fe3a4-140">Ottiene l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-140">Obtains the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="fe3a4-141">**Windows server 2008 R2 e Windows server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-141">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                 |
| [<span data-ttu-id="fe3a4-142">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-142">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="fe3a4-143">Restituisce il nome dell'evento di log per l'indice dell'evento di log specificato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-143">Returns the log event name for the specified log event index.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="fe3a4-144">**Getprotocolname**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-144">**GetProtocolName**</span></span>](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="fe3a4-145">Restituisce il nome del protocollo per l'indice di protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-145">Returns the protocol name for the specified protocol index.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="fe3a4-146">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-146">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="fe3a4-147">Indica se il tipo di registro eventi specificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-147">Indicates whether the specified event log type is enabled.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="fe3a4-148">**IsTransportEnabled**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-148">**IsTransportEnabled**</span></span>](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="fe3a4-149">Determina se il trasporto specificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-149">Determines whether the specified transport is enabled.</span></span><br/> <span data-ttu-id="fe3a4-150">**Windows server 2008 R2 e Windows server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-150">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                        |
| [<span data-ttu-id="fe3a4-151">**QueryCertContext**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-151">**QueryCertContext**</span></span>](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | <span data-ttu-id="fe3a4-152">Indica se il certificato specificato è installato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-152">Indicates whether the specified certificate is installed.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="fe3a4-153">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-153">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | <span data-ttu-id="fe3a4-154">Ricicla i pool di applicazioni RPC in IIS.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-154">Recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="fe3a4-155">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-155">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="fe3a4-156">**RefreshCertContext**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-156">**RefreshCertContext**</span></span>](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | <span data-ttu-id="fe3a4-157">Aggiorna il certificato utilizzato dal server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-157">Refreshes the certificate that is used by the RD Gateway server.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="fe3a4-158">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-158">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | <span data-ttu-id="fe3a4-159">Imposta il plug-in di autenticazione corrente per il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-159">Sets the current authentication plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="fe3a4-160">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-160">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="fe3a4-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span></span>](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | <span data-ttu-id="fe3a4-162">Imposta il plug-in di autenticazione corrente per il server Gateway Desktop remoto e ricicla i pool di applicazioni RPC in IIS.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-162">Sets the current authentication plug-in for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="fe3a4-163">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-163">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                      |
| [<span data-ttu-id="fe3a4-164">**SetAuthorizationPlugin**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-164">**SetAuthorizationPlugin**</span></span>](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | <span data-ttu-id="fe3a4-165">Imposta il plug-in di autorizzazione corrente per il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-165">Sets the current authorization plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="fe3a4-166">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-166">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                     |
| [<span data-ttu-id="fe3a4-167">**SetCertificate**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-167">**SetCertificate**</span></span>](setcertificate-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="fe3a4-168">Imposta l'hash del certificato per il binding HTTPS sulla porta 443 in IIS.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-168">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span><br/> <span data-ttu-id="fe3a4-169">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                       |
| [<span data-ttu-id="fe3a4-170">**SetCertificateACL**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-170">**SetCertificateACL**</span></span>](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="fe3a4-171">Imposta gli elenchi di controllo di accesso (ACL) del certificato per questo server.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-171">Sets the certificate access control lists (ACLs) for this server.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="fe3a4-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span></span>](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | <span data-ttu-id="fe3a4-173">Imposta i plug-in di autenticazione e autorizzazione correnti per il server Gateway Desktop remoto e ricicla i pool di applicazioni RPC in IIS.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-173">Sets the current authentication and authorization plug-ins for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="fe3a4-174">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-174">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                   |
| [<span data-ttu-id="fe3a4-175">**SetEnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-175">**SetEnforceChannelBinding**</span></span>](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="fe3a4-176">Imposta la proprietà **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="fe3a4-176">Sets the **EnforceChannelBinding** property.</span></span><br/> <span data-ttu-id="fe3a4-177">**Windows server 2008 R2 e Windows server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-177">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="fe3a4-178">**SetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-178">**SetIPAndPort**</span></span>](setipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="fe3a4-179">Imposta l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-179">Sets the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="fe3a4-180">**Windows server 2008 R2 e Windows server 2008:** Questo metodo non è disponibile prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-180">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                    |
| [<span data-ttu-id="fe3a4-181">**SetMaxConnections**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-181">**SetMaxConnections**</span></span>](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="fe3a4-182">Imposta il numero massimo di connessioni consentite tramite Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-182">Sets the maximum number of allowed connections through RD Gateway.</span></span> <span data-ttu-id="fe3a4-183">Questo metodo modifica le proprietà **MaxConnections** e **UnlimitedConnections** .</span><span class="sxs-lookup"><span data-stu-id="fe3a4-183">This method changes the **MaxConnections** and **UnlimitedConnections** properties.</span></span><br/>                                                                                                |
| [<span data-ttu-id="fe3a4-184">**SetSslBridging**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-184">**SetSslBridging**</span></span>](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="fe3a4-185">Imposta il tipo di bridging SSL che verrà utilizzato dal server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-185">Sets the type of SSL bridging to be used by the RD Gateway server.</span></span><br/> <span data-ttu-id="fe3a4-186">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-186">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="fe3a4-187">**TSGRemoveAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-187">**TSGRemoveAdminMsg**</span></span>](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="fe3a4-188">Rimuove il messaggio amministrativo per il server gateway.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-188">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="fe3a4-189">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-189">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="fe3a4-190">**TSGRemoveConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-190">**TSGRemoveConsentMsg**</span></span>](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | <span data-ttu-id="fe3a4-191">Rimuove il messaggio amministrativo per il server gateway.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-191">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="fe3a4-192">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-192">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="fe3a4-193">**TSGStoreAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-193">**TSGStoreAdminMsg**</span></span>](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="fe3a4-194">Aggiorna il messaggio amministrativo per il server gateway.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-194">Updates the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="fe3a4-195">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-195">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="fe3a4-196">**TSGStoreConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-196">**TSGStoreConsentMsg**</span></span>](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="fe3a4-197">Aggiorna il messaggio di consenso per il server gateway.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-197">Updates the consent message for the gateway server.</span></span><br/> <span data-ttu-id="fe3a4-198">**Windows Server 2008:** Questo metodo non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-198">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="fe3a4-199">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe3a4-199">Properties</span></span>

<span data-ttu-id="fe3a4-200">La classe **Win32 \_ TSGatewayServerSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-200">The **Win32\_TSGatewayServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe3a4-201">**adminMessageEndTime**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-201">**adminMessageEndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-204">Ora di fine del messaggio amministrativo.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-204">The administrative message end time.</span></span>

<span data-ttu-id="fe3a4-205">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-205">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-206">**adminMessageStartTime**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-206">**adminMessageStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-209">Ora di inizio del messaggio amministrativo.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-209">The administrative message start time.</span></span>

<span data-ttu-id="fe3a4-210">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-210">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-211">**adminMessageText**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-211">**adminMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-212">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-214">Testo del messaggio amministrativo.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-214">The administrative message text.</span></span>

<span data-ttu-id="fe3a4-215">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-215">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-216">**AuthenticationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-216">**AuthenticationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-219">CLSID del plug-in di autenticazione corrente.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-219">The CLSID of the current authentication plug-in.</span></span>

<span data-ttu-id="fe3a4-220">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-220">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-221">**AuthenticationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-221">**AuthenticationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-224">Descrizione del plug-in di autenticazione corrente.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-224">The description of the current authentication plug-in.</span></span>

<span data-ttu-id="fe3a4-225">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-225">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-226">**AuthenticationPluginName**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-226">**AuthenticationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-229">Nome del plug-in di autenticazione corrente.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-229">The name of the current authentication plug-in.</span></span>

<span data-ttu-id="fe3a4-230">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-230">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-231">**AuthorizationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-231">**AuthorizationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-234">CLSID del plug-in di autorizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-234">The CLSID of the current authorization plug-in.</span></span>

<span data-ttu-id="fe3a4-235">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-235">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-236">**AuthorizationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-236">**AuthorizationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-239">Descrizione del plug-in di autorizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-239">The description of the current authorization plug-in.</span></span>

<span data-ttu-id="fe3a4-240">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-240">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-241">**AuthorizationPluginName**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-241">**AuthorizationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-244">Nome del plug-in di autorizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-244">The name of the current authorization plug-in.</span></span>

<span data-ttu-id="fe3a4-245">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-245">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-246">**CentralCAPEnabled**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-246">**CentralCAPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-247">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-249">Specifica se per il controllo del server vengono utilizzati i server CAP centrali RD.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-249">Specifies whether central RD CAP servers are used for controlling this server.</span></span> <span data-ttu-id="fe3a4-250">Questa proprietà può essere modificata chiamando il metodo [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3a4-250">This property can be changed by calling the [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-251">**CertHash**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-251">**CertHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-252">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-252">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-254">Specifica l'hash del certificato per il binding HTTPS sulla porta 443 in IIS.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-254">Specifies the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

<span data-ttu-id="fe3a4-255">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-255">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-256">**consentMessageText**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-256">**consentMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-259">Testo del messaggio di consenso.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-259">The consent message text.</span></span>

<span data-ttu-id="fe3a4-260">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-260">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-261">**EnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-261">**EnforceChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-262">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-264">Indica se l'associazione di canale viene applicata per il trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-264">Indicates if channel binding is enforced for the HTTP transport.</span></span> <span data-ttu-id="fe3a4-265">Il valore di questa proprietà può essere modificato tramite il metodo [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3a4-265">This property value can be changed by using the [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) method.</span></span>

<span data-ttu-id="fe3a4-266">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è disponibile prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-266">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available before Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-267">**IsConfigured**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-267">**IsConfigured**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-268">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-270">Specifica se sono configurate le impostazioni RPC e IIS richieste dal servizio Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-270">Specifies if IIS and RPC settings required by the RD Gateway service are configured.</span></span>

<span data-ttu-id="fe3a4-271">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-271">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-272">**MaxConnections**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-272">**MaxConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-273">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-275">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe3a4-275">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-276">Restituisce il numero massimo di connessioni consentite tramite Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-276">Returns the maximum number of connections that are allowed through RD Gateway.</span></span> <span data-ttu-id="fe3a4-277">Questa proprietà può essere impostata tramite il metodo [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3a4-277">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-278">**MaximumAllowedConnectionsBySku**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-278">**MaximumAllowedConnectionsBySku**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-279">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-281">Numero massimo di connessioni consentite dall'unità di mantenimento delle scorte (SKU).</span><span class="sxs-lookup"><span data-stu-id="fe3a4-281">Maximum number of connections that the stock-keeping unit (SKU) allows.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-282">**MaxLogEvents**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-282">**MaxLogEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-283">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-285">Restituisce il numero massimo di eventi di log.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-285">Returns the maximum number of log events.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-286">**MaxProtocols**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-286">**MaxProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-287">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-289">Numero di protocolli supportati da Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-289">Number of protocols supported by RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-290">**OnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-290">**OnlyConsentCapableClients**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-291">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-293">Specifica se solo i client che supportano i messaggi di consenso sono autorizzati a connettersi al Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-293">Specifies if only clients capable of consent messages are allowed to connect to the RD Gateway.</span></span>

<span data-ttu-id="fe3a4-294">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-294">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="fe3a4-295">diverso da zero</span><span class="sxs-lookup"><span data-stu-id="fe3a4-295">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="fe3a4-296">Solo i client abilitati per i messaggi di consenso possono connettersi.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-296">Only consent message capable clients can connect.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-297">zero</span><span class="sxs-lookup"><span data-stu-id="fe3a4-297">zero</span></span>
</dt> <dd>

<span data-ttu-id="fe3a4-298">Anche i client che non supportano messaggi di consenso possono connettersi.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-298">Clients that are not consent message capable can also connect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fe3a4-299">**RequestSOH**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-299">**RequestSOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-300">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-302">Questa proprietà non è supportata a partire da Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-302">This property is not supported starting with Windows Server 2016.</span></span>

<span data-ttu-id="fe3a4-303">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="fe3a4-303">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="fe3a4-304">Specifica se il server deve richiedere un rapporto di integrità (SoH) dal client.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-304">Specifies whether the server must request a Statement of Health (SoH) from the client.</span></span> <span data-ttu-id="fe3a4-305">Questa proprietà può essere modificata tramite il metodo [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3a4-305">This property can be changed by using the [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-306">**SkuName**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-306">**SkuName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-309">Nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-309">Name of the SKU.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-310">**SslBridging**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-310">**SslBridging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-311">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-313">Specifica il tipo di bridging SSL che verrà utilizzato dal server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-313">Specifies which type of SSL bridging to be used by the RD Gateway server.</span></span> <span data-ttu-id="fe3a4-314">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-314">This can be one of the following values.</span></span>

<span data-ttu-id="fe3a4-315">**Windows Server 2008:** Questa proprietà non è disponibile prima di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-315">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="fe3a4-316">0</span><span class="sxs-lookup"><span data-stu-id="fe3a4-316">0</span></span>
</dt> <dd>

<span data-ttu-id="fe3a4-317">Nessun bridging SSL.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-317">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-318">1</span><span class="sxs-lookup"><span data-stu-id="fe3a4-318">1</span></span>
</dt> <dd>

<span data-ttu-id="fe3a4-319">Bridging da HTTPS a HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-319">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="fe3a4-320">2</span><span class="sxs-lookup"><span data-stu-id="fe3a4-320">2</span></span>
</dt> <dd>

<span data-ttu-id="fe3a4-321">Bridging da HTTPS a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-321">HTTPS to HTTPS bridging.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fe3a4-322">**UnlimitedConnections**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-322">**UnlimitedConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe3a4-323">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe3a4-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe3a4-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe3a4-325">Indica se è consentito un numero illimitato di connessioni tramite Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-325">Indicates whether an unlimited number of connections are allowed through RD Gateway.</span></span> <span data-ttu-id="fe3a4-326">Questa proprietà può essere impostata tramite il metodo [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3a4-326">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe3a4-327">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe3a4-327">Remarks</span></span>

<span data-ttu-id="fe3a4-328">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-328">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="fe3a4-329">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fe3a4-329">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fe3a4-330">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fe3a4-330">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fe3a4-331">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="fe3a4-331">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fe3a4-332">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fe3a4-332">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3a4-333">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe3a4-333">Requirements</span></span>



| <span data-ttu-id="fe3a4-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe3a4-334">Requirement</span></span> | <span data-ttu-id="fe3a4-335">Valore</span><span class="sxs-lookup"><span data-stu-id="fe3a4-335">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3a4-336">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe3a4-336">Minimum supported client</span></span><br/> | <span data-ttu-id="fe3a4-337">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fe3a4-337">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fe3a4-338">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe3a4-338">Minimum supported server</span></span><br/> | <span data-ttu-id="fe3a4-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe3a4-339">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fe3a4-340">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe3a4-340">Namespace</span></span><br/>                | <span data-ttu-id="fe3a4-341">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fe3a4-341">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fe3a4-342">MOF</span><span class="sxs-lookup"><span data-stu-id="fe3a4-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe3a4-343"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe3a4-343"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe3a4-344">DLL</span><span class="sxs-lookup"><span data-stu-id="fe3a4-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe3a4-345"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe3a4-345"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fe3a4-346">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe3a4-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3a4-347">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-347">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="fe3a4-348">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-348">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="fe3a4-349">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-349">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="fe3a4-350">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-350">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="fe3a4-351">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-351">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="fe3a4-352">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="fe3a4-352">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

