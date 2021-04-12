---
title: restricted (attributo)
description: L'attributo \ Restricted \ specifica che una libreria o un membro di un modulo, un'interfaccia o un'interfaccia dispatch non può essere chiamata in modo arbitrario.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- attributo MIDL limitato
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398958"
---
# <a name="restricted-attribute"></a><span data-ttu-id="c2b0c-104">restricted (attributo)</span><span class="sxs-lookup"><span data-stu-id="c2b0c-104">restricted attribute</span></span>

<span data-ttu-id="c2b0c-105">L'attributo **\[ Restricted \]** specifica che una libreria o un membro di un modulo, un'interfaccia o un'interfaccia dispatch non può essere chiamata in modo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-105">The **\[restricted\]** attribute specifies that a library, or member of a module, interface, or dispinterface cannot be called arbitrarily.</span></span>

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a><span data-ttu-id="c2b0c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2b0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2b0c-107">*altri attributi*</span><span class="sxs-lookup"><span data-stu-id="c2b0c-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="c2b0c-108">Zero o più attributi MIDL.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="c2b0c-109">*tipo di istruzione*</span><span class="sxs-lookup"><span data-stu-id="c2b0c-109">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c2b0c-110">Uno dei seguenti: [**libreria**](library.md), [**modulo**](module.md), [**interfaccia**](interface.md), interfaccia [**Dispatch**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="c2b0c-110">One of the following: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2b0c-111">*nome istruzione*</span><span class="sxs-lookup"><span data-stu-id="c2b0c-111">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c2b0c-112">Identificatore con cui il software fa riferimento a questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-112">The identifier by which the software refers to this statement.</span></span>

</dd> <dt>

<span data-ttu-id="c2b0c-113">*definizioni*</span><span class="sxs-lookup"><span data-stu-id="c2b0c-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="c2b0c-114">Elementi del linguaggio MIDL che definiscono il contenuto di questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-114">MIDL language elements that define the contents of this statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2b0c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2b0c-115">Remarks</span></span>

<span data-ttu-id="c2b0c-116">Questo attributo consente di controllare l'accesso a elementi di interfacce, librerie, moduli e dispinterfaces.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-116">This attribute enables you to control access to elements of interfaces, libraries, modules, and dispinterfaces.</span></span> <span data-ttu-id="c2b0c-117">Ad esempio, può impedire l'utilizzo di un elemento di dati da un programmatore di macro.</span><span class="sxs-lookup"><span data-stu-id="c2b0c-117">For example, it can prevent a data item from being used by a macro programmer.</span></span> <span data-ttu-id="c2b0c-118">È possibile applicare questo attributo a un membro di una [**coclasse**](coclass.md), indipendentemente dal fatto che il membro sia un'interfaccia dispatch o un'interfaccia e indipendentemente dal fatto che il membro sia un sink (in ingresso) o un'origine (in uscita).</span><span class="sxs-lookup"><span data-stu-id="c2b0c-118">You can apply this attribute to a member of a [**coclass**](coclass.md), independent of whether the member is a dispinterface or interface, and independent of whether the member is a sink (incoming) or source (outgoing).</span></span> <span data-ttu-id="c2b0c-119">Un membro di una **coclasse** non può avere sia gli attributi **\[ limitati \]** che quelli **\[ predefiniti \]** .</span><span class="sxs-lookup"><span data-stu-id="c2b0c-119">A member of a **coclass** cannot have both the **\[restricted\]** and **\[default\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="c2b0c-120">Flags</span><span class="sxs-lookup"><span data-stu-id="c2b0c-120">Flags</span></span>

<span data-ttu-id="c2b0c-121">IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED</span><span class="sxs-lookup"><span data-stu-id="c2b0c-121">IMPLTYPEFLAG\_FRESTRICTED, FUNCFLAG\_FRESTRICTED</span></span>

## <a name="examples"></a><span data-ttu-id="c2b0c-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="c2b0c-122">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a><span data-ttu-id="c2b0c-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c2b0c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b0c-124">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="c2b0c-124">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="c2b0c-125">**libreria**</span><span class="sxs-lookup"><span data-stu-id="c2b0c-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="c2b0c-126">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="c2b0c-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="c2b0c-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="c2b0c-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="c2b0c-128">**modulo**</span><span class="sxs-lookup"><span data-stu-id="c2b0c-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="c2b0c-129">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="c2b0c-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c2b0c-130">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="c2b0c-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c2b0c-131">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="c2b0c-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 