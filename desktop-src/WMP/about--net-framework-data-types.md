---
title: Informazioni sui tipi di dati .NET Framework
description: Informazioni sui tipi di dati .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player, .NET Framework
- Modello a oggetti Media Player Windows, .NET Framework
- modello a oggetti, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Windows Media Player ActiveX Control, .NET Framework
- Controllo ActiveX Windows Media Player Mobile, .NET Framework
- Controllo ActiveX, .NET Framework
- .NET Framework, tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045214"
---
# <a name="about-net-framework-data-types"></a><span data-ttu-id="46720-111">Informazioni sui tipi di dati .NET Framework</span><span class="sxs-lookup"><span data-stu-id="46720-111">About .NET Framework Data Types</span></span>

<span data-ttu-id="46720-112">Questa sezione contiene le informazioni necessarie per tradurre il riferimento del modello a oggetti orientato allo script in Microsoft .NET tipi di dati di base del Framework.</span><span class="sxs-lookup"><span data-stu-id="46720-112">This section contains the information you need to translate the script-oriented Object Model Reference into Microsoft .NET Framework base data types.</span></span> <span data-ttu-id="46720-113">Il riferimento agli script di Windows Media Player include quasi tutte le informazioni necessarie per utilizzare il controllo Media Player di Windows in un programma basato su .NET Framework e, nella maggior parte dei casi, la sintassi sarà simile a quella di altri linguaggi di scripting, ad esempio Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="46720-113">The Windows Media Player script reference has almost all the information you need to use the Windows Media Player control in a .NET Framework-based program, and in most cases, the syntax will be similar to that of other scripting languages such as Microsoft JScript.</span></span>

<span data-ttu-id="46720-114">Il riferimento a Windows Media Player fornisce il tipo di dati JScript e, se necessario, la conversione in C++.</span><span class="sxs-lookup"><span data-stu-id="46720-114">The Windows Media Player reference provides the JScript data type and, if necessary, the C++ conversion.</span></span> <span data-ttu-id="46720-115">Un **numero** , ad esempio, potrebbe essere restituito da un metodo.</span><span class="sxs-lookup"><span data-stu-id="46720-115">For example, a **Number** might be returned by a method.</span></span> <span data-ttu-id="46720-116">JScript considera tutti i numeri nello stesso modo, ma altri linguaggi distinguono tra tipi diversi di numeri (Integer, virgola mobile e così via).</span><span class="sxs-lookup"><span data-stu-id="46720-116">JScript treats all numbers in the same way, but other languages distinguish between different types of numbers (integer, floating point, and so on).</span></span> <span data-ttu-id="46720-117">Il riferimento fornisce la conversione C++ per i tipi di dati numerici perché i numeri possono essere elaborati in modo diverso in C++.</span><span class="sxs-lookup"><span data-stu-id="46720-117">The reference gives the C++ conversion for number data types because numbers can be processed differently by C++.</span></span> <span data-ttu-id="46720-118">Ad esempio, C++ usa il tipo di dati **int** per i calcoli Integer e **float** per virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="46720-118">For example, C++ uses the **int** data type for integer arithmetic and **float** for floating point.</span></span>

<span data-ttu-id="46720-119">Il .NET Framework utilizza un sistema leggermente diverso di tipi di dati di base.</span><span class="sxs-lookup"><span data-stu-id="46720-119">The .NET Framework uses a slightly different system of base data types.</span></span> <span data-ttu-id="46720-120">Nella tabella seguente vengono illustrate le differenze nei tipi di dati comuni che è probabile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="46720-120">The following table shows the differences in the common data types you are likely to use.</span></span> <span data-ttu-id="46720-121">Per ulteriori informazioni su .NET Framework tipi di dati di base e sulla conversione ad altri sistemi con tipi di dati, vedere la guida per gli sviluppatori .NET Framework informazioni sui tipi di dati di base dello spazio dei nomi del sistema.</span><span class="sxs-lookup"><span data-stu-id="46720-121">For more information on .NET Framework base data types and the conversion to other data type systems, see the .NET Framework Developer's Guide discussion of System Namespace base data types.</span></span>

