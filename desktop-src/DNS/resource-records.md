---
title: Record di risorse
description: Informazioni sui record di risorse. Un record di risorse è l'unità di immissione di informazioni nei file di zona DNS, usata per risolvere tutte le query DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010674"
---
# <a name="resource-records"></a><span data-ttu-id="550e5-104">Record di risorse</span><span class="sxs-lookup"><span data-stu-id="550e5-104">Resource Records</span></span>

<span data-ttu-id="550e5-105">Un record di risorse, comunemente noto come RR, è l'unità di immissione di informazioni nei file di zona DNS; Le richieste riservate sono i blocchi predefiniti di base delle informazioni su nome host e IP e vengono usate per risolvere tutte le query DNS.</span><span class="sxs-lookup"><span data-stu-id="550e5-105">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="550e5-106">I record di risorse esistono tutti i tipi per fornire servizi estesi di risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="550e5-106">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="550e5-107">Tipi diversi di RR hanno formati diversi, in quanto contengono dati diversi.</span><span class="sxs-lookup"><span data-stu-id="550e5-107">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="550e5-108">In generale, tuttavia, molte RR condividono un formato comune, come illustrato nell'esempio di record di risorse di indirizzo seguente.</span><span class="sxs-lookup"><span data-stu-id="550e5-108">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="550e5-109">L'esempio fittizio seguente illustra i campi trovati in un record di risorse A:</span><span class="sxs-lookup"><span data-stu-id="550e5-109">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="550e5-110">Il primo campo (microsoft.com) indica il proprietario.</span><span class="sxs-lookup"><span data-stu-id="550e5-110">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="550e5-111">Il secondo campo (600) è il parametro della durata (TTL), espresso in secondi.</span><span class="sxs-lookup"><span data-stu-id="550e5-111">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="550e5-112">Il terzo campo (IN) è il campo della classe che rappresenta la famiglia di protocolli, che è quasi sempre IN, per la classe Internet.</span><span class="sxs-lookup"><span data-stu-id="550e5-112">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="550e5-113">Il quarto campo (A) è il tipo di risorsa rappresentato da RR.</span><span class="sxs-lookup"><span data-stu-id="550e5-113">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="550e5-114">Il quinto campo (150.150.150.1) sono i dati delle risorse o RDATA.</span><span class="sxs-lookup"><span data-stu-id="550e5-114">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="550e5-115">Questo campo è un tipo di variabile che fornisce informazioni appropriate per il tipo di risorsa. In questo caso, si tratta di un indirizzo IP a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="550e5-115">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="550e5-116">In DNS vengono comunemente usati i tipi di record di risorse seguenti:</span><span class="sxs-lookup"><span data-stu-id="550e5-116">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="550e5-117">Inizio dell'autorità (SOA)</span><span class="sxs-lookup"><span data-stu-id="550e5-117">Start of authority (SOA)</span></span>
-   <span data-ttu-id="550e5-118">Server dei nomi (NS)</span><span class="sxs-lookup"><span data-stu-id="550e5-118">Name server (NS)</span></span>
-   <span data-ttu-id="550e5-119">[*Record puntatore*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="550e5-119">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="550e5-120">Indirizzo (A)</span><span class="sxs-lookup"><span data-stu-id="550e5-120">Address (A)</span></span>
-   <span data-ttu-id="550e5-121">Indirizzo IPv6 (AAAA)</span><span class="sxs-lookup"><span data-stu-id="550e5-121">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="550e5-122">Mail exchange (MX)</span><span class="sxs-lookup"><span data-stu-id="550e5-122">Mail exchange (MX)</span></span>
-   <span data-ttu-id="550e5-123">[*Nome canonico*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="550e5-123">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="550e5-124">Windows Internet Naming Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="550e5-124">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="550e5-125">Wins Reverse Look up (WINSR)</span><span class="sxs-lookup"><span data-stu-id="550e5-125">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="550e5-126">In DNS sono disponibili molti altri tipi di record di risorse.</span><span class="sxs-lookup"><span data-stu-id="550e5-126">There are many other resource record types in DNS.</span></span> <span data-ttu-id="550e5-127">Per altre informazioni, vedere [Dns WMI Provider Reference](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="550e5-127">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




