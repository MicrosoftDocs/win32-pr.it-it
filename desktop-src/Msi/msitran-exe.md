---
description: Msitran.exe USA MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo e MsiDatabaseApplyTransform per generare o applicare un file di trasformazione. Questo strumento è disponibile solo nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316257"
---
# <a name="msitranexe"></a><span data-ttu-id="3c77c-103">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="3c77c-103">Msitran.exe</span></span>

<span data-ttu-id="3c77c-104">Msitran.exe USA [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)e [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) per generare o applicare un file di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="3c77c-104">Msitran.exe uses [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa), and [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) to generate or apply a transform file.</span></span>

<span data-ttu-id="3c77c-105">Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="3c77c-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c77c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c77c-106">Syntax</span></span>

<span data-ttu-id="3c77c-107">Utilizzare la sintassi seguente per generare una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="3c77c-107">Use the following syntax to generate a transform.</span></span>

<span data-ttu-id="3c77c-108">**MSITran-g** *{base DB} {Ref DB} {nome file di trasformazione} \[ {condizioni di errore/condizioni \] di convalida}*</span><span class="sxs-lookup"><span data-stu-id="3c77c-108">**msitran -g** *{base db}{ref db}{transform file name}\[{error conditions / validation conditions}\]*</span></span>

<span data-ttu-id="3c77c-109">Utilizzare la sintassi seguente per applicare una trasformazione</span><span class="sxs-lookup"><span data-stu-id="3c77c-109">Use the following syntax to apply a transform</span></span>

