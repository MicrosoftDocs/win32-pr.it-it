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
# <a name="authentication-level"></a>Livello di autenticazione

Il livello di autenticazione controlla la quantità di sicurezza che un client o un server vuole dal proprio SSP. Il livello di autenticazione viene impostato passando un valore xxx del livello di autenticazione RPC \_ C appropriato \_ \_ \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) tramite il parametro *dwAuthnLevel* . I livelli di autenticazione del client e del server vengono confrontati durante l'handshake e per la connessione viene utilizzata l'impostazione di protezione di livello superiore.

I diversi livelli di autenticazione sono descritti di seguito, dalla protezione della sicurezza di livello più basso al più alto:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Nessuno (nessun \_ \_ livello auth C \_ RPC \_ )
</dt> <dd>

Non viene eseguita alcuna autenticazione durante la comunicazione tra client e server. Tutte le impostazioni di sicurezza vengono ignorate. Questo livello di autenticazione può essere impostato solo se il [livello del servizio di autenticazione](com-authentication-service-constants.md) è RPC \_ C \_ AuthN \_ None.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Predefinito ( \_ valore predefinito per il \_ livello auth C RPC \_ \_ )
</dt> <dd>

COM sceglie il livello di autenticazione utilizzando la normale negoziazione della copertura di sicurezza. Non verrà mai scelto un livello di autenticazione None.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connetti ( \_ connessione a \_ livello auth C RPC \_ \_ )
</dt> <dd>

Viene eseguito il normale handshake di autenticazione tra il client e il server e viene stabilita una chiave di sessione, ma tale chiave non viene mai utilizzata per la comunicazione tra il client e il server. Tutte le comunicazioni dopo l'handshake non sono sicure.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call ( \_ chiamata al \_ livello auth C RPC \_ \_ )
</dt> <dd>

Vengono firmate solo le intestazioni dell'inizio di ogni chiamata. Il resto dei dati scambiati tra il client e il server non è né firmato né crittografato. La maggior parte dei provider di servizi condivisi non supporta questo livello di autenticazione e lo innalza automaticamente al pacchetto.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Pacchetto ( \_ PKT a \_ livello auth C RPC \_ \_ )
</dt> <dd>

L'intestazione di ogni pacchetto è firmata, ma non crittografata. I pacchetti stessi non sono firmati o crittografati.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integrità dei pacchetti ( \_ \_ integrità PKT del livello auth C RPC \_ \_ \_ )
</dt> <dd>

Ogni pacchetto di dati è firmato integralmente, ma non è crittografato. Poiché tutti i dati sono firmati dal mittente, il destinatario può essere certo che nessuno dei dati è stato alterato durante il transito.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacy del pacchetto ( \_ \_ Pkt Privacy del livello di autenticazione RPC C \_ \_ \_ )
</dt> <dd>

Ogni pacchetto di dati è firmato e crittografato. Ciò consente di proteggere l'intera comunicazione tra il client e il server.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[AuthenticationLevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




