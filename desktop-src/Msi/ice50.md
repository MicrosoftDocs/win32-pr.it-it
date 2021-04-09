---
description: ICE50 verifica che le icone di collegamento vengano specificate per la visualizzazione corretta e corrispondano all'estensione del file di destinazione.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968100"
---
# <a name="ice50"></a><span data-ttu-id="8d0e1-103">ICE50</span><span class="sxs-lookup"><span data-stu-id="8d0e1-103">ICE50</span></span>

<span data-ttu-id="8d0e1-104">ICE50 verifica che le icone di collegamento vengano specificate per la visualizzazione corretta e corrispondano all'estensione del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8d0e1-104">ICE50 checks that shortcut icons are specified to display correctly and match their target file's extension.</span></span>

## <a name="result"></a><span data-ttu-id="8d0e1-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="8d0e1-105">Result</span></span>

<span data-ttu-id="8d0e1-106">ICE50 Invia un messaggio di errore se l'estensione dei file di icona e di destinazione non corrisponde.</span><span class="sxs-lookup"><span data-stu-id="8d0e1-106">ICE50 posts an error message if the extension of the icon and target files do not match.</span></span> <span data-ttu-id="8d0e1-107">ICE50 pubblica un avviso se le icone sono archiviate in file che non hanno un'estensione. exe o. ico.</span><span class="sxs-lookup"><span data-stu-id="8d0e1-107">ICE50 posts a warning if icons are stored in files that do not have an .exe or .ico extension.</span></span>

## <a name="example"></a><span data-ttu-id="8d0e1-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="8d0e1-108">Example</span></span>

<span data-ttu-id="8d0e1-109">ICE50 segnala l'errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="8d0e1-109">ICE50 reports the following error for the example shown.</span></span>



| <span data-ttu-id="8d0e1-110">Errore o avviso ICE50</span><span class="sxs-lookup"><span data-stu-id="8d0e1-110">ICE50 error or warning</span></span>                                                                                                              | <span data-ttu-id="8d0e1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d0e1-111">Description</span></span>                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0e1-112">L'estensione dell'icona ' icon2. dat ' per il collegamento ' Shortcut2' non corrisponde all'estensione del file di chiave per il componente ' Component2'.</span><span class="sxs-lookup"><span data-stu-id="8d0e1-112">The extension of Icon 'Icon2.dat' for Shortcut 'Shortcut2' does not match the extension of the Key File for component 'Component2'.</span></span> | <span data-ttu-id="8d0e1-113">Se le estensioni dell'icona e il file di destinazione non corrispondono, il collegamento non avrà il menu di scelta rapida corretto quando viene annunciato il componente.</span><span class="sxs-lookup"><span data-stu-id="8d0e1-113">If the extensions of the icon and the target file do not match, the shortcut will not have the correct context menu when the component is advertised.</span></span> <span data-ttu-id="8d0e1-114">Per correggere l'errore, rinominare l'icona in modo che corrisponda all'estensione del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8d0e1-114">To fix this error, rename the icon to match the extension of the target file.</span></span><br/> |
| <span data-ttu-id="8d0e1-115">L'estensione dell'icona ' Icon1.bat' per il collegamento ' Shortcut1' non è "exe" o "ico".</span><span class="sxs-lookup"><span data-stu-id="8d0e1-115">The extension of Icon 'Icon1.bat' for Shortcut 'Shortcut1' is not "exe" or "ico".</span></span> <span data-ttu-id="8d0e1-116">L'icona non viene visualizzata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8d0e1-116">The Icon will not be displayed correctly.</span></span>         | <span data-ttu-id="8d0e1-117">Non tutte le versioni della shell visualizzano correttamente le icone archiviate in file privi di estensioni di "exe" o "ico".</span><span class="sxs-lookup"><span data-stu-id="8d0e1-117">Not all versions of the shell correctly display icons stored in files that do not have extensions of "exe" or "ico".</span></span> <span data-ttu-id="8d0e1-118">Per correggere il problema, rinominare l'icona con estensione "exe" o "ico".</span><span class="sxs-lookup"><span data-stu-id="8d0e1-118">To fix this warning, rename the icon have an extension of "exe" or "ico".</span></span><br/>                                      |



 

