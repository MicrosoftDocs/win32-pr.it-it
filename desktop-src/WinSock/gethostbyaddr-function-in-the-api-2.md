---
description: La funzione gethostbyaddr usa la funzione WSALookupServiceBegin per eseguire una query su SVCID \_ inet \_ HOSTNAMEBYADDR come GUID della classe del servizio.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Funzione gethostbyaddr nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306969"
---
# <a name="gethostbyaddr-function-in-the-api"></a><span data-ttu-id="c56a6-103">Funzione gethostbyaddr nell'API</span><span class="sxs-lookup"><span data-stu-id="c56a6-103">gethostbyaddr Function in the API</span></span>

<span data-ttu-id="c56a6-104">La funzione [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) usa la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query su SVCID \_ inet \_ HOSTNAMEBYADDR come GUID della classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="c56a6-104">The [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="c56a6-105">L'indirizzo host viene fornito come stringa decimnal IPv4 punteggiata (ad esempio, "192.9.200.120") nel membro *lpszServiceInstanceName* della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passata alla funzione **WSALookupServiceBegin** .</span><span class="sxs-lookup"><span data-stu-id="c56a6-105">The host address is supplied as a dotted decimnal IPv4 string (for example, "192.9.200.120") in the *lpszServiceInstanceName* member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="c56a6-106">Il \_32.dll WS2 specifica il \_ BLOB restituito LUP \_ e il provider del servizio nome inserisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza).</span><span class="sxs-lookup"><span data-stu-id="c56a6-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="c56a6-107">I provider di servizi dei nomi devono rispettare \_ anche questi altri flag restituiti LUP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="c56a6-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span> 

| <span data-ttu-id="c56a6-108">Flag</span><span class="sxs-lookup"><span data-stu-id="c56a6-108">Flag</span></span>              | <span data-ttu-id="c56a6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c56a6-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56a6-110">\_nome restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="c56a6-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="c56a6-111">Restituisce il membro del **\_ nome h** dalla struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="c56a6-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="c56a6-112">LUP \_ restituire \_ addr</span><span class="sxs-lookup"><span data-stu-id="c56a6-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="c56a6-113">Restituisce le informazioni di indirizzamento da [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle strutture delle [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . il valore predefinito per le informazioni sulla porta è zero.</span><span class="sxs-lookup"><span data-stu-id="c56a6-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c56a6-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c56a6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c56a6-115">Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="c56a6-115">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="c56a6-116">Risoluzione dei nomi indipendente dal protocollo</span><span class="sxs-lookup"><span data-stu-id="c56a6-116">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="c56a6-117">Registrazione e risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="c56a6-117">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
