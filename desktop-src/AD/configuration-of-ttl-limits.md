---
title: Configurazione dei limiti TTL
description: Un client può richiedere un valore TTL per una voce compresa tra 1 e 31557600, ovvero da 1 secondo a 1 anno.
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configurazione dei limiti TTL AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707195"
---
# <a name="configuration-of-ttl-limits"></a><span data-ttu-id="c2ba8-104">Configurazione dei limiti TTL</span><span class="sxs-lookup"><span data-stu-id="c2ba8-104">Configuration of TTL Limits</span></span>

<span data-ttu-id="c2ba8-105">Un client può richiedere un valore TTL per una voce compresa tra 1 e 31557600, ovvero da 1 secondo a 1 anno.</span><span class="sxs-lookup"><span data-stu-id="c2ba8-105">A client can request a TTL value for an entry ranging between 1 and 31557600 (that is, from 1 second to 1 year).</span></span> <span data-ttu-id="c2ba8-106">Questo intervallo di valori di attributo verrà applicato dai valori degli attributi **RangeLower** e **rangeUpper** nella definizione **attributeSchema** per l'attributo **entryTTL** .</span><span class="sxs-lookup"><span data-stu-id="c2ba8-106">This attribute value range will be enforced by the **rangeLower** and **rangeUpper** attribute values in the **attributeSchema** definition for the **entryTTL** attribute.</span></span> <span data-ttu-id="c2ba8-107">In base allo standard RFC 2589, non è necessario che i server di directory accettino questo valore e potrebbe restituire un valore TTL diverso al client.</span><span class="sxs-lookup"><span data-stu-id="c2ba8-107">As per RFC 2589, directory servers are not required to accept this value and might return a different TTL value to the client.</span></span> <span data-ttu-id="c2ba8-108">I client devono essere in grado di utilizzare questo valore dettato dal server come periodo di aggiornamento del client (CRP), che determina la frequenza con cui il client dovrà eseguire l'operazione di aggiornamento sulla voce dinamica.</span><span class="sxs-lookup"><span data-stu-id="c2ba8-108">Clients must be able to use this server-dictated value as their client refresh period (CRP) which will govern how often the client will need to perform the refresh operation on the dynamic entry.</span></span>

<span data-ttu-id="c2ba8-109">Active Directory Domain Services offrire agli amministratori la possibilità di configurare i valori TTL predefiniti e minimi per una foresta.</span><span class="sxs-lookup"><span data-stu-id="c2ba8-109">Active Directory Domain Services provide administrators with the ability to configure the default and minimum TTL values for a forest.</span></span> <span data-ttu-id="c2ba8-110">Il valore TTL predefinito è quello che verrà assegnato a una voce dinamica appena creata se non viene specificato in modo esplicito una durata (TTL).</span><span class="sxs-lookup"><span data-stu-id="c2ba8-110">The default TTL value is what will be assigned to a newly created dynamic entry if a TTL is not explicitly specified.</span></span> <span data-ttu-id="c2ba8-111">Il valore TTL minimo eseguirà l'override di qualsiasi valore TTL specificato dal client inferiore al minimo configurato.</span><span class="sxs-lookup"><span data-stu-id="c2ba8-111">The minimum TTL will override any client specified TTL value that is lower than the configured minimum.</span></span> <span data-ttu-id="c2ba8-112">Non è necessario fornire alcun valore TTL massimo configurabile perché un valore massimo verrà imposto dal valore dell'attributo **rangeUpper** nell'oggetto **attributeSchema** .</span><span class="sxs-lookup"><span data-stu-id="c2ba8-112">No configurable maximum TTL value needs to be provided because a maximum will be imposed by the **rangeUpper** attribute value in the **attributeSchema** object.</span></span> <span data-ttu-id="c2ba8-113">Consentendo agli amministratori di configurare questi valori, è possibile impostare i valori TTL che imporrà un traffico di aggiornamento basso o, all'altra estrema, fornire una directory altamente aggiornata.</span><span class="sxs-lookup"><span data-stu-id="c2ba8-113">Allowing administrators to configure these values will enable them to set TTL values which will enforce a low refresh traffic or, at the other extreme, provide a highly up-to-date directory.</span></span>

<span data-ttu-id="c2ba8-114">I valori predefiniti per i due parametri TTL configurabili saranno i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2ba8-114">The default values for the two configurable TTL parameters will be as follows:</span></span>

-   <span data-ttu-id="c2ba8-115">Valore TTL predefinito = 86400 secondi (1 giorno)</span><span class="sxs-lookup"><span data-stu-id="c2ba8-115">Default TTL value = 86400 seconds (1 day)</span></span>
-   <span data-ttu-id="c2ba8-116">Valore TTL minimo = 900 secondi (15 minuti)</span><span class="sxs-lookup"><span data-stu-id="c2ba8-116">Minimum TTL value = 900 seconds (15 minutes)</span></span>

<span data-ttu-id="c2ba8-117">I parametri TTL configurabili verranno archiviati come voci AVA (Assertion value Assertion) nel formato "<nome-valore>=</span><span class="sxs-lookup"><span data-stu-id="c2ba8-117">The configurable TTL parameters will be stored as AVA (attribute value assertion) entries of the form "<value-name>=</span></span><value><span data-ttu-id="c2ba8-118">"nell'attributo **ms-DS-Other-Settings** dell'oggetto NTDS-Service fornito dal DN seguente nella partizione di configurazione:</span><span class="sxs-lookup"><span data-stu-id="c2ba8-118">" in the attribute **ms-DS-Other-Settings** of the NTDS-Service object given by the following DN in the Configuration partition:</span></span>


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



<span data-ttu-id="c2ba8-119">La sintassi AVA esatta, per i due parametri TTL configurabili, è la seguente, in cui NNNN è espresso in secondi:</span><span class="sxs-lookup"><span data-stu-id="c2ba8-119">The exact AVA syntax, for the two configurable TTL parameters, is as follows where NNNN is expressed in seconds:</span></span>


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



<span data-ttu-id="c2ba8-120">Questi valori possono essere impostati da un amministratore tramite l'utilità da riga di comando Ntdsutil.</span><span class="sxs-lookup"><span data-stu-id="c2ba8-120">These values can be set by an administrator through the command-line utility ntdsutil.</span></span>

 

 




