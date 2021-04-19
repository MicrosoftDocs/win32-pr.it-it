---
description: L'azione RemoveEnvironmentStrings modifica i valori delle variabili di ambiente.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Azione RemoveEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319963"
---
# <a name="removeenvironmentstrings-action"></a><span data-ttu-id="5eab0-103">Azione RemoveEnvironmentStrings</span><span class="sxs-lookup"><span data-stu-id="5eab0-103">RemoveEnvironmentStrings Action</span></span>

<span data-ttu-id="5eab0-104">L'azione RemoveEnvironmentStrings modifica i valori delle variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="5eab0-104">The RemoveEnvironmentStrings action modifies the values of environment variables.</span></span>

<span data-ttu-id="5eab0-105">Si noti che le variabili di ambiente non cambiano per l'installazione in corso quando viene eseguita l'azione [WriteEnvironmentStrings](writeenvironmentstrings-action.md) o RemoveEnvironmentStrings.</span><span class="sxs-lookup"><span data-stu-id="5eab0-105">Note that environment variables do not change for the installation in progress when either the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) or RemoveEnvironmentStrings action are run.</span></span> <span data-ttu-id="5eab0-106">In Windows 2000 queste informazioni vengono archiviate nel registro di sistema e viene inviato un messaggio per notificare al sistema le modifiche apportate al completamento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="5eab0-106">On Windows 2000, this information is stored in the registry and a message is sent to notify the system of changes when the installation completes.</span></span> <span data-ttu-id="5eab0-107">Un nuovo processo o un altro processo che verifica la presenza di questi messaggi utilizzerà le nuove variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="5eab0-107">A new process, or another process that checks for these messages, will use the new environment variables.</span></span>

<span data-ttu-id="5eab0-108">Il programma di installazione esegue l' [azione WriteEnvironmentStrings](writeenvironmentstrings-action.md) solo durante l'installazione o la reinstallazione di un componente ed esegue l'azione RemoveEnvironmentStrings solo durante la rimozione di un componente.</span><span class="sxs-lookup"><span data-stu-id="5eab0-108">The installer runs the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) only during the installation or reinstallation of a component, and runs the RemoveEnvironmentStrings action only during the removal of a component.</span></span>

