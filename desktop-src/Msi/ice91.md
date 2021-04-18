---
description: ICE91 pubblica un avviso se un file, un file con estensione ini o un file di collegamento è installato in una directory solo per singolo utente.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316272"
---
# <a name="ice91"></a><span data-ttu-id="5bbb0-103">ICE91</span><span class="sxs-lookup"><span data-stu-id="5bbb0-103">ICE91</span></span>

<span data-ttu-id="5bbb0-104">ICE91 pubblica un avviso se un file, un file con estensione ini o un file di collegamento è installato in una directory solo per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-104">ICE91 posts a warning if a file, .ini file, or shortcut file is installed into a per-user only directory.</span></span> <span data-ttu-id="5bbb0-105">Questi avvisi sono innocui se il pacchetto viene usato solo per l'installazione nel contesto di [installazione](installation-context.md) per utente e mai usato per le installazioni per computer.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-105">These warnings are harmless if the package is only used for installation in the per-user [installation context](installation-context.md) and never used for per-machine installations.</span></span>

<span data-ttu-id="5bbb0-106">I file, i file con estensione ini o i collegamenti nelle directory solo per utente vengono installati nel profilo di un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-106">Files, .ini files, or shortcuts in per-user only directories are installed into a particular user's profile.</span></span> <span data-ttu-id="5bbb0-107">Anche se l'utente imposta la proprietà [**ALLUSERS**](allusers.md) per le installazioni per computer, i file, i file ini o i collegamenti nelle directory solo per singolo utente non vengono copiati nel profilo "tutti gli utenti" e non sono disponibili ad altri utenti.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-107">Even if the user sets the [**ALLUSERS**](allusers.md) property for a per-machine installations, files, .ini files, or shortcuts in per-user only directories are not copied in to the "All Users" profile and are not available to other users.</span></span> <span data-ttu-id="5bbb0-108">Le directory solo per utente non variano in base alla proprietà **ALLUSERS** .</span><span class="sxs-lookup"><span data-stu-id="5bbb0-108">The per-user only directories do not vary with the **ALLUSERS** property.</span></span> <span data-ttu-id="5bbb0-109">Di seguito è riportato un elenco delle directory solo per utente:</span><span class="sxs-lookup"><span data-stu-id="5bbb0-109">The following is a list of the per-user only directories:</span></span>

-   <span data-ttu-id="5bbb0-110">CartellaDatiApp</span><span class="sxs-lookup"><span data-stu-id="5bbb0-110">AppDataFolder</span></span>
-   <span data-ttu-id="5bbb0-111">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-111">FavoritesFolder</span></span>
-   <span data-ttu-id="5bbb0-112">NetHoodFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-112">NetHoodFolder</span></span>
-   <span data-ttu-id="5bbb0-113">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-113">PersonalFolder</span></span>
-   <span data-ttu-id="5bbb0-114">PrintHoodFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-114">PrintHoodFolder</span></span>
-   <span data-ttu-id="5bbb0-115">RecentFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-115">RecentFolder</span></span>
-   <span data-ttu-id="5bbb0-116">SendToFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-116">SendToFolder</span></span>
-   <span data-ttu-id="5bbb0-117">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-117">MyPicturesFolder</span></span>
-   <span data-ttu-id="5bbb0-118">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-118">LocalAppDataFolder</span></span>

## <a name="result"></a><span data-ttu-id="5bbb0-119">Risultato</span><span class="sxs-lookup"><span data-stu-id="5bbb0-119">Result</span></span>

<span data-ttu-id="5bbb0-120">ICE91 invia gli avvisi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-120">ICE91 posts the following warnings.</span></span>



