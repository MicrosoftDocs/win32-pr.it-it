---
description: Windows Sockets 2 non presuppone che l'ordine dei byte di rete per tutti i protocolli sia lo stesso.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Routine di conversione Byte-Order estese
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526184"
---
# <a name="extended-byte-order-conversion-routines"></a>Routine di conversione Byte-Order estese

Windows Sockets 2 non presuppone che l'ordine dei byte di rete per tutti i protocolli sia lo stesso. Viene fornito un set di routine di conversione per la conversione di quantità a 16 bit e a 32 bit da e verso l'ordine dei byte di rete. Queste routine accettano come parametro di input l'handle del socket a cui è associata una struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Il membro **NetworkByteOrder** della struttura **di \_ informazioni WSAPROTOCOL** specifica l'ordine dei byte di rete desiderato (attualmente big-endian o little-endian).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Porting delle applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**\_informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
