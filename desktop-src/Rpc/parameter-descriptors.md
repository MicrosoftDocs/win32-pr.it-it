---
title: Descrittori di parametro
description: Come indicato in precedenza, 8211; OI e \ 8211; descrittori di parametro di stile OIF sono disponibili.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729410"
---
# <a name="parameter-descriptors"></a><span data-ttu-id="8d432-103">Descrittori di parametro</span><span class="sxs-lookup"><span data-stu-id="8d432-103">Parameter Descriptors</span></span>

<span data-ttu-id="8d432-104">Come indicato in precedenza, esistono descrittori di parametro di stile [**– OI**](/windows/desktop/Midl/-oi) e **– OIF** .</span><span class="sxs-lookup"><span data-stu-id="8d432-104">As mentioned previously, [**–Oi**](/windows/desktop/Midl/-oi) and **–Oif** style parameter descriptors exist.</span></span>

## <a name="the-oi-parameter-descriptors"></a><span data-ttu-id="8d432-105">Descrittori di parametro – OI</span><span class="sxs-lookup"><span data-stu-id="8d432-105">The –Oi Parameter Descriptors</span></span>

<span data-ttu-id="8d432-106">Gli stub completamente interpretati richiedono informazioni aggiuntive per ogni parametro in una chiamata RPC.</span><span class="sxs-lookup"><span data-stu-id="8d432-106">Fully interpreted stubs require additional information for each of the parameters in an RPC call.</span></span> <span data-ttu-id="8d432-107">Le descrizioni dei parametri di una procedura seguono immediatamente dopo la descrizione della procedura.</span><span class="sxs-lookup"><span data-stu-id="8d432-107">The parameter descriptions of a procedure follow immediately after the description of the procedure.</span></span>

[<span data-ttu-id="8d432-108">**Semplice-OI**</span><span class="sxs-lookup"><span data-stu-id="8d432-108">**Simple –Oi**</span></span>](/windows/desktop/Midl/-oi)

<span data-ttu-id="8d432-109">**Descrittori di parametro**</span><span class="sxs-lookup"><span data-stu-id="8d432-109">**Parameter Descriptors**</span></span>

<span data-ttu-id="8d432-110">Il formato per la descrizione di un \[  \] parametro di tipo semplice in o restituito è:</span><span class="sxs-lookup"><span data-stu-id="8d432-110">The format for the description of an \[**in**\] or return simple type parameter is:</span></span>

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="8d432-111">–oppure–</span><span class="sxs-lookup"><span data-stu-id="8d432-111">–or–</span></span>

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="8d432-112">Dove il \_ tipo semplice<1> è il token FC che indica il tipo semplice.</span><span class="sxs-lookup"><span data-stu-id="8d432-112">Where simple\_type<1> is the FC token indicating the simple type.</span></span> <span data-ttu-id="8d432-113">I codici sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d432-113">The codes are as follows:</span></span>

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

<span data-ttu-id="8d432-114">**Altro-OI**</span><span class="sxs-lookup"><span data-stu-id="8d432-114">**Other –Oi**</span></span>

<span data-ttu-id="8d432-115">**Descrittori di parametro**</span><span class="sxs-lookup"><span data-stu-id="8d432-115">**Parameter Descriptors**</span></span>

<span data-ttu-id="8d432-116">Il formato per la descrizione di tutti gli altri tipi di parametro è:</span><span class="sxs-lookup"><span data-stu-id="8d432-116">The format for the description for all other parameter types is:</span></span>

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

<span data-ttu-id="8d432-117">Dove la \_ direzione param<1> campo per ognuna di queste descrizioni deve essere uno dei seguenti elementi indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8d432-117">Where the param\_direction<1> field for each of these descriptions must be one of those shown in the following table.</span></span>



