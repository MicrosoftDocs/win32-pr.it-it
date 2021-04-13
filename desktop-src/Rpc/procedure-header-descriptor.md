---
title: Descrittore di intestazioni di routine
description: L'intestazione è stata estesa più volte nel corso della durata del motore di rapporto di recapito. Il compilatore corrente genera comunque intestazioni diverse a seconda della modalità del compilatore. Tuttavia, le intestazioni più recenti sono un superset di quelle precedenti.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473902"
---
# <a name="procedure-header-descriptor"></a><span data-ttu-id="c7d57-105">Descrittore di intestazioni di routine</span><span class="sxs-lookup"><span data-stu-id="c7d57-105">Procedure Header Descriptor</span></span>

<span data-ttu-id="c7d57-106">L'intestazione è stata estesa più volte nel corso della durata del motore di rapporto di recapito.</span><span class="sxs-lookup"><span data-stu-id="c7d57-106">The header has been extended several times over the life of the NDR engine.</span></span> <span data-ttu-id="c7d57-107">Il compilatore corrente genera comunque intestazioni diverse a seconda della modalità del compilatore.</span><span class="sxs-lookup"><span data-stu-id="c7d57-107">The current compiler still generates different headers depending on the mode of the compiler.</span></span> <span data-ttu-id="c7d57-108">Tuttavia, le intestazioni più recenti sono un superset di quelle precedenti.</span><span class="sxs-lookup"><span data-stu-id="c7d57-108">However, more recent headers are a superset of the older ones.</span></span>

## <a name="the-old-oi-header"></a><span data-ttu-id="c7d57-109">Intestazione-OI precedente</span><span class="sxs-lookup"><span data-stu-id="c7d57-109">The Old –Oi Header</span></span>

<span data-ttu-id="c7d57-110">Il formato dell'intestazione è il seguente:</span><span class="sxs-lookup"><span data-stu-id="c7d57-110">The header has the following format:</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="c7d57-111">Dove \_ il tipo di handle<1> può essere uno dei valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c7d57-111">Where handle\_type<1> can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="c7d57-112">Hex</span><span class="sxs-lookup"><span data-stu-id="c7d57-112">Hex</span></span> | <span data-ttu-id="c7d57-113">Handle</span><span class="sxs-lookup"><span data-stu-id="c7d57-113">Handle</span></span>               |
|-----|----------------------|
| <span data-ttu-id="c7d57-114">31</span><span class="sxs-lookup"><span data-stu-id="c7d57-114">31</span></span>  | <span data-ttu-id="c7d57-115">\_associazione FC \_ generica</span><span class="sxs-lookup"><span data-stu-id="c7d57-115">FC\_BIND\_GENERIC</span></span>    |
| <span data-ttu-id="c7d57-116">32</span><span class="sxs-lookup"><span data-stu-id="c7d57-116">32</span></span>  | <span data-ttu-id="c7d57-117">\_ \_ primitiva bind FC</span><span class="sxs-lookup"><span data-stu-id="c7d57-117">FC\_BIND\_PRIMITIVE</span></span>  |
| <span data-ttu-id="c7d57-118">33</span><span class="sxs-lookup"><span data-stu-id="c7d57-118">33</span></span>  | <span data-ttu-id="c7d57-119">\_handle automatico \_ FC</span><span class="sxs-lookup"><span data-stu-id="c7d57-119">FC\_AUTO\_HANDLE</span></span>     |
| <span data-ttu-id="c7d57-120">34</span><span class="sxs-lookup"><span data-stu-id="c7d57-120">34</span></span>  | <span data-ttu-id="c7d57-121">\_handle di callback FC \_</span><span class="sxs-lookup"><span data-stu-id="c7d57-121">FC\_CALLBACK\_HANDLE</span></span> |
| <span data-ttu-id="c7d57-122">0</span><span class="sxs-lookup"><span data-stu-id="c7d57-122">0</span></span>   | <span data-ttu-id="c7d57-123">(handle esplicito)</span><span class="sxs-lookup"><span data-stu-id="c7d57-123">(explicit handle)</span></span>    |



 

