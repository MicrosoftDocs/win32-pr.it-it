---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 5 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 32b10271-44b1-4c5d-9c8b-eed1b4cd31e2
title: Tipo di azione personalizzata 5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85460c9a41dca060ca2634c013999c2c340ddfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313357"
---
# <a name="custom-action-type-5"></a><span data-ttu-id="8cb00-103">Tipo di azione personalizzata 5</span><span class="sxs-lookup"><span data-stu-id="8cb00-103">Custom Action Type 5</span></span>

<span data-ttu-id="8cb00-104">Questa azione personalizzata è scritta in JScript, ad esempio ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="8cb00-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="8cb00-105">Windows Installer non supporta JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="8cb00-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="8cb00-106">Per ulteriori informazioni, vedere [script](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="8cb00-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="8cb00-107">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="8cb00-107">Source</span></span>

<span data-ttu-id="8cb00-108">Lo script viene generato da un flusso binario temporaneo.</span><span class="sxs-lookup"><span data-stu-id="8cb00-108">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="8cb00-109">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="8cb00-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="8cb00-110">La colonna di dati nella tabella binaria contiene i dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="8cb00-110">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="8cb00-111">Per ogni riga viene allocato un flusso separato.</span><span class="sxs-lookup"><span data-stu-id="8cb00-111">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="8cb00-112">I nuovi dati binari possono essere inseriti da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella.</span><span class="sxs-lookup"><span data-stu-id="8cb00-112">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="8cb00-113">Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato in base al tipo di azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="8cb00-113">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed according to the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="8cb00-114">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="8cb00-114">Type Value</span></span>

<span data-ttu-id="8cb00-115">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base dell'azione personalizzata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8cb00-115">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of 32-bit custom action.</span></span>



| <span data-ttu-id="8cb00-116">Costanti</span><span class="sxs-lookup"><span data-stu-id="8cb00-116">Constants</span></span>                                                              | <span data-ttu-id="8cb00-117">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="8cb00-117">Hexadecimal</span></span> | <span data-ttu-id="8cb00-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="8cb00-118">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="8cb00-119">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="8cb00-119">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="8cb00-120">0x05</span><span class="sxs-lookup"><span data-stu-id="8cb00-120">0x05</span></span>        | <span data-ttu-id="8cb00-121">5</span><span class="sxs-lookup"><span data-stu-id="8cb00-121">5</span></span>       |



 

<span data-ttu-id="8cb00-122">Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="8cb00-122">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="8cb00-123">Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="8cb00-123">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="8cb00-124">Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="8cb00-124">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="8cb00-125">Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="8cb00-125">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="8cb00-126">Costanti</span><span class="sxs-lookup"><span data-stu-id="8cb00-126">Constants</span></span>                                                                                                     | <span data-ttu-id="8cb00-127">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="8cb00-127">Hexadecimal</span></span> | <span data-ttu-id="8cb00-128">Decimal</span><span class="sxs-lookup"><span data-stu-id="8cb00-128">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="8cb00-129">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="8cb00-129">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="8cb00-130">0x0001005</span><span class="sxs-lookup"><span data-stu-id="8cb00-130">0x0001005</span></span>   | <span data-ttu-id="8cb00-131">4101</span><span class="sxs-lookup"><span data-stu-id="8cb00-131">4101</span></span>    |



 

## <a name="target"></a><span data-ttu-id="8cb00-132">Destinazione</span><span class="sxs-lookup"><span data-stu-id="8cb00-132">Target</span></span>

<span data-ttu-id="8cb00-133">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene una funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="8cb00-133">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="8cb00-134">L'elaborazione invia innanzitutto lo script per l'analisi e quindi chiama la funzione script facoltativa.</span><span class="sxs-lookup"><span data-stu-id="8cb00-134">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="8cb00-135">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="8cb00-135">Return Processing Options</span></span>

<span data-ttu-id="8cb00-136">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="8cb00-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="8cb00-137">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="8cb00-137">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="8cb00-138">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="8cb00-138">Execution Scheduling Options</span></span>

<span data-ttu-id="8cb00-139">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8cb00-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="8cb00-140">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="8cb00-140">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="8cb00-141">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="8cb00-141">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="8cb00-142">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="8cb00-142">In-Script Execution Options</span></span>

<span data-ttu-id="8cb00-143">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="8cb00-143">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="8cb00-144">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="8cb00-144">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="8cb00-145">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="8cb00-145">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="8cb00-146">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="8cb00-146">Return Values</span></span>

<span data-ttu-id="8cb00-147">Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in [valori restituiti di azioni personalizzate JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="8cb00-147">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cb00-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cb00-148">Remarks</span></span>

<span data-ttu-id="8cb00-149">Un'azione personalizzata scritta in JScript o VBScript richiede l'installazione dell' [**oggetto Session**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="8cb00-149">A custom action that is written in JScript or VBScript requires the installation of [**Session Object**](session-object.md).</span></span> <span data-ttu-id="8cb00-150">Il programma di installazione associa l'oggetto **sessione** allo script con la *sessione* del nome.</span><span class="sxs-lookup"><span data-stu-id="8cb00-150">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="8cb00-151">Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.</span><span class="sxs-lookup"><span data-stu-id="8cb00-151">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="8cb00-152">Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata dopo la tabella, utilizzando la chiave primaria come nome file (colonna nome per la tabella binaria), con un'estensione predefinita ". IBD".</span><span class="sxs-lookup"><span data-stu-id="8cb00-152">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="8cb00-153">Il nome deve usare il formato del nome file 8,3 Se il file system o il sistema di controllo della versione non supporta nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="8cb00-153">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="8cb00-154">Il file di archivio permanente sostituisce i dati del flusso con il nome file utilizzato, in modo che i dati possano essere individuati quando la tabella viene importata.</span><span class="sxs-lookup"><span data-stu-id="8cb00-154">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cb00-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cb00-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cb00-156">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="8cb00-156">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



