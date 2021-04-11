---
title: Personalizzazione del recapito multimediale
description: Personalizzazione del recapito multimediale
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Playlist Windows Media Metafile, personalizzazione del recapito multimediale
- playlist, personalizzazione del recapito multimediale
- playlist di metafile, personalizzazione del recapito multimediale
- Playlist Windows Media Metafile, personalizzazione del recapito multimediale
- playlist, personalizzazione del recapito multimediale
- playlist di metafile, personalizzazione del recapito multimediale
- personalizzazione del recapito multimediale
- personalizzazione del recapito multimediale
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221018"
---
# <a name="personalizing-media-delivery"></a><span data-ttu-id="6236f-111">Personalizzazione del recapito multimediale</span><span class="sxs-lookup"><span data-stu-id="6236f-111">Personalizing Media Delivery</span></span>

<span data-ttu-id="6236f-112">A differenza della comunicazione unidirezionale che trasmette contenuto identico a un pubblico di massa, le tecnologie Windows Media forniscono gli strumenti per usare i dati demografici per individuare le trasmissioni.</span><span class="sxs-lookup"><span data-stu-id="6236f-112">Unlike one-way communication that broadcasts identical content to a mass audience, Windows Media Technologies provides you with the tools to use demographics to individualize broadcasts.</span></span> <span data-ttu-id="6236f-113">Con Internet, la comunicazione bidirezionale su larga scala è immediatamente disponibile.</span><span class="sxs-lookup"><span data-stu-id="6236f-113">With the Internet, two-way communication on a large scale is readily available.</span></span> <span data-ttu-id="6236f-114">Questo interscambio dinamico di informazioni consente ai provider di contenuti di conoscerne i destinatari e rispondere con presentazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="6236f-114">This dynamic interchange of information enables content providers to know their audience and respond with customized presentations.</span></span>

<span data-ttu-id="6236f-115">Nell'esempio seguente, usando una società fittizia, viene illustrato come è possibile personalizzare la distribuzione di contenuti in streaming.</span><span class="sxs-lookup"><span data-stu-id="6236f-115">The following example, using a fictional company, illustrates how delivery of streaming content can be personalized.</span></span> <span data-ttu-id="6236f-116">In questa discussione si presuppone che l'utente abbia familiarità con Active Server pagine (file ASP o ASP) e definendo le variabili.</span><span class="sxs-lookup"><span data-stu-id="6236f-116">This discussion assumes that you are familiar with Active Server Pages (ASP, or .asp files) and defining variables.</span></span>

<span data-ttu-id="6236f-117">News Network è un'organizzazione di notizie di broadcast fittizio che ha ampliato le proprie operazioni per includere un sito Web.</span><span class="sxs-lookup"><span data-stu-id="6236f-117">News Network is a fictional broadcast news organization that has expanded its operations to include a website.</span></span> <span data-ttu-id="6236f-118">La funzionalità principale del sito è una sezione in cui gli utenti possono creare telegiornali personalizzati.</span><span class="sxs-lookup"><span data-stu-id="6236f-118">The main feature of the site is a section where users can create their own personalized newscasts.</span></span> <span data-ttu-id="6236f-119">Anziché visualizzare un telegiornale tradizionale destinato a un pubblico di massa, un utente visualizza un programma di notizie completo che contiene solo argomenti di interesse personale.</span><span class="sxs-lookup"><span data-stu-id="6236f-119">Instead of viewing a traditional newscast that is aimed at a mass audience, a user views a complete news program that contains only topics of personal interest.</span></span> <span data-ttu-id="6236f-120">La sequenza seguente descrive un'esperienza utente tipica.</span><span class="sxs-lookup"><span data-stu-id="6236f-120">The following sequence describes a typical user experience.</span></span>

1.  <span data-ttu-id="6236f-121">Un nuovo utente passa al sito e fa clic su **Crea il telegiornale personale**.</span><span class="sxs-lookup"><span data-stu-id="6236f-121">A new user goes to the site, and clicks **Create Your Personal Newscast**.</span></span>
2.  <span data-ttu-id="6236f-122">Verrà visualizzato un modulo preferenza.</span><span class="sxs-lookup"><span data-stu-id="6236f-122">A preference form opens.</span></span> <span data-ttu-id="6236f-123">In questo formato, l'utente risponde alle domande relative alle preferenze personali, ad esempio le storie di notizie preferite, le storie di notizie preferite, i passatempi e il metodo usuale per ricevere notizie giornaliere.</span><span class="sxs-lookup"><span data-stu-id="6236f-123">On this form, the user answers questions regarding personal preferences, such as favorite news stories, least favorite news stories, hobbies, and usual method of receiving daily news.</span></span>
3.  <span data-ttu-id="6236f-124">L'utente invia queste informazioni e, dopo alcuni secondi, Visualizza un telegiornale completo di 15 minuti che contiene contenuto del programma, transizioni e commerciali.</span><span class="sxs-lookup"><span data-stu-id="6236f-124">The user sends this information, and a few seconds later views a complete, 15-minute, personal newscast containing program content, transitions, and commercials.</span></span> <span data-ttu-id="6236f-125">La selezione di ogni elemento multimediale, inclusi gli annunci pubblicitari, si basa sul profilo utente e viene eseguita automaticamente con i componenti di Windows Media Technologies e gli strumenti Internet disponibili.</span><span class="sxs-lookup"><span data-stu-id="6236f-125">Selection of each media element, including commercials, is based on the user profile, and is accomplished automatically with Windows Media Technologies components and off-the-shelf Internet tools.</span></span>

