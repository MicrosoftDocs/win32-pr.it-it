---
title: ms_union (attributo)
description: La parola chiave \ MS \_ Union \ viene utilizzata per controllare l'allineamento del rapporto di recapito delle unioni non incapsulate.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- attributo ms_union MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045568"
---
# <a name="ms_union-attribute"></a><span data-ttu-id="a484d-104">\_attributo ms Union</span><span class="sxs-lookup"><span data-stu-id="a484d-104">ms\_union attribute</span></span>

<span data-ttu-id="a484d-105">La parola chiave \[ **MS \_ Union** \] viene utilizzata per controllare l'allineamento del rapporto di recapito delle unioni non incapsulate.</span><span class="sxs-lookup"><span data-stu-id="a484d-105">The keyword \[**ms\_union**\] is used to control the NDR alignment of nonencapsulated unions.</span></span>

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a><span data-ttu-id="a484d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a484d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a484d-107">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="a484d-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a484d-108">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a484d-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a484d-109">*tipo di procedura*</span><span class="sxs-lookup"><span data-stu-id="a484d-109">*procedure-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a484d-110">Specifica il tipo restituito della routine a cui viene applicato l'attributo.</span><span class="sxs-lookup"><span data-stu-id="a484d-110">Specifies the return type of the procedure to which the attribute is being applied.</span></span>

</dd> <dt>

<span data-ttu-id="a484d-111">*nome procedura*</span><span class="sxs-lookup"><span data-stu-id="a484d-111">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a484d-112">Specifica il nome della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="a484d-112">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a484d-113">*param-list*</span><span class="sxs-lookup"><span data-stu-id="a484d-113">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a484d-114">Specifica l'elenco di parametri della stored procedure, che può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="a484d-114">Specifies the procedure's parameter list, which may be empty.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a484d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a484d-115">Remarks</span></span>

<span data-ttu-id="a484d-116">Non usare mai questa opzione o attributo con nuove interfacce.</span><span class="sxs-lookup"><span data-stu-id="a484d-116">Never use this switch or attribute with new interfaces.</span></span> <span data-ttu-id="a484d-117">Si tratta di una funzionalità di compatibilità con le versioni precedenti. Il compilatore MIDL in questa versione di Microsoft RPC rispecchia il comportamento del compilatore IDL OSF DCE per le unioni non incapsulate.</span><span class="sxs-lookup"><span data-stu-id="a484d-117">This is a backward compatibility feature only.The MIDL compiler in this version of Microsoft RPC mirrors the behavior of the OSF DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="a484d-118">Tuttavia, poiché le versioni precedenti del compilatore MIDL non lo hanno fatto, l' [**opzione \_ Union/MS**](-ms-union.md) fornisce la compatibilità con le interfacce compilate in versioni precedenti del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="a484d-118">However, because earlier versions of the MIDL compiler did not do so, the [**/ms\_union**](-ms-union.md) switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="a484d-119">La funzionalità di **MS \_ Union** può essere utilizzata come attributo di interfaccia IDL, attributo di tipo IDL o come opzione della riga di comando ( [**/MS \_ Union**](-ms-union.md)).</span><span class="sxs-lookup"><span data-stu-id="a484d-119">The **ms\_union** feature can be used as an IDL interface attribute, an IDL type attribute, or as a command-line switch ( [**/ms\_union**](-ms-union.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="a484d-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="a484d-120">Examples</span></span>

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a><span data-ttu-id="a484d-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a484d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a484d-122">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="a484d-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a484d-123">**\_Unione/MS**</span><span class="sxs-lookup"><span data-stu-id="a484d-123">**/ms\_union**</span></span>](-ms-union.md)
</dt> </dl>

 

 




