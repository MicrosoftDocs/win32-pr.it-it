---
title: Costanti della sequenza di protocollo
description: Microsoft RPC supporta le sequenze di protocollo seguenti.
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
ms.openlocfilehash: 7e2dd716cdd969040f5315ef05200912acc54878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047190"
---
# <a name="protocol-sequence-constants"></a>Costanti della sequenza di protocollo

Microsoft RPC supporta le sequenze di protocollo seguenti.



| Costante/valore                                                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>**ncacn \_ NB \_**</dt> <dt>-NetBIOS orientato alla connessione TCP su Transmission Control Protocol (TCP)</dt> </dl>          | Solo client: MS-DOS, Windows 3. *x* client e server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ NB \_**</dt> <dt>: NetBIOS basato sulla connessione IPX su Internet Packet Exchange (IPX)</dt> </dl>               | Solo client: MS-DOS, Windows 3. *x* client e server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>**ncacn \_ NB \_ NB**</dt> <dt>: interfaccia utente avanzata NetBIOS (NetBEUI)</dt> basata sulla connessione </dl>                    | Solo client: MS-DOS, Windows 3. *x* client e server: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> <dt>protocollo TCP/IP orientato alla connessione Transmission Control Protocol</dt> <dt>**\_ IP \_ di ncacn**</dt> </dl>  | Solo client: MS-DOS, Windows 3. *x* e client e server Apple Macintosh: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>pipe denominate orientate alla connessione</dt> <dt>**\_ NP ncacn**</dt> </dl>                                                            | Solo client: MS-DOS, Windows 3. *x*, client e Server Windows 95: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**ncacn \_ SPX**</dt> <dt>(Connection-oriented Sequenced Packet Exchange)</dt> </dl>                                     | Solo client: MS-DOS, Windows 3. *x* client e server: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>trasporto DECnet orientato alla connessione</dt> <dt>**ncacn \_ DNET \_ NSP**</dt> </dl>                                    | Solo client: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ in \_ DSP per la**</dt> <dt>connessione</dt> DSP </dl>                                             | Client: server Apple Macintosh: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> <dt>**ncacn \_ le reti virtuali \_ spp**</dt> <dt>-trasporto di elaborazione parallela scalabile (SPP)</dt> </dl>     | Solo client: MS-DOS, Windows 3. *x* client e server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**ncadg \_ IP \_ UDP**</dt> datagramma <dt>(senza connessione) User Datagram Protocol/Internet Protocol (UDP/IP)</dt> </dl>   | Solo client: MS-DOS, Windows 3. *x* client e server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_**</dt> <dt>datagramma IPX (senza connessione) IPX</dt> </dl>                                                           | Solo client: MS-DOS, Windows 3. *x* client e server: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> datagramma <dt>**ncadg \_ mq**</dt> <dt>(senza connessione) tramite il server di Accodamento messaggi Microsoft (MSMQ)</dt> </dl>                   | Solo client: client e server Windows Me/98/95: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4,0 con SP3 e versioni successive<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>TCP/IP orientato alla connessione HTTP di ncacn con Microsoft Internet Information Server come proxy http</dt> <dt>**\_**</dt> </dl> | Solo client: client e server Windows Me/98/95: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt></dt> <dt>chiamata di procedura locale</dt> ncalrpc </dl>                                                                           | Client e server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Commenti

Il trasporto [**ncalrpc**](/windows/desktop/Midl/ncalrpc) supporta \_ \_ \_ solo l'autenticazione WinNT C AuthN. Per altre informazioni, vedere [sicurezza](security.md) e [autenticazione-costanti del servizio](authentication-service-constants.md).

Microsoft RPC supporta [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) solo nelle applicazioni client, non nelle applicazioni server.

 

