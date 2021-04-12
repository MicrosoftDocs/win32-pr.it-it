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
# <a name="extended-byte-order-conversion-routines"></a><span data-ttu-id="f9e28-103">Routine di conversione Byte-Order estese</span><span class="sxs-lookup"><span data-stu-id="f9e28-103">Extended Byte-Order Conversion Routines</span></span>

<span data-ttu-id="f9e28-104">Windows Sockets 2 non presuppone che l'ordine dei byte di rete per tutti i protocolli sia lo stesso.</span><span class="sxs-lookup"><span data-stu-id="f9e28-104">Windows Sockets 2 does not assume that the network byte order for all protocols is the same.</span></span> <span data-ttu-id="f9e28-105">Viene fornito un set di routine di conversione per la conversione di quantità a 16 bit e a 32 bit da e verso l'ordine dei byte di rete.</span><span class="sxs-lookup"><span data-stu-id="f9e28-105">A set of conversion routines is supplied for converting 16-bit and 32-bit quantities to and from network byte order.</span></span> <span data-ttu-id="f9e28-106">Queste routine accettano come parametro di input l'handle del socket a cui è associata una struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="f9e28-106">These routines take as an input parameter the socket handle that has a [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure associated with it.</span></span> <span data-ttu-id="f9e28-107">Il membro **NetworkByteOrder** della struttura **di \_ informazioni WSAPROTOCOL** specifica l'ordine dei byte di rete desiderato (attualmente big-endian o little-endian).</span><span class="sxs-lookup"><span data-stu-id="f9e28-107">The **NetworkByteOrder** member of the **WSAPROTOCOL\_INFO** structure specifies the desired network byte order (currently either big-endian or little-endian).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9e28-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9e28-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9e28-109">**htonl**</span><span class="sxs-lookup"><span data-stu-id="f9e28-109">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="f9e28-110">**htons**</span><span class="sxs-lookup"><span data-stu-id="f9e28-110">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="f9e28-111">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="f9e28-111">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="f9e28-112">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="f9e28-112">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="f9e28-113">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="f9e28-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="f9e28-114">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="f9e28-114">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="f9e28-115">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="f9e28-115">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="f9e28-116">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="f9e28-116">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="f9e28-117">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="f9e28-117">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="f9e28-118">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="f9e28-118">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[<span data-ttu-id="f9e28-119">**\_informazioni WSAPROTOCOL**</span><span class="sxs-lookup"><span data-stu-id="f9e28-119">**WSAPROTOCOL\_INFO**</span></span>](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
