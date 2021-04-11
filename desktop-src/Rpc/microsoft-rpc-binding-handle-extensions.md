---
title: Microsoft RPC Binding-Handle Extensions
description: Le estensioni Microsoft per il linguaggio IDL supportano più parametri di handle che vengono visualizzati in posizioni diverse dal primo parametro, più a sinistra.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104047507"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a><span data-ttu-id="ef2ef-103">Microsoft RPC Binding-Handle Extensions</span><span class="sxs-lookup"><span data-stu-id="ef2ef-103">Microsoft RPC Binding-Handle Extensions</span></span>

<span data-ttu-id="ef2ef-104">Le estensioni Microsoft per il linguaggio IDL supportano più parametri di handle che vengono visualizzati in posizioni diverse dal primo parametro, più a sinistra.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-104">The Microsoft extensions to the IDL language support multiple handle parameters that appear in positions other than the first, leftmost, parameter.</span></span> <span data-ttu-id="ef2ef-105">I passaggi seguenti descrivono la sequenza che il compilatore MIDL passa per risolvere il parametro binding-handle in modalità di compatibilità DCE (/**OSF**) e in modalità predefinita (Microsoft-Extended).</span><span class="sxs-lookup"><span data-stu-id="ef2ef-105">The following steps describe the sequence that the MIDL compiler goes through to resolve the binding-handle parameter in DCE-compatibility mode (/**osf**), and in default (Microsoft-extended) mode.</span></span>

## <a name="dce-compatibility-mode"></a><span data-ttu-id="ef2ef-106">Modalità di compatibilità DCE</span><span class="sxs-lookup"><span data-stu-id="ef2ef-106">DCE-compatibility mode</span></span>

