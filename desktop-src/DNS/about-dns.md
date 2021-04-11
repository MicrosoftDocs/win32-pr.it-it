---
title: Informazioni su DNS
description: Domain Name System (DNS) è un protocollo standard del settore usato per individuare i computer in una rete basata su IP. Gli utenti possono ricordare i nomi visualizzati, ad esempio www.microsoft.com più semplici degli indirizzi basati su numeri, ad esempio 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Informazioni sul DNS Domain Name System
- Domain Name System DNS, informazioni
- Domain Name System DNS, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234910"
---
# <a name="about-dns"></a><span data-ttu-id="95816-107">Informazioni su DNS</span><span class="sxs-lookup"><span data-stu-id="95816-107">About DNS</span></span>

<span data-ttu-id="95816-108">Domain Name System (DNS) è un protocollo standard del settore usato per individuare i computer in una rete basata su IP.</span><span class="sxs-lookup"><span data-stu-id="95816-108">Domain Name System (DNS) is an industry-standard protocol used to locate computers on an IP-based network.</span></span> <span data-ttu-id="95816-109">Gli utenti possono ricordare i nomi visualizzati, ad esempio `www.microsoft.com` gli indirizzi basati sui numeri, ad esempio 207.46.131.137.</span><span class="sxs-lookup"><span data-stu-id="95816-109">Users can remember display names, such as `www.microsoft.com` easier than number-based addresses, such as 207.46.131.137.</span></span>

<span data-ttu-id="95816-110">Le reti IP, ad esempio le reti Internet e Windows, si basano sugli indirizzi numerici per trasmettere i dati in tutta la rete. è pertanto necessario convertire i nomi visualizzati, ad esempio, `www.microsoft.com` in indirizzi numerici che la rete è in grado di riconoscere, ad esempio 207.46.131.137.</span><span class="sxs-lookup"><span data-stu-id="95816-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to transmit data throughout the network; therefore, it is necessary to translate display names (such as `www.microsoft.com`) into numeric addresses that the network can recognize (such as 207.46.131.137).</span></span> <span data-ttu-id="95816-111">DNS è il servizio da scegliere in Windows per individuare tali risorse e convertirle in indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="95816-111">DNS is the service of choice in Windows to locate such resources and translate them into IP addresses.</span></span>

<span data-ttu-id="95816-112">DNS è il servizio localizzatore primario per Active Directory e pertanto DNS può essere considerato un servizio di base per Windows e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="95816-112">DNS is the primary locator service for Active Directory, and therefore, DNS can be considered a base service for both Windows and Active Directory.</span></span> <span data-ttu-id="95816-113">Windows fornisce funzioni che consentono ai programmatori di applicazioni di usare funzioni DNS quali la creazione di query DNS a livello di codice, il confronto di record e la ricerca di nomi.</span><span class="sxs-lookup"><span data-stu-id="95816-113">Windows provides functions that enable application programmers to use DNS functions such as programmatically making DNS queries, comparing records, and looking up names.</span></span>

<span data-ttu-id="95816-114">Molte funzioni DNS sono in realtà tipi di funzione, in quanto è presente un nome di base per la funzione, ma il suo utilizzo dipende dalla codifica dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="95816-114">Many DNS functions are actually function types, in that there is a base name for the function, but its use depends on character encoding.</span></span> <span data-ttu-id="95816-115">La funzione [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) , ad esempio, è elencata nel riferimento alla funzione dell'API (Application Programming Interface) DNS come **DnsQuery**, tuttavia, l'uso nelle applicazioni varia a seconda che la codifica dei caratteri sia ANSI (designata mediante l'aggiunta di \_ un oggetto al nome del tipo di funzione), Unicode (designata aggiungendo \_ W al nome del tipo di funzione) o UTF-8 (designato aggiungendo \_ UTF al nome del tipo di funzione).</span><span class="sxs-lookup"><span data-stu-id="95816-115">For example, the [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) function is listed in the function reference of the DNS Application Programming Interface (API) as **DnsQuery**, but its use in applications depends on whether the character encoding is ANSI (designated by appending \_A to the function type name), Unicode (designated by appending \_W to the function type name), or UTF-8 (designated by appending \_UTF to the function type name).</span></span> <span data-ttu-id="95816-116">Pertanto, la chiamata di funzione per la funzione **DnsQuery** è in realtà una delle seguenti:</span><span class="sxs-lookup"><span data-stu-id="95816-116">Therefore, the function call for the **DnsQuery** function would actually be one of the following:</span></span>

<span data-ttu-id="95816-117">DnsQuery \_ a ( \_ a per la codifica ANSI)</span><span class="sxs-lookup"><span data-stu-id="95816-117">DnsQuery\_A (\_A for ANSI encoding)</span></span>

<span data-ttu-id="95816-118">DnsQuery \_ w ( \_ w per codifica Unicode)</span><span class="sxs-lookup"><span data-stu-id="95816-118">DnsQuery\_W (\_W for Unicode encoding)</span></span>

<span data-ttu-id="95816-119">DnsQuery \_ UTF8 ( \_ UTF8 per codifica UTF-8)</span><span class="sxs-lookup"><span data-stu-id="95816-119">DnsQuery\_UTF8 (\_UTF8 for UTF-8 encoding)</span></span>

<span data-ttu-id="95816-120">Tutte le funzioni che richiedono questa convenzione indicano chiaramente questo requisito entro le prime frasi della definizione di funzione.</span><span class="sxs-lookup"><span data-stu-id="95816-120">All functions that require this convention clearly state this requirement within the first few sentences of their function definition.</span></span> <span data-ttu-id="95816-121">Usare il nome della funzione appropriato. ad esempio, non è possibile chiamare semplicemente [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) anziché DnsQuery \_ A.</span><span class="sxs-lookup"><span data-stu-id="95816-121">Use the proper function name; for example, you cannot simply call [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) instead of DnsQuery\_A.</span></span>

 

 




