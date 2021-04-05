---
title: Record di risorse
description: Un record di risorse, noto come RR, è l'unità di immissione di informazioni nei file di zona DNS. RRs sono i blocchi predefiniti di base del nome host e le informazioni IP e vengono usati per risolvere tutte le query DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712799"
---
# <a name="resource-records"></a><span data-ttu-id="ee10b-103">Record di risorse</span><span class="sxs-lookup"><span data-stu-id="ee10b-103">Resource Records</span></span>

<span data-ttu-id="ee10b-104">Un record di risorse, noto come RR, è l'unità di immissione di informazioni nei file di zona DNS. RRs sono i blocchi predefiniti di base del nome host e le informazioni IP e vengono usati per risolvere tutte le query DNS.</span><span class="sxs-lookup"><span data-stu-id="ee10b-104">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="ee10b-105">I record di risorse esistono come molti tipi per offrire servizi estesi per la risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ee10b-105">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="ee10b-106">Diversi tipi di RRs hanno formati diversi, poiché contengono dati diversi.</span><span class="sxs-lookup"><span data-stu-id="ee10b-106">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="ee10b-107">In generale, tuttavia, molti RRs condividono un formato comune, come illustrato nell'esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="ee10b-107">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="ee10b-108">Nell'esempio fittizio riportato di seguito vengono illustrati i campi presenti in un record di risorse:</span><span class="sxs-lookup"><span data-stu-id="ee10b-108">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="ee10b-109">Il primo campo (microsoft.com) indica il proprietario.</span><span class="sxs-lookup"><span data-stu-id="ee10b-109">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="ee10b-110">Il secondo campo (600) è il parametro TTL (time-to-Live), in secondi.</span><span class="sxs-lookup"><span data-stu-id="ee10b-110">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="ee10b-111">Il terzo campo (IN) è il campo della classe che rappresenta la famiglia di protocolli, che è quasi sempre IN, per la classe Internet.</span><span class="sxs-lookup"><span data-stu-id="ee10b-111">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="ee10b-112">Il quarto campo (A) è il tipo di risorsa che rappresenta l'RR.</span><span class="sxs-lookup"><span data-stu-id="ee10b-112">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="ee10b-113">Il quinto campo (150.150.150.1) è i dati della risorsa, o RDATA.</span><span class="sxs-lookup"><span data-stu-id="ee10b-113">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="ee10b-114">Questo campo è un tipo di variabile che fornisce le informazioni appropriate per il tipo di risorsa. in questo caso, si tratta di un indirizzo IP a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ee10b-114">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="ee10b-115">I tipi di record di risorse seguenti sono comunemente usati in DNS:</span><span class="sxs-lookup"><span data-stu-id="ee10b-115">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="ee10b-116">Inizio dell'autorità (SOA)</span><span class="sxs-lookup"><span data-stu-id="ee10b-116">Start of authority (SOA)</span></span>
-   <span data-ttu-id="ee10b-117">Server del nome (NS)</span><span class="sxs-lookup"><span data-stu-id="ee10b-117">Name server (NS)</span></span>
-   <span data-ttu-id="ee10b-118">[*Record puntatore*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="ee10b-118">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="ee10b-119">Indirizzo (A)</span><span class="sxs-lookup"><span data-stu-id="ee10b-119">Address (A)</span></span>
-   <span data-ttu-id="ee10b-120">Indirizzo IPv6 (AAAA)</span><span class="sxs-lookup"><span data-stu-id="ee10b-120">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="ee10b-121">Mail Exchange (MX)</span><span class="sxs-lookup"><span data-stu-id="ee10b-121">Mail exchange (MX)</span></span>
-   <span data-ttu-id="ee10b-122">[*Nome canonico*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="ee10b-122">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="ee10b-123">Windows Internet Naming Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="ee10b-123">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="ee10b-124">Ricerca inversa WINS (WINSr)</span><span class="sxs-lookup"><span data-stu-id="ee10b-124">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="ee10b-125">Sono disponibili molti altri tipi di record di risorse in DNS.</span><span class="sxs-lookup"><span data-stu-id="ee10b-125">There are many other resource record types in DNS.</span></span> <span data-ttu-id="ee10b-126">Per ulteriori informazioni, vedere [riferimento del provider WMI DNS](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee10b-126">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




