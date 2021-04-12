---
description: ICEM11 verifica che un modulo merge configurabile elenchi la tabella ModuleConfiguration e la tabella ModuleSubstitution nella tabella ModuleIgnoreTable del modulo.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232444"
---
# <a name="icem11"></a><span data-ttu-id="569ac-103">ICEM11</span><span class="sxs-lookup"><span data-stu-id="569ac-103">ICEM11</span></span>

<span data-ttu-id="569ac-104">ICEM11 verifica che un modulo merge configurabile elenchi la tabella [ModuleConfiguration](moduleconfiguration-table.md) e la [tabella ModuleSubstitution](modulesubstitution-table.md) nella [tabella ModuleIgnoreTable](moduleignoretable-table.md) del modulo.</span><span class="sxs-lookup"><span data-stu-id="569ac-104">ICEM11 verifies that a Configurable Merge Module lists the [ModuleConfiguration table](moduleconfiguration-table.md) and [ModuleSubstitution table](modulesubstitution-table.md) in the [ModuleIgnoreTable table](moduleignoretable-table.md) of the module.</span></span> <span data-ttu-id="569ac-105">In questo modo si garantisce che gli strumenti di merge che non riconoscono i moduli unione configurabili (minori della versione 2,0) non copino queste tabelle nel database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="569ac-105">This ensures that merge tools that do not recognize configurable merge modules(less than version 2.0) do not copy these tables into the target database.</span></span>

<span data-ttu-id="569ac-106">Questo ICEM è disponibile nel file Mergemod. cub fornito in Windows Installer SDK 2,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="569ac-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="569ac-107">Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="569ac-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="569ac-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="569ac-108">Result</span></span>

<span data-ttu-id="569ac-109">ICEM11 Invia un errore se il modulo contiene una tabella ModuleConfiguration o ModuleSubstitution non elencata nella tabella ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="569ac-109">ICEM11 posts an error if the module contains a ModuleConfiguration or ModuleSubstitution table not listed in the ModuleIgnoreTable table.</span></span>

## <a name="example"></a><span data-ttu-id="569ac-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="569ac-110">Example</span></span>

<span data-ttu-id="569ac-111">ICEM11 invia i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="569ac-111">ICEM11 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

<span data-ttu-id="569ac-112">[ModuleConfiguration](moduleconfiguration-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="569ac-112">[ModuleConfiguration](moduleconfiguration-table.md) (partial)</span></span>



| <span data-ttu-id="569ac-113">Nome</span><span class="sxs-lookup"><span data-stu-id="569ac-113">Name</span></span>     | <span data-ttu-id="569ac-114">Formato</span><span class="sxs-lookup"><span data-stu-id="569ac-114">Format</span></span> | <span data-ttu-id="569ac-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="569ac-115">Type</span></span>   | <span data-ttu-id="569ac-116">ContextData</span><span class="sxs-lookup"><span data-stu-id="569ac-116">ContextData</span></span> | <span data-ttu-id="569ac-117">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="569ac-117">DefaultValue</span></span> |
|----------|--------|--------|-------------|--------------|
| <span data-ttu-id="569ac-118">IconKey1</span><span class="sxs-lookup"><span data-stu-id="569ac-118">IconKey1</span></span> | <span data-ttu-id="569ac-119">1</span><span class="sxs-lookup"><span data-stu-id="569ac-119">1</span></span>      | <span data-ttu-id="569ac-120">Binary</span><span class="sxs-lookup"><span data-stu-id="569ac-120">Binary</span></span> | <span data-ttu-id="569ac-121">Icona</span><span class="sxs-lookup"><span data-stu-id="569ac-121">Icon</span></span>        | <span data-ttu-id="569ac-122">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="569ac-122">DefaultIcon</span></span>  |



 

[<span data-ttu-id="569ac-123">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="569ac-123">ModuleSubstitution</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="569ac-124">Tabella</span><span class="sxs-lookup"><span data-stu-id="569ac-124">Table</span></span>   | <span data-ttu-id="569ac-125">Riga</span><span class="sxs-lookup"><span data-stu-id="569ac-125">Row</span></span>              | <span data-ttu-id="569ac-126">Colonna</span><span class="sxs-lookup"><span data-stu-id="569ac-126">Column</span></span> | <span data-ttu-id="569ac-127">valore</span><span class="sxs-lookup"><span data-stu-id="569ac-127">Value</span></span>        |
|---------|------------------|--------|--------------|
| <span data-ttu-id="569ac-128">Control</span><span class="sxs-lookup"><span data-stu-id="569ac-128">Control</span></span> | <span data-ttu-id="569ac-129">Dialog1; Control1</span><span class="sxs-lookup"><span data-stu-id="569ac-129">Dialog1;Control1</span></span> | <span data-ttu-id="569ac-130">Testo</span><span class="sxs-lookup"><span data-stu-id="569ac-130">Text</span></span>   | <span data-ttu-id="569ac-131">\[IconKey1\]</span><span class="sxs-lookup"><span data-stu-id="569ac-131">\[IconKey1\]</span></span> |



 

[<span data-ttu-id="569ac-132">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="569ac-132">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)



| <span data-ttu-id="569ac-133">Tabella</span><span class="sxs-lookup"><span data-stu-id="569ac-133">Table</span></span>               |
|---------------------|
| <span data-ttu-id="569ac-134">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="569ac-134">ModuleConfiguration</span></span> |



 

<span data-ttu-id="569ac-135">Per correggere l'errore, includere entrambe le tabelle ModuleSubstitution e ModuleConfiguration nella tabella ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="569ac-135">To fix this error include both the ModuleSubstitution and ModuleConfiguration tables in the ModuleIgnoreTable table.</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="569ac-136">Tabella utilizzata durante l'esecuzione</span><span class="sxs-lookup"><span data-stu-id="569ac-136">Table Used During Execution</span></span>

[<span data-ttu-id="569ac-137">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="569ac-137">ModuleSubstitution</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="569ac-138">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="569ac-138">ModuleConfiguration</span></span>](moduleconfiguration-table.md)

[<span data-ttu-id="569ac-139">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="569ac-139">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)

## <a name="related-topics"></a><span data-ttu-id="569ac-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="569ac-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="569ac-141">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="569ac-141">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



