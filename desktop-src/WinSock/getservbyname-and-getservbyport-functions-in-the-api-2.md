---
description: Le funzioni getservbyname e getservbyport usano la funzione WSALookupServiceBegin per eseguire query SVCID \_ inet \_ SERVICEBYNAME come GUID della classe del servizio.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funzioni getservbyname e getservbyport nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306958"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a><span data-ttu-id="378fe-103">Funzioni getservbyname e getservbyport nell'API</span><span class="sxs-lookup"><span data-stu-id="378fe-103">getservbyname and getservbyport Functions in the API</span></span>

<span data-ttu-id="378fe-104">Le funzioni [**GetServByName**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usano la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire query SVCID \_ inet \_ SERVICEBYNAME come GUID della classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="378fe-104">The [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions use the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_SERVICEBYNAME as the service class GUID.</span></span> <span data-ttu-id="378fe-105">Il membro *lpszServiceInstanceName* della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passato alla funzione **WSALookupServiceBegin** fa riferimento a una stringa che indica il nome del servizio o la porta del servizio e, facoltativamente, il protocollo del servizio.</span><span class="sxs-lookup"><span data-stu-id="378fe-105">The *lpszServiceInstanceName* member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function references a string to indicate the service name or service port, and (optionally) the service protocol.</span></span> <span data-ttu-id="378fe-106">La formattazione della stringa è illustrata come FTP o TCP o 21/TCP o solo FTP.</span><span class="sxs-lookup"><span data-stu-id="378fe-106">The formatting of the string is illustrated as FTP or TCP or 21/TCP or just FTP.</span></span> <span data-ttu-id="378fe-107">La stringa non distingue tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="378fe-107">The string is not case sensitive.</span></span> <span data-ttu-id="378fe-108">La barra contrassegnata, se presente, separa l'identificatore del protocollo dalla parte precedente della stringa.</span><span class="sxs-lookup"><span data-stu-id="378fe-108">The slash mark, if present, separates the protocol identifier from the preceding part of the string.</span></span> <span data-ttu-id="378fe-109">Il \_32.dll WS2 specifica il \_ BLOB restituito LUP \_ e il provider dello spazio dei nomi inserisce una struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza).</span><span class="sxs-lookup"><span data-stu-id="378fe-109">The Ws2\_32.dll will specify LUP\_RETURN\_BLOB and the namespace provider will place a [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="378fe-110">I provider dello spazio dei nomi devono rispettare anche questi altri \_ flag restituiti LUP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="378fe-110">Namespace providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="378fe-111">Flag</span><span class="sxs-lookup"><span data-stu-id="378fe-111">Flag</span></span>              | <span data-ttu-id="378fe-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="378fe-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="378fe-113">\_nome restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="378fe-113">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="378fe-114">Restituisce il membro del **\_ nome s** dalla struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) in *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="378fe-114">Returns the **s\_name** member from [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="378fe-115">\_tipo restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="378fe-115">LUP\_RETURN\_TYPE</span></span> | <span data-ttu-id="378fe-116">Restituisce il GUID canonico in *lpServiceClassId* . si comprende che un servizio identificato come FTP o 21 può trovarsi in un'altra porta secondo le convenzioni stabilite localmente.</span><span class="sxs-lookup"><span data-stu-id="378fe-116">Returns canonical GUID in *lpServiceClassId* It is understood that a service identified as FTP or 21 may be on another port according to locally established conventions.</span></span> <span data-ttu-id="378fe-117">Il parametro della **\_ porta s** della struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicare la posizione in cui il servizio può essere contattato nell'ambiente locale.</span><span class="sxs-lookup"><span data-stu-id="378fe-117">The **s\_port** parameter of the [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure should indicate where the service can be contacted in the local environment.</span></span> <span data-ttu-id="378fe-118">Il GUID canonico restituito quando \_ \_ è impostato il tipo restituito LUP deve essere uno dei GUID predefiniti di Svcs. h che corrisponde al numero di porta indicato nella struttura **SERVENT** .</span><span class="sxs-lookup"><span data-stu-id="378fe-118">The canonical GUID returned when LUP\_RETURN\_TYPE is set should be one of the predefined GUIDs from Svcs.h that corresponds to the port number indicated in the **SERVENT** structure.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="378fe-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="378fe-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="378fe-120">Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="378fe-120">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="378fe-121">Risoluzione dei nomi indipendente dal protocollo</span><span class="sxs-lookup"><span data-stu-id="378fe-121">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="378fe-122">Registrazione e risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="378fe-122">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



