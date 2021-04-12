---
description: La query WSALookupServiceBegin USA SVCID \_ inet \_ HOSTNAMEBYADDR come GUID della classe del servizio.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Funzione gethostbyaddr in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526172"
---
# <a name="gethostbyaddr-function-in-the-spi"></a><span data-ttu-id="95f8a-103">Funzione gethostbyaddr in SPI</span><span class="sxs-lookup"><span data-stu-id="95f8a-103">gethostbyaddr Function in the SPI</span></span>

<span data-ttu-id="95f8a-104">La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) USA SVCID \_ inet \_ HOSTNAMEBYADDR come GUID della classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="95f8a-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="95f8a-105">L'indirizzo host viene fornito in *lpszServiceInstanceName* come stringa di indirizzo IPv4 decimale punteggiata (ad esempio, 192.9.200.120).</span><span class="sxs-lookup"><span data-stu-id="95f8a-105">The host address is supplied in *lpszServiceInstanceName* as a dotted-decimal IPv4 address string (for example, 192.9.200.120).</span></span> <span data-ttu-id="95f8a-106">Il *\_32.dllWS2* specifica il \_ BLOB restituito LUP \_ e NSP inserisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza).</span><span class="sxs-lookup"><span data-stu-id="95f8a-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="95f8a-107">Rete deve rispettare anche questi altri \_ \_ \* flag di LUP restituiti.</span><span class="sxs-lookup"><span data-stu-id="95f8a-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="95f8a-108">Flag</span><span class="sxs-lookup"><span data-stu-id="95f8a-108">Flag</span></span>              | <span data-ttu-id="95f8a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95f8a-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f8a-110">\_nome restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="95f8a-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="95f8a-111">Restituisce il membro del **\_ nome h** dalla struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="95f8a-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="95f8a-112">LUP \_ restituire \_ addr</span><span class="sxs-lookup"><span data-stu-id="95f8a-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="95f8a-113">Restituisce le informazioni di indirizzamento da [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle strutture delle [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . il valore predefinito per le informazioni sulla porta è zero.</span><span class="sxs-lookup"><span data-stu-id="95f8a-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

 

 
