---
title: attributo implicit_handle
description: L'attributo \ Implicit \_ handle \ ACF specifica l'handle usato per le funzioni che non includono un handle esplicito come parametro di procedura.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- attributo implicit_handle MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857229"
---
# <a name="implicit_handle-attribute"></a><span data-ttu-id="d57d3-104">\_attributo handle implicito</span><span class="sxs-lookup"><span data-stu-id="d57d3-104">implicit\_handle attribute</span></span>

<span data-ttu-id="d57d3-105">L'attributo ACF dell' **\[ \_ handle \] implicito** specifica l'handle usato per le funzioni che non includono un handle esplicito come parametro di procedura.</span><span class="sxs-lookup"><span data-stu-id="d57d3-105">The **\[implicit\_handle\]** ACF attribute specifies the handle used for functions that do not include an explicit handle as a procedure parameter.</span></span>

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a><span data-ttu-id="d57d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d57d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57d3-107">*tipo di handle*</span><span class="sxs-lookup"><span data-stu-id="d57d3-107">*handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d57d3-108">Specifica il tipo di dati dell'handle, ad esempio l' [**handle \_**](handle-t.md) del tipo di base t o un tipo di handle definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d57d3-108">Specifies the handle data type, such as the base type [**handle\_t**](handle-t.md) or a user-defined handle type.</span></span>

</dd> <dt>

<span data-ttu-id="d57d3-109">*nome handle*</span><span class="sxs-lookup"><span data-stu-id="d57d3-109">*handle-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d57d3-110">Specifica il nome dell'handle.</span><span class="sxs-lookup"><span data-stu-id="d57d3-110">Specifies the name of the handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d57d3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d57d3-111">Remarks</span></span>

<span data-ttu-id="d57d3-112">L'handle specificato dall'attributo **\[ \_ handle \] implicito** viene utilizzato in modi diversi a seconda della natura della routine.</span><span class="sxs-lookup"><span data-stu-id="d57d3-112">The handle specified by the **\[implicit\_handle\]** attribute is used in different ways depending on the nature of the procedure.</span></span> <span data-ttu-id="d57d3-113">Se la procedura è remota, l'handle verrà usato come handle di binding per la chiamata remota.</span><span class="sxs-lookup"><span data-stu-id="d57d3-113">If the procedure is remote, the handle will be used as the binding handle for the remote call.</span></span> <span data-ttu-id="d57d3-114">L'handle implicito può essere usato anche per stabilire un'associazione iniziale per una funzione che usa un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="d57d3-114">The implicit handle may also be used to establish an initial binding for a function that uses a context handle.</span></span> <span data-ttu-id="d57d3-115">Se la procedura è una procedura di serializzazione, l'handle viene utilizzato come un handle di serializzazione che controlla l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d57d3-115">If the procedure is a serializing procedure, the handle is used as a serializing handle controlling the operation.</span></span> <span data-ttu-id="d57d3-116">Nel caso della serializzazione del tipo, l'handle viene utilizzato come handle di serializzazione per tutti i tipi serializzati.</span><span class="sxs-lookup"><span data-stu-id="d57d3-116">In the case of type serialization, the handle is used as the serialization handle for all the serialized types.</span></span>

<span data-ttu-id="d57d3-117">L'attributo **\[ \_ handle \] implicito** specifica una variabile globale che contiene un handle utilizzato da qualsiasi funzione che necessita di handle impliciti.</span><span class="sxs-lookup"><span data-stu-id="d57d3-117">The **\[implicit\_handle\]** attribute specifies a global variable that contains a handle used by any function needing implicit handles.</span></span>

<span data-ttu-id="d57d3-118">Il tipo di handle di binding implicito deve essere [**handle \_ t**](handle-t.md) (o un tipo basato su **handle \_ t**) o un tipo di handle definito dall'utente specificato con l'attributo [**handle**](handle.md) .</span><span class="sxs-lookup"><span data-stu-id="d57d3-118">The implicit binding handle type must be either [**handle\_t**](handle-t.md) (or a type based on **handle\_t**) or a user-defined handle type specified with the [**handle**](handle.md) attribute.</span></span> <span data-ttu-id="d57d3-119">L'handle di serializzazione implicita deve essere un tipo basato su **handle \_ t**.</span><span class="sxs-lookup"><span data-stu-id="d57d3-119">The implicit serializing handle must be a type based on **handle\_t**.</span></span>

<span data-ttu-id="d57d3-120">Se il tipo di handle implicito non è definito nel file IDL o nei file inclusi e importati dal file IDL per il computer MIDL, è necessario fornire il file contenente la definizione del tipo di handle quando si compilano gli stub.</span><span class="sxs-lookup"><span data-stu-id="d57d3-120">If the implicit handle type is not defined in the IDL file or in any files included and imported by the IDL file for the MIDL computer, you must supply the file containing the handle-type definition when you compile the stubs.</span></span> <span data-ttu-id="d57d3-121">Usare l'istruzione di [**inclusione**](include.md) di ACF per includere il file contenente la definizione del tipo di handle.</span><span class="sxs-lookup"><span data-stu-id="d57d3-121">Use the ACF [**include**](include.md) statement to include the file containing the handle-type definition.</span></span>

<span data-ttu-id="d57d3-122">L'attributo **\[ \_ handle \] implicito** può essere presente al massimo una volta.</span><span class="sxs-lookup"><span data-stu-id="d57d3-122">The **\[implicit\_handle\]** attribute can occur once, at most.</span></span> <span data-ttu-id="d57d3-123">L'attributo **\[ \_ handle \] implicito** può verificarsi solo [**\[ \_ \]**](auto-handle.md) se gli attributi handle automatico e [**\[ \_ handle \] esplicito**](explicit-handle.md) non vengono eseguiti.</span><span class="sxs-lookup"><span data-stu-id="d57d3-123">The **\[implicit\_handle\]** attribute can occur only if the [**\[auto\_handle\]**](auto-handle.md) and [**\[explicit\_handle\]**](explicit-handle.md) attributes do not occur.</span></span>

## <a name="examples"></a><span data-ttu-id="d57d3-124">Esempi</span><span class="sxs-lookup"><span data-stu-id="d57d3-124">Examples</span></span>

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a><span data-ttu-id="d57d3-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d57d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57d3-126">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="d57d3-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d57d3-127">**\_handle automatico**</span><span class="sxs-lookup"><span data-stu-id="d57d3-127">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="d57d3-128">**handle esplicito \_**</span><span class="sxs-lookup"><span data-stu-id="d57d3-128">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="d57d3-129">**handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="d57d3-129">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="d57d3-130">**includere**</span><span class="sxs-lookup"><span data-stu-id="d57d3-130">**include**</span></span>](include.md)
</dt> </dl>

 

 




