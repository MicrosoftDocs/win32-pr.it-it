---
description: ICE57 convalida che i singoli componenti non combinano i dati per computer e per utente. Questa azione personalizzata ICE controlla le voci del registro di sistema, i file, i percorsi delle chiavi di directory e i collegamenti non annunciati.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232855"
---
# <a name="ice57"></a><span data-ttu-id="3e436-104">ICE57</span><span class="sxs-lookup"><span data-stu-id="3e436-104">ICE57</span></span>

<span data-ttu-id="3e436-105">ICE57 convalida che i singoli componenti non combinano i dati per computer e per utente.</span><span class="sxs-lookup"><span data-stu-id="3e436-105">ICE57 validates that individual components do not mix per-machine and per-user data.</span></span> <span data-ttu-id="3e436-106">Questa azione personalizzata ICE controlla le voci del registro di sistema, i file, i percorsi delle chiavi di directory e i collegamenti non annunciati.</span><span class="sxs-lookup"><span data-stu-id="3e436-106">This ICE custom action checks registry entries, files, directory key paths, and non-advertised shortcuts.</span></span>

<span data-ttu-id="3e436-107">La combinazione di dati per singolo utente e computer nello stesso componente può comportare solo l'installazione parziale del componente per alcuni utenti in un ambiente multiutente.</span><span class="sxs-lookup"><span data-stu-id="3e436-107">Mixing per-user and per-machine data in the same component could result in only partial installation of the component for some users in a multi-user environment.</span></span>

