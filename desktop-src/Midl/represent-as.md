---
title: attributo represent_as
description: L'attributo \ rappresenta \_ As \ ACF associa un tipo locale denominato nella lingua di destinazione repr-Type con un tipo di trasferimento denominato-type trasferito tra client e server.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- attributo represent_as MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045474"
---
# <a name="represent_as-attribute"></a><span data-ttu-id="c4079-104">rappresenta \_ come attributo</span><span class="sxs-lookup"><span data-stu-id="c4079-104">represent\_as attribute</span></span>

<span data-ttu-id="c4079-105">L'attributo **\[ rappresenta \_ come \]** ACF associa un tipo locale denominato nel linguaggio di destinazione *repr-Type* con un tipo di trasferimento *denominato-type* trasferito tra client e server.</span><span class="sxs-lookup"><span data-stu-id="c4079-105">The **\[represent\_as\]** ACF attribute associates a named local type in the target language *repr-type* with a transfer type *named-type* that is transferred between client and server.</span></span>

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a><span data-ttu-id="c4079-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4079-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4079-107">*tipo denominato*</span><span class="sxs-lookup"><span data-stu-id="c4079-107">*named-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c4079-108">Specifica il tipo di dati di trasferimento denominato trasferiti tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="c4079-108">Specifies the named transfer data type that is transferred between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="c4079-109">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="c4079-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c4079-110">Specifica uno o più attributi che si applicano al tipo.</span><span class="sxs-lookup"><span data-stu-id="c4079-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="c4079-111">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="c4079-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c4079-112">*tipo di repr*</span><span class="sxs-lookup"><span data-stu-id="c4079-112">*repr-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c4079-113">Specifica il tipo locale rappresentato nella lingua di destinazione presentata alle applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="c4079-113">Specifies the represented local type in the target language that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4079-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4079-114">Remarks</span></span>

<span data-ttu-id="c4079-115">Quando si usa **\[ rappresenta \_ come \]**, è necessario specificare routine che convertono tra i tipi local e transfer e la memoria libera utilizzata per conservare i dati convertiti.</span><span class="sxs-lookup"><span data-stu-id="c4079-115">When using **\[represent\_as\]**, you must supply routines that convert between the local and the transfer types and that free memory used to hold the converted data.</span></span> <span data-ttu-id="c4079-116">L'attributo **\[ rappresenta \_ come \]** indica agli stub di chiamare le routine di conversione fornite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c4079-116">The **\[represent\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="c4079-117">Il tipo trasferito *denominato-type* deve essere risolto in un tipo di base MIDL, un tipo predefinito o un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="c4079-117">The transferred type *named-type* must resolve to a MIDL base type, predefined type, or to a type identifier.</span></span> <span data-ttu-id="c4079-118">Per altre informazioni, vedere [tipi di base MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="c4079-118">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="c4079-119">È necessario specificare le routine seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4079-119">You must supply the following routines:</span></span>



| <span data-ttu-id="c4079-120">Nome routine</span><span class="sxs-lookup"><span data-stu-id="c4079-120">Routine name</span></span>                   | <span data-ttu-id="c4079-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4079-121">Description</span></span>                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4079-122">*\_tipo denominato \* \* \* \_ da \_ locale*\*</span><span class="sxs-lookup"><span data-stu-id="c4079-122">*named\_type\*\*\*\_from\_local*\*</span></span> | <span data-ttu-id="c4079-123">Converte i dati dal tipo locale al tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="c4079-123">Converts data from the local type to the network type.</span></span> <span data-ttu-id="c4079-124">La routine alloca memoria per il tipo di dati di rete, inclusa la memoria per tutti i dati a cui fanno riferimento i puntatori nel tipo di dati di rete.</span><span class="sxs-lookup"><span data-stu-id="c4079-124">The routine allocates memory for the network data type, including memory for any data referenced by pointers in the network data type.</span></span>              |
| <span data-ttu-id="c4079-125">*\_tipo denominato \* \* \* \_ in \_ locale*\*</span><span class="sxs-lookup"><span data-stu-id="c4079-125">*named\_type\*\*\*\_to\_local*\*</span></span>   | <span data-ttu-id="c4079-126">Converte i dati dal tipo di rete al tipo locale.</span><span class="sxs-lookup"><span data-stu-id="c4079-126">Converts data from the network type to the local type.</span></span> <span data-ttu-id="c4079-127">La routine è responsabile dell'allocazione della memoria per i dati a cui fanno riferimento i puntatori nel tipo locale.</span><span class="sxs-lookup"><span data-stu-id="c4079-127">The routine is responsible for allocating memory for data referenced by pointers in the local type.</span></span> <span data-ttu-id="c4079-128">RPC alloca memoria per il tipo locale stesso.</span><span class="sxs-lookup"><span data-stu-id="c4079-128">RPC allocates memory for the local type itself.</span></span> |
| <span data-ttu-id="c4079-129">*\_tipo denominato \* \* \* \_ \_ locale disponibile*\*</span><span class="sxs-lookup"><span data-stu-id="c4079-129">*named\_type\*\*\*\_free\_local*\*</span></span> | <span data-ttu-id="c4079-130">Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo locale.</span><span class="sxs-lookup"><span data-stu-id="c4079-130">Frees memory allocated for data referenced by pointers in the local type.</span></span> <span data-ttu-id="c4079-131">RPC libera memoria per il tipo stesso</span><span class="sxs-lookup"><span data-stu-id="c4079-131">RPC frees memory for the type itself</span></span>                                                                                             |
| <span data-ttu-id="c4079-132">*\_tipo denominato \* \* \* \_ \_ inst libero*\*</span><span class="sxs-lookup"><span data-stu-id="c4079-132">*named\_type\*\*\*\_free\_inst*\*</span></span>  | <span data-ttu-id="c4079-133">Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo di rete e per il tipo di rete stesso.</span><span class="sxs-lookup"><span data-stu-id="c4079-133">Frees memory allocated for the data referenced by pointers in the network type and for the network type itself.</span></span>                                                                                            |



 

