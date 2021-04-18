---
description: Pagina di navigazione per le opzioni del socket Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Opzioni socket
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306897"
---
# <a name="socket-options"></a>Opzioni socket

In questa sezione vengono descritte le opzioni del socket Winsock per varie edizioni dei sistemi operativi Windows. Per ottenere e impostare le opzioni del socket, usare le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) . Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, utilizzare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

Alcune opzioni del socket richiedono una spiegazione più che queste tabelle possono comportare; tali opzioni contengono collegamenti ad altre pagine.

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**\_IP IPPROTO**
</dt> <dd> <dl> <dt>



Opzioni del socket applicabili a livello di IPv4. Per altre informazioni, vedere le [**\_ Opzioni del socket IP di IPPROTO**](ipproto-ip-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**\_IPv6 IPPROTO**
</dt> <dd> <dl> <dt>



Opzioni del socket applicabili a livello di IPv6. Per ulteriori informazioni, vedere le [**\_ Opzioni del socket IPv6 di IPPROTO**](ipproto-ipv6-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**
</dt> <dd> <dl> <dt>



Opzioni del socket applicabili a livello di multicast affidabile. Per ulteriori informazioni, vedere le [**\_ Opzioni del socket IPPROTO RM**](ipproto-rm-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**\_TCP IPPROTO**
</dt> <dd> <dl> <dt>



Opzioni socket applicabili a livello TCP. Per ulteriori informazioni, vedere le [**\_ Opzioni del socket TCP IPPROTO**](ipproto-tcp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**\_UDP IPPROTO**
</dt> <dd> <dl> <dt>



Opzioni del socket applicabili a livello di UDP. Per ulteriori informazioni, vedere le [**\_ Opzioni del socket UDP di IPPROTO**](ipproto-udp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**
</dt> <dd> <dl> <dt>



Opzioni del socket applicabili a livello di IPX. Per ulteriori informazioni, vedere le [**\_ Opzioni del socket IPX di NSPROTO**](nsproto-ipx-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOLENOIDE \_ AppleTalk**
</dt> <dd> <dl> <dt>



Opzioni del socket applicabili a livello di AppleTalk. Per ulteriori informazioni, vedere le [**\_ Opzioni del socket**](sol-appletalk-socket-options.md)per la tecnologia solenoide.


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**
</dt> <dd> <dl> <dt>



Opzioni del socket applicabili al livello del protocollo di gestione dei collegamenti a infrarossi. Per altre informazioni, vedere le [**\_ Opzioni del socket Sol IRLMP**](sol-irlmp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**\_socket Sol**
</dt> <dd> <dl> <dt>



Opzioni socket applicabili a livello di socket. Per ulteriori informazioni, vedere le [**\_ Opzioni del socket di socket Sol**](sol-socket-socket-options.md).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Tutte le \_ \* Opzioni del socket sono valide anche per IPv4 e IPv6 (ad eccezione di \_ broadcast, perché broadcast non è implementato in IPv6).

 

 