<span data-ttu-id="3e436-108">Vedere la proprietà [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="3e436-108">See the [**ALLUSERS**](allusers.md) property.</span></span>

## <a name="result"></a><span data-ttu-id="3e436-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="3e436-109">Result</span></span>

<span data-ttu-id="3e436-110">ICE57 Invia un errore se trova un componente che contiene le voci del registro di sistema per computer e per utente, i file, i percorsi delle chiavi di directory o i collegamenti non annunciati.</span><span class="sxs-lookup"><span data-stu-id="3e436-110">ICE57 posts an error if it finds any component that contains both a per-machine and per-user registry entries, files, directory key paths, or non-advertised shortcuts.</span></span>

## <a name="example"></a><span data-ttu-id="3e436-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="3e436-111">Example</span></span>

<span data-ttu-id="3e436-112">ICE57reports gli errori seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="3e436-112">ICE57reports the following errors for the example shown.</span></span>

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

<span data-ttu-id="3e436-113">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="3e436-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="3e436-114">Componente</span><span class="sxs-lookup"><span data-stu-id="3e436-114">Component</span></span>  | <span data-ttu-id="3e436-115">Directory</span><span class="sxs-lookup"><span data-stu-id="3e436-115">Directory</span></span>  | <span data-ttu-id="3e436-116">Attributi</span><span class="sxs-lookup"><span data-stu-id="3e436-116">Attributes</span></span> | <span data-ttu-id="3e436-117">KeyPath</span><span class="sxs-lookup"><span data-stu-id="3e436-117">KeyPath</span></span> |
|------------|------------|------------|---------|
| <span data-ttu-id="3e436-118">Component1</span><span class="sxs-lookup"><span data-stu-id="3e436-118">Component1</span></span> | <span data-ttu-id="3e436-119">Directory</span><span class="sxs-lookup"><span data-stu-id="3e436-119">DirectoryA</span></span> | <span data-ttu-id="3e436-120">0</span><span class="sxs-lookup"><span data-stu-id="3e436-120">0</span></span>          | <span data-ttu-id="3e436-121">FileA</span><span class="sxs-lookup"><span data-stu-id="3e436-121">FileA</span></span>   |
| <span data-ttu-id="3e436-122">Component2</span><span class="sxs-lookup"><span data-stu-id="3e436-122">Component2</span></span> | <span data-ttu-id="3e436-123">Directory</span><span class="sxs-lookup"><span data-stu-id="3e436-123">DirectoryA</span></span> | <span data-ttu-id="3e436-124">4</span><span class="sxs-lookup"><span data-stu-id="3e436-124">4</span></span>          | <span data-ttu-id="3e436-125">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="3e436-125">RegKeyB</span></span> |
| <span data-ttu-id="3e436-126">Component3</span><span class="sxs-lookup"><span data-stu-id="3e436-126">Component3</span></span> | <span data-ttu-id="3e436-127">Directory</span><span class="sxs-lookup"><span data-stu-id="3e436-127">DirectoryA</span></span> | <span data-ttu-id="3e436-128">0</span><span class="sxs-lookup"><span data-stu-id="3e436-128">0</span></span>          | <span data-ttu-id="3e436-129">FileC</span><span class="sxs-lookup"><span data-stu-id="3e436-129">FileC</span></span>   |
| <span data-ttu-id="3e436-130">Component4</span><span class="sxs-lookup"><span data-stu-id="3e436-130">Component4</span></span> | <span data-ttu-id="3e436-131">Directory</span><span class="sxs-lookup"><span data-stu-id="3e436-131">DirectoryA</span></span> | <span data-ttu-id="3e436-132">4</span><span class="sxs-lookup"><span data-stu-id="3e436-132">4</span></span>          | <span data-ttu-id="3e436-133">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="3e436-133">RegKeyD</span></span> |



 

<span data-ttu-id="3e436-134">[Tabella del registro di sistema](registry-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="3e436-134">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="3e436-135">Registro</span><span class="sxs-lookup"><span data-stu-id="3e436-135">Registry</span></span> | <span data-ttu-id="3e436-136">Radice</span><span class="sxs-lookup"><span data-stu-id="3e436-136">Root</span></span> | <span data-ttu-id="3e436-137">Componente\_</span><span class="sxs-lookup"><span data-stu-id="3e436-137">Component\_</span></span> |
|----------|------|-------------|
| <span data-ttu-id="3e436-138">RegKeyA</span><span class="sxs-lookup"><span data-stu-id="3e436-138">RegKeyA</span></span>  | <span data-ttu-id="3e436-139">1</span><span class="sxs-lookup"><span data-stu-id="3e436-139">1</span></span>    | <span data-ttu-id="3e436-140">Component1</span><span class="sxs-lookup"><span data-stu-id="3e436-140">Component1</span></span>  |
| <span data-ttu-id="3e436-141">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="3e436-141">RegKeyB</span></span>  | <span data-ttu-id="3e436-142">1</span><span class="sxs-lookup"><span data-stu-id="3e436-142">1</span></span>    | <span data-ttu-id="3e436-143">Component2</span><span class="sxs-lookup"><span data-stu-id="3e436-143">Component2</span></span>  |
| <span data-ttu-id="3e436-144">RegKeyC</span><span class="sxs-lookup"><span data-stu-id="3e436-144">RegKeyC</span></span>  | <span data-ttu-id="3e436-145">-1</span><span class="sxs-lookup"><span data-stu-id="3e436-145">-1</span></span>   | <span data-ttu-id="3e436-146">Component3</span><span class="sxs-lookup"><span data-stu-id="3e436-146">Component3</span></span>  |
| <span data-ttu-id="3e436-147">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="3e436-147">RegKeyD</span></span>  | <span data-ttu-id="3e436-148">-1</span><span class="sxs-lookup"><span data-stu-id="3e436-148">-1</span></span>   | <span data-ttu-id="3e436-149">Component4</span><span class="sxs-lookup"><span data-stu-id="3e436-149">Component4</span></span>  |



 

<span data-ttu-id="3e436-150">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="3e436-150">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="3e436-151">File</span><span class="sxs-lookup"><span data-stu-id="3e436-151">File</span></span>  | <span data-ttu-id="3e436-152">Componente\_</span><span class="sxs-lookup"><span data-stu-id="3e436-152">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="3e436-153">FileA</span><span class="sxs-lookup"><span data-stu-id="3e436-153">FileA</span></span> | <span data-ttu-id="3e436-154">Component1</span><span class="sxs-lookup"><span data-stu-id="3e436-154">Component1</span></span>  |
| <span data-ttu-id="3e436-155">FileB</span><span class="sxs-lookup"><span data-stu-id="3e436-155">FileB</span></span> | <span data-ttu-id="3e436-156">Component2</span><span class="sxs-lookup"><span data-stu-id="3e436-156">Component2</span></span>  |
| <span data-ttu-id="3e436-157">FileC</span><span class="sxs-lookup"><span data-stu-id="3e436-157">FileC</span></span> | <span data-ttu-id="3e436-158">Component3</span><span class="sxs-lookup"><span data-stu-id="3e436-158">Component3</span></span>  |
| <span data-ttu-id="3e436-159">Campo</span><span class="sxs-lookup"><span data-stu-id="3e436-159">FileD</span></span> | <span data-ttu-id="3e436-160">Component4</span><span class="sxs-lookup"><span data-stu-id="3e436-160">Component4</span></span>  |



 

[<span data-ttu-id="3e436-161">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="3e436-161">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="3e436-162">Directory</span><span class="sxs-lookup"><span data-stu-id="3e436-162">Directory</span></span>  | <span data-ttu-id="3e436-163">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="3e436-163">Directory\_Parent</span></span> | <span data-ttu-id="3e436-164">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="3e436-164">DefaultDir</span></span> |
|------------|-------------------|------------|
| <span data-ttu-id="3e436-165">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="3e436-165">TARGETDIR</span></span>  |                   | <span data-ttu-id="3e436-166">SourceDir</span><span class="sxs-lookup"><span data-stu-id="3e436-166">SourceDir</span></span>  |
| <span data-ttu-id="3e436-167">Directory</span><span class="sxs-lookup"><span data-stu-id="3e436-167">DirectoryA</span></span> | <span data-ttu-id="3e436-168">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="3e436-168">TARGETDIR</span></span>         | <span data-ttu-id="3e436-169">Directory</span><span class="sxs-lookup"><span data-stu-id="3e436-169">DirectoryA</span></span> |



 

<span data-ttu-id="3e436-170">Per correggere gli errori, riorganizzare l'applicazione in modo che ogni componente contenga solo risorse per utente o per computer e non entrambi.</span><span class="sxs-lookup"><span data-stu-id="3e436-170">To fix the errors, reorganize the application such that each component contains only per-user or per-machine resources, and not both.</span></span>

<span data-ttu-id="3e436-171">Il primo messaggio di errore viene pubblicato perché Component1 contiene Filea (per computer) e la chiave del registro di sistema HKCU RegKeyA (per utente).</span><span class="sxs-lookup"><span data-stu-id="3e436-171">The first error message is posted because Component1 contains FileA (per-machine) and the HKCU registry key RegKeyA (per user).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e436-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3e436-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e436-173">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="3e436-173">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



