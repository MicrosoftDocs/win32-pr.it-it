---
description: La tabella RemoveRegistry contiene le informazioni del registro di sistema che l'applicazione deve eliminare dal registro di sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Tabella RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967736"
---
# <a name="removeregistry-table"></a><span data-ttu-id="447de-103">Tabella RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="447de-103">RemoveRegistry Table</span></span>

<span data-ttu-id="447de-104">La tabella RemoveRegistry contiene le informazioni del registro di sistema che l'applicazione deve eliminare dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="447de-104">The RemoveRegistry table contains the registry information the application needs to delete from the system registry.</span></span>

<span data-ttu-id="447de-105">La tabella RemoveRegistry include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="447de-105">The RemoveRegistry table has the following columns.</span></span>



| <span data-ttu-id="447de-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="447de-106">Column</span></span>         | <span data-ttu-id="447de-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="447de-107">Type</span></span>                         | <span data-ttu-id="447de-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="447de-108">Key</span></span> | <span data-ttu-id="447de-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="447de-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="447de-110">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="447de-110">RemoveRegistry</span></span> | [<span data-ttu-id="447de-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="447de-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="447de-112">S</span><span class="sxs-lookup"><span data-stu-id="447de-112">Y</span></span>   | <span data-ttu-id="447de-113">N</span><span class="sxs-lookup"><span data-stu-id="447de-113">N</span></span>        |
| <span data-ttu-id="447de-114">Radice</span><span class="sxs-lookup"><span data-stu-id="447de-114">Root</span></span>           | [<span data-ttu-id="447de-115">Integer</span><span class="sxs-lookup"><span data-stu-id="447de-115">Integer</span></span>](integer.md)       | <span data-ttu-id="447de-116">N</span><span class="sxs-lookup"><span data-stu-id="447de-116">N</span></span>   | <span data-ttu-id="447de-117">N</span><span class="sxs-lookup"><span data-stu-id="447de-117">N</span></span>        |
| <span data-ttu-id="447de-118">Chiave</span><span class="sxs-lookup"><span data-stu-id="447de-118">Key</span></span>            | [<span data-ttu-id="447de-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="447de-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="447de-120">N</span><span class="sxs-lookup"><span data-stu-id="447de-120">N</span></span>   | <span data-ttu-id="447de-121">N</span><span class="sxs-lookup"><span data-stu-id="447de-121">N</span></span>        |
| <span data-ttu-id="447de-122">Nome</span><span class="sxs-lookup"><span data-stu-id="447de-122">Name</span></span>           | [<span data-ttu-id="447de-123">Formattato</span><span class="sxs-lookup"><span data-stu-id="447de-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="447de-124">N</span><span class="sxs-lookup"><span data-stu-id="447de-124">N</span></span>   | <span data-ttu-id="447de-125">S</span><span class="sxs-lookup"><span data-stu-id="447de-125">Y</span></span>        |
| <span data-ttu-id="447de-126">Componente\_</span><span class="sxs-lookup"><span data-stu-id="447de-126">Component\_</span></span>    | [<span data-ttu-id="447de-127">Identificatore</span><span class="sxs-lookup"><span data-stu-id="447de-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="447de-128">N</span><span class="sxs-lookup"><span data-stu-id="447de-128">N</span></span>   | <span data-ttu-id="447de-129">N</span><span class="sxs-lookup"><span data-stu-id="447de-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="447de-130">Colonne</span><span class="sxs-lookup"><span data-stu-id="447de-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="447de-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="447de-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span></span>
</dt> <dd>

<span data-ttu-id="447de-132">Chiave per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="447de-132">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="447de-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Radice</span><span class="sxs-lookup"><span data-stu-id="447de-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="447de-134">Chiave radice predefinita per il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="447de-134">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="447de-135">Costante</span><span class="sxs-lookup"><span data-stu-id="447de-135">Constant</span></span>                          | <span data-ttu-id="447de-136">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="447de-136">Hexadecimal</span></span> | <span data-ttu-id="447de-137">Decimal</span><span class="sxs-lookup"><span data-stu-id="447de-137">Decimal</span></span> | <span data-ttu-id="447de-138">Chiave radice</span><span class="sxs-lookup"><span data-stu-id="447de-138">Root key</span></span>                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="447de-139">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="447de-139">(none)</span></span>                            | <span data-ttu-id="447de-140">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="447de-140">\- 0x001</span></span>    | <span data-ttu-id="447de-141">-1</span><span class="sxs-lookup"><span data-stu-id="447de-141">-1</span></span>      | <span data-ttu-id="447de-142">**HKEY \_ Il programma di installazione \_ dell'utente corrente** imposta questa chiave durante l'installazione per utente.</span><span class="sxs-lookup"><span data-stu-id="447de-142">**HKEY\_CURRENT\_USER** Installer sets this key while doing a per-user installation.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="447de-143">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="447de-143">(none)</span></span>                            | <span data-ttu-id="447de-144">-0x001</span><span class="sxs-lookup"><span data-stu-id="447de-144">-0x001</span></span>      | <span data-ttu-id="447de-145">-1</span><span class="sxs-lookup"><span data-stu-id="447de-145">-1</span></span>      | <span data-ttu-id="447de-146">**HKEY \_ Il programma di installazione del \_ computer locale** imposta questa chiave durante l'installazione di tutti gli utenti con [**ALLUSERS**](allusers.md) impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="447de-146">**HKEY\_LOCAL\_MACHINE** Installer sets this key while doing an all-users installation with [**ALLUSERS**](allusers.md) set to 1.</span></span><br/>                                                                       |
| <span data-ttu-id="447de-147">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="447de-147">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="447de-148">0x000</span><span class="sxs-lookup"><span data-stu-id="447de-148">0x000</span></span>       | <span data-ttu-id="447de-149">0</span><span class="sxs-lookup"><span data-stu-id="447de-149">0</span></span>       | <span data-ttu-id="447de-150">**HKEY \_ \_Radice classi** il programma di installazione rimuove il valore **da \\ HKCU Software \\ Classes** hive durante le installazioni nel [contesto di installazione](installation-context.md)per utente e per computer.</span><span class="sxs-lookup"><span data-stu-id="447de-150">**HKEY\_CLASSES\_ROOT** The installer removes the value from the **HKCU\\Software\\Classes** hive during installations in the per-user and per-machine [installation context](installation-context.md).</span></span><br/> |
| <span data-ttu-id="447de-151">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="447de-151">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="447de-152">0x001</span><span class="sxs-lookup"><span data-stu-id="447de-152">0x001</span></span>       | <span data-ttu-id="447de-153">1</span><span class="sxs-lookup"><span data-stu-id="447de-153">1</span></span>       | <span data-ttu-id="447de-154">**HKEY \_ \_ utente corrente**</span><span class="sxs-lookup"><span data-stu-id="447de-154">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="447de-155">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="447de-155">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="447de-156">0x002</span><span class="sxs-lookup"><span data-stu-id="447de-156">0x002</span></span>       | <span data-ttu-id="447de-157">2</span><span class="sxs-lookup"><span data-stu-id="447de-157">2</span></span>       | <span data-ttu-id="447de-158">**\_computer locale \_ HKEY**</span><span class="sxs-lookup"><span data-stu-id="447de-158">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="447de-159">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="447de-159">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="447de-160">0x003</span><span class="sxs-lookup"><span data-stu-id="447de-160">0x003</span></span>       | <span data-ttu-id="447de-161">3</span><span class="sxs-lookup"><span data-stu-id="447de-161">3</span></span>       | <span data-ttu-id="447de-162">**\_utenti HKEY**</span><span class="sxs-lookup"><span data-stu-id="447de-162">**HKEY\_USERS**</span></span>                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="447de-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave</span><span class="sxs-lookup"><span data-stu-id="447de-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="447de-164">Chiave localizzabile per il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="447de-164">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="447de-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="447de-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="447de-166">Nome del valore del registro di sistema localizzabile.</span><span class="sxs-lookup"><span data-stu-id="447de-166">The localizable registry value name.</span></span>

<span data-ttu-id="447de-167">La stringa seguente nella colonna Name ha un significato speciale.</span><span class="sxs-lookup"><span data-stu-id="447de-167">The following string in the Name column has special significance.</span></span>



| <span data-ttu-id="447de-168">string</span><span class="sxs-lookup"><span data-stu-id="447de-168">String</span></span> | <span data-ttu-id="447de-169">Significato</span><span class="sxs-lookup"><span data-stu-id="447de-169">Meaning</span></span>                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="447de-170">"-"</span><span class="sxs-lookup"><span data-stu-id="447de-170">"-"</span></span>    | <span data-ttu-id="447de-171">La chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi, quando viene installato il componente.</span><span class="sxs-lookup"><span data-stu-id="447de-171">The key is to be deleted, if present, with all of its values and subkeys, when the component is installed.</span></span> |



 

<span data-ttu-id="447de-172">Si noti che la [tabella del registro di sistema](registry-table.md) deve essere utilizzata per creare o rimuovere una chiave del registro di sistema quando il componente viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="447de-172">Note that the [Registry table](registry-table.md) should be used to create or remove a registry key when the component is removed.</span></span>

</dd> <dt>

<span data-ttu-id="447de-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="447de-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="447de-174">Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md) che fa riferimento al componente che controlla l'eliminazione del valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="447de-174">External key into the first column of the [Component table](component-table.md) referencing the component that controls the deletion of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="447de-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="447de-175">Remarks</span></span>

<span data-ttu-id="447de-176">Le informazioni del registro di sistema vengono eliminate dal registro di sistema quando il componente corrispondente è stato selezionato per l'installazione locale o per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="447de-176">The registry information is deleted from the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="447de-177">Questa tabella viene definita quando viene eseguita l' [azione RemoveRegistryValues](removeregistryvalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="447de-177">This table is referred to when the [RemoveRegistryValues action](removeregistryvalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="447de-178">Convalida</span><span class="sxs-lookup"><span data-stu-id="447de-178">Validation</span></span>

<dl>

[<span data-ttu-id="447de-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="447de-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="447de-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="447de-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="447de-181">ICE32</span><span class="sxs-lookup"><span data-stu-id="447de-181">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="447de-182">ICE46</span><span class="sxs-lookup"><span data-stu-id="447de-182">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="447de-183">ICE69</span><span class="sxs-lookup"><span data-stu-id="447de-183">ICE69</span></span>](ice69.md)  
</dl>

 

 




