---
title: add iplisten
description: Specifica un indirizzo IPv4 o IPv6 da aggiungere all'elenco di ascolto IP.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Aggiungi iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "103956241"
---
# <a name="add-iplisten"></a><span data-ttu-id="452d4-104">add iplisten</span><span class="sxs-lookup"><span data-stu-id="452d4-104">add iplisten</span></span>

<span data-ttu-id="452d4-105">Specifica un indirizzo IPv4 o IPv6 da aggiungere all'elenco di ascolto IP.</span><span class="sxs-lookup"><span data-stu-id="452d4-105">Specifies an IPv4 or IPv6 address to be added to the IP listen list.</span></span>

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="452d4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="452d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="452d4-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="452d4-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="452d4-108">Specifica l'indirizzo IPv4 o IPv6 da aggiungere all'elenco di ascolto IP.</span><span class="sxs-lookup"><span data-stu-id="452d4-108">Specifies the IPv4 or IPv6 address to be added to the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="452d4-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="452d4-109">Remarks</span></span>

<span data-ttu-id="452d4-110">Aggiunge un nuovo indirizzo IP all'elenco di ascolto IP.</span><span class="sxs-lookup"><span data-stu-id="452d4-110">Adds a new IP address to the IP listen list.</span></span> <span data-ttu-id="452d4-111">Il numero di porta non è incluso.</span><span class="sxs-lookup"><span data-stu-id="452d4-111">This does not include the port number.</span></span> <span data-ttu-id="452d4-112">Questo elenco viene usato per definire l'ambito dell'elenco di indirizzi a cui viene eseguito il binding del servizio HTTP.</span><span class="sxs-lookup"><span data-stu-id="452d4-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="452d4-113">"0.0.0.0" indica qualsiasi indirizzo IPv4 e "::" indica qualsiasi indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="452d4-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="452d4-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="452d4-114">Examples</span></span>

<span data-ttu-id="452d4-115">**add iplisten ipaddress=fe80::1**</span><span class="sxs-lookup"><span data-stu-id="452d4-115">**add iplisten ipaddress=fe80::1**</span></span>

<span data-ttu-id="452d4-116">**add iplisten ipaddress=1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="452d4-116">**add iplisten ipaddress=1.1.1.1**</span></span>

<span data-ttu-id="452d4-117">**add iplisten ipaddress=0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="452d4-117">**add iplisten ipaddress=0.0.0.0**</span></span>

<span data-ttu-id="452d4-118">**add iplisten ipaddress=::**</span><span class="sxs-lookup"><span data-stu-id="452d4-118">**add iplisten ipaddress=::**</span></span>

 

 




