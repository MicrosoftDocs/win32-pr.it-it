---
title: public (attributo)
description: L'attributo \ Public \ include un alias dichiarato con la parola chiave typedef nella libreria dei tipi.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- MIDL attributo pubblico
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299634"
---
# <a name="public-attribute"></a><span data-ttu-id="2e37b-104">public (attributo)</span><span class="sxs-lookup"><span data-stu-id="2e37b-104">public attribute</span></span>

<span data-ttu-id="2e37b-105">L'attributo **\[ \] public** include un alias dichiarato con la parola chiave [**typedef**](typedef.md) nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="2e37b-105">The **\[public\]** attribute includes an alias declared with the [**typedef**](typedef.md) keyword in the type library.</span></span>

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a><span data-ttu-id="2e37b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e37b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e37b-107">*tipo di dati*</span><span class="sxs-lookup"><span data-stu-id="2e37b-107">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2e37b-108">Tipo di dati per il quale l'identificatore sarà un alias.</span><span class="sxs-lookup"><span data-stu-id="2e37b-108">The data type that the identifier will be an alias for.</span></span>

</dd> <dt>

<span data-ttu-id="2e37b-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="2e37b-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2e37b-110">Un altro nome in base al quale il *tipo di dati* sarà noto nel software.</span><span class="sxs-lookup"><span data-stu-id="2e37b-110">Another name by which *data-type* will be known in the software.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e37b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e37b-111">Remarks</span></span>

<span data-ttu-id="2e37b-112">Per impostazione predefinita, un alias dichiarato con [**typedef**](typedef.md) e privo di altri attributi viene considerato come **\# definito** e non è incluso nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="2e37b-112">By default, an alias that is declared with [**typedef**](typedef.md) and has no other attributes is treated as a **\#define** and is not included in the type library.</span></span> <span data-ttu-id="2e37b-113">L'utilizzo dell'attributo **\[ public \]** garantisce che l'alias diventi parte della libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="2e37b-113">Using the **\[public\]** attribute ensures that the alias becomes part of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="2e37b-114">Per il compilatore MIDL è necessario applicare in modo esplicito l'attributo **\[ public \]** a ogni typedef che si desidera public.</span><span class="sxs-lookup"><span data-stu-id="2e37b-114">The MIDL compiler requires that you explicitly apply the **\[public\]** attribute to each typedef that you want public.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2e37b-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="2e37b-115">Examples</span></span>

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a><span data-ttu-id="2e37b-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2e37b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e37b-117">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="2e37b-117">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="2e37b-118">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="2e37b-118">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="2e37b-119">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="2e37b-119">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="2e37b-120">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="2e37b-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="2e37b-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="2e37b-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 