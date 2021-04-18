---
title: transmit_as (attributo)
description: L'attributo \ trasmissione \_ As \ indica al compilatore di associare Type-ID, ovvero un tipo presentato che le applicazioni client e server manipolano, con un tipo trasmesso Xmit-Type.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- attributo transmit_as MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299621"
---
# <a name="transmit_as-attribute"></a><span data-ttu-id="8c601-104">Trasmetti \_ come attributo</span><span class="sxs-lookup"><span data-stu-id="8c601-104">transmit\_as attribute</span></span>

<span data-ttu-id="8c601-105">L'attributo **\[ trasmissione \_ As \]** indica al compilatore di associare \*\*Type-ID \* \* *,* che è un tipo presentato che le applicazioni client e server manipolano con un tipo trasmesso **Xmit-Type.**</span><span class="sxs-lookup"><span data-stu-id="8c601-105">The **\[transmit\_as\]** attribute instructs the compiler to associate \**type-id\*\*\*,* which is a presented type that client and server applications manipulate, with a transmitted type **xmit-type.**</span></span>

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a><span data-ttu-id="8c601-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c601-107">*tipo di Xmit*</span><span class="sxs-lookup"><span data-stu-id="8c601-107">*xmit-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8c601-108">Specifica il tipo di dati trasmesso tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="8c601-108">Specifies the data type that is transmitted between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="8c601-109">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="8c601-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8c601-110">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="8c601-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="8c601-111">Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**\_ tipo di commutione**](switch-type.md), **\]** il riferimento dell'attributo del puntatore **\[** [](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md)e **\]** la stringa degli attributi di utilizzo **\[** [](string.md) **\]** e **\[** [**ignorano**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="8c601-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="8c601-112">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="8c601-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="8c601-113">*identificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="8c601-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="8c601-114">Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="8c601-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="8c601-115">Una specifica di archiviazione facoltativa può precedere *Type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="8c601-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="8c601-116">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="8c601-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8c601-117">Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="8c601-117">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="8c601-118">Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="8c601-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="8c601-119">Il *declarator-list* è costituito da uno o più dichiaratori separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="8c601-119">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="8c601-120">Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8c601-120">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8c601-121">*ID tipo*</span><span class="sxs-lookup"><span data-stu-id="8c601-121">*type-id*</span></span> 
</dt> <dd>

<span data-ttu-id="8c601-122">Specifica il nome del tipo di dati presentato alle applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="8c601-122">Specifies the name of the data type that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c601-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c601-123">Remarks</span></span>

<span data-ttu-id="8c601-124">Per utilizzare l'attributo **\[ trasmissione \_ As \]** , l'utente deve fornire routine che convertono i dati tra i tipi presentati e trasmessi. tali routine devono inoltre liberare memoria utilizzata per conservare i dati convertiti.</span><span class="sxs-lookup"><span data-stu-id="8c601-124">To use the **\[transmit\_as\]** attribute, the user must supply routines that convert data between the presented and the transmitted types; these routines must also free memory used to hold the converted data.</span></span> <span data-ttu-id="8c601-125">L'attributo **\[ trasmissione \_ As \]** indica agli stub di chiamare le routine di conversione fornite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8c601-125">The **\[transmit\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="8c601-126">Il tipo trasmesso *Xmit-Type* deve essere risolto in un tipo di base MIDL, un tipo predefinito o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="8c601-126">The transmitted type *xmit-type* must resolve to a MIDL base type, predefined type, or a type identifier.</span></span> <span data-ttu-id="8c601-127">Per altre informazioni, vedere [tipi di base MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="8c601-127">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="8c601-128">L'utente deve fornire le routine seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c601-128">The user must supply the following routines.</span></span>



