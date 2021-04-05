---
description: Un socket non elaborato è un tipo di socket che consente l'accesso al provider di trasporto sottostante. Per diversi motivi, non è consigliabile usare i socket non elaborati durante il porting di applicazioni a Winsock.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Socket non elaborati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131023"
---
# <a name="raw-sockets"></a><span data-ttu-id="065f8-104">Socket non elaborati</span><span class="sxs-lookup"><span data-stu-id="065f8-104">Raw Sockets</span></span>

<span data-ttu-id="065f8-105">Un socket non elaborato è un tipo di socket che consente l'accesso al provider di trasporto sottostante.</span><span class="sxs-lookup"><span data-stu-id="065f8-105">A raw socket is a type of socket that allows access to the underlying transport provider.</span></span> <span data-ttu-id="065f8-106">Per diversi motivi, non è consigliabile usare i socket non elaborati durante il porting di applicazioni a Winsock.</span><span class="sxs-lookup"><span data-stu-id="065f8-106">The use of raw sockets when porting applications to Winsock is not recommended for several reasons.</span></span>

<span data-ttu-id="065f8-107">La specifica di Windows Sockets non impone che un provider di servizi Winsock supporti i socket non elaborati, ovvero i socket di tipo **Sock \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="065f8-107">The Windows Sockets specification does not mandate that a Winsock service provider support raw sockets, that is, sockets of type **SOCK\_RAW**.</span></span> <span data-ttu-id="065f8-108">Tuttavia, i provider di servizi sono invitati a fornire supporto per socket non elaborato.</span><span class="sxs-lookup"><span data-stu-id="065f8-108">However, service providers are encouraged to supply raw socket support.</span></span> <span data-ttu-id="065f8-109">Un'applicazione compatibile con Windows Sockets che desidera utilizzare i socket non elaborati deve tentare di aprire il socket con la chiamata al [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e, in caso di esito negativo, tentare di utilizzare un altro tipo di socket o indicare l'errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="065f8-109">A Windows Sockets-compliant application that wishes to use raw sockets should attempt to open the socket with the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call, and if it fails either attempt to use another socket type or indicate the failure to the user.</span></span>

<span data-ttu-id="065f8-110">In Windows 7, Windows Server 2008 R2, Windows Vista e Windows XP con Service Pack 2 (SP2), la possibilità di inviare traffico su socket non elaborati è stata limitata in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="065f8-110">On Windows 7, Windows Server 2008 R2, Windows Vista, and Windows XP with Service Pack 2 (SP2), the ability to send traffic over raw sockets has been restricted in several ways.</span></span> <span data-ttu-id="065f8-111">Per ulteriori informazioni, vedere [TCP/IP raw Sockets](tcp-ip-raw-sockets-2.md).</span><span class="sxs-lookup"><span data-stu-id="065f8-111">For more information, see [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="065f8-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="065f8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="065f8-113">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="065f8-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="065f8-114">**presa**</span><span class="sxs-lookup"><span data-stu-id="065f8-114">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="065f8-115">Socket TCP/IP raw</span><span class="sxs-lookup"><span data-stu-id="065f8-115">TCP/IP Raw Sockets</span></span>](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[<span data-ttu-id="065f8-116">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="065f8-116">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



