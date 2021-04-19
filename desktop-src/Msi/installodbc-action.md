---
description: L'azione InstallODBC installa driver, traduttori e origini dati nella tabella ODBCDriver, nella tabella ODBCTranslator e nella tabella ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Azione InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317757"
---
# <a name="installodbc-action"></a><span data-ttu-id="2501d-103">Azione InstallODBC</span><span class="sxs-lookup"><span data-stu-id="2501d-103">InstallODBC Action</span></span>

<span data-ttu-id="2501d-104">L'azione InstallODBC installa driver, traduttori e origini dati nella tabella [ODBCDriver](odbcdriver-table.md), nella tabella [ODBCTranslator](odbctranslator-table.md)e nella [tabella ODBCDataSource](odbcdatasource-table.md).</span><span class="sxs-lookup"><span data-stu-id="2501d-104">The InstallODBC action installs the drivers, translators, and data sources in the [ODBCDriver Table](odbcdriver-table.md), [ODBCTranslator Table](odbctranslator-table.md), and [ODBCDataSource Table](odbcdatasource-table.md).</span></span> <span data-ttu-id="2501d-105">Se un driver o un convertitore esiste già, l'azione InstallODBC esegue le chiamate SQL necessarie per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="2501d-105">If a driver or translator already exists, the InstallODBC action makes SQL calls necessary for the installation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2501d-106">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="2501d-106">Sequence Restrictions</span></span>

<span data-ttu-id="2501d-107">L'azione InstallODBC non copia o rimuove i file e deve essere eseguita in seguito a azioni che copiano o rimuovono i file.</span><span class="sxs-lookup"><span data-stu-id="2501d-107">The InstallODBC action does not copy or remove files, and must be after actions that copy or remove files.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2501d-108">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="2501d-108">ActionData Messages</span></span>

<span data-ttu-id="2501d-109">Nella tabella seguente vengono identificati i messaggi ActionData per ogni driver installato.</span><span class="sxs-lookup"><span data-stu-id="2501d-109">The following table identifies the ActionData messages for each installed driver.</span></span>



