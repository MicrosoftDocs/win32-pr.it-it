---
description: Questa tabella temporanea Abilita l'opzione di disinstallazione patch azione personalizzata per le azioni personalizzate aggiunte o aggiornate da una patch.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316256"
---
# <a name="msitransformview"></a><span data-ttu-id="39499-103">MsiTransformView</span><span class="sxs-lookup"><span data-stu-id="39499-103">MsiTransformView</span></span>

<span data-ttu-id="39499-104">Questa tabella temporanea Abilita l' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) per le azioni personalizzate aggiunte o aggiornate da una patch.</span><span class="sxs-lookup"><span data-stu-id="39499-104">This temporary table enables the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) for custom actions added or updated by a patch.</span></span>

<span data-ttu-id="39499-105">Se una patch aggiunge o aggiorna un'azione personalizzata con l'attributo **msidbCustomActionTypePatchUninstall** , Windows Installer esegue l'azione personalizzata nuova o aggiornata quando la patch viene disinstallata.</span><span class="sxs-lookup"><span data-stu-id="39499-105">If a patch adds or updates a custom action having the **msidbCustomActionTypePatchUninstall** attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="39499-106">Windows Installer rende gli aggiornamenti all'interno della patch disinstallati disponibili per l'azione personalizzata di disinstallazione della patch.</span><span class="sxs-lookup"><span data-stu-id="39499-106">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="39499-107">La patch deve includere una *<PatchGUID>* tabella MsiTransformView per fornire queste informazioni Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="39499-107">The patch must include a MsiTransformView *<PatchGUID>* table to provide this information to Windows Installer.</span></span> <span data-ttu-id="39499-108">Le informazioni contenute in questa tabella sono disponibili per qualsiasi azione personalizzata immediata e non sono disponibili per le azioni personalizzate posticipate.</span><span class="sxs-lookup"><span data-stu-id="39499-108">The information in this table is available to any immediate custom action, and is unavailable to deferred custom actions.</span></span>

<span data-ttu-id="39499-109">**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="39499-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="39499-110">L' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) è disponibile a partire da Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="39499-110">The [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="39499-111">Questa tabella deve essere denominata MsiTransformView *<PatchGUID>* Table, dove *<PatchGUID>* è il GUID che identifica in modo univoco la patch.</span><span class="sxs-lookup"><span data-stu-id="39499-111">This table should be named MsiTransformView *<PatchGUID>* Table, where *<PatchGUID>* is the GUID that uniquely identifies the patch.</span></span> <span data-ttu-id="39499-112">La *<PatchGUID>* tabella MsiTransformView include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="39499-112">The MsiTransformView *<PatchGUID>* Table has the following columns.</span></span>



