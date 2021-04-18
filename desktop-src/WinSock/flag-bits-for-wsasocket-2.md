---
description: In alcuni casi, i socket aggiunti a una sessione multipoint possono presentare alcune differenze nel comportamento dei socket da punto a punto.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Bit del flag per WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306982"
---
# <a name="flag-bits-for-wsasocket"></a><span data-ttu-id="85521-103">Bit del flag per WSASocket</span><span class="sxs-lookup"><span data-stu-id="85521-103">Flag Bits for WSASocket</span></span>

<span data-ttu-id="85521-104">In alcuni casi, i socket aggiunti a una sessione multipoint possono presentare alcune differenze nel comportamento dei socket da punto a punto.</span><span class="sxs-lookup"><span data-stu-id="85521-104">In some instances sockets joined to a multipoint session may have some differences in behavior from point-to-point sockets.</span></span> <span data-ttu-id="85521-105">Ad esempio, un \_ socket foglia d in uno schema di piano dati radice può inviare informazioni solo al \_ partecipante radice d.</span><span class="sxs-lookup"><span data-stu-id="85521-105">For example, a d\_leaf socket in a rooted data plane scheme can only send information to the d\_root participant.</span></span> <span data-ttu-id="85521-106">In questo modo l'applicazione deve essere in grado di indicare l'uso previsto di un socket coincidente con la relativa creazione.</span><span class="sxs-lookup"><span data-stu-id="85521-106">This creates a need for the application to be able to indicate the intended use of a socket coincident with its creation.</span></span> <span data-ttu-id="85521-107">Questa operazione viene eseguita tramite un bit di quattro flag che può essere impostato nel parametro *dwFlags* su [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span><span class="sxs-lookup"><span data-stu-id="85521-107">This is done through four-flag bits that can be set in the *dwFlags* parameter to [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span></span>

-   <span data-ttu-id="85521-108">\_ \_ Radice del flag WSA multipoint \_ c \_ , per la creazione di un socket che funge da \_ radice c e consentito solo se un piano di controllo radice è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="85521-108">WSA\_FLAG\_MULTIPOINT\_C\_ROOT, for the creation of a socket acting as a c\_root, and only allowed if a rooted control plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="85521-109">Il \_ flag WSA \_ multipoint \_ C \_ foglia, per la creazione di un socket che funge da \_ foglia c e consentito solo se XP1 \_ supporta \_ multipoint è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="85521-109">WSA\_FLAG\_MULTIPOINT\_C\_LEAF, for the creation of a socket acting as a c\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="85521-110">FLAG WSA: \_ \_ \_ radice multipoint d \_ , per la creazione di un socket che funge da \_ radice d e consentito solo se un piano dati radice è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="85521-110">WSA\_FLAG\_MULTIPOINT\_D\_ROOT, for the creation of a socket acting as a d\_root, and only allowed if a rooted data plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="85521-111">La \_ \_ foglia multipoint \_ d del flag WSA \_ , per la creazione di un socket che funge da \_ foglia d, ed è consentita solo se XP1 \_ supporta \_ multipoint è indicato nella voce di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="85521-111">WSA\_FLAG\_MULTIPOINT\_D\_LEAF, for the creation of a socket acting as a d\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>

<span data-ttu-id="85521-112">Si noti che quando si crea un socket MultiPoint, esattamente uno dei due flag del piano di controllo e uno dei due flag del piano dati deve essere impostato nel parametro *dwFlags* di [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="85521-112">Note that when creating a multipoint socket, exactly one of the two control-plane flags, and one of the two data-plane flags must be set in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)'s *dwFlags* parameter.</span></span> <span data-ttu-id="85521-113">Quindi, le quattro possibilità per la creazione di socket multipoint sono:</span><span class="sxs-lookup"><span data-stu-id="85521-113">Thus, the four possibilities for creating multipoint sockets are:</span></span>

-   <span data-ttu-id="85521-114">" \_ radice c radice/d \_ "</span><span class="sxs-lookup"><span data-stu-id="85521-114">"c\_root/d\_root"</span></span>
-   <span data-ttu-id="85521-115">" \_ foglia radice c/d \_ "</span><span class="sxs-lookup"><span data-stu-id="85521-115">"c\_root/d\_leaf"</span></span>
-   <span data-ttu-id="85521-116">" \_ radice foglia/d c \_ "</span><span class="sxs-lookup"><span data-stu-id="85521-116">"c\_leaf/d\_root"</span></span>
-   <span data-ttu-id="85521-117">"foglia c \_ /d \_ foglia"</span><span class="sxs-lookup"><span data-stu-id="85521-117">"c\_leaf /d\_leaf"</span></span>

 

 