<span data-ttu-id="8d0e1-119">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="8d0e1-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="8d0e1-120">File</span><span class="sxs-lookup"><span data-stu-id="8d0e1-120">File</span></span>  | <span data-ttu-id="8d0e1-121">FileName</span><span class="sxs-lookup"><span data-stu-id="8d0e1-121">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="8d0e1-122">File1</span><span class="sxs-lookup"><span data-stu-id="8d0e1-122">File1</span></span> | <span data-ttu-id="8d0e1-123">File1.bat</span><span class="sxs-lookup"><span data-stu-id="8d0e1-123">File1.bat</span></span> |
| <span data-ttu-id="8d0e1-124">File2</span><span class="sxs-lookup"><span data-stu-id="8d0e1-124">File2</span></span> | <span data-ttu-id="8d0e1-125">File2.pl</span><span class="sxs-lookup"><span data-stu-id="8d0e1-125">File2.pl</span></span>  |



 

<span data-ttu-id="8d0e1-126">[Tabella delle funzionalità](feature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="8d0e1-126">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="8d0e1-127">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="8d0e1-127">Feature</span></span>  |
|----------|
| <span data-ttu-id="8d0e1-128">Feature1</span><span class="sxs-lookup"><span data-stu-id="8d0e1-128">Feature1</span></span> |



 

<span data-ttu-id="8d0e1-129">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="8d0e1-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="8d0e1-130">Componente</span><span class="sxs-lookup"><span data-stu-id="8d0e1-130">Component</span></span>  | <span data-ttu-id="8d0e1-131">KeyPath</span><span class="sxs-lookup"><span data-stu-id="8d0e1-131">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="8d0e1-132">Component1</span><span class="sxs-lookup"><span data-stu-id="8d0e1-132">Component1</span></span> | <span data-ttu-id="8d0e1-133">File1</span><span class="sxs-lookup"><span data-stu-id="8d0e1-133">File1</span></span>   |
| <span data-ttu-id="8d0e1-134">Component2</span><span class="sxs-lookup"><span data-stu-id="8d0e1-134">Component2</span></span> | <span data-ttu-id="8d0e1-135">File2</span><span class="sxs-lookup"><span data-stu-id="8d0e1-135">File2</span></span>   |



 

[<span data-ttu-id="8d0e1-136">Icona tabella</span><span class="sxs-lookup"><span data-stu-id="8d0e1-136">Icon Table</span></span>](icon-table.md)



| <span data-ttu-id="8d0e1-137">Nome</span><span class="sxs-lookup"><span data-stu-id="8d0e1-137">Name</span></span>      | <span data-ttu-id="8d0e1-138">Data</span><span class="sxs-lookup"><span data-stu-id="8d0e1-138">Data</span></span>            |
|-----------|-----------------|
| <span data-ttu-id="8d0e1-139">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="8d0e1-139">Icon1.bat</span></span> | <span data-ttu-id="8d0e1-140">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="8d0e1-140">\[Binary Data\]</span></span> |
| <span data-ttu-id="8d0e1-141">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="8d0e1-141">Icon2.dat</span></span> | <span data-ttu-id="8d0e1-142">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="8d0e1-142">\[Binary Data\]</span></span> |



 

<span data-ttu-id="8d0e1-143">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="8d0e1-143">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="8d0e1-144">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="8d0e1-144">Shortcut</span></span>  | <span data-ttu-id="8d0e1-145">Componente</span><span class="sxs-lookup"><span data-stu-id="8d0e1-145">Component</span></span>  | <span data-ttu-id="8d0e1-146">Destinazione</span><span class="sxs-lookup"><span data-stu-id="8d0e1-146">Target</span></span>   | <span data-ttu-id="8d0e1-147">Icona\_</span><span class="sxs-lookup"><span data-stu-id="8d0e1-147">Icon\_</span></span>    |
|-----------|------------|----------|-----------|
| <span data-ttu-id="8d0e1-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="8d0e1-148">Shortcut1</span></span> | <span data-ttu-id="8d0e1-149">Component1</span><span class="sxs-lookup"><span data-stu-id="8d0e1-149">Component1</span></span> | <span data-ttu-id="8d0e1-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="8d0e1-150">Feature1</span></span> | <span data-ttu-id="8d0e1-151">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="8d0e1-151">Icon1.bat</span></span> |
| <span data-ttu-id="8d0e1-152">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="8d0e1-152">Shortcut2</span></span> | <span data-ttu-id="8d0e1-153">Component2</span><span class="sxs-lookup"><span data-stu-id="8d0e1-153">Component2</span></span> | <span data-ttu-id="8d0e1-154">Feature1</span><span class="sxs-lookup"><span data-stu-id="8d0e1-154">Feature1</span></span> | <span data-ttu-id="8d0e1-155">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="8d0e1-155">Icon2.dat</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8d0e1-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d0e1-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d0e1-157">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="8d0e1-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