<span data-ttu-id="6236f-126">L'elenco seguente descrive il modo in cui i vari strumenti interagiscono per creare un telegiornale personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6236f-126">The following list describes how the various tools interact to create a personalized newscast.</span></span>

1.  <span data-ttu-id="6236f-127">Il modulo di preferenza che l'utente compila è una pagina di Active Server (ASP) (Choices. asp).</span><span class="sxs-lookup"><span data-stu-id="6236f-127">The preference form that the user fills out is an Active Server Page (ASP) (Choices.asp).</span></span> <span data-ttu-id="6236f-128">I dati ottenuti dal formato preferenza vengono analizzati da due componenti server.</span><span class="sxs-lookup"><span data-stu-id="6236f-128">Data obtained from the preference form is analyzed by two server components.</span></span> <span data-ttu-id="6236f-129">Un componente usa le informazioni per eseguire una query su un database Microsoft SQL Server di storie di notizie.</span><span class="sxs-lookup"><span data-stu-id="6236f-129">One component uses the information to query a Microsoft SQL Server database of news stories.</span></span> <span data-ttu-id="6236f-130">L'altro componente è un server ad che usa un set complesso di regole in base ai requisiti contrattuali e ai dati demografici per pianificare gli annunci appropriati per l'utente in quel momento.</span><span class="sxs-lookup"><span data-stu-id="6236f-130">The other component is an ad server that uses a complex set of rules based on contractual requirements and demographics to schedule ads appropriate to the user at that time.</span></span>
2.  <span data-ttu-id="6236f-131">I due database restituiscono parti diverse di una playlist.</span><span class="sxs-lookup"><span data-stu-id="6236f-131">The two databases return different portions of a playlist.</span></span> <span data-ttu-id="6236f-132">Il database di News Story restituisce un set di voci di storie appropriate e il server di Active Directory restituisce un set di voci commerciali appropriate.</span><span class="sxs-lookup"><span data-stu-id="6236f-132">The news story database returns a set of appropriate story Entries, and the ad server returns a set of appropriate commercial Entries.</span></span>
3.  <span data-ttu-id="6236f-133">Una seconda pagina ASP (PlayShow. asp) riceve le voci dal database di News Story e da ad server e combina quelle con le voci di visualizzazione standard di apertura, chiusura e transizione.</span><span class="sxs-lookup"><span data-stu-id="6236f-133">A second ASP page (PlayShow.asp) receives the Entries from the news story database and ad server, and combines those with standard show open, close, and transition Entries.</span></span> <span data-ttu-id="6236f-134">Tutte le voci vengono quindi disposte in base al modello fornito da PlayShow. asp e la pagina ASP restituisce una playlist per l'utente.</span><span class="sxs-lookup"><span data-stu-id="6236f-134">All Entries are then laid out according to the template provided by PlayShow.asp, and the ASP page returns a playlist to the user.</span></span>
4.  <span data-ttu-id="6236f-135">Il controllo Windows Media Player incorporato nel computer dell'utente riproduce la playlist dall'inizio alla fine e l'utente visualizza un telegiornale personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6236f-135">The embedded Windows Media Player control on the user's computer plays the playlist from beginning to end, and the user views a personalized newscast.</span></span>

<span data-ttu-id="6236f-136">L'esempio seguente è una parte di un file di playlist che un utente può ricevere.</span><span class="sxs-lookup"><span data-stu-id="6236f-136">The following example is a portion of a playlist file that a user might receive.</span></span> <span data-ttu-id="6236f-137">Ad essi sono stati aggiunti banner ad, collegamenti MOREINFO ed ABSTRACT.</span><span class="sxs-lookup"><span data-stu-id="6236f-137">Ad banners, MOREINFO links, and ABSTRACTS have been added to it.</span></span>


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   <span data-ttu-id="6236f-138">Ogni riferimento a società, organizzazioni, prodotti, persone ed eventi utilizzati negli esempi è puramente casuale</span><span class="sxs-lookup"><span data-stu-id="6236f-138">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="6236f-139">e ha il solo scopo di illustrare l'uso del prodotto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6236f-139">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6236f-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6236f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6236f-141">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="6236f-141">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6236f-142">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="6236f-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6236f-143">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="6236f-143">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6236f-144">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6236f-144">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6236f-145">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6236f-145">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




