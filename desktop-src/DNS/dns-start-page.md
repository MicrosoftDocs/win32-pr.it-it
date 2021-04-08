---
title: Domain Name System
description: Domain Name System (DNS), un servizio di localizzazione in Microsoft Windows, è un protocollo standard del settore che individua i computer in una rete basata su IP.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS (vedere Domain Name System)
- Domain Name System
- Domain Name System, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104058578"
---
# <a name="domain-name-system"></a><span data-ttu-id="71ed7-107">Domain Name System</span><span class="sxs-lookup"><span data-stu-id="71ed7-107">Domain Name System</span></span>

## <a name="purpose"></a><span data-ttu-id="71ed7-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="71ed7-108">Purpose</span></span>

<span data-ttu-id="71ed7-109">Domain Name System (DNS), un servizio di localizzazione in Microsoft Windows, è un protocollo standard del settore che individua i computer in una rete basata su IP.</span><span class="sxs-lookup"><span data-stu-id="71ed7-109">Domain Name System (DNS), a locator service in Microsoft Windows, is an industry-standard protocol that locates computers on an IP-based network.</span></span> <span data-ttu-id="71ed7-110">Le reti IP, ad esempio le reti Internet e Windows, si basano su indirizzi numerici per elaborare i dati.</span><span class="sxs-lookup"><span data-stu-id="71ed7-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to process data.</span></span> <span data-ttu-id="71ed7-111">Gli utenti, tuttavia, possono ricordare più facilmente gli indirizzi dei nomi, pertanto è necessario convertire i nomi descrittivi (ad esempio `www.microsoft.com` ) in indirizzi che la rete è in grado di riconoscere (ad esempio 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="71ed7-111">Users however, can more easily remember name addresses, so it is necessary to translate user-friendly names (such as `www.microsoft.com`) into addresses that the network can recognize (such as 207.46.131.137).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="71ed7-112">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="71ed7-112">Where applicable</span></span>

<span data-ttu-id="71ed7-113">Windows e Active Directory utilizzano DNS.</span><span class="sxs-lookup"><span data-stu-id="71ed7-113">Windows and Active Directory use DNS.</span></span> <span data-ttu-id="71ed7-114">DNS è il servizio localizzatore primario per Internet e Active Directory e pertanto DNS è considerato un servizio di base per Windows e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71ed7-114">DNS is the primary locator service for the Internet and Active Directory, and therefore, DNS is considered a base service for Windows and Active Directory.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="71ed7-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="71ed7-115">Developer audience</span></span>

<span data-ttu-id="71ed7-116">Windows fornisce funzioni che consentono ai programmatori di applicazioni di usare DNS, ad esempio query DNS a livello di codice, confronto tra record e ricerca nome.</span><span class="sxs-lookup"><span data-stu-id="71ed7-116">Windows provides functions that enable application programmers to use DNS, such as programmatic DNS query, record compare, and name lookup.</span></span>

<span data-ttu-id="71ed7-117">I componenti DNS programmabili sono progettati per l'uso da programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="71ed7-117">Programmable DNS components are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="71ed7-118">È necessaria una certa familiarità con le funzionalità di rete e DNS.</span><span class="sxs-lookup"><span data-stu-id="71ed7-118">Familiarity with networking and DNS is required.</span></span> <span data-ttu-id="71ed7-119">I programmatori devono conoscere la suite di protocolli IP, nonché il protocollo DNS e le operazioni DNS.</span><span class="sxs-lookup"><span data-stu-id="71ed7-119">Programmers should be familiar with the IP-protocol suite, as well as the DNS protocol and DNS operations.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="71ed7-120">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="71ed7-120">Run-time requirements</span></span>

<span data-ttu-id="71ed7-121">DNS viene usato in tutte le reti IP che richiedono un servizio localizzatore compatibile con Internet.</span><span class="sxs-lookup"><span data-stu-id="71ed7-121">DNS is used on all IP networks that require an Internet-compatible locator service.</span></span> <span data-ttu-id="71ed7-122">Tuttavia, l'API DNS richiede Windows 2000 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="71ed7-122">However, the DNS API requires Windows 2000 or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="71ed7-123">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="71ed7-123">In this section</span></span>



| <span data-ttu-id="71ed7-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="71ed7-124">Topic</span></span>                                                             | <span data-ttu-id="71ed7-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71ed7-125">Description</span></span>                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="71ed7-126">Documenti standard DNS</span><span class="sxs-lookup"><span data-stu-id="71ed7-126">DNS Standards Documents</span></span>](dns-standards-documents.md)<br/> | <span data-ttu-id="71ed7-127">Collegamenti ai documenti degli standard DNS pubblici.</span><span class="sxs-lookup"><span data-stu-id="71ed7-127">Links to public DNS standards documents.</span></span><br/>                                  |
| [<span data-ttu-id="71ed7-128">Informazioni su DNS</span><span class="sxs-lookup"><span data-stu-id="71ed7-128">About DNS</span></span>](about-dns.md)<br/>                             | <span data-ttu-id="71ed7-129">Informazioni generali sul DNS.</span><span class="sxs-lookup"><span data-stu-id="71ed7-129">General information about DNS.</span></span><br/>                                            |
| [<span data-ttu-id="71ed7-130">Riferimento DNS</span><span class="sxs-lookup"><span data-stu-id="71ed7-130">DNS Reference</span></span>](dns-reference.md)<br/>                     | <span data-ttu-id="71ed7-131">Documentazione di riferimento per DNS.</span><span class="sxs-lookup"><span data-stu-id="71ed7-131">Reference documentation for DNS.</span></span><br/>                                          |
| [<span data-ttu-id="71ed7-132">Provider WMI DNS</span><span class="sxs-lookup"><span data-stu-id="71ed7-132">DNS WMI Provider</span></span>](dns-wmi-provider.md)<br/>               | <span data-ttu-id="71ed7-133">Informazioni generali e documentazione di riferimento per il provider WMI DNS.</span><span class="sxs-lookup"><span data-stu-id="71ed7-133">General information and reference documentation for the DNS WMI provider.</span></span><br/> |
| [<span data-ttu-id="71ed7-134">Glossario</span><span class="sxs-lookup"><span data-stu-id="71ed7-134">Glossary</span></span>](glossary-gly.md)<br/>                           | <span data-ttu-id="71ed7-135">Glossario dei termini e delle definizioni DNS.</span><span class="sxs-lookup"><span data-stu-id="71ed7-135">Glossary of DNS terms and definitions.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="71ed7-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71ed7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ed7-137">DHCP</span><span class="sxs-lookup"><span data-stu-id="71ed7-137">DHCP</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="71ed7-138">Helper protocollo Internet</span><span class="sxs-lookup"><span data-stu-id="71ed7-138">Internet Protocol Helper</span></span>](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

<span data-ttu-id="71ed7-139">[Servizi directory](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="71ed7-139">[Directory Services](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span></span>
</dt> </dl>

 

