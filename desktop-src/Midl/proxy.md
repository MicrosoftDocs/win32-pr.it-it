---
title: attributo proxy
description: L'attributo \ proxy \ impedisce che l'automazione si registri come gestore di proxy/stub per un'interfaccia duale.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- attributo MIDL proxy
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472758"
---
# <a name="proxy-attribute"></a><span data-ttu-id="357df-104">attributo proxy</span><span class="sxs-lookup"><span data-stu-id="357df-104">proxy attribute</span></span>

<span data-ttu-id="357df-105">L'attributo **\[ proxy \]** impedisce che l'automazione si registri come gestore di proxy/stub per un'interfaccia duale.</span><span class="sxs-lookup"><span data-stu-id="357df-105">The **\[proxy\]** attribute prevents Automation from registering as a proxy/stub handler for a dual interface.</span></span>

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="357df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="357df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="357df-107">*stringa-UUID*</span><span class="sxs-lookup"><span data-stu-id="357df-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="357df-108">Specifica una stringa costituita da 8 cifre esadecimali seguite da un trattino, quindi da tre gruppi di 4 cifre esadecimali seguite da un trattino e quindi da 12 cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="357df-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="357df-109">È possibile racchiudere la stringa UUID tra virgolette, tranne quando si usa l'opzione del compilatore MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="357df-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> <dt>

<span data-ttu-id="357df-110">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="357df-110">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="357df-111">Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="357df-111">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="357df-112">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="357df-112">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="357df-113">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="357df-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="357df-114">Nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="357df-114">Name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="357df-115">*interfaccia di base*</span><span class="sxs-lookup"><span data-stu-id="357df-115">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="357df-116">Specifica il nome di un'interfaccia da cui questa interfaccia derivata eredita le funzioni membro, i codici di stato e gli attributi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="357df-116">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="357df-117">L'interfaccia derivata non eredita le definizioni dei tipi.</span><span class="sxs-lookup"><span data-stu-id="357df-117">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="357df-118">A tale scopo, usare la parola chiave [**Import**](import.md) per importare il file IDL dell'interfaccia di base.</span><span class="sxs-lookup"><span data-stu-id="357df-118">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="357df-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="357df-119">Remarks</span></span>

<span data-ttu-id="357df-120">L'uso dell' \[ attributo **proxy** \] per un'interfaccia duale impedisce al TLB di assumere gli stub generati.</span><span class="sxs-lookup"><span data-stu-id="357df-120">Using the \[ **proxy**\] attribute for a dual interface prevents the TLB from taking over generated stubs.</span></span> <span data-ttu-id="357df-121">Se questo attributo viene specificato, non è necessario annullare la registrazione del proxy TypeLib quando viene annullata la registrazione della libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="357df-121">If this attribute is specified, the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

### <a name="flags"></a><span data-ttu-id="357df-122">Flags</span><span class="sxs-lookup"><span data-stu-id="357df-122">Flags</span></span>

<dl> <dt>

<span data-ttu-id="357df-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_proxy TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="357df-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="357df-124">Le interfacce possono essere contrassegnate con il \_ flag proxy TypeFlag per indicare che utilizzeranno una libreria a collegamento dinamico proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="357df-124">Interfaces can be marked with the TYPEFLAG\_PROXY flag to indicate they will be using a proxy/stub dynamic link library.</span></span> <span data-ttu-id="357df-125">Questo flag specifica che non deve essere annullata la registrazione del proxy TypeLib quando viene annullata la registrazione della libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="357df-125">This flag specifies the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="357df-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="357df-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="357df-127">**Generazione di una libreria dei tipi con MIDL**</span><span class="sxs-lookup"><span data-stu-id="357df-127">**Generating a Type Library with MIDL**</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="357df-128">**Dual**</span><span class="sxs-lookup"><span data-stu-id="357df-128">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="357df-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="357df-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 