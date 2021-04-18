---
description: Azioni personalizzate scritte in JScript o Visual Basic, Scripting Edition (VBScript) può chiamare una funzione facoltativa. Queste funzioni devono restituire uno dei valori mostrati nella tabella seguente.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valori restituiti di azioni personalizzate JScript e VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309463"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a><span data-ttu-id="f093d-104">Valori restituiti di azioni personalizzate JScript e VBScript</span><span class="sxs-lookup"><span data-stu-id="f093d-104">Return Values of JScript and VBScript Custom Actions</span></span>

<span data-ttu-id="f093d-105">Azioni personalizzate scritte in JScript o Visual Basic, Scripting Edition (VBScript) può chiamare una funzione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="f093d-105">Custom actions written in JScript or Visual Basic, Scripting Edition (VBScript) can call an optional function.</span></span> <span data-ttu-id="f093d-106">Queste funzioni devono restituire uno dei valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f093d-106">These functions must return one of the values shown in the following table.</span></span>



| <span data-ttu-id="f093d-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f093d-107">Return value</span></span>              | <span data-ttu-id="f093d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="f093d-108">Value</span></span>        | <span data-ttu-id="f093d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f093d-109">Description</span></span>                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f093d-110">msiDoActionStatusNoAction</span><span class="sxs-lookup"><span data-stu-id="f093d-110">msiDoActionStatusNoAction</span></span> | <span data-ttu-id="f093d-111">0</span><span class="sxs-lookup"><span data-stu-id="f093d-111">0</span></span>            | <span data-ttu-id="f093d-112">L'azione non è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="f093d-112">Action not executed.</span></span>                                                                                       |
| <span data-ttu-id="f093d-113">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="f093d-113">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="f093d-114">IDOK = 1</span><span class="sxs-lookup"><span data-stu-id="f093d-114">IDOK = 1</span></span>     | <span data-ttu-id="f093d-115">L'azione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="f093d-115">Action completed successfully.</span></span>                                                                             |
| <span data-ttu-id="f093d-116">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="f093d-116">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="f093d-117">IDCANCEL = 2</span><span class="sxs-lookup"><span data-stu-id="f093d-117">IDCANCEL = 2</span></span> | <span data-ttu-id="f093d-118">Terminazione prematura dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f093d-118">Premature termination by user.</span></span>                                                                             |
| <span data-ttu-id="f093d-119">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="f093d-119">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="f093d-120">IDABORT = 3</span><span class="sxs-lookup"><span data-stu-id="f093d-120">IDABORT = 3</span></span>  | <span data-ttu-id="f093d-121">Errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="f093d-121">Unrecoverable error.</span></span> <span data-ttu-id="f093d-122">Restituito se si verifica un errore durante l'analisi o l'esecuzione di JScript o VBScript.</span><span class="sxs-lookup"><span data-stu-id="f093d-122">Returned if there is an error during parsing or execution of the JScript or VBScript.</span></span> |
| <span data-ttu-id="f093d-123">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="f093d-123">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="f093d-124">IDRETRY = 4</span><span class="sxs-lookup"><span data-stu-id="f093d-124">IDRETRY = 4</span></span>  | <span data-ttu-id="f093d-125">Sequenza sospesa da riprendere in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="f093d-125">Suspended sequence to be resumed later.</span></span>                                                                    |
| <span data-ttu-id="f093d-126">msiDoActionStatusFinished</span><span class="sxs-lookup"><span data-stu-id="f093d-126">msiDoActionStatusFinished</span></span> | <span data-ttu-id="f093d-127">IDIGNORE = 5</span><span class="sxs-lookup"><span data-stu-id="f093d-127">IDIGNORE = 5</span></span> | <span data-ttu-id="f093d-128">Ignora le azioni rimanenti.</span><span class="sxs-lookup"><span data-stu-id="f093d-128">Skip remaining actions.</span></span> <span data-ttu-id="f093d-129">Non è un errore.</span><span class="sxs-lookup"><span data-stu-id="f093d-129">Not an error.</span></span>                                                                      |



 

<span data-ttu-id="f093d-130">Si noti che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log.</span><span class="sxs-lookup"><span data-stu-id="f093d-130">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="f093d-131">Se, ad esempio, il valore restituito dell'azione viene visualizzato come 1 (uno) nel file di log, significa che l'azione ha restituito msiDoActionStatusSuccess.</span><span class="sxs-lookup"><span data-stu-id="f093d-131">For example, if the action return value appears as 1 (one) in the log file, this means that the action returned msiDoActionStatusSuccess.</span></span> <span data-ttu-id="f093d-132">Per ulteriori informazioni su questa traduzione, vedere [registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f093d-132">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="f093d-133">Per restituire un valore diverso da esito positivo da un'azione personalizzata script, è necessario utilizzare una destinazione di funzione per l'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f093d-133">To return a value other than success from a script custom action, you must use a function target for the custom action.</span></span> <span data-ttu-id="f093d-134">La funzione di destinazione viene specificata nella colonna di destinazione della [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="f093d-134">The target function is specified in the Target column of the [CustomAction Table](customaction-table.md).</span></span>

<span data-ttu-id="f093d-135">Nell'esempio di script seguente viene illustrato come restituire l'esito positivo o negativo di un'azione personalizzata VBScript.</span><span class="sxs-lookup"><span data-stu-id="f093d-135">The following script example shows you how to return success or failure from a VBScript custom action.</span></span>


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



<span data-ttu-id="f093d-136">Se questo VBScript era incorporato nella [tabella binaria](binary-table.md) del pacchetto di installazione come MyCA.vbs, la voce della [tabella CustomAction](customaction-table.md) per lo script sarà la seguente:</span><span class="sxs-lookup"><span data-stu-id="f093d-136">If this VBScript were embedded in the [Binary table](binary-table.md) of the installation package as MyCA.vbs, the [CustomAction Table](customaction-table.md) entry for the script would be the following:</span></span>



| <span data-ttu-id="f093d-137">Azione</span><span class="sxs-lookup"><span data-stu-id="f093d-137">Action</span></span>         | <span data-ttu-id="f093d-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="f093d-138">Type</span></span> | <span data-ttu-id="f093d-139">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="f093d-139">Source</span></span>   | <span data-ttu-id="f093d-140">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f093d-140">Target</span></span>       |
|----------------|------|----------|--------------|
| <span data-ttu-id="f093d-141">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="f093d-141">MyCustomAction</span></span> | <span data-ttu-id="f093d-142">6</span><span class="sxs-lookup"><span data-stu-id="f093d-142">6</span></span>    | <span data-ttu-id="f093d-143">MyCA.vbs</span><span class="sxs-lookup"><span data-stu-id="f093d-143">MyCA.vbs</span></span> | <span data-ttu-id="f093d-144">MyVBScriptCA</span><span class="sxs-lookup"><span data-stu-id="f093d-144">MyVBScriptCA</span></span> |



 

 

 



