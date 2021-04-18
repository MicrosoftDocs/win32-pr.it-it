---
title: Informazioni sulla libreria
description: Informazioni sulla libreria
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Library, informazioni
- libreria, informazioni
- metadati, Windows Media Player Library
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297753"
---
# <a name="about-the-library"></a><span data-ttu-id="ddec8-113">Informazioni sulla libreria</span><span class="sxs-lookup"><span data-stu-id="ddec8-113">About the Library</span></span>

<span data-ttu-id="ddec8-114">La libreria è un database di informazioni o *metadati* sul contenuto multimediale digitale disponibile per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ddec8-114">The library is a database of information, or *metadata*, about the digital media content that is available to Windows Media Player.</span></span> <span data-ttu-id="ddec8-115">Alcune delle informazioni vengono visualizzate nel riquadro **libreria** del lettore; la maggior quantità è disponibile tramite codice.</span><span class="sxs-lookup"><span data-stu-id="ddec8-115">Some of the information is displayed in the **Library** pane in the Player; more of it is available through code.</span></span>

<span data-ttu-id="ddec8-116">(In Windows Media Player 9 serie e versioni precedenti questa funzionalità è denominata **libreria multimediale**).</span><span class="sxs-lookup"><span data-stu-id="ddec8-116">(In Windows Media Player 9 Series and earlier, this feature is called **Media Library**.)</span></span>

<span data-ttu-id="ddec8-117">La libreria offre agli utenti un modo semplice per organizzare e accedere al contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="ddec8-117">The library gives users an easy way to organize and access digital media content.</span></span> <span data-ttu-id="ddec8-118">Ad esempio, gli utenti possono visualizzare musica organizzata in base all'album, dall'artista, dal genere o semplicemente come un elenco di tutti i brani musicali.</span><span class="sxs-lookup"><span data-stu-id="ddec8-118">For example, users can view music organized by album, by artist, by genre, or simply as a list of all music.</span></span> <span data-ttu-id="ddec8-119">È possibile utilizzare il modello a oggetti di Windows Media Player SDK per accedere alla libreria per riprodurre contenuto, recuperare playlist, aggiungere contenuto, rimuovere contenuto e modificare i metadati associati.</span><span class="sxs-lookup"><span data-stu-id="ddec8-119">You can use the Windows Media Player SDK object model to access the library to play content, retrieve playlists, add content, remove content, and change the associated metadata.</span></span> <span data-ttu-id="ddec8-120">Windows Media Player protegge la privacy degli utenti limitando la possibilità di accedere alla libreria dal codice in determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="ddec8-120">Windows Media Player protects users' privacy by restricting your ability to access the library from code under certain conditions.</span></span> <span data-ttu-id="ddec8-121">Per ulteriori informazioni sui diritti di accesso, vedere [Library Access](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ddec8-121">For more information about access rights, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ddec8-122">La libreria archivia i metadati su due tipi di base di contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="ddec8-122">The library stores metadata about two basic types of digital media content.</span></span> <span data-ttu-id="ddec8-123">Il primo tipo, elementi multimediali digitali, è un singolo file di contenuto, ad esempio un brano musicale o una foto.</span><span class="sxs-lookup"><span data-stu-id="ddec8-123">The first type, digital media items, are individual content files, such as a music track or a photo.</span></span> <span data-ttu-id="ddec8-124">Il secondo tipo, playlist, è costituito da file che rappresentano un gruppo di elementi multimediali digitali, in genere destinati a essere riprodotti in un ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="ddec8-124">The second type, playlists, are files that represent a group of digital media items, typically intended to be played in a specified order.</span></span> <span data-ttu-id="ddec8-125">I metadati associati al contenuto multimediale digitale vengono archiviati come coppie nome-valore.</span><span class="sxs-lookup"><span data-stu-id="ddec8-125">The metadata associated with digital media content is stored as name-value pairs.</span></span> <span data-ttu-id="ddec8-126">I metadati che descrivono la persona che ha eseguito un brano, ad esempio, sono denominati "Artist" e il valore associato è in genere una stringa di testo contenente il nome dell'esecutore.</span><span class="sxs-lookup"><span data-stu-id="ddec8-126">For example, the metadata that describes the person who performed a song is named "Artist" and the value associated with it typically is a text string containing the performer's name.</span></span> <span data-ttu-id="ddec8-127">Ogni nome di metadati univoco è denominato *attributo*.</span><span class="sxs-lookup"><span data-stu-id="ddec8-127">Each unique metadata name is called an *attribute*.</span></span> <span data-ttu-id="ddec8-128">Per un elenco degli attributi supportati, vedere il [riferimento all'attributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ddec8-128">For a listing of supported attributes, see the [Attribute Reference](attribute-reference.md).</span></span> <span data-ttu-id="ddec8-129">Per informazioni sull'uso degli attributi nel codice, vedere [attributi degli elementi multimediali](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="ddec8-129">For information about using attributes in code, see [Media Item Attributes](media-item-attributes.md).</span></span>

<span data-ttu-id="ddec8-130">Nelle sezioni seguenti vengono fornite ulteriori informazioni sull'utilizzo della libreria:</span><span class="sxs-lookup"><span data-stu-id="ddec8-130">The following sections provide more information about working with the library:</span></span>

-   [<span data-ttu-id="ddec8-131">Accesso alla libreria a livello di codice</span><span class="sxs-lookup"><span data-stu-id="ddec8-131">Accessing the Library Programmatically</span></span>](accessing-the-library-programmatically.md)
-   [<span data-ttu-id="ddec8-132">Informazioni sui servizi di libreria</span><span class="sxs-lookup"><span data-stu-id="ddec8-132">About Library Services</span></span>](about-library-services.md)

## <a name="related-topics"></a><span data-ttu-id="ddec8-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddec8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddec8-134">**Informazioni sul modello a oggetti del lettore**</span><span class="sxs-lookup"><span data-stu-id="ddec8-134">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




