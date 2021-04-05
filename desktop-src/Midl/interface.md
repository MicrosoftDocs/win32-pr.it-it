---
title: interface (attributo)
description: La parola chiave Interface specifica il nome dell'interfaccia. Il nome dell'interfaccia deve essere specificato sia nel file IDL che nell'ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- attributo di interfaccia MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872385"
---
# <a name="interface-attribute"></a><span data-ttu-id="defe0-105">interface (attributo)</span><span class="sxs-lookup"><span data-stu-id="defe0-105">interface attribute</span></span>

<span data-ttu-id="defe0-106">La parola chiave **Interface** specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="defe0-106">The **interface** keyword specifies the name of the interface.</span></span> <span data-ttu-id="defe0-107">Il nome dell'interfaccia deve essere specificato sia nel file IDL che nell'ACF.</span><span class="sxs-lookup"><span data-stu-id="defe0-107">The interface name must be provided in both the IDL file and the ACF.</span></span>

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a><span data-ttu-id="defe0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="defe0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="defe0-109">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="defe0-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="defe0-110">Specifica gli attributi che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="defe0-110">Specifies attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="defe0-111">Gli attributi di interfaccia validi per un file IDL includono **\[** [**endpoint**](endpoint.md) **\]** , **\[** [**local**](local.md) **\]** , **\[** [**Object**](object.md) **\]** , **\[** [**pointer \_ default**](pointer-default.md) **\]** , **\[** [**UUID**](uuid.md) **\]** e **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="defe0-111">Valid interface attributes for an IDL file include **\[**[**endpoint**](endpoint.md)**\]**, **\[**[**local**](local.md)**\]**, **\[**[**object**](object.md)**\]**, **\[**[**pointer\_default**](pointer-default.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span> <span data-ttu-id="defe0-112">Gli attributi di interfaccia validi per un ACF includono **\[** [**Encode**](encode.md), **\]** **\[** [**Decode**](decode.md) **\]** , **\[** [**\_ handle automatico**](auto-handle.md) **\]** o **\[** [**\_ handle implicito**](implicit-handle.md) **\]** e **\[** [**codice**](code.md) **\]** o **\[** [**NoCode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="defe0-112">Valid interface attributes for an ACF include **\[**[**encode**](encode.md)**\]**, **\[**[**decode**](decode.md)**\]**, either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]**, and either **\[**[**code**](code.md)**\]** or **\[**[**nocode**](nocode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="defe0-113">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="defe0-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="defe0-114">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="defe0-114">Specifies the name of the interface.</span></span> <span data-ttu-id="defe0-115">Il nome dell'interfaccia deve essere un nome univoco e deve iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="defe0-115">The interface name must be a unique name and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="defe0-116">*interfaccia di base*</span><span class="sxs-lookup"><span data-stu-id="defe0-116">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="defe0-117">Specifica il nome di un'interfaccia da cui questa interfaccia derivata eredita le funzioni membro, i codici di stato e gli attributi di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="defe0-117">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="defe0-118">L'interfaccia derivata non eredita le definizioni dei tipi.</span><span class="sxs-lookup"><span data-stu-id="defe0-118">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="defe0-119">A tale scopo, usare la parola chiave [**Import**](import.md) per importare il file IDL dell'interfaccia di base.</span><span class="sxs-lookup"><span data-stu-id="defe0-119">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> <dt>

<span data-ttu-id="defe0-120">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="defe0-120">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="defe0-121">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="defe0-121">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="defe0-122">Per altre informazioni, vedere [attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="defe0-122">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="defe0-123">Il *declarator-list* è costituito da uno o più dichiaratori, separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="defe0-123">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="defe0-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="defe0-124">Remarks</span></span>

<span data-ttu-id="defe0-125">I nomi di interfaccia nel file IDL e ACF devono essere uguali, tranne quando si usa l'opzione del compilatore MIDL [**/ACF**](-acf.md).</span><span class="sxs-lookup"><span data-stu-id="defe0-125">The interface names in the IDL file and ACF must be the same, except when you use the MIDL compiler switch [**/acf**](-acf.md).</span></span>

<span data-ttu-id="defe0-126">Il nome dell'interfaccia costituisce la prima parte del nome delle strutture di dati di gestione dell'interfaccia che sono parametri per le funzioni di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="defe0-126">The interface name forms the first part of the name of interface-handle data structures that are parameters to the RPC run-time functions.</span></span> <span data-ttu-id="defe0-127">Per ulteriori informazioni, vedere [**RPC \_ if \_ handle**](/windows/desktop/Rpc/rpc-if-handle).</span><span class="sxs-lookup"><span data-stu-id="defe0-127">For more information, see [**RPC\_IF\_HANDLE**](/windows/desktop/Rpc/rpc-if-handle).</span></span>

<span data-ttu-id="defe0-128">Se l'intestazione dell'interfaccia include l'attributo dell' **\[** [**oggetto**](object.md) **\]** per indicare un'interfaccia com, deve includere anche l' **\[** [](uuid.md) **\]** attributo uuid ed è necessario specificare l'interfaccia com di base da cui è derivata.</span><span class="sxs-lookup"><span data-stu-id="defe0-128">If the interface header includes the **\[**[**object**](object.md)**\]** attribute to indicate a COM interface, it must also include the **\[**[**uuid**](uuid.md)**\]** attribute and must specify the base COM interface from which it is derived.</span></span> <span data-ttu-id="defe0-129">Per ulteriori informazioni sulle interfacce COM, vedere **\[** [**oggetto**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="defe0-129">For more information about COM interfaces, see **\[**[**object**](object.md)**\]**.</span></span>

<span data-ttu-id="defe0-130">È anche possibile usare la parola chiave **Interface** con la parola chiave [**typedef**](typedef.md) per definire un tipo di dati dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="defe0-130">You can also use the **interface** keyword with the [**typedef**](typedef.md) keyword to define an interface data type.</span></span>

## <a name="examples"></a><span data-ttu-id="defe0-131">Esempi</span><span class="sxs-lookup"><span data-stu-id="defe0-131">Examples</span></span>

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a><span data-ttu-id="defe0-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="defe0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defe0-133">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="defe0-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="defe0-134">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="defe0-134">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="defe0-135">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="defe0-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="defe0-136">**locale**</span><span class="sxs-lookup"><span data-stu-id="defe0-136">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="defe0-137">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="defe0-137">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="defe0-138">**puntatore \_ predefinito**</span><span class="sxs-lookup"><span data-stu-id="defe0-138">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="defe0-139">**\_gestore RPC if \_**</span><span class="sxs-lookup"><span data-stu-id="defe0-139">**RPC\_IF\_HANDLE**</span></span>](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[<span data-ttu-id="defe0-140">**typedef**</span><span class="sxs-lookup"><span data-stu-id="defe0-140">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="defe0-141">**uuid**</span><span class="sxs-lookup"><span data-stu-id="defe0-141">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="defe0-142">**Versione**</span><span class="sxs-lookup"><span data-stu-id="defe0-142">**version**</span></span>](version.md)
</dt> </dl>

 

 