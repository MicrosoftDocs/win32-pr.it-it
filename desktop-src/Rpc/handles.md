---
title: Selettori
description: Fino a due parti nella descrizione della stringa di formato di un handle di indirizzo di una procedura.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338718"
---
# <a name="handles"></a><span data-ttu-id="2fc13-103">Selettori</span><span class="sxs-lookup"><span data-stu-id="2fc13-103">Handles</span></span>

<span data-ttu-id="2fc13-104">Fino a due parti nella descrizione della stringa di formato di un handle di indirizzo di una procedura.</span><span class="sxs-lookup"><span data-stu-id="2fc13-104">As many as two parts in the format string description of a procedure address handles.</span></span> <span data-ttu-id="2fc13-105">La prima parte è il \_ tipo di handle<1> campo della descrizione di una stored procedure, usato per indicare gli handle impliciti.</span><span class="sxs-lookup"><span data-stu-id="2fc13-105">The first part is the handle\_type<1> field of a procedure's description, used to indicate implicit handles.</span></span> <span data-ttu-id="2fc13-106">Questa parte è sempre presente.</span><span class="sxs-lookup"><span data-stu-id="2fc13-106">This part is always present.</span></span> <span data-ttu-id="2fc13-107">La seconda parte è una descrizione di parametro di qualsiasi handle esplicito nella procedura.</span><span class="sxs-lookup"><span data-stu-id="2fc13-107">The second part is a parameter description of any explicit handle in the procedure.</span></span> <span data-ttu-id="2fc13-108">Entrambe le sezioni riportate di seguito, insieme a una descrizione del supporto del compilatore MIDL aggiuntivo della struttura del descrittore stub per i problemi di gestione delle associazioni.</span><span class="sxs-lookup"><span data-stu-id="2fc13-108">Both are explained in the following sections, along with a discussion of the additional MIDL compiler support of the Stub Descriptor structure for binding handle issues.</span></span>

## <a name="implicit-handles"></a><span data-ttu-id="2fc13-109">Handle impliciti</span><span class="sxs-lookup"><span data-stu-id="2fc13-109">Implicit Handles</span></span>

<span data-ttu-id="2fc13-110">Se una stored procedure utilizza un handle implicito per l'associazione, il tipo di handle \_<1> campo della descrizione della procedura contiene uno dei tre valori diversi da zero validi.</span><span class="sxs-lookup"><span data-stu-id="2fc13-110">If a procedure uses an implicit handle for binding, the handle\_type<1> field of the procedure's description contains one of three valid nonzero values.</span></span> <span data-ttu-id="2fc13-111">Il supporto del compilatore MIDL per gli handle impliciti è disponibile nel \_ campo informazioni handle implicite \_ della struttura del descrittore Stub:</span><span class="sxs-lookup"><span data-stu-id="2fc13-111">MIDL compiler support for implicit handles is found in the IMPLICIT\_HANDLE\_INFO field of the Stub Descriptor structure:</span></span>

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

<span data-ttu-id="2fc13-112">Se la stored procedure utilizza un handle automatico, il membro **pAutoHandle** contiene l'indirizzo della variabile dello stub definita-handle automatico.</span><span class="sxs-lookup"><span data-stu-id="2fc13-112">If the procedure uses an auto handle, the **pAutoHandle** member contains the address of the stub defined–auto handle variable.</span></span>

<span data-ttu-id="2fc13-113">Se la stored procedure utilizza un handle primitivo implicito, il membro **pPrimitiveHandle** contiene l'indirizzo della variabile di handle primitiva definita dallo stub.</span><span class="sxs-lookup"><span data-stu-id="2fc13-113">If the procedure uses an implicit primitive handle, the **pPrimitiveHandle** member contains the address of the stub defined–primitive handle variable.</span></span>

