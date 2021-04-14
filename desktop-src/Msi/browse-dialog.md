---
description: Una finestra di dialogo Sfoglia consente all'utente di selezionare una directory. La directory non deve esistere e può essere creata tramite questo controllo.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Sfoglia finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401703"
---
# <a name="browse-dialog"></a><span data-ttu-id="b2c65-104">Sfoglia finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b2c65-104">Browse Dialog</span></span>

<span data-ttu-id="b2c65-105">Una finestra di dialogo Sfoglia consente all'utente di selezionare una directory.</span><span class="sxs-lookup"><span data-stu-id="b2c65-105">A Browse dialog box enables the user to select a directory.</span></span> <span data-ttu-id="b2c65-106">La directory non deve esistere e può essere creata tramite questo controllo.</span><span class="sxs-lookup"><span data-stu-id="b2c65-106">The directory does not have to exist and may be created by using this control.</span></span>

<span data-ttu-id="b2c65-107">Questo tipo di finestra di dialogo contiene in genere i tre controlli seguenti.</span><span class="sxs-lookup"><span data-stu-id="b2c65-107">This type of dialog box commonly contains the following three controls.</span></span> <span data-ttu-id="b2c65-108">Questi controlli sono connessi alla stessa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2c65-108">These controls are connected to the same property.</span></span> <span data-ttu-id="b2c65-109">Tale proprietà è il percorso selezionato.</span><span class="sxs-lookup"><span data-stu-id="b2c65-109">That property is the path being selected.</span></span>

-   <span data-ttu-id="b2c65-110">[Controllo PathEdit](pathedit-control.md) per selezionare la sezione finale del percorso.</span><span class="sxs-lookup"><span data-stu-id="b2c65-110">A [PathEdit control](pathedit-control.md) to select the tail section of the path.</span></span> <span data-ttu-id="b2c65-111">Questo controllo non può perdere lo stato attivo se la coda immessa non è valida nel volume presente.</span><span class="sxs-lookup"><span data-stu-id="b2c65-111">This control cannot lose focus if the entered tail is not valid on the present volume.</span></span>
-   <span data-ttu-id="b2c65-112">[Controllo DirectoryCombo](directorycombo-control.md) per visualizzare il percorso attualmente selezionato visualizzato dal controllo PathEdit.</span><span class="sxs-lookup"><span data-stu-id="b2c65-112">A [DirectoryCombo control](directorycombo-control.md) to show the presently selected path that is displayed by the PathEdit control.</span></span> <span data-ttu-id="b2c65-113">Questo controllo non Mostra l'ultimo segmento del percorso.</span><span class="sxs-lookup"><span data-stu-id="b2c65-113">This control does not show the last segment of the path.</span></span>
-   <span data-ttu-id="b2c65-114">Un [controllo Directory](directorylist-control.md) per visualizzare le cartelle sotto la directory attualmente visualizzata dal DirectoryCombo.</span><span class="sxs-lookup"><span data-stu-id="b2c65-114">A [DirectoryList control](directorylist-control.md) to show the folders below the directory currently displayed by the DirectoryCombo.</span></span> <span data-ttu-id="b2c65-115">È anche possibile visualizzare una cartella che non è ancora stata creata.</span><span class="sxs-lookup"><span data-stu-id="b2c65-115">This can also show a folder that is not yet created.</span></span>

<span data-ttu-id="b2c65-116">Una finestra di dialogo Sfoglia contiene in genere anche un [controllo DirectoryCombo](directorycombo-control.md) che specifica i tipi di volume da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="b2c65-116">A Browse dialog box also usually contains a [DirectoryCombo control](directorycombo-control.md) that specifies the volume types to display.</span></span> <span data-ttu-id="b2c65-117">È comune che tutti i tipi di volume vengano visualizzati in una finestra di dialogo Sfoglia.</span><span class="sxs-lookup"><span data-stu-id="b2c65-117">It is common for all volume types to be displayed on a Browse dialog box.</span></span>

