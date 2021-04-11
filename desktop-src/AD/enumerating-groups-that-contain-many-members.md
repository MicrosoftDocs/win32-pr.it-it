---
title: Enumerazione dei gruppi che contengono molti membri
description: I membri di un gruppo vengono archiviati in un attributo multivalore denominato member.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Enumerazione dei gruppi che contengono molti membri Active Directory
- gruppi Active Directory, enumerazione di gruppi con molti membri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2d9a5c9abc6e77ac72672379789d1028f92c3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117563"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="36a72-105">Enumerazione dei gruppi che contengono molti membri</span><span class="sxs-lookup"><span data-stu-id="36a72-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="36a72-106">I membri di un gruppo vengono archiviati in un attributo multivalore denominato **member**.</span><span class="sxs-lookup"><span data-stu-id="36a72-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="36a72-107">L'attributo **member** può contenere un numero elevato di valori.</span><span class="sxs-lookup"><span data-stu-id="36a72-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="36a72-108">L'enumerazione dei membri può risultare inefficiente quando il numero di valori in un attributo multivalore diventa grande.</span><span class="sxs-lookup"><span data-stu-id="36a72-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="36a72-109">Il server limiterà anche il numero massimo di valori che possono essere recuperati in una singola query.</span><span class="sxs-lookup"><span data-stu-id="36a72-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="36a72-110">Ciò significa che se un gruppo può avere più membri rispetto a quelli che possono essere forniti dal server, l'unico modo per enumerare tutti i membri consiste nell'usare il recupero incrementale dei dati, noto come *recupero di intervalli*.</span><span class="sxs-lookup"><span data-stu-id="36a72-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="36a72-111">Il recupero di intervalli implica la richiesta di un numero limitato di valori di attributo in una singola query.</span><span class="sxs-lookup"><span data-stu-id="36a72-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="36a72-112">Il numero di valori richiesti deve essere minore o uguale al numero massimo di valori supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="36a72-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="36a72-113">Per ridurre il numero di volte in cui la query deve contattare il server, il numero di valori richiesti dovrebbe essere il più vicino possibile a questo valore massimo.</span><span class="sxs-lookup"><span data-stu-id="36a72-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="36a72-114">Per consentire a un'applicazione di funzionare correttamente con tutti i server, è necessario usare un numero massimo di 1000.</span><span class="sxs-lookup"><span data-stu-id="36a72-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="36a72-115">La versione del server che fornisce i dati richiesti determina il numero massimo di valori che possono essere recuperati in una singola query.</span><span class="sxs-lookup"><span data-stu-id="36a72-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="36a72-116">Nella tabella seguente sono elencate la versione del server e il numero massimo di valori che possono essere recuperati in una singola query.</span><span class="sxs-lookup"><span data-stu-id="36a72-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="36a72-117">Versione del sistema operativo del server</span><span class="sxs-lookup"><span data-stu-id="36a72-117">Server operating system version</span></span> | <span data-ttu-id="36a72-118">Numero massimo di valori recuperati</span><span class="sxs-lookup"><span data-stu-id="36a72-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="36a72-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="36a72-119">Windows 2000</span></span>                    | <span data-ttu-id="36a72-120">1000</span><span class="sxs-lookup"><span data-stu-id="36a72-120">1000</span></span>                     |
| <span data-ttu-id="36a72-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36a72-121">Windows Server 2003</span></span>             | <span data-ttu-id="36a72-122">1500</span><span class="sxs-lookup"><span data-stu-id="36a72-122">1500</span></span>                     |



 

<span data-ttu-id="36a72-123">Per ulteriori informazioni sul recupero di intervalli di valori di attributo con ADSI, vedere Recupero di intervalli di [attributi](/windows/desktop/ADSI/attribute-range-retrieval).</span><span class="sxs-lookup"><span data-stu-id="36a72-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="36a72-124">Per ulteriori informazioni sul recupero di intervalli di valori di attributo con [System. DirectoryServices](/dotnet/api/system.directoryservices), vedere [enumerazione di membri in un gruppo di grandi dimensioni](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="36a72-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 