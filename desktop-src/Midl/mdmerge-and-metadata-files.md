---
title: MDMERGE e file di metadati
description: Compone più file di metadati (con estensione winmd) in un numero di file di metadati di output, in base allo spazio dei nomi.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- file WinMD
- Metadati di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955203"
---
# <a name="mdmerge-and-metadata-files"></a><span data-ttu-id="0bed5-106">MDMERGE e file di metadati</span><span class="sxs-lookup"><span data-stu-id="0bed5-106">MDMERGE and metadata files</span></span>

<span data-ttu-id="0bed5-107">Compone più file di metadati (con estensione winmd) in un numero di file di metadati di output, in base allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0bed5-107">Composes multiple metadata (.winmd) files into a number of output metadata files, based on namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="0bed5-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0bed5-108">Usage</span></span>

<span data-ttu-id="0bed5-109">Eseguire MDMERGE dalla riga di comando usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="0bed5-109">Run MDMERGE from the command line using the following command:</span></span>

<span data-ttu-id="0bed5-110"> *< ***Opzioni*** di Mdmerge>*</span><span class="sxs-lookup"><span data-stu-id="0bed5-110">**mdmerge** *<***options***>*</span></span>

<span data-ttu-id="0bed5-111">dove *<  Options >* rappresenta le opzioni della riga di comando che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0bed5-111">where *<***options***>* represents the command-line options you want to use.</span></span>

<span data-ttu-id="0bed5-112">Generare file di metadati per i componenti Windows Runtime personalizzati usando il compilatore MIDLRT.</span><span class="sxs-lookup"><span data-stu-id="0bed5-112">Generate metadata files for your custom Windows Runtime components by using the MIDLRT compiler.</span></span> <span data-ttu-id="0bed5-113">Per altre informazioni, vedere [MIDLRT and Windows Runtime Components](midlrt-and-windows-runtime-components.md).</span><span class="sxs-lookup"><span data-stu-id="0bed5-113">For more info, see [MIDLRT and Windows Runtime components](midlrt-and-windows-runtime-components.md).</span></span>

## <a name="command-line-switches"></a><span data-ttu-id="0bed5-114">Opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="0bed5-114">Command-line switches</span></span>

<span data-ttu-id="0bed5-115">Nell'elenco seguente vengono illustrate le opzioni della riga di comando utilizzate da MDMERGE.</span><span class="sxs-lookup"><span data-stu-id="0bed5-115">The following list shows the command-line switches that MDMERGE uses.</span></span>

<dl>

[<span data-ttu-id="0bed5-116">**/i**</span><span class="sxs-lookup"><span data-stu-id="0bed5-116">**/i**</span></span>](-mdmerge-i.md)  
[<span data-ttu-id="0bed5-117">**\_dir/Metadata**</span><span class="sxs-lookup"><span data-stu-id="0bed5-117">**/metadata\_dir**</span></span>](-mdmerge-metadata-dir.md)  
[<span data-ttu-id="0bed5-118">**/n**</span><span class="sxs-lookup"><span data-stu-id="0bed5-118">**/n**</span></span>](-mdmerge-n.md)  
[<span data-ttu-id="0bed5-119">**/o**</span><span class="sxs-lookup"><span data-stu-id="0bed5-119">**/o**</span></span>](-mdmerge-o.md)  
[<span data-ttu-id="0bed5-120">**/partial**</span><span class="sxs-lookup"><span data-stu-id="0bed5-120">**/partial**</span></span>](-mdmerge-partial.md)  
[<span data-ttu-id="0bed5-121">**/v**</span><span class="sxs-lookup"><span data-stu-id="0bed5-121">**/v**</span></span>](-mdmerge-v.md)  
</dl>

<span data-ttu-id="0bed5-122">Quando si usano i parametri **-h** e **/?** è disponibile un elenco completo delle opzioni e delle opzioni del compilatore MDMERGE.</span><span class="sxs-lookup"><span data-stu-id="0bed5-122">A complete listing of MDMERGE compiler switches and options is available when you use the **-h** and **/?**</span></span> <span data-ttu-id="0bed5-123">interruttori.</span><span class="sxs-lookup"><span data-stu-id="0bed5-123">switches.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bed5-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bed5-124">Remarks</span></span>

<span data-ttu-id="0bed5-125">La composizione dei metadati consente a più file IDL di contenere definizioni per i componenti Windows Runtime nello stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0bed5-125">Metadata composition enables multiple IDL files to contain definitions for Windows Runtime components in the same namespace.</span></span> <span data-ttu-id="0bed5-126">Ciò consente di definire tutti i tipi in uno spazio dei nomi all'interno di un singolo file IDL.</span><span class="sxs-lookup"><span data-stu-id="0bed5-126">This frees you from defining all of the types in a namespace within a single IDL file.</span></span>

<span data-ttu-id="0bed5-127">È probabile che siano presenti numerosi componenti Windows Runtime usati dalle app.</span><span class="sxs-lookup"><span data-stu-id="0bed5-127">You're likely to have numerous Windows Runtime components that your apps use.</span></span> <span data-ttu-id="0bed5-128">Quando si esegue il passaggio finale per produrre assembly di metadati distribuibile Windows Runtime, è possibile configurare MDMERGE per unire i componenti da più directory di metadati, ad esempio quelli installati con il sistema (% WINDOWS% \\ system32 \\ WinMetadata), i tipi di base e la directory di compilazione del progetto corrente.</span><span class="sxs-lookup"><span data-stu-id="0bed5-128">When you perform the final step to produce deployable Windows Runtime metadata assemblies, you can configure MDMERGE to merge components from multiple metadata directories, like those that are installed with the system (%WINDOWS%\\system32\\WinMetadata), your foundation types, and your current project’s build directory.</span></span> <span data-ttu-id="0bed5-129">Tutti i tipi necessari vengono uniti negli assembly di metadati corretti, distribuibile, che è possibile creare in un pacchetto per Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0bed5-129">All necessary types are merged into the correct, deployable, metadata assemblies that you can package for the Windows Store.</span></span>

<span data-ttu-id="0bed5-130">È possibile utilizzare l'opzione [**/n**](-mdmerge-n.md) per specificare la profondità dello spazio dei nomi supportata per la composizione degli assembly di metadati.</span><span class="sxs-lookup"><span data-stu-id="0bed5-130">You can use the [**/n**](-mdmerge-n.md) option to specify the supported namespace depth for composing metadata assemblies.</span></span> <span data-ttu-id="0bed5-131">Ciò consente di configurare una suddivisione a caldo per i componenti di Windows Runtime, in modo da creare un pacchetto di un singolo file con estensione WinMD anziché di molti.</span><span class="sxs-lookup"><span data-stu-id="0bed5-131">This enables configuring a hot split for your Windows Runtime components, so that only a single .winmd file is packaged instead of many.</span></span> <span data-ttu-id="0bed5-132">In questo modo si riducono i tempi di caricamento e I/O dei file richiesti dalle app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0bed5-132">This reduces the load times and file I/O required by your Windows Store apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bed5-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0bed5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bed5-134">Componenti di MIDLRT e Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="0bed5-134">MIDLRT and Windows Runtime components</span></span>](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




