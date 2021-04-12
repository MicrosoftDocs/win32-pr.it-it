---
description: Funzione gethostbyname nell'API Winsock.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Funzione gethostbyname nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129191"
---
# <a name="gethostbyname-function-in-the-api"></a><span data-ttu-id="aca0f-103">Funzione gethostbyname nell'API</span><span class="sxs-lookup"><span data-stu-id="aca0f-103">gethostbyname Function in the API</span></span>

<span data-ttu-id="aca0f-104">La funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) usa la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query su SVCID \_ inet \_ HOSTADDRBYNAME come GUID della classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="aca0f-104">The [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="aca0f-105">Il nome host viene fornito nel membro **lpszServiceInstanceName** della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passato alla funzione **WSALookupServiceBegin** .</span><span class="sxs-lookup"><span data-stu-id="aca0f-105">The host name is supplied in the **lpszServiceInstanceName** member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="aca0f-106">Il \_32.dll WS2 specifica il \_ BLOB restituito LUP \_ e il provider del servizio nome inserisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza).</span><span class="sxs-lookup"><span data-stu-id="aca0f-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="aca0f-107">I provider di servizi dei nomi devono rispettare \_ anche questi altri flag restituiti LUP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="aca0f-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="aca0f-108">Flag</span><span class="sxs-lookup"><span data-stu-id="aca0f-108">Flag</span></span>              | <span data-ttu-id="aca0f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aca0f-109">Description</span></span>                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aca0f-110">\_nome restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="aca0f-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="aca0f-111">Restituisce il membro del **\_ nome h** dalla struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="aca0f-111">Returns the **h\_name** member from the [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                           |
| <span data-ttu-id="aca0f-112">LUP \_ restituire \_ addr</span><span class="sxs-lookup"><span data-stu-id="aca0f-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="aca0f-113">Restituisce le informazioni di indirizzamento da [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle strutture delle [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . il valore predefinito per le informazioni sulla porta è zero.</span><span class="sxs-lookup"><span data-stu-id="aca0f-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="aca0f-114">Si noti che questa routine non risolve i nomi host che sono costituiti da un indirizzo IPv4 punteggiato.</span><span class="sxs-lookup"><span data-stu-id="aca0f-114">Note that this routine does not resolve host names that consist of a dotted IPv4 address.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="aca0f-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aca0f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aca0f-116">Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="aca0f-116">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="aca0f-117">Risoluzione dei nomi indipendente dal protocollo</span><span class="sxs-lookup"><span data-stu-id="aca0f-117">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="aca0f-118">Registrazione e risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="aca0f-118">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
