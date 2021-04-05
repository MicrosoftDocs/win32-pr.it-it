---
description: Di seguito è riportata una guida per la protezione della programmazione di Windows Sockets.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Programmazione Winsock sicura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755074"
---
# <a name="secure-winsock-programming"></a><span data-ttu-id="0b32a-103">Programmazione Winsock sicura</span><span class="sxs-lookup"><span data-stu-id="0b32a-103">Secure Winsock Programming</span></span>

<span data-ttu-id="0b32a-104">Di seguito è riportata una guida per la protezione della programmazione di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="0b32a-104">The following is a guide to secure Windows Sockets programming.</span></span> <span data-ttu-id="0b32a-105">È progettato per fornire informazioni sulla sicurezza di Winsock e sulle opzioni disponibili per lo sviluppatore di applicazioni di rete sicure.</span><span class="sxs-lookup"><span data-stu-id="0b32a-105">It is designed to provide an understanding of Winsock security and the options available to the secure network application developer.</span></span>

-   [<span data-ttu-id="0b32a-106">Con \_ REUSEADDR e \_ EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="0b32a-106">Using SO\_REUSEADDR and SO\_EXCLUSIVEADDRUSE</span></span>](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [<span data-ttu-id="0b32a-107">Estensioni Secure socket Winsock</span><span class="sxs-lookup"><span data-stu-id="0b32a-107">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)

<span data-ttu-id="0b32a-108">Le comunicazioni che usano i socket possono anche essere crittografate usando gli standard SSL/TLS usando un canale sicuro, noto anche come tecnologia Schannel.</span><span class="sxs-lookup"><span data-stu-id="0b32a-108">Communications using sockets can also be encrypted using the SSL/TLS standards using Secure Channel, also known as Schannel technology.</span></span> <span data-ttu-id="0b32a-109">Schannel è un Security Support Provider (SSP) che contiene un set di protocolli di sicurezza che forniscono l'autenticazione delle identità e la comunicazione privata protetta tramite crittografia.</span><span class="sxs-lookup"><span data-stu-id="0b32a-109">Schannel is a security support provider (SSP) that contains a set of security protocols that provide identity authentication and secure, private communication through encryption.</span></span> <span data-ttu-id="0b32a-110">Schannel viene usato principalmente per le applicazioni Internet che richiedono comunicazioni di Hypertext Transfer Protocol (HTTP) sicure.</span><span class="sxs-lookup"><span data-stu-id="0b32a-110">Schannel is primarily used for Internet applications that require secure Hypertext Transfer Protocol (HTTP) communications.</span></span> <span data-ttu-id="0b32a-111">Per altre informazioni, vedere [canale sicuro](../secauthn/secure-channel.md).</span><span class="sxs-lookup"><span data-stu-id="0b32a-111">For more information, please see [Secure Channel](../secauthn/secure-channel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b32a-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b32a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b32a-113">Canale sicuro</span><span class="sxs-lookup"><span data-stu-id="0b32a-113">Secure Channel</span></span>](../secauthn/secure-channel.md)
</dt> </dl>

 

 