<span data-ttu-id="3c77c-110">**MSITran-a** *{Transform} {database} \[ {condizioni di errore \] }*</span><span class="sxs-lookup"><span data-stu-id="3c77c-110">**msitran -a** *{transform}{database}\[{error conditions}\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="3c77c-111">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="3c77c-111">Command Line Options</span></span>

<span data-ttu-id="3c77c-112">Msitran.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3c77c-112">Msitran.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="3c77c-113">Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.</span><span class="sxs-lookup"><span data-stu-id="3c77c-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="3c77c-114">Opzione</span><span class="sxs-lookup"><span data-stu-id="3c77c-114">Option</span></span> | <span data-ttu-id="3c77c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c77c-115">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="3c77c-116">-g</span><span class="sxs-lookup"><span data-stu-id="3c77c-116">-g</span></span>     | <span data-ttu-id="3c77c-117">Generazione della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="3c77c-117">Transform generation.</span></span>  |
| <span data-ttu-id="3c77c-118">-a</span><span class="sxs-lookup"><span data-stu-id="3c77c-118">-a</span></span>     | <span data-ttu-id="3c77c-119">Trasforma applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c77c-119">Transform application.</span></span> |



 

<span data-ttu-id="3c77c-120">Quando si applica una trasformazione, è possibile che vengano eliminati gli errori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3c77c-120">The following errors may be suppressed when applying a transform.</span></span> <span data-ttu-id="3c77c-121">Per non visualizzare un errore, includere il carattere appropriato nell'argomento {error conditions}.</span><span class="sxs-lookup"><span data-stu-id="3c77c-121">To suppress an error, include the appropriate character in the {error conditions} argument.</span></span> <span data-ttu-id="3c77c-122">Le condizioni specificate con-g vengono inserite nelle informazioni di riepilogo della trasformazione, ma non vengono utilizzate quando si applica una trasformazione con-a.</span><span class="sxs-lookup"><span data-stu-id="3c77c-122">Conditions specified with -g are placed in the summary information of the transform, but are not used when applying a transform with -a.</span></span> <span data-ttu-id="3c77c-123">Per informazioni, vedere [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span><span class="sxs-lookup"><span data-stu-id="3c77c-123">For information, see [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span></span>



| <span data-ttu-id="3c77c-124">Opzione</span><span class="sxs-lookup"><span data-stu-id="3c77c-124">Option</span></span> | <span data-ttu-id="3c77c-125">Errore eliminato</span><span class="sxs-lookup"><span data-stu-id="3c77c-125">Suppressed error</span></span>           |
|--------|----------------------------|
| <span data-ttu-id="3c77c-126">a</span><span class="sxs-lookup"><span data-stu-id="3c77c-126">a</span></span>      | <span data-ttu-id="3c77c-127">Aggiungi riga esistente.</span><span class="sxs-lookup"><span data-stu-id="3c77c-127">Add existing row.</span></span>          |
| <span data-ttu-id="3c77c-128">b</span><span class="sxs-lookup"><span data-stu-id="3c77c-128">b</span></span>      | <span data-ttu-id="3c77c-129">Elimina la riga non esistente.</span><span class="sxs-lookup"><span data-stu-id="3c77c-129">Delete non-existing row.</span></span>   |
| <span data-ttu-id="3c77c-130">c</span><span class="sxs-lookup"><span data-stu-id="3c77c-130">c</span></span>      | <span data-ttu-id="3c77c-131">Aggiungere una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="3c77c-131">Add existing table.</span></span>        |
| <span data-ttu-id="3c77c-132">d</span><span class="sxs-lookup"><span data-stu-id="3c77c-132">d</span></span>      | <span data-ttu-id="3c77c-133">Elimina la tabella non esistente.</span><span class="sxs-lookup"><span data-stu-id="3c77c-133">Delete non-existing table.</span></span> |
| <span data-ttu-id="3c77c-134">h</span><span class="sxs-lookup"><span data-stu-id="3c77c-134">e</span></span>      | <span data-ttu-id="3c77c-135">Modificare la riga esistente.</span><span class="sxs-lookup"><span data-stu-id="3c77c-135">Modify existing row.</span></span>       |
| <span data-ttu-id="3c77c-136">f</span><span class="sxs-lookup"><span data-stu-id="3c77c-136">f</span></span>      | <span data-ttu-id="3c77c-137">Modificare la tabella codici.</span><span class="sxs-lookup"><span data-stu-id="3c77c-137">Change codepage.</span></span>           |



 

<span data-ttu-id="3c77c-138">Le condizioni di convalida seguenti possono essere utilizzate per indicare quando una trasformazione può essere applicata a un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3c77c-138">The following validation conditions may be used to indicate when a transform may be applied to a package.</span></span> <span data-ttu-id="3c77c-139">Queste condizioni possono essere specificate con-g, ma non con-a.</span><span class="sxs-lookup"><span data-stu-id="3c77c-139">These conditions may be specified with -g, but not -a.</span></span>



| <span data-ttu-id="3c77c-140">Opzione</span><span class="sxs-lookup"><span data-stu-id="3c77c-140">Option</span></span> | <span data-ttu-id="3c77c-141">Condizione di convalida</span><span class="sxs-lookup"><span data-stu-id="3c77c-141">Validation condition</span></span>                                  |
|--------|-------------------------------------------------------|
| <span data-ttu-id="3c77c-142">g</span><span class="sxs-lookup"><span data-stu-id="3c77c-142">g</span></span>      | <span data-ttu-id="3c77c-143">Controllare il codice di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c77c-143">Check upgrade code.</span></span>                                   |
| <span data-ttu-id="3c77c-144">l</span><span class="sxs-lookup"><span data-stu-id="3c77c-144">l</span></span>      | <span data-ttu-id="3c77c-145">Controllare la lingua.</span><span class="sxs-lookup"><span data-stu-id="3c77c-145">Check language.</span></span>                                       |
| <span data-ttu-id="3c77c-146">p</span><span class="sxs-lookup"><span data-stu-id="3c77c-146">p</span></span>      | <span data-ttu-id="3c77c-147">Controllare la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="3c77c-147">Check platform.</span></span>                                       |
| <span data-ttu-id="3c77c-148">r</span><span class="sxs-lookup"><span data-stu-id="3c77c-148">r</span></span>      | <span data-ttu-id="3c77c-149">Verificare il prodotto.</span><span class="sxs-lookup"><span data-stu-id="3c77c-149">Check product.</span></span>                                        |
| <span data-ttu-id="3c77c-150">s</span><span class="sxs-lookup"><span data-stu-id="3c77c-150">s</span></span>      | <span data-ttu-id="3c77c-151">Controllare solo la versione principale.</span><span class="sxs-lookup"><span data-stu-id="3c77c-151">Check major version only.</span></span>                             |
| <span data-ttu-id="3c77c-152">u</span><span class="sxs-lookup"><span data-stu-id="3c77c-152">t</span></span>      | <span data-ttu-id="3c77c-153">Controllare solo le versioni principale e secondaria.</span><span class="sxs-lookup"><span data-stu-id="3c77c-153">Check major and minor versions only.</span></span>                  |
| <span data-ttu-id="3c77c-154">u</span><span class="sxs-lookup"><span data-stu-id="3c77c-154">u</span></span>      | <span data-ttu-id="3c77c-155">Controllare le versioni principale, secondaria e di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c77c-155">Check major, minor, and upgrade versions.</span></span>             |
| <span data-ttu-id="3c77c-156">v</span><span class="sxs-lookup"><span data-stu-id="3c77c-156">v</span></span>      | <span data-ttu-id="3c77c-157">Versione del database applicata < versione del database di base.</span><span class="sxs-lookup"><span data-stu-id="3c77c-157">Applied database version < Base database version.</span></span>  |
| <span data-ttu-id="3c77c-158">w</span><span class="sxs-lookup"><span data-stu-id="3c77c-158">w</span></span>      | <span data-ttu-id="3c77c-159">Versione del database applicata <= versione del database di base.</span><span class="sxs-lookup"><span data-stu-id="3c77c-159">Applied database version <= Base database version.</span></span> |
| <span data-ttu-id="3c77c-160">x</span><span class="sxs-lookup"><span data-stu-id="3c77c-160">x</span></span>      | <span data-ttu-id="3c77c-161">Versione del database applicata = versione del database di base.</span><span class="sxs-lookup"><span data-stu-id="3c77c-161">Applied database version = Base database version.</span></span>     |
| <span data-ttu-id="3c77c-162">y</span><span class="sxs-lookup"><span data-stu-id="3c77c-162">y</span></span>      | <span data-ttu-id="3c77c-163">Versione del database applicata >= versione del database di base.</span><span class="sxs-lookup"><span data-stu-id="3c77c-163">Applied database version >= Base database version.</span></span> |
| <span data-ttu-id="3c77c-164">z</span><span class="sxs-lookup"><span data-stu-id="3c77c-164">z</span></span>      | <span data-ttu-id="3c77c-165">Versione del database applicata > versione del database di base.</span><span class="sxs-lookup"><span data-stu-id="3c77c-165">Applied database version > Base database version.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="3c77c-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c77c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c77c-167">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3c77c-167">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="3c77c-168">Trasformazioni di database</span><span class="sxs-lookup"><span data-stu-id="3c77c-168">Database Transforms</span></span>](database-transforms.md)
</dt> <dt>

[<span data-ttu-id="3c77c-169">Esempio di trasformazione della personalizzazione</span><span class="sxs-lookup"><span data-stu-id="3c77c-169">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> <dt>

[<span data-ttu-id="3c77c-170">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="3c77c-170">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



