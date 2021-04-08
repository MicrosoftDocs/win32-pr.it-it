---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un'azione personalizzata di tipo 1 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Tipo di azione personalizzata 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058237"
---
# <a name="custom-action-type-1"></a><span data-ttu-id="c3a9a-103">Tipo di azione personalizzata 1</span><span class="sxs-lookup"><span data-stu-id="c3a9a-103">Custom Action Type 1</span></span>

<span data-ttu-id="c3a9a-104">Questa azione personalizzata chiama una libreria a collegamento dinamico (DLL) scritta in C o C++.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="c3a9a-105">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="c3a9a-105">Source</span></span>

<span data-ttu-id="c3a9a-106">La DLL viene generata da un flusso binario temporaneo.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-106">The DLL is generated from a temporary binary stream.</span></span> <span data-ttu-id="c3a9a-107">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3a9a-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="c3a9a-108">La colonna di dati nella tabella binaria contiene i dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="c3a9a-109">Per ogni riga viene allocato un flusso separato.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-109">A separate stream is allocated for each row.</span></span> <span data-ttu-id="c3a9a-110">I nuovi dati binari possono essere inseriti da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="c3a9a-111">Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato a seconda del tipo di azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="c3a9a-112">Valore tipo</span><span class="sxs-lookup"><span data-stu-id="c3a9a-112">Type Value</span></span>

<span data-ttu-id="c3a9a-113">Includere i seguenti bit di flag nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-113">Include the following flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="c3a9a-114">Costanti</span><span class="sxs-lookup"><span data-stu-id="c3a9a-114">Constants</span></span>                                                          | <span data-ttu-id="c3a9a-115">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="c3a9a-115">Hexadecimal</span></span> | <span data-ttu-id="c3a9a-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="c3a9a-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="c3a9a-117">**msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="c3a9a-117">**msidbCustomActionTypeDll** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="c3a9a-118">0x001</span><span class="sxs-lookup"><span data-stu-id="c3a9a-118">0x001</span></span>       | <span data-ttu-id="c3a9a-119">1</span><span class="sxs-lookup"><span data-stu-id="c3a9a-119">1</span></span>       |



 

## <a name="target"></a><span data-ttu-id="c3a9a-120">Destinazione</span><span class="sxs-lookup"><span data-stu-id="c3a9a-120">Target</span></span>

<span data-ttu-id="c3a9a-121">La DLL viene chiamata tramite il punto di ingresso denominato nel campo di destinazione della [tabella CustomAction](customaction-table.md), passando un solo argomento che rappresenta l'handle della sessione di installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-121">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="c3a9a-122">Il nome del punto di ingresso specificato nella tabella deve corrispondere a quello esportato dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-122">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="c3a9a-123">Si noti che se la funzione entry non è specificata da un oggetto. File DEF o con una specifica/EXPORT: linker, il nome può avere un carattere di sottolineatura e un @4 suffisso "".</span><span class="sxs-lookup"><span data-stu-id="c3a9a-123">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="c3a9a-124">La funzione chiamata deve specificare la \_ \_ convenzione di chiamata stdcall.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-124">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="c3a9a-125">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="c3a9a-125">Return Processing Options</span></span>

<span data-ttu-id="c3a9a-126">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="c3a9a-127">Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="c3a9a-127">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="c3a9a-128">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="c3a9a-128">Execution Scheduling Options</span></span>

<span data-ttu-id="c3a9a-129">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-129">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="c3a9a-130">Queste opzioni controllano la multipla esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-130">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="c3a9a-131">Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="c3a9a-131">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="c3a9a-132">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="c3a9a-132">In-Script Execution Options</span></span>

<span data-ttu-id="c3a9a-133">Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="c3a9a-134">Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-134">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="c3a9a-135">Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="c3a9a-135">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="c3a9a-136">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="c3a9a-136">Return Values</span></span>

<span data-ttu-id="c3a9a-137">Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c3a9a-137">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a9a-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3a9a-138">Remarks</span></span>

<span data-ttu-id="c3a9a-139">Un'azione personalizzata che chiama una libreria a collegamento dinamico (DLL) richiede un handle per la sessione di installazione.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-139">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="c3a9a-140">Se si tratta anche di un'azione personalizzata di esecuzione posticipata, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-140">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="c3a9a-141">Per informazioni sul modo in cui un'azione personalizzata di questo tipo può ottenere informazioni sul contesto, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c3a9a-141">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="c3a9a-142">Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata dopo la tabella, utilizzando la chiave primaria come nome file (colonna nome per la tabella binaria), con un'estensione predefinita ". IBD".</span><span class="sxs-lookup"><span data-stu-id="c3a9a-142">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="c3a9a-143">Il nome deve usare il formato 8,3 Se il sistema di controllo della versione o file system non supporta nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-143">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="c3a9a-144">Il file di archivio permanente sostituisce i dati del flusso con il nome file utilizzato, in modo che i dati possano essere individuati quando la tabella viene importata.</span><span class="sxs-lookup"><span data-stu-id="c3a9a-144">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3a9a-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3a9a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3a9a-146">\_Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="c3a9a-146">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c3a9a-147">Librerie a collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="c3a9a-147">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> <dt>

[<span data-ttu-id="c3a9a-148">Recupero delle informazioni di contesto per le azioni personalizzate di esecuzione posticipata</span><span class="sxs-lookup"><span data-stu-id="c3a9a-148">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



