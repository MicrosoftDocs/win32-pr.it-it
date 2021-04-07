---
description: Quando una tabella che contiene solo caratteri ASCII viene esportata in un file di archivio di testo, il file con estensione IDT rispetta il formato di file di archivio di base.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Dati ASCII nei file di archivio di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881109"
---
# <a name="ascii-data-in-text-archive-files"></a><span data-ttu-id="0367d-103">Dati ASCII nei file di archivio di testo</span><span class="sxs-lookup"><span data-stu-id="0367d-103">ASCII Data in Text Archive Files</span></span>

<span data-ttu-id="0367d-104">Quando una tabella che contiene solo caratteri ASCII viene esportata in un [file di archivio di testo](text-archive-files.md), il file con estensione IDT rispetta il formato di file di [Archivio](archive-file-format.md)di base.</span><span class="sxs-lookup"><span data-stu-id="0367d-104">When a table that contains only ASCII characters is exported to a [text archive file](text-archive-files.md), the .idt file adheres to the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="0367d-105">Se la tabella contiene informazioni non ASCII, il formato del file di archivio viene esteso per includere le informazioni sulla tabella codici.</span><span class="sxs-lookup"><span data-stu-id="0367d-105">If the table contains non-ASCII information, the format of the archive file is extended to include code page information.</span></span>

## <a name="text-archive-files-that-contain-only-ascii-characters"></a><span data-ttu-id="0367d-106">File di archivio di testo che contengono solo caratteri ASCII</span><span class="sxs-lookup"><span data-stu-id="0367d-106">Text archive files that contain only ASCII characters</span></span>

<span data-ttu-id="0367d-107">Quando una tabella che contiene solo caratteri ASCII viene esportata in un file di archivio, il file con estensione IDT si trova nel [formato di file di archivio](archive-file-format.md)di base.</span><span class="sxs-lookup"><span data-stu-id="0367d-107">When a table that contains only ASCII characters is exported to an archive file, the .idt file is in the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="0367d-108">Ogni flusso della tabella viene esportato come file con estensione IBD.</span><span class="sxs-lookup"><span data-stu-id="0367d-108">Each stream in the table is exported as a file with an .ibd file name extension.</span></span> <span data-ttu-id="0367d-109">I file con estensione IBD vengono archiviati in una cartella con lo stesso nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="0367d-109">The .ibd files are stored in a folder with the same name as the table.</span></span> <span data-ttu-id="0367d-110">Si consideri, ad esempio, l'esportazione della seguente tabella [binaria](binary-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0367d-110">For example, consider the export of the following [Binary](binary-table.md) table.</span></span>



| <span data-ttu-id="0367d-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0367d-111">Name</span></span>  | <span data-ttu-id="0367d-112">Data</span><span class="sxs-lookup"><span data-stu-id="0367d-112">Data</span></span>      |
|-------|-----------|
| <span data-ttu-id="0367d-113">Libri</span><span class="sxs-lookup"><span data-stu-id="0367d-113">Books</span></span> | <span data-ttu-id="0367d-114">Libri. IBD</span><span class="sxs-lookup"><span data-stu-id="0367d-114">Books.ibd</span></span> |
| <span data-ttu-id="0367d-115">Cars</span><span class="sxs-lookup"><span data-stu-id="0367d-115">Cars</span></span>  | <span data-ttu-id="0367d-116">Automobili. IBD</span><span class="sxs-lookup"><span data-stu-id="0367d-116">Cars.ibd</span></span>  |



 

<span data-ttu-id="0367d-117">La struttura di directory dopo l'esportazione della tabella è la seguente.</span><span class="sxs-lookup"><span data-stu-id="0367d-117">The directory structure after exporting this table is as follows.</span></span> <span data-ttu-id="0367d-118">Le informazioni nella tabella di database vengono esportate in Binary. IDT.</span><span class="sxs-lookup"><span data-stu-id="0367d-118">The information in the database table is exported to Binary.idt.</span></span> <span data-ttu-id="0367d-119">I due flussi di dati binari vengono esportati in book. IBD e Cars. IBD salvati nella cartella denominata Binary.</span><span class="sxs-lookup"><span data-stu-id="0367d-119">The two streams of binary data are exported to Book.ibd and Cars.ibd saved in the folder named Binary.</span></span>

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

