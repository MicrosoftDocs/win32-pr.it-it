---
title: /ms_union opzione
description: L' \_ opzione Union/MS controlla l'allineamento del rapporto di recapito delle unioni non incapsulate. Nota Questo attributo viene fornito per la compatibilità con le versioni precedenti.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union switch MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857549"
---
# <a name="ms_union-switch"></a><span data-ttu-id="6cba5-104">\_Switch Unione/MS</span><span class="sxs-lookup"><span data-stu-id="6cba5-104">/ms\_union switch</span></span>

<span data-ttu-id="6cba5-105">L' **opzione \_ Union/MS** controlla l'allineamento del rapporto di recapito delle unioni non incapsulate.</span><span class="sxs-lookup"><span data-stu-id="6cba5-105">The **/ms\_union** switch controls the NDR alignment of nonencapsulated unions.</span></span>

> [!Note]  
> <span data-ttu-id="6cba5-106">Questo attributo viene fornito per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="6cba5-106">This attribute is provided for backwards compatibility.</span></span> <span data-ttu-id="6cba5-107">Non è consigliabile usarlo in una nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6cba5-107">It is not recommended for use in a new interface.</span></span>

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a><span data-ttu-id="6cba5-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="6cba5-108">Switch Options</span></span>

<span data-ttu-id="6cba5-109">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="6cba5-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cba5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6cba5-110">Remarks</span></span>

<span data-ttu-id="6cba5-111">Il compilatore MIDL riflette il comportamento del compilatore IDL OSF-DCE per le unioni non incapsulate.</span><span class="sxs-lookup"><span data-stu-id="6cba5-111">The MIDL compiler mirrors the behavior of the OSF-DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="6cba5-112">Tuttavia, poiché le versioni precedenti del compilatore MIDL non lo hanno fatto, l' **opzione \_ Union/MS** fornisce la compatibilità con le interfacce compilate in versioni precedenti del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="6cba5-112">However, because earlier versions of the MIDL compiler did not do so, the **/ms\_union** switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="6cba5-113">La \_ funzionalità di MS Union può essere utilizzata come opzione della riga di comando (**/MS \_ Union**), un attributo di interfaccia IDL o come attributo di tipo IDL.</span><span class="sxs-lookup"><span data-stu-id="6cba5-113">The ms\_union feature can be used as a command-line switch (**/ms\_union**), an IDL interface attribute, or as an IDL-type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="6cba5-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="6cba5-114">Examples</span></span>

<span data-ttu-id="6cba5-115">**\_file. idl di MIDL/MS Union**</span><span class="sxs-lookup"><span data-stu-id="6cba5-115">**midl /ms\_union file.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6cba5-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6cba5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cba5-117">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="6cba5-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6cba5-118">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="6cba5-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




