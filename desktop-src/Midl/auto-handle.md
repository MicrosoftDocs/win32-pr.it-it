---
title: attributo auto_handle
description: L'attributo \ auto \_ handle \ ACF indica allo stub di stabilire automaticamente l'associazione per una funzione che non dispone di un parametro di handle di binding esplicito. Si noti che questo attributo è obsoleto e non è più supportato.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- attributo auto_handle MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471910"
---
# <a name="auto_handle-attribute"></a><span data-ttu-id="a8a9f-104">\_attributo handle automatico</span><span class="sxs-lookup"><span data-stu-id="a8a9f-104">auto\_handle attribute</span></span>

<span data-ttu-id="a8a9f-105">L'attributo **\[ \_ gestione \] automatica** ACF indica allo stub di stabilire automaticamente l'associazione per una funzione che non dispone di un parametro di handle di binding esplicito.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-105">The **\[auto\_handle\]** ACF attribute directs the stub to automatically establish the binding for a function that does not have an explicit binding-handle parameter.</span></span>

> [!Note]  
> <span data-ttu-id="a8a9f-106">Questo attributo è obsoleto e non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-106">This attribute is obsolete and no longer supported.</span></span> <span data-ttu-id="a8a9f-107">È consigliabile usare l'opzione [**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="a8a9f-107">Use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="a8a9f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8a9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a9f-109">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="a8a9f-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a9f-110">Specifica zero o più attributi che si applicano all'interfaccia nel suo complesso, ad esempio [**Code**](code.md) o [**NoCode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="a8a9f-110">Specifies zero or more attributes that apply to the interface as a whole, such as [**code**](code.md) or [**nocode**](nocode.md).</span></span> <span data-ttu-id="a8a9f-111">Separare gli attributi di interfaccia con virgole.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-111">Separate interface attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a8a9f-112">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="a8a9f-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a9f-113">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a8a9f-114">*interfaccia-definizione*</span><span class="sxs-lookup"><span data-stu-id="a8a9f-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a9f-115">Specifica le istruzioni IDL che formano la definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-115">Specifies IDL statements that form the definition of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8a9f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8a9f-116">Remarks</span></span>

<span data-ttu-id="a8a9f-117">L'attributo **\[ \_ handle \] automatico** viene visualizzato nell'intestazione Interface di ACF.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-117">The **\[auto\_handle\]** attribute appears in the interface header of the ACF.</span></span> <span data-ttu-id="a8a9f-118">Viene inoltre visualizzato nell'intestazione di interfaccia del file IDL quando si specifica l'opzione del compilatore MIDL [**/app \_ config**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="a8a9f-118">It also appears in the interface header of the IDL file when you specify the MIDL compiler switch [**/app\_config**](-app-config.md).</span></span>

<span data-ttu-id="a8a9f-119">Quando il client chiama una funzione che utilizza il binding automatico e non esiste alcun binding a un server, lo stub stabilisce automaticamente l'associazione.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-119">When the client calls a function that uses automatic binding and no binding to a server exists, the stub automatically establishes the binding.</span></span> <span data-ttu-id="a8a9f-120">L'associazione viene riutilizzata per le chiamate successive ad altre funzioni nell'interfaccia che utilizzano l'associazione automatica.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-120">The binding is reused for subsequent calls to other functions in the interface that use automatic binding.</span></span> <span data-ttu-id="a8a9f-121">Il programma dell'applicazione client non deve dichiarare né eseguire alcuna elaborazione relativa all'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-121">The client application program does not have to declare or perform any processing relating to the binding handle.</span></span>

<span data-ttu-id="a8a9f-122">Quando ACF non è presente o non include l'attributo [**\[ \_ handle \] implicito**](implicit-handle.md) , il compilatore MIDL usa l' **\[ \_ handle \] automatico** e genera un messaggio informativo.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-122">When the ACF is not present or does not include the [**\[implicit\_handle\]**](implicit-handle.md) attribute, the MIDL compiler uses **\[auto\_handle\]** and issues an informational message.</span></span> <span data-ttu-id="a8a9f-123">Il compilatore MIDL usa anche l' **\[ \_ handle \] automatico**, se necessario, per stabilire l'associazione iniziale per un [**\[ \_ handle \] di contesto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="a8a9f-123">The MIDL compiler also uses **\[auto\_handle\]**, if needed, to establish the initial binding for a [**\[context\_handle\]**](context-handle.md).</span></span>

<span data-ttu-id="a8a9f-124">L'attributo **\[ \_ handle \] automatico** può verificarsi solo se l' [**\[ \_ handle \] implicito**](implicit-handle.md) o l'attributo [**\[ \_ handle \] esplicito**](explicit-handle.md) non si verifica.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-124">The **\[auto\_handle\]** attribute can occur only if the [**\[implicit\_handle\]**](implicit-handle.md) or [**\[explicit\_handle\]**](explicit-handle.md) attribute does not occur.</span></span> <span data-ttu-id="a8a9f-125">L'attributo **\[ \_ handle \] automatico** può essere presente all'interno dell'intestazione dell'interfaccia ACF o IDL al massimo una volta.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-125">The **\[auto\_handle\]** attribute can occur in the ACF or IDL interface header at most once.</span></span>

> [!Note]  
> <span data-ttu-id="a8a9f-126">Non è possibile usare l'associazione automatica (con l'attributo **\[ \_ handle \] automatico** o per impostazione predefinita) se si elaborano i dati attraverso le pipe.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-126">You cannot use automatic binding (either with the **\[auto\_handle\]** attribute, or by default) if you are processing data through pipes.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a8a9f-127">Esempi</span><span class="sxs-lookup"><span data-stu-id="a8a9f-127">Examples</span></span>

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a><span data-ttu-id="a8a9f-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a8a9f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a9f-129">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="a8a9f-129">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="a8a9f-130">**configurazione di/app \_**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-130">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="a8a9f-131">**codice**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-131">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="a8a9f-132">**handle esplicito \_**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-132">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="a8a9f-133">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a8a9f-134">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-134">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="a8a9f-135">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-135">**nocode**</span></span>](nocode.md)
</dt> </dl>

 

 




