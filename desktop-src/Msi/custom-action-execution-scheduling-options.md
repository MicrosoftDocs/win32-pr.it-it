---
description: Poiché un'azione personalizzata può essere pianificata sia nell'interfaccia utente che nelle tabelle di sequenza di esecuzione e può essere eseguita nel servizio o nel processo client, un'azione personalizzata può essere potenzialmente eseguita più volte.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Opzioni di pianificazione dell'esecuzione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313358"
---
# <a name="custom-action-execution-scheduling-options"></a><span data-ttu-id="0ce85-103">Opzioni di pianificazione dell'esecuzione di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="0ce85-103">Custom Action Execution Scheduling Options</span></span>

<span data-ttu-id="0ce85-104">Poiché un'azione personalizzata può essere pianificata sia nell'interfaccia utente che nelle tabelle di sequenza di esecuzione e può essere eseguita nel servizio o nel processo client, un'azione personalizzata può essere potenzialmente eseguita più volte.</span><span class="sxs-lookup"><span data-stu-id="0ce85-104">Because a custom action can be scheduled in both the UI and execute sequence tables, and can be executed either in the service or client process, a custom action can potentially execute multiple times.</span></span>

<span data-ttu-id="0ce85-105">Si noti che il programma di installazione:</span><span class="sxs-lookup"><span data-stu-id="0ce85-105">Note that the installer:</span></span>

-   <span data-ttu-id="0ce85-106">Esegue le azioni in una tabella di sequenza immediatamente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0ce85-106">Executes actions in a sequence table immediately by default.</span></span>
-   <span data-ttu-id="0ce85-107">Non esegue un'azione se il campo dell'espressione condizionale della tabella di sequenza restituisce false.</span><span class="sxs-lookup"><span data-stu-id="0ce85-107">Does not execute an action if the conditional expression field of the sequence table evaluates to False.</span></span>
-   <span data-ttu-id="0ce85-108">Elabora la tabella di sequenza dell'interfaccia utente nel processo client se il livello di interfaccia dell'utente interno è impostato sulla modalità di interfaccia utente completa (vedere [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) per una descrizione dei livelli dell'interfaccia utente).</span><span class="sxs-lookup"><span data-stu-id="0ce85-108">Processes the UI sequence table in the client process if the internal user's interface level is set to the full UI mode (see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) for a description of UI levels).</span></span>
-   <span data-ttu-id="0ce85-109">È un servizio registrato per impostazione predefinita quando si utilizza Windows 2000 e, in questo caso, la tabella Execute Sequence viene elaborata nel servizio del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="0ce85-109">Is a service registered by default when using Windows 2000 and, in this case, the execute sequence table is processed in the installer service.</span></span>

<span data-ttu-id="0ce85-110">È possibile utilizzare i flag di opzione seguenti per controllare la più immediata esecuzione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="0ce85-110">You can use the following option flags to control multiple immediate execution of custom actions.</span></span> <span data-ttu-id="0ce85-111">Per impostare un'opzione, aggiungere il valore di questa tabella al valore nel campo Type della [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ce85-111">To set an option, add the value in this table to the value in the Type field of the [CustomAction table](customaction-table.md).</span></span> <span data-ttu-id="0ce85-112">Nessuno dei seguenti flag deve essere utilizzato con [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0ce85-112">None of the following flags should be used with [deferred execution custom actions](deferred-execution-custom-actions.md).</span></span>

<dl> <dt>

<span data-ttu-id="0ce85-113"><span id="_default_"></span><span id="_DEFAULT_"></span>predefinita</span><span class="sxs-lookup"><span data-stu-id="0ce85-113"><span id="_default_"></span><span id="_DEFAULT_"></span>(default)</span></span>
</dt> <dd>

<span data-ttu-id="0ce85-114">Esadecimale: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ce85-114">Hexadecimal: 0x00000000</span></span>

<span data-ttu-id="0ce85-115">Decimale: 0</span><span class="sxs-lookup"><span data-stu-id="0ce85-115">Decimal: 0</span></span>

<span data-ttu-id="0ce85-116">Eseguire sempre.</span><span class="sxs-lookup"><span data-stu-id="0ce85-116">Always execute.</span></span> <span data-ttu-id="0ce85-117">L'azione può essere eseguita due volte se presente in entrambe le tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="0ce85-117">Action may run twice if present in both sequence tables.</span></span>

</dd> <dt>

<span data-ttu-id="0ce85-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span><span class="sxs-lookup"><span data-stu-id="0ce85-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span></span> 
</dt> <dd>

<span data-ttu-id="0ce85-119">Esadecimale: 0x00000100</span><span class="sxs-lookup"><span data-stu-id="0ce85-119">Hexadecimal: 0x00000100</span></span>

<span data-ttu-id="0ce85-120">Decimale: 256</span><span class="sxs-lookup"><span data-stu-id="0ce85-120">Decimal: 256</span></span>

