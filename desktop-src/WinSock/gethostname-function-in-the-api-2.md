---
description: La funzione GetHostName utilizza la funzione WSALookupServiceBegin per eseguire una query sul \_ nome host SVCID come GUID della classe del servizio.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Funzione GetHostName nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306967"
---
# <a name="gethostname-function-in-the-api"></a><span data-ttu-id="e98dc-103">Funzione GetHostName nell'API</span><span class="sxs-lookup"><span data-stu-id="e98dc-103">gethostname Function in the API</span></span>

<span data-ttu-id="e98dc-104">La funzione [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) utilizza la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query sul \_ nome host SVCID come GUID della classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="e98dc-104">The [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="e98dc-105">Se il membro **lpszServiceInstanceName** della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passato alla funzione **WSALookupServiceBegin** è **null** o fa riferimento a una stringa **null** , ovvero.</span><span class="sxs-lookup"><span data-stu-id="e98dc-105">If the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function is **NULL** or references a **NULL** string (that is .</span></span> <span data-ttu-id="e98dc-106">""), l'host locale deve essere risolto.</span><span class="sxs-lookup"><span data-stu-id="e98dc-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="e98dc-107">In caso contrario, viene eseguita una ricerca in un nome host specificato.</span><span class="sxs-lookup"><span data-stu-id="e98dc-107">Otherwise, a lookup on a specified host name occurs.</span></span> <span data-ttu-id="e98dc-108">Ai fini dell'emulazione di **GetHostName** , WS2 \_32.dll specifica un puntatore **null** per il membro **lpszServiceInstanceName** e specifica LUP \_ nome restituito \_ in modo che il nome host venga restituito nel membro **lpszServiceInstanceName** .</span><span class="sxs-lookup"><span data-stu-id="e98dc-108">For the purposes of emulating **gethostname** the Ws2\_32.dll specifies a **NULL** pointer for the **lpszServiceInstanceName** member, and specifies LUP\_RETURN\_NAME so that the host name is returned in the **lpszServiceInstanceName** member.</span></span> <span data-ttu-id="e98dc-109">Se un'applicazione usa questa query e specifica LUP \_ return \_ addr, l'indirizzo host viene fornito in una struttura di [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="e98dc-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address is provided in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span> <span data-ttu-id="e98dc-110">L' \_ azione LUP return \_ BLOB non è definita per questa query.</span><span class="sxs-lookup"><span data-stu-id="e98dc-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="e98dc-111">Le informazioni sulla porta vengono predefinite su zero, a meno che il membro **lpszQueryString** della struttura **WSAQUERYSET** passato alla funzione **WSALookupServiceBegin** faccia riferimento a un servizio quale FTP, nel qual caso viene fornito l'indirizzo di trasporto completo del servizio indicato.</span><span class="sxs-lookup"><span data-stu-id="e98dc-111">Port information is defaulted to zero unless the **lpszQueryString** member of the **WSAQUERYSET** structure passed to the **WSALookupServiceBegin** function references a service such as FTP, in which case the complete transport address of the indicated service is supplied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e98dc-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e98dc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e98dc-113">Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="e98dc-113">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="e98dc-114">Risoluzione dei nomi indipendente dal protocollo</span><span class="sxs-lookup"><span data-stu-id="e98dc-114">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="e98dc-115">Registrazione e risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="e98dc-115">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
