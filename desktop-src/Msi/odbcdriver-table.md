---
description: La tabella ODBCDriver elenca i driver ODBC che appartengono all'installazione.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabella ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525782"
---
# <a name="odbcdriver-table"></a><span data-ttu-id="9adad-103">Tabella ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="9adad-103">ODBCDriver Table</span></span>

<span data-ttu-id="9adad-104">La tabella ODBCDriver elenca i driver ODBC che appartengono all'installazione.</span><span class="sxs-lookup"><span data-stu-id="9adad-104">The ODBCDriver table lists the ODBC drivers belonging to the installation.</span></span>

<span data-ttu-id="9adad-105">La tabella ODBCDriver include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="9adad-105">The ODBCDriver table has the following columns.</span></span>



| <span data-ttu-id="9adad-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="9adad-106">Column</span></span>      | <span data-ttu-id="9adad-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="9adad-107">Type</span></span>                         | <span data-ttu-id="9adad-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="9adad-108">Key</span></span> | <span data-ttu-id="9adad-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="9adad-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="9adad-110">Driver</span><span class="sxs-lookup"><span data-stu-id="9adad-110">Driver</span></span>      | [<span data-ttu-id="9adad-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9adad-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="9adad-112">S</span><span class="sxs-lookup"><span data-stu-id="9adad-112">Y</span></span>   | <span data-ttu-id="9adad-113">N</span><span class="sxs-lookup"><span data-stu-id="9adad-113">N</span></span>        |
| <span data-ttu-id="9adad-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="9adad-114">Component\_</span></span> | [<span data-ttu-id="9adad-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9adad-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="9adad-116">N</span><span class="sxs-lookup"><span data-stu-id="9adad-116">N</span></span>   | <span data-ttu-id="9adad-117">N</span><span class="sxs-lookup"><span data-stu-id="9adad-117">N</span></span>        |
| <span data-ttu-id="9adad-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9adad-118">Description</span></span> | [<span data-ttu-id="9adad-119">Text</span><span class="sxs-lookup"><span data-stu-id="9adad-119">Text</span></span>](text.md)             | <span data-ttu-id="9adad-120">N</span><span class="sxs-lookup"><span data-stu-id="9adad-120">N</span></span>   | <span data-ttu-id="9adad-121">N</span><span class="sxs-lookup"><span data-stu-id="9adad-121">N</span></span>        |
| <span data-ttu-id="9adad-122">file\_</span><span class="sxs-lookup"><span data-stu-id="9adad-122">File\_</span></span>      | [<span data-ttu-id="9adad-123">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9adad-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="9adad-124">N</span><span class="sxs-lookup"><span data-stu-id="9adad-124">N</span></span>   | <span data-ttu-id="9adad-125">N</span><span class="sxs-lookup"><span data-stu-id="9adad-125">N</span></span>        |
| <span data-ttu-id="9adad-126">\_Installazione file</span><span class="sxs-lookup"><span data-stu-id="9adad-126">File\_Setup</span></span> | [<span data-ttu-id="9adad-127">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9adad-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="9adad-128">N</span><span class="sxs-lookup"><span data-stu-id="9adad-128">N</span></span>   | <span data-ttu-id="9adad-129">S</span><span class="sxs-lookup"><span data-stu-id="9adad-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9adad-130">Colonne</span><span class="sxs-lookup"><span data-stu-id="9adad-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9adad-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span><span class="sxs-lookup"><span data-stu-id="9adad-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span></span>
</dt> <dd>

<span data-ttu-id="9adad-132">Nome del token interno per il driver.</span><span class="sxs-lookup"><span data-stu-id="9adad-132">Internal token name for driver.</span></span> <span data-ttu-id="9adad-133">Chiave primaria per la tabella</span><span class="sxs-lookup"><span data-stu-id="9adad-133">A primary key for the table</span></span>

</dd> <dt>

<span data-ttu-id="9adad-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="9adad-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="9adad-135">Chiave esterna nella tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="9adad-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="9adad-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="9adad-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="9adad-137">Descrizione registrata per il driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="9adad-137">The description registered for this ODBC driver.</span></span> <span data-ttu-id="9adad-138">Questo valore non può essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="9adad-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="9adad-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="9adad-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="9adad-140">File DLL per i driver elencati nella colonna driver.</span><span class="sxs-lookup"><span data-stu-id="9adad-140">The DLL file for drivers listed in the Driver column.</span></span> <span data-ttu-id="9adad-141">La \_ colonna file è una chiave esterna nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="9adad-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="9adad-142">Il nome file immesso nella colonna FileName del record della tabella file deve essere nel formato di file breve.</span><span class="sxs-lookup"><span data-stu-id="9adad-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="9adad-143">\|Impossibile utilizzare la sintassi LFN di SFN.</span><span class="sxs-lookup"><span data-stu-id="9adad-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="9adad-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Installazione file</span><span class="sxs-lookup"><span data-stu-id="9adad-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="9adad-145">Il file DLL di installazione del driver se è diverso dal driver.</span><span class="sxs-lookup"><span data-stu-id="9adad-145">The setup DLL file for the driver if it is different than from Driver.</span></span> <span data-ttu-id="9adad-146">La \_ colonna file è una chiave esterna nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="9adad-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="9adad-147">Il nome file immesso nella colonna FileName del record della tabella file deve essere nel formato di file breve.</span><span class="sxs-lookup"><span data-stu-id="9adad-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="9adad-148">\|Impossibile utilizzare la sintassi LFN di SFN.</span><span class="sxs-lookup"><span data-stu-id="9adad-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9adad-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="9adad-149">Remarks</span></span>

<span data-ttu-id="9adad-150">Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="9adad-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="9adad-151">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9adad-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="9adad-152">Convalida</span><span class="sxs-lookup"><span data-stu-id="9adad-152">Validation</span></span>

<dl>

[<span data-ttu-id="9adad-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="9adad-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9adad-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="9adad-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9adad-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="9adad-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