<span data-ttu-id="0367d-120">Il file di archivio Binary. IDT è nel [formato di file di archivio](archive-file-format.md) di base e avrà un aspetto simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="0367d-120">The Binary.idt archive file is in the basic [archive file format](archive-file-format.md) and would look as follows.</span></span>

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a><span data-ttu-id="0367d-121">File di archivio di testo che contengono caratteri non ASCII</span><span class="sxs-lookup"><span data-stu-id="0367d-121">Text archive files that contain non- ASCII characters</span></span>

<span data-ttu-id="0367d-122">Se il file contiene dati non ASCII, il formato del [file di archivio](archive-file-format.md) di base del file con estensione IDT viene esteso per includere le informazioni sulla tabella codici.</span><span class="sxs-lookup"><span data-stu-id="0367d-122">If the file contains non-ASCII data, the basic [archive file format](archive-file-format.md) of the .idt file is extended to include code page information.</span></span> <span data-ttu-id="0367d-123">La terza riga della tabella. IDT è la tabella codici numerica seguita dal nome della tabella e dai nomi delle colonne chiave primaria separati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="0367d-123">The third row in the .idt table is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="0367d-124">Un file con estensione IDT che contiene informazioni non ASCII deve essere salvato nel formato ASCII.</span><span class="sxs-lookup"><span data-stu-id="0367d-124">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="0367d-125">Un file di archivio di testo, ad esempio, può contenere i nomi di colonna e di tabella codificati come UTF-8, ma il file di archivio deve essere ASCII.</span><span class="sxs-lookup"><span data-stu-id="0367d-125">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span>

 

<span data-ttu-id="0367d-126">La tabella ActionText seguente localizzata in francese conterrebbe informazioni non ASCII.</span><span class="sxs-lookup"><span data-stu-id="0367d-126">The following ActionText table localized into French would contain non-ASCII information.</span></span> <span data-ttu-id="0367d-127">La tabella codici numerica utilizzata per le stringhe francesi è 1252.</span><span class="sxs-lookup"><span data-stu-id="0367d-127">The numeric code page used for French strings is 1252.</span></span>



| <span data-ttu-id="0367d-128">Azione</span><span class="sxs-lookup"><span data-stu-id="0367d-128">Action</span></span>    | <span data-ttu-id="0367d-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0367d-129">Description</span></span>                                  | <span data-ttu-id="0367d-130">Modello</span><span class="sxs-lookup"><span data-stu-id="0367d-130">Template</span></span> |
|-----------|----------------------------------------------|----------|
| <span data-ttu-id="0367d-131">PUBBLICIZZA</span><span class="sxs-lookup"><span data-stu-id="0367d-131">ADVERTISE</span></span> | <span data-ttu-id="0367d-132">Pubblicazione d'informations sur l'applicazione</span><span class="sxs-lookup"><span data-stu-id="0367d-132">Publication d'informations sur l'application</span></span> |          |



 

<span data-ttu-id="0367d-133">Il file di archivio esportato, ActionText. IDT, sarà il seguente.</span><span class="sxs-lookup"><span data-stu-id="0367d-133">The exported archive file, ActionText.idt, would be as follows.</span></span>

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> <span data-ttu-id="0367d-134">Se un file di archivio di testo contiene dati non ASCII, il file di archivio include informazioni sulla tabella codici.</span><span class="sxs-lookup"><span data-stu-id="0367d-134">If a text archive file contains non-ASCII data, the archive file includes code page information.</span></span> <span data-ttu-id="0367d-135">I file di archivio con le informazioni sulla tabella codici possono essere importati di nuovo solo in un database di tale tabella codici esatta oppure in un database indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="0367d-135">Archive files with code page information can only be imported back into a database of that exact code page or into a language neutral database.</span></span> <span data-ttu-id="0367d-136">Nel caso di un database indipendente dalla lingua, la tabella codici viene impostata sulla tabella codici del file di archivio.</span><span class="sxs-lookup"><span data-stu-id="0367d-136">In the case of a language neutral database, the code page is set to the code page of the archive file.</span></span> <span data-ttu-id="0367d-137">Per ulteriori informazioni sul modo in cui Windows Installer gestisce le tabelle codici, vedere la sezione [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="0367d-137">For more information about how Windows Installer handles code pages see the section [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

 

 

 



