---
description: Specifica un prefisso collegato all'interfaccia \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefissi di sito IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306900"
---
# <a name="ipv6-site-prefixes"></a><span data-ttu-id="0e771-103">Prefissi di sito IPv6</span><span class="sxs-lookup"><span data-stu-id="0e771-103">IPv6 Site Prefixes</span></span>

<span data-ttu-id="0e771-104">Il comando RTU IPv6 consente la configurazione dei prefissi di collegamento pubblicati con una lunghezza del prefisso del sito.</span><span class="sxs-lookup"><span data-stu-id="0e771-104">The ipv6 rtu command allows published on-link prefixes to be configured with a site prefix length.</span></span> <span data-ttu-id="0e771-105">Se specificato, la lunghezza del prefisso del sito viene inserita in un'opzione di informazioni sul prefisso negli annunci router.</span><span class="sxs-lookup"><span data-stu-id="0e771-105">If specified, the site prefix length is put into a prefix information option in router advertisements.</span></span> <span data-ttu-id="0e771-106">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="0e771-106">For example:</span></span>

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

<span data-ttu-id="0e771-107">Specifica un prefisso collegato all'interfaccia \# 4.</span><span class="sxs-lookup"><span data-stu-id="0e771-107">specifies a prefix that is on-link to interface \#4.</span></span> <span data-ttu-id="0e771-108">Il prefisso viene pubblicato, vale a dire che è incluso negli annunci router se l'interfaccia \# 4 è un'interfaccia pubblicitaria.</span><span class="sxs-lookup"><span data-stu-id="0e771-108">The prefix is published, meaning that it is included in router advertisements if interface \#4 is an advertising interface.</span></span> <span data-ttu-id="0e771-109">La durata nell'opzione informazioni sul prefisso è di 1800 secondi (30 minuti).</span><span class="sxs-lookup"><span data-stu-id="0e771-109">The lifetime in the prefix information option is 1800 seconds (30 minutes).</span></span> <span data-ttu-id="0e771-110">La lunghezza del prefisso del sito nell'opzione informazioni sul prefisso è 48.</span><span class="sxs-lookup"><span data-stu-id="0e771-110">The site prefix length in the prefix information option is 48.</span></span>

<span data-ttu-id="0e771-111">La ricezione di un'opzione di informazioni sul prefisso che specifica un prefisso del sito determina la creazione di una voce nella tabella dei prefissi del sito, che può essere visualizzata tramite il comando IPv6 SPT.</span><span class="sxs-lookup"><span data-stu-id="0e771-111">The receipt of a prefix information option that specifies a site prefix causes an entry to be created in the site prefix table, which can be displayed by using the ipv6 spt command.</span></span> <span data-ttu-id="0e771-112">La tabella dei prefissi del sito viene usata per rimuovere gli indirizzi locali del sito non appropriati da quelli restituiti da [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e dalle funzioni correlate.</span><span class="sxs-lookup"><span data-stu-id="0e771-112">The site prefix table is used to remove inappropriate site-local addresses from those returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and related functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e771-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e771-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e771-114">Collegamento IPv6-indirizzi locali e locali del sito</span><span class="sxs-lookup"><span data-stu-id="0e771-114">IPv6 Link-local and Site-local Addresses</span></span>](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="0e771-115">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="0e771-115">Netsh.exe</span></span>](netsh-exe.md)
</dt> </dl>

 

 



