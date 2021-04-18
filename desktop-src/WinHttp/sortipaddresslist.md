---
description: Ordina un elenco di indirizzi IP.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: sortIpAddressList (funzione)
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
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305582"
---
# <a name="sortipaddresslist-function"></a><span data-ttu-id="2b803-103">sortIpAddressList (funzione)</span><span class="sxs-lookup"><span data-stu-id="2b803-103">sortIpAddressList function</span></span>

<span data-ttu-id="2b803-104">Ordina un elenco di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="2b803-104">Sorts a list of IP addresses.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b803-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b803-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b803-106">*IpAddress*</span><span class="sxs-lookup"><span data-stu-id="2b803-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="2b803-107">Stringa delimitata da punto e virgola contenente indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="2b803-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b803-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b803-108">Return value</span></span>

<span data-ttu-id="2b803-109">Elenco di indirizzi IP delimitati da punti e virgola o una stringa vuota se non è possibile ordinare l'elenco di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="2b803-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b803-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b803-110">Remarks</span></span>

<span data-ttu-id="2b803-111">Gli implementatori di FindProxyforURLEx devono aggiungere codice che suddivide la stringa di indirizzi IP delimitati da punto e virgola in indirizzi distinti.</span><span class="sxs-lookup"><span data-stu-id="2b803-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="2b803-112">Esempi</span><span class="sxs-lookup"><span data-stu-id="2b803-112">Examples</span></span>

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a><span data-ttu-id="2b803-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2b803-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b803-114">Definizioni API helper proxy compatibili con IPv6</span><span class="sxs-lookup"><span data-stu-id="2b803-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="2b803-115">Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione</span><span class="sxs-lookup"><span data-stu-id="2b803-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