<span data-ttu-id="2fc13-114">Infine, se la stored procedure utilizza un handle generico implicito, il membro **pGenericBindingInfo** contiene l'indirizzo del puntatore alla struttura **di \_ \_ informazioni di associazione generica** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2fc13-114">Finally, if the procedure uses an implicit generic handle, the **pGenericBindingInfo** member holds the address of the pointer to the corresponding **GENERIC\_BINDING\_INFO** structure.</span></span> <span data-ttu-id="2fc13-115">La **\_ \_ Descrizione dello stub MIDL** della struttura di dati contiene un puntatore a una raccolta di strutture di **\_ \_ coppie di associazioni generiche** .</span><span class="sxs-lookup"><span data-stu-id="2fc13-115">The data structure **MIDL\_STUB\_DESC** contains a pointer to a collection of **GENERIC\_BINDING\_PAIR** structures.</span></span> <span data-ttu-id="2fc13-116">La voce nella posizione zero di questa raccolta è riservata alle routine **Bind** e **UNBIND** corrispondenti all'handle di associazione generico a cui fa riferimento **PGenericBindingInfo** nelle **\_ \_ informazioni di handle implicite**.</span><span class="sxs-lookup"><span data-stu-id="2fc13-116">The entry in the zero position of this collection is reserved for the **bind** and **unbind** routines corresponding to the generic binding handle referenced by **pGenericBindingInfo** in **IMPLICIT\_HANDLE\_INFO**.</span></span> <span data-ttu-id="2fc13-117">Il tipo di handle di associazione implicito è indicato nella stringa di formato.</span><span class="sxs-lookup"><span data-stu-id="2fc13-117">The type of implicit binding handle is indicated in the format string.</span></span>

## <a name="explicit-handles"></a><span data-ttu-id="2fc13-118">Handle espliciti</span><span class="sxs-lookup"><span data-stu-id="2fc13-118">Explicit Handles</span></span>

<span data-ttu-id="2fc13-119">Esistono tre possibili tipi di handle espliciti: context, Generic e primitive.</span><span class="sxs-lookup"><span data-stu-id="2fc13-119">There are three possible explicit handle types: context, generic, and primitive.</span></span> <span data-ttu-id="2fc13-120">Nel caso di un handle esplicito (o un \[  \] handle del contesto solo in uscita, gestito allo stesso modo), le informazioni dell'handle di associazione vengono visualizzate come uno dei parametri della procedura.</span><span class="sxs-lookup"><span data-stu-id="2fc13-120">In the case of an explicit handle (or an \[**out**\] only context handle, which is handled in the same way), the binding handle information appears as one of the procedure's parameters.</span></span> <span data-ttu-id="2fc13-121">Le tre possibili descrizioni sono le seguenti.</span><span class="sxs-lookup"><span data-stu-id="2fc13-121">The three possible descriptions are as follows.</span></span>

<span data-ttu-id="2fc13-122">Primitiva</span><span class="sxs-lookup"><span data-stu-id="2fc13-122">Primitive</span></span>

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

<span data-ttu-id="2fc13-123">Il flag<1> indica se l'handle viene passato da un puntatore.</span><span class="sxs-lookup"><span data-stu-id="2fc13-123">The flag<1> indicates whether the handle is passed by a pointer.</span></span>

<span data-ttu-id="2fc13-124">L'offset<2> fornisce l'offset dall'inizio dello stack all'handle primitivo.</span><span class="sxs-lookup"><span data-stu-id="2fc13-124">The offset<2> provides the offset from the beginning of the stack to the primitive handle.</span></span>

> [!Note]  
> <span data-ttu-id="2fc13-125">Una descrizione dell'handle primitivo nella stringa di formato del tipo è ridotta a un singolo FC \_ Ignore.</span><span class="sxs-lookup"><span data-stu-id="2fc13-125">A primitive handle description in the type format string is reduced to a single FC\_IGNORE.</span></span>

 

<span data-ttu-id="2fc13-126">Generico</span><span class="sxs-lookup"><span data-stu-id="2fc13-126">Generic</span></span>

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

<span data-ttu-id="2fc13-127">Il flag \_ e le \_ dimensioni<1> hanno il flag superiore e il bocconcino di dimensioni inferiori.</span><span class="sxs-lookup"><span data-stu-id="2fc13-127">The flag\_and \_size<1> has the upper flag nibble and the lower size nibble.</span></span> <span data-ttu-id="2fc13-128">Il flag indica se l'handle viene passato da un puntatore.</span><span class="sxs-lookup"><span data-stu-id="2fc13-128">The flag indicates whether the handle is passed by a pointer.</span></span> <span data-ttu-id="2fc13-129">Il campo dimensione fornisce le dimensioni del tipo di handle generico definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2fc13-129">The size field provides the size of the user defined–generic handle type.</span></span> <span data-ttu-id="2fc13-130">Questa dimensione è limitata a 1, 2 o 4 byte nei sistemi a 32 bit e 1, 2, 4 o 8 byte nei sistemi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2fc13-130">This size is limited to be 1, 2 or 4 bytes on 32-bit systems and 1, 2, 4 or 8 bytes on 64-bit systems.</span></span>

