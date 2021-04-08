---
title: typedef (attributo)
description: La parola chiave typedef di IDL consente dichiarazioni typedef molto simili alle dichiarazioni typedef del linguaggio C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef attributo MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725143"
---
# <a name="typedef-attribute"></a><span data-ttu-id="e1a5d-104">typedef (attributo)</span><span class="sxs-lookup"><span data-stu-id="e1a5d-104">typedef attribute</span></span>

<span data-ttu-id="e1a5d-105">La parola chiave **typedef** di IDL consente dichiarazioni **typedef** molto simili alle dichiarazioni **typedef** del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-105">The IDL **typedef** keyword allows **typedef** declarations that are very similar to C-language **typedef** declarations.</span></span>

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a><span data-ttu-id="e1a5d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1a5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1a5d-107">*IDL-Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e1a5d-107">*idl-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a5d-108">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="e1a5d-109">Gli attributi di tipo validi in un file IDL includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md), **\]** il riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**univoco**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi di utilizzo **\[** [**\_ gestione del contesto**](context-handle.md) **\]** , **\[** [**stringa**](string.md) **\]** e **\[** [**Ignora**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e1a5d-109">Valid type attributes in an IDL file include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="e1a5d-110">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e1a5d-111">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="e1a5d-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a5d-112">Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="e1a5d-113">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-113">An optional storage specification can precede *type-specifier*.</span></span> <span data-ttu-id="e1a5d-114">La parola chiave [**const**](const.md) può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-114">The [**const**](const.md) keyword can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e1a5d-115">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="e1a5d-115">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a5d-116">Specifica i dichiaratori MIDL standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-116">Specifies standard MIDL declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e1a5d-117">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e1a5d-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e1a5d-118">Il *declarator-list* è costituito da uno o più dichiaratori, separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-118">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="e1a5d-119">*ACF-Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e1a5d-119">*acf-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a5d-120">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-120">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="e1a5d-121">Gli attributi di tipo validi in un ACF includono **\[** [**allocare**](allocate.md) **\]** , **\[** [**codificare**](encode.md) **\]** e **\[** [**decodificare**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e1a5d-121">Valid type attributes in an ACF include **\[**[**allocate**](allocate.md)**\]**, **\[**[**encode**](encode.md)**\]**, and **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="e1a5d-122">*typeName*</span><span class="sxs-lookup"><span data-stu-id="e1a5d-122">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="e1a5d-123">Specifica un tipo definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-123">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1a5d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1a5d-124">Remarks</span></span>

<span data-ttu-id="e1a5d-125">La dichiarazione di **typedef** IDL è aumentata per consentire di associare gli attributi di tipo ai tipi definiti.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-125">The IDL **typedef** declaration is augmented to allow you to associate type attributes with the defined types.</span></span> <span data-ttu-id="e1a5d-126">Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md) **\]** , **\[** [**trasmissione \_ come**](transmit-as.md) **\]** ; riferimento all'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**univoco**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e l' **\[** [**\_ handle di contesto**](context-handle.md) **\]** , la **\[** [**stringa**](string.md) **\]** e l' **\[** [**Ignore**](ignore.md) **\]** degli attributi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-126">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span>

<span data-ttu-id="e1a5d-127">La parola chiave **typedef** in un ACF applica gli attributi ai tipi definiti nel file IDL corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-127">The **typedef** keyword in an ACF applies attributes to types that are defined in the corresponding IDL file.</span></span> <span data-ttu-id="e1a5d-128">Ad esempio, l'attributo [**allocate**](allocate.md) Type consente di personalizzare l'allocazione e la deallocazione della memoria sia dall'applicazione che dagli stub.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-128">For example, the [**allocate**](allocate.md) type attribute allows you to customize memory allocation and deallocation by both the application and the stubs.</span></span>

<span data-ttu-id="e1a5d-129">L'istruzione ACF **typedef** viene visualizzata come parte del corpo di ACF.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-129">The ACF **typedef** statement appears as part of the ACF body.</span></span> <span data-ttu-id="e1a5d-130">Si noti che la sintassi di ACF **typedef** è diversa dalla sintassi **typedef** di IDL e dalla sintassi **typedef** del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-130">Note that the ACF **typedef** syntax is different from the IDL **typedef** syntax and the C-language **typedef** syntax.</span></span> <span data-ttu-id="e1a5d-131">Non è possibile introdurre nuovi tipi nell'ACF.</span><span class="sxs-lookup"><span data-stu-id="e1a5d-131">No new types can be introduced in the ACF.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1a5d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1a5d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1a5d-133">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="e1a5d-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-134">**allocare**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-134">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-135">**matrici**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-135">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-136">**const**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-136">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-137">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-138">**decodificare**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-138">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-139">**codificare**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-139">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-140">**enum**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-140">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-141">**gestire**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-141">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-142">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="e1a5d-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-143">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-143">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-144">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-144">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-145">**ref**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-145">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-146">**string**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-147">**struct**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-147">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-148">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-148">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-149">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-150">**Unione**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-150">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e1a5d-151">**unico**</span><span class="sxs-lookup"><span data-stu-id="e1a5d-151">**unique**</span></span>](unique.md)
</dt> </dl>

 

 