<span data-ttu-id="0ce85-121">Eseguire non più di una volta se presente in entrambe le tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="0ce85-121">Execute no more than once if present in both sequence tables.</span></span> <span data-ttu-id="0ce85-122">Ignora sempre l'azione nella sequenza di esecuzione se è stata eseguita la sequenza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0ce85-122">Always skips action in execute sequence if UI sequence has run.</span></span> <span data-ttu-id="0ce85-123">Nessun effetto nella sequenza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0ce85-123">No effect in UI sequence.</span></span> <span data-ttu-id="0ce85-124">Non è necessario che l'azione sia presente o eseguita nella sequenza dell'interfaccia utente da ignorare nella sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0ce85-124">The action is not required to be present or run in the UI sequence to be skipped in the execute sequence.</span></span> <span data-ttu-id="0ce85-125">Non interessato dalla registrazione del servizio di installazione.</span><span class="sxs-lookup"><span data-stu-id="0ce85-125">Not affected by install service registration.</span></span>

</dd> <dt>

<span data-ttu-id="0ce85-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span><span class="sxs-lookup"><span data-stu-id="0ce85-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span></span>
</dt> <dd>

<span data-ttu-id="0ce85-127">Esadecimale: 0x00000200</span><span class="sxs-lookup"><span data-stu-id="0ce85-127">Hexadecimal: 0x00000200</span></span>

<span data-ttu-id="0ce85-128">Decimale: 512</span><span class="sxs-lookup"><span data-stu-id="0ce85-128">Decimal: 512</span></span>

<span data-ttu-id="0ce85-129">Eseguire una sola volta per processo se in entrambe le tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="0ce85-129">Execute once per process if in both sequence tables.</span></span> <span data-ttu-id="0ce85-130">Ignora l'azione nella sequenza di esecuzione se la sequenza dell'interfaccia utente è stata eseguita nello stesso processo, ad esempio entrambi eseguiti nel processo client.</span><span class="sxs-lookup"><span data-stu-id="0ce85-130">Skips action in execute sequence if UI sequence has been run in same process, for example both run in the client process.</span></span> <span data-ttu-id="0ce85-131">Utilizzato per impedire l'esecuzione di due azioni che modificano lo stato della sessione, ad esempio dati di proprietà e database.</span><span class="sxs-lookup"><span data-stu-id="0ce85-131">Used to prevent actions that modify the session state, such as property and database data, from running twice.</span></span>

</dd> <dt>

<span data-ttu-id="0ce85-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span><span class="sxs-lookup"><span data-stu-id="0ce85-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span></span>
</dt> <dd>

<span data-ttu-id="0ce85-133">Esadecimale: 0x00000300</span><span class="sxs-lookup"><span data-stu-id="0ce85-133">Hexadecimal: 0x00000300</span></span>

<span data-ttu-id="0ce85-134">Decimale: 768</span><span class="sxs-lookup"><span data-stu-id="0ce85-134">Decimal: 768</span></span>

<span data-ttu-id="0ce85-135">Eseguire solo se in esecuzione sul client dopo l'esecuzione della sequenza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0ce85-135">Execute only if running on client after UI sequence has run.</span></span> <span data-ttu-id="0ce85-136">L'azione viene eseguita solo se la sequenza di esecuzione viene eseguita nel client seguente sequenza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0ce85-136">The action runs only if the execute sequence is run on the client following UI sequence.</span></span> <span data-ttu-id="0ce85-137">Può essere usato per fornire la logica/o oppure per disattivare l'elaborazione correlata all'interfaccia utente, se già eseguita per la sessione client.</span><span class="sxs-lookup"><span data-stu-id="0ce85-137">May be used to provide either/or logic, or to suppress the UI-related processing if already done for the client session.</span></span>

</dd> </dl>

<span data-ttu-id="0ce85-138">Si noti che per eseguire un'azione personalizzata durante due modalità di esecuzione diverse, creare due voci nella [tabella CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0ce85-138">Note that to run a custom action during two different run modes, author two entries into the [CustomAction table](customaction-table.md) .</span></span> <span data-ttu-id="0ce85-139">Ad esempio, per eseguire un'azione personalizzata che chiama una libreria di collegamento dinamico (DLL) C/C++ ( [tipo di azione personalizzata 1](custom-action-type-1.md)) quando la modalità è MSIRUNMODE \_ scheduled e MSIRUNMODE \_ rollback, inserire due voci nella tabella CustomAction che chiamano la stessa dll ma con tipi numerici diversi.</span><span class="sxs-lookup"><span data-stu-id="0ce85-139">For example, to have a custom action that calls a C/C++ dynamic link library (DLL) ( [Custom Action Type 1](custom-action-type-1.md)) both when the mode is MSIRUNMODE\_SCHEDULED and MSIRUNMODE\_ROLLBACK, put two entries in the CustomAction table that call the same DLL but that have different numeric types.</span></span> <span data-ttu-id="0ce85-140">Includere il codice che chiama [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) per determinare quando eseguire l'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0ce85-140">Include code that calls [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) to determine when to run which custom action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ce85-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ce85-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ce85-142">Riferimento all'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="0ce85-142">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="0ce85-143">Informazioni sulle azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="0ce85-143">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="0ce85-144">Uso di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="0ce85-144">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



