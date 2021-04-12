---
description: Msival2.exe è un'utilità della riga di comando in grado di eseguire una suite di analizzatori di coerenza interni (CIEM).
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234035"
---
# <a name="msival2exe"></a><span data-ttu-id="86474-103">Msival2.exe</span><span class="sxs-lookup"><span data-stu-id="86474-103">Msival2.exe</span></span>

<span data-ttu-id="86474-104">Msival2.exe è un'utilità della riga di comando in grado di eseguire una suite di [analizzatori di coerenza interni (CIEM](internal-consistency-evaluators-ices.md)).</span><span class="sxs-lookup"><span data-stu-id="86474-104">Msival2.exe is a command line utility that can run a suite of [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="86474-105">Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="86474-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="86474-106">Per ulteriori informazioni su CIEM e il file CUB, vedere [utilizzo di analizzatori di coerenza interni](using-internal-consistency-evaluators.md).</span><span class="sxs-lookup"><span data-stu-id="86474-106">For more information about ICEs and the CUB file, see [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86474-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86474-107">Syntax</span></span>

<span data-ttu-id="86474-108">**MSIVal2** *{database} {cub file} \[ -f \] \[ -l {logfile} \] \[ -i {ID ghiaccio} \[ : {Ice ID}... \] \]*</span><span class="sxs-lookup"><span data-stu-id="86474-108">**Msival2** *{database}{CUB file}\[-f\]\[-l {logfile}\]\[-i {ICE Id}\[:{ICE Id}...\]\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="86474-109">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="86474-109">Command Line Options</span></span>

<span data-ttu-id="86474-110">Msival2.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="86474-110">Msival2.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="86474-111">Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.</span><span class="sxs-lookup"><span data-stu-id="86474-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="86474-112">Opzione</span><span class="sxs-lookup"><span data-stu-id="86474-112">Option</span></span> | <span data-ttu-id="86474-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86474-113">Description</span></span>                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86474-114">-f</span><span class="sxs-lookup"><span data-stu-id="86474-114">-f</span></span>     | <span data-ttu-id="86474-115">Filtrare tutti i messaggi informativi dai risultati visualizzati.</span><span class="sxs-lookup"><span data-stu-id="86474-115">Filter out all informational messages from the displayed results.</span></span> <span data-ttu-id="86474-116">Vengono visualizzati tutti gli altri tipi di messaggi.</span><span class="sxs-lookup"><span data-stu-id="86474-116">All other types of messages are displayed.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="86474-117">-i</span><span class="sxs-lookup"><span data-stu-id="86474-117">-i</span></span>     | <span data-ttu-id="86474-118">Eseguire solo i ghiacci elencati nella riga di comando nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="86474-118">Run only the ICEs listed on the command line in the order specified.</span></span> <span data-ttu-id="86474-119">Ogni azione personalizzata ICE dovrebbe essere elencata come appare nella [tabella CustomAction](customaction-table.md) del file cub.</span><span class="sxs-lookup"><span data-stu-id="86474-119">Each ICE custom action should be listed as it appears in the [CustomAction table](customaction-table.md) of the CUB file.</span></span> <span data-ttu-id="86474-120">Se questa opzione viene omessa, lo strumento esegue il set predefinito di file di base (CIEM) specificato dall'autore del file CUB.</span><span class="sxs-lookup"><span data-stu-id="86474-120">If this option is omitted, the tool runs the default set of ICEs specified by the author of the CUB file.</span></span> |
| <span data-ttu-id="86474-121">-l</span><span class="sxs-lookup"><span data-stu-id="86474-121">-l</span></span>     | <span data-ttu-id="86474-122">Scrive i risultati nel file specificato.</span><span class="sxs-lookup"><span data-stu-id="86474-122">Write results to the specified file.</span></span> <span data-ttu-id="86474-123">Il file non deve essere già esistente.</span><span class="sxs-lookup"><span data-stu-id="86474-123">The file must not already exist.</span></span> <span data-ttu-id="86474-124">Se il file esiste, non verrà sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="86474-124">If the file exists, it is not overwritten.</span></span>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="86474-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86474-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86474-126">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="86474-126">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="86474-127">Analizzatori di coerenza interni-CIEM</span><span class="sxs-lookup"><span data-stu-id="86474-127">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
</dt> <dt>

[<span data-ttu-id="86474-128">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="86474-128">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



