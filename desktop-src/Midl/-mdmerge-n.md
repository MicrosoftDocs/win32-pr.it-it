---
title: /n (opzione)
description: L'opzione/n specifica la profondità della composizione per la composizione dei file di metadati.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n switch MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331934"
---
# <a name="n-switch"></a><span data-ttu-id="983b1-104">/n (opzione)</span><span class="sxs-lookup"><span data-stu-id="983b1-104">/n switch</span></span>

<span data-ttu-id="983b1-105">L'opzione **/n** specifica la profondità della composizione per la composizione dei file di metadati.</span><span class="sxs-lookup"><span data-stu-id="983b1-105">The **/n** switch specifies the composition depth for composing metadata files.</span></span>

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a><span data-ttu-id="983b1-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="983b1-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="983b1-107">*profondità dello spazio dei nomi \_*</span><span class="sxs-lookup"><span data-stu-id="983b1-107">*namespace\_depth*</span></span> 
</dt> <dd>

<span data-ttu-id="983b1-108">Specifica la profondità dello spazio dei nomi da comporre in un unico file di metadati.</span><span class="sxs-lookup"><span data-stu-id="983b1-108">Specifies the namespace depth to compose into a single metadata file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="983b1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="983b1-109">Remarks</span></span>

<span data-ttu-id="983b1-110">Di seguito sono riportati i possibili formati di valore che è possibile specificare con l'opzione **/n** .</span><span class="sxs-lookup"><span data-stu-id="983b1-110">Here are the possible value formats that you can specify with the **/n** switch.</span></span>



| <span data-ttu-id="983b1-111">Formato del valore</span><span class="sxs-lookup"><span data-stu-id="983b1-111">Value format</span></span>                   | <span data-ttu-id="983b1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="983b1-112">Description</span></span>                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="983b1-113">Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="983b1-113">Int32 > 0</span></span>                   | <span data-ttu-id="983b1-114">Comporre tutti i tipi in corrispondenza della profondità dello spazio dei nomi specificata nell'opzione.</span><span class="sxs-lookup"><span data-stu-id="983b1-114">Compose all types at the namespace depth specified in the switch.</span></span>               |
| <span data-ttu-id="983b1-115">-1</span><span class="sxs-lookup"><span data-stu-id="983b1-115">-1</span></span>                             | <span data-ttu-id="983b1-116">Comporre tutti i tipi in un file IDL per ogni spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="983b1-116">Compose all types into one IDL file per namespace.</span></span>                              |
| <span data-ttu-id="983b1-117"><namespace>: Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="983b1-117"><namespace>:Int32 > 0</span></span> | <span data-ttu-id="983b1-118">Comporre tutti i tipi con lo spazio dei nomi corrispondente alla profondità specificata nell'opzione.</span><span class="sxs-lookup"><span data-stu-id="983b1-118">Compose all types with matching namespace at the depth specified in the switch.</span></span> |
| <span data-ttu-id="983b1-119"><namespace>:-1</span><span class="sxs-lookup"><span data-stu-id="983b1-119"><namespace>:-1</span></span>           | <span data-ttu-id="983b1-120">Comporre tutti i tipi con lo spazio dei nomi corrispondente in un unico file per spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="983b1-120">Compose all types with matching namespace into one file per namespace.</span></span>          |



 

<span data-ttu-id="983b1-121">Nella tabella seguente vengono illustrati i risultati di diverse combinazioni dell'opzione **/n** che opera su questi spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="983b1-121">The following table shows the results from different combinations of the **/n** switch working on these namespaces.</span></span>

