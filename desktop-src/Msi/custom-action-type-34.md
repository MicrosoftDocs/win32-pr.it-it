---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 34 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Tipo di azione personalizzata 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315475"
---
# <a name="custom-action-type-34"></a><span data-ttu-id="ea153-103">Tipo di azione personalizzata 34</span><span class="sxs-lookup"><span data-stu-id="ea153-103">Custom Action Type 34</span></span>

<span data-ttu-id="ea153-104">Questa azione personalizzata chiama un eseguibile avviato con una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ea153-104">This custom action calls an executable launched with a command line.</span></span> <span data-ttu-id="ea153-105">Per ulteriori informazioni, vedere [file eseguibili](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="ea153-105">For more information, see [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="ea153-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="ea153-106">Source</span></span>

<span data-ttu-id="ea153-107">Il file eseguibile viene generato da un file.</span><span class="sxs-lookup"><span data-stu-id="ea153-107">The executable is generated from a file.</span></span> <span data-ttu-id="ea153-108">Il campo di origine della tabella [CustomAction](customaction-table.md) contiene una chiave nella tabella [directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ea153-108">The Source field of the [CustomAction](customaction-table.md) table contains a key into the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="ea153-109">La voce della tabella di directory a cui viene fatto riferimento viene usata per risolvere il percorso completo di una directory di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ea153-109">The referenced Directory table entry is used to resolve the full path to a working directory.</span></span> <span data-ttu-id="ea153-110">Non è necessario che sia il percorso della directory che contiene il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ea153-110">This is not required to be the path to the directory containing the executable.</span></span>

## <a name="type-value"></a><span data-ttu-id="ea153-111">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="ea153-111">Type Value</span></span>

<span data-ttu-id="ea153-112">Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="ea153-112">Include the following value in the Type column of the [CustomAction](customaction-table.md) table to specify the basic numeric type.</span></span>



| <span data-ttu-id="ea153-113">Costanti</span><span class="sxs-lookup"><span data-stu-id="ea153-113">Constants</span></span>                                                         | <span data-ttu-id="ea153-114">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="ea153-114">Hexadecimal</span></span> | <span data-ttu-id="ea153-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="ea153-115">Decimal</span></span> |
|-------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="ea153-116">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="ea153-116">**msidbCustomActionTypeExe** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="ea153-117">0x022</span><span class="sxs-lookup"><span data-stu-id="ea153-117">0x022</span></span>       | <span data-ttu-id="ea153-118">34</span><span class="sxs-lookup"><span data-stu-id="ea153-118">34</span></span>      |



 

## <a name="target"></a><span data-ttu-id="ea153-119">Destinazione</span><span class="sxs-lookup"><span data-stu-id="ea153-119">Target</span></span>

<span data-ttu-id="ea153-120">La colonna di destinazione della tabella [CustomAction](customaction-table.md) contiene il percorso completo e il nome del file eseguibile seguito da argomenti facoltativi per l'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ea153-120">The Target column of the [CustomAction](customaction-table.md) table contains the full path and name of the executable file followed by optional arguments to the executable.</span></span> <span data-ttu-id="ea153-121">Il percorso completo e il nome del file eseguibile sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="ea153-121">The full path and name to the executable file is required.</span></span> <span data-ttu-id="ea153-122">Le virgolette devono essere utilizzate per i nomi di file o i percorsi lunghi.</span><span class="sxs-lookup"><span data-stu-id="ea153-122">Quotation marks must be used around long file names or paths.</span></span> <span data-ttu-id="ea153-123">Il valore viene trattato come testo [formattato](formatted.md) e può contenere riferimenti a proprietà, file, directory o altri attributi di testo formattato.</span><span class="sxs-lookup"><span data-stu-id="ea153-123">The value is treated as [formatted](formatted.md) text and may contain references to properties, files, directories, or other formatted text attributes.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="ea153-124">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="ea153-124">Return Processing Options</span></span>

<span data-ttu-id="ea153-125">Includere i bit di flag facoltativi nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="ea153-125">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify return processing options.</span></span> <span data-ttu-id="ea153-126">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="ea153-126">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="ea153-127">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="ea153-127">Execution Scheduling Options</span></span>

<span data-ttu-id="ea153-128">Includere i bit di flag facoltativi nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ea153-128">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify execution scheduling options.</span></span> <span data-ttu-id="ea153-129">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ea153-129">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="ea153-130">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="ea153-130">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="ea153-131">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="ea153-131">In-Script Execution Options</span></span>

<span data-ttu-id="ea153-132">Includere i bit di flag facoltativi nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="ea153-132">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify an in-script execution option.</span></span> <span data-ttu-id="ea153-133">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="ea153-133">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="ea153-134">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="ea153-134">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="ea153-135">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="ea153-135">Return Values</span></span>

<span data-ttu-id="ea153-136">Per l'esito positivo, le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="ea153-136">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="ea153-137">Il programma di installazione interpreta qualsiasi altro valore restituito come errore.</span><span class="sxs-lookup"><span data-stu-id="ea153-137">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="ea153-138">Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della tabella [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ea153-138">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction](customaction-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea153-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea153-139">Remarks</span></span>

<span data-ttu-id="ea153-140">Un'azione personalizzata che avvia un file eseguibile accetta una riga di comando, che in genere contiene proprietà designate dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="ea153-140">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="ea153-141">Se si tratta anche di un' [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md), il programma di installazione utilizza [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) per creare il processo quando viene richiamata l'azione personalizzata dallo script di installazione.</span><span class="sxs-lookup"><span data-stu-id="ea153-141">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea153-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea153-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea153-143">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="ea153-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 
