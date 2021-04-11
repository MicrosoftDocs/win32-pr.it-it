---
title: attributo handle_t
description: La \_ parola chiave handle t dichiara che un oggetto deve essere del tipo di handle primitivo handle \_ t. Un handle di associazione primitivo è un oggetto dati che può essere utilizzato dall'applicazione per rappresentare l'associazione.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- attributo handle_t MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337055"
---
# <a name="handle_t-attribute"></a><span data-ttu-id="51b13-105">handle \_ t (attributo)</span><span class="sxs-lookup"><span data-stu-id="51b13-105">handle\_t attribute</span></span>

<span data-ttu-id="51b13-106">La parola chiave **handle \_ t** dichiara che un oggetto deve essere del tipo di handle primitivo **handle \_ t**.</span><span class="sxs-lookup"><span data-stu-id="51b13-106">The **handle\_t** keyword declares an object to be of the primitive handle type **handle\_t**.</span></span> <span data-ttu-id="51b13-107">Un handle di associazione primitivo è un oggetto dati che può essere utilizzato dall'applicazione per rappresentare l'associazione.</span><span class="sxs-lookup"><span data-stu-id="51b13-107">A primitive binding handle is a data object that can be used by the application to represent the binding.</span></span>

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a><span data-ttu-id="51b13-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="51b13-108">Parameters</span></span>

<span data-ttu-id="51b13-109">Questo attributo non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="51b13-109">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="51b13-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="51b13-110">Remarks</span></span>

<span data-ttu-id="51b13-111">Il tipo di **handle \_ t** è uno dei tipi predefiniti del linguaggio di definizione dell'interfaccia (IDL).</span><span class="sxs-lookup"><span data-stu-id="51b13-111">The **handle\_t** type is one of the predefined types of the interface definition language (IDL).</span></span> <span data-ttu-id="51b13-112">Può essere visualizzato come identificatore di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="51b13-112">It can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="51b13-113">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="51b13-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="51b13-114">In Microsoft RPC, i parametri di tipo **handle \_ t** possono verificarsi solo come **\[** parametri [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="51b13-114">In Microsoft RPC, parameters of type **handle\_t** can occur only as **\[**[**in**](in.md)**\]** parameters.</span></span> <span data-ttu-id="51b13-115">Gli handle primitivi non possono avere l' **\[** attributo [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="51b13-115">Primitive handles cannot have the **\[**[**unique**](unique.md)**\]** or **\[**[**ptr**](ptr.md)**\]** attribute.</span></span>

<span data-ttu-id="51b13-116">I parametri di tipo **handle \_ t** (parametri di handle primitivi) non vengono trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="51b13-116">Parameters of type **handle\_t** (primitive handle parameters) are not transmitted on the network.</span></span>

## <a name="see-also"></a><span data-ttu-id="51b13-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51b13-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b13-118">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="51b13-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="51b13-119">Binding e handle</span><span class="sxs-lookup"><span data-stu-id="51b13-119">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="51b13-120">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="51b13-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="51b13-121">**in**</span><span class="sxs-lookup"><span data-stu-id="51b13-121">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="51b13-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="51b13-122">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="51b13-123">**ptr**</span><span class="sxs-lookup"><span data-stu-id="51b13-123">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="51b13-124">**unico**</span><span class="sxs-lookup"><span data-stu-id="51b13-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 