<span data-ttu-id="c7d57-124">Se il tipo di handle \_<1> campo è diverso da zero, la stored procedure utilizza un handle implicito del tipo indicato.</span><span class="sxs-lookup"><span data-stu-id="c7d57-124">If the handle\_type<1> field is nonzero, then the procedure uses an implicit handle of the indicated kind.</span></span> <span data-ttu-id="c7d57-125">Per ulteriori informazioni, vedere l'argomento [Handles](handles.md) .</span><span class="sxs-lookup"><span data-stu-id="c7d57-125">See the [Handles](handles.md) topic for a more information.</span></span> <span data-ttu-id="c7d57-126">Se il \_ tipo di handle<1> campo è zero, l'handle utilizzato per l'associazione è uno dei parametri della procedura.</span><span class="sxs-lookup"><span data-stu-id="c7d57-126">If the handle\_type<1> field is zero, the handle used for binding is one of the procedure's parameters.</span></span>

<span data-ttu-id="c7d57-127">Gli handle espliciti possono essere primitivi, generici e di contesto; l'ultimo token FC è il seguente.</span><span class="sxs-lookup"><span data-stu-id="c7d57-127">Explicit handles can be primitive, generic, and context; the last one has the following FC token.</span></span>



| <span data-ttu-id="c7d57-128">Hex</span><span class="sxs-lookup"><span data-stu-id="c7d57-128">Hex</span></span> | <span data-ttu-id="c7d57-129">Handle</span><span class="sxs-lookup"><span data-stu-id="c7d57-129">Handle</span></span>            |
|-----|-------------------|
| <span data-ttu-id="c7d57-130">30</span><span class="sxs-lookup"><span data-stu-id="c7d57-130">30</span></span>  | <span data-ttu-id="c7d57-131">\_contesto di associazione FC \_</span><span class="sxs-lookup"><span data-stu-id="c7d57-131">FC\_BIND\_CONTEXT</span></span> |



 

<span data-ttu-id="c7d57-132">Per convenzione, il tipo di handle per le interfacce DCOM è la \_ gestione automatica FC \_ .</span><span class="sxs-lookup"><span data-stu-id="c7d57-132">By convention, the handle type for DCOM interfaces is FC\_AUTO\_HANDLE.</span></span>

<span data-ttu-id="c7d57-133">Il \_ campo OI flags<1> è una maschera a 8 bit dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="c7d57-133">The Oi\_flags<1> field is an 8-bit mask of the following flags.</span></span>



