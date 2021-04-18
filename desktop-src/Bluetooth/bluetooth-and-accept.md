---
title: Bluetooth e accetta
description: Bluetooth usa la funzione Accept per abilitare i tentativi di connessione in ingresso in un socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accettare
- Bluetooth
- Bluetooth
- Bluetooth e accetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300343"
---
# <a name="bluetooth-and-accept"></a><span data-ttu-id="d4392-107">Bluetooth e accetta</span><span class="sxs-lookup"><span data-stu-id="d4392-107">Bluetooth and accept</span></span>

<span data-ttu-id="d4392-108">Bluetooth usa la funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) per abilitare i tentativi di connessione in ingresso in un socket.</span><span class="sxs-lookup"><span data-stu-id="d4392-108">Bluetooth uses the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function to enable incoming connection attempts on a socket.</span></span> <span data-ttu-id="d4392-109">Il \_ valore addr BTH dell'applicazione client viene ottenuto leggendo la sezione specifica del trasporto Bluetooth della struttura [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) restituita.</span><span class="sxs-lookup"><span data-stu-id="d4392-109">The BTH\_ADDR of the client application is obtained by reading the Bluetooth transport-specific section of the returned [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) structure.</span></span> <span data-ttu-id="d4392-110">L'uso della funzione **Accept** con Bluetooth ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="d4392-110">Use of the **accept** function with Bluetooth has the following format:</span></span>

-   <span data-ttu-id="d4392-111">Il parametro *addr* della funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) è un puntatore facoltativo a un buffer che riceve l'indirizzo dell'entità di connessione, come noto al livello di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="d4392-111">The *addr* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to a buffer that receives the address of the connecting entity, as known to the communications layer.</span></span> <span data-ttu-id="d4392-112">Viene restituito un puntatore a una struttura [**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con l'indirizzo del dispositivo Bluetooth remoto.</span><span class="sxs-lookup"><span data-stu-id="d4392-112">A pointer to a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure with the remote Bluetooth device address is returned.</span></span>
-   <span data-ttu-id="d4392-113">Il parametro *addrlen* della funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) è un puntatore facoltativo a un Integer che contiene la lunghezza, in byte, di addr. Il valore integer deve essere maggiore o uguale al valore di **sizeof** ([**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span><span class="sxs-lookup"><span data-stu-id="d4392-113">The *addrlen* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to an integer that contains the length, in bytes, of addr. The integer must be greater or equal to the value of **sizeof** ([**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4392-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4392-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4392-115">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d4392-115">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="d4392-116">**accettare**</span><span class="sxs-lookup"><span data-stu-id="d4392-116">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 