| <span data-ttu-id="8d432-118">Hex</span><span class="sxs-lookup"><span data-stu-id="8d432-118">Hex</span></span> | <span data-ttu-id="8d432-119">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="8d432-119">Flag</span></span>                          | <span data-ttu-id="8d432-120">Significato</span><span class="sxs-lookup"><span data-stu-id="8d432-120">Meaning</span></span>                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8d432-121">4D</span><span class="sxs-lookup"><span data-stu-id="8d432-121">4d</span></span>  | <span data-ttu-id="8d432-122">FC \_ in \_ param</span><span class="sxs-lookup"><span data-stu-id="8d432-122">FC\_IN\_PARAM</span></span>                 | <span data-ttu-id="8d432-123">Parametro in.</span><span class="sxs-lookup"><span data-stu-id="8d432-123">An in parameter.</span></span>                                            |
| <span data-ttu-id="8d432-124">50</span><span class="sxs-lookup"><span data-stu-id="8d432-124">50</span></span>  | <span data-ttu-id="8d432-125">FC \_ in \_ uscita \_ param</span><span class="sxs-lookup"><span data-stu-id="8d432-125">FC\_IN\_OUT\_PARAM</span></span>            | <span data-ttu-id="8d432-126">Parametro in/out.</span><span class="sxs-lookup"><span data-stu-id="8d432-126">An in/out parameter.</span></span>                                        |
| <span data-ttu-id="8d432-127">51</span><span class="sxs-lookup"><span data-stu-id="8d432-127">51</span></span>  | <span data-ttu-id="8d432-128">\_param out \_ FC</span><span class="sxs-lookup"><span data-stu-id="8d432-128">FC\_OUT\_PARAM</span></span>                | <span data-ttu-id="8d432-129">Parametro out.</span><span class="sxs-lookup"><span data-stu-id="8d432-129">An out parameter.</span></span>                                           |
| <span data-ttu-id="8d432-130">52</span><span class="sxs-lookup"><span data-stu-id="8d432-130">52</span></span>  | <span data-ttu-id="8d432-131">\_param return \_ FC</span><span class="sxs-lookup"><span data-stu-id="8d432-131">FC\_RETURN\_PARAM</span></span>             | <span data-ttu-id="8d432-132">Valore restituito di una routine.</span><span class="sxs-lookup"><span data-stu-id="8d432-132">A procedure return value.</span></span>                                   |
| <span data-ttu-id="8d432-133">4F</span><span class="sxs-lookup"><span data-stu-id="8d432-133">4f</span></span>  | <span data-ttu-id="8d432-134">FC \_ in \_ param \_ senza \_ \_ inst libero</span><span class="sxs-lookup"><span data-stu-id="8d432-134">FC\_IN\_PARAM\_NO\_FREE\_INST</span></span> | <span data-ttu-id="8d432-135">Oggetto in Xmit/Rep come parametro per il quale non viene liberato.</span><span class="sxs-lookup"><span data-stu-id="8d432-135">An in xmit/rep as a parameter for which no freeing is made.</span></span> |



 

<span data-ttu-id="8d432-136">La dimensione dello stack \_<1> corrisponde alla dimensione del parametro nello stack, espressa come numero di numeri interi che il parametro occupa nello stack.</span><span class="sxs-lookup"><span data-stu-id="8d432-136">The stack\_size<1> is the size of the parameter on the stack, expressed as the number of integers the parameter occupies on the stack.</span></span>

> [!Note]  
> <span data-ttu-id="8d432-137">La modalità [**-OI**](/windows/desktop/Midl/-oi) non è supportata nelle piattaforme a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="8d432-137">The [**–Oi**](/windows/desktop/Midl/-oi) mode is not supported on 64-bit platforms.</span></span>

 

<span data-ttu-id="8d432-138">L'offset del tipo \_<2> campo è l'offset nella tabella della stringa di formato del tipo, che indica il descrittore di tipo per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="8d432-138">The type\_offset<2> field is the offset in the type format string table, indicating the type descriptor for the argument.</span></span>

