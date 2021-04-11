---
title: attributo ncacn_dnet_nsp
description: La \_ \_ parola chiave ncacn DNET NSP identifica DECnet come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- attributo ncacn_dnet_nsp MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117714"
---
# <a name="ncacn_dnet_nsp-attribute"></a><span data-ttu-id="0bf66-105">ncacn \_ DNET- \_ attributo NSP</span><span class="sxs-lookup"><span data-stu-id="0bf66-105">ncacn\_dnet\_nsp attribute</span></span>

<span data-ttu-id="0bf66-106">La parola chiave **ncacn \_ DNET \_ NSP** identifica DECnet come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="0bf66-106">The **ncacn\_dnet\_nsp** keyword identifies DECnet as the protocol family for the endpoint.</span></span> <span data-ttu-id="0bf66-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0bf66-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="0bf66-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bf66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf66-109">*nome server*</span><span class="sxs-lookup"><span data-stu-id="0bf66-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf66-110">Specifica il nome o l'indirizzo Internet per il server, o host, computer.</span><span class="sxs-lookup"><span data-stu-id="0bf66-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="0bf66-111">Il nome è una stringa di caratteri.</span><span class="sxs-lookup"><span data-stu-id="0bf66-111">The name is a character string.</span></span>

</dd> <dt>

<span data-ttu-id="0bf66-112">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="0bf66-112">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf66-113">Specifica un nome di oggetto o un numero di oggetto DECnet.</span><span class="sxs-lookup"><span data-stu-id="0bf66-113">Specifies a DECnet object name or object number.</span></span> <span data-ttu-id="0bf66-114">Il nome dell'oggetto può essere composto da un massimo di 16 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0bf66-114">The object name can consist of up to 16 characters.</span></span> <span data-ttu-id="0bf66-115">I numeri degli oggetti possono essere preceduti dal simbolo di cancelletto ( \# ).</span><span class="sxs-lookup"><span data-stu-id="0bf66-115">Object numbers can be prefixed by the pound sign (\#).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bf66-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bf66-116">Remarks</span></span>

<span data-ttu-id="0bf66-117">La sintassi della stringa della porta di trasporto DECnet, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="0bf66-117">The syntax of the DECnet transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="0bf66-118">Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="0bf66-118">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="0bf66-119">È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="0bf66-119">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="0bf66-120">Questa famiglia di protocolli non è supportata in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0bf66-120">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0bf66-121">Esempi</span><span class="sxs-lookup"><span data-stu-id="0bf66-121">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="0bf66-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0bf66-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf66-123">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="0bf66-123">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="0bf66-124">**Associazione stringa**</span><span class="sxs-lookup"><span data-stu-id="0bf66-124">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 