| <span data-ttu-id="c7d57-134">Hex</span><span class="sxs-lookup"><span data-stu-id="c7d57-134">Hex</span></span> | <span data-ttu-id="c7d57-135">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="c7d57-135">Flag</span></span>                         | <span data-ttu-id="c7d57-136">Significato</span><span class="sxs-lookup"><span data-stu-id="c7d57-136">Meaning</span></span>                                  |
|-----|------------------------------|------------------------------------------|
| <span data-ttu-id="c7d57-137">01</span><span class="sxs-lookup"><span data-stu-id="c7d57-137">01</span></span>  | <span data-ttu-id="c7d57-138">\_Ptr completo \_ OI \_ usato</span><span class="sxs-lookup"><span data-stu-id="c7d57-138">Oi\_FULL\_PTR\_USED</span></span>          | <span data-ttu-id="c7d57-139">Usa il pacchetto completo del puntatore.</span><span class="sxs-lookup"><span data-stu-id="c7d57-139">Uses the full pointer package.</span></span>           |
| <span data-ttu-id="c7d57-140">02</span><span class="sxs-lookup"><span data-stu-id="c7d57-140">02</span></span>  | <span data-ttu-id="c7d57-141">\_Alloc RPCSS di OI \_ \_ usato</span><span class="sxs-lookup"><span data-stu-id="c7d57-141">Oi\_RPCSS\_ALLOC\_USED</span></span>       | <span data-ttu-id="c7d57-142">Usa il pacchetto di memoria RpcSs.</span><span class="sxs-lookup"><span data-stu-id="c7d57-142">Uses the RpcSs memory package.</span></span>           |
| <span data-ttu-id="c7d57-143">04</span><span class="sxs-lookup"><span data-stu-id="c7d57-143">04</span></span>  | <span data-ttu-id="c7d57-144">Procedura dell' \_ oggetto OI \_</span><span class="sxs-lookup"><span data-stu-id="c7d57-144">Oi\_OBJECT\_PROC</span></span>             | <span data-ttu-id="c7d57-145">Procedura in un'interfaccia dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c7d57-145">A procedure in an object interface.</span></span>      |
| <span data-ttu-id="c7d57-146">08</span><span class="sxs-lookup"><span data-stu-id="c7d57-146">08</span></span>  | <span data-ttu-id="c7d57-147">OI \_ ha \_ RPCFLAGS</span><span class="sxs-lookup"><span data-stu-id="c7d57-147">Oi\_HAS\_RPCFLAGS</span></span>            | <span data-ttu-id="c7d57-148">La stored procedure contiene flag RPC diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="c7d57-148">The procedure has nonzero Rpc flags.</span></span>     |
| <span data-ttu-id="c7d57-149">10</span><span class="sxs-lookup"><span data-stu-id="c7d57-149">10</span></span>  | <span data-ttu-id="c7d57-150">OI\_\*</span><span class="sxs-lookup"><span data-stu-id="c7d57-150">Oi\_\*</span></span>                       | <span data-ttu-id="c7d57-151">Di overload.</span><span class="sxs-lookup"><span data-stu-id="c7d57-151">Overloaded.</span></span>                              |
| <span data-ttu-id="c7d57-152">20</span><span class="sxs-lookup"><span data-stu-id="c7d57-152">20</span></span>  | <span data-ttu-id="c7d57-153">OI\_\*</span><span class="sxs-lookup"><span data-stu-id="c7d57-153">Oi\_\*</span></span>                       | <span data-ttu-id="c7d57-154">Di overload.</span><span class="sxs-lookup"><span data-stu-id="c7d57-154">Overloaded.</span></span>                              |
| <span data-ttu-id="c7d57-155">40</span><span class="sxs-lookup"><span data-stu-id="c7d57-155">40</span></span>  | <span data-ttu-id="c7d57-156">OI \_ Usa \_ le \_ nuove \_ routine init</span><span class="sxs-lookup"><span data-stu-id="c7d57-156">Oi\_USE\_NEW\_INIT\_ROUTINES</span></span> | <span data-ttu-id="c7d57-157">Usa le routine di Windows NT 3.5 beta2 + init.</span><span class="sxs-lookup"><span data-stu-id="c7d57-157">Uses Windows NT3.5 Beta2+ init routines.</span></span> |
| <span data-ttu-id="c7d57-158">80</span><span class="sxs-lookup"><span data-stu-id="c7d57-158">80</span></span>  |                              | <span data-ttu-id="c7d57-159">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c7d57-159">Unused.</span></span>                                  |



 

<span data-ttu-id="c7d57-160">I flag seguenti sono in overload.</span><span class="sxs-lookup"><span data-stu-id="c7d57-160">The following flags are overloaded.</span></span>



