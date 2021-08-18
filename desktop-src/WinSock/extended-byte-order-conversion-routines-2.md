---
description: Windows Sockets 2 non presuppone che l'ordine dei byte di rete per tutti i protocolli sia lo stesso.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Routine Byte-Order conversione estesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2be1c217e89d19e607a64dfc943449351021506dc88f73ebcd4234a26b2b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132524"
---
# <a name="extended-byte-order-conversion-routines"></a>Routine Byte-Order conversione estesa

Windows Sockets 2 non presuppone che l'ordine dei byte di rete per tutti i protocolli sia lo stesso. Viene fornito un set di routine di conversione per la conversione di quantità a 16 bit e a 32 bit da e verso l'ordine dei byte di rete. Queste routine accettano come parametro di input l'handle del socket a cui è associata una struttura [**WSAPROTOCOL \_ INFO.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Il **membro NetworkByteOrder** della struttura **WSAPROTOCOL \_ INFO** specifica l'ordine dei byte di rete desiderato (attualmente big-endian o little-endian).

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

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
