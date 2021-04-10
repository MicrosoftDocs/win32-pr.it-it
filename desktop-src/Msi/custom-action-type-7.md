---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 7 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Tipo di azione personalizzata 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050153"
---
# <a name="custom-action-type-7"></a><span data-ttu-id="7a334-103">Tipo di azione personalizzata 7</span><span class="sxs-lookup"><span data-stu-id="7a334-103">Custom Action Type 7</span></span>

<span data-ttu-id="7a334-104">Il tipo di azione personalizzata 7 viene usato con le installazioni simultanee.</span><span class="sxs-lookup"><span data-stu-id="7a334-104">The Custom Action Type 7 is used with concurrent installations.</span></span> <span data-ttu-id="7a334-105">Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico.</span><span class="sxs-lookup"><span data-stu-id="7a334-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="7a334-106">Per ulteriori informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="7a334-106">For more information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="7a334-107">Questa azione personalizzata consente di installare un altro pacchetto di installazione annidato all'interno del primo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7a334-107">This custom action installs another installer package that is nested inside of the first package.</span></span>

## <a name="source"></a><span data-ttu-id="7a334-108">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="7a334-108">Source</span></span>

<span data-ttu-id="7a334-109">Il database dell'applicazione simultanea viene archiviato come sottoarchivio del pacchetto e il nome della sottoarchiviazione viene designato nel campo di origine della [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a334-109">The database of the concurrent application is stored as a substorage of the package, and the name of the substorage is designated in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="7a334-110">Tipo numerico</span><span class="sxs-lookup"><span data-stu-id="7a334-110">Numeric Type</span></span>



| <span data-ttu-id="7a334-111">Nome tipo</span><span class="sxs-lookup"><span data-stu-id="7a334-111">Type name</span></span>                                                      | <span data-ttu-id="7a334-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7a334-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="7a334-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span><span class="sxs-lookup"><span data-stu-id="7a334-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span></span> | <span data-ttu-id="7a334-114">7</span><span class="sxs-lookup"><span data-stu-id="7a334-114">7</span></span>     |



 

## <a name="target"></a><span data-ttu-id="7a334-115">Destinazione</span><span class="sxs-lookup"><span data-stu-id="7a334-115">Target</span></span>

<span data-ttu-id="7a334-116">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene le impostazioni delle proprietà da passare all'installazione simultanea.</span><span class="sxs-lookup"><span data-stu-id="7a334-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings to be passed to the concurrent installation.</span></span> <span data-ttu-id="7a334-117">Queste impostazioni delle proprietà possono specificare funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7a334-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="7a334-118">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="7a334-118">Return Processing Options</span></span>

<span data-ttu-id="7a334-119">La sessione di installazione simultanea viene eseguita come thread separato nel processo corrente.</span><span class="sxs-lookup"><span data-stu-id="7a334-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="7a334-120">Un'installazione simultanea non può essere eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="7a334-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="7a334-121">Vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="7a334-121">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="7a334-122">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="7a334-122">Execution Scheduling Options</span></span>

<span data-ttu-id="7a334-123">Sono disponibili flag di opzioni che consentono di controllare la potenziale esecuzione multipla di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="7a334-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="7a334-124">Vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="7a334-124">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="7a334-125">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="7a334-125">In-Script Execution Options</span></span>

<span data-ttu-id="7a334-126">Questa azione personalizzata non usa questa opzione.</span><span class="sxs-lookup"><span data-stu-id="7a334-126">This custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="7a334-127">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="7a334-127">Return Values</span></span>

<span data-ttu-id="7a334-128">Lo stato di restituzione dell'uscita utente, dell'esito negativo, della sospensione o dell'esito positivo di un'installazione simultanea viene elaborato nello stesso modo di qualsiasi altra azione.</span><span class="sxs-lookup"><span data-stu-id="7a334-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="7a334-129">Si noti tuttavia che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log.</span><span class="sxs-lookup"><span data-stu-id="7a334-129">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="7a334-130">Se, ad esempio, il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito l'errore \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7a334-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="7a334-131">Per ulteriori informazioni su questa traduzione, vedere [registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7a334-131">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="7a334-132">Si noti che se l'installazione simultanea è impostata su **msidbCustomActionTypeContinue** , viene restituito l'errore install \_ \_ USEREXIT, Error Install reboot \_ \_ , ERROR \_ install \_ reboot \_ Now oppure Error \_ Success \_ reboot \_ Required viene considerato come errore \_ riuscito.</span><span class="sxs-lookup"><span data-stu-id="7a334-132">Note that if a concurrent install has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="7a334-133">Ciò significa che se si imposta **msidbCustomActionTypeContinue** e l'installazione simultanea richiede un riavvio, il requisito per il riavvio verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="7a334-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="7a334-134">Inoltre, il codice di errore dell'azione personalizzata di installazione simultanea verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="7a334-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="7a334-135">Se **msidbCustomActionTypeContinue** non è impostato, i codici restituiti seguenti più l'errore \_ Success vengono considerati come operazione riuscita e hanno i significati seguenti.</span><span class="sxs-lookup"><span data-stu-id="7a334-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="7a334-136">Altri codici restituiti vengono considerati come errori.</span><span class="sxs-lookup"><span data-stu-id="7a334-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="7a334-137">Messaggio</span><span class="sxs-lookup"><span data-stu-id="7a334-137">Message</span></span>                          | <span data-ttu-id="7a334-138">Significato</span><span class="sxs-lookup"><span data-stu-id="7a334-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a334-139">ERRORE \_ installazione \_ riavvio</span><span class="sxs-lookup"><span data-stu-id="7a334-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="7a334-140">Il flag di riavvio verrà impostato per il riavvio alla fine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="7a334-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="7a334-141">ERRORE \_ installazione \_ riavvio \_ ora</span><span class="sxs-lookup"><span data-stu-id="7a334-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="7a334-142">Per completare l'installazione, è necessario riavviare il.</span><span class="sxs-lookup"><span data-stu-id="7a334-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="7a334-143">Il riavvio verrà elaborato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="7a334-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="7a334-144">ERRORE \_ di \_ riavvio \_ necessario</span><span class="sxs-lookup"><span data-stu-id="7a334-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="7a334-145">È stato richiesto un riavvio, ma è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="7a334-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="7a334-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a334-146">Remarks</span></span>

<span data-ttu-id="7a334-147">Un'espressione condizionale è necessaria per abilitare l'installazione simultanea durante l'installazione o la rimozione del componente o della funzionalità associata.</span><span class="sxs-lookup"><span data-stu-id="7a334-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a334-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a334-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a334-149">Installazioni simultanee</span><span class="sxs-lookup"><span data-stu-id="7a334-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="7a334-150">Riferimento all'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="7a334-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="7a334-151">Informazioni sulle azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="7a334-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="7a334-152">Uso di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="7a334-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="7a334-153">Valori restituiti dell'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="7a334-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



