---
title: void (attributo)
description: Il tipo di base void indica una routine senza argomenti o una routine che non restituisce un valore di risultato.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- attributo void MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299189"
---
# <a name="void-attribute"></a><span data-ttu-id="524ac-104">void (attributo)</span><span class="sxs-lookup"><span data-stu-id="524ac-104">void attribute</span></span>

<span data-ttu-id="524ac-105">Il tipo di base **void** indica una routine senza argomenti o una routine che non restituisce un valore di risultato.</span><span class="sxs-lookup"><span data-stu-id="524ac-105">The base type **void** indicates a procedure with no arguments or a procedure that does not return a result value.</span></span>

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="524ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="524ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="524ac-107">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="524ac-107">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="524ac-108">Specifica il nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="524ac-108">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="524ac-109">*parameter-list*</span><span class="sxs-lookup"><span data-stu-id="524ac-109">*parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="524ac-110">Specifica l'elenco di parametri passati alla funzione insieme ai tipi di parametro e agli attributi dei parametri associati.</span><span class="sxs-lookup"><span data-stu-id="524ac-110">Specifies the list of parameters passed to the function along with the associated parameter types and parameter attributes.</span></span>

</dd> <dt>

<span data-ttu-id="524ac-111">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="524ac-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="524ac-112">Specifica il nome del tipo restituito dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="524ac-112">Specifies the name of the type returned by the function.</span></span>

</dd> <dt>

<span data-ttu-id="524ac-113">*context-handle-tipo*</span><span class="sxs-lookup"><span data-stu-id="524ac-113">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="524ac-114">Specifica il nome del tipo che accetta l'attributo dell' **\[** [**\_ handle di contesto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="524ac-114">Specifies the name of the type that takes the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="524ac-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="524ac-115">Remarks</span></span>

<span data-ttu-id="524ac-116">Il tipo di **puntatore \* void**, che in C descrive un puntatore generico di cui è possibile eseguire il cast per rappresentare qualsiasi tipo di puntatore, è limitato in MIDL al relativo utilizzo con la parola chiave dell' **\[ \_ handle \] di contesto** .</span><span class="sxs-lookup"><span data-stu-id="524ac-116">The pointer type **void \***, which in C describes a generic pointer that can be cast to represent any pointer type, is limited in MIDL to its use with the **\[context\_handle\]** keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="524ac-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="524ac-117">Examples</span></span>

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a><span data-ttu-id="524ac-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="524ac-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="524ac-119">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="524ac-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="524ac-120">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="524ac-120">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="524ac-121">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="524ac-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