<span data-ttu-id="2fc13-131">Il campo Offset<2> fornisce l'offset dall'inizio dello stack del puntatore ai dati delle dimensioni specificate.</span><span class="sxs-lookup"><span data-stu-id="2fc13-131">The offset<2> field provides the offset from the beginning of the stack of the pointer to the data of the size given.</span></span>

<span data-ttu-id="2fc13-132">L' \_ \_ Indice pair di routine di associazione \_<1> campo fornisce l'indice nel campo AGenericBindingRoutinePairs del descrittore Stub ai puntatori a funzione di routine **Bind** e **UNBIND** per l'handle generico.</span><span class="sxs-lookup"><span data-stu-id="2fc13-132">The binding\_routine\_pair\_index<1> field gives the index into the aGenericBindingRoutinePairs field of the Stub Descriptor to the **bind** and **unbind** routine function pointers for the generic handle.</span></span>

> [!Note]  
> <span data-ttu-id="2fc13-133">Una descrizione di handle generica nel formato del tipo è la descrizione solo del tipo di dati correlato.</span><span class="sxs-lookup"><span data-stu-id="2fc13-133">A generic handle description in the type format is the description of the related data type only.</span></span>

 

<span data-ttu-id="2fc13-134">Context</span><span class="sxs-lookup"><span data-stu-id="2fc13-134">Context</span></span>

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

<span data-ttu-id="2fc13-135">I flag<1> indicano il modo in cui viene passato l'handle e il tipo.</span><span class="sxs-lookup"><span data-stu-id="2fc13-135">The flags<1> indicate how the handle is passed and what type it is.</span></span> <span data-ttu-id="2fc13-136">I flag validi sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2fc13-136">Valid flags are shown in the following table.</span></span>



| <span data-ttu-id="2fc13-137">Hex</span><span class="sxs-lookup"><span data-stu-id="2fc13-137">Hex</span></span> | <span data-ttu-id="2fc13-138">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="2fc13-138">Flag</span></span>                                   |
|-----|----------------------------------------|
| <span data-ttu-id="2fc13-139">80</span><span class="sxs-lookup"><span data-stu-id="2fc13-139">80</span></span>  | <span data-ttu-id="2fc13-140">il \_ parametro handle \_ è \_ tramite \_ ptr</span><span class="sxs-lookup"><span data-stu-id="2fc13-140">HANDLE\_PARAM\_IS\_VIA\_PTR</span></span>            |
| <span data-ttu-id="2fc13-141">40</span><span class="sxs-lookup"><span data-stu-id="2fc13-141">40</span></span>  | <span data-ttu-id="2fc13-142">il \_ parametro handle \_ è \_ in</span><span class="sxs-lookup"><span data-stu-id="2fc13-142">HANDLE\_PARAM\_IS\_IN</span></span>                  |
| <span data-ttu-id="2fc13-143">20</span><span class="sxs-lookup"><span data-stu-id="2fc13-143">20</span></span>  | <span data-ttu-id="2fc13-144">il \_ parametro handle \_ è \_ out</span><span class="sxs-lookup"><span data-stu-id="2fc13-144">HANDLE\_PARAM\_IS\_OUT</span></span>                 |
| <span data-ttu-id="2fc13-145">21</span><span class="sxs-lookup"><span data-stu-id="2fc13-145">21</span></span>  | <span data-ttu-id="2fc13-146">il \_ parametro handle \_ viene \_ restituito</span><span class="sxs-lookup"><span data-stu-id="2fc13-146">HANDLE\_PARAM\_IS\_RETURN</span></span>              |
| <span data-ttu-id="2fc13-147">08</span><span class="sxs-lookup"><span data-stu-id="2fc13-147">08</span></span>  | <span data-ttu-id="2fc13-148">\_handle di \_ contesto RIGOROSo NDR \_</span><span class="sxs-lookup"><span data-stu-id="2fc13-148">NDR\_STRICT\_CONTEXT\_HANDLE</span></span>           |
| <span data-ttu-id="2fc13-149">04</span><span class="sxs-lookup"><span data-stu-id="2fc13-149">04</span></span>  | <span data-ttu-id="2fc13-150">\_handle di contesto NDR \_ \_ senza \_ serializzazione</span><span class="sxs-lookup"><span data-stu-id="2fc13-150">NDR\_CONTEXT\_HANDLE\_NO\_SERIALIZE</span></span>    |
| <span data-ttu-id="2fc13-151">02</span><span class="sxs-lookup"><span data-stu-id="2fc13-151">02</span></span>  | <span data-ttu-id="2fc13-152">\_ \_ serializzazione handle di contesto NDR \_</span><span class="sxs-lookup"><span data-stu-id="2fc13-152">NDR\_CONTEXT\_HANDLE\_SERIALIZE</span></span>        |
| <span data-ttu-id="2fc13-153">01</span><span class="sxs-lookup"><span data-stu-id="2fc13-153">01</span></span>  | <span data-ttu-id="2fc13-154">l' \_ handle del contesto NDR \_ \_ non può \_ essere \_ null</span><span class="sxs-lookup"><span data-stu-id="2fc13-154">NDR\_CONTEXT\_HANDLE\_CANNOT\_BE\_NULL</span></span> |



 