| <span data-ttu-id="c7d57-161">Hex</span><span class="sxs-lookup"><span data-stu-id="c7d57-161">Hex</span></span> | <span data-ttu-id="c7d57-162">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="c7d57-162">Flag</span></span>                                    | <span data-ttu-id="c7d57-163">Significato</span><span class="sxs-lookup"><span data-stu-id="c7d57-163">Meaning</span></span>                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c7d57-164">10</span><span class="sxs-lookup"><span data-stu-id="c7d57-164">10</span></span>  | <span data-ttu-id="c7d57-165">\_viene \_ usato Encode</span><span class="sxs-lookup"><span data-stu-id="c7d57-165">ENCODE\_IS\_USED</span></span>                        | <span data-ttu-id="c7d57-166">Usato solo nella selezione.</span><span class="sxs-lookup"><span data-stu-id="c7d57-166">Used only in pickling.</span></span>                              |
| <span data-ttu-id="c7d57-167">20</span><span class="sxs-lookup"><span data-stu-id="c7d57-167">20</span></span>  | <span data-ttu-id="c7d57-168">\_viene usato Decode \_</span><span class="sxs-lookup"><span data-stu-id="c7d57-168">DECODE\_IS\_USED</span></span>                        | <span data-ttu-id="c7d57-169">Usato solo nella selezione.</span><span class="sxs-lookup"><span data-stu-id="c7d57-169">Used only in pickling.</span></span>                              |
| <span data-ttu-id="c7d57-170">10</span><span class="sxs-lookup"><span data-stu-id="c7d57-170">10</span></span>  | <span data-ttu-id="c7d57-171">OI \_ ignorare \_ la \_ \_ gestione delle eccezioni degli oggetti</span><span class="sxs-lookup"><span data-stu-id="c7d57-171">Oi\_IGNORE\_OBJECT\_EXCEPTION\_HANDLING</span></span> | <span data-ttu-id="c7d57-172">Non più usato (OLE precedente).</span><span class="sxs-lookup"><span data-stu-id="c7d57-172">Not used anymore (old OLE).</span></span>                         |
| <span data-ttu-id="c7d57-173">20</span><span class="sxs-lookup"><span data-stu-id="c7d57-173">20</span></span>  | <span data-ttu-id="c7d57-174">OI \_ ha un \_ comma \_ o un \_ errore</span><span class="sxs-lookup"><span data-stu-id="c7d57-174">Oi\_HAS\_COMM\_OR\_FAULT</span></span>                | <span data-ttu-id="c7d57-175">Solo in RPC non elaborata, \[ comunicazione \_ , stato di errore \_ \] .</span><span class="sxs-lookup"><span data-stu-id="c7d57-175">In raw RPC only, \[comm \_, fault\_status\].</span></span>        |
| <span data-ttu-id="c7d57-176">20</span><span class="sxs-lookup"><span data-stu-id="c7d57-176">20</span></span>  | <span data-ttu-id="c7d57-177">L' \_ \_ interprete OI obj USA \_ v2 \_</span><span class="sxs-lookup"><span data-stu-id="c7d57-177">Oi\_OBJ\_USE\_V2\_INTERPRETER</span></span>           | <span data-ttu-id="c7d57-178">Solo in DCOM usare l'interprete [**– OIF**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="c7d57-178">In DCOM only, use [**–Oif**](/windows/desktop/Midl/-oi) interpreter.</span></span> |



 

<span data-ttu-id="c7d57-179">Il \_ campo dei flag rpc<4> descrive come impostare il campo **RpcFlags** della struttura [**del \_ messaggio RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) .</span><span class="sxs-lookup"><span data-stu-id="c7d57-179">The rpc\_flags<4> field describes how to set the **RpcFlags** field of the [**RPC\_MESSAGE**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) structure.</span></span> <span data-ttu-id="c7d57-180">Questo campo è presente solo se i \_ flag oi<1> campo ha \_ \_ RPCFLAGS impostato OI.</span><span class="sxs-lookup"><span data-stu-id="c7d57-180">This field is only present if the Oi\_flags<1> field has Oi\_HAD\_RPCFLAGS set.</span></span> <span data-ttu-id="c7d57-181">Se questo campo non è presente, i flag RPC per la procedura remota sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="c7d57-181">If this field is not present, then the RPC flags for the remote procedure are zero.</span></span>

> [!Note]  
> <span data-ttu-id="c7d57-182">Per ottenere prestazioni, gli interpreti asincroni hanno sempre i \_ flag rpc<4> campo.</span><span class="sxs-lookup"><span data-stu-id="c7d57-182">For performance, the async interpreters always have the rpc\_flags<4> field present.</span></span>

 

<span data-ttu-id="c7d57-183">Il \_ campo proc num<2> fornisce il numero di procedura della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="c7d57-183">The proc\_num<2> field provides the procedure's procedure number.</span></span>

<span data-ttu-id="c7d57-184">La dimensione dello stack \_<2> fornisce la dimensione totale di tutti i parametri nello stack, inclusi tutti i valori di puntatore e/o valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c7d57-184">The stack\_size<2> provides the total size of all parameters on the stack, including any this pointer and/or return value.</span></span>

<span data-ttu-id="c7d57-185">La descrizione dell'handle esplicito \_ \_<> campo è descritta più avanti in questo documento.</span><span class="sxs-lookup"><span data-stu-id="c7d57-185">The explicit\_handle\_description<> field is described later in this document.</span></span> <span data-ttu-id="c7d57-186">Questo campo non è presente se la stored procedure utilizza un handle implicito.</span><span class="sxs-lookup"><span data-stu-id="c7d57-186">This field is not present if the procedure uses an implicit handle.</span></span>

 

 