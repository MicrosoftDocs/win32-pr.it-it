---
title: delete iplisten
description: Specifica un indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- Elimina HTTP iplisten
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104045969"
---
# <a name="delete-iplisten"></a><span data-ttu-id="116cb-104">delete iplisten</span><span class="sxs-lookup"><span data-stu-id="116cb-104">delete iplisten</span></span>

<span data-ttu-id="116cb-105">Specifica un indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.</span><span class="sxs-lookup"><span data-stu-id="116cb-105">Specifies an IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="116cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="116cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="116cb-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ Address = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="116cb-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[address=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="116cb-108">Specifica l'indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.</span><span class="sxs-lookup"><span data-stu-id="116cb-108">Specifies the IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="116cb-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="116cb-109">Remarks</span></span>

<span data-ttu-id="116cb-110">Elimina un indirizzo IP nell'elenco di ascolto IP.</span><span class="sxs-lookup"><span data-stu-id="116cb-110">Deletes an IP address to the IP listen list.</span></span> <span data-ttu-id="116cb-111">Il numero di porta non è incluso.</span><span class="sxs-lookup"><span data-stu-id="116cb-111">This does not include the port number.</span></span> <span data-ttu-id="116cb-112">Questo elenco viene usato per definire l'ambito dell'elenco di indirizzi a cui viene eseguito il binding del servizio HTTP.</span><span class="sxs-lookup"><span data-stu-id="116cb-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="116cb-113">"0.0.0.0" indica qualsiasi indirizzo IPv4 e "::" indica qualsiasi indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="116cb-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="116cb-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="116cb-114">Examples</span></span>

<span data-ttu-id="116cb-115">**Elimina indirizzo iplisten = FE80:: 1**</span><span class="sxs-lookup"><span data-stu-id="116cb-115">**delete iplisten address=fe80::1**</span></span>

<span data-ttu-id="116cb-116">**Elimina indirizzo iplisten = 1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="116cb-116">**delete iplisten address=1.1.1.1**</span></span>

<span data-ttu-id="116cb-117">**Elimina indirizzo iplisten = 0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="116cb-117">**delete iplisten address=0.0.0.0**</span></span>

<span data-ttu-id="116cb-118">**Elimina indirizzo iplisten =::**</span><span class="sxs-lookup"><span data-stu-id="116cb-118">**delete iplisten address=::**</span></span>

 

 




