---
description: Funzione gethostbyname nell'SPI Winsock.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Funzione gethostbyname in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306968"
---
# <a name="gethostbyname-function-in-the-spi"></a><span data-ttu-id="f98c2-103">Funzione gethostbyname in SPI</span><span class="sxs-lookup"><span data-stu-id="f98c2-103">gethostbyname Function in the SPI</span></span>

<span data-ttu-id="f98c2-104">La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) USA SVCID \_ inet \_ HOSTADDRBYNAME come GUID della classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="f98c2-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="f98c2-105">Il nome host viene fornito in *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="f98c2-105">The host name is supplied in *lpszServiceInstanceName*.</span></span> <span data-ttu-id="f98c2-106">Il *\_32.dllWS2* specifica il \_ BLOB restituito LUP \_ e NSP inserisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza).</span><span class="sxs-lookup"><span data-stu-id="f98c2-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="f98c2-107">Rete deve rispettare anche questi altri \_ \_ \* flag di LUP restituiti.</span><span class="sxs-lookup"><span data-stu-id="f98c2-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="f98c2-108">Flag</span><span class="sxs-lookup"><span data-stu-id="f98c2-108">Flag</span></span>              | <span data-ttu-id="f98c2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f98c2-109">Description</span></span>                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f98c2-110">\_nome restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="f98c2-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="f98c2-111">Restituisce il membro del **\_ nome h** dalla struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="f98c2-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                            |
| <span data-ttu-id="f98c2-112">LUP \_ restituire \_ addr</span><span class="sxs-lookup"><span data-stu-id="f98c2-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="f98c2-113">Restituisce le informazioni di indirizzamento da [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle strutture delle [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . il valore predefinito per le informazioni sulla porta è zero.</span><span class="sxs-lookup"><span data-stu-id="f98c2-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="f98c2-114">Si noti che questa routine non risolve i nomi host costituiti da una stringa di indirizzo IPv4 decimale punteggiata.</span><span class="sxs-lookup"><span data-stu-id="f98c2-114">Note that this routine does not resolve host names consisting of a dotted-decimal IPv4 address string.</span></span> |



 

 

 
