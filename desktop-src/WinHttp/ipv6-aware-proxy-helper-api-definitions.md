---
description: Per sfruttare i vantaggi delle funzioni abilitate per IPv6, gli amministratori IT devono definire all'interno del proprio script WPAD una funzione denominata FindProxyForURLEx (URL, host) che sostituisce la funzione FindProxyForUrl (URL, host) legacy.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: IPv6-Aware definizioni API helper proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317019"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a><span data-ttu-id="0593e-103">IPv6-Aware definizioni API helper proxy</span><span class="sxs-lookup"><span data-stu-id="0593e-103">IPv6-Aware Proxy Helper API Definitions</span></span>

<span data-ttu-id="0593e-104">Per sfruttare i vantaggi delle funzioni abilitate per IPv6, gli amministratori IT devono definire all'interno del proprio script WPAD una funzione denominata FindProxyForURLEx (URL, host) che sostituisce la funzione FindProxyForUrl (URL, host) legacy.</span><span class="sxs-lookup"><span data-stu-id="0593e-104">In order to take advantage of the IPv6 enabled functions, IT administrators must define within their WPAD script, a function called FindProxyForURLEx (url, host) which will replace the legacy FindProxyForUrl (url, host) function.</span></span> <span data-ttu-id="0593e-105">Solo dalla nuova funzione FindProxyForURLEx gli amministratori saranno in grado di eseguire le nuove funzioni.</span><span class="sxs-lookup"><span data-stu-id="0593e-105">Only from the new FindProxyForURLEx function will administrators be able to execute the new functions.</span></span>

<span data-ttu-id="0593e-106">Si è tentato anche di semplificare il lavoro per gli sviluppatori, allineando le funzioni in modo da restituire tipi diversi di indirizzi IP nello stesso ordine di preferenza degli altri componenti di rete, in particolare gli indirizzi IPv6 seguiti dagli indirizzi IPv4 (ovvero il comportamento corrente per la funzione funzione getaddrinfo (..) di Winsock.</span><span class="sxs-lookup"><span data-stu-id="0593e-106">We also attempted to simplify work for developers, by aligning our functions to return different types of IP addresses in the same order of preference as other networking components, specifically IPv6 addresses followed by IPv4 addresses (i.e. current behavior for Winsock’s getaddrinfo(..) function).</span></span>

<span data-ttu-id="0593e-107">Le funzioni seguenti sono estensioni per la [specifica del formato di file di Navigator proxy auto-config (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) per consentire agli script WPAD di gestire le reti compatibili con IPv6.</span><span class="sxs-lookup"><span data-stu-id="0593e-107">The following functions are extensions to the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) to enable WPAD scripts to handle IPv6 capable networks.</span></span>

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a><span data-ttu-id="0593e-108">Funzioni e ambiente predefiniti per la funzione JavaScript FindProxyforURLEx</span><span class="sxs-lookup"><span data-stu-id="0593e-108">Predefined Functions and Environment for the JavaScript Function FindProxyforURLEx</span></span>

<span data-ttu-id="0593e-109">Condizioni basate sul nome host</span><span class="sxs-lookup"><span data-stu-id="0593e-109">Hostname based conditions</span></span>

<dl> <dt>

[<span data-ttu-id="0593e-110">**isResolvableEx**</span><span class="sxs-lookup"><span data-stu-id="0593e-110">**isResolvableEx**</span></span>](isresolvableex.md)
</dt> <dd>

<span data-ttu-id="0593e-111">Determina se una determinata stringa host può essere risolta in un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="0593e-111">Determines if a given host string can resolve to an IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="0593e-112">**isInNetEx**</span><span class="sxs-lookup"><span data-stu-id="0593e-112">**isInNetEx**</span></span>](isinnetex.md)
</dt> <dd>

<span data-ttu-id="0593e-113">Determina se un indirizzo IP si trova in una subnet specifica.</span><span class="sxs-lookup"><span data-stu-id="0593e-113">Determines if an IP address is in a specific subnet.</span></span>

</dd> </dl>

<span data-ttu-id="0593e-114">Funzioni di utilità correlate</span><span class="sxs-lookup"><span data-stu-id="0593e-114">Related utility functions</span></span>

<dl> <dt>

[<span data-ttu-id="0593e-115">**dnsResolveEx**</span><span class="sxs-lookup"><span data-stu-id="0593e-115">**dnsResolveEx**</span></span>](dnsresolveex.md)
</dt> <dd>

<span data-ttu-id="0593e-116">Risolvere una stringa host nel relativo indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="0593e-116">Resolve a host string to its IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="0593e-117">**myIPAddressEx**</span><span class="sxs-lookup"><span data-stu-id="0593e-117">**myIPAddressEx**</span></span>](myipaddressex.md)
</dt> <dd>

<span data-ttu-id="0593e-118">Trova tutti gli indirizzi IP per localhost.</span><span class="sxs-lookup"><span data-stu-id="0593e-118">Finds all the IP addresses for localhost.</span></span>

</dd> <dt>

[<span data-ttu-id="0593e-119">**sortIpAddressList**</span><span class="sxs-lookup"><span data-stu-id="0593e-119">**sortIpAddressList**</span></span>](sortipaddresslist.md)
</dt> <dd>

<span data-ttu-id="0593e-120">Ordina un elenco di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="0593e-120">Sorts a list of IP addresses.</span></span>

</dd> <dt>

[<span data-ttu-id="0593e-121">**getClientVersion**</span><span class="sxs-lookup"><span data-stu-id="0593e-121">**getClientVersion**</span></span>](getclientversion.md)
</dt> <dd>

<span data-ttu-id="0593e-122">Ottiene la versione del motore di elaborazione WPAD.</span><span class="sxs-lookup"><span data-stu-id="0593e-122">Gets the version of the WPAD processing engine.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="0593e-123">Questa funzionalità richiede Windows Internet Explorer 7 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0593e-123">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