| <span data-ttu-id="8c601-129">Nome routine</span><span class="sxs-lookup"><span data-stu-id="8c601-129">Routine name</span></span>              | <span data-ttu-id="8c601-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c601-130">Description</span></span>                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c601-131">*ID-tipo \* \* \* \_ in \_ Xmit*\*</span><span class="sxs-lookup"><span data-stu-id="8c601-131">*type-id\*\*\*\_to\_xmit*\*</span></span>   | <span data-ttu-id="8c601-132">Converte i dati dal tipo presentato al tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="8c601-132">Converts data from the presented type to the transmitted type.</span></span> <span data-ttu-id="8c601-133">Questa routine alloca memoria per il tipo trasmesso e per tutti i dati a cui fanno riferimento i puntatori nel tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="8c601-133">This routine allocates memory for the transmitted type and for any data referenced by pointers in the transmitted type.</span></span>                            |
| <span data-ttu-id="8c601-134">*ID-tipo \* \* \* \_ da \_ Xmit*\*</span><span class="sxs-lookup"><span data-stu-id="8c601-134">*type-id\*\*\*\_from\_xmit*\*</span></span> | <span data-ttu-id="8c601-135">Converte i dati dal tipo trasmesso al tipo presentato.</span><span class="sxs-lookup"><span data-stu-id="8c601-135">Converts data from the transmitted type to the presented type.</span></span> <span data-ttu-id="8c601-136">Questa routine è responsabile dell'allocazione della memoria per i dati a cui fanno riferimento i puntatori nel tipo presentato.</span><span class="sxs-lookup"><span data-stu-id="8c601-136">This routine is responsible for allocating memory for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="8c601-137">RPC alloca memoria per il tipo stesso.</span><span class="sxs-lookup"><span data-stu-id="8c601-137">RPC allocates memory for the type itself.</span></span> |
| <span data-ttu-id="8c601-138">*ID tipo \* \* \* \_ inst libero \_*\*</span><span class="sxs-lookup"><span data-stu-id="8c601-138">*type-id\*\*\*\_free\_inst*\*</span></span> | <span data-ttu-id="8c601-139">Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo presentato.</span><span class="sxs-lookup"><span data-stu-id="8c601-139">Frees memory allocated for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="8c601-140">RPC libera la memoria per il tipo stesso.</span><span class="sxs-lookup"><span data-stu-id="8c601-140">RPC frees memory for the type itself.</span></span>                                                                                               |
| <span data-ttu-id="8c601-141">*ID-tipo \* \* \* \_ \_ Xmit gratuito*\*</span><span class="sxs-lookup"><span data-stu-id="8c601-141">*type-id\*\*\*\_free\_xmit*\*</span></span> | <span data-ttu-id="8c601-142">Libera lo spazio di archiviazione usato dal chiamante per il tipo trasmesso e per i dati a cui fanno riferimento i puntatori nel tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="8c601-142">Frees storage used by the caller for the transmitted type and for data referenced by pointers in the transmitted type.</span></span>                                                                                            |



 

 

<span data-ttu-id="8c601-143">Lo stub client chiama *Type-ID \* \* \* \_ in \_ Xmit*\* per allocare spazio per il tipo trasmesso e per convertire i dati in oggetti di tipo *Xmit-Type.*</span><span class="sxs-lookup"><span data-stu-id="8c601-143">The client stub calls *type-id\*\*\*\_to\_xmit*\* to allocate space for the transmitted type and to translate the data into objects of type *xmit-type.*</span></span> <span data-ttu-id="8c601-144">Lo stub del server alloca spazio per il tipo di dati originale e chiama *Type-ID \* \* \* \_ da \_ Xmit*\* per tradurre i dati dal tipo trasmesso al tipo presentato.</span><span class="sxs-lookup"><span data-stu-id="8c601-144">The server stub allocates space for the original data type and calls *type-id\*\*\*\_from\_xmit*\* to translate the data from its transmitted type to the presented type.</span></span>

<span data-ttu-id="8c601-145">Al ritorno dal codice dell'applicazione, lo stub del server chiama *Type-ID \* \* \_ \* \_ inst libero*\* per deallocare lo spazio di archiviazione per *Type-ID* sul lato server.</span><span class="sxs-lookup"><span data-stu-id="8c601-145">Upon return from the application code, the server stub calls *type-id\*\*\*\_free\_inst*\* to deallocate the storage for *type-id* on the server side.</span></span> <span data-ttu-id="8c601-146">Lo stub client chiama *Type-ID \* \* \* \_ Free \_ Xmit*\* per deallocare l'archiviazione di *tipo Xmit* sul lato client.</span><span class="sxs-lookup"><span data-stu-id="8c601-146">The client stub calls *type-id\*\*\*\_free\_xmit*\* to deallocate the *xmit-type* storage on the client side.</span></span>

