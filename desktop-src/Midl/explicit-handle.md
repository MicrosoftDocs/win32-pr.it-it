---
title: attributo explicit_handle
description: L'attributo \ Explicit \_ handle \ ACF specifica che ogni routine ha, come primo parametro, un handle primitivo, ad esempio un tipo di handle \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- attributo explicit_handle MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299086"
---
# <a name="explicit_handle-attribute"></a><span data-ttu-id="35fa2-104">\_attributo handle esplicito</span><span class="sxs-lookup"><span data-stu-id="35fa2-104">explicit\_handle attribute</span></span>

<span data-ttu-id="35fa2-105">L' \[ attributo di **\_ handle ACF esplicito** \] specifica che ogni routine ha come primo parametro un handle primitivo, ad esempio un tipo di [**handle \_ t**](handle-t.md) .</span><span class="sxs-lookup"><span data-stu-id="35fa2-105">The \[**explicit\_handle**\] ACF attribute specifies that each procedure has, as its first parameter, a primitive handle, such as a [**handle\_t**](handle-t.md) type.</span></span>

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="35fa2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35fa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fa2-107">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="35fa2-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="35fa2-108">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="35fa2-108">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35fa2-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="35fa2-109">Remarks</span></span>

<span data-ttu-id="35fa2-110">Quando si utilizza l'attributo **\[ \_ handle \] esplicito** , ogni routine dispone di un handle primitivo come primo parametro anche se il file IDL non contiene questo handle nell'elenco dei parametri.</span><span class="sxs-lookup"><span data-stu-id="35fa2-110">When you use the **\[explicit\_handle\]** attribute, each procedure has a primitive handle as its first parameter even if the IDL file does not contain this handle in its parameter list.</span></span> <span data-ttu-id="35fa2-111">I prototipi emessi per il file di intestazione e le routine stub contengono il parametro aggiuntivo e tale parametro viene usato come handle per indirizzare la chiamata remota.</span><span class="sxs-lookup"><span data-stu-id="35fa2-111">The prototypes emitted to the header file and stub routines contain the additional parameter, and that parameter is used as the handle for directing the remote call.</span></span>

<span data-ttu-id="35fa2-112">L'attributo **\[ \_ handle \] esplicito** influiscono sia sulle procedure remote sia sulle procedure di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="35fa2-112">The **\[explicit\_handle\]** attribute affects both remote procedures and serialization procedures.</span></span> <span data-ttu-id="35fa2-113">Per la serializzazione del tipo, le routine di supporto vengono generate con il parametro iniziale come handle esplicito (serializzazione).</span><span class="sxs-lookup"><span data-stu-id="35fa2-113">For type serialization, the support routines are generated with the initial parameter as an explicit (serialization) handle.</span></span> <span data-ttu-id="35fa2-114">Se non viene utilizzato l'attributo **\[ \_ handle \] esplicito** , l'applicazione può comunque specificare che un'operazione dispone di un handle esplicito (associazione o serializzazione) che indirizza la chiamata.</span><span class="sxs-lookup"><span data-stu-id="35fa2-114">If the **\[explicit\_handle\]** attribute is not used, the application can still specify that an operation have an explicit handle (binding or serialization) directing the call.</span></span> <span data-ttu-id="35fa2-115">A tale scopo, al file IDL viene fornito un prototipo con un argomento contenente un tipo di handle.</span><span class="sxs-lookup"><span data-stu-id="35fa2-115">To do this, a prototype with an argument containing a handle type is supplied to the IDL file.</span></span> <span data-ttu-id="35fa2-116">Si noti che in modalità predefinita, un argomento che non viene visualizzato per primo può essere usato anche come handle che indirizza la chiamata.</span><span class="sxs-lookup"><span data-stu-id="35fa2-116">Note that in default mode, an argument that does not appear first can also be used as a handle directing the call.</span></span>

<span data-ttu-id="35fa2-117">Pertanto, mentre l'attributo **\[ \_ handle \] esplicito** è un modo per fornire al prototipo IDL un attributo di **\[ \_ handle \] esplicito** primitivo, non richiede necessariamente una modifica al file IDL.</span><span class="sxs-lookup"><span data-stu-id="35fa2-117">Therefore, while the **\[explicit\_handle\]** attribute is a way of giving the IDL prototype a primitive **\[explicit\_handle\]** attribute, it does not necessarily require a change to the IDL file.</span></span> <span data-ttu-id="35fa2-118">In modalità [**/OSF**](-osf.md) solo il primo argomento può essere utilizzato come tipo di handle esplicito.</span><span class="sxs-lookup"><span data-stu-id="35fa2-118">In [**/osf**](-osf.md) mode only the first argument can be used as an explicit handle type.</span></span>

<span data-ttu-id="35fa2-119">L'attributo **\[ \_ handle \] esplicito** può essere utilizzato come attributo di interfaccia o attributo Operation.</span><span class="sxs-lookup"><span data-stu-id="35fa2-119">The **\[explicit\_handle\]** attribute can be used as either an interface attribute or an operation attribute.</span></span> <span data-ttu-id="35fa2-120">Come attributo di interfaccia, influiscono su tutte le operazioni nell'interfaccia e su tutti i tipi che richiedono il supporto della serializzazione.</span><span class="sxs-lookup"><span data-stu-id="35fa2-120">As an interface attribute, it affects all the operations in the interface and all the types that require serialization support.</span></span> <span data-ttu-id="35fa2-121">Se, tuttavia, viene utilizzato come attributo dell'operazione, influiscono solo su tale operazione specifica.</span><span class="sxs-lookup"><span data-stu-id="35fa2-121">If, however, it is used as an operation attribute, it affects only that particular operation.</span></span> <span data-ttu-id="35fa2-122">Se un metodo contiene uno o più \[ \] handle di contesto, l'handle \[ di contesto più a sinistra \] viene usato come handle di associazione e non viene creato alcun handle esplicito aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="35fa2-122">If a method contains one or more \[in\] context handles, the left most \[in\] context handle is used as the binding handle, and no additional explicit handle is created.</span></span>

## <a name="examples"></a><span data-ttu-id="35fa2-123">Esempi</span><span class="sxs-lookup"><span data-stu-id="35fa2-123">Examples</span></span>

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="35fa2-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="35fa2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fa2-125">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="35fa2-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="35fa2-126">**\_handle automatico**</span><span class="sxs-lookup"><span data-stu-id="35fa2-126">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="35fa2-127">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="35fa2-127">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="35fa2-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="35fa2-128">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




