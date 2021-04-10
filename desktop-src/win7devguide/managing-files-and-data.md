---
title: Gestione di file e dati
description: Gli utenti hanno accesso più semplice a file e dati in Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963237"
---
# <a name="managing-files-and-data"></a><span data-ttu-id="3da71-103">Gestione di file e dati</span><span class="sxs-lookup"><span data-stu-id="3da71-103">Managing Files and Data</span></span>

<span data-ttu-id="3da71-104">Gli utenti hanno accesso più semplice a file e dati in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3da71-104">Users have easier access to files and data in Windows 7.</span></span> <span data-ttu-id="3da71-105">Le nuove API rendono i file e le visualizzazioni più informativi, consentendo alle applicazioni di fornire informazioni rilevanti e distintive in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="3da71-105">New APIs make files and views more informative, enabling applications to deliver relevant and distinctive information to Windows Explorer.</span></span> <span data-ttu-id="3da71-106">Inoltre, le applicazioni traggono vantaggio dal nuovo modello di *librerie* , una nozione utile, più astratta dello spazio di archiviazione degli utenti rispetto alle cartelle e possono anche partecipare a librerie comuni di tipi di file simili condivisi da applicazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="3da71-106">In addition, applications benefit from the new *Libraries* model, a useful, more abstract notion of user storage space than folders, and can also participate in common libraries of similar file types that are shared by different applications.</span></span>

## <a name="libraries"></a><span data-ttu-id="3da71-107">Librerie</span><span class="sxs-lookup"><span data-stu-id="3da71-107">Libraries</span></span>

<span data-ttu-id="3da71-108">Windows 7 introduce il concetto di *librerie* come destinazioni in cui gli sviluppatori e gli utenti finali possono trovare e organizzare i dati come raccolte di elementi che possono estendersi su più posizioni nel computer locale e nei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="3da71-108">Windows 7 introduces the concept of *Libraries* as destinations where developers and end-users can find and organize their data as collections of items that can span multiple locations on the local computer as well as on remote computers.</span></span>

<span data-ttu-id="3da71-109">Le API della *libreria* forniscono agli sviluppatori un modo semplice per creare applicazioni in grado di creare, interagire e supportare le *librerie* come elementi di prima classe all'interno delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3da71-109">The *Library* APIs provide a straightforward way for developers to create applications that create, interact with, and support *Libraries* as first-class items within applications.</span></span> <span data-ttu-id="3da71-110">Le *librerie* possono essere selezionate anche tramite la finestra di dialogo di selezione cartelle.</span><span class="sxs-lookup"><span data-stu-id="3da71-110">*Libraries* can also be selected by using the folder picker dialog box.</span></span> <span data-ttu-id="3da71-111">Le applicazioni possono enumerare gli ambiti di libreria rilevanti oppure possono utilizzare la libreria direttamente come cartella.</span><span class="sxs-lookup"><span data-stu-id="3da71-111">Applications can enumerate relevant library scopes, or they can use the library directly as a folder.</span></span> <span data-ttu-id="3da71-112">(Vedere [librerie di Windows](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) e [librerie di Windows 7: risorse per sviluppatori](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span><span class="sxs-lookup"><span data-stu-id="3da71-112">(See [Windows Libraries](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) and [Windows 7 Libraries: Developer Resources](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span></span>

![libreria immagini di Windows 7](images/windows7-10.jpg)

<span data-ttu-id="3da71-114">La *Libreria immagini* Mostra le immagini indipendentemente dalla posizione in cui sono archiviate</span><span class="sxs-lookup"><span data-stu-id="3da71-114">*Pictures Library* shows your pictures no matter where they are stored</span></span>

## <a name="file-formats-and-data-stores"></a><span data-ttu-id="3da71-115">Formati di file e archivi dati</span><span class="sxs-lookup"><span data-stu-id="3da71-115">File Formats and Data Stores</span></span>

<span data-ttu-id="3da71-116">In Windows 7, Esplora risorse facilita la gestione dei file e la manipolazione per l'utente in diversi modi:</span><span class="sxs-lookup"><span data-stu-id="3da71-116">In Windows 7, Windows Explorer makes file management and manipulation easier for the user in several ways:</span></span>

-   <span data-ttu-id="3da71-117">L'anteprima per il tipo di file dell'applicazione è più accessibile con un pulsante nuovo che consente agli utenti di visualizzare e nascondere il riquadro di anteprima.</span><span class="sxs-lookup"><span data-stu-id="3da71-117">The preview for your application's file type is more accessible with a new button that lets users show and hide the preview pane.</span></span>
-   <span data-ttu-id="3da71-118">Gli stack visivi immersivi aggregano immagini di anteprima per i tipi di file in una vista.</span><span class="sxs-lookup"><span data-stu-id="3da71-118">Immersive visual stacks aggregate thumbnail images for file types in a view.</span></span>
-   <span data-ttu-id="3da71-119">Le visualizzazioni di Esplora risorse mostrano informazioni utili basate sulle proprietà scritte con il gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="3da71-119">Windows Explorer views show useful information based on properties written with your property handler.</span></span>
-   <span data-ttu-id="3da71-120">I frammenti di documento e l'evidenziazione dei riscontri usano l'implementazione dell'interfaccia **IFilter** per semplificare la ricerca e la ricerca di file.</span><span class="sxs-lookup"><span data-stu-id="3da71-120">Document snippets and hit highlighting use your **IFilter** interface implementation to make searching and finding files easier.</span></span>
-   <span data-ttu-id="3da71-121">I verbi e i comandi del menu di scelta rapida sono più facili che mai implementare.</span><span class="sxs-lookup"><span data-stu-id="3da71-121">Context-menu verbs and commands are easier than ever to implement.</span></span>

<span data-ttu-id="3da71-122">Implementando tutti i gestori di formato appropriati per gli elementi restituiti dal gestore di protocollo, i risultati della ricerca dall'archivio dati personalizzato possono essere ricchi di risultati della ricerca dei file.</span><span class="sxs-lookup"><span data-stu-id="3da71-122">By implementing all of the appropriate format handlers for the items returned from your protocol handler, search results from your custom data store can be as rich as search results from files.</span></span> <span data-ttu-id="3da71-123">Le *librerie* vengono create automaticamente per i gestori del protocollo, in modo che gli utenti possano definire facilmente l'ambito delle proprie ricerche.</span><span class="sxs-lookup"><span data-stu-id="3da71-123">*Libraries* are automatically created for your protocol handlers so users can scope their searches easily.</span></span> <span data-ttu-id="3da71-124">La logica per la creazione di *librerie* può essere facilmente personalizzata tramite il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3da71-124">And the logic for creating *Libraries* can be easily customized through the registry.</span></span> <span data-ttu-id="3da71-125">Vedere [sviluppo di filtri per la ricerca di Windows](../search/-search-3x-wds-extidx-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3da71-125">(See [Developing Filters for Windows Search](../search/-search-3x-wds-extidx-filters.md).)</span></span>

![raccolta documenti di Windows 7](images/windows7-11.jpg)

<span data-ttu-id="3da71-127">In Windows 7, Esplora risorse rende più semplice la gestione e la manipolazione dei file</span><span class="sxs-lookup"><span data-stu-id="3da71-127">In Windows 7, Windows Explorer makes file management and manipulation easier</span></span>

 

 