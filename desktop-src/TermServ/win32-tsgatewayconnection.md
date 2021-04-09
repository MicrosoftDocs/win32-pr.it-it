---
title: Classe Win32_TSGatewayConnection
description: Rappresenta una connessione da un computer client a un server Gateway Desktop remoto di Desktop remoto.
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayConnection Servizi Desktop remoto
- Classe Win32_TSGatewayConnection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121206"
---
# <a name="win32_tsgatewayconnection-class"></a><span data-ttu-id="1d0c6-105">Win32 \_ TSGatewayConnection (classe)</span><span class="sxs-lookup"><span data-stu-id="1d0c6-105">Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="1d0c6-106">Rappresenta una connessione da un computer client a un server Gateway Desktop remoto di Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-106">Represents a connection from a client computer to a Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0c6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d0c6-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="1d0c6-108">Members</span><span class="sxs-lookup"><span data-stu-id="1d0c6-108">Members</span></span>

<span data-ttu-id="1d0c6-109">La classe **Win32 \_ TSGatewayConnection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1d0c6-109">The **Win32\_TSGatewayConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="1d0c6-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="1d0c6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d0c6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d0c6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d0c6-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="1d0c6-112">Methods</span></span>

<span data-ttu-id="1d0c6-113">La classe **Win32 \_ TSGatewayConnection** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-113">The **Win32\_TSGatewayConnection** class has these methods.</span></span>