<span data-ttu-id="46720-122">Questa tabella indica il nome della classe .NET Framework e il tipo di dati C#.</span><span class="sxs-lookup"><span data-stu-id="46720-122">This table gives the .NET Framework class name and the C# data type.</span></span> <span data-ttu-id="46720-123">I tipi di dati per le altre lingue vengono definiti per ogni lingua nei rispettivi riferimenti al linguaggio.</span><span class="sxs-lookup"><span data-stu-id="46720-123">Data types for other languages are defined for each language in their respective language references.</span></span>



| <span data-ttu-id="46720-124">Tipo di dati script</span><span class="sxs-lookup"><span data-stu-id="46720-124">Script data type</span></span> | <span data-ttu-id="46720-125">Tipo di dati C++</span><span class="sxs-lookup"><span data-stu-id="46720-125">C++ data type</span></span>     | <span data-ttu-id="46720-126">Classe .NET Framework (tipo di dati C#)</span><span class="sxs-lookup"><span data-stu-id="46720-126">.NET Framework class (C# data type )</span></span> |
|------------------|-------------------|---------------------------------------|
| <span data-ttu-id="46720-127">**Number**</span><span class="sxs-lookup"><span data-stu-id="46720-127">**Number**</span></span>       | <span data-ttu-id="46720-128">**int**</span><span class="sxs-lookup"><span data-stu-id="46720-128">**int**</span></span>           | <span data-ttu-id="46720-129">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="46720-129">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="46720-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="46720-130">**Number**</span></span>       | <span data-ttu-id="46720-131">**long**</span><span class="sxs-lookup"><span data-stu-id="46720-131">**long**</span></span>          | <span data-ttu-id="46720-132">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="46720-132">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="46720-133">**Number**</span><span class="sxs-lookup"><span data-stu-id="46720-133">**Number**</span></span>       | <span data-ttu-id="46720-134">**double**</span><span class="sxs-lookup"><span data-stu-id="46720-134">**double**</span></span>        | <span data-ttu-id="46720-135">**Double** (**Double**)</span><span class="sxs-lookup"><span data-stu-id="46720-135">**Double** (**double**)</span></span>               |
| <span data-ttu-id="46720-136">**Number**</span><span class="sxs-lookup"><span data-stu-id="46720-136">**Number**</span></span>       | <span data-ttu-id="46720-137">**float**</span><span class="sxs-lookup"><span data-stu-id="46720-137">**float**</span></span>         | <span data-ttu-id="46720-138">**Singolo** (**float**)</span><span class="sxs-lookup"><span data-stu-id="46720-138">**Single** (**float**)</span></span>                |
| <span data-ttu-id="46720-139">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="46720-139">**String**</span></span>       | <span data-ttu-id="46720-140">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="46720-140">**BSTR**</span></span>          | <span data-ttu-id="46720-141">**String** (**stringa**)</span><span class="sxs-lookup"><span data-stu-id="46720-141">**String** (**string**)</span></span>               |
| <span data-ttu-id="46720-142">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="46720-142">**Boolean**</span></span>      | <span data-ttu-id="46720-143">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="46720-143">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="46720-144">**Boolean** (**bool**)</span><span class="sxs-lookup"><span data-stu-id="46720-144">**Boolean** (**bool**)</span></span>                |
| <span data-ttu-id="46720-145">**Object**</span><span class="sxs-lookup"><span data-stu-id="46720-145">**Object**</span></span>       | <span data-ttu-id="46720-146">**Object**</span><span class="sxs-lookup"><span data-stu-id="46720-146">**Object**</span></span>        | <span data-ttu-id="46720-147">**Oggetto** (**oggetto**)</span><span class="sxs-lookup"><span data-stu-id="46720-147">**Object** (**object**)</span></span>               |



 

<span data-ttu-id="46720-148">Se si utilizza Visual Studio, è possibile utilizzare la tecnologia Microsoft IntelliSense per determinare il tipo di dati previsto per una funzione specifica.</span><span class="sxs-lookup"><span data-stu-id="46720-148">If you are using Visual Studio, you can use the Microsoft IntelliSense technology to determine what data type is expected for a specific function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46720-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46720-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46720-150">**Incorporamento del controllo Media Player Windows in una soluzione .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="46720-150">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="46720-151">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="46720-151">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




