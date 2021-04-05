---
title: Compilazione del markup della barra multifunzione
description: Affinché il Framework della barra multifunzione di Windows utilizzi il file di markup della barra multifunzione, il file di markup deve essere compilato in un file di risorse in formato binario.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Barra multifunzione di Windows, compilazione del markup
- Barra multifunzione, compilazione del markup
- Barra multifunzione di Windows, flusso di lavoro del compilatore
- Barra multifunzione, flusso di lavoro del compilatore
- Barra multifunzione di Windows, compilatore comando interfaccia utente (UICC.exe)
- Barra multifunzione, compilatore comando interfaccia utente (UICC.exe)
- Compilatore comando interfaccia utente (UICC.exe)
- UICC.exe (compilatore di comandi dell'interfaccia utente)
- compilazione del markup della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515949"
---
# <a name="compiling-ribbon-markup"></a><span data-ttu-id="5638c-112">Compilazione del markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="5638c-112">Compiling Ribbon Markup</span></span>

<span data-ttu-id="5638c-113">Affinché il Framework della barra multifunzione di Windows utilizzi il file di [markup della barra multifunzione](windowsribbon-schema.md) , il file di markup deve essere compilato in un file di risorse in formato binario.</span><span class="sxs-lookup"><span data-stu-id="5638c-113">For the Windows Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="5638c-114">Un compilatore di markup dedicato, il compilatore di comandi dell'interfaccia utente (UICC), è incluso in Windows Software Development Kit (SDK) (7,0 o versione successiva) a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="5638c-114">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="5638c-115">Oltre a compilare la versione binaria del markup, UICC genera un file di intestazione di definizione ID (con estensione h) che espone tutti gli elementi di markup all'applicazione host della barra multifunzione e un file di risorse (RC) usato per collegare le risorse di tipo immagine e stringa all'applicazione host in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="5638c-115">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

-   [<span data-ttu-id="5638c-116">Flusso di lavoro del compilatore</span><span class="sxs-lookup"><span data-stu-id="5638c-116">Compiler Workflow</span></span>](#compiler-workflow)
-   [<span data-ttu-id="5638c-117">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="5638c-117">Command-Line Syntax</span></span>](#command-line-syntax)
    -   [<span data-ttu-id="5638c-118">Argomenti e opzioni</span><span class="sxs-lookup"><span data-stu-id="5638c-118">Arguments and Options</span></span>](#arguments-and-options)
    -   [<span data-ttu-id="5638c-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="5638c-119">Example</span></span>](#example)
-   [<span data-ttu-id="5638c-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5638c-120">Related topics</span></span>](#related-topics)

## <a name="compiler-workflow"></a><span data-ttu-id="5638c-121">Flusso di lavoro del compilatore</span><span class="sxs-lookup"><span data-stu-id="5638c-121">Compiler Workflow</span></span>

<span data-ttu-id="5638c-122">Nel diagramma seguente viene illustrato il flusso di lavoro del compilatore di markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="5638c-122">The workflow of the Ribbon markup compiler is illustrated in the following diagram.</span></span>

![diagramma che illustra il flusso di lavoro del compilatore di markup Ribbon.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a><span data-ttu-id="5638c-124">Sintassi della riga di comando</span><span class="sxs-lookup"><span data-stu-id="5638c-124">Command-Line Syntax</span></span>

<span data-ttu-id="5638c-125">Nell'esempio seguente viene illustrata la sintassi della riga di comando per il compilatore di markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="5638c-125">The command-line syntax for the Ribbon markup compiler is shown in the following example.</span></span>


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a><span data-ttu-id="5638c-126">Argomenti e opzioni</span><span class="sxs-lookup"><span data-stu-id="5638c-126">Arguments and Options</span></span>

<span data-ttu-id="5638c-127">Gli argomenti e le opzioni per questo strumento sono descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5638c-127">The arguments and options for this tool are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="5638c-128">Le opzioni della riga di comando elencate devono essere specificate nell'ordine indicato.</span><span class="sxs-lookup"><span data-stu-id="5638c-128">The command-line options listed must be specified in the order given.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5638c-129">Opzione</span><span class="sxs-lookup"><span data-stu-id="5638c-129">Option</span></span></th>
<th><span data-ttu-id="5638c-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5638c-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5638c-131">/header<headerFile></span><span class="sxs-lookup"><span data-stu-id="5638c-131">/header:<headerFile></span></span></td>
<td><span data-ttu-id="5638c-132">Genera un file di intestazione denominato <headerFile> che contiene i simboli delle risorse dell'ID comando di markup.</span><span class="sxs-lookup"><span data-stu-id="5638c-132">Generate a header file called <headerFile> that contains the markup Command ID resource symbols.</span></span> <span data-ttu-id="5638c-133">Se omesso, non viene generato un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="5638c-133">If omitted, a header file is not generated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5638c-134">/res<resourceFile></span><span class="sxs-lookup"><span data-stu-id="5638c-134">/res:<resourceFile></span></span></td>
<td><span data-ttu-id="5638c-135">Generare un file di risorse denominato <resourceFile> che collega tutte le risorse di tipo image e String, il file di markup binario e il file di intestazione all'applicazione host in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="5638c-135">Generate a resource file called <resourceFile> that links all image and string resources, the binary markup file, and the header file to the host application at build time.</span></span> <span data-ttu-id="5638c-136">Se omesso, non viene generato un file di risorse.</span><span class="sxs-lookup"><span data-stu-id="5638c-136">If omitted, a resource file is not generated.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5638c-137">/Name<ribbonName></span><span class="sxs-lookup"><span data-stu-id="5638c-137">/name:<ribbonName></span></span></td>
<td><span data-ttu-id="5638c-138">Nome della risorsa per il file di markup binario registrato in <resourceFile> .</span><span class="sxs-lookup"><span data-stu-id="5638c-138">The resource name for the binary markup file that is logged in the <resourceFile>.</span></span> <span data-ttu-id="5638c-139">Il valore predefinito è APPLICATION_RIBBON.</span><span class="sxs-lookup"><span data-stu-id="5638c-139">The default is APPLICATION_RIBBON.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5638c-140">/W{0\1\2}</span><span class="sxs-lookup"><span data-stu-id="5638c-140">/W{0\1\2}</span></span></td>
<td><span data-ttu-id="5638c-141">Filtrare i messaggi di evento in base alla gravità.</span><span class="sxs-lookup"><span data-stu-id="5638c-141">Filter the event messages based on severity.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5638c-142">0</span><span class="sxs-lookup"><span data-stu-id="5638c-142">0</span></span><br/></td>
<td><span data-ttu-id="5638c-143">Solo messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="5638c-143">Error messages only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5638c-144">1</span><span class="sxs-lookup"><span data-stu-id="5638c-144">1</span></span><br/></td>
<td><span data-ttu-id="5638c-145">Solo messaggi di errore e di avviso.</span><span class="sxs-lookup"><span data-stu-id="5638c-145">Error and Warning messages only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5638c-146"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="5638c-146"><strong>2</strong></span></span><br/></td>
<td><span data-ttu-id="5638c-147">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5638c-147">Default.</span></span> <br/> <span data-ttu-id="5638c-148">Messaggi di errore, di avviso e informativi.</span><span class="sxs-lookup"><span data-stu-id="5638c-148">Error, Warning, and Informational messages.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a><span data-ttu-id="5638c-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="5638c-149">Example</span></span>

<span data-ttu-id="5638c-150">Nell'esempio seguente viene illustrato come utilizzare il compilatore di markup della barra multifunzione per generare un set tipico di file di risorse per un'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="5638c-150">The following example demonstrates how to use the Ribbon markup compiler to generate a typical set of resource files for a Ribbon application.</span></span>

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a><span data-ttu-id="5638c-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5638c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5638c-152">Dichiarazione di comandi e controlli con markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="5638c-152">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="5638c-153">Creazione di un'applicazione Ribbon</span><span class="sxs-lookup"><span data-stu-id="5638c-153">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





