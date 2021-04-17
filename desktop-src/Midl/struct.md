---
title: struct (attributo)
description: La parola chiave struct viene usata in un identificatore del tipo di struttura.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- attributo struct MIDL
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299736"
---
# <a name="struct-attribute"></a><span data-ttu-id="e793b-104">struct (attributo)</span><span class="sxs-lookup"><span data-stu-id="e793b-104">struct attribute</span></span>

<span data-ttu-id="e793b-105">La parola chiave **struct** viene usata in un identificatore del tipo di struttura.</span><span class="sxs-lookup"><span data-stu-id="e793b-105">The **struct** keyword is used in a structure type specifier.</span></span>

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="e793b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e793b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e793b-107">*struct-Tag*</span><span class="sxs-lookup"><span data-stu-id="e793b-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="e793b-108">Specifica un tag facoltativo per la struttura.</span><span class="sxs-lookup"><span data-stu-id="e793b-108">Specifies an optional tag for the structure.</span></span>

</dd> <dt>

<span data-ttu-id="e793b-109">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e793b-109">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e793b-110">Specifica zero o più attributi di campo che si applicano al membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="e793b-110">Specifies zero or more field attributes that apply to the structure member.</span></span> <span data-ttu-id="e793b-111">Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** e **\[** [**size \_ è**](size-is.md) **\]** ; la stringa degli attributi **\[** [](string.md) **\]** di utilizzo e **\[** [**Ignore**](ignore.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e il **\[** [**\_ tipo di opzione**](switch-type.md)attribute Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="e793b-111">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="e793b-112">Separare più attributi di campo con virgole.</span><span class="sxs-lookup"><span data-stu-id="e793b-112">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e793b-113">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="e793b-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e793b-114">Specifica un [tipo di base](midl-base-types.md), uno **struct**, un' [**Unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="e793b-114">Specifies a [base type](midl-base-types.md), **struct**, [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="e793b-115">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="e793b-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e793b-116">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="e793b-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e793b-117">Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="e793b-117">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e793b-118">I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="e793b-118">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="e793b-119">Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.</span><span class="sxs-lookup"><span data-stu-id="e793b-119">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e793b-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e793b-120">Remarks</span></span>

<span data-ttu-id="e793b-121">L'identificatore del tipo di struttura IDL, **struct**, differisce dall'identificatore di tipo C standard nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e793b-121">The IDL structure type specifier, **struct**, differs from the standard C type specifier in the following ways:</span></span>

-   <span data-ttu-id="e793b-122">Ogni membro della struttura può essere associato a attributi di campo facoltativi che descrivono le caratteristiche del membro della struttura ai fini di una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="e793b-122">Each structure member can be associated with optional field attributes that describe characteristics of that structure member for the purposes of a remote procedure call.</span></span>
-   <span data-ttu-id="e793b-123">I campi di bit e i dichiaratori di funzione non sono consentiti nelle strutture utilizzate nelle chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="e793b-123">Bit fields and function declarators are not allowed in structures that are used in remote procedure calls.</span></span> <span data-ttu-id="e793b-124">Questi costrutti di dichiaratori C standard possono essere usati solo se la struttura non è trasmessa sulla rete.</span><span class="sxs-lookup"><span data-stu-id="e793b-124">These standard C declarator constructs can be used only if the structure is not transmitted on the network.</span></span>

<span data-ttu-id="e793b-125">La forma delle strutture deve essere la stessa nelle diverse piattaforme per garantire l'interconnettività.</span><span class="sxs-lookup"><span data-stu-id="e793b-125">The shape of structures must be the same across platforms to ensure interconnectivity.</span></span>

## <a name="examples"></a><span data-ttu-id="e793b-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="e793b-126">Examples</span></span>

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="e793b-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e793b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e793b-128">**matrici**</span><span class="sxs-lookup"><span data-stu-id="e793b-128">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e793b-129">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="e793b-129">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="e793b-130">Attributi array e Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="e793b-130">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="e793b-131">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="e793b-131">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e793b-132">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="e793b-132">**/c\_ext**</span></span>](-c-ext.md)
</dt> <dt>

[<span data-ttu-id="e793b-133">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="e793b-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e793b-134">**enum**</span><span class="sxs-lookup"><span data-stu-id="e793b-134">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e793b-135">**il primo \_ è**</span><span class="sxs-lookup"><span data-stu-id="e793b-135">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="e793b-136">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="e793b-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e793b-137">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="e793b-137">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e793b-138">**ultimo \_ è**</span><span class="sxs-lookup"><span data-stu-id="e793b-138">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="e793b-139">**lunghezza \_**</span><span class="sxs-lookup"><span data-stu-id="e793b-139">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="e793b-140">**Max \_ è**</span><span class="sxs-lookup"><span data-stu-id="e793b-140">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="e793b-141">**/osf**</span><span class="sxs-lookup"><span data-stu-id="e793b-141">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="e793b-142">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e793b-142">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e793b-143">**ref**</span><span class="sxs-lookup"><span data-stu-id="e793b-143">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e793b-144">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="e793b-144">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="e793b-145">**string**</span><span class="sxs-lookup"><span data-stu-id="e793b-145">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e793b-146">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="e793b-146">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="e793b-147">**Unione**</span><span class="sxs-lookup"><span data-stu-id="e793b-147">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e793b-148">**unico**</span><span class="sxs-lookup"><span data-stu-id="e793b-148">**unique**</span></span>](unique.md)
</dt> </dl>

 

 