| <span data-ttu-id="1d0c6-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="1d0c6-114">Method</span></span>                                                                     | <span data-ttu-id="1d0c6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d0c6-115">Description</span></span>                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d0c6-116">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-116">**CheckStatus**</span></span>](checkstatus-win32-tsgatewayconnection.md)               | <span data-ttu-id="1d0c6-117">Controlla lo stato di una connessione al server Gateway Desktop remoto e indica se il server di destinazione è configurato per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-117">Checks the status of an RD Gateway server connection, and whether the target server is configured for load balancing.</span></span><br/> |
| [<span data-ttu-id="1d0c6-118">**Disconnetti**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-118">**Disconnect**</span></span>](disconnect-win32-tsgatewayconnection.md)                 | <span data-ttu-id="1d0c6-119">Termina la connessione.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-119">Ends the connection.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="1d0c6-120">**DisconnectProtocol**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-120">**DisconnectProtocol**</span></span>](disconnectprotocol-win32-tsgatewayconnection.md) | <span data-ttu-id="1d0c6-121">Termina tutte le connessioni che utilizzano il protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-121">Ends all connections that use the specified protocol.</span></span><br/>                                                                 |
| [<span data-ttu-id="1d0c6-122">**DisconnectUser**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-122">**DisconnectUser**</span></span>](disconnectuser-win32-tsgatewayconnection.md)         | <span data-ttu-id="1d0c6-123">Termina tutte le connessioni dell'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-123">Ends all connections of the specified user.</span></span><br/>                                                                           |



 

### <a name="properties"></a><span data-ttu-id="1d0c6-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d0c6-124">Properties</span></span>

<span data-ttu-id="1d0c6-125">La classe **Win32 \_ TSGatewayConnection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-125">The **Win32\_TSGatewayConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d0c6-126">**ChannelId**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-126">**ChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-127">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-129">Identificatore del canale.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-129">Channel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-130">**ClientAddress**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-130">**ClientAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-133">Indirizzo IP del client.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-133">Client IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-134">**ConnectedPort**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-134">**ConnectedPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-137">Porta sulla risorsa connessa a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-137">Port on the connected resource to which the user is connected.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-138">**ConnectedResource**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-138">**ConnectedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-141">Nome del computer (o cluster) a cui è connesso il client.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-141">Name of the computer (or cluster) to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-142">**ConnectedTime**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-142">**ConnectedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-145">Timestamp relativo al momento in cui è stata stabilita la connessione.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-145">The time stamp for when the connection was established.</span></span> <span data-ttu-id="1d0c6-146">Questa volta viene reimpostato quando la connessione viene reimpostata, anche se viene riconnessa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-146">This time is reset when the connection is reset, even if it is automatically reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-147">**ConnectionDuration**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-147">**ConnectionDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-150">Tempo trascorso dall'ora di connessione.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-150">The time that has elapsed since the connected time.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-151">**ConnectionKey**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-151">**ConnectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-154">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d0c6-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-155">Identificatore di connessione nel formato "tunnelId: channelID".</span><span class="sxs-lookup"><span data-stu-id="1d0c6-155">Connection identifier in the format "tunnelId:channelID".</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-156">**FullUserName**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-156">**FullUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-159">Nome utente completo dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-159">Full user name of the connected user.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-160">**Tempoinattività**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-160">**IdleTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-163">Tempo di inattività della connessione.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-163">Idle time of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-164">**NumberOfKilobytesReceived**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-164">**NumberOfKilobytesReceived**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-165">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-167">Numero di kilobyte ricevuti dal computer client dal server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-167">Number of kilobytes received from the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-168">**NumberOfKilobytesSent**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-168">**NumberOfKilobytesSent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-169">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-171">Numero di kilobyte inviati al computer client dal server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-171">Number of kilobytes sent to the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-172">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-172">**ProtocolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-175">Protocollo utilizzato per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-175">Protocol that is used to connect to the RD Gateway server.</span></span>

<dt>

<span data-ttu-id="1d0c6-176">RDP</span><span class="sxs-lookup"><span data-stu-id="1d0c6-176">"RDP"</span></span>
</dt> <dd>

<span data-ttu-id="1d0c6-177">Protocollo per il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-177">The protocol for the RD Gateway server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d0c6-178">**TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-178">**TransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-179">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-181">Specifica il tipo di trasporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-181">Specifies the transport type for the connection.</span></span> <span data-ttu-id="1d0c6-182">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-182">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="1d0c6-183">0</span><span class="sxs-lookup"><span data-stu-id="1d0c6-183">0</span></span>
</dt> <dd>

<span data-ttu-id="1d0c6-184">RPC sul trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-184">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-185">1</span><span class="sxs-lookup"><span data-stu-id="1d0c6-185">1</span></span>
</dt> <dd>

<span data-ttu-id="1d0c6-186">Trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-186">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-187">2</span><span class="sxs-lookup"><span data-stu-id="1d0c6-187">2</span></span>
</dt> <dd>

<span data-ttu-id="1d0c6-188">Trasporto UDP.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-188">UDP transport.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d0c6-189">**TunnelId**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-189">**TunnelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-190">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-192">Identificatore del tunnel.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-192">Tunnel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1d0c6-193">**UserName**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-193">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d0c6-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d0c6-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d0c6-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d0c6-196">Nome utente connesso al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-196">User name connected to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d0c6-197">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d0c6-197">Remarks</span></span>

<span data-ttu-id="1d0c6-198">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-198">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="1d0c6-199">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1d0c6-199">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1d0c6-200">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1d0c6-200">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1d0c6-201">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1d0c6-201">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1d0c6-202">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1d0c6-202">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0c6-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d0c6-203">Requirements</span></span>



| <span data-ttu-id="1d0c6-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d0c6-204">Requirement</span></span> | <span data-ttu-id="1d0c6-205">Valore</span><span class="sxs-lookup"><span data-stu-id="1d0c6-205">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0c6-206">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d0c6-206">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0c6-207">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1d0c6-207">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1d0c6-208">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d0c6-208">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0c6-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d0c6-209">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1d0c6-210">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d0c6-210">Namespace</span></span><br/>                | <span data-ttu-id="1d0c6-211">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1d0c6-211">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1d0c6-212">MOF</span><span class="sxs-lookup"><span data-stu-id="1d0c6-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d0c6-213"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d0c6-213"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d0c6-214">DLL</span><span class="sxs-lookup"><span data-stu-id="1d0c6-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d0c6-215"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d0c6-215"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1d0c6-216">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d0c6-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0c6-217">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-217">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="1d0c6-218">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-218">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="1d0c6-219">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-219">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="1d0c6-220">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-220">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="1d0c6-221">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-221">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="1d0c6-222">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="1d0c6-222">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