<span data-ttu-id="b2c65-118">Le finestre di dialogo di esplorazione contengono in genere tre [controlli pulsante](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="b2c65-118">Browse dialog boxes commonly contain three [PushButton controls](pushbutton-control.md).</span></span> <span data-ttu-id="b2c65-119">Questi pulsanti sono collegati ai rispettivi ControlEvents nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b2c65-119">These buttons are linked to their respective ControlEvents in [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="b2c65-120">Questi pulsanti vengono usati per attivare le opzioni di controllo seguenti.</span><span class="sxs-lookup"><span data-stu-id="b2c65-120">These buttons are used for activating the following control options.</span></span>



| <span data-ttu-id="b2c65-121">Opzione di controllo</span><span class="sxs-lookup"><span data-stu-id="b2c65-121">Control option</span></span> | <span data-ttu-id="b2c65-122">ControlEvent</span><span class="sxs-lookup"><span data-stu-id="b2c65-122">ControlEvent</span></span>                                            |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="b2c65-123">Livello superiore</span><span class="sxs-lookup"><span data-stu-id="b2c65-123">Up One Level</span></span>   | [<span data-ttu-id="b2c65-124">DirectoryListUp</span><span class="sxs-lookup"><span data-stu-id="b2c65-124">DirectoryListUp</span></span>](directorylistup-controlevent.md)     |
| <span data-ttu-id="b2c65-125">Nuova cartella</span><span class="sxs-lookup"><span data-stu-id="b2c65-125">New Folder</span></span>     | [<span data-ttu-id="b2c65-126">DirectoryListNew</span><span class="sxs-lookup"><span data-stu-id="b2c65-126">DirectoryListNew</span></span>](directorylistnew-controlevent.md)   |
| <span data-ttu-id="b2c65-127">Apri</span><span class="sxs-lookup"><span data-stu-id="b2c65-127">Open</span></span>           | [<span data-ttu-id="b2c65-128">DirectoryListOpen</span><span class="sxs-lookup"><span data-stu-id="b2c65-128">DirectoryListOpen</span></span>](directorylistopen-controlevent.md) |



 

<span data-ttu-id="b2c65-129">Affinché l'opzione nuova cartella funzioni con un nome di cartella non predefinito, è necessario specificare il percorso della nuova cartella nella [tabella UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="b2c65-129">For the New Folder option to work with a non-default folder name, the new folder's path must be specified in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="b2c65-130">Per il nome del file, la stringa di percorso deve usare il formato "nome file breve nome file \| lungo".</span><span class="sxs-lookup"><span data-stu-id="b2c65-130">The path string should use the "short file name\|long file name" form for the file name.</span></span> <span data-ttu-id="b2c65-131">Ad esempio, usare un nome file, ad esempio "Prod ~ 1 \| My Fabulous Product".</span><span class="sxs-lookup"><span data-stu-id="b2c65-131">For example, use a file name such as "MyProd~1\|My Fabulous Product".</span></span> <span data-ttu-id="b2c65-132">Per ulteriori informazioni sul formato del nome file, vedere il tipo di dati della colonna [filename](filename.md) .</span><span class="sxs-lookup"><span data-stu-id="b2c65-132">See the [Filename](filename.md) column data type for more information about the file name format.</span></span> <span data-ttu-id="b2c65-133">Se il percorso non è presente nella tabella UIText o se è impostato su un valore non valido, per impostazione predefinita viene impostato sul valore "FLDR \| New Folder".</span><span class="sxs-lookup"><span data-stu-id="b2c65-133">If the path is not present in the UIText table, or if it is set to an invalid value, then it is set to a value of "Fldr\|New Folder" by default.</span></span> <span data-ttu-id="b2c65-134">Il pulsante **nuova cartella** può essere omesso se la finestra di dialogo deve solo cercare le cartelle esistenti.</span><span class="sxs-lookup"><span data-stu-id="b2c65-134">The **New Folder** button can be omitted if the dialog box only need to search for existing folders.</span></span>

 

 



