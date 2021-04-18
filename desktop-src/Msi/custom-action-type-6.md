---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un'azione personalizzata di tipo 6 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Tipo di azione personalizzata 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314299"
---
# <a name="custom-action-type-6"></a><span data-ttu-id="4662d-103">Tipo di azione personalizzata 6</span><span class="sxs-lookup"><span data-stu-id="4662d-103">Custom Action Type 6</span></span>

<span data-ttu-id="4662d-104">Questa azione personalizzata è scritta in VBScript.</span><span class="sxs-lookup"><span data-stu-id="4662d-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="4662d-105">Per ulteriori informazioni, vedere [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="4662d-105">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="4662d-106">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="4662d-106">Source</span></span>

<span data-ttu-id="4662d-107">Lo script viene generato da un flusso binario temporaneo.</span><span class="sxs-lookup"><span data-stu-id="4662d-107">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="4662d-108">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="4662d-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="4662d-109">La colonna di dati nella tabella binaria contiene i dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="4662d-109">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="4662d-110">Per ogni riga viene allocato un flusso separato.</span><span class="sxs-lookup"><span data-stu-id="4662d-110">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="4662d-111">I nuovi dati binari possono essere inseriti da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella.</span><span class="sxs-lookup"><span data-stu-id="4662d-111">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="4662d-112">Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato a seconda del tipo di azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4662d-112">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="4662d-113">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="4662d-113">Type Value</span></span>

<span data-ttu-id="4662d-114">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4662d-114">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="4662d-115">Costanti</span><span class="sxs-lookup"><span data-stu-id="4662d-115">Constants</span></span>                                                               | <span data-ttu-id="4662d-116">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="4662d-116">Hexadecimal</span></span> | <span data-ttu-id="4662d-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="4662d-117">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="4662d-118">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="4662d-118">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="4662d-119">0x006</span><span class="sxs-lookup"><span data-stu-id="4662d-119">0x006</span></span>       | <span data-ttu-id="4662d-120">6</span><span class="sxs-lookup"><span data-stu-id="4662d-120">6</span></span>       |



 

<span data-ttu-id="4662d-121">Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4662d-121">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="4662d-122">Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="4662d-122">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="4662d-123">Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4662d-123">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="4662d-124">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4662d-124">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="4662d-125">Costanti</span><span class="sxs-lookup"><span data-stu-id="4662d-125">Constants</span></span>                                                                                                      | <span data-ttu-id="4662d-126">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="4662d-126">Hexadecimal</span></span> | <span data-ttu-id="4662d-127">Decimal</span><span class="sxs-lookup"><span data-stu-id="4662d-127">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="4662d-128">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="4662d-128">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="4662d-129">0x0001006</span><span class="sxs-lookup"><span data-stu-id="4662d-129">0x0001006</span></span>   | <span data-ttu-id="4662d-130">4102</span><span class="sxs-lookup"><span data-stu-id="4662d-130">4102</span></span>    |



 

## <a name="target"></a><span data-ttu-id="4662d-131">Destinazione</span><span class="sxs-lookup"><span data-stu-id="4662d-131">Target</span></span>

<span data-ttu-id="4662d-132">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene una funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="4662d-132">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="4662d-133">L'elaborazione invia innanzitutto lo script per l'analisi e quindi chiama la funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="4662d-133">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="4662d-134">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="4662d-134">Return Processing Options</span></span>

<span data-ttu-id="4662d-135">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="4662d-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="4662d-136">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="4662d-136">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="4662d-137">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="4662d-137">Execution Scheduling Options</span></span>

<span data-ttu-id="4662d-138">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4662d-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="4662d-139">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="4662d-139">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="4662d-140">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="4662d-140">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="4662d-141">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="4662d-141">In-Script Execution Options</span></span>

<span data-ttu-id="4662d-142">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="4662d-142">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="4662d-143">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="4662d-143">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="4662d-144">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="4662d-144">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="4662d-145">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="4662d-145">Return Values</span></span>

<span data-ttu-id="4662d-146">Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in [valori restituiti di azioni personalizzate JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4662d-146">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4662d-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="4662d-147">Remarks</span></span>

<span data-ttu-id="4662d-148">Un'azione personalizzata scritta in JScript o VBScript richiede l'installazione dell' [**oggetto Session**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="4662d-148">A custom action that is written in JScript or VBScript requires the installation of the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="4662d-149">Il programma di installazione associa l'oggetto **sessione** allo script con la *sessione* del nome.</span><span class="sxs-lookup"><span data-stu-id="4662d-149">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="4662d-150">Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.</span><span class="sxs-lookup"><span data-stu-id="4662d-150">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="4662d-151">Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata dopo la tabella, utilizzando la chiave primaria come nome file (colonna nome per la tabella binaria), con un'estensione predefinita ". IBD".</span><span class="sxs-lookup"><span data-stu-id="4662d-151">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="4662d-152">Il nome deve usare il formato del nome file 8,3 Se il file system o il sistema di controllo della versione non supporta nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="4662d-152">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="4662d-153">Il file di archivio permanente sostituisce i dati del flusso con il nome file utilizzato, in modo che i dati possano essere individuati quando la tabella viene importata.</span><span class="sxs-lookup"><span data-stu-id="4662d-153">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4662d-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4662d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4662d-155">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="4662d-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



