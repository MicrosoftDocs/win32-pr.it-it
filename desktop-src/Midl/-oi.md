---
title: Opzione/Oi
description: Le opzioni/OI e/OIC indirizzano il compilatore MIDL per l'uso di un metodo di marshalling completamente interpretato. L'opzione/Oicf fornisce ulteriori miglioramenti delle prestazioni.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /OI switch MIDL
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223539"
---
# <a name="oi-switch"></a><span data-ttu-id="99939-105">Opzione/Oi</span><span class="sxs-lookup"><span data-stu-id="99939-105">/Oi switch</span></span>

<span data-ttu-id="99939-106">Le opzioni **/OI** e **/OIC** indirizzano il compilatore MIDL per l'uso di un metodo di marshalling completamente interpretato.</span><span class="sxs-lookup"><span data-stu-id="99939-106">The **/Oi** and **/Oic** switches direct the MIDL compiler to use a fully-interpreted marshaling method.</span></span> <span data-ttu-id="99939-107">L'opzione **/Oicf** fornisce ulteriori miglioramenti delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="99939-107">The **/Oicf** switch provides additional performance enhancements.</span></span>

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a><span data-ttu-id="99939-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="99939-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="99939-109">*OI*</span><span class="sxs-lookup"><span data-stu-id="99939-109">*Oi*</span></span> 
</dt> <dd>

<span data-ttu-id="99939-110">Specifica il metodo completamente interpretato per il marshalling del codice stub passato tra client e server.</span><span class="sxs-lookup"><span data-stu-id="99939-110">Specifies the fully-interpreted method for marshaling stub code passed between client and server.</span></span>

> [!Note]  
> <span data-ttu-id="99939-111">Questa opzione è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="99939-111">This switch is obsolete.</span></span> <span data-ttu-id="99939-112">Si consiglia di usare l'opzione **/Oicf** al suo posto.</span><span class="sxs-lookup"><span data-stu-id="99939-112">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="99939-113">*OIC*</span><span class="sxs-lookup"><span data-stu-id="99939-113">*Oic*</span></span> 
</dt> <dd>

<span data-ttu-id="99939-114">Specifica il metodo proxy senza codice per il marshalling che fornisce tutte le funzionalità di **/OI** e riduce ulteriormente le dimensioni del codice stub client per le interfacce oggetto.</span><span class="sxs-lookup"><span data-stu-id="99939-114">Specifies the codeless proxy method of marshaling that provides all the features of **/Oi** and also further reduces the size of the client stub code for object interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="99939-115">Questa opzione è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="99939-115">This switch is obsolete.</span></span> <span data-ttu-id="99939-116">Si consiglia di usare l'opzione **/Oicf** al suo posto.</span><span class="sxs-lookup"><span data-stu-id="99939-116">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="99939-117">*OIF o Oicf*</span><span class="sxs-lookup"><span data-stu-id="99939-117">*Oif or Oicf*</span></span> 
</dt> <dd>

<span data-ttu-id="99939-118">Specifica il metodo proxy senza codice del marshalling che include tutte le funzionalità fornite da **/OI** e **/OIC** , ma usa un nuovo interprete (stringhe di formato rapido) che offre prestazioni migliori rispetto a **/OI** o **/OIC**.</span><span class="sxs-lookup"><span data-stu-id="99939-118">Specifies the codeless proxy method of marshaling that includes all the features provided by **/Oi** and **/Oic** but uses a new interpreter (fast format strings) that provides better performance than **/Oi** or **/Oic**.</span></span> <span data-ttu-id="99939-119">Questa opzione include miglioramenti recenti di RPC ed è consigliata per gli scenari RPC moderni.</span><span class="sxs-lookup"><span data-stu-id="99939-119">This switch includes recent RPC enhancements and is recommended for modern RPC scenarios.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99939-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="99939-120">Remarks</span></span>

<span data-ttu-id="99939-121">Si notino le restrizioni relative alle piattaforme di supporto.</span><span class="sxs-lookup"><span data-stu-id="99939-121">Please note the restrictions related to supporting platforms.</span></span>

<span data-ttu-id="99939-122">Il compilatore MIDL 3,0 fornisce due metodi per il marshalling del codice: completamente interpretato ( **/OI**, **/OIC** e **/Oicf**) e in modalità mista ( [**/OS**](-os.md)).</span><span class="sxs-lookup"><span data-stu-id="99939-122">The MIDL 3.0 compiler provides two methods for marshaling code: fully-interpreted ( **/Oi**, **/Oic** and **/Oicf**) and mixed-mode ( [**/Os**](-os.md)).</span></span> <span data-ttu-id="99939-123">A partire dalla versione MIDL 6.0.359, il compilatore MIDL genera gli stub **/Oicf** Â  [**/robust**](-robust.md) per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="99939-123">Starting with MIDL version 6.0.359, the MIDL compiler generates **/Oicf** Â  [**/robust**](-robust.md) stubs by default.</span></span> <span data-ttu-id="99939-124">Alcune funzionalità del linguaggio non sono supportate in alcune modalità.</span><span class="sxs-lookup"><span data-stu-id="99939-124">Some language features are not supported in some modes.</span></span> <span data-ttu-id="99939-125">In questo caso, il compilatore passa automaticamente alla modalità appropriata e genera un avviso.</span><span class="sxs-lookup"><span data-stu-id="99939-125">In this case, the compiler automatically switches to the appropriate mode and issues a warning.</span></span>

