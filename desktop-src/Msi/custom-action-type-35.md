---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 35 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Tipo di azione personalizzata 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318287"
---
# <a name="custom-action-type-35"></a><span data-ttu-id="950d7-103">Tipo di azione personalizzata 35</span><span class="sxs-lookup"><span data-stu-id="950d7-103">Custom Action Type 35</span></span>

<span data-ttu-id="950d7-104">Questa azione personalizzata imposta la directory di installazione da una stringa di testo formattata.</span><span class="sxs-lookup"><span data-stu-id="950d7-104">This custom action sets the install directory from a formatted text string.</span></span> <span data-ttu-id="950d7-105">Per ulteriori informazioni, vedere [modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)</span><span class="sxs-lookup"><span data-stu-id="950d7-105">For more information, see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="source"></a><span data-ttu-id="950d7-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="950d7-106">Source</span></span>

<span data-ttu-id="950d7-107">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="950d7-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Directory table](directory-table.md).</span></span> <span data-ttu-id="950d7-108">La directory designata viene impostata dalla stringa formattata nel campo di destinazione usando [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span><span class="sxs-lookup"><span data-stu-id="950d7-108">The designated directory is set by the formatted string in the Target field using [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span></span> <span data-ttu-id="950d7-109">In questo modo, il percorso di destinazione e la proprietà associata vengono impostati sul valore espanso della stringa di testo formattata nel campo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="950d7-109">This sets the target path and associated property to the expanded value of the formatted text string in the Target field.</span></span> <span data-ttu-id="950d7-110">Non tentare di modificare il percorso di una directory di destinazione durante un' [installazione di manutenzione](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="950d7-110">Do not attempt to change the location of a target directory during a [maintenance installation](maintenance-installation.md).</span></span> <span data-ttu-id="950d7-111">Non tentare di modificare il percorso della directory di destinazione se alcuni componenti che usano tale percorso sono già installati per qualsiasi utente.</span><span class="sxs-lookup"><span data-stu-id="950d7-111">Do not attempt to change the target directory path if some components using that path are already installed for any user.</span></span>

## <a name="type-value"></a><span data-ttu-id="950d7-112">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="950d7-112">Type Value</span></span>

<span data-ttu-id="950d7-113">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="950d7-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="950d7-114">Costanti</span><span class="sxs-lookup"><span data-stu-id="950d7-114">Constants</span></span>                                                              | <span data-ttu-id="950d7-115">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="950d7-115">Hexadecimal</span></span> | <span data-ttu-id="950d7-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="950d7-116">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="950d7-117">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="950d7-117">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="950d7-118">0x023</span><span class="sxs-lookup"><span data-stu-id="950d7-118">0x023</span></span>       | <span data-ttu-id="950d7-119">35</span><span class="sxs-lookup"><span data-stu-id="950d7-119">35</span></span>      |



 

## <a name="target"></a><span data-ttu-id="950d7-120">Destinazione</span><span class="sxs-lookup"><span data-stu-id="950d7-120">Target</span></span>

<span data-ttu-id="950d7-121">La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata utilizzando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori dei campi numerici).</span><span class="sxs-lookup"><span data-stu-id="950d7-121">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="950d7-122">I parametri da sostituire sono racchiusi tra parentesi quadre \[ ... \] e possono essere proprietà, variabili di ambiente (% prefix), percorsi di file ( \# prefisso) o percorsi di directory dei componenti ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="950d7-122">Parameters to be replaced are enclosed in square brackets \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="950d7-123">Si noti che i percorsi di directory terminano sempre con un separatore di directory.</span><span class="sxs-lookup"><span data-stu-id="950d7-123">Note that directory paths always end with a directory separator.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="950d7-124">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="950d7-124">Return Processing Options</span></span>

<span data-ttu-id="950d7-125">L'azione personalizzata non usa queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="950d7-125">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="950d7-126">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="950d7-126">Execution Scheduling Options</span></span>

<span data-ttu-id="950d7-127">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="950d7-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="950d7-128">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="950d7-128">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="950d7-129">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="950d7-129">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="950d7-130">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="950d7-130">In-Script Execution Options</span></span>

<span data-ttu-id="950d7-131">L'azione personalizzata non usa queste opzioni.</span><span class="sxs-lookup"><span data-stu-id="950d7-131">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="950d7-132">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="950d7-132">Return Values</span></span>

<span data-ttu-id="950d7-133">Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="950d7-133">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="950d7-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="950d7-134">Remarks</span></span>

<span data-ttu-id="950d7-135">Se si imposta una [proprietà privata](private-properties.md) nella sequenza dell'interfaccia utente creando un'azione personalizzata in una delle tabelle di sequenza dell'interfaccia utente, tale proprietà non viene impostata nella sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="950d7-135">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="950d7-136">Per impostare la proprietà nella sequenza di esecuzione, è inoltre necessario inserire un'azione personalizzata in una tabella della sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="950d7-136">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="950d7-137">In alternativa, è possibile rendere la proprietà una [proprietà pubblica](public-properties.md) e includerla nella [**proprietà SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="950d7-137">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="950d7-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="950d7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="950d7-139">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="950d7-139">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="950d7-140">Azioni personalizzate del testo formattato</span><span class="sxs-lookup"><span data-stu-id="950d7-140">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



