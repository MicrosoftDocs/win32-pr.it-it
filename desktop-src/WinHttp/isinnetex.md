---
description: Determina se un indirizzo IP si trova in una subnet specifica.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isInNetEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317015"
---
# <a name="isinnetex-function"></a><span data-ttu-id="4a0c4-103">isInNetEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="4a0c4-103">isInNetEx function</span></span>

<span data-ttu-id="4a0c4-104">Determina se un indirizzo IP si trova in una subnet specifica.</span><span class="sxs-lookup"><span data-stu-id="4a0c4-104">Determines if an IP address is in a specific subnet.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a0c4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a0c4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a0c4-106">*IPaddress*</span><span class="sxs-lookup"><span data-stu-id="4a0c4-106">*IPaddress*</span></span> 
</dt> <dd>

<span data-ttu-id="4a0c4-107">Stringa contenente indirizzi IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="4a0c4-107">A string containing IPv6/IPv4 addresses.</span></span>

</dd> <dt>

<span data-ttu-id="4a0c4-108">*IPprefix*</span><span class="sxs-lookup"><span data-stu-id="4a0c4-108">*IPprefix*</span></span> 
</dt> <dd>

<span data-ttu-id="4a0c4-109">Stringa che contiene il prefisso IP delimitato da due punti con i primi n bit specificati nel campo di bit, ad esempio 3ffe: 8311: ffff::/48 o 123.112.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="4a0c4-109">A string containing colon delimited IP prefix with top n bits specified in the bit field (i.e. 3ffe:8311:ffff::/48 or 123.112.0.0/16).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a0c4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a0c4-110">Return value</span></span>

<span data-ttu-id="4a0c4-111">TRUE se l'host si trova nella stessa subnet. in caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="4a0c4-111">TRUE if the host is in the same subnet; otherwise, FALSE.</span></span>

<span data-ttu-id="4a0c4-112">Restituisce anche FALSE se il prefisso non è nel formato corretto o se nel confronto vengono utilizzati indirizzi e prefissi di tipi diversi, ad esempio un prefisso IPv4 e un indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="4a0c4-112">Also returns FALSE if the prefix is not in the correct format or if addresses and prefixes of different types are used in the comparison (i.e. IPv4 prefix and an IPv6 address).</span></span>

## <a name="examples"></a><span data-ttu-id="4a0c4-113">Esempi</span><span class="sxs-lookup"><span data-stu-id="4a0c4-113">Examples</span></span>

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a><span data-ttu-id="4a0c4-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4a0c4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a0c4-115">Definizioni API helper proxy compatibili con IPv6</span><span class="sxs-lookup"><span data-stu-id="4a0c4-115">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="4a0c4-116">Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione</span><span class="sxs-lookup"><span data-stu-id="4a0c4-116">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



