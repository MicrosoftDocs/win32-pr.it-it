---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 39 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Tipo di azione personalizzata 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882734"
---
# <a name="custom-action-type-39"></a><span data-ttu-id="dfe2b-103">Tipo di azione personalizzata 39</span><span class="sxs-lookup"><span data-stu-id="dfe2b-103">Custom Action Type 39</span></span>

<span data-ttu-id="dfe2b-104">Il tipo di azione personalizzata 39 viene usato con le installazioni simultanee.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-104">The Custom Action Type 39 is used with concurrent installations.</span></span> <span data-ttu-id="dfe2b-105">Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="dfe2b-106">Per informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="dfe2b-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="dfe2b-107">Digitare 39 azione personalizzata consente di installare un'applicazione annunciata o già installata.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-107">Type 39 custom action installs an application that is advertised or already installed.</span></span> <span data-ttu-id="dfe2b-108">Questo tipo di azione personalizzata può essere utilizzato per reinstallare o rimuovere un prodotto che è stato installato come installazione simultanea dal pacchetto di installazione del prodotto corrente.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-108">This custom action type may be used to reinstall or remove a product that has been installed as a concurrent installation by the current product's installation package.</span></span> <span data-ttu-id="dfe2b-109">Non è possibile usare l'azione personalizzata di tipo 39 per reinstallare o rimuovere il prodotto precedentemente installato in qualsiasi altro modo.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-109">The Type 39 custom action cannot be used to reinstall or remove any product previously installed by any other means.</span></span> <span data-ttu-id="dfe2b-110">Se, ad esempio, il prodotto secondario viene installato utilizzando un tipo 39, un tipo 23 o un'azione personalizzata di tipo 7 durante l'installazione del prodotto principale, è possibile utilizzare un'azione personalizzata di tipo 39 per rimuovere il prodotto secondario quando viene disinstallato il prodotto primario.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-110">For example, if the secondary product is installed using a Type 39, Type 23, or Type 7 custom action during the installation of the primary product, a Type 39 custom action may be used to remove the secondary product when the primary product is uninstalled.</span></span>

## <a name="source"></a><span data-ttu-id="dfe2b-111">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="dfe2b-111">Source</span></span>

<span data-ttu-id="dfe2b-112">Il campo di origine della [tabella CustomAction](customaction-table.md) contiene il codice prodotto per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-112">The Source field of the [CustomAction table](customaction-table.md) contains the product code for the application.</span></span>

## <a name="numeric-type"></a><span data-ttu-id="dfe2b-113">Tipo numerico</span><span class="sxs-lookup"><span data-stu-id="dfe2b-113">Numeric Type</span></span>



| <span data-ttu-id="dfe2b-114">Nome tipo</span><span class="sxs-lookup"><span data-stu-id="dfe2b-114">Type name</span></span>                                                     | <span data-ttu-id="dfe2b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="dfe2b-115">Value</span></span> |
|---------------------------------------------------------------|-------|
| <span data-ttu-id="dfe2b-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span><span class="sxs-lookup"><span data-stu-id="dfe2b-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span></span> | <span data-ttu-id="dfe2b-117">39</span><span class="sxs-lookup"><span data-stu-id="dfe2b-117">39</span></span>    |



 

## <a name="target"></a><span data-ttu-id="dfe2b-118">Destinazione</span><span class="sxs-lookup"><span data-stu-id="dfe2b-118">Target</span></span>

<span data-ttu-id="dfe2b-119">Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene le impostazioni delle proprietà che devono essere passate all'installazione simultanea.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-119">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="dfe2b-120">Queste impostazioni delle proprietà possono specificare funzionalità.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-120">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="dfe2b-121">Opzioni di elaborazione restituite</span><span class="sxs-lookup"><span data-stu-id="dfe2b-121">Return Processing Options</span></span>

<span data-ttu-id="dfe2b-122">Il tipo di azione personalizzata 39 ha esito negativo se l'applicazione non è annunciata o installata.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-122">The custom action type 39 fails if the application is not advertised or installed.</span></span> <span data-ttu-id="dfe2b-123">Per evitare questo errore, è necessario impostare **msidbCustomActionTypeContinueflag**.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-123">To avoid this failure, you must set the **msidbCustomActionTypeContinueflag**.</span></span>

<span data-ttu-id="dfe2b-124">Non è possibile eseguire un'installazione simultanea in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-124">A concurrent install cannot run asynchronously.</span></span>