<span data-ttu-id="2fc13-155">I primi quattro flag sono sempre presenti, le ultime quattro sono state aggiunte in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2fc13-155">The first four flags have always been present, the last four were added in Windows 2000.</span></span>

<span data-ttu-id="2fc13-156">Il campo Offset<2> fornisce l'offset dall'inizio dello stack all'handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="2fc13-156">The offset<2> field provides the offset from the start of the stack to the context handle.</span></span>

<span data-ttu-id="2fc13-157">L' \_ \_ indice di routine rundown del contesto \_<1> fornisce un indice nel campo **apfnNdrRundownRoutines** del descrittore dello stub alla routine di rundown utilizzata per questo handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="2fc13-157">The context\_rundown\_routine\_index<1> provides an index into the **apfnNdrRundownRoutines** field of the Stub Descriptor to the rundown routine used for this context handle.</span></span> <span data-ttu-id="2fc13-158">Il compilatore genera sempre un indice.</span><span class="sxs-lookup"><span data-stu-id="2fc13-158">The compiler always generates an index.</span></span> <span data-ttu-id="2fc13-159">Per routine che non dispongono di una routine di rundown, questo è un indice di una posizione della tabella che contiene null.</span><span class="sxs-lookup"><span data-stu-id="2fc13-159">For routines that do not have a rundown routine, this is an index to a table position that holds null.</span></span>

<span data-ttu-id="2fc13-160">Per gli stub compilati in **-Oi2**, il parametro \_ num<1> fornisce il numero ordinale, a partire da zero, che specifica quale handle del contesto si trova nella procedura specificata.</span><span class="sxs-lookup"><span data-stu-id="2fc13-160">For stubs built in **–Oi2**, the param\_num<1> provides the ordinal count, starting at zero, specifying which context handle it is in the given procedure.</span></span>

<span data-ttu-id="2fc13-161">Per le versioni precedenti dell'interprete, il param \_ num<1> fornisce il numero di parametro dell'handle di contesto, a partire da zero, nella relativa procedura.</span><span class="sxs-lookup"><span data-stu-id="2fc13-161">For previous versions of the interpreter, the param\_num<1> provides the context handle's parameter number, starting at zero, in its procedure.</span></span>

> [!Note]  
> <span data-ttu-id="2fc13-162">Una descrizione dell'handle di contesto nella stringa di formato del tipo non avrà l'offset<2> nella descrizione.</span><span class="sxs-lookup"><span data-stu-id="2fc13-162">A context handle description in the type format string will not have the offset<2> in the description.</span></span>

 

## <a name="the-new-oif-header"></a><span data-ttu-id="2fc13-163">Nuova intestazione – OIF</span><span class="sxs-lookup"><span data-stu-id="2fc13-163">The New –Oif Header</span></span>

<span data-ttu-id="2fc13-164">Come indicato in precedenza, l'intestazione [**-OIF**](/windows/desktop/Midl/-oi) si espande sull'intestazione **-OI** .</span><span class="sxs-lookup"><span data-stu-id="2fc13-164">As mentioned previously, the [**–Oif**](/windows/desktop/Midl/-oi) header expands on the **–Oi** header.</span></span> <span data-ttu-id="2fc13-165">Per praticità, vengono visualizzati tutti i campi:</span><span class="sxs-lookup"><span data-stu-id="2fc13-165">For convenience, all fields are shown here:</span></span>

