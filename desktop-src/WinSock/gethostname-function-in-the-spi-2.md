---
description: La query WSALookupServiceBegin usa il \_ nome host SVCID come GUID della classe del servizio.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: Funzione gethostname in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306966"
---
# <a name="gethostname-function-in-the-spi"></a><span data-ttu-id="0df71-103">Funzione gethostname in SPI</span><span class="sxs-lookup"><span data-stu-id="0df71-103">gethostname Function in the SPI</span></span>

<span data-ttu-id="0df71-104">La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa il \_ nome host SVCID come GUID della classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="0df71-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="0df71-105">Se *lpszServiceInstanceName* è null o fa riferimento a una stringa null (ovvero.</span><span class="sxs-lookup"><span data-stu-id="0df71-105">If *lpszServiceInstanceName* is null or references a null string (that is .</span></span> <span data-ttu-id="0df71-106">""), l'host locale deve essere risolto.</span><span class="sxs-lookup"><span data-stu-id="0df71-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="0df71-107">In caso contrario, verrà eseguita una ricerca in un nome host specificato.</span><span class="sxs-lookup"><span data-stu-id="0df71-107">Otherwise, a lookup on a specified host name shall occur.</span></span> <span data-ttu-id="0df71-108">Ai fini dell'emulazione di [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) , il WS2 \_32.dll specifica un puntatore null per *lpszServiceInstanceName* e specifica LUP \_ nome restituito \_ in modo che il nome host venga restituito nel parametro *lpszServiceInstanceName* .</span><span class="sxs-lookup"><span data-stu-id="0df71-108">For the purposes of emulating [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) the Ws2\_32.dll will specify a null pointer for *lpszServiceInstanceName*, and specify LUP\_RETURN\_NAME so that the host name is returned in the *lpszServiceInstanceName* parameter.</span></span> <span data-ttu-id="0df71-109">Se un'applicazione usa questa query e specifica LUP \_ return \_ addr, l'indirizzo host verrà fornito in una struttura **di \_ informazioni di CSADDR** .</span><span class="sxs-lookup"><span data-stu-id="0df71-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address will be provided in a **CSADDR\_INFO** structure.</span></span> <span data-ttu-id="0df71-110">L' \_ azione LUP return \_ BLOB non è definita per questa query.</span><span class="sxs-lookup"><span data-stu-id="0df71-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="0df71-111">Le informazioni sulla porta verranno automaticamente azzerate a meno che *lpszQueryString* faccia riferimento a un servizio quale FTP, nel qual caso verrà fornito l'indirizzo di trasporto completo del servizio indicato.</span><span class="sxs-lookup"><span data-stu-id="0df71-111">Port information will be defaulted to zero unless the *lpszQueryString* references a service such as ftp, in which case the complete transport address of the indicated service will be supplied.</span></span>

 

 