<span data-ttu-id="99939-126">Se le prestazioni sono un problema, il metodo in modalità mista ( [**/OS**](-os.md)) può essere l'approccio migliore.</span><span class="sxs-lookup"><span data-stu-id="99939-126">If performance is a concern, the mixed-mode ( [**/Os**](-os.md)) method can be the best approach.</span></span> <span data-ttu-id="99939-127">In questa modalità, il compilatore sceglie di effettuare il marshalling di alcuni parametri inline negli stub generati.</span><span class="sxs-lookup"><span data-stu-id="99939-127">In this mode, the compiler chooses to marshal some parameters inline in the generated stubs.</span></span> <span data-ttu-id="99939-128">Sebbene il risultato sia una dimensione dello stub più grande, offre prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="99939-128">While this results in larger stub size, it offers increased performance.</span></span>

<span data-ttu-id="99939-129">Il metodo completamente interpretato esegue il marshalling dei dati completamente offline.</span><span class="sxs-lookup"><span data-stu-id="99939-129">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="99939-130">Questo consente di ridurre notevolmente le dimensioni del codice stub, ma comporta una riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="99939-130">This considerably reduces the size of the stub code, but results in decreased performance.</span></span> <span data-ttu-id="99939-131">Inoltre, con il metodo completamente interpretato, è previsto un limite di 16 parametri per ogni procedura.</span><span class="sxs-lookup"><span data-stu-id="99939-131">Also, with the fully-interpreted method, there is a limit of 16 parameters for each procedure.</span></span> <span data-ttu-id="99939-132">Qualsiasi routine contenente più di 16 parametri verrà automaticamente elaborata in modalità [**/OS**](-os.md) .</span><span class="sxs-lookup"><span data-stu-id="99939-132">Any procedure containing more than 16 parameters will automatically be processed in [**/Os**](-os.md) mode.</span></span> <span data-ttu-id="99939-133">Tra le modalità interpretate, **/Oicf** offre le migliori prestazioni e **/OI** offre la migliore compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="99939-133">Among the interpreted modes, **/Oicf** offers the best performance and **/Oi** offers the best backward compatibility.</span></span>

<span data-ttu-id="99939-134">È possibile usare l'opzione **/OIF** se l'applicazione usa le funzionalità MIDL introdotte con MIDL 3,0, ad esempio il \[ [**\_ marshalling di rete**](wire-marshal.md) \] e \[ gli attributi di [**\_ marshalling degli utenti**](user-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="99939-134">You may want to use the **/Oif** option if your application uses MIDL features that were introduced with MIDL 3.0, such as the \[[**wire\_marshal**](wire-marshal.md)\] and \[[**user\_marshal**](user-marshal.md)\] attributes.</span></span> <span data-ttu-id="99939-135">Se l'applicazione usa le [pipe](/windows/desktop/Rpc/pipes) , è necessario usare l'opzione **/OIF** . Se si specifica un'altra modalità, il compilatore MIDL passerà a **/OIF**.</span><span class="sxs-lookup"><span data-stu-id="99939-135">If your application uses [pipes](/windows/desktop/Rpc/pipes) you must use the **/Oif** option; if you specify another mode, the MIDL compiler will switch to **/Oif**.</span></span>

<span data-ttu-id="99939-136">Per ottimizzare la modalità di marshalling del codice stub, Microsoft RPC fornisce un attributo di \[ [**ottimizzazione**](optimize.md) ACF \] .</span><span class="sxs-lookup"><span data-stu-id="99939-136">To fine-tune the way your stub code is marshaled, Microsoft RPC provides an ACF \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="99939-137">Questo attributo viene utilizzato come attributo di interfaccia o attributo di operazione per selezionare la modalità di marshalling per le singole interfacce o per singole operazioni.</span><span class="sxs-lookup"><span data-stu-id="99939-137">This attribute is used as an interface attribute or operation attribute to select the marshaling mode for individual interfaces or for individual operations.</span></span>

### <a name="calling-conventions"></a><span data-ttu-id="99939-138">Convenzioni di chiamata</span><span class="sxs-lookup"><span data-stu-id="99939-138">Calling Conventions</span></span>

<span data-ttu-id="99939-139">Gli stub generati dal compilatore MIDL nel metodo interpretato mediante le opzioni **/OI**, **/OIC** o **/OIF** devono essere compilati come una routine stdcall o cdecl durante la compilazione C.</span><span class="sxs-lookup"><span data-stu-id="99939-139">Stubs generated by the MIDL compiler in the interpreted method using the **/Oi**, **/Oic**, or **/Oif** switches must be compiled as either a stdcall or a cdecl procedure during the C compilation.</span></span> <span data-ttu-id="99939-140">Una convenzione di chiamata PASCAL o fastcall non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="99939-140">A PASCAL or Fastcall calling convention will not work.</span></span> <span data-ttu-id="99939-141">Inoltre, lo stub del server deve essere compilato come stdcall.</span><span class="sxs-lookup"><span data-stu-id="99939-141">Additionally, the server stub must be compiled as stdcall.</span></span>

## <a name="examples"></a><span data-ttu-id="99939-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="99939-142">Examples</span></span>

<span data-ttu-id="99939-143">**MIDL/OI nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="99939-143">**midl /Oi filename.idl**</span></span>

<span data-ttu-id="99939-144">**MIDL/OIC nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="99939-144">**midl /Oic filename.idl**</span></span>

<span data-ttu-id="99939-145">**MIDL/OIF nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="99939-145">**midl /Oif filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="99939-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99939-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99939-147">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="99939-147">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="99939-148">**/No \_ affidabile**</span><span class="sxs-lookup"><span data-stu-id="99939-148">**/no\_robust**</span></span>](-no-robust.md)
</dt> <dt>

[<span data-ttu-id="99939-149">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="99939-149">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="99939-150">**/OS**</span><span class="sxs-lookup"><span data-stu-id="99939-150">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="99939-151">**ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="99939-151">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="99939-152">**/No \_ Format \_ opz**</span><span class="sxs-lookup"><span data-stu-id="99939-152">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 