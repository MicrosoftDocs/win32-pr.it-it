---
title: opzione/target
description: L'opzione/target consente al compilatore MIDL di abilitare le ottimizzazioni disponibili solo nelle versioni recenti di Windows. Il commutatore/target attiva automaticamente opzioni aggiuntive.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- Switch/target MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104058404"
---
# <a name="target-switch"></a><span data-ttu-id="a0edb-105">opzione/target</span><span class="sxs-lookup"><span data-stu-id="a0edb-105">/target switch</span></span>

<span data-ttu-id="a0edb-106">L'opzione **/target** consente al compilatore MIDL di abilitare le ottimizzazioni disponibili solo nelle versioni recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="a0edb-106">The **/target** switch enables the MIDL compiler to enable optimizations available only on recent versions of Windows.</span></span> <span data-ttu-id="a0edb-107">Il commutatore **/target** attiva automaticamente opzioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="a0edb-107">The **/target** switch automatically activates additional switches.</span></span>

``` syntax
midl /target level
```

## <a name="switch-options"></a><span data-ttu-id="a0edb-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="a0edb-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="a0edb-109">*level*</span><span class="sxs-lookup"><span data-stu-id="a0edb-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="a0edb-110">Specifica il livello di destinazione, ad esempio NT50, NT51, NT60, NT61, NT62 o NT100.</span><span class="sxs-lookup"><span data-stu-id="a0edb-110">Specifies the target level, such as NT50, NT51, NT60, NT61, NT62, or NT100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0edb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0edb-111">Remarks</span></span>

<span data-ttu-id="a0edb-112">Il commutatore **/target** attiva automaticamente opzioni aggiuntive, in base al sistema operativo, come specificato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="a0edb-112">The **/target** switch automatically activates additional switches, based on the operating system, as specified in the following table:</span></span>



| <span data-ttu-id="a0edb-113">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a0edb-113">Operating system</span></span> | <span data-ttu-id="a0edb-114">livello/target</span><span class="sxs-lookup"><span data-stu-id="a0edb-114">/target level</span></span> | <span data-ttu-id="a0edb-115">Opzioni attivate</span><span class="sxs-lookup"><span data-stu-id="a0edb-115">Switches Activated</span></span>                     |
|------------------|---------------|----------------------------------------|
| <span data-ttu-id="a0edb-116">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a0edb-116">Windows 2000</span></span>     | <span data-ttu-id="a0edb-117">NT50</span><span class="sxs-lookup"><span data-stu-id="a0edb-117">NT50</span></span>          | <span data-ttu-id="a0edb-118">/Oicf/Error tutti/robust</span><span class="sxs-lookup"><span data-stu-id="a0edb-118">/Oicf /error all /robust</span></span>               |
| <span data-ttu-id="a0edb-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0edb-119">Windows XP</span></span>       | <span data-ttu-id="a0edb-120">NT51</span><span class="sxs-lookup"><span data-stu-id="a0edb-120">NT51</span></span>          | <span data-ttu-id="a0edb-121">/Oicf/error all/robust/Protocol all</span><span class="sxs-lookup"><span data-stu-id="a0edb-121">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="a0edb-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0edb-122">Windows Vista</span></span>    | <span data-ttu-id="a0edb-123">NT60</span><span class="sxs-lookup"><span data-stu-id="a0edb-123">NT60</span></span>          | <span data-ttu-id="a0edb-124">/Oicf/error all/robust/Protocol all</span><span class="sxs-lookup"><span data-stu-id="a0edb-124">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="a0edb-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0edb-125">Windows 7</span></span>        | <span data-ttu-id="a0edb-126">NT61</span><span class="sxs-lookup"><span data-stu-id="a0edb-126">NT61</span></span>          | <span data-ttu-id="a0edb-127">/Oicf/error all/robust/Protocol all</span><span class="sxs-lookup"><span data-stu-id="a0edb-127">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="a0edb-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0edb-128">Windows 8</span></span>        | <span data-ttu-id="a0edb-129">NT62</span><span class="sxs-lookup"><span data-stu-id="a0edb-129">NT62</span></span>          | <span data-ttu-id="a0edb-130">/Oicf/error all/robust/Protocol all</span><span class="sxs-lookup"><span data-stu-id="a0edb-130">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="a0edb-131">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a0edb-131">Windows 10</span></span>       | <span data-ttu-id="a0edb-132">NT100</span><span class="sxs-lookup"><span data-stu-id="a0edb-132">NT100</span></span>         | <span data-ttu-id="a0edb-133">/Oicf/error all/robust/Protocol all</span><span class="sxs-lookup"><span data-stu-id="a0edb-133">/Oicf /error all /robust /protocol all</span></span> |
 

<span data-ttu-id="a0edb-134">Per assicurarsi che uno stub venga eseguito nel sistema specificato dall'opzione **/target** , MIDL genera un errore quando è presente una funzionalità disponibile solo in una versione più recente di Windows.</span><span class="sxs-lookup"><span data-stu-id="a0edb-134">To ensure a stub runs on the system specified by the **/target** switch, MIDL issues an error when a feature available only on a more recent version of Windows is present.</span></span> <span data-ttu-id="a0edb-135">Nella tabella seguente viene specificato il livello **/target** minimo necessario per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a0edb-135">The following table specifies the minimum **/target** level required to enable the feature.</span></span> <span data-ttu-id="a0edb-136">I livelli di destinazione più elevati includono tutte le funzionalità dei livelli di destinazione inferiori.</span><span class="sxs-lookup"><span data-stu-id="a0edb-136">Higher target levels include all features from lower target levels.</span></span>