<span data-ttu-id="c4079-134">Lo stub client chiama \*\* \* \* \_ da \_ local\*\* per allocare spazio per il tipo trasmesso e per tradurre i dati dal tipo locale al tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="c4079-134">The client stub calls *named-type\*\*\*\_from\_local*\* to allocate space for the transmitted type and to translate the data from the local type to the network type.</span></span> <span data-ttu-id="c4079-135">Lo stub del server alloca spazio per il tipo di dati originale e chiama il *tipo denominato \* \* \* \_ a \_ local*\* per tradurre i dati dal tipo di rete al tipo locale.</span><span class="sxs-lookup"><span data-stu-id="c4079-135">The server stub allocates space for the original data type and calls *named-type\*\*\*\_to\_local*\* to translate the data from the network type to the local type.</span></span>

<span data-ttu-id="c4079-136">Al ritorno dal codice dell'applicazione, il client e il server Stub chiamano il *tipo denominato \* \* \* \_ Free \_ inst*\* per deallocare l'archiviazione per il tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="c4079-136">Upon return from the application code, the client and server stubs call *named-type\*\*\*\_free\_inst*\* to deallocate the storage for network type.</span></span> <span data-ttu-id="c4079-137">Per la deallocazione dell'archiviazione restituita dalla routine, lo stub client chiama il \*tipo denominato \* \* \* \_ \_ local libero\*\*.</span><span class="sxs-lookup"><span data-stu-id="c4079-137">The client stub calls *named-type\*\*\*\_free\_local*\* to deallocate storage returned by the routine.</span></span>

<span data-ttu-id="c4079-138">I tipi seguenti non possono avere un oggetto **\[ rappresentato \_ come \]** attributo:</span><span class="sxs-lookup"><span data-stu-id="c4079-138">The following types cannot have a **\[represent\_as\]** attribute:</span></span>

-   <span data-ttu-id="c4079-139">Matrici conformi, variabili o conformi.</span><span class="sxs-lookup"><span data-stu-id="c4079-139">Conformant, varying, or conformant-varying arrays</span></span>
-   <span data-ttu-id="c4079-140">Strutture in cui l'ultimo membro è una matrice conforme (struttura conforme)</span><span class="sxs-lookup"><span data-stu-id="c4079-140">Structures in which the last member is a conformant array (a conformant structure)</span></span>
-   <span data-ttu-id="c4079-141">Puntatori o tipi che contengono un puntatore</span><span class="sxs-lookup"><span data-stu-id="c4079-141">Pointers or types that contain a pointer</span></span>
-   <span data-ttu-id="c4079-142">Pipe o tipi che contengono pipe</span><span class="sxs-lookup"><span data-stu-id="c4079-142">Pipes or types that contain pipes</span></span>
-   <span data-ttu-id="c4079-143">Tipi utilizzati come tipo di base per una pipe</span><span class="sxs-lookup"><span data-stu-id="c4079-143">Types that are used as the base type for a pipe</span></span>
-   <span data-ttu-id="c4079-144">Handle di tipi [**predefiniti \_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="c4079-144">Predefined types [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>
-   <span data-ttu-id="c4079-145">Tipi con attributo [**\[ handle \]**](handle.md)</span><span class="sxs-lookup"><span data-stu-id="c4079-145">Types that have the [**\[handle\]**](handle.md) attribute</span></span>

## <a name="examples"></a><span data-ttu-id="c4079-146">Esempi</span><span class="sxs-lookup"><span data-stu-id="c4079-146">Examples</span></span>

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a><span data-ttu-id="c4079-147">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c4079-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4079-148">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="c4079-148">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="c4079-149">**matrici**</span><span class="sxs-lookup"><span data-stu-id="c4079-149">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="c4079-150">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="c4079-150">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="c4079-151">**handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="c4079-151">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="c4079-152">**typedef**</span><span class="sxs-lookup"><span data-stu-id="c4079-152">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="c4079-153">**void**</span><span class="sxs-lookup"><span data-stu-id="c4079-153">**void**</span></span>](void.md)
</dt> </dl>

 

 