| <span data-ttu-id="5bbb0-121">Avviso di ICE91</span><span class="sxs-lookup"><span data-stu-id="5bbb0-121">ICE91 warning</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="5bbb0-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bbb0-122">Description</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbb0-123">Il file ' \[ 1 \] ' verrà installato nella directory per utente ' \[ 2 \] ' che non varia in base al valore di [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="5bbb0-123">The file '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="5bbb0-124">Il file non verrà copiato nel profilo di ogni utente anche se si desidera un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-124">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>     | <span data-ttu-id="5bbb0-125">Il file viene installato in una directory solo per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-125">The file is installed into a per-user only directory.</span></span> <span data-ttu-id="5bbb0-126">Non viene installato nel profilo di ogni utente durante un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-126">It is not installed into each user's profile during a per-machine installation.</span></span>      |
| <span data-ttu-id="5bbb0-127">Il IniFile ' \[ 1 \] ' verrà installato nella directory per utente ' \[ 2 \] ' che non varia in base al valore di [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="5bbb0-127">The IniFile '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="5bbb0-128">Il file non verrà copiato nel profilo di ogni utente anche se si desidera un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-128">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>  | <span data-ttu-id="5bbb0-129">Il file ini viene installato in una directory solo per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-129">The .ini file is installed into a per-user only directory.</span></span> <span data-ttu-id="5bbb0-130">Non viene installato nel profilo di ogni utente durante un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-130">It is not installed into each user's profile during a per-machine installation.</span></span> |
| <span data-ttu-id="5bbb0-131">Il collegamento ' \[ 1 \] ' verrà installato nella directory per utente ' \[ 2 \] ' che non varia in base al valore di [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="5bbb0-131">The shortcut '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="5bbb0-132">Il file non verrà copiato nel profilo di ogni utente anche se si desidera un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-132">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span> | <span data-ttu-id="5bbb0-133">Il collegamento viene installato in una directory solo per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-133">The shortcut is installed into a per-user only directory.</span></span> <span data-ttu-id="5bbb0-134">Non viene installato nel profilo di ogni utente durante un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="5bbb0-134">It is not installed into each user's profile during a per-machine installation.</span></span>  |



 

## <a name="example"></a><span data-ttu-id="5bbb0-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="5bbb0-135">Example</span></span>

<span data-ttu-id="5bbb0-136">ICE91 segnala gli avvisi seguenti per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="5bbb0-136">ICE91 reports the following warnings for the example:</span></span>

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

<span data-ttu-id="5bbb0-137">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="5bbb0-137">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="5bbb0-138">File</span><span class="sxs-lookup"><span data-stu-id="5bbb0-138">File</span></span>  | <span data-ttu-id="5bbb0-139">Componente\_</span><span class="sxs-lookup"><span data-stu-id="5bbb0-139">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="5bbb0-140">File1</span><span class="sxs-lookup"><span data-stu-id="5bbb0-140">File1</span></span> | <span data-ttu-id="5bbb0-141">C1</span><span class="sxs-lookup"><span data-stu-id="5bbb0-141">C1</span></span>          |



 

<span data-ttu-id="5bbb0-142">[Tabella componenti](component-table.md) (parziale) (parziale) (parziale) (parziale)</span><span class="sxs-lookup"><span data-stu-id="5bbb0-142">[Component Table](component-table.md) (partial) (partial) (partial) (partial)</span></span>



| <span data-ttu-id="5bbb0-143">Componente</span><span class="sxs-lookup"><span data-stu-id="5bbb0-143">Component</span></span> | <span data-ttu-id="5bbb0-144">Directory\_</span><span class="sxs-lookup"><span data-stu-id="5bbb0-144">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="5bbb0-145">C1</span><span class="sxs-lookup"><span data-stu-id="5bbb0-145">C1</span></span>        | <span data-ttu-id="5bbb0-146">MyDir</span><span class="sxs-lookup"><span data-stu-id="5bbb0-146">MyDir</span></span>       |



 

[<span data-ttu-id="5bbb0-147">Tabella IniFile</span><span class="sxs-lookup"><span data-stu-id="5bbb0-147">IniFile Table</span></span>](inifile-table.md)



| <span data-ttu-id="5bbb0-148">IniFile</span><span class="sxs-lookup"><span data-stu-id="5bbb0-148">IniFile</span></span>  | <span data-ttu-id="5bbb0-149">DirProperty</span><span class="sxs-lookup"><span data-stu-id="5bbb0-149">DirProperty</span></span> |
|----------|-------------|
| <span data-ttu-id="5bbb0-150">IniFile1</span><span class="sxs-lookup"><span data-stu-id="5bbb0-150">IniFile1</span></span> | <span data-ttu-id="5bbb0-151">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="5bbb0-151">MyIniDir</span></span>    |



 

[<span data-ttu-id="5bbb0-152">Tabella di collegamento</span><span class="sxs-lookup"><span data-stu-id="5bbb0-152">Shortcut Table</span></span>](shortcut-table.md)



| <span data-ttu-id="5bbb0-153">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="5bbb0-153">Shortcut</span></span>  | <span data-ttu-id="5bbb0-154">Directory\_</span><span class="sxs-lookup"><span data-stu-id="5bbb0-154">Directory\_</span></span>   |
|-----------|---------------|
| <span data-ttu-id="5bbb0-155">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="5bbb0-155">Shortcut1</span></span> | <span data-ttu-id="5bbb0-156">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="5bbb0-156">MyShortcutDir</span></span> |



 

[<span data-ttu-id="5bbb0-157">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="5bbb0-157">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="5bbb0-158">Directory</span><span class="sxs-lookup"><span data-stu-id="5bbb0-158">Directory</span></span>     | <span data-ttu-id="5bbb0-159">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="5bbb0-159">Directory\_Parent</span></span>  |
|---------------|--------------------|
| <span data-ttu-id="5bbb0-160">MyDir</span><span class="sxs-lookup"><span data-stu-id="5bbb0-160">MyDir</span></span>         | <span data-ttu-id="5bbb0-161">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-161">FavoritesFolder</span></span>    |
| <span data-ttu-id="5bbb0-162">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="5bbb0-162">MyIniDir</span></span>      | <span data-ttu-id="5bbb0-163">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-163">LocalAppDataFolder</span></span> |
| <span data-ttu-id="5bbb0-164">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="5bbb0-164">MyShortcutDir</span></span> | <span data-ttu-id="5bbb0-165">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="5bbb0-165">PersonalFolder</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="5bbb0-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5bbb0-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bbb0-167">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="5bbb0-167">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