| <span data-ttu-id="a0edb-137">Livello/target minimo richiesto</span><span class="sxs-lookup"><span data-stu-id="a0edb-137">Minimum required /target level</span></span> | <span data-ttu-id="a0edb-138">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="a0edb-138">Features</span></span>                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0edb-139">NT50</span><span class="sxs-lookup"><span data-stu-id="a0edb-139">NT50</span></span>                           | <span data-ttu-id="a0edb-140">/Robust</span><span class="sxs-lookup"><span data-stu-id="a0edb-140">/robust</span></span><br/> <span data-ttu-id="a0edb-141">\[message\]</span><span class="sxs-lookup"><span data-stu-id="a0edb-141">\[message\]</span></span><br/> <span data-ttu-id="a0edb-142">\[async\]</span><span class="sxs-lookup"><span data-stu-id="a0edb-142">\[async\]</span></span><br/> <span data-ttu-id="a0edb-143">\[\_UUID asincrono\]</span><span class="sxs-lookup"><span data-stu-id="a0edb-143">\[async\_uuid\]</span></span><br/> <span data-ttu-id="a0edb-144">\[notifica \] in modalità/Oicf</span><span class="sxs-lookup"><span data-stu-id="a0edb-144">\[notify\] in /Oicf mode</span></span><br/> <span data-ttu-id="a0edb-145">\[codificare \] o \[ decodificare \] in modalità/Oicf</span><span class="sxs-lookup"><span data-stu-id="a0edb-145">\[encode\] or \[decode\] in /Oicf mode</span></span><br/>                   |
| <span data-ttu-id="a0edb-146">NT51</span><span class="sxs-lookup"><span data-stu-id="a0edb-146">NT51</span></span>                           | <span data-ttu-id="a0edb-147">supporto/Protocol a 64 bit</span><span class="sxs-lookup"><span data-stu-id="a0edb-147">/protocol 64-bit support</span></span><br/> <span data-ttu-id="a0edb-148">\[\_Ignora parziale\]</span><span class="sxs-lookup"><span data-stu-id="a0edb-148">\[partial\_ignore\]</span></span><br/> <span data-ttu-id="a0edb-149">\[forza \_ allocazione\]</span><span class="sxs-lookup"><span data-stu-id="a0edb-149">\[force\_allocate\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="a0edb-150">NT60</span><span class="sxs-lookup"><span data-stu-id="a0edb-150">NT60</span></span>                           | <span data-ttu-id="a0edb-151">Marshalling della struttura complessa forzata</span><span class="sxs-lookup"><span data-stu-id="a0edb-151">Forced complex structure marshalling</span></span><br/> <span data-ttu-id="a0edb-152">Handle di contesto in una matrice o una struttura</span><span class="sxs-lookup"><span data-stu-id="a0edb-152">Context handles in an array or structure</span></span><br/> <span data-ttu-id="a0edb-153">\[\]supporto dell'intervallo per le stringhe non dimensionate</span><span class="sxs-lookup"><span data-stu-id="a0edb-153">\[range\] support for unsized strings</span></span><br/> <span data-ttu-id="a0edb-154">\[tipo \_ strict \_ handle di contesto \_\]</span><span class="sxs-lookup"><span data-stu-id="a0edb-154">\[type\_strict\_context\_handle\]</span></span><br/> |
| <span data-ttu-id="a0edb-155">NT61</span><span class="sxs-lookup"><span data-stu-id="a0edb-155">NT61</span></span>                           | <span data-ttu-id="a0edb-156">Le chiamate dirette a Stub COM per le interfacce con metodi inferiori a 32 richiedono il collegamento di stub COM con **OLE32.DLL**.</span><span class="sxs-lookup"><span data-stu-id="a0edb-156">Direct COM stub calls for interfaces with less than 32 methods requires linking COM stubs with **OLE32.DLL**.</span></span><br/>                                                                          |
| <span data-ttu-id="a0edb-157">NT62</span><span class="sxs-lookup"><span data-stu-id="a0edb-157">NT62</span></span>                           | <span data-ttu-id="a0edb-158">Supporto ARM</span><span class="sxs-lookup"><span data-stu-id="a0edb-158">ARM support</span></span><br/> <span data-ttu-id="a0edb-159">Supporto di WinRT</span><span class="sxs-lookup"><span data-stu-id="a0edb-159">WinRT support</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="a0edb-160">NT100</span><span class="sxs-lookup"><span data-stu-id="a0edb-160">NT100</span></span>                          | <span data-ttu-id="a0edb-161">\[\]supporto system_handle</span><span class="sxs-lookup"><span data-stu-id="a0edb-161">\[system_handle\] support</span></span><br /> |


 

## <a name="examples"></a><span data-ttu-id="a0edb-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="a0edb-162">Examples</span></span>

<span data-ttu-id="a0edb-163">**NT50/target MIDL**</span><span class="sxs-lookup"><span data-stu-id="a0edb-163">**midl /target NT50**</span></span>

## <a name="see-also"></a><span data-ttu-id="a0edb-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0edb-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0edb-165">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="a0edb-165">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a0edb-166">**/osf**</span><span class="sxs-lookup"><span data-stu-id="a0edb-166">**/osf**</span></span>](-osf.md)
</dt> </dl>
