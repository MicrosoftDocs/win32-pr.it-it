---
title: Livello di autenticazione
description: Il livello di autenticazione controlla la sicurezza richiesta da un client o un server al provider di servizi condivisi.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c468408a22f1ea0c0fae67d7ce3d5f5b40f8a6342538614c1619acd40574ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311151"
---
# <a name="authentication-level"></a>Livello di autenticazione

Il livello di autenticazione controlla la sicurezza richiesta da un client o un server al provider di servizi condivisi. Il livello di autenticazione viene impostato passando un valore RPC C AUTHN LEVEL xxx appropriato a \_ \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) tramite il *parametro dwAuthnLevel.* I livelli di autenticazione del client e del server vengono confrontati durante l'handshake e per la connessione viene usata l'impostazione di protezione di livello superiore.

I diversi livelli di autenticazione sono descritti di seguito, dalla protezione di livello più basso a quella più elevata:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Nessuno (RPC \_ C \_ AUTHN \_ LEVEL \_ NONE)
</dt> <dd>

Durante la comunicazione tra client e server non viene eseguita alcuna autenticazione. Tutte le impostazioni di sicurezza vengono ignorate. Questo livello di autenticazione può essere impostato solo se il livello [di servizio di autenticazione](com-authentication-service-constants.md) è RPC C \_ \_ AUTHN \_ NONE.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Impostazione predefinita (RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT)
</dt> <dd>

COM sceglie il livello di autenticazione usando la normale negoziazione basata sulla sicurezza. Non sceglierà mai il livello di autenticazione Nessuno.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connessione (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT)
</dt> <dd>

L'handshake di autenticazione normale si verifica tra il client e il server e viene stabilita una chiave di sessione, ma tale chiave non viene mai usata per la comunicazione tra il client e il server. Tutte le comunicazioni dopo l'handshake non sono sicure.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC \_ C \_ AUTHN \_ LEVEL \_ CALL)
</dt> <dd>

Solo le intestazioni dell'inizio di ogni chiamata sono firmate. Il resto dei dati s scambiati tra il client e il server non è firmato né crittografato. La maggior parte dei provider di servizi di sicurezza non supporta questo livello di autenticazione e lo alza automaticamente di livello a Pacchetto.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Packet (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT)
</dt> <dd>

L'intestazione di ogni pacchetto è firmata ma non crittografata. I pacchetti stessi non sono firmati o crittografati.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integrità dei pacchetti \_ (RPC C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY)
</dt> <dd>

Ogni pacchetto di dati viene firmato per intero, ma non crittografato. Poiché tutti i dati sono firmati dal mittente, il destinatario può essere certo che nessuno dei dati sia stato manomesso durante il transito.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacy dei pacchetti (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY)
</dt> <dd>

Ogni pacchetto di dati è firmato e crittografato. Ciò consente di proteggere l'intera comunicazione tra il client e il server.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[AuthenticationLevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




