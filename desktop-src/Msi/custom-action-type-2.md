---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzata 2 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Tipo di azione personalizzata 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315476"
---
# <a name="custom-action-type-2"></a><span data-ttu-id="a8d80-103">Tipo di azione personalizzata 2</span><span class="sxs-lookup"><span data-stu-id="a8d80-103">Custom Action Type 2</span></span>

<span data-ttu-id="a8d80-104">Questa azione personalizzata chiama un eseguibile avviato con una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="a8d80-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="a8d80-105">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="a8d80-105">Source</span></span>

<span data-ttu-id="a8d80-106">Il file eseguibile viene generato da un flusso binario temporaneo.</span><span class="sxs-lookup"><span data-stu-id="a8d80-106">The executable is generated from a temporary binary stream.</span></span> <span data-ttu-id="a8d80-107">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8d80-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="a8d80-108">La colonna di dati nella tabella binaria contiene i dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="a8d80-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="a8d80-109">Per ogni riga viene allocato un flusso separato.</span><span class="sxs-lookup"><span data-stu-id="a8d80-109">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="a8d80-110">I nuovi dati binari possono essere inseriti da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella.</span><span class="sxs-lookup"><span data-stu-id="a8d80-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="a8d80-111">Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato a seconda del tipo di azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a8d80-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="a8d80-112">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="a8d80-112">Type Value</span></span>

<span data-ttu-id="a8d80-113">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="a8d80-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="a8d80-114">Costanti</span><span class="sxs-lookup"><span data-stu-id="a8d80-114">Constants</span></span>                                                          | <span data-ttu-id="a8d80-115">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="a8d80-115">Hexadecimal</span></span> | <span data-ttu-id="a8d80-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="a8d80-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="a8d80-117">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="a8d80-117">**msidbCustomActionTypeExe** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="a8d80-118">0x002</span><span class="sxs-lookup"><span data-stu-id="a8d80-118">0x002</span></span>       | <span data-ttu-id="a8d80-119">2</span><span class="sxs-lookup"><span data-stu-id="a8d80-119">2</span></span>       |



 

## <a name="target"></a><span data-ttu-id="a8d80-120">Destinazione</span><span class="sxs-lookup"><span data-stu-id="a8d80-120">Target</span></span>

<span data-ttu-id="a8d80-121">La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene la stringa della riga di comando per il file eseguibile denominato nella colonna di origine.</span><span class="sxs-lookup"><span data-stu-id="a8d80-121">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable named in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="a8d80-122">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="a8d80-122">Return Processing Options</span></span>

<span data-ttu-id="a8d80-123">Includere i bit di flag facoltativi nella colonna Type della tabella CustomAction per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="a8d80-123">Include optional flag bits in the Type column of the CustomAction table to specify return processing options.</span></span> <span data-ttu-id="a8d80-124">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="a8d80-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="a8d80-125">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="a8d80-125">Execution Scheduling Options</span></span>

<span data-ttu-id="a8d80-126">Includere i bit di flag facoltativi nella colonna Type della tabella CustomAction per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a8d80-126">Include optional flag bits in the Type column of the CustomAction table to specify execution scheduling options.</span></span> <span data-ttu-id="a8d80-127">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a8d80-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="a8d80-128">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="a8d80-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="a8d80-129">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="a8d80-129">In-Script Execution Options</span></span>

<span data-ttu-id="a8d80-130">Includere i bit di flag facoltativi nella colonna Type della tabella CustomAction per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="a8d80-130">Include optional flag bits in the Type column of the CustomAction table to specify an in-script execution option.</span></span> <span data-ttu-id="a8d80-131">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="a8d80-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="a8d80-132">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="a8d80-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="a8d80-133">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="a8d80-133">Return Values</span></span>

<span data-ttu-id="a8d80-134">Per l'esito positivo, le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="a8d80-134">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="a8d80-135">Il programma di installazione interpreta qualsiasi altro valore restituito come errore.</span><span class="sxs-lookup"><span data-stu-id="a8d80-135">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="a8d80-136">Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="a8d80-136">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8d80-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8d80-137">Remarks</span></span>

<span data-ttu-id="a8d80-138">Un'azione personalizzata che avvia un file eseguibile accetta una riga di comando, che in genere contiene proprietà designate dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="a8d80-138">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="a8d80-139">Se si tratta anche di un' [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md), il programma di installazione utilizza [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) per creare il processo quando viene richiamata l'azione personalizzata dallo script di installazione.</span><span class="sxs-lookup"><span data-stu-id="a8d80-139">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="a8d80-140">Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata dopo la tabella, utilizzando la chiave primaria come nome file (colonna nome per la tabella binaria), con un'estensione predefinita ". IBD".</span><span class="sxs-lookup"><span data-stu-id="a8d80-140">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="a8d80-141">Il nome deve usare il formato 8,3 Se il sistema di controllo della versione o file system non supporta nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="a8d80-141">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="a8d80-142">Il file di archivio permanente sostituisce i dati del flusso con il nome file utilizzato, in modo che i dati possano essere individuati quando la tabella viene importata.</span><span class="sxs-lookup"><span data-stu-id="a8d80-142">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8d80-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8d80-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8d80-144">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="a8d80-144">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="a8d80-145">File eseguibili</span><span class="sxs-lookup"><span data-stu-id="a8d80-145">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
