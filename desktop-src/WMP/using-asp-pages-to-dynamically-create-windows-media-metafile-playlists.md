---
title: Utilizzo di pagine ASP per la creazione dinamica di playlist di metafile di Windows Media
description: Utilizzo di pagine ASP per la creazione dinamica di playlist di metafile di Windows Media
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Playlist Windows Media Metafile, creazione
- playlist di metafile, creazione
- playlist, creazione
- Playlist Windows Media Metafile, creazione dinamica
- playlist di metafile, creazione dinamica
- playlist, creazione dinamica
- Playlist Windows Media Metafile, pagine ASP
- playlist di metafile, pagine ASP
- playlist, pagine ASP
- creazione di playlist Windows Media Metafile
- creazione dinamica di playlist Windows Media Metafile
- ASP (pagine)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515688"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a><span data-ttu-id="15934-115">Utilizzo di pagine ASP per la creazione dinamica di playlist di metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="15934-115">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>

<span data-ttu-id="15934-116">È possibile utilizzare Active Server pagine (file ASP o ASP) per generare in modo dinamico le playlist in base alle informazioni fornite dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="15934-116">You can use Active Server Pages (ASP, or .asp files) to dynamically generate playlists based on information provided by users.</span></span> <span data-ttu-id="15934-117">Una pagina ASP è una pagina Web dinamica utilizzata insieme a Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="15934-117">An ASP page is a dynamic webpage used in conjunction with Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="15934-118">ASP è un ambiente in cui è possibile combinare HTML, script e componenti server ActiveX riutilizzabili per creare soluzioni aziendali dinamiche e potenti basate sul Web.</span><span class="sxs-lookup"><span data-stu-id="15934-118">ASP is an environment in which you can combine HTML, scripts, and reusable ActiveX server components to create dynamic and powerful Web-based business solutions.</span></span> <span data-ttu-id="15934-119">Le pagine ASP consentono l'esecuzione di script sul lato server per IIS con supporto nativo sia per Microsoft Visual Basic Scripting Edition (VBScript) che per Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="15934-119">ASP pages enable server-side scripting for IIS with native support for both Microsoft Visual Basic Scripting Edition (VBScript) and Microsoft JScript.</span></span> <span data-ttu-id="15934-120">In questa discussione si presuppone che l'utente abbia familiarità con ASP e definendo le variabili.</span><span class="sxs-lookup"><span data-stu-id="15934-120">This discussion assumes that you are familiar with ASP and defining variables.</span></span>

<span data-ttu-id="15934-121">Tutte le informazioni di intestazione devono essere contenute nella prima riga della stringa di pagina ASP restituita a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="15934-121">All header information must be contained on the first line of the ASP page string returned to Windows Media Player.</span></span>

<span data-ttu-id="15934-122">Quando si usano le pagine ASP per generare playlist, è necessario specificare i valori per le proprietà **ContentType** dell'oggetto **risposta** e la **scadenza** della pagina ASP a causa di problemi di latenza con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="15934-122">When you use ASP pages to generate playlists, you must specify values for the **Response** object's **ContentType** and **expires** properties in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="15934-123">Il valore **Response. ContentType** deve essere un'estensione di nome file valida per i file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="15934-123">The **Response.ContentType** value must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="15934-124">I valori accettabili sono WMA, Wax, WMV, WVX, ASF e ASX.</span><span class="sxs-lookup"><span data-stu-id="15934-124">Acceptable values include wma, wax, wmv, wvx, asf, and asx.</span></span>

<span data-ttu-id="15934-125">La proprietà **Response. Expires** specifica il periodo di tempo, in secondi, in cui Windows Media Player memorizza nella cache il file della playlist.</span><span class="sxs-lookup"><span data-stu-id="15934-125">The **Response.expires** property specifies the length of time, in seconds, that Windows Media Player caches the playlist file.</span></span> <span data-ttu-id="15934-126">Se si specifica un valore pari a zero, in Windows Media Player richiesta una nuova playlist dal server ogni volta che l'utente aggiorna la pagina.</span><span class="sxs-lookup"><span data-stu-id="15934-126">Specifying a value of zero results in Windows Media Player requesting a new playlist from the server each time the user refreshes the page.</span></span>

<span data-ttu-id="15934-127">Per informazioni dettagliate sull'uso dell'oggetto **risposta** nelle pagine Active Server, vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="15934-127">See the Platform SDK for details about using the **Response** object in Active Server Pages.</span></span>

<span data-ttu-id="15934-128">Il codice seguente è un esempio di pagina ASP utilizzata per generare una playlist di Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="15934-128">The following code is an example of an ASP page used to generate a Windows Media metafile playlist.</span></span>


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="15934-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15934-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15934-130">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="15934-130">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




