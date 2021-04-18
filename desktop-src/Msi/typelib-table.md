---
description: La tabella TypeLib contiene le informazioni che devono essere inserite nella registrazione del registro di sistema delle librerie dei tipi.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Tabella TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305628"
---
# <a name="typelib-table"></a><span data-ttu-id="a1964-103">Tabella TypeLib</span><span class="sxs-lookup"><span data-stu-id="a1964-103">TypeLib Table</span></span>

<span data-ttu-id="a1964-104">La tabella TypeLib contiene le informazioni che devono essere inserite nella registrazione del registro di sistema delle librerie dei tipi.</span><span class="sxs-lookup"><span data-stu-id="a1964-104">The TypeLib table contains the information that needs to be placed in the registry registration of type libraries.</span></span>

<span data-ttu-id="a1964-105">La tabella TypeLib contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="a1964-105">The TypeLib table has the following columns.</span></span>



| <span data-ttu-id="a1964-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="a1964-106">Column</span></span>      | <span data-ttu-id="a1964-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1964-107">Type</span></span>                               | <span data-ttu-id="a1964-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="a1964-108">Key</span></span> | <span data-ttu-id="a1964-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="a1964-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="a1964-110">LibID</span><span class="sxs-lookup"><span data-stu-id="a1964-110">LibID</span></span>       | [<span data-ttu-id="a1964-111">GUID</span><span class="sxs-lookup"><span data-stu-id="a1964-111">GUID</span></span>](guid.md)                   | <span data-ttu-id="a1964-112">S</span><span class="sxs-lookup"><span data-stu-id="a1964-112">Y</span></span>   | <span data-ttu-id="a1964-113">N</span><span class="sxs-lookup"><span data-stu-id="a1964-113">N</span></span>        |
| <span data-ttu-id="a1964-114">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="a1964-114">Language</span></span>    | [<span data-ttu-id="a1964-115">Integer</span><span class="sxs-lookup"><span data-stu-id="a1964-115">Integer</span></span>](integer.md)             | <span data-ttu-id="a1964-116">S</span><span class="sxs-lookup"><span data-stu-id="a1964-116">Y</span></span>   | <span data-ttu-id="a1964-117">N</span><span class="sxs-lookup"><span data-stu-id="a1964-117">N</span></span>        |
| <span data-ttu-id="a1964-118">Componente\_</span><span class="sxs-lookup"><span data-stu-id="a1964-118">Component\_</span></span> | [<span data-ttu-id="a1964-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="a1964-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="a1964-120">S</span><span class="sxs-lookup"><span data-stu-id="a1964-120">Y</span></span>   | <span data-ttu-id="a1964-121">N</span><span class="sxs-lookup"><span data-stu-id="a1964-121">N</span></span>        |
| <span data-ttu-id="a1964-122">Versione</span><span class="sxs-lookup"><span data-stu-id="a1964-122">Version</span></span>     | [<span data-ttu-id="a1964-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="a1964-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="a1964-124">N</span><span class="sxs-lookup"><span data-stu-id="a1964-124">N</span></span>   | <span data-ttu-id="a1964-125">S</span><span class="sxs-lookup"><span data-stu-id="a1964-125">Y</span></span>        |
| <span data-ttu-id="a1964-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1964-126">Description</span></span> | [<span data-ttu-id="a1964-127">Text</span><span class="sxs-lookup"><span data-stu-id="a1964-127">Text</span></span>](text.md)                   | <span data-ttu-id="a1964-128">N</span><span class="sxs-lookup"><span data-stu-id="a1964-128">N</span></span>   | <span data-ttu-id="a1964-129">S</span><span class="sxs-lookup"><span data-stu-id="a1964-129">Y</span></span>        |
| <span data-ttu-id="a1964-130">Directory\_</span><span class="sxs-lookup"><span data-stu-id="a1964-130">Directory\_</span></span> | [<span data-ttu-id="a1964-131">Identificatore</span><span class="sxs-lookup"><span data-stu-id="a1964-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="a1964-132">N</span><span class="sxs-lookup"><span data-stu-id="a1964-132">N</span></span>   | <span data-ttu-id="a1964-133">S</span><span class="sxs-lookup"><span data-stu-id="a1964-133">Y</span></span>        |
| <span data-ttu-id="a1964-134">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="a1964-134">Feature\_</span></span>   | [<span data-ttu-id="a1964-135">Identificatore</span><span class="sxs-lookup"><span data-stu-id="a1964-135">Identifier</span></span>](identifier.md)       | <span data-ttu-id="a1964-136">N</span><span class="sxs-lookup"><span data-stu-id="a1964-136">N</span></span>   | <span data-ttu-id="a1964-137">N</span><span class="sxs-lookup"><span data-stu-id="a1964-137">N</span></span>        |
| <span data-ttu-id="a1964-138">Costo</span><span class="sxs-lookup"><span data-stu-id="a1964-138">Cost</span></span>        | [<span data-ttu-id="a1964-139">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="a1964-139">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="a1964-140">N</span><span class="sxs-lookup"><span data-stu-id="a1964-140">N</span></span>   | <span data-ttu-id="a1964-141">S</span><span class="sxs-lookup"><span data-stu-id="a1964-141">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a1964-142">Colonne</span><span class="sxs-lookup"><span data-stu-id="a1964-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a1964-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span><span class="sxs-lookup"><span data-stu-id="a1964-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span></span>
</dt> <dd>

<span data-ttu-id="a1964-144">GUID che identifica la libreria.</span><span class="sxs-lookup"><span data-stu-id="a1964-144">The GUID that identifies the library.</span></span>

</dd> <dt>

<span data-ttu-id="a1964-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio</span><span class="sxs-lookup"><span data-stu-id="a1964-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="a1964-146">Lingua della libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="a1964-146">The language of the type library.</span></span> <span data-ttu-id="a1964-147">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="a1964-147">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="a1964-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="a1964-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="a1964-149">Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1964-149">External key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a1964-150">Questa colonna identifica il componente che appartiene alla funzionalità \_ il cui file di chiave è la libreria dei tipi registrata.</span><span class="sxs-lookup"><span data-stu-id="a1964-150">This column identifies the component belonging to Feature\_ whose key file is the type library being registered.</span></span>

</dd> <dt>

<span data-ttu-id="a1964-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versione</span><span class="sxs-lookup"><span data-stu-id="a1964-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="a1964-152">Questa è la versione della libreria.</span><span class="sxs-lookup"><span data-stu-id="a1964-152">This is the version of the library.</span></span> <span data-ttu-id="a1964-153">Le versioni principale e secondaria vengono codificate nel valore integer a quattro byte.</span><span class="sxs-lookup"><span data-stu-id="a1964-153">The major and minor versions are encoded in the four byte integer value.</span></span> <span data-ttu-id="a1964-154">La versione secondaria si trova negli otto bit inferiori.</span><span class="sxs-lookup"><span data-stu-id="a1964-154">The minor version is in the lower eight bits.</span></span> <span data-ttu-id="a1964-155">La versione principale è la metà di sedici bit.</span><span class="sxs-lookup"><span data-stu-id="a1964-155">The major version is in the middle sixteen bits.</span></span>

</dd> <dt>

<span data-ttu-id="a1964-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1964-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="a1964-157">Descrizione localizzabile della libreria.</span><span class="sxs-lookup"><span data-stu-id="a1964-157">A localizable description of the library.</span></span>

</dd> <dt>

<span data-ttu-id="a1964-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span><span class="sxs-lookup"><span data-stu-id="a1964-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="a1964-159">Chiave esterna nella prima colonna della tabella di [directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1964-159">External key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="a1964-160">In questa colonna viene identificato il percorso della Guida per la libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="a1964-160">This column identifies the Help path for the type library.</span></span> <span data-ttu-id="a1964-161">Questa colonna viene ignorata durante la pubblicità.</span><span class="sxs-lookup"><span data-stu-id="a1964-161">This column is ignored during advertising.</span></span>

</dd> <dt>

<span data-ttu-id="a1964-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="a1964-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="a1964-163">Chiave esterna nella prima colonna della tabella delle [funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a1964-163">External key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="a1964-164">In questa colonna viene specificata la funzionalità che deve essere installata per rendere operativa la libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="a1964-164">This column specifies the feature that must be installed for the type library to be operational.</span></span>

</dd> <dt>

<span data-ttu-id="a1964-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costo</span><span class="sxs-lookup"><span data-stu-id="a1964-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="a1964-166">Costo associato alla registrazione della libreria dei tipi in byte.</span><span class="sxs-lookup"><span data-stu-id="a1964-166">The cost associated with the registration of the type library in bytes.</span></span> <span data-ttu-id="a1964-167">Deve essere un numero non negativo o null.</span><span class="sxs-lookup"><span data-stu-id="a1964-167">This must be a non-negative number or null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1964-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1964-168">Remarks</span></span>

<span data-ttu-id="a1964-169">Questa tabella viene definita quando viene eseguita l'azione [RegisterTypeLibraries](registertypelibraries-action.md) o [UnregisterTypeLibraries](unregistertypelibraries-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a1964-169">This table is referred to when the [RegisterTypeLibraries action](registertypelibraries-action.md) or the [UnregisterTypeLibraries action](unregistertypelibraries-action.md) is executed.</span></span>

<span data-ttu-id="a1964-170">Il programma di installazione scrive tutte le informazioni di registrazione della libreria dei tipi nel \_ \_ percorso del registro di sistema HKLM (hKey local machine).</span><span class="sxs-lookup"><span data-stu-id="a1964-170">The installer writes all type library registration information into the HKEY\_LOCAL\_MACHINE (HKLM) registry location.</span></span> <span data-ttu-id="a1964-171">Questo è il caso anche per le installazioni per utente.</span><span class="sxs-lookup"><span data-stu-id="a1964-171">This is the case even for per-user installations.</span></span> <span data-ttu-id="a1964-172">Non è possibile registrare le librerie di tipi in percorsi per utente (HKCU).</span><span class="sxs-lookup"><span data-stu-id="a1964-172">Type libraries cannot be registered in per-user locations (HKCU).</span></span>

<span data-ttu-id="a1964-173">Gli autori dei pacchetti di installazione si sconsigliano vivamente di utilizzare la tabella TypeLib.</span><span class="sxs-lookup"><span data-stu-id="a1964-173">Installation package authors are strongly advised against using the TypeLib table.</span></span> <span data-ttu-id="a1964-174">Devono invece registrare le librerie dei tipi usando la tabella [del registro di sistema](registry-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a1964-174">Instead, they should register type libraries by using the [Registry](registry-table.md) table.</span></span> <span data-ttu-id="a1964-175">I motivi per evitare la registrazione automatica includono:</span><span class="sxs-lookup"><span data-stu-id="a1964-175">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="a1964-176">Se un'installazione che utilizza la tabella TypeLib ha esito negativo ed è necessario eseguirne il rollback, è possibile che il rollback non ripristini il computer nello stesso stato esistente prima del rollback.</span><span class="sxs-lookup"><span data-stu-id="a1964-176">If an installation using the TypeLib table fails and must be rolled back, the rollback may not restore the computer to the same state that existed prior to the rollback.</span></span> <span data-ttu-id="a1964-177">Le librerie di tipi registrate prima del rollback potrebbero non essere registrate dopo il rollback.</span><span class="sxs-lookup"><span data-stu-id="a1964-177">Type libraries registered prior to rollback may not be registered after rollback.</span></span>

## <a name="validation"></a><span data-ttu-id="a1964-178">Convalida</span><span class="sxs-lookup"><span data-stu-id="a1964-178">Validation</span></span>

<dl>

[<span data-ttu-id="a1964-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="a1964-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a1964-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="a1964-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a1964-181">ICE19</span><span class="sxs-lookup"><span data-stu-id="a1964-181">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="a1964-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="a1964-182">ICE32</span></span>](ice32.md)  
</dl>

 

 