-   <span data-ttu-id="983b1-122">Windows. Foundation. Collections. all'IIterable</span><span class="sxs-lookup"><span data-stu-id="983b1-122">Windows.Foundation.Collections.IIterable</span></span>
-   <span data-ttu-id="983b1-123">Windows. UI. DirectUI. Controls. Button</span><span class="sxs-lookup"><span data-stu-id="983b1-123">Windows.UI.DirectUI.Controls.Button</span></span>
-   <span data-ttu-id="983b1-124">Windows. UI. DirectUI. Controls. ListView</span><span class="sxs-lookup"><span data-stu-id="983b1-124">Windows.UI.DirectUI.Controls.ListView</span></span>
-   <span data-ttu-id="983b1-125">Windows. UI. immersive. Application. PlayToSpazio. target</span><span class="sxs-lookup"><span data-stu-id="983b1-125">Windows.UI.Immersive.Application.PlayTo.Target</span></span>
-   <span data-ttu-id="983b1-126">Windows. Web. Syndication. RSS</span><span class="sxs-lookup"><span data-stu-id="983b1-126">Windows.Web.Syndication.RSS</span></span>



| <span data-ttu-id="983b1-127">Commutatori</span><span class="sxs-lookup"><span data-stu-id="983b1-127">Switches</span></span>                         | <span data-ttu-id="983b1-128">Risultato</span><span class="sxs-lookup"><span data-stu-id="983b1-128">Result</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="983b1-129">Spiegazione</span><span class="sxs-lookup"><span data-stu-id="983b1-129">Explanation</span></span>                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="983b1-130">**/n:-1**  / **n:1**</span><span class="sxs-lookup"><span data-stu-id="983b1-130">**/n:-1** /**n:1**</span></span>               | <span data-ttu-id="983b1-131">Windows.winmd</span><span class="sxs-lookup"><span data-stu-id="983b1-131">Windows.winmd</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="983b1-132">L'ultima opzione/n esegue l'override di tutte le opzioni-n precedenti.</span><span class="sxs-lookup"><span data-stu-id="983b1-132">The last /n switch overrides all previous –n switches.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="983b1-133">**/n:-1/n: Windows. UI: 2**</span><span class="sxs-lookup"><span data-stu-id="983b1-133">**/n:-1/n:Windows.UI:2**</span></span>         | <dl> <span data-ttu-id="983b1-134">Windows <dt>. Foundation. winmd</dt> <dt>Windows. UI. winmd</dt> <dt>Windows. Web. Syndication. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="983b1-134"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.winmd</dt> <dt>Windows.Web.Syndication.winmd</dt></span></span> </dl> | <dl> <span data-ttu-id="983b1-135"><dt>**Windows. Foundation** è sempre composto in – n:2.</dt></span><span class="sxs-lookup"><span data-stu-id="983b1-135"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="983b1-136"><dt>I tipi **Windows. UI** sono raggruppati.</dt></span><span class="sxs-lookup"><span data-stu-id="983b1-136"><dt>**Windows.UI** types are grouped.</dt></span></span> <span data-ttu-id="983b1-137"><dt>**Windows. Web. Syndication** è costituito in n:-1.</dt></span><span class="sxs-lookup"><span data-stu-id="983b1-137"><dt>**Windows.Web.Syndication** is composed at n:-1.</dt></span></span> </dl>       |
| <span data-ttu-id="983b1-138">**/n: 1/n: Windows. UI. DirectUI: 3**</span><span class="sxs-lookup"><span data-stu-id="983b1-138">**/n:1/n:Windows.UI.DirectUI:3**</span></span> | <dl> <span data-ttu-id="983b1-139">Windows <dt>. Foundation. winmd</dt> <dt>Windows. UI. directui. winmd</dt> <dt>Windows. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="983b1-139"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt></span></span> </dl>       | <dl> <span data-ttu-id="983b1-140"><dt>**Windows. Foundation** è sempre composto in – n:2.</dt></span><span class="sxs-lookup"><span data-stu-id="983b1-140"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="983b1-141"><dt>**Windows. UI. directui** è composto al livello 3.</dt></span><span class="sxs-lookup"><span data-stu-id="983b1-141"><dt>**Windows.UI.DirectUI** is composed at level 3.</dt></span></span> <span data-ttu-id="983b1-142"><dt>Tutti gli altri tipi sono composti al livello 1.</dt></span><span class="sxs-lookup"><span data-stu-id="983b1-142"><dt>All other types are composed at level 1.</dt></span></span> </dl> |



 

