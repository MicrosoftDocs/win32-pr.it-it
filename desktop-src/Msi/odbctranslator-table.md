---
description: Nella tabella ODBCTranslator sono elencati i convertitori ODBC che appartengono all'installazione.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Tabella ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319002"
---
# <a name="odbctranslator-table"></a><span data-ttu-id="b3b3a-103">Tabella ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="b3b3a-103">ODBCTranslator Table</span></span>

<span data-ttu-id="b3b3a-104">Nella tabella ODBCTranslator sono elencati i convertitori ODBC che appartengono all'installazione.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-104">The ODBCTranslator table lists the ODBC translators belonging to the installation.</span></span>

<span data-ttu-id="b3b3a-105">La tabella ODBCTranslator include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-105">The ODBCTranslator table has the following columns.</span></span>



| <span data-ttu-id="b3b3a-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="b3b3a-106">Column</span></span>      | <span data-ttu-id="b3b3a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3b3a-107">Type</span></span>                         | <span data-ttu-id="b3b3a-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="b3b3a-108">Key</span></span> | <span data-ttu-id="b3b3a-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b3b3a-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="b3b3a-110">Traduttore</span><span class="sxs-lookup"><span data-stu-id="b3b3a-110">Translator</span></span>  | [<span data-ttu-id="b3b3a-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="b3b3a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b3b3a-112">S</span><span class="sxs-lookup"><span data-stu-id="b3b3a-112">Y</span></span>   | <span data-ttu-id="b3b3a-113">N</span><span class="sxs-lookup"><span data-stu-id="b3b3a-113">N</span></span>        |
| <span data-ttu-id="b3b3a-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b3b3a-114">Component\_</span></span> | [<span data-ttu-id="b3b3a-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="b3b3a-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="b3b3a-116">N</span><span class="sxs-lookup"><span data-stu-id="b3b3a-116">N</span></span>   | <span data-ttu-id="b3b3a-117">N</span><span class="sxs-lookup"><span data-stu-id="b3b3a-117">N</span></span>        |
| <span data-ttu-id="b3b3a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3b3a-118">Description</span></span> | [<span data-ttu-id="b3b3a-119">Text</span><span class="sxs-lookup"><span data-stu-id="b3b3a-119">Text</span></span>](text.md)             | <span data-ttu-id="b3b3a-120">N</span><span class="sxs-lookup"><span data-stu-id="b3b3a-120">N</span></span>   | <span data-ttu-id="b3b3a-121">N</span><span class="sxs-lookup"><span data-stu-id="b3b3a-121">N</span></span>        |
| <span data-ttu-id="b3b3a-122">file\_</span><span class="sxs-lookup"><span data-stu-id="b3b3a-122">File\_</span></span>      | [<span data-ttu-id="b3b3a-123">Identificatore</span><span class="sxs-lookup"><span data-stu-id="b3b3a-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="b3b3a-124">N</span><span class="sxs-lookup"><span data-stu-id="b3b3a-124">N</span></span>   | <span data-ttu-id="b3b3a-125">N</span><span class="sxs-lookup"><span data-stu-id="b3b3a-125">N</span></span>        |
| <span data-ttu-id="b3b3a-126">\_Installazione file</span><span class="sxs-lookup"><span data-stu-id="b3b3a-126">File\_Setup</span></span> | [<span data-ttu-id="b3b3a-127">Identificatore</span><span class="sxs-lookup"><span data-stu-id="b3b3a-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="b3b3a-128">N</span><span class="sxs-lookup"><span data-stu-id="b3b3a-128">N</span></span>   | <span data-ttu-id="b3b3a-129">S</span><span class="sxs-lookup"><span data-stu-id="b3b3a-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b3b3a-130">Colonne</span><span class="sxs-lookup"><span data-stu-id="b3b3a-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b3b3a-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span><span class="sxs-lookup"><span data-stu-id="b3b3a-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span></span>
</dt> <dd>

<span data-ttu-id="b3b3a-132">Nome del token interno per Translator.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-132">Internal token name for translator.</span></span> <span data-ttu-id="b3b3a-133">Chiave primaria per la tabella.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="b3b3a-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="b3b3a-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="b3b3a-135">Chiave esterna nella tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="b3b3a-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3b3a-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="b3b3a-137">Descrizione registrata per questo convertitore di driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-137">The description registered for this ODBC driver translator.</span></span> <span data-ttu-id="b3b3a-138">Questo valore non può essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="b3b3a-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="b3b3a-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="b3b3a-140">File DLL per il trasferimento elencato nella colonna Translator.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-140">The DLL file for the transfer listed in the Translator column.</span></span> <span data-ttu-id="b3b3a-141">La \_ colonna file è una chiave esterna nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="b3b3a-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="b3b3a-142">Il nome file immesso nella colonna FileName del record della tabella file deve essere nel formato di file breve.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="b3b3a-143">\|Impossibile utilizzare la sintassi LFN di SFN.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="b3b3a-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Installazione file</span><span class="sxs-lookup"><span data-stu-id="b3b3a-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="b3b3a-145">Il file DLL di installazione per il traduttore se è diverso dalla colonna Translator.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-145">The setup DLL file for the translator if it is different from the Translator column.</span></span> <span data-ttu-id="b3b3a-146">La \_ colonna file è una chiave esterna nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="b3b3a-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="b3b3a-147">Il nome file immesso nella colonna FileName del record della tabella file deve essere nel formato di file breve.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="b3b3a-148">\|Impossibile utilizzare la sintassi LFN di SFN.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3b3a-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3b3a-149">Remarks</span></span>

<span data-ttu-id="b3b3a-150">Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="b3b3a-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="b3b3a-151">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b3b3a-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="b3b3a-152">Convalida</span><span class="sxs-lookup"><span data-stu-id="b3b3a-152">Validation</span></span>

<dl>

[<span data-ttu-id="b3b3a-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="b3b3a-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b3b3a-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="b3b3a-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b3b3a-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="b3b3a-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



