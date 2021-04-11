---
description: ICE40 esegue la convalida varie.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131871"
---
# <a name="ice40"></a><span data-ttu-id="09476-103">ICE40</span><span class="sxs-lookup"><span data-stu-id="09476-103">ICE40</span></span>

<span data-ttu-id="09476-104">ICE40 esegue la convalida varie.</span><span class="sxs-lookup"><span data-stu-id="09476-104">ICE40 does miscellaneous validation.</span></span>

## <a name="result"></a><span data-ttu-id="09476-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="09476-105">Result</span></span>

<span data-ttu-id="09476-106">ICE40 invia avvisi sugli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="09476-106">ICE40 posts warnings on the following:</span></span>

-   <span data-ttu-id="09476-107">La proprietà [**REINSTALLMODE**](reinstallmode.md) è stata sottoposta a override.</span><span class="sxs-lookup"><span data-stu-id="09476-107">The [**REINSTALLMODE**](reinstallmode.md) property has been overridden.</span></span>
-   <span data-ttu-id="09476-108">La [tabella RemoveIniFile](removeinifile-table.md) include una voce Delete tag senza valore.</span><span class="sxs-lookup"><span data-stu-id="09476-108">The [RemoveIniFile table](removeinifile-table.md) has a Delete Tag entry with no value.</span></span>
-   <span data-ttu-id="09476-109">Nel file con estensione msi manca la [tabella degli errori](error-table.md) e la proprietà di [**Riepilogo dei conteggi delle pagine**](page-count-summary.md) è minore o uguale a 100.</span><span class="sxs-lookup"><span data-stu-id="09476-109">The .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <span data-ttu-id="09476-110">Questo avviso di ghiaccio è obsoleto perché per Windows Installer non è necessario che il pacchetto includa una tabella degli errori.</span><span class="sxs-lookup"><span data-stu-id="09476-110">This ICE warning is obsolete because Windows Installer does not require the package to have an Error table.</span></span> <span data-ttu-id="09476-111">È possibile recuperare i messaggi di errore utilizzando Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="09476-111">Error messages can be retrieved using Msimsg.dll.</span></span>

## <a name="example"></a><span data-ttu-id="09476-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="09476-112">Example</span></span>

[<span data-ttu-id="09476-113">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="09476-113">Property Table</span></span>](property-table.md)



| <span data-ttu-id="09476-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="09476-114">Property</span></span>                               | <span data-ttu-id="09476-115">Valore</span><span class="sxs-lookup"><span data-stu-id="09476-115">Value</span></span> |
|----------------------------------------|-------|
| [<span data-ttu-id="09476-116">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="09476-116">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="09476-117">A</span><span class="sxs-lookup"><span data-stu-id="09476-117">A</span></span>     |



 

[<span data-ttu-id="09476-118">Tabella RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="09476-118">RemoveIniFile Table</span></span>](removeinifile-table.md)



| <span data-ttu-id="09476-119">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="09476-119">RemoveIniFile</span></span>                          | <span data-ttu-id="09476-120">Azione</span><span class="sxs-lookup"><span data-stu-id="09476-120">Action</span></span> | <span data-ttu-id="09476-121">Valore</span><span class="sxs-lookup"><span data-stu-id="09476-121">Value</span></span> |
|----------------------------------------|--------|-------|
| [<span data-ttu-id="09476-122">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="09476-122">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="09476-123">4</span><span class="sxs-lookup"><span data-stu-id="09476-123">4</span></span>      |       |



 

## <a name="results"></a><span data-ttu-id="09476-124">Risultati</span><span class="sxs-lookup"><span data-stu-id="09476-124">Results</span></span>

<span data-ttu-id="09476-125">ICE40 segnala i seguenti errori.</span><span class="sxs-lookup"><span data-stu-id="09476-125">ICE40 would report the following errors.</span></span>



| <span data-ttu-id="09476-126">Errore ICE40</span><span class="sxs-lookup"><span data-stu-id="09476-126">ICE40 error</span></span>                                                                                           | <span data-ttu-id="09476-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09476-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09476-128">[**REINSTALLMODE**](reinstallmode.md) è definito nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="09476-128">[**REINSTALLMODE**](reinstallmode.md) is defined in the Property table.</span></span> <span data-ttu-id="09476-129">Questo può causare problemi.</span><span class="sxs-lookup"><span data-stu-id="09476-129">This may cause difficulties.</span></span> | <span data-ttu-id="09476-130">La definizione della proprietà [**REINSTALLMODE**](reinstallmode.md) nel file con estensione msi può causare un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="09476-130">Defining the [**REINSTALLMODE**](reinstallmode.md) property in .msi file can lead to unexpected behavior.</span></span> <span data-ttu-id="09476-131">Per correggere l'errore, non definire questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="09476-131">To fix this error, do not define this property.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="09476-132">La voce RemoveIniFile Remove1 deve avere un valore, perché l'azione è "Delete tag" (4).</span><span class="sxs-lookup"><span data-stu-id="09476-132">RemoveIniFile entry Remove1 must have a value, because the Action is "Delete Tag" (4).</span></span>                | <span data-ttu-id="09476-133">È presente un'azione Elimina tag nella colonna RemoveIniFile della [tabella RemoveIniFile](removeinifile-table.md) senza specificare un tag da eliminare nella colonna valore.</span><span class="sxs-lookup"><span data-stu-id="09476-133">There is a Delete Tag action in the in the RemoveIniFile column of the [RemoveIniFile table](removeinifile-table.md) without specifying a tag to delete in the Value column.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="09476-134">Tabella degli errori mancante.</span><span class="sxs-lookup"><span data-stu-id="09476-134">Error Table is missing.</span></span> <span data-ttu-id="09476-135">Verranno generati solo i messaggi di errore numerici.</span><span class="sxs-lookup"><span data-stu-id="09476-135">Only numerical error messages will be generated.</span></span>                              | <span data-ttu-id="09476-136">Questo avviso di ghiaccio è obsoleto perché per Windows Installer non è necessario che il pacchetto includa una [tabella degli errori](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="09476-136">This ICE warning is obsolete because Windows Installer does not require the package to have an [Error table](error-table.md).</span></span> <span data-ttu-id="09476-137">È possibile recuperare i messaggi di errore utilizzando Msimsg.dll.</span><span class="sxs-lookup"><span data-stu-id="09476-137">Error messages can be retrieved using Msimsg.dll.</span></span><br/> <span data-ttu-id="09476-138">Questo avviso indica che nel file con estensione msi manca la [tabella degli errori](error-table.md) e che la proprietà di [**Riepilogo dei conteggi delle pagine**](page-count-summary.md) è minore o uguale a 100.</span><span class="sxs-lookup"><span data-stu-id="09476-138">This warning means that the .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <br/> <span data-ttu-id="09476-139">Per correggere l'errore, utilizzare una versione corrente del Windows Installer oppure aggiungere una tabella degli errori al pacchetto di installazione e creare modelli di formattazione nella colonna messaggio per i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="09476-139">To fix this error, use a current version of the Windows Installer, or add an Error table to the installation package and author formatting templates in the Message column for error messages.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="09476-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09476-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09476-141">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="09476-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