<span data-ttu-id="8c601-147">I tipi seguenti non possono avere un attributo **\[ trasmissione \_ As \]** :</span><span class="sxs-lookup"><span data-stu-id="8c601-147">The following types cannot have a **\[transmit\_as\]** attribute:</span></span>

-   <span data-ttu-id="8c601-148">Handle di contesto (tipi con l'attributo del tipo di **\[** [**\_ handle di contesto**](context-handle.md) **\]** e i tipi usati come parametri con l'attributo dell' **\[ \_ handle \] di contesto** )</span><span class="sxs-lookup"><span data-stu-id="8c601-148">Context handles (types with the **\[**[**context\_handle**](context-handle.md)**\]** type attribute and types that are used as parameters with the **\[context\_handle\]** attribute)</span></span>
-   <span data-ttu-id="8c601-149">Tipi che sono pipe o derivate da pipe</span><span class="sxs-lookup"><span data-stu-id="8c601-149">Types that are pipes or derived from pipes</span></span>
-   <span data-ttu-id="8c601-150">Tipi di dati utilizzati come tipo di base di una definizione di pipe</span><span class="sxs-lookup"><span data-stu-id="8c601-150">Data types that are used as the base type of a pipe definition</span></span>
-   <span data-ttu-id="8c601-151">Parametri che sono puntatori o si risolvono ai puntatori</span><span class="sxs-lookup"><span data-stu-id="8c601-151">Parameters that are pointers or resolve to pointers</span></span>
-   <span data-ttu-id="8c601-152">Parametri conformi, variabili o matrici aperte</span><span class="sxs-lookup"><span data-stu-id="8c601-152">Parameters that are conformant, varying, or open arrays</span></span>
-   <span data-ttu-id="8c601-153">Strutture che contengono matrici conformi</span><span class="sxs-lookup"><span data-stu-id="8c601-153">Structures that contain conformant arrays</span></span>
-   <span data-ttu-id="8c601-154">Handle di tipo predefinito [**\_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="8c601-154">The predefined type [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>

<span data-ttu-id="8c601-155">I tipi trasmessi devono essere conformi alle restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c601-155">Types that are transmitted must conform to the following restrictions:</span></span>

-   <span data-ttu-id="8c601-156">Non devono essere puntatori o contenere puntatori.</span><span class="sxs-lookup"><span data-stu-id="8c601-156">They must not be pointers or contain pointers.</span></span>
-   <span data-ttu-id="8c601-157">Non devono essere pipe né contenere pipe.</span><span class="sxs-lookup"><span data-stu-id="8c601-157">They must not be pipes or contain pipes.</span></span>

## <a name="examples"></a><span data-ttu-id="8c601-158">Esempi</span><span class="sxs-lookup"><span data-stu-id="8c601-158">Examples</span></span>

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a><span data-ttu-id="8c601-159">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8c601-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c601-160">**matrici**</span><span class="sxs-lookup"><span data-stu-id="8c601-160">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="8c601-161">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="8c601-161">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="8c601-162">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="8c601-162">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="8c601-163">**enum**</span><span class="sxs-lookup"><span data-stu-id="8c601-163">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="8c601-164">**gestire**</span><span class="sxs-lookup"><span data-stu-id="8c601-164">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="8c601-165">**handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="8c601-165">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="8c601-166">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="8c601-166">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8c601-167">**ignorare**</span><span class="sxs-lookup"><span data-stu-id="8c601-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="8c601-168">**ptr**</span><span class="sxs-lookup"><span data-stu-id="8c601-168">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="8c601-169">**ref**</span><span class="sxs-lookup"><span data-stu-id="8c601-169">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="8c601-170">**string**</span><span class="sxs-lookup"><span data-stu-id="8c601-170">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="8c601-171">**struct**</span><span class="sxs-lookup"><span data-stu-id="8c601-171">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="8c601-172">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="8c601-172">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="8c601-173">**typedef**</span><span class="sxs-lookup"><span data-stu-id="8c601-173">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="8c601-174">**Unione**</span><span class="sxs-lookup"><span data-stu-id="8c601-174">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="8c601-175">**unico**</span><span class="sxs-lookup"><span data-stu-id="8c601-175">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="8c601-176">**void**</span><span class="sxs-lookup"><span data-stu-id="8c601-176">**void**</span></span>](void.md)
</dt> </dl>

 

 