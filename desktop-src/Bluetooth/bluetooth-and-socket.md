---
title: Bluetooth e socket
description: Crea un socket per le connessioni in ingresso o in uscita.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- connettore Bluetooth
- Bluetooth e connettore Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727650"
---
# <a name="bluetooth-and-socket"></a><span data-ttu-id="33e6e-106">Bluetooth e socket</span><span class="sxs-lookup"><span data-stu-id="33e6e-106">Bluetooth and socket</span></span>

<span data-ttu-id="33e6e-107">La funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crea un socket per le connessioni in ingresso o in uscita.:</span><span class="sxs-lookup"><span data-stu-id="33e6e-107">The [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function creates a socket for incoming or outgoing connections.:</span></span>

<span data-ttu-id="33e6e-108">Per creare un socket usando Bluetooth, usare le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="33e6e-108">To create a socket using Bluetooth, use the following settings:</span></span>

-   <span data-ttu-id="33e6e-109">Il parametro *AF* della funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) è sempre impostato su **AF \_ BTH** per i Socket Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="33e6e-109">The *af* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always set to **AF\_BTH** for Bluetooth sockets.</span></span>
-   <span data-ttu-id="33e6e-110">Il parametro di *tipo* della funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) è sempre **\_ Stream Sock**; **Calzino \_** I socket DGRAM non sono supportati da Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="33e6e-110">The *type* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always **SOCK\_STREAM**; **SOCK\_DGRAM** sockets are not supported by Bluetooth.</span></span>
-   <span data-ttu-id="33e6e-111">Per il parametro del *protocollo* , **BTHPROTO \_ rfcomm** è il protocollo supportato.</span><span class="sxs-lookup"><span data-stu-id="33e6e-111">For the *protocol* parameter, **BTHPROTO\_RFCOMM** is the supported protocol.</span></span>

<span data-ttu-id="33e6e-112">Per ulteriori informazioni, vedere [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span><span class="sxs-lookup"><span data-stu-id="33e6e-112">For more information, see [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="33e6e-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33e6e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33e6e-114">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="33e6e-114">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="33e6e-115">**presa**</span><span class="sxs-lookup"><span data-stu-id="33e6e-115">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 