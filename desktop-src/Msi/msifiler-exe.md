---
description: MsiFiler.exe popola la tabella dei file con le versioni, le lingue e le dimensioni dei file basate su una directory di origine. Consente inoltre di aggiornare la tabella MsiFileHash con gli hash di file.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306576"
---
# <a name="msifilerexe"></a><span data-ttu-id="0e3da-104">Msifiler.exe</span><span class="sxs-lookup"><span data-stu-id="0e3da-104">Msifiler.exe</span></span>

<span data-ttu-id="0e3da-105">MsiFiler.exe popola la [tabella dei file](file-table.md) con le versioni, le lingue e le dimensioni dei file basate su una directory di origine.</span><span class="sxs-lookup"><span data-stu-id="0e3da-105">MsiFiler.exe populates the [File table](file-table.md) with file versions, languages, and sizes based upon a source directory.</span></span> <span data-ttu-id="0e3da-106">Consente inoltre di aggiornare la [tabella MsiFileHash](msifilehash-table.md) con gli hash di file.</span><span class="sxs-lookup"><span data-stu-id="0e3da-106">It can also update the [MsiFileHash table](msifilehash-table.md) with file hashes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e3da-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e3da-107">Syntax</span></span>

<span data-ttu-id="0e3da-108">**msifiler.exe-d** *{database}* **\[ -v \] \[ -h \] \[ -s ALTSOURCE \]**</span><span class="sxs-lookup"><span data-stu-id="0e3da-108">**msifiler.exe -d** *{database}* **\[-v\] \[-h\] \[-s ALTSOURCE\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="0e3da-109">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="0e3da-109">Command Line Options</span></span>

<span data-ttu-id="0e3da-110">Msifiler.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0e3da-110">Msifiler.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="0e3da-111">Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.</span><span class="sxs-lookup"><span data-stu-id="0e3da-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="0e3da-112">Opzione</span><span class="sxs-lookup"><span data-stu-id="0e3da-112">Option</span></span> | <span data-ttu-id="0e3da-113">Parametro</span><span class="sxs-lookup"><span data-stu-id="0e3da-113">Parameter</span></span>   | <span data-ttu-id="0e3da-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e3da-114">Description</span></span>                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3da-115">-d</span><span class="sxs-lookup"><span data-stu-id="0e3da-115">-d</span></span>     | <span data-ttu-id="0e3da-116">*database*</span><span class="sxs-lookup"><span data-stu-id="0e3da-116">*database*</span></span>  | <span data-ttu-id="0e3da-117">Il database (file con estensione msi) da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0e3da-117">The database (.msi file) that is to be updated.</span></span>                                                                                                                              |
| <span data-ttu-id="0e3da-118">-v</span><span class="sxs-lookup"><span data-stu-id="0e3da-118">-v</span></span>     |             | <span data-ttu-id="0e3da-119">Usare la modalità verbose.</span><span class="sxs-lookup"><span data-stu-id="0e3da-119">Use verbose mode.</span></span>                                                                                                                                                            |
| <span data-ttu-id="0e3da-120">-H</span><span class="sxs-lookup"><span data-stu-id="0e3da-120">-h</span></span>     |             | <span data-ttu-id="0e3da-121">Popolare la [tabella MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="0e3da-121">Populate the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="0e3da-122">Questa operazione crea la tabella se non esiste già.</span><span class="sxs-lookup"><span data-stu-id="0e3da-122">This creates the table if it does not already exist.</span></span> <span data-ttu-id="0e3da-123">La tabella MsiFileHash può essere utilizzata solo con file senza versione.</span><span class="sxs-lookup"><span data-stu-id="0e3da-123">The MsiFileHash table can only be used with unversioned files.</span></span> |
| <span data-ttu-id="0e3da-124">-S</span><span class="sxs-lookup"><span data-stu-id="0e3da-124">-s</span></span>     | <span data-ttu-id="0e3da-125">*ALTSOURCE*</span><span class="sxs-lookup"><span data-stu-id="0e3da-125">*ALTSOURCE*</span></span> | <span data-ttu-id="0e3da-126">ALTSOURCE specifica una directory alternativa per trovare i file.</span><span class="sxs-lookup"><span data-stu-id="0e3da-126">ALTSOURCE specifies an alternative directory to find the files.</span></span>                                                                                                              |



 

<span data-ttu-id="0e3da-127">Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0e3da-127">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e3da-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e3da-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e3da-129">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0e3da-129">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="0e3da-130">Uso della tabella di directory</span><span class="sxs-lookup"><span data-stu-id="0e3da-130">Using the Directory Table</span></span>](using-the-directory-table.md)
</dt> <dt>

[<span data-ttu-id="0e3da-131">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="0e3da-131">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



