---
description: L'azione MoveFiles individua i file esistenti nel computer dell'utente e li sposta o li copia in una nuova posizione.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Azione MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885509"
---
# <a name="movefiles-action"></a><span data-ttu-id="ab985-103">Azione MoveFiles</span><span class="sxs-lookup"><span data-stu-id="ab985-103">MoveFiles Action</span></span>

<span data-ttu-id="ab985-104">L'azione MoveFiles individua i file esistenti nel computer dell'utente e li sposta o li copia in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="ab985-104">The MoveFiles action locates existing files on the user's computer and moves or copies those files to a new location.</span></span> <span data-ttu-id="ab985-105">L'azione MoveFiles esegue una query sulla [tabella MoveFile](movefile-table.md) e sposta i file specificati se il componente collegato alle voci è specificato per l'installazione locale o viene eseguito dall'origine.</span><span class="sxs-lookup"><span data-stu-id="ab985-105">The MoveFiles action queries the [MoveFile table](movefile-table.md) and moves files specified there if the component linked to the entries is specified to be install locally or is being run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ab985-106">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="ab985-106">Sequence Restrictions</span></span>

<span data-ttu-id="ab985-107">L'azione MoveFiles deve essere successiva all'azione [InstallValidate](installvalidate-action.md) e prima dell'azione [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ab985-107">The MoveFiles action must come after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ab985-108">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="ab985-108">ActionData Messages</span></span>



| <span data-ttu-id="ab985-109">Campo</span><span class="sxs-lookup"><span data-stu-id="ab985-109">Field</span></span> | <span data-ttu-id="ab985-110">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="ab985-110">Description of action data</span></span>                  |
|-------|---------------------------------------------|
| <span data-ttu-id="ab985-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ab985-111">\[1\]</span></span> | <span data-ttu-id="ab985-112">Identificatore del file spostato.</span><span class="sxs-lookup"><span data-stu-id="ab985-112">Identifier of moved file.</span></span>                   |
| <span data-ttu-id="ab985-113">\[6\]</span><span class="sxs-lookup"><span data-stu-id="ab985-113">\[6\]</span></span> | <span data-ttu-id="ab985-114">Dimensioni del file installato in byte.</span><span class="sxs-lookup"><span data-stu-id="ab985-114">Size of installed file in bytes.</span></span>            |
| <span data-ttu-id="ab985-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="ab985-115">\[9\]</span></span> | <span data-ttu-id="ab985-116">Identificatore della directory che contiene il file spostato.</span><span class="sxs-lookup"><span data-stu-id="ab985-116">Identifier of directory holding moved file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ab985-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab985-117">Remarks</span></span>

