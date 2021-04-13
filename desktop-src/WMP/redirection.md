---
title: Reindirizzamento
description: Reindirizzamento
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Playlist Windows Media Metafile, Reindirizzamento
- playlist, Reindirizzamento
- playlist di metafile, Reindirizzamento
- Media Player di Windows, Reindirizzamento
- reindirizzamento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328572"
---
# <a name="redirection"></a><span data-ttu-id="0abdd-108">Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="0abdd-108">Redirection</span></span>

<span data-ttu-id="0abdd-109">Nella playlist il browser viene reindirizzato a Windows Media Player per riprodurre il flusso multimediale o il file multimediale designato.</span><span class="sxs-lookup"><span data-stu-id="0abdd-109">The playlist will redirect the browser to Windows Media Player to play the designated media stream or media file.</span></span> <span data-ttu-id="0abdd-110">La playlist di metafile più semplice contiene solo il Uniform Resource Locator (URL) di un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="0abdd-110">The most basic metafile playlist contains only the Uniform Resource Locator (URL) of a media file.</span></span>

<span data-ttu-id="0abdd-111">Per creare una playlist di metafile di base, aprire l'editor di testo preferito, ad esempio il blocco note Microsoft, quindi digitare il codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="0abdd-111">To create a basic metafile playlist, open your favorite text editor, such as Microsoft Notepad, and type the following example code.</span></span>


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



<span data-ttu-id="0abdd-112">Sostituire un percorso valido del file Windows Media usando la sintassi riportata nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0abdd-112">Substitute a valid path to your Windows Media file using the syntax in the following table.</span></span>



| <span data-ttu-id="0abdd-113">Origine del contenuto</span><span class="sxs-lookup"><span data-stu-id="0abdd-113">Source of content</span></span>                                                                                 | <span data-ttu-id="0abdd-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0abdd-114">Syntax</span></span>                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0abdd-115">Il contenuto è un file in un server Windows Media</span><span class="sxs-lookup"><span data-stu-id="0abdd-115">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="0abdd-116">mms://ServerName/Path/FileName.wma</span><span class="sxs-lookup"><span data-stu-id="0abdd-116">mms://ServerName/Path/FileName.wma</span></span>        |
| <span data-ttu-id="0abdd-117">Il contenuto è un multicast broadcast a cui si accede da un Windows Media Station</span><span class="sxs-lookup"><span data-stu-id="0abdd-117">Content is a broadcast multicast that is accessed from a Windows Media station</span></span>                    | https://WebServerName/Stations/kxyz.nsc    |
| <span data-ttu-id="0abdd-118">Il contenuto è un unicast broadcast a cui si accede da un punto di pubblicazione in un server Windows Media</span><span class="sxs-lookup"><span data-stu-id="0abdd-118">Content is a broadcast unicast that is accessed from a publishing point on a Windows Media server</span></span> | <span data-ttu-id="0abdd-119">mms://ServerName/PublishingPointAlias</span><span class="sxs-lookup"><span data-stu-id="0abdd-119">mms://ServerName/PublishingPointAlias</span></span>     |
| <span data-ttu-id="0abdd-120">Il contenuto è un file in un server Web</span><span class="sxs-lookup"><span data-stu-id="0abdd-120">Content is a file on a web server</span></span>                                                                 | https://WebServerName/Path/Filename.wma    |
| <span data-ttu-id="0abdd-121">Il contenuto è un file su un disco rigido locale</span><span class="sxs-lookup"><span data-stu-id="0abdd-121">Content is a file on a local hard disk</span></span>                                                            | <span data-ttu-id="0abdd-122">file://c: \\ percorso \\ nomefile. WMA</span><span class="sxs-lookup"><span data-stu-id="0abdd-122">file://c:\\Path\\Filename.wma</span></span>             |
| <span data-ttu-id="0abdd-123">Il contenuto è un file in una condivisione di rete</span><span class="sxs-lookup"><span data-stu-id="0abdd-123">Content is a file on a network share</span></span>                                                              | <span data-ttu-id="0abdd-124">file:// \\ \\ NomeServer \\ percorso \\ nomefile. WMA</span><span class="sxs-lookup"><span data-stu-id="0abdd-124">file://\\\\ServerName\\Path\\Filename.wma</span></span> |
| <span data-ttu-id="0abdd-125">Il contenuto è un file in un server Windows Media</span><span class="sxs-lookup"><span data-stu-id="0abdd-125">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="0abdd-126">mms://ServerName/Path/FileName.wmv</span><span class="sxs-lookup"><span data-stu-id="0abdd-126">mms://ServerName/Path/FileName.wmv</span></span>        |



 

<span data-ttu-id="0abdd-127">Salvare il file creato con un nome file e un'estensione, come descritto in [estensioni di file](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0abdd-127">Save the file you have created with a file name and extension as described in [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="0abdd-128">Fare doppio clic su di esso in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="0abdd-128">Double-click it in Windows Explorer.</span></span> <span data-ttu-id="0abdd-129">Windows Media Player dovrebbe aprire e avviare lo streaming del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0abdd-129">Windows Media Player should open and start streaming the content.</span></span> <span data-ttu-id="0abdd-130">È possibile salvare il file nel server Web, insieme alle pagine Web, e collegarlo a un elemento **href** oppure incorporarlo in una pagina Web usando il tag **oggetto** di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0abdd-130">You can save the file to your web server, along with your webpages, and link to it with an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** tag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0abdd-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0abdd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0abdd-132">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="0abdd-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0abdd-133">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="0abdd-133">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0abdd-134">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0abdd-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0abdd-135">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0abdd-135">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