-   <span data-ttu-id="ef2ef-107">Handle di associazione visualizzato nella prima posizione.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-107">Binding handle that appears in first position.</span></span>
-   <span data-ttu-id="ef2ef-108">Più \[ [**a sinistra in**](/windows/desktop/Midl/in), parametro dell' [**\_ handle del contesto**](/windows/desktop/Midl/context-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="ef2ef-108">Leftmost \[[**in**](/windows/desktop/Midl/in), [**context\_handle**](/windows/desktop/Midl/context-handle)\] parameter.</span></span>
-   <span data-ttu-id="ef2ef-109">Handle di associazione implicito specificato dall' \[ [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) \] o dall' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="ef2ef-109">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="ef2ef-110">Se non è presente alcun ACF, per impostazione predefinita viene utilizzato l' \[ **\_ handle automatico** \] .</span><span class="sxs-lookup"><span data-stu-id="ef2ef-110">If no ACF present, default to use of \[**auto\_handle**\].</span></span>

## <a name="default-mode"></a><span data-ttu-id="ef2ef-111">Modalità predefinita</span><span class="sxs-lookup"><span data-stu-id="ef2ef-111">Default mode</span></span>

-   <span data-ttu-id="ef2ef-112">Handle di binding esplicito più a sinistra.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-112">Leftmost explicit binding handle.</span></span>
-   <span data-ttu-id="ef2ef-113">Handle di associazione implicito specificato dall' \[ [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) \] o dall' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="ef2ef-113">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="ef2ef-114">Se non è presente alcun ACF, per impostazione predefinita viene utilizzato l' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="ef2ef-114">If no ACF present, default to use of \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="ef2ef-115">I compilatori IDL DCE cercano un handle di binding esplicito come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-115">DCE IDL compilers look for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="ef2ef-116">Quando il primo parametro non è un handle di binding e vengono specificati uno o più handle di contesto, viene utilizzato l'handle del contesto più a sinistra come handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-116">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="ef2ef-117">Quando il primo parametro non è un handle e non sono presenti handle di contesto, la procedura usa l'associazione implicita usando l'handle \[ [**implicito \_**](/windows/desktop/Midl/implicit-handle) dell'attributo ACF \] o l' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="ef2ef-117">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="ef2ef-118">Le estensioni Microsoft per IDL consentono all'handle di associazione di trovarsi in una posizione diversa dal primo parametro.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-118">The Microsoft extensions to the IDL allow the binding handle to be in a position other than the first parameter.</span></span> <span data-ttu-id="ef2ef-119">Il punto di controllo più \[ [**a sinistra nel parametro di**](/windows/desktop/Midl/in) \] handle esplicito, che si tratti di un handle primitivo, definito dal programmatore o di contesto, è l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-119">The leftmost \[[**in**](/windows/desktop/Midl/in)\] explicit-handle parameter–whether it is a primitive, programmer-defined, or context handle–is the binding handle.</span></span> <span data-ttu-id="ef2ef-120">Quando non sono presenti parametri di handle, la procedura usa l'associazione implicita usando l'handle \[ [**implicito \_**](/windows/desktop/Midl/implicit-handle) dell'attributo ACF \] o l' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .</span><span class="sxs-lookup"><span data-stu-id="ef2ef-120">When there are no handle parameters, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="ef2ef-121">Le regole seguenti si applicano sia alla modalità di compatibilità DCE (/OSF) che alla modalità predefinita:</span><span class="sxs-lookup"><span data-stu-id="ef2ef-121">The following rules apply to both DCE-compatibility (/osf) mode and default mode:</span></span>

-   <span data-ttu-id="ef2ef-122">Quando non è presente alcun ACF, viene usata l'associazione di handle automatico.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-122">Auto-handle binding is used when no ACF is present.</span></span>
-   <span data-ttu-id="ef2ef-123">Esplicito \[ [**in**](/windows/desktop/Midl/in) \] o \[ **in**, gli handle [**out**](/windows/desktop/Midl/out-idl) \] per una singola funzione hanno la precedenza su qualsiasi associazione implicita specificata per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-123">Explicit \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, [**out**](/windows/desktop/Midl/out-idl)\] handles for an individual function preempt any implicit binding specified for the interface.</span></span>
-   <span data-ttu-id="ef2ef-124">Più \[ [**in**](/windows/desktop/Midl/in) \] o \[ **in**, gli \] handle primitivi non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-124">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] primitive handles are not supported.</span></span>
-   <span data-ttu-id="ef2ef-125">Più \[ [**in**](/windows/desktop/Midl/in) \] o \[ **in**, \] sono consentiti gli handle del contesto espliciti.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-125">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] explicit context handles are allowed.</span></span>
-   <span data-ttu-id="ef2ef-126">Tutti i parametri di handle definiti dal programmatore, ad eccezione del parametro binding-handle, vengono trattati come dati trasmissibili.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-126">All programmer-defined handle parameters except the binding-handle parameter are treated as transmissible data.</span></span>

<span data-ttu-id="ef2ef-127">La tabella seguente contiene esempi e descrive come vengono assegnati gli handle di associazione in ogni modalità del compilatore.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-127">The following table contains examples and describes how binding handles are assigned in each compiler mode.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef2ef-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="ef2ef-128">Example</span></span></th>
<th><span data-ttu-id="ef2ef-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef2ef-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td><span data-ttu-id="ef2ef-130">Nessun handle esplicito specificato.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-130">No explicit handle is specified.</span></span> <span data-ttu-id="ef2ef-131">Viene utilizzato l'handle di associazione implicito, specificato da [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] o [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>].</span><span class="sxs-lookup"><span data-stu-id="ef2ef-131">The implicit binding handle, specified by [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] or [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], is used.</span></span> <span data-ttu-id="ef2ef-132">Quando non è presente alcun ACF, viene usato un handle automatico.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-132">When no ACF is present, an auto handle is used.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td><span data-ttu-id="ef2ef-133">Viene specificato un handle esplicito di tipo handle_t.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-133">An explicit handle of type handle_t is specified.</span></span> <span data-ttu-id="ef2ef-134">Il parametro <em>H</em> è l'handle di associazione per la procedura.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-134">The parameter <em>H</em> is the binding handle for the procedure.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td><span data-ttu-id="ef2ef-135">Il primo parametro non è un handle.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-135">The first parameter is not a handle.</span></span> <span data-ttu-id="ef2ef-136">In modalità predefinita, il parametro dell'handle più a sinistra, <em>H</em>, è l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-136">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="ef2ef-137">In modalità/OSF viene utilizzata l'associazione implicita.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-137">In /osf mode, implicit binding is used.</span></span> <span data-ttu-id="ef2ef-138">Viene restituito un errore perché si prevede che il secondo parametro sia trasmissibile e non handle_t possibile trasmettere.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-138">An error is reported because the second parameter is expected to be transmissible, and handle_t cannot be transmitted.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td><span data-ttu-id="ef2ef-139">Il primo parametro non è un handle.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-139">The first parameter is not a handle.</span></span> <span data-ttu-id="ef2ef-140">In modalità predefinita, il parametro dell'handle più a sinistra, <em>H</em>, è l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-140">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="ef2ef-141">Gli stub chiamano le routine fornite dall'utente MY_HDL_bind e MY_HDL_unbind.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-141">The stubs call the user-supplied routines MY_HDL_bind and MY_HDL_unbind.</span></span> <span data-ttu-id="ef2ef-142">In modalità/OSF, viene utilizzata l'associazione implicita.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-142">In/osf mode, implicit binding is used.</span></span> <span data-ttu-id="ef2ef-143">Il parametro <em>H</em> dell'handle definito dal programmatore viene considerato come dati trasmissibili.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-143">The programmer-defined handle parameter <em>H</em> is treated as transmissible data.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td><span data-ttu-id="ef2ef-144">Il primo parametro è un handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-144">The first parameter is a binding handle.</span></span> <span data-ttu-id="ef2ef-145">Il parametro <em>H</em> è il parametro dell'handle di binding.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-145">The parameter <em>H</em> is the binding-handle parameter.</span></span> <span data-ttu-id="ef2ef-146">Il secondo parametro dell'handle definito dal programmatore viene considerato come dati trasmissibili.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-146">The second programmer-defined handle parameter is treated as transmissible data.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td><span data-ttu-id="ef2ef-147">L'handle di associazione è un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-147">The binding handle is a context handle.</span></span> <span data-ttu-id="ef2ef-148">Il parametro <em>H</em> è l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="ef2ef-148">The parameter <em>H</em> is the binding handle.</span></span></td>
</tr>
</tbody>
</table>



 

 

 