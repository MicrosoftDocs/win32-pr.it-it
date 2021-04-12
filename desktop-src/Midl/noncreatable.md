---
title: noncreatable (attributo)
description: L'attributo \ noncreable \ definisce un oggetto di cui non è possibile creare un'istanza.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- attributo MIDL non creabile
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337039"
---
# <a name="noncreatable-attribute"></a><span data-ttu-id="55af4-104">noncreatable (attributo)</span><span class="sxs-lookup"><span data-stu-id="55af4-104">noncreatable attribute</span></span>

<span data-ttu-id="55af4-105">L'attributo non generabile definisce un oggetto di cui non è possibile creare un'istanza. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="55af4-105">The **\[noncreatable\]** attribute defines an object that cannot be instantiated by itself.</span></span>

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="55af4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55af4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55af4-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="55af4-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="55af4-108">Altri attributi che si applicano alla classe.</span><span class="sxs-lookup"><span data-stu-id="55af4-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="55af4-109">*coclass-nome*</span><span class="sxs-lookup"><span data-stu-id="55af4-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="55af4-110">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="55af4-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="55af4-111">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="55af4-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="55af4-112">Elenco di interfacce per la classe.</span><span class="sxs-lookup"><span data-stu-id="55af4-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55af4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="55af4-113">Remarks</span></span>

<span data-ttu-id="55af4-114">Usare l'attributo **\[ noncreable \]** in un'istruzione [**coclass**](coclass.md) per indicare agli utenti che non possono creare un nuovo oggetto di questa classe al livello principale, ovvero chiamando **CreateInstance** o **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="55af4-114">Use the **\[noncreatable\]** attribute on a [**coclass**](coclass.md) statement to indicate to users that they cannot create a new object of this class at the top level—that is, by calling **CreateInstance** or **CoCreateInstance**.</span></span> <span data-ttu-id="55af4-115">La creazione di un'istanza di un oggetto di questa classe richiede una chiamata al metodo a un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="55af4-115">Instantiation of an object of this class requires a method call to another object.</span></span> <span data-ttu-id="55af4-116">In Microsoft Excel, ad esempio, l'oggetto "Cell" non è creabile e deve essere ottenuto da un oggetto foglio di lavoro di Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="55af4-116">For example, in Microsoft Excel, the "Cell" object is noncreatable and must be obtained from a Microsoft Excel Worksheet object.</span></span>

<span data-ttu-id="55af4-117">I metodi che restituiscono istanze di classi non creabili devono restituire il tipo esatto dell'oggetto, anziché i tipi **Variant** o **IDispatch** \* .</span><span class="sxs-lookup"><span data-stu-id="55af4-117">Methods that return instances of noncreatable classes should return the exact type of the object, rather than **VARIANT** or **IDispatch**\* types.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="55af4-118">Rappresentazione TypeFlag:</span><span class="sxs-lookup"><span data-stu-id="55af4-118">Typeflag Representation:</span></span>

<span data-ttu-id="55af4-119">Assenza di TYPEFLAG \_ FCANCREATE.</span><span class="sxs-lookup"><span data-stu-id="55af4-119">The absence of TYPEFLAG\_FCANCREATE.</span></span>

## <a name="examples"></a><span data-ttu-id="55af4-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="55af4-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="55af4-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="55af4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55af4-122">**coclass**</span><span class="sxs-lookup"><span data-stu-id="55af4-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="55af4-123">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="55af4-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="55af4-124">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="55af4-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="55af4-125">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="55af4-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 