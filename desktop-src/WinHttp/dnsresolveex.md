---
description: Risolvere una stringa host nell'indirizzo IP
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: dnsResolveEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1c63ba3e20653c41864394d9c563c851f2aab5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316010"
---
# <a name="dnsresolveex-function"></a><span data-ttu-id="8aad9-103">dnsResolveEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="8aad9-103">dnsResolveEx function</span></span>

<span data-ttu-id="8aad9-104">Risolvere una stringa host nell'indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="8aad9-104">Resolve a host string to its IP address</span></span>

## <a name="parameters"></a><span data-ttu-id="8aad9-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8aad9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aad9-106">*host*</span><span class="sxs-lookup"><span data-stu-id="8aad9-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="8aad9-107">Stringa contenente l'host HTTP fornito a FindProxyForUrl.</span><span class="sxs-lookup"><span data-stu-id="8aad9-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aad9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8aad9-108">Return value</span></span>

<span data-ttu-id="8aad9-109">Stringa delimitata da punto e virgola contenente indirizzi IPv6 e IPv4 o una stringa vuota se l'host non è risolvibile.</span><span class="sxs-lookup"><span data-stu-id="8aad9-109">A semi-colon delimited string containing IPv6 and IPv4 addresses or an empty string if host is not resolvable.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aad9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8aad9-110">Remarks</span></span>

<span data-ttu-id="8aad9-111">Gli implementatori di FindProxyforURLEx devono aggiungere codice che suddivide la stringa di indirizzi IP delimitati da punto e virgola in indirizzi distinti.</span><span class="sxs-lookup"><span data-stu-id="8aad9-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="8aad9-112">Esempi</span><span class="sxs-lookup"><span data-stu-id="8aad9-112">Examples</span></span>

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a><span data-ttu-id="8aad9-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8aad9-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aad9-114">Definizioni API helper proxy compatibili con IPv6</span><span class="sxs-lookup"><span data-stu-id="8aad9-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="8aad9-115">Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione</span><span class="sxs-lookup"><span data-stu-id="8aad9-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



