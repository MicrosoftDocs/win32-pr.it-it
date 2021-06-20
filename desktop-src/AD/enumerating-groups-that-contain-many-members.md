---
title: Enumerazione di gruppi che contengono molti membri
description: Informazioni sull'enumerazione Azure Active Directory che contengono molti membri usando il recupero incrementale dei dati (recupero di intervalli).
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Enumerazione di gruppi che contengono molti membri in Active Directory
- groups Active Directory , enumerazione di gruppi con molti membri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cab63b809fdbd2666f39a09d32f601346da00e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405154"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="636a9-105">Enumerazione di gruppi che contengono molti membri</span><span class="sxs-lookup"><span data-stu-id="636a9-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="636a9-106">I membri di un gruppo vengono archiviati in un attributo multivalore denominato **membro**.</span><span class="sxs-lookup"><span data-stu-id="636a9-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="636a9-107">**L'attributo** del membro può contenere un numero elevato di valori.</span><span class="sxs-lookup"><span data-stu-id="636a9-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="636a9-108">L'enumerazione dei membri può risultare inefficiente quando il numero di valori in un attributo multivalore diventa elevato.</span><span class="sxs-lookup"><span data-stu-id="636a9-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="636a9-109">Il server limiterà anche il numero massimo di valori che possono essere recuperati in una singola query.</span><span class="sxs-lookup"><span data-stu-id="636a9-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="636a9-110">Ciò significa che se un gruppo può avere più membri di quelli che possono essere forniti dal server, l'unico modo per enumerare tutti i membri è usare il recupero incrementale dei dati, noto come recupero di *intervalli.*</span><span class="sxs-lookup"><span data-stu-id="636a9-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="636a9-111">Il recupero di intervalli comporta la richiesta di un numero limitato di valori di attributo in una singola query.</span><span class="sxs-lookup"><span data-stu-id="636a9-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="636a9-112">Il numero di valori richiesti deve essere minore o uguale al numero massimo di valori supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="636a9-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="636a9-113">Per ridurre il numero di volte in cui la query deve contattare il server, il numero di valori richiesti deve essere il più vicino possibile a questo valore massimo.</span><span class="sxs-lookup"><span data-stu-id="636a9-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="636a9-114">Per consentire a un'applicazione di funzionare correttamente con tutti i server, è necessario usare un numero massimo di 1000.</span><span class="sxs-lookup"><span data-stu-id="636a9-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="636a9-115">La versione del server che fornisce i dati richiesti determina il numero massimo di valori che possono essere recuperati in una singola query.</span><span class="sxs-lookup"><span data-stu-id="636a9-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="636a9-116">Nella tabella seguente sono elencati la versione del server e il numero massimo di valori che è possibile recuperare in una singola query.</span><span class="sxs-lookup"><span data-stu-id="636a9-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="636a9-117">Versione del sistema operativo del server</span><span class="sxs-lookup"><span data-stu-id="636a9-117">Server operating system version</span></span> | <span data-ttu-id="636a9-118">Valori massimi recuperati</span><span class="sxs-lookup"><span data-stu-id="636a9-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="636a9-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="636a9-119">Windows 2000</span></span>                    | <span data-ttu-id="636a9-120">1000</span><span class="sxs-lookup"><span data-stu-id="636a9-120">1000</span></span>                     |
| <span data-ttu-id="636a9-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="636a9-121">Windows Server 2003</span></span>             | <span data-ttu-id="636a9-122">1500</span><span class="sxs-lookup"><span data-stu-id="636a9-122">1500</span></span>                     |



 

<span data-ttu-id="636a9-123">Per altre informazioni sul recupero di intervalli di valori di attributo con ADSI, vedere [Recupero di intervalli di attributi.](/windows/desktop/ADSI/attribute-range-retrieval)</span><span class="sxs-lookup"><span data-stu-id="636a9-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="636a9-124">Per altre informazioni sul recupero di intervalli di valori di attributo [con System.DirectoryServices](/dotnet/api/system.directoryservices), vedere [Enumerazione dei membri in un gruppo di grandi dimensioni.](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx)</span><span class="sxs-lookup"><span data-stu-id="636a9-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 