| <span data-ttu-id="2501d-110">Campo</span><span class="sxs-lookup"><span data-stu-id="2501d-110">Field</span></span>       | <span data-ttu-id="2501d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2501d-111">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="2501d-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2501d-112">\[1\]</span></span>       | <span data-ttu-id="2501d-113">Descrizione del driver.</span><span class="sxs-lookup"><span data-stu-id="2501d-113">Driver description.</span></span> <span data-ttu-id="2501d-114">Chiave del driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="2501d-114">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="2501d-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2501d-115">\[2\]</span></span>       | <span data-ttu-id="2501d-116">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="2501d-116">ComponentId.</span></span>                                                             |
| <span data-ttu-id="2501d-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="2501d-117">\[3\]</span></span>       | <span data-ttu-id="2501d-118">cartella.</span><span class="sxs-lookup"><span data-stu-id="2501d-118">Folder.</span></span>                                                                  |
| <span data-ttu-id="2501d-119">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="2501d-119">\[4, 5, …\]</span></span> | <span data-ttu-id="2501d-120">Coppie di attributi e valori da [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="2501d-120">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="2501d-121">Nella tabella seguente vengono identificati i messaggi ActionData per ogni traduttore installato.</span><span class="sxs-lookup"><span data-stu-id="2501d-121">The following table identifies the ActionData messages for each installed translator.</span></span>



| <span data-ttu-id="2501d-122">Campo</span><span class="sxs-lookup"><span data-stu-id="2501d-122">Field</span></span>       | <span data-ttu-id="2501d-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2501d-123">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="2501d-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2501d-124">\[1\]</span></span>       | <span data-ttu-id="2501d-125">Descrizione del driver.</span><span class="sxs-lookup"><span data-stu-id="2501d-125">Driver description.</span></span> <span data-ttu-id="2501d-126">Chiave del driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="2501d-126">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="2501d-127">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2501d-127">\[2\]</span></span>       | <span data-ttu-id="2501d-128">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="2501d-128">ComponentId.</span></span>                                                             |
| <span data-ttu-id="2501d-129">\[3\]</span><span class="sxs-lookup"><span data-stu-id="2501d-129">\[3\]</span></span>       | <span data-ttu-id="2501d-130">cartella.</span><span class="sxs-lookup"><span data-stu-id="2501d-130">Folder.</span></span>                                                                  |
| <span data-ttu-id="2501d-131">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="2501d-131">\[4, 5, …\]</span></span> | <span data-ttu-id="2501d-132">Coppie di attributi e valori da [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="2501d-132">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="2501d-133">Nella tabella seguente vengono identificati i messaggi ActionData per ogni origine dati installata.</span><span class="sxs-lookup"><span data-stu-id="2501d-133">The following table identifies the ActionData messages for each installed data source.</span></span>



| <span data-ttu-id="2501d-134">Campo</span><span class="sxs-lookup"><span data-stu-id="2501d-134">Field</span></span>       | <span data-ttu-id="2501d-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2501d-135">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="2501d-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2501d-136">\[1\]</span></span>       | <span data-ttu-id="2501d-137">Descrizione del driver.</span><span class="sxs-lookup"><span data-stu-id="2501d-137">Driver description.</span></span> <span data-ttu-id="2501d-138">Chiave del driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="2501d-138">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="2501d-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2501d-139">\[2\]</span></span>       | <span data-ttu-id="2501d-140">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="2501d-140">ComponentId.</span></span>                                                             |
| <span data-ttu-id="2501d-141">\[3\]</span><span class="sxs-lookup"><span data-stu-id="2501d-141">\[3\]</span></span>       | <span data-ttu-id="2501d-142">Registrazione: ODBC \_ Add \_ DSN o ODBC \_ Add \_ sys \_ DSN.</span><span class="sxs-lookup"><span data-stu-id="2501d-142">Registration: ODBC\_ADD\_DSN or ODBC\_ADD\_SYS\_DSN.</span></span>                     |
| <span data-ttu-id="2501d-143">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="2501d-143">\[4, 5, …\]</span></span> | <span data-ttu-id="2501d-144">Coppie di attributi e valori da [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="2501d-144">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2501d-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="2501d-145">Remarks</span></span>

<span data-ttu-id="2501d-146">È necessario che Gestione driver ODBC sia stato creato nel pacchetto di Microsoft Installer e che sia incluso un componente denominato ODBCDriverManager.</span><span class="sxs-lookup"><span data-stu-id="2501d-146">The ODBC Driver Manager must be authored in the Microsoft Installer package and a component named ODBCDriverManager must be included.</span></span> <span data-ttu-id="2501d-147">Se necessario, il gestore viene installato.</span><span class="sxs-lookup"><span data-stu-id="2501d-147">The manager is installed if necessary.</span></span>

<span data-ttu-id="2501d-148">Per rinominare il componente, impostare una proprietà denominata ODBCDriverManager sul nuovo nome del componente.</span><span class="sxs-lookup"><span data-stu-id="2501d-148">To rename the component, set a property named ODBCDriverManager to the new name of the component.</span></span> <span data-ttu-id="2501d-149">Se è necessario installare una gestione driver ODBC a 64 bit, il componente che lo trasporta dovrebbe essere denominato ODBCDriverManager64.</span><span class="sxs-lookup"><span data-stu-id="2501d-149">If a 64-bit ODBC Driver Manager is to be installed, the component that carries it should be named ODBCDriverManager64.</span></span>

-   <span data-ttu-id="2501d-150">L'azione InstallODBC esegue una query sulla [tabella ODBCDataSource](odbcdatasource-table.md) e sulla [tabella ODBCSourceAttribute](odbcsourceattribute-table.md) per ogni origine dati da installare e sugli attributi dell'origine dati.</span><span class="sxs-lookup"><span data-stu-id="2501d-150">The InstallODBC action queries the [ODBCDataSource Table](odbcdatasource-table.md) and the [ODBCSourceAttribute Table](odbcsourceattribute-table.md) for each data source to be installed, and the attributes of the data source.</span></span>
-   <span data-ttu-id="2501d-151">L'azione InstallODBC esegue una query sulla [tabella ODBCDriver](odbcdriver-table.md) e sulla [tabella ODBCTranslator](odbctranslator-table.md) per ogni driver e convertitore selezionato per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="2501d-151">The InstallODBC action queries the [ODBCDriver Table](odbcdriver-table.md) and the [ODBCTranslator Table](odbctranslator-table.md) for each driver and translator that is selected for installation.</span></span>
-   <span data-ttu-id="2501d-152">L'azione InstallODBC esegue una query sulla [tabella ODBCAttribute](odbcattribute-table.md) per gli attributi dei driver e dei convertitori.</span><span class="sxs-lookup"><span data-stu-id="2501d-152">The InstallODBC action queries the [ODBCAttribute Table](odbcattribute-table.md) for the attributes of the drivers and translators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2501d-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2501d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2501d-154">Esempi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2501d-154">Windows Installer Examples</span></span>](windows-installer-examples.md)
</dt> </dl>

 

 