<span data-ttu-id="5eab0-109">I valori vengono scritti o rimossi in base alla selezione di azioni e modificatori primari.</span><span class="sxs-lookup"><span data-stu-id="5eab0-109">Values are written or removed based on the selection of primary actions and modifiers.</span></span> <span data-ttu-id="5eab0-110">Questi elementi sono descritti nella sezione messaggi ActionData seguenti.</span><span class="sxs-lookup"><span data-stu-id="5eab0-110">These are described in the following ActionData Messages section.</span></span> <span data-ttu-id="5eab0-111">Si noti che, a seconda dell'azione specificata, WriteEnvironmentStrings può rimuovere le variabili e RemoveEnvironmentStrings può aggiungerle in base alla creazione della [tabella dell'ambiente](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="5eab0-111">Note that depending upon the action specified, WriteEnvironmentStrings may remove variables, and RemoveEnvironmentStrings may add them based on the authoring of the [Environment table](environment-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5eab0-112">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="5eab0-112">Sequence Restrictions</span></span>

<span data-ttu-id="5eab0-113">L' [azione InstallValidate](installvalidate-action.md) deve essere eseguita prima dell'azione RemoveEnvironmentStrings.</span><span class="sxs-lookup"><span data-stu-id="5eab0-113">The [InstallValidate action](installvalidate-action.md) must be executed before the RemoveEnvironmentStrings action.</span></span> <span data-ttu-id="5eab0-114">Poiché l'azione WriteEnvironmentStrings e l'azione RemoveEnvironmentStrings non vengono mai applicate durante l'installazione o la rimozione di un componente, la relativa sequenza relativa non è limitata.</span><span class="sxs-lookup"><span data-stu-id="5eab0-114">Because the WriteEnvironmentStrings action and RemoveEnvironmentStrings action are never both applied during the installation or removal of a component, their relative sequence is not restricted.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5eab0-115">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="5eab0-115">ActionData Messages</span></span>



| <span data-ttu-id="5eab0-116">Campo</span><span class="sxs-lookup"><span data-stu-id="5eab0-116">Field</span></span> | <span data-ttu-id="5eab0-117">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="5eab0-117">Description of action data</span></span>                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eab0-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5eab0-118">\[1\]</span></span> | <span data-ttu-id="5eab0-119">Nome della variabile di ambiente da modificare.</span><span class="sxs-lookup"><span data-stu-id="5eab0-119">Name of the environment variable to modify.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="5eab0-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="5eab0-120">\[2\]</span></span> | <span data-ttu-id="5eab0-121">Valore della variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="5eab0-121">The environment variable value.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="5eab0-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="5eab0-122">\[3\]</span></span> | <span data-ttu-id="5eab0-123">Si tratta di un campo di flag di bit che specificano l'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5eab0-123">This is a field of bit flags that specify the action to be performed.</span></span> <span data-ttu-id="5eab0-124">Includere solo un bit per un'azione primaria.</span><span class="sxs-lookup"><span data-stu-id="5eab0-124">Include only one bit for a primary action.</span></span> <span data-ttu-id="5eab0-125">In questo campo può essere incluso più di un bit del modificatore.</span><span class="sxs-lookup"><span data-stu-id="5eab0-125">There may be more than one modifier bit included in this field.</span></span> <span data-ttu-id="5eab0-126">Vedere le seguenti descrizioni dei flag di bit.</span><span class="sxs-lookup"><span data-stu-id="5eab0-126">See the following bit flag descriptions.</span></span> |



 



| <span data-ttu-id="5eab0-127">Valore bit</span><span class="sxs-lookup"><span data-stu-id="5eab0-127">Bit value</span></span> | <span data-ttu-id="5eab0-128">Descrizione delle azioni primarie</span><span class="sxs-lookup"><span data-stu-id="5eab0-128">Description of primary actions</span></span>                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eab0-129">0x1</span><span class="sxs-lookup"><span data-stu-id="5eab0-129">0x1</span></span>       | <span data-ttu-id="5eab0-130">Ai posti.</span><span class="sxs-lookup"><span data-stu-id="5eab0-130">Set.</span></span> <span data-ttu-id="5eab0-131">Imposta il valore della variabile di ambiente in tutti i casi.</span><span class="sxs-lookup"><span data-stu-id="5eab0-131">Sets the value of the environment variable in all cases.</span></span><br/> <span data-ttu-id="5eab0-132">Se questo bit è combinato con un bit di modificatore Append o prefix, l'azione aggiunge il valore a qualsiasi valore esistente nella variabile.</span><span class="sxs-lookup"><span data-stu-id="5eab0-132">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/> |
| <span data-ttu-id="5eab0-133">0x2</span><span class="sxs-lookup"><span data-stu-id="5eab0-133">0x2</span></span>       | <span data-ttu-id="5eab0-134">Ai posti.</span><span class="sxs-lookup"><span data-stu-id="5eab0-134">Set.</span></span> <span data-ttu-id="5eab0-135">Imposta il valore se la variabile è assente.</span><span class="sxs-lookup"><span data-stu-id="5eab0-135">Sets the value if the variable is absent.</span></span><br/> <span data-ttu-id="5eab0-136">Se questo bit è combinato con un bit di modificatore Append o prefix, l'azione aggiunge il valore a qualsiasi valore esistente nella variabile.</span><span class="sxs-lookup"><span data-stu-id="5eab0-136">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/>                |
| <span data-ttu-id="5eab0-137">0x4</span><span class="sxs-lookup"><span data-stu-id="5eab0-137">0x4</span></span>       | <span data-ttu-id="5eab0-138">Rimuovi.</span><span class="sxs-lookup"><span data-stu-id="5eab0-138">Remove.</span></span> <span data-ttu-id="5eab0-139">Rimuove il valore dalla variabile.</span><span class="sxs-lookup"><span data-stu-id="5eab0-139">Removes the value from the variable.</span></span><br/> <span data-ttu-id="5eab0-140">Se questo bit è combinato con un bit di modificatore Append o prefix, il valore viene rimosso dalla stringa esistente, se il valore esiste.</span><span class="sxs-lookup"><span data-stu-id="5eab0-140">If this bit is combined with an Append or Prefix modifier bit, the value is removed from the existing string, if the value exists.</span></span><br/>               |



 



| <span data-ttu-id="5eab0-141">Valore bit</span><span class="sxs-lookup"><span data-stu-id="5eab0-141">Bit value</span></span>  | <span data-ttu-id="5eab0-142">Descrizione del modificatore</span><span class="sxs-lookup"><span data-stu-id="5eab0-142">Description of modifier</span></span>                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eab0-143">0x20000000</span><span class="sxs-lookup"><span data-stu-id="5eab0-143">0x20000000</span></span> | <span data-ttu-id="5eab0-144">Se questo bit è impostato, le azioni vengono applicate alle variabili di ambiente del computer.</span><span class="sxs-lookup"><span data-stu-id="5eab0-144">If this bit is set, actions are applied to the machine environment variables.</span></span><br/> <span data-ttu-id="5eab0-145">Se questo bit non è impostato, le azioni vengono applicate alle variabili di ambiente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5eab0-145">If this bit is not set, actions are applied to the user's environment variables.</span></span><br/> |
| <span data-ttu-id="5eab0-146">0x40000000</span><span class="sxs-lookup"><span data-stu-id="5eab0-146">0x40000000</span></span> | <span data-ttu-id="5eab0-147">Append.</span><span class="sxs-lookup"><span data-stu-id="5eab0-147">Append.</span></span> <span data-ttu-id="5eab0-148">Questo bit è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5eab0-148">This bit is optional.</span></span> <span data-ttu-id="5eab0-149">Non impostare i modificatori Append e prefix.</span><span class="sxs-lookup"><span data-stu-id="5eab0-149">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |
| <span data-ttu-id="5eab0-150">0x80000000</span><span class="sxs-lookup"><span data-stu-id="5eab0-150">0x80000000</span></span> | <span data-ttu-id="5eab0-151">Prefisso.</span><span class="sxs-lookup"><span data-stu-id="5eab0-151">Prefix.</span></span> <span data-ttu-id="5eab0-152">Questo bit è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5eab0-152">This bit is optional.</span></span> <span data-ttu-id="5eab0-153">Non impostare i modificatori Append e prefix.</span><span class="sxs-lookup"><span data-stu-id="5eab0-153">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |



 

 

 




