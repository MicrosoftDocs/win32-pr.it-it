---
description: Questa tabella contiene i file di icona. Ogni icona della tabella viene copiata in un file come parte dell'annuncio del prodotto da utilizzare per i collegamenti annunciati e i server OLE. Vedere limitazioni OLE sui flussi.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Icona tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227195"
---
# <a name="icon-table"></a><span data-ttu-id="e1cc7-105">Icona tabella</span><span class="sxs-lookup"><span data-stu-id="e1cc7-105">Icon Table</span></span>

<span data-ttu-id="e1cc7-106">Questa tabella contiene i file di icona.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-106">This table contains the icon files.</span></span> <span data-ttu-id="e1cc7-107">Ogni icona della tabella viene copiata in un file come parte dell'annuncio del prodotto da utilizzare per i collegamenti annunciati e i server OLE.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-107">Each icon from the table is copied to a file as a part of product advertisement to be used for advertised shortcuts and OLE servers.</span></span> <span data-ttu-id="e1cc7-108">Vedere [limitazioni OLE sui flussi](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e1cc7-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="e1cc7-109">La tabella Icon contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-109">The Icon table has the following columns.</span></span>



| <span data-ttu-id="e1cc7-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="e1cc7-110">Column</span></span> | <span data-ttu-id="e1cc7-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1cc7-111">Type</span></span>                         | <span data-ttu-id="e1cc7-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="e1cc7-112">Key</span></span> | <span data-ttu-id="e1cc7-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="e1cc7-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="e1cc7-114">Nome</span><span class="sxs-lookup"><span data-stu-id="e1cc7-114">Name</span></span>   | [<span data-ttu-id="e1cc7-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="e1cc7-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="e1cc7-116">S</span><span class="sxs-lookup"><span data-stu-id="e1cc7-116">Y</span></span>   | <span data-ttu-id="e1cc7-117">N</span><span class="sxs-lookup"><span data-stu-id="e1cc7-117">N</span></span>        |
| <span data-ttu-id="e1cc7-118">Data</span><span class="sxs-lookup"><span data-stu-id="e1cc7-118">Data</span></span>   | [<span data-ttu-id="e1cc7-119">Binario</span><span class="sxs-lookup"><span data-stu-id="e1cc7-119">Binary</span></span>](binary.md)         | <span data-ttu-id="e1cc7-120">N</span><span class="sxs-lookup"><span data-stu-id="e1cc7-120">N</span></span>   | <span data-ttu-id="e1cc7-121">N</span><span class="sxs-lookup"><span data-stu-id="e1cc7-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e1cc7-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="e1cc7-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e1cc7-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="e1cc7-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="e1cc7-124">Nome del file icona.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-124">Name of the icon file.</span></span>

</dd> <dt>

<span data-ttu-id="e1cc7-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati</span><span class="sxs-lookup"><span data-stu-id="e1cc7-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="e1cc7-126">Dati dell'icona binaria in formato PE (. dll o. exe) o icona (. ico).</span><span class="sxs-lookup"><span data-stu-id="e1cc7-126">The binary icon data in PE (.dll or .exe) or icon (.ico) format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1cc7-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1cc7-127">Remarks</span></span>

<span data-ttu-id="e1cc7-128">Questa tabella viene definita quando viene eseguita l' [azione PublishProduct](publishproduct-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e1cc7-128">This table is referred to when the [PublishProduct action](publishproduct-action.md) is executed.</span></span>

<span data-ttu-id="e1cc7-129">Le icone per i collegamenti, le estensioni dei nomi di file e i CLSID devono essere archiviati in file separati dal file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-129">The icons for shortcuts, file name extensions, and CLSIDs must be stored in files that are separate from the target file itself.</span></span> <span data-ttu-id="e1cc7-130">Questa operazione è necessaria perché il programma di installazione deve copiare solo i file dell'icona piccola nel computer dell'utente quando si annuncia la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-130">This is required because the installer should copy only the small icon files to the user's machine when advertising the resource.</span></span> <span data-ttu-id="e1cc7-131">Uno sviluppatore di un pacchetto di installazione deve quindi creare file distinti contenenti solo le icone.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-131">A developer of an installation package therefore needs to author separate files containing only the icons.</span></span> <span data-ttu-id="e1cc7-132">Questi file di icona vengono quindi archiviati come dati binari nella tabella delle icone.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-132">These icon files are then stored as binary data in the Icon table.</span></span>

<span data-ttu-id="e1cc7-133">I file di icona associati esclusivamente a estensioni di file o CLSID possono avere qualsiasi estensione, ad esempio. ico.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-133">Icon files that are associated strictly with file name extensions or CLSIDs can have any extension, such as .ico.</span></span> <span data-ttu-id="e1cc7-134">Tuttavia, i file di icona associati ai collegamenti devono essere nel formato binario EXE e devono essere denominati in modo tale che l'estensione corrisponda all'estensione della destinazione.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-134">However, Icon files that are associated with shortcuts must be in the EXE binary format and must be named such that their extension matches the extension of the target.</span></span> <span data-ttu-id="e1cc7-135">Il collegamento non funzionerà se questa regola non è seguita.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-135">The shortcut will not work if this rule is not followed.</span></span> <span data-ttu-id="e1cc7-136">Se, ad esempio, un collegamento consiste nel puntare a una risorsa con il file di chiave Red.bar, anche il file dell'icona deve avere la barra di estensione.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-136">For example, if a shortcut is to point to a resource having the key file Red.bar, then the icon file must also have the extension .bar.</span></span> <span data-ttu-id="e1cc7-137">È possibile inserire più icone nello stesso file icona purché tutti i file di destinazione abbiano la stessa estensione.</span><span class="sxs-lookup"><span data-stu-id="e1cc7-137">Multiple icons can be stuffed into the same icon file as long as all of the target files have the same extension.</span></span>

## <a name="validation"></a><span data-ttu-id="e1cc7-138">Convalida</span><span class="sxs-lookup"><span data-stu-id="e1cc7-138">Validation</span></span>

<dl>

[<span data-ttu-id="e1cc7-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="e1cc7-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e1cc7-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="e1cc7-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e1cc7-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="e1cc7-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="e1cc7-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="e1cc7-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e1cc7-143">ICE36</span><span class="sxs-lookup"><span data-stu-id="e1cc7-143">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="e1cc7-144">ICE50</span><span class="sxs-lookup"><span data-stu-id="e1cc7-144">ICE50</span></span>](ice50.md)  
</dl>

 

 