## <a name="the-oif-parameter-descriptors"></a><span data-ttu-id="8d432-139">Descrittori di parametro – OIF</span><span class="sxs-lookup"><span data-stu-id="8d432-139">The –Oif Parameter Descriptors</span></span>

<span data-ttu-id="8d432-140">Esistono due formati possibili per la descrizione di un parametro, uno per i tipi di base, un altro per tutti gli altri tipi.</span><span class="sxs-lookup"><span data-stu-id="8d432-140">There are two possible formats for a parameter description, one for base types, another for all other types.</span></span>

<span data-ttu-id="8d432-141">Tipi di base:</span><span class="sxs-lookup"><span data-stu-id="8d432-141">Base types:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

<span data-ttu-id="8d432-142">Altro:</span><span class="sxs-lookup"><span data-stu-id="8d432-142">Other:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

<span data-ttu-id="8d432-143">In entrambi \_ gli offset dello stack<2> indica l'offset nello stack di argomenti virtuale, espresso in byte.</span><span class="sxs-lookup"><span data-stu-id="8d432-143">In both stack\_offset<2> indicates the offset on the virtual argument stack, in bytes.</span></span> <span data-ttu-id="8d432-144">Per i tipi di base, il tipo di argomento viene fornito direttamente dal carattere di formato corrispondente al tipo.</span><span class="sxs-lookup"><span data-stu-id="8d432-144">For base types, the argument type is given directly by the format character corresponding to the type.</span></span> <span data-ttu-id="8d432-145">Per gli altri tipi, il \_ campo Offset tipo<2> fornisce l'offset nella tabella della stringa di formato del tipo in cui si trova il descrittore di tipo per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="8d432-145">For other types, the type\_offset<2> field gives the offset in the type format string table where the type descriptor for the argument is located.</span></span>

