---
title: Livello di autenticazione
description: Il livello di autenticazione controlla la quantità di sicurezza che un client o un server vuole dal proprio SSP.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332639"
---
# <a name="authentication-level"></a><span data-ttu-id="4dadd-103">Livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="4dadd-103">Authentication Level</span></span>

<span data-ttu-id="4dadd-104">Il livello di autenticazione controlla la quantità di sicurezza che un client o un server vuole dal proprio SSP.</span><span class="sxs-lookup"><span data-stu-id="4dadd-104">The authentication level controls how much security a client or server wants from its SSP.</span></span> <span data-ttu-id="4dadd-105">Il livello di autenticazione viene impostato passando un valore xxx del livello di autenticazione RPC \_ C appropriato \_ \_ \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) tramite il parametro *dwAuthnLevel* .</span><span class="sxs-lookup"><span data-stu-id="4dadd-105">The authentication level is set by passing an appropriate RPC\_C\_AUTHN\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwAuthnLevel* parameter.</span></span> <span data-ttu-id="4dadd-106">I livelli di autenticazione del client e del server vengono confrontati durante l'handshake e per la connessione viene utilizzata l'impostazione di protezione di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="4dadd-106">The authentication levels from the client and server are compared during the handshake, and the higher level security protection setting is used for the connection.</span></span>

<span data-ttu-id="4dadd-107">I diversi livelli di autenticazione sono descritti di seguito, dalla protezione della sicurezza di livello più basso al più alto:</span><span class="sxs-lookup"><span data-stu-id="4dadd-107">The different authentication levels are described as follows, from lowest level security protection to highest:</span></span>

<dl> <dt>

<span data-ttu-id="4dadd-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Nessuno (nessun \_ \_ livello auth C \_ RPC \_ )</span><span class="sxs-lookup"><span data-stu-id="4dadd-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC\_C\_AUTHN\_LEVEL\_NONE)</span></span>
</dt> <dd>

<span data-ttu-id="4dadd-109">Non viene eseguita alcuna autenticazione durante la comunicazione tra client e server.</span><span class="sxs-lookup"><span data-stu-id="4dadd-109">No authentication is performed during the communication between client and server.</span></span> <span data-ttu-id="4dadd-110">Tutte le impostazioni di sicurezza vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="4dadd-110">All security settings are ignored.</span></span> <span data-ttu-id="4dadd-111">Questo livello di autenticazione può essere impostato solo se il [livello del servizio di autenticazione](com-authentication-service-constants.md) è RPC \_ C \_ AuthN \_ None.</span><span class="sxs-lookup"><span data-stu-id="4dadd-111">This authentication level can be set only if the [authentication service level](com-authentication-service-constants.md) is RPC\_C\_AUTHN\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="4dadd-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Predefinito ( \_ valore predefinito per il \_ livello auth C RPC \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4dadd-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC\_C\_AUTHN\_LEVEL\_DEFAULT)</span></span>
</dt> <dd>

<span data-ttu-id="4dadd-113">COM sceglie il livello di autenticazione utilizzando la normale negoziazione della copertura di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4dadd-113">COM chooses the authentication level by using its normal security blanket negotiation.</span></span> <span data-ttu-id="4dadd-114">Non verrà mai scelto un livello di autenticazione None.</span><span class="sxs-lookup"><span data-stu-id="4dadd-114">It will never choose an authentication level of None.</span></span>

</dd> <dt>

<span data-ttu-id="4dadd-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connetti ( \_ connessione a \_ livello auth C RPC \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4dadd-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC\_C\_AUTHN\_LEVEL\_CONNECT)</span></span>
</dt> <dd>

<span data-ttu-id="4dadd-116">Viene eseguito il normale handshake di autenticazione tra il client e il server e viene stabilita una chiave di sessione, ma tale chiave non viene mai utilizzata per la comunicazione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="4dadd-116">The normal authentication handshake occurs between the client and server, and a session key is established but that key is never used for communication between the client and server.</span></span> <span data-ttu-id="4dadd-117">Tutte le comunicazioni dopo l'handshake non sono sicure.</span><span class="sxs-lookup"><span data-stu-id="4dadd-117">All communication after the handshake is nonsecure.</span></span>

</dd> <dt>

<span data-ttu-id="4dadd-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call ( \_ chiamata al \_ livello auth C RPC \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4dadd-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC\_C\_AUTHN\_LEVEL\_CALL)</span></span>
</dt> <dd>

<span data-ttu-id="4dadd-119">Vengono firmate solo le intestazioni dell'inizio di ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="4dadd-119">Only the headers of the beginning of each call are signed.</span></span> <span data-ttu-id="4dadd-120">Il resto dei dati scambiati tra il client e il server non è né firmato né crittografato.</span><span class="sxs-lookup"><span data-stu-id="4dadd-120">The rest of the data exchanged between the client and server is neither signed nor encrypted.</span></span> <span data-ttu-id="4dadd-121">La maggior parte dei provider di servizi condivisi non supporta questo livello di autenticazione e lo innalza automaticamente al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4dadd-121">Most SSPs do not support this authentication level and silently promote it to Packet.</span></span>

</dd> <dt>

<span data-ttu-id="4dadd-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Pacchetto ( \_ PKT a \_ livello auth C RPC \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4dadd-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Packet (RPC\_C\_AUTHN\_LEVEL\_PKT)</span></span>
</dt> <dd>

<span data-ttu-id="4dadd-123">L'intestazione di ogni pacchetto è firmata, ma non crittografata.</span><span class="sxs-lookup"><span data-stu-id="4dadd-123">The header of each packet is signed but not encrypted.</span></span> <span data-ttu-id="4dadd-124">I pacchetti stessi non sono firmati o crittografati.</span><span class="sxs-lookup"><span data-stu-id="4dadd-124">The packets themselves are not signed or encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="4dadd-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integrità dei pacchetti ( \_ \_ integrità PKT del livello auth C RPC \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4dadd-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Packet Integrity (RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY)</span></span>
</dt> <dd>

<span data-ttu-id="4dadd-126">Ogni pacchetto di dati è firmato integralmente, ma non è crittografato.</span><span class="sxs-lookup"><span data-stu-id="4dadd-126">Each packet of data is signed in its entirety but is not encrypted.</span></span> <span data-ttu-id="4dadd-127">Poiché tutti i dati sono firmati dal mittente, il destinatario può essere certo che nessuno dei dati è stato alterato durante il transito.</span><span class="sxs-lookup"><span data-stu-id="4dadd-127">Because all of the data is signed by the sender, the recipient can be certain that none of the data has been tampered with during transit.</span></span>

</dd> <dt>

<span data-ttu-id="4dadd-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacy del pacchetto ( \_ \_ Pkt Privacy del livello di autenticazione RPC C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="4dadd-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Packet Privacy (RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY)</span></span>
</dt> <dd>

<span data-ttu-id="4dadd-129">Ogni pacchetto di dati è firmato e crittografato.</span><span class="sxs-lookup"><span data-stu-id="4dadd-129">Each data packet is signed and encrypted.</span></span> <span data-ttu-id="4dadd-130">Ciò consente di proteggere l'intera comunicazione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="4dadd-130">This helps protect the entire communication between the client and server.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="4dadd-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4dadd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dadd-132">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="4dadd-132">AuthenticationLevel</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="4dadd-133">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="4dadd-133">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
</dt> </dl>

 

 




