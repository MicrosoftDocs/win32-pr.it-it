---
description: Determina se una determinata stringa host può essere risolta in un indirizzo IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isResolvableEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317011"
---
# <a name="isresolvableex-function"></a><span data-ttu-id="29940-103">isResolvableEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="29940-103">isResolvableEx function</span></span>

<span data-ttu-id="29940-104">Determina se una determinata stringa host può essere risolta in un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="29940-104">Determines if a given host string can resolve to an IP address.</span></span>

## <a name="parameters"></a><span data-ttu-id="29940-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="29940-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29940-106">*host*</span><span class="sxs-lookup"><span data-stu-id="29940-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="29940-107">Stringa contenente l'host HTTP fornito a FindProxyForUrl.</span><span class="sxs-lookup"><span data-stu-id="29940-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29940-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29940-108">Return value</span></span>

<span data-ttu-id="29940-109">TRUE se l'host è risolvibile in un indirizzo IPv4 o IPv6. in caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="29940-109">TRUE if the host is resolvable to a IPv4 or IPv6 address; otherwise, FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="29940-110">Esempi</span><span class="sxs-lookup"><span data-stu-id="29940-110">Examples</span></span>

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a><span data-ttu-id="29940-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="29940-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29940-112">Definizioni API helper proxy compatibili con IPv6</span><span class="sxs-lookup"><span data-stu-id="29940-112">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="29940-113">Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione</span><span class="sxs-lookup"><span data-stu-id="29940-113">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