<span data-ttu-id="ab985-118">La tabella MoveFiles contiene una colonna denominata "Options" che specifica i file di origine da spostare o copiare.</span><span class="sxs-lookup"><span data-stu-id="ab985-118">The MoveFiles table contain a column named "options" which specifies the source files to be moved or copied.</span></span> <span data-ttu-id="ab985-119">Un file di origine spostato viene eliminato dopo essere stato copiato in un nuovo percorso.</span><span class="sxs-lookup"><span data-stu-id="ab985-119">A moved source file is deleted after it has been copied to a new location.</span></span> <span data-ttu-id="ab985-120">Per la sintassi esatta, vedere la [tabella MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab985-120">For the exact syntax, see the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="ab985-121">Le colonne SourceFolder e DestFolder della tabella MoveFile sono nomi di proprietà i cui valori sono previsti per la risoluzione nei percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="ab985-121">The SourceFolder and DestFolder columns of the MoveFile table are property names whose values are expected to resolve to fully qualified paths.</span></span> <span data-ttu-id="ab985-122">Queste proprietà possono essere qualsiasi voce di directory nella tabella di [directory](directory-table.md) , qualsiasi proprietà di cartella predefinita (ad esempio,[**FavoritesFolder**](favoritesfolder.md)) o una proprietà impostata da qualsiasi voce nella tabella [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ab985-122">These properties can be any of the directory entries in the [Directory](directory-table.md) table, any predefined folder property ([**FavoritesFolder**](favoritesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="ab985-123">Queste proprietà possono contenere un percorso completo contenente il nome file di un file specifico.</span><span class="sxs-lookup"><span data-stu-id="ab985-123">These properties may contain a full path containing the file name to a specific file.</span></span> <span data-ttu-id="ab985-124">Ad esempio, è possibile creare la tabella AppSearch per cercare un file specifico e impostare una proprietà sul percorso completo di tale file.</span><span class="sxs-lookup"><span data-stu-id="ab985-124">For example, the AppSearch table can be authored to search for a particular file and set a property to the full path to that file.</span></span> <span data-ttu-id="ab985-125">In questo esempio, la colonna SourceName nella tabella MoveFile può essere lasciata vuota per indicare che il valore nella proprietà SourceFolder contiene un percorso file completo.</span><span class="sxs-lookup"><span data-stu-id="ab985-125">In this example, the SourceName column in the MoveFile table can be left blank to indicate that the value in the SourceFolder property contains a full file path.</span></span> <span data-ttu-id="ab985-126">Il punto e virgola è il delimitatore di elenco per le trasformazioni, le origini e le patch e non deve essere usato nei nomi file o nei percorsi.</span><span class="sxs-lookup"><span data-stu-id="ab985-126">The semicolon is the list delimiter for transforms, sources, and patches and should not be used in file names or paths.</span></span>

<span data-ttu-id="ab985-127">L'azione MoveFiles non agisce sulle voci della tabella MoveFile in cui la proprietà SourceFolder o DestFolder non restituisce un percorso completo.</span><span class="sxs-lookup"><span data-stu-id="ab985-127">The MoveFiles action does not act on entries in the MoveFile table in which either the SourceFolder or DestFolder property does not evaluate to a full path.</span></span>

<span data-ttu-id="ab985-128">L'azione MoveFiles tenta di spostare o copiare tutti i file nella directory di origine che corrispondono al nome specificato nella colonna SourceName della tabella MoveFiles.</span><span class="sxs-lookup"><span data-stu-id="ab985-128">The MoveFiles action attempts to move or copy all files in the source directory that match the name given in the SourceName column of the MoveFiles table.</span></span> <span data-ttu-id="ab985-129">Il nome nella colonna SourceName può includere \* o?</span><span class="sxs-lookup"><span data-stu-id="ab985-129">The name in the SourceName column can include either the \* or ?</span></span> <span data-ttu-id="ab985-130">caratteri jolly che consentono lo spostamento o la copia di un gruppo di file.</span><span class="sxs-lookup"><span data-stu-id="ab985-130">wildcards which allow a group of files to be moved or copied.</span></span> <span data-ttu-id="ab985-131">La colonna SourceName, ad esempio, può contenere una voce " \* . xls" e l'azione MoveFiles sposta o copia ogni cartella di lavoro di Microsoft Excel dalla directory di origine alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="ab985-131">For example, the SourceName column may contain an entry of "\*.xls" and the MoveFiles action moves or copies every Microsoft Excel workbook from the source directory to the destination.</span></span>

<span data-ttu-id="ab985-132">Il nome da assegnare al file di destinazione può essere specificato nella colonna destName della tabella MoveFile.</span><span class="sxs-lookup"><span data-stu-id="ab985-132">The name to be given to the destination file can be specified in the DestName column of the MoveFile table.</span></span> <span data-ttu-id="ab985-133">Il nome del file di destinazione mantiene il nome del file di origine se questa colonna viene lasciata vuota.</span><span class="sxs-lookup"><span data-stu-id="ab985-133">The destination file name retains the source file name if this column is left blank.</span></span>

<span data-ttu-id="ab985-134">Se un \* carattere jolly "" viene immesso nella colonna SourceName della [tabella MoveFile](movefile-table.md) e nella colonna destName viene specificato un nome file di destinazione, tutti i file spostati o copiati manterranno i nomi nelle origini.</span><span class="sxs-lookup"><span data-stu-id="ab985-134">If a "\*" wildcard is entered in the SourceName column of the [MoveFile table](movefile-table.md) and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="ab985-135">I file che vengono spostati o copiati dall'azione MoveFiles non vengono eliminati quando il prodotto viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="ab985-135">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

 

 



