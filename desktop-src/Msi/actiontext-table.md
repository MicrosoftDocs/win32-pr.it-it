---
description: La tabella ActionText contiene testo da visualizzare in una finestra di dialogo di avanzamento e scritta nel log per le azioni che importano molto tempo per l'esecuzione. Il testo visualizzato è costituito dalla descrizione dell'azione e, facoltativamente, dal formato dati dell'azione.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabella ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311087"
---
# <a name="actiontext-table"></a><span data-ttu-id="605e3-104">Tabella ActionText</span><span class="sxs-lookup"><span data-stu-id="605e3-104">ActionText Table</span></span>

<span data-ttu-id="605e3-105">La tabella ActionText contiene testo da visualizzare in una finestra di dialogo di avanzamento e scritta nel log per le azioni che importano molto tempo per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="605e3-105">The ActionText Table contains text to be displayed in a progress dialog box, and written to the log for actions that take a long time to execute.</span></span> <span data-ttu-id="605e3-106">Il testo visualizzato è costituito dalla descrizione dell'azione e, facoltativamente, dal formato dati dell'azione.</span><span class="sxs-lookup"><span data-stu-id="605e3-106">The displayed text consists of the action description and optionally formatted data from the action.</span></span>

<span data-ttu-id="605e3-107">La tabella ActionText include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="605e3-107">The ActionText Table has the following columns.</span></span>



| <span data-ttu-id="605e3-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="605e3-108">Column</span></span>      | <span data-ttu-id="605e3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="605e3-109">Type</span></span>                         | <span data-ttu-id="605e3-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="605e3-110">Key</span></span> | <span data-ttu-id="605e3-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="605e3-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="605e3-112">Azione</span><span class="sxs-lookup"><span data-stu-id="605e3-112">Action</span></span>      | [<span data-ttu-id="605e3-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="605e3-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="605e3-114">S</span><span class="sxs-lookup"><span data-stu-id="605e3-114">Y</span></span>   | <span data-ttu-id="605e3-115">N</span><span class="sxs-lookup"><span data-stu-id="605e3-115">N</span></span>        |
| <span data-ttu-id="605e3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="605e3-116">Description</span></span> | [<span data-ttu-id="605e3-117">Text</span><span class="sxs-lookup"><span data-stu-id="605e3-117">Text</span></span>](text.md)             | <span data-ttu-id="605e3-118">N</span><span class="sxs-lookup"><span data-stu-id="605e3-118">N</span></span>   | <span data-ttu-id="605e3-119">S</span><span class="sxs-lookup"><span data-stu-id="605e3-119">Y</span></span>        |
| <span data-ttu-id="605e3-120">Modello</span><span class="sxs-lookup"><span data-stu-id="605e3-120">Template</span></span>    | [<span data-ttu-id="605e3-121">Modello</span><span class="sxs-lookup"><span data-stu-id="605e3-121">Template</span></span>](template.md)     | <span data-ttu-id="605e3-122">N</span><span class="sxs-lookup"><span data-stu-id="605e3-122">N</span></span>   | <span data-ttu-id="605e3-123">S</span><span class="sxs-lookup"><span data-stu-id="605e3-123">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="605e3-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="605e3-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="605e3-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="605e3-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="605e3-126">Nome dell'azione.</span><span class="sxs-lookup"><span data-stu-id="605e3-126">Name of the action.</span></span>

<span data-ttu-id="605e3-127">Chiave della tabella primaria.</span><span class="sxs-lookup"><span data-stu-id="605e3-127">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="605e3-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="605e3-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="605e3-129">Descrizione localizzata visualizzata nella finestra di dialogo dello stato di avanzamento o scritta nel log durante l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="605e3-129">Localized description that is displayed in the progress dialog box, or written to the log when the action is executing.</span></span>

</dd> <dt>

<span data-ttu-id="605e3-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Modello</span><span class="sxs-lookup"><span data-stu-id="605e3-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Template</span></span>
</dt> <dd>

<span data-ttu-id="605e3-131">Modello di formato localizzato utilizzato per formattare i record di dati dell'azione da visualizzare durante l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="605e3-131">A localized format template that is used to format action data records to display during action execution.</span></span> <span data-ttu-id="605e3-132">Se non viene fornito un modello, i dati dell'azione non vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="605e3-132">If a template is not supplied, then the action data is not displayed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="605e3-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="605e3-133">Remarks</span></span>

<span data-ttu-id="605e3-134">Le voci nella tabella ActionText, in genere, fanno riferimento a azioni nelle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="605e3-134">Typically, the entries in the ActionText table refer to actions in sequence tables.</span></span> <span data-ttu-id="605e3-135">Sono presenti altre azioni eseguite dal programma di installazione che non sono elencate nella tabella di sequenza, ma che è comunque necessario specificare nella tabella.</span><span class="sxs-lookup"><span data-stu-id="605e3-135">There are other actions the installer performs that are not listed in the sequence table, but still need to be specified in the table.</span></span> <span data-ttu-id="605e3-136">Nella tabella seguente vengono identificate le voci di tabella richieste in cui il nome e il modello dell'azione devono essere creati esattamente come illustrato, ma la descrizione può essere personalizzata.</span><span class="sxs-lookup"><span data-stu-id="605e3-136">The following table identifies the required table entries where the action name and template must be authored exactly as shown, but the description can be customized.</span></span>



| <span data-ttu-id="605e3-137">Azione</span><span class="sxs-lookup"><span data-stu-id="605e3-137">Action</span></span>          | <span data-ttu-id="605e3-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="605e3-138">Description</span></span>                             | <span data-ttu-id="605e3-139">Modello</span><span class="sxs-lookup"><span data-stu-id="605e3-139">Template</span></span> |
|-----------------|-----------------------------------------|----------|
| <span data-ttu-id="605e3-140">Rollback</span><span class="sxs-lookup"><span data-stu-id="605e3-140">Rollback</span></span>        | <span data-ttu-id="605e3-141">Annulla le azioni.</span><span class="sxs-lookup"><span data-stu-id="605e3-141">Undoes actions.</span></span>                         | <span data-ttu-id="605e3-142">\[1\]</span><span class="sxs-lookup"><span data-stu-id="605e3-142">\[1\]</span></span>    |
| <span data-ttu-id="605e3-143">RollbackCleanup</span><span class="sxs-lookup"><span data-stu-id="605e3-143">RollbackCleanup</span></span> | <span data-ttu-id="605e3-144">Rimuove i file obsoleti.</span><span class="sxs-lookup"><span data-stu-id="605e3-144">Removes old files.</span></span>                      | <span data-ttu-id="605e3-145">\[1\]</span><span class="sxs-lookup"><span data-stu-id="605e3-145">\[1\]</span></span>    |
| <span data-ttu-id="605e3-146">GenerateScript</span><span class="sxs-lookup"><span data-stu-id="605e3-146">GenerateScript</span></span>  | <span data-ttu-id="605e3-147">Genera operazioni di sistema per l'azione.</span><span class="sxs-lookup"><span data-stu-id="605e3-147">Generates system operations for action.</span></span> | <span data-ttu-id="605e3-148">\[1\]</span><span class="sxs-lookup"><span data-stu-id="605e3-148">\[1\]</span></span>    |



 

> [!Note]  
> <span data-ttu-id="605e3-149">Il testo dell'azione viene visualizzato solo per le azioni eseguite all'interno dello script di installazione.</span><span class="sxs-lookup"><span data-stu-id="605e3-149">Action text is only displayed for actions that run within the installation script.</span></span> <span data-ttu-id="605e3-150">Il testo dell'azione viene pertanto visualizzato solo per le azioni sequenziate tra le azioni [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="605e3-150">Therefore, action text is only displayed for actions that are sequenced between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

 

<span data-ttu-id="605e3-151">È possibile importare una tabella ActionText localizzata nel database usando Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="605e3-151">You can import a localized ActionText table into your database by using Msidb.exe or [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="605e3-152">L'SDK include una tabella ActionText localizzata per ogni lingua elencata nella sezione [localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md) .</span><span class="sxs-lookup"><span data-stu-id="605e3-152">The SDK includes a localized ActionText Table for each of the languages listed in the [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) section.</span></span> <span data-ttu-id="605e3-153">Se la tabella ActionText non è popolata, il programma di installazione carica le stringhe localizzate per la lingua specificata dalla proprietà [**ProductLanguage**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="605e3-153">If the ActionText table is not populated, the installer loads localized strings for the language specified by the [**ProductLanguage**](productlanguage.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="605e3-154">Convalida</span><span class="sxs-lookup"><span data-stu-id="605e3-154">Validation</span></span>

<dl>

[<span data-ttu-id="605e3-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="605e3-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="605e3-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="605e3-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="605e3-157">ICE46</span><span class="sxs-lookup"><span data-stu-id="605e3-157">ICE46</span></span>](ice46.md)  
</dl>

 

 