<span data-ttu-id="983b1-143">Di seguito sono riportate le regole per la gestione di più istanze dell'opzione **/n** .</span><span class="sxs-lookup"><span data-stu-id="983b1-143">Here are the rules for handling multiple instances of the **/n** switch.</span></span>

-   <span data-ttu-id="983b1-144">L'istanza più specifica prevale.</span><span class="sxs-lookup"><span data-stu-id="983b1-144">The most specific instance prevails.</span></span> <span data-ttu-id="983b1-145">Se ad esempio si specifica **– n:A.B.C: 4 – n:A.B: 5**, MDMERGE risolve a. b. c. D al livello 4, perché a. b. c è più specifico di A.B.</span><span class="sxs-lookup"><span data-stu-id="983b1-145">For example, if you specify **–n:A.B.C:4–n:A.B:5**, MDMERGE resolves A.B.C.D at level 4, because A.B.C is more specific than A.B.</span></span> <span data-ttu-id="983b1-146">A. B. E. F viene risolto alla profondità 5, perché corrisponde A un. B ma non a A.B.C.</span><span class="sxs-lookup"><span data-stu-id="983b1-146">A.B.E.F resolves at depth 5, because it matches A.B but not A.B.C.</span></span>
-   <span data-ttu-id="983b1-147">L'ultima istanza prevale.</span><span class="sxs-lookup"><span data-stu-id="983b1-147">The last instance prevails.</span></span> <span data-ttu-id="983b1-148">Se ad esempio si specifica **– n:5 – n:2**, i tipi sono composti al livello 2.</span><span class="sxs-lookup"><span data-stu-id="983b1-148">For example, if you specify **–n:5–n:2**, the types are composed at level 2.</span></span>
-   <span data-ttu-id="983b1-149">Entrambe le regole si applicano.</span><span class="sxs-lookup"><span data-stu-id="983b1-149">Both of these rules apply.</span></span> <span data-ttu-id="983b1-150">Se si specifica – n:A.B.C: 4 – n:A.B.C: 1, lo spazio dei nomi A. B. C viene composto al livello 1.</span><span class="sxs-lookup"><span data-stu-id="983b1-150">If you specify –n:A.B.C:4 –n:A.B.C:1, namespace A.B.C is composed at level 1.</span></span>

## <a name="examples"></a><span data-ttu-id="983b1-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="983b1-151">Examples</span></span>

<span data-ttu-id="983b1-152">**mdmerge.exe-Metadata \_ dir $ ( \_ percorso metadati SDK \_ )-i $ ( \_ percorso metadati interno SDK \_ \_ )-o $ ( \_ percorso obj) \\ $O \\ SystemMetadata-v-n:-1-n:Windows.Foundation: 2**</span><span class="sxs-lookup"><span data-stu-id="983b1-152">**mdmerge.exe -metadata\_dir $(SDK\_METADATA\_PATH) -i $(INTERNAL\_SDK\_METADATA\_PATH) -o $(OBJ\_PATH)\\$O\\SystemMetadata -v -n:-1 -n:Windows.Foundation:2**</span></span>

## <a name="requirements"></a><span data-ttu-id="983b1-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="983b1-153">Requirements</span></span>



| <span data-ttu-id="983b1-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="983b1-154">Requirement</span></span> | <span data-ttu-id="983b1-155">Valore</span><span class="sxs-lookup"><span data-stu-id="983b1-155">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="983b1-156">Client</span><span class="sxs-lookup"><span data-stu-id="983b1-156">Client</span></span><br/> | <span data-ttu-id="983b1-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="983b1-157">Windows 8</span></span><br/>           |
| <span data-ttu-id="983b1-158">Server</span><span class="sxs-lookup"><span data-stu-id="983b1-158">Server</span></span><br/> | <span data-ttu-id="983b1-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="983b1-159">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="983b1-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="983b1-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983b1-161">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="983b1-161">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





