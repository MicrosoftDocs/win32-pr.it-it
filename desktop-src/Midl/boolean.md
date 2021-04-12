---
title: attributo booleano
description: La parola chiave booleana indica che l'espressione o l'espressione costante associata all'identificatore accetta solo i valori TRUE e FALSE.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- attributo booleano MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397811"
---
# <a name="boolean-attribute"></a><span data-ttu-id="c7d93-104">attributo booleano</span><span class="sxs-lookup"><span data-stu-id="c7d93-104">boolean attribute</span></span>

<span data-ttu-id="c7d93-105">La parola chiave **booleana** indica che l'espressione o l'espressione costante associata all'identificatore accetta solo i valori **true** e **false**.</span><span class="sxs-lookup"><span data-stu-id="c7d93-105">The keyword **boolean** indicates that the expression or constant expression associated with the identifier takes only the values **TRUE** and **FALSE**.</span></span>

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="c7d93-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7d93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d93-107">*nome identificatore*</span><span class="sxs-lookup"><span data-stu-id="c7d93-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d93-108">Specifica un identificatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="c7d93-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="c7d93-109">Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="c7d93-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7d93-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7d93-110">Remarks</span></span>

<span data-ttu-id="c7d93-111">Il tipo **booleano** è uno dei tipi di base del linguaggio IDL.</span><span class="sxs-lookup"><span data-stu-id="c7d93-111">The **boolean** type is one of the base types of the IDL language.</span></span> <span data-ttu-id="c7d93-112">Il tipo **booleano** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="c7d93-112">The **boolean** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="c7d93-113">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="c7d93-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="c7d93-114">Il tipo di base **booleano** non è compatibile con l'attributo [**oleautomation**](oleautomation.md) .</span><span class="sxs-lookup"><span data-stu-id="c7d93-114">The **boolean** base type is not compatible with the [**oleautomation**](oleautomation.md) attribute.</span></span> <span data-ttu-id="c7d93-115">Usare VARIANT \_ bool nelle interfacce compatibili con l'automazione.</span><span class="sxs-lookup"><span data-stu-id="c7d93-115">Use VARIANT\_BOOL in your Automation-compatible interfaces.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="c7d93-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7d93-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d93-117">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="c7d93-117">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="c7d93-118">**const**</span><span class="sxs-lookup"><span data-stu-id="c7d93-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="c7d93-119">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="c7d93-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c7d93-120">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="c7d93-120">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="c7d93-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="c7d93-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




