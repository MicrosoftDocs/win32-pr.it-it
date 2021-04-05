---
title: in (attributo)
description: L'attributo \ in \ indica che un parametro deve essere passato dalla routine chiamante alla routine chiamata.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- in attributo MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726967"
---
# <a name="in-attribute"></a><span data-ttu-id="5beac-104">in (attributo)</span><span class="sxs-lookup"><span data-stu-id="5beac-104">in attribute</span></span>

<span data-ttu-id="5beac-105">L'attributo **\[ in \]** indica che un parametro deve essere passato dalla routine chiamante alla routine chiamata.</span><span class="sxs-lookup"><span data-stu-id="5beac-105">The **\[in\]** attribute indicates that a parameter is to be passed from the calling procedure to the called procedure.</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="5beac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5beac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5beac-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5beac-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5beac-108">Specifica zero o più attributi che si applicano alla funzione.</span><span class="sxs-lookup"><span data-stu-id="5beac-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="5beac-109">Gli attributi di funzione validi sono **\[ callback \]**, **\[ \] local**, l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e la **\[ stringa \]** degli attributi Usage, **\[ Ignore \]** e **\[ \_ handle \] di contesto**.</span><span class="sxs-lookup"><span data-stu-id="5beac-109">Valid function attributes are **\[callback\]**, **\[local\]**, the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**, and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="5beac-110">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="5beac-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="5beac-111">Specifica un **\_ tipo di base**, uno [**struct**](struct.md), un' [**unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="5beac-111">Specifies a **base\_type**, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="5beac-112">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="5beac-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="5beac-113">*puntatore-dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="5beac-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="5beac-114">Specifica zero o più dichiaratori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="5beac-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="5beac-115">Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="5beac-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="5beac-116">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="5beac-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5beac-117">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="5beac-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="5beac-118">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5beac-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5beac-119">Specifica zero o più attributi appropriati per il tipo di parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="5beac-119">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="5beac-120">Gli attributi di parametro con l'attributo in possono anche prendere l'attributo direzionale **\[ \] out**; gli attributi **\[ \] di** campo **\[ First \_ sono \]**, **\[ Last \_ is \]**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ size \_ is \]** e **\[ Switch \_ Type \]**, l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]**; e l' **\[ \_ handle \]** e la **\[ stringa \]** del contesto degli attributi Usage.</span><span class="sxs-lookup"><span data-stu-id="5beac-120">Parameter attributes with the **\[in\]** attribute can also take the directional attribute **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]** and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="5beac-121">L'attributo Usage **\[ Ignore \]** non può essere utilizzato come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="5beac-121">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="5beac-122">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="5beac-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5beac-123">*dichiaratore*</span><span class="sxs-lookup"><span data-stu-id="5beac-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="5beac-124">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="5beac-124">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="5beac-125">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="5beac-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="5beac-126">Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5beac-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5beac-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="5beac-127">Remarks</span></span>

<span data-ttu-id="5beac-128">Nell'attributo **\[ in \]** è presente un attributo CONVERSE, **\[** [**out**](out-idl.md) **\]** , che indica che un parametro deve essere restituito dalla routine chiamata alla procedura chiamante.</span><span class="sxs-lookup"><span data-stu-id="5beac-128">The **\[in\]** attribute has a converse attribute, **\[**[**out**](out-idl.md)**\]**, which indicates that a parameter is to be returned from the called procedure to the calling procedure.</span></span> <span data-ttu-id="5beac-129">Gli attributi **\[ in \]** e **\[ out \]** sono noti come attributi di parametro direzionali perché specificano la direzione in cui vengono passati i parametri.</span><span class="sxs-lookup"><span data-stu-id="5beac-129">The **\[in\]** and **\[out\]** attributes are known as directional parameter attributes because they specify the direction in which parameters are passed.</span></span> <span data-ttu-id="5beac-130">Un parametro può essere definito come **\[ in \]**, **\[ out \]** o **\[ in**, **out \]**.</span><span class="sxs-lookup"><span data-stu-id="5beac-130">A parameter can be defined as **\[in\]**, **\[out\]**, or **\[in**, **out\]**.</span></span>

<span data-ttu-id="5beac-131">L'attributo **\[ in \]** identifica i parametri sottoposti a marshalling dallo stub client per la trasmissione al server.</span><span class="sxs-lookup"><span data-stu-id="5beac-131">The **\[in\]** attribute identifies parameters that are marshaled by the client stub for transmission to the server.</span></span>

<span data-ttu-id="5beac-132">Per impostazione predefinita, l'attributo **\[ in \]** viene applicato a un parametro quando non è specificato alcun attributo di parametro direzionale.</span><span class="sxs-lookup"><span data-stu-id="5beac-132">The **\[in\]** attribute is applied to a parameter by default when no directional parameter attribute is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="5beac-133">Esempi</span><span class="sxs-lookup"><span data-stu-id="5beac-133">Examples</span></span>

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a><span data-ttu-id="5beac-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5beac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5beac-135">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="5beac-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5beac-136">**\_alloca utente \_ MIDL**</span><span class="sxs-lookup"><span data-stu-id="5beac-136">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="5beac-137">**out**</span><span class="sxs-lookup"><span data-stu-id="5beac-137">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 