<span data-ttu-id="dfe2b-125">Vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="dfe2b-125">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="dfe2b-126">Opzioni di pianificazione dell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="dfe2b-126">Execution Scheduling Options</span></span>

<span data-ttu-id="dfe2b-127">Sono disponibili flag di opzioni che consentono di controllare la potenziale esecuzione multipla di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-127">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="dfe2b-128">Vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="dfe2b-128">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="dfe2b-129">Opzioni di esecuzione In-Script</span><span class="sxs-lookup"><span data-stu-id="dfe2b-129">In-Script Execution Options</span></span>

<span data-ttu-id="dfe2b-130">L'azione personalizzata non usa questa opzione.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-130">The custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="dfe2b-131">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="dfe2b-131">Return Values</span></span>

<span data-ttu-id="dfe2b-132">Lo stato di restituzione dell'uscita utente, dell'esito negativo, della sospensione o dell'esito positivo di un'installazione simultanea viene elaborato nello stesso modo di qualsiasi altra azione.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-132">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="dfe2b-133">Si noti tuttavia che Windows Installer converte i valori restituiti da tutte le azioni quando scrive il valore restituito nel file di log.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-133">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="dfe2b-134">Se, ad esempio, il valore restituito dell'azione viene visualizzato come 1 nel file di log, significa che l'azione ha restituito l'errore \_ Success.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-134">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="dfe2b-135">Per altre informazioni, vedere [registrazione dei valori restituiti dell'azione](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="dfe2b-135">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="dfe2b-136">Si noti che se l'installazione simultanea è impostata su **msidbCustomActionTypeContinue** , viene restituito un errore di installazione di USEREXIT, il riavvio dell'installazione dell'errore, l'installazione del riavvio del sistema \_ \_ \_ \_ \_ \_ \_ ora o l'errore \_ \_ \_ di riavvio richiesto viene considerato come \_ esito positivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-136">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="dfe2b-137">Ciò significa che se si imposta **msidbCustomActionTypeContinue** e l'installazione simultanea richiede un riavvio, il requisito per il riavvio verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-137">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="dfe2b-138">Inoltre, il codice di errore dell'azione personalizzata di installazione simultanea verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-138">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="dfe2b-139">Se **msidbCustomActionTypeContinue** non è impostato, i codici restituiti seguenti più l'errore \_ Success vengono considerati come operazione riuscita e hanno i significati seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-139">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="dfe2b-140">Altri codici restituiti vengono considerati come errori.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-140">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="dfe2b-141">Messaggio</span><span class="sxs-lookup"><span data-stu-id="dfe2b-141">Message</span></span>                          | <span data-ttu-id="dfe2b-142">Significato</span><span class="sxs-lookup"><span data-stu-id="dfe2b-142">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe2b-143">ERRORE \_ installazione \_ riavvio</span><span class="sxs-lookup"><span data-stu-id="dfe2b-143">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="dfe2b-144">Il flag di riavvio verrà impostato per il riavvio alla fine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-144">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="dfe2b-145">ERRORE \_ installazione \_ riavvio \_ ora</span><span class="sxs-lookup"><span data-stu-id="dfe2b-145">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="dfe2b-146">Per completare l'installazione, è necessario riavviare il.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-146">A restart is required before completing the installation.</span></span> <span data-ttu-id="dfe2b-147">Il riavvio verrà elaborato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-147">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="dfe2b-148">ERRORE \_ di \_ riavvio \_ necessario</span><span class="sxs-lookup"><span data-stu-id="dfe2b-148">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="dfe2b-149">È stato richiesto un riavvio, ma è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-149">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="dfe2b-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfe2b-150">Remarks</span></span>

<span data-ttu-id="dfe2b-151">Un'espressione condizionale è necessaria per abilitare l'installazione simultanea durante l'installazione o la rimozione del componente o della funzionalità associata.</span><span class="sxs-lookup"><span data-stu-id="dfe2b-151">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfe2b-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dfe2b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfe2b-153">Installazioni simultanee</span><span class="sxs-lookup"><span data-stu-id="dfe2b-153">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="dfe2b-154">Riferimento all'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="dfe2b-154">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="dfe2b-155">Informazioni sulle azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="dfe2b-155">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="dfe2b-156">Uso di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="dfe2b-156">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



