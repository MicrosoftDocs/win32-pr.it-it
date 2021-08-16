---
title: Costanti della sequenza di protocollo
description: Rpc Microsoft supporta le sequenze di protocollo seguenti.
ms.assetid: 51284532-b0ac-4bf2-b322-91393b2b9dc6
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
- ncacn_nb_ipx
- ncacn_nb_nb
- ncacn_ip_tcp
- ncacn_np
- ncacn_spx
- ncacn_dnet_nsp
- ncacn_at_dsp
- ncacn_vns_spp
- ncadg_ip_udp
- ncadg_ipx
- ncadg_mq
- ncacn_http
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72c28486bfa3981870ac331ae83f0cbb532bba4d27c44062ce902823e4e3c259
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927135"
---
# <a name="protocol-sequence-constants"></a>Costanti della sequenza di protocollo

Rpc Microsoft supporta le sequenze di protocollo seguenti.



| Costante/valore                                                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>**ncacn \_ nb \_ tcp**</dt> NetBIOS orientato alla connessione <dt>su Transmission Control Protocol (TCP)</dt> </dl>          | Solo client: MS-DOS, Windows 3. *x* Client e Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ nb \_ ipx**</dt> NetBIOS orientato alla connessione <dt>su Internet Packet Exchange (IPX)</dt> </dl>               | Solo client: MS-DOS, Windows 3. *x* Client e Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>**ncacn \_ nb \_ nb**</dt> <dt>Connection-oriented NetBIOS Enhanced Interfaccia utente (NetBEUI)</dt> </dl>                    | Solo client: MS-DOS, Windows 3. *x* Client e Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> <dt>**ncacn \_ ip \_ tcp**</dt> <dt>Connection-oriented Transmission Control Protocol/Internet Protocol (TCP/IP)</dt> </dl>  | Solo client: MS-DOS, Windows 3. *x* e Apple Macintosh Client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>**ncacn \_ np**</dt> <dt>Named pipe orientate alla connessione</dt> </dl>                                                            | Solo client: MS-DOS, Windows 3. *x*, Windows 95 Client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**ncacn \_ spx**</dt> <dt>Connection-oriented Sequenced Packet Exchange (SPX)</dt> </dl>                                     | Solo client: MS-DOS, Windows 3. *x* Client e Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_ nsp**</dt> <dt>Trasporto DECnet orientato alla connessione</dt> </dl>                                    | Solo client: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ at \_ dsp**</dt> <dt>Connection-oriented AppleTalk DSP</dt> </dl>                                             | Client: Apple Macintosh Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> <dt>**Trasporto ncacn \_ vns \_ spp**</dt> <dt>Vines scalable parallel processing (SPP)</dt> orientato alla connessione </dl>     | Solo client: MS-DOS, Windows 3. *x* Client e Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**ncadg \_ ip \_ udp**</dt> <dt>Datagram (senza connessione) User Datagram Protocol/Internet Protocol (UDP/IP)</dt> </dl>   | Solo client: MS-DOS, Windows 3. *x* Client e Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_ ipx**</dt> <dt>Datagram (senza connessione) IPX</dt> </dl>                                                           | Solo client: MS-DOS, Windows 3. *x* Client e Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**ncadg \_ mq**</dt> <dt>Datagram (senza connessione) sul server Microsoft Message Queue (MSMQ)</dt> </dl>                   | Solo client: Windows Me/98/95 Client e Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4.0 con SP3 e versioni successive<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**ncacn \_ http**</dt> <dt>TCP/IP orientato alla connessione con Microsoft Internet Information Server come proxy HTTP</dt> </dl> | Solo client: Windows Me/98/95 Client and Server: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt>**ncalrpc**</dt> <dt>Local procedure call</dt> </dl>                                                                           | Client e server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Commenti

Il [**trasporto ncalrpc**](/windows/desktop/Midl/ncalrpc) supporta solo l'autenticazione \_ WINNT RPC C \_ \_ AUTHN. Per altre informazioni, vedere [Costanti security](security.md) e [authentication-service.](authentication-service-constants.md)

Microsoft RPC supporta [**RpcBindingCopy solo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) nelle applicazioni client, non nelle applicazioni server.

 