<span data-ttu-id="2fc13-166">(Intestazione precedente)</span><span class="sxs-lookup"><span data-stu-id="2fc13-166">(The old header)</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="2fc13-167">(Estensioni [**-OIF**](/windows/desktop/Midl/-oi) )</span><span class="sxs-lookup"><span data-stu-id="2fc13-167">(The [**–Oif**](/windows/desktop/Midl/-oi) extensions)</span></span>

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

<span data-ttu-id="2fc13-168">La costante \_ \_ \_ dimensione del buffer client<2> fornisce le dimensioni del buffer di marshalling che potrebbero essere state pre-calcolate dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="2fc13-168">The constant\_client\_buffer\_size<2> provides the size of the marshaling buffer that could have been pre-computed by the compiler.</span></span> <span data-ttu-id="2fc13-169">Può trattarsi solo di una dimensione parziale, perché il flag ClientMustSize attiva il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="2fc13-169">This may be only a partial size, as the ClientMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="2fc13-170">La \_ dimensione del buffer del server costante \_ \_<2> fornisce le dimensioni del buffer di marshalling come pre-calcolato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="2fc13-170">The constant\_server\_buffer\_size<2> provides the size of the marshaling buffer as precomputed by the compiler.</span></span> <span data-ttu-id="2fc13-171">Può trattarsi solo di una dimensione parziale, perché il flag ServerMustSize attiva il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="2fc13-171">This may be only a partial size, as the ServerMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="2fc13-172">I \_ flag di consenso esplicito dell'interprete \_ sono definiti in Ndrtypes. h:</span><span class="sxs-lookup"><span data-stu-id="2fc13-172">The INTERPRETER\_OPT\_FLAGS are defined in Ndrtypes.h:</span></span>

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   <span data-ttu-id="2fc13-173">Il bit ServerMustSize viene impostato se il server deve eseguire un passaggio di ridimensionamento del buffer.</span><span class="sxs-lookup"><span data-stu-id="2fc13-173">The ServerMustSize bit is set if the server needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="2fc13-174">Il bit ClientMustSize viene impostato se il client deve eseguire un passaggio di ridimensionamento del buffer.</span><span class="sxs-lookup"><span data-stu-id="2fc13-174">The ClientMustSize bit is set if the client needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="2fc13-175">Il bit HasReturn viene impostato se la routine ha un valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2fc13-175">The HasReturn bit is set if the procedure has a return value.</span></span>
-   <span data-ttu-id="2fc13-176">Il bit HasPipes viene impostato se il pacchetto pipe deve essere utilizzato per supportare un argomento pipe.</span><span class="sxs-lookup"><span data-stu-id="2fc13-176">The HasPipes bit is set if the pipe package needs to be used to support a pipe argument.</span></span>
-   <span data-ttu-id="2fc13-177">Il bit HasAsyncUuid viene impostato se la procedura è una procedura DCOM asincrona.</span><span class="sxs-lookup"><span data-stu-id="2fc13-177">The HasAsyncUuid bit is set if the procedure is an asynchronous DCOM procedure.</span></span>
-   <span data-ttu-id="2fc13-178">Il bit HasExtensions indica che vengono utilizzate le estensioni Windows 2000 e successive.</span><span class="sxs-lookup"><span data-stu-id="2fc13-178">The HasExtensions bit indicates that Windows 2000 and later extensions are used.</span></span>
-   <span data-ttu-id="2fc13-179">Il bit HasAsyncHandle indica una procedura RPC asincrona.</span><span class="sxs-lookup"><span data-stu-id="2fc13-179">The HasAsyncHandle bit indicates an asynchronous RPC procedure.</span></span>

<span data-ttu-id="2fc13-180">Il bit HasAsyncHandle è stato inizialmente usato per un'implementazione DCOM diversa del supporto asincrono e pertanto non può essere usato per il supporto asincrono dello stile corrente in DCOM.</span><span class="sxs-lookup"><span data-stu-id="2fc13-180">The HasAsyncHandle bit has been initially used for a different DCOM implementation of async support, and hence could not be used for the current style async support in DCOM.</span></span> <span data-ttu-id="2fc13-181">Il bit HasAsyncUuid attualmente indica questo.</span><span class="sxs-lookup"><span data-stu-id="2fc13-181">The HasAsyncUuid bit currently indicates this.</span></span>

 

 