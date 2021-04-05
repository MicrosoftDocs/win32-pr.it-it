---
title: attributo forse
description: La parola chiave \ Maybe indica che non è necessario eseguire la chiamata di procedura remota ogni volta che viene chiamata e che il client non prevede una risposta. Si noti che il protocollo \ Maybe non garantisce né il recapito né il completamento della chiamata.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- attributo MIDL probabilmente
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045570"
---
# <a name="maybe-attribute"></a><span data-ttu-id="b9f18-105">attributo forse</span><span class="sxs-lookup"><span data-stu-id="b9f18-105">maybe attribute</span></span>

<span data-ttu-id="b9f18-106">La parola chiave **\[ potrebbe \]** indicare che non è necessario eseguire la chiamata di procedura remota ogni volta che viene chiamata e che il client non prevede una risposta.</span><span class="sxs-lookup"><span data-stu-id="b9f18-106">The keyword **\[maybe\]** indicates that the remote procedure call does not need to execute every time it is called and the client does not expect a response.</span></span> <span data-ttu-id="b9f18-107">Si noti che il protocollo **\[ probabilmente \]** non garantisce né il recapito né il completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="b9f18-107">Note that the **\[maybe\]** protocol ensures neither delivery nor completion of the call.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="b9f18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9f18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9f18-109">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b9f18-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f18-110">Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="b9f18-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="b9f18-111">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="b9f18-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="b9f18-112">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="b9f18-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f18-113">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b9f18-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="b9f18-114">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="b9f18-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f18-115">Specifica gli attributi aggiuntivi da applicare alla funzione.</span><span class="sxs-lookup"><span data-stu-id="b9f18-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="b9f18-116">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="b9f18-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="b9f18-117">*returnType*</span><span class="sxs-lookup"><span data-stu-id="b9f18-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f18-118">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="b9f18-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="b9f18-119">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="b9f18-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f18-120">Specifica il nome della funzione a cui verrà applicato l'attributo **\[ Maybe \]** .</span><span class="sxs-lookup"><span data-stu-id="b9f18-120">Specifies the name of the function to which the **\[maybe\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="b9f18-121">*params*</span><span class="sxs-lookup"><span data-stu-id="b9f18-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f18-122">Elenco dei parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="b9f18-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9f18-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9f18-123">Remarks</span></span>

<span data-ttu-id="b9f18-124">Una chiamata con l'attributo **\[ Maybe \]** non può contenere parametri di output ed è implicitamente una **\[** [**chiamata idempotente**](idempotent.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b9f18-124">A call with the **\[maybe\]** attribute cannot contain output parameters and is implicitly an **\[**[**idempotent**](idempotent.md)**\]** call.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9f18-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9f18-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f18-126">**trasmissione**</span><span class="sxs-lookup"><span data-stu-id="b9f18-126">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="b9f18-127">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="b9f18-127">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="b9f18-128">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="b9f18-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