<span data-ttu-id="8d432-146">Il campo attributo parametro è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="8d432-146">The parameter attribute field is defined as follows:</span></span>

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   <span data-ttu-id="8d432-147">Il bit **MustSize** viene impostato solo se il parametro deve essere ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="8d432-147">The **MustSize** bit is set only if the parameter must be sized.</span></span>
-   <span data-ttu-id="8d432-148">Se il server deve chiamare la routine NdrFree del parametro, viene impostato il bit **MustFree** \* .</span><span class="sxs-lookup"><span data-stu-id="8d432-148">The **MustFree** bit is set if the server must call the parameter's NdrFree\* routine.</span></span>
-   <span data-ttu-id="8d432-149">Il bit **IsSimpleRef** è impostato per un parametro che è un puntatore di riferimento a un elemento diverso da un altro puntatore e senza attributi di allocazione.</span><span class="sxs-lookup"><span data-stu-id="8d432-149">The **IsSimpleRef** bit is set for a parameter that is a reference pointer to anything other than another pointer, and which has no allocate attributes.</span></span> <span data-ttu-id="8d432-150">Per tale tipo, l'offset del tipo della descrizione del parametro \_<> campo, ad eccezione di un puntatore di riferimento a un tipo di base, fornisce l'offset al tipo di referente. il puntatore di riferimento viene semplicemente ignorato.</span><span class="sxs-lookup"><span data-stu-id="8d432-150">For such a type, the parameter description's type\_offset<> field, except for a reference pointer to a base type, provides the offset to the referent's type; the reference pointer is simply skipped.</span></span>
-   <span data-ttu-id="8d432-151">Il bit **IsDontCallFreeInst** è impostato per determinate rappresentazioni \_ come parametri le cui routine di istanza gratuite non devono essere chiamate.</span><span class="sxs-lookup"><span data-stu-id="8d432-151">The **IsDontCallFreeInst** bit is set for certain represent\_as parameters whose free instance routines should not be called.</span></span>
-   <span data-ttu-id="8d432-152">I bit **ServerAllocSize** sono diversi da zero se il parametro è \[ **out** \] , \[ **in** \] o \[ **in, out** \] pointer to Pointer o pointer to enum16 e verrà inizializzato nello stack dell'interprete server, invece di usare una chiamata a **i \_ RpcAllocate**.</span><span class="sxs-lookup"><span data-stu-id="8d432-152">The **ServerAllocSize** bits are nonzero if the parameter is \[**out**\], \[**in**\], or \[**in,out**\] pointer to pointer, or pointer to enum16, and will be initialized on the server interpreter's stack, rather than using a call to **I\_RpcAllocate**.</span></span> <span data-ttu-id="8d432-153">Se è diverso da zero, questo valore viene moltiplicato per 8 per ottenere il numero di byte per il parametro.</span><span class="sxs-lookup"><span data-stu-id="8d432-153">If nonzero, this value is multiplied by 8 to get the number of bytes for the parameter.</span></span> <span data-ttu-id="8d432-154">Si noti che questa operazione significa che almeno 8 byte vengono sempre allocati per un puntatore.</span><span class="sxs-lookup"><span data-stu-id="8d432-154">Note that doing so means at least 8 bytes are always allocated for a pointer.</span></span>
-   <span data-ttu-id="8d432-155">Il bit **IsBasetype** è impostato per i tipi semplici di cui viene eseguito il marshalling dal ciclo principale dell'interprete [**OIF**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="8d432-155">The **IsBasetype** bit is set for simple types that are being marshaled by the main [**–Oif**](/windows/desktop/Midl/-oi) interpreter loop.</span></span> <span data-ttu-id="8d432-156">In particolare, un tipo semplice con un attributo di intervallo su di esso non è contrassegnato come tipo di base per forzare il marshalling della routine di intervallo tramite l'invio tramite un \_ token di intervallo FC.</span><span class="sxs-lookup"><span data-stu-id="8d432-156">In particular, a simple type with a range attribute on it is not flagged as a base type in order to force the range routine marshaling through dispatching using an FC\_RANGE token.</span></span>
-   <span data-ttu-id="8d432-157">Il bit **IsByValue** è impostato per i tipi composti inviati per valore, ma non è impostato per i tipi semplici, indipendentemente dal fatto che l'argomento sia un puntatore.</span><span class="sxs-lookup"><span data-stu-id="8d432-157">The **IsByValue** bit is set for compound types being sent by value, but is not set for simple types, regardless of whether the argument is a pointer.</span></span> <span data-ttu-id="8d432-158">I tipi composti per i quali è impostata sono strutture, unioni, [**trasmissione \_ come**](/windows/desktop/Midl/transmit-as), [**rappresentano \_ come**](/windows/desktop/Midl/represent-as), [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) e SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="8d432-158">The compound types for which it is set are structures, unions, [**transmit\_as**](/windows/desktop/Midl/transmit-as), [**represent\_as**](/windows/desktop/Midl/represent-as), [**wire\_marshal**](/windows/desktop/Midl/wire-marshal) and SAFEARRAY.</span></span> <span data-ttu-id="8d432-159">In generale, il bit è stato introdotto per il vantaggio del ciclo dell'interprete principale nell'interprete [**-Oicf**](/windows/desktop/Midl/-oi) , per garantire che gli argomenti non semplici (definiti argomenti di tipo composto) siano dereferenziati correttamente.</span><span class="sxs-lookup"><span data-stu-id="8d432-159">In general, the bit was introduced for the benefit of the main interpreter loop in the [**–Oicf**](/windows/desktop/Midl/-oi) interpreter, to ensure the nonsimple arguments (referred to as compound type arguments) are properly dereferenced.</span></span> <span data-ttu-id="8d432-160">Questo bit non è mai stato usato nelle versioni precedenti dell'interprete.</span><span class="sxs-lookup"><span data-stu-id="8d432-160">This bit was never used in previous versions of the interpreter.</span></span>

 

 