| <span data-ttu-id="39499-113">Colonna</span><span class="sxs-lookup"><span data-stu-id="39499-113">Column</span></span>  | <span data-ttu-id="39499-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="39499-114">Type</span></span>                         | <span data-ttu-id="39499-115">Chiave</span><span class="sxs-lookup"><span data-stu-id="39499-115">Key</span></span> | <span data-ttu-id="39499-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="39499-116">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="39499-117">Tabella</span><span class="sxs-lookup"><span data-stu-id="39499-117">Table</span></span>   | [<span data-ttu-id="39499-118">Identificatore</span><span class="sxs-lookup"><span data-stu-id="39499-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="39499-119">S</span><span class="sxs-lookup"><span data-stu-id="39499-119">Y</span></span>   | <span data-ttu-id="39499-120">N</span><span class="sxs-lookup"><span data-stu-id="39499-120">N</span></span>        |
| <span data-ttu-id="39499-121">Colonna</span><span class="sxs-lookup"><span data-stu-id="39499-121">Column</span></span>  | [<span data-ttu-id="39499-122">Text</span><span class="sxs-lookup"><span data-stu-id="39499-122">Text</span></span>](text.md)             | <span data-ttu-id="39499-123">S</span><span class="sxs-lookup"><span data-stu-id="39499-123">Y</span></span>   | <span data-ttu-id="39499-124">N</span><span class="sxs-lookup"><span data-stu-id="39499-124">N</span></span>        |
| <span data-ttu-id="39499-125">Riga</span><span class="sxs-lookup"><span data-stu-id="39499-125">Row</span></span>     | [<span data-ttu-id="39499-126">Text</span><span class="sxs-lookup"><span data-stu-id="39499-126">Text</span></span>](text.md)             | <span data-ttu-id="39499-127">S</span><span class="sxs-lookup"><span data-stu-id="39499-127">Y</span></span>   | <span data-ttu-id="39499-128">S</span><span class="sxs-lookup"><span data-stu-id="39499-128">Y</span></span>        |
| <span data-ttu-id="39499-129">Data</span><span class="sxs-lookup"><span data-stu-id="39499-129">Data</span></span>    | [<span data-ttu-id="39499-130">Text</span><span class="sxs-lookup"><span data-stu-id="39499-130">Text</span></span>](text.md)             | <span data-ttu-id="39499-131">N</span><span class="sxs-lookup"><span data-stu-id="39499-131">N</span></span>   | <span data-ttu-id="39499-132">S</span><span class="sxs-lookup"><span data-stu-id="39499-132">Y</span></span>        |
| <span data-ttu-id="39499-133">Corrente</span><span class="sxs-lookup"><span data-stu-id="39499-133">Current</span></span> | [<span data-ttu-id="39499-134">Text</span><span class="sxs-lookup"><span data-stu-id="39499-134">Text</span></span>](text.md)             | <span data-ttu-id="39499-135">N</span><span class="sxs-lookup"><span data-stu-id="39499-135">N</span></span>   | <span data-ttu-id="39499-136">S</span><span class="sxs-lookup"><span data-stu-id="39499-136">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="39499-137">Colonna</span><span class="sxs-lookup"><span data-stu-id="39499-137">Column</span></span>

<dl> <dt>

<span data-ttu-id="39499-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo</span><span class="sxs-lookup"><span data-stu-id="39499-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="39499-139">Nome di una tabella di database modificata.</span><span class="sxs-lookup"><span data-stu-id="39499-139">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="39499-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna</span><span class="sxs-lookup"><span data-stu-id="39499-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="39499-141">Nome di una colonna di tabella modificata o di inserimento, eliminazione, creazione o eliminazione.</span><span class="sxs-lookup"><span data-stu-id="39499-141">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="39499-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Riga</span><span class="sxs-lookup"><span data-stu-id="39499-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="39499-143">Elenco dei valori di chiave primaria separati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="39499-143">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="39499-144">I valori di chiave primaria null sono rappresentati da un singolo carattere di spazio.</span><span class="sxs-lookup"><span data-stu-id="39499-144">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="39499-145">Un valore null in questa colonna indica una modifica dello schema.</span><span class="sxs-lookup"><span data-stu-id="39499-145">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="39499-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati</span><span class="sxs-lookup"><span data-stu-id="39499-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="39499-147">Dati, nome di un flusso di dati o definizione di colonna.</span><span class="sxs-lookup"><span data-stu-id="39499-147">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="39499-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrente</span><span class="sxs-lookup"><span data-stu-id="39499-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="39499-149">Valore corrente dal database di riferimento o da un numero di colonna.</span><span class="sxs-lookup"><span data-stu-id="39499-149">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39499-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="39499-150">Remarks</span></span>

<span data-ttu-id="39499-151">Patch disinstallare le azioni personalizzate vengono eseguite quando la patch viene disinstallata.</span><span class="sxs-lookup"><span data-stu-id="39499-151">Patch uninstall custom actions run when the patch is uninstalled.</span></span> <span data-ttu-id="39499-152">Non vengono eseguite quando il prodotto viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="39499-152">They do not run when the product is uninstalled.</span></span> <span data-ttu-id="39499-153">Usare l' [opzione di disinstallazione patch di azione personalizzata](custom-action-patch-uninstall-option.md) e questa tabella per eseguire un'operazione personalizzata solo quando la patch viene disinstallata.</span><span class="sxs-lookup"><span data-stu-id="39499-153">Use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) and this table to run a custom only when the patch is being uninstalled.</span></span>

<span data-ttu-id="39499-154">Una patch può aggiornare un'azione personalizzata fornita nel pacchetto originale (file con estensione msi). Per eseguire la versione aggiornata dell'azione personalizzata quando la patch viene disinstallata, contrassegnare l'azione personalizzata con l'attributo **msidbCustomActionTypePatchUninstall** nel pacchetto originale.</span><span class="sxs-lookup"><span data-stu-id="39499-154">A patch can update a custom action provided in the original package (.msi file.) To run the updated version of the custom action when the patch is uninstalled, mark the custom action with the **msidbCustomActionTypePatchUninstall** attribute in the original package.</span></span>

 

 



