---
description: Questo argomento fornisce una panoramica concettuale della tecnologia MUI (Multilingual User Interface), il supporto della piattaforma che fornisce per l'abilitazione di esperienze utente multilingue e i vantaggi offerti dall'ecosistema Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Panoramica di MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570854"
---
# <a name="overview-of-mui"></a><span data-ttu-id="d3982-103">Panoramica di MUI</span><span class="sxs-lookup"><span data-stu-id="d3982-103">Overview of MUI</span></span>

<span data-ttu-id="d3982-104">Questo argomento fornisce una panoramica concettuale della tecnologia MUI (Multilingual User Interface), il supporto della piattaforma che fornisce per l'abilitazione di esperienze utente multilingue e i vantaggi offerti dall'ecosistema Windows.</span><span class="sxs-lookup"><span data-stu-id="d3982-104">This topic provides a conceptual overview of the Multilingual User Interface (MUI) technology, the platform support it provides for enabling multilingual user experiences, and the benefits it offers to the Windows ecosystem.</span></span>

<span data-ttu-id="d3982-105">In questa pagina:</span><span class="sxs-lookup"><span data-stu-id="d3982-105">On this page:</span></span>

-   [<span data-ttu-id="d3982-106">Necessità di elaborazione multilingue</span><span class="sxs-lookup"><span data-stu-id="d3982-106">The need for multilingual computing</span></span>](#the-need-for-multilingual-computing)
-   [<span data-ttu-id="d3982-107">Il ruolo di MUI nell'abilitazione del calcolo multilingue</span><span class="sxs-lookup"><span data-stu-id="d3982-107">The role of MUI in enabling multilingual computing</span></span>](#the-role-of-mui-in-enabling-multilingual-computing)
-   [<span data-ttu-id="d3982-108">Concetti di base di MUI</span><span class="sxs-lookup"><span data-stu-id="d3982-108">Core concepts of MUI</span></span>](#core-concepts-of-mui)
-   [<span data-ttu-id="d3982-109">Cronologia di MUI in Windows</span><span class="sxs-lookup"><span data-stu-id="d3982-109">History of MUI in Windows</span></span>](#history-of-mui-in-windows)
-   [<span data-ttu-id="d3982-110">Vantaggi della tecnologia MUI</span><span class="sxs-lookup"><span data-stu-id="d3982-110">Benefits of MUI technology</span></span>](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a><span data-ttu-id="d3982-111">Necessità di elaborazione multilingue</span><span class="sxs-lookup"><span data-stu-id="d3982-111">The need for multilingual computing</span></span>

<span data-ttu-id="d3982-112">Per trarre vantaggio dalle opportunità di crescita offerte dai mercati internazionali, le piattaforme e le applicazioni Microsoft supportano più lingue, culture e mercati che mai.</span><span class="sxs-lookup"><span data-stu-id="d3982-112">To benefit from the growth opportunities presented by international markets, Microsoft's platforms and applications support more languages, cultures and markets than ever before.</span></span>

<span data-ttu-id="d3982-113">La lingua, le impostazioni cultura e le specifiche del mercato sono ancora estremamente rilevanti per gli utenti internazionali, nonostante le crescenti tendenze di globalizzazione.</span><span class="sxs-lookup"><span data-stu-id="d3982-113">Language, culture, and market specifics are still extremely relevant to international users, despite increasing globalization trends.</span></span> <span data-ttu-id="d3982-114">Il grafico a torta seguente mostra che i relatori non in lingua inglese costituiscono ancora il 91,5% della popolazione mondiale.</span><span class="sxs-lookup"><span data-stu-id="d3982-114">The following pie chart shows that non-English speakers still make up 91.5 percent of the world's population.</span></span>

![grafico a torta con tre segmenti; quello con etichetta "lingua inglese 91,5%" è notevolmente più grande rispetto alle altre due combinazioni](images/overview-of-mui-fig1.gif)

<span data-ttu-id="d3982-116">In tutto il mondo sono presenti 193 paesi e oltre 6.900 linguaggi di vita noti attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="d3982-116">Worldwide, there are 193 countries and over 6,900 known living languages in use today.</span></span> <span data-ttu-id="d3982-117">L'inglese, nonostante il suo ruolo di linguaggio aziendale, viene parlato solo del 8,5% della popolazione del mondo come prima o secondo linguaggio.</span><span class="sxs-lookup"><span data-stu-id="d3982-117">English, despite its role as the world's business language, is only spoken by 8.5% of the world's population as a first or second language.</span></span> <span data-ttu-id="d3982-118">Per fornire informazioni Native al 94% della popolazione del mondo, è necessario che queste informazioni siano disponibili nella 347 (circa il 5%). dei linguaggi del mondo con almeno un milione di relatori.</span><span class="sxs-lookup"><span data-stu-id="d3982-118">To provide native information to 94% of the world's population, this information would need to be available in the 347 (about 5%) of the world's languages that have at least a million speakers.</span></span> <span data-ttu-id="d3982-119">Ciò vale soprattutto per quanto le tendenze di globalizzazione hanno accresciuto le aspettative di questi utenti riguardo alla tecnologia e alla sua disponibilità nei propri mercati.</span><span class="sxs-lookup"><span data-stu-id="d3982-119">This is especially true as globalization trends have increased the expectations of these users regarding technology and its availability in their markets.</span></span>

<span data-ttu-id="d3982-120">La necessità di localizzare il software in più lingue è aumentata nel corso degli anni e Microsoft offre ora Windows Vista e altri prodotti in più lingue che mai.</span><span class="sxs-lookup"><span data-stu-id="d3982-120">The need to localize software in more languages has increased over the years and Microsoft is now providing Windows Vista and other products in more languages than ever.</span></span> <span data-ttu-id="d3982-121">Questa evoluzione è particolarmente chiara con Microsoft Windows, dal momento che non supporta 30 lingue con Windows 98 a quasi 100 con Windows Vista, come illustrato nel seguente grafico a barre.</span><span class="sxs-lookup"><span data-stu-id="d3982-121">This evolution is especially clear with Microsoft Windows, as it has gone from supporting 30 languages with Windows 98 to almost 100 with Windows Vista, as illustrated in the following bar chart.</span></span>

![grafico a barre che mostra che il numero di lingue è molto più grande in Windows Vista rispetto a Windows 98 o Windows XP](images/overview-of-mui-fig2.gif)

<span data-ttu-id="d3982-123">*Figura 2: numero di lingue supportate dalle versioni di Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="d3982-123">*Figure 2—Number of languages supported by Microsoft Windows releases*</span></span>

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a><span data-ttu-id="d3982-124">Il ruolo di MUI nell'abilitazione del calcolo multilingue</span><span class="sxs-lookup"><span data-stu-id="d3982-124">The role of MUI in enabling multilingual computing</span></span>

<span data-ttu-id="d3982-125">Come illustrato nella sezione precedente, la [globalizzazione](glossary-for-understanding-mui.md) e la [localizzazione](glossary-for-understanding-mui.md) delle applicazioni sono diventati una necessità in un mondo integrato più a livello globale.</span><span class="sxs-lookup"><span data-stu-id="d3982-125">As discussed in the previous section, [globalization](glossary-for-understanding-mui.md) and [localization](glossary-for-understanding-mui.md) of applications have become a necessity in a more globally integrated world.</span></span> <span data-ttu-id="d3982-126">In particolare, dato che sempre più aziende si trovano a livello globale, internamente o attraverso le loro reti aziendali, la necessità di applicazioni multilingue è in continua crescita.</span><span class="sxs-lookup"><span data-stu-id="d3982-126">In particular, as more and more enterprises are going global, either internally or through their business networks, the need for multi-lingual applications is increasing dramatically.</span></span> <span data-ttu-id="d3982-127">Sono quindi gli ostacoli che attualmente queste società devono affrontare nella distribuzione globale di queste applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d3982-127">So are the hurdles that these companies currently face in deploying these applications globally.</span></span>

<span data-ttu-id="d3982-128">Per fornire supporto per più lingue per i sistemi operativi Windows, nonché per le applicazioni software create per la piattaforma Windows, sono necessarie nuove strategie che consentono di implementare tutti gli scenari principali con un sovraccarico minimo di progettazione.</span><span class="sxs-lookup"><span data-stu-id="d3982-128">Providing support for more languages for Windows operating systems, as well as software applications built for the Windows platform, requires new strategies which enable all major scenarios to be implemented with minimal engineering overhead.</span></span>

<span data-ttu-id="d3982-129">La tecnologia MUI è destinata agli sviluppatori e agli ISV che mirano a creare e supportare applicazioni multilingue per la piattaforma Windows.</span><span class="sxs-lookup"><span data-stu-id="d3982-129">MUI technology is targeted at developers and ISVs aiming to build and support multilingual applications for the Windows platform.</span></span> <span data-ttu-id="d3982-130">MUI è anche di importanza fondamentale per gli OEM e le aziende, che possono usarlo per distribuire il sistema operativo Windows e aggiungere applicazioni a computer in linguaggi diversi tramite la distribuzione di un'unica immagine.</span><span class="sxs-lookup"><span data-stu-id="d3982-130">MUI is also of key significance to OEMs and enterprises, who can leverage it to deploy the Windows operating system and add applications to computers across different languages through single image deployment.</span></span>

## <a name="core-concepts-of-mui"></a><span data-ttu-id="d3982-131">Concetti di base di MUI</span><span class="sxs-lookup"><span data-stu-id="d3982-131">Core concepts of MUI</span></span>

<span data-ttu-id="d3982-132">L'idea fondamentale della tecnologia MUI è [separare l'archiviazione delle risorse localizzabili dal codice sorgente dell'applicazione](mui-fundamental-concepts-explained.md), in modo da poter progettare un'applicazione multilingue come una combinazione di un file binario Core indipendente dalla lingua e un set di file di risorse localizzati specifici del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="d3982-132">The fundamental idea behind MUI is to [separate the storage of localizable resources from application source code](mui-fundamental-concepts-explained.md), so as to be able to architect any multilingual application as a combination of a language-neutral core binary and a set of language-specific localized resource files.</span></span>

<span data-ttu-id="d3982-133">Una volta che il codice sorgente dell'applicazione viene archiviato separatamente dalle risorse localizzate, diventa semplice [caricare dinamicamente le risorse localizzate appropriate](mui-fundamental-concepts-explained.md) per un determinato contesto dell'applicazione in base a una logica che prende in considerazione le impostazioni a livello di sistema, utente e applicazione per la lingua dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d3982-133">Once application source code is stored separately from the localized resources, it becomes easy to [dynamically load the appropriate localized resources](mui-fundamental-concepts-explained.md) for a given application context based on a logic that takes into account system, user and application-level settings for the user interface language.</span></span>

<span data-ttu-id="d3982-134">Questi attributi fondamentali di MUI contribuiscono a semplificare gli scenari aziendali, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d3982-134">These fundamental attributes of MUI help facilitate business scenarios such as:</span></span>

-   <span data-ttu-id="d3982-135">Un modello di localizzazione migliorato per l'interfaccia utente e il contenuto della guida, tramite la separazione fisica del codice sorgente dell'applicazione e le risorse localizzabili.</span><span class="sxs-lookup"><span data-stu-id="d3982-135">An improved localization model for user interface and help content, via the physical separation of application source code and localizable resources.</span></span>
-   <span data-ttu-id="d3982-136">Trattare le risorse localizzabili come contenuto dinamico e caricarle in base alle impostazioni della lingua dell'interfaccia utente e alle preferenze di fallback.</span><span class="sxs-lookup"><span data-stu-id="d3982-136">Treating the localizable resources as dynamic content and loading them according to the UI language settings and fallback preferences.</span></span> <span data-ttu-id="d3982-137">Questo consente scenari come:</span><span class="sxs-lookup"><span data-stu-id="d3982-137">This enables scenarios such as:</span></span>
    -   <span data-ttu-id="d3982-138">Passare da una lingua dell'interfaccia utente a un'altra in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d3982-138">Switching from one UI language to another one at run-time.</span></span>
    -   <span data-ttu-id="d3982-139">Creazione di immagini di distribuzione singola a livello di area o globale che coprono un set di lingue per OEM e aziende.</span><span class="sxs-lookup"><span data-stu-id="d3982-139">Creating regional or worldwide single deployment images that cover a set of languages for OEMs and enterprises.</span></span>

## <a name="history-of-mui-in-windows"></a><span data-ttu-id="d3982-140">Cronologia di MUI in Windows</span><span class="sxs-lookup"><span data-stu-id="d3982-140">History of MUI in Windows</span></span>

<span data-ttu-id="d3982-141">Il livello di supporto disponibile per un'esperienza utente multilingue a livello di sistema operativo Windows e per lo sviluppo di applicazioni multilingue sulla piattaforma Windows si è evoluto nel tempo e nelle diverse versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="d3982-141">The level of support available for a multilingual user experience at the Windows operating system level and for multilingual application development on the Windows platform has evolved over time and across the different versions of Windows.</span></span>

<span data-ttu-id="d3982-142">Le funzionalità supportate [prima di Windows Vista](evolution-of-mui-support-across-windows-versions.md) erano abbastanza semplici, con immagini di Windows in una sola lingua e un'opzione per l'aggiunta di interfacce utente multilingue in scenari specifici.</span><span class="sxs-lookup"><span data-stu-id="d3982-142">The supported functionality [before Windows Vista](evolution-of-mui-support-across-windows-versions.md) was fairly basic, with single-language Windows images and an option to add-on Multilingual User Interface Packs in specific scenarios.</span></span> <span data-ttu-id="d3982-143">Non è disponibile alcun supporto per gli sviluppatori per le applicazioni multilingue.</span><span class="sxs-lookup"><span data-stu-id="d3982-143">No developer support for multilingual applications was available.</span></span>

<span data-ttu-id="d3982-144">[Con Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft ha realizzato un investimento significativo in MUI e Windows Vista è stato creato da zero su una piattaforma MUI.</span><span class="sxs-lookup"><span data-stu-id="d3982-144">[With Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft made a significant investment in MUI, and Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="d3982-145">Sebbene questo rappresenti un importante progresso nella strategia di localizzazione di Windows, poiché si tratta di una chiave fondamentale per Microsoft per fornire Windows in più lingue, è prima di tutto un ottimo vantaggio per gli utenti, gli sviluppatori e i clienti di Windows.</span><span class="sxs-lookup"><span data-stu-id="d3982-145">While this represents a major advance in Windows localization strategy, as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users, developers, and customers.</span></span> <span data-ttu-id="d3982-146">Offre diversi vantaggi principali, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d3982-146">It provides several major benefits such as:</span></span>

-   <span data-ttu-id="d3982-147">Sistema operativo indipendente dalla lingua con supporto incorporato per MUI.</span><span class="sxs-lookup"><span data-stu-id="d3982-147">A language-neutral operating system with built-in support for MUI.</span></span>
-   <span data-ttu-id="d3982-148">Creazione di pacchetti, distribuzione e installazione configurabili per supportare scenari multilingue.</span><span class="sxs-lookup"><span data-stu-id="d3982-148">Configurable packaging, deployment, and installation to support multilingual scenarios.</span></span>
-   <span data-ttu-id="d3982-149">Distribuzione con un'unica immagine con più lingue.</span><span class="sxs-lookup"><span data-stu-id="d3982-149">Single-image deployment with multiple languages.</span></span>
-   <span data-ttu-id="d3982-150">Un modello di manutenzione migliorato in cui il codice eseguibile può essere aggiornato indipendentemente dalle risorse.</span><span class="sxs-lookup"><span data-stu-id="d3982-150">An improved servicing model where the executable code can be updated independently of the resources.</span></span>
-   <span data-ttu-id="d3982-151">Supporto per gli sviluppatori per la creazione di applicazioni multilingue.</span><span class="sxs-lookup"><span data-stu-id="d3982-151">Developer support for building multilingual applications.</span></span>

<span data-ttu-id="d3982-152">La tabella seguente fornisce una panoramica dettagliata del supporto della piattaforma Windows per MUI:</span><span class="sxs-lookup"><span data-stu-id="d3982-152">The following table provides a detailed overview of the Windows platform support for MUI:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3982-153">Category</span><span class="sxs-lookup"><span data-stu-id="d3982-153">Category</span></span></th>
<th><span data-ttu-id="d3982-154">Supporto</span><span class="sxs-lookup"><span data-stu-id="d3982-154">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3982-155">Versioni di Windows supportate (solo supporto del sistema operativo)</span><span class="sxs-lookup"><span data-stu-id="d3982-155">Supported Windows versions (OS support only)</span></span></td>
<td><ul>
<li><span data-ttu-id="d3982-156">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d3982-156">Windows 2000 Professional</span></span></li>
<li><span data-ttu-id="d3982-157">Famiglia di server Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d3982-157">Windows 2000 Server family</span></span></li>
<li><span data-ttu-id="d3982-158">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="d3982-158">Windows XP Professional</span></span></li>
<li><span data-ttu-id="d3982-159">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="d3982-159">Windows XP Tablet PC Edition</span></span></li>
<li><span data-ttu-id="d3982-160">Famiglia Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3982-160">Windows Server 2003 family</span></span></li>
<li><span data-ttu-id="d3982-161">Windows XP Embedded</span><span class="sxs-lookup"><span data-stu-id="d3982-161">Windows XP Embedded</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3982-162">Versioni di Windows supportate (supporto per applicazioni del sistema operativo &)</span><span class="sxs-lookup"><span data-stu-id="d3982-162">Supported Windows versions (OS & application support)</span></span></td>
<td><ul>
<li><span data-ttu-id="d3982-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3982-163">Windows Vista</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3982-164">Versioni di Windows non supportate</span><span class="sxs-lookup"><span data-stu-id="d3982-164">Unsupported Windows versions</span></span></td>
<td><ul>
<li><span data-ttu-id="d3982-165">Windows 9x</span><span class="sxs-lookup"><span data-stu-id="d3982-165">Windows 9x</span></span></li>
<li><span data-ttu-id="d3982-166">Windows me</span><span class="sxs-lookup"><span data-stu-id="d3982-166">Windows Me</span></span></li>
<li><span data-ttu-id="d3982-167">Windows XP Home Edition</span><span class="sxs-lookup"><span data-stu-id="d3982-167">Windows XP Home Edition</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a><span data-ttu-id="d3982-168">Vantaggi della tecnologia MUI</span><span class="sxs-lookup"><span data-stu-id="d3982-168">Benefits of MUI technology</span></span>

<span data-ttu-id="d3982-169">MUI influisca positivamente su più aspetti dell'ecosistema Windows:</span><span class="sxs-lookup"><span data-stu-id="d3982-169">MUI positively impacts multiple aspects of the Windows ecosystem:</span></span>

-   <span data-ttu-id="d3982-170">[Vantaggi per gli sviluppatori](benefits-of-mui-explained.md): molti vantaggi sono offerti agli sviluppatori di applicazioni dalla disponibilità del supporto delle API MUI per creare applicazioni multilingue modellate in base agli stessi principi del supporto multilingue nel sistema operativo Windows di base.</span><span class="sxs-lookup"><span data-stu-id="d3982-170">[Benefits for Developers](benefits-of-mui-explained.md): Numerous benefits are offered to application developers by the availability of MUI API support to build multilingual applications modeled on the same principles as the multilingual support in the core Windows operating system itself.</span></span> <span data-ttu-id="d3982-171">Questi vantaggi includono:</span><span class="sxs-lookup"><span data-stu-id="d3982-171">These benefits include:</span></span>
    -   <span data-ttu-id="d3982-172">Possibilità di fornire un'esperienza di visualizzazione della lingua coerente con i vantaggi offerti dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d3982-172">The ability to provide a display language experience that is consistent with what the operating system itself offers.</span></span>
    -   <span data-ttu-id="d3982-173">Possibilità di estendere facilmente il supporto del linguaggio per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3982-173">The ability to easily extend the language support for an application.</span></span>
    -   <span data-ttu-id="d3982-174">La possibilità di gestire e gestire facilmente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3982-174">The ability to easily maintain and service the application.</span></span>
    -   <span data-ttu-id="d3982-175">La possibilità di abilitare la distribuzione a immagine singola delle applicazioni da parte degli OEM.</span><span class="sxs-lookup"><span data-stu-id="d3982-175">The ability to enable single-image deployment of applications by OEMs.</span></span>
-   <span data-ttu-id="d3982-176">[Vantaggi per le aziende](benefits-of-mui-explained.md): il vantaggio principale offerto da MUI per le aziende è la possibilità di implementare, supportare e gestire la stessa immagine multilingue in tutto il mondo con un'unica installazione.</span><span class="sxs-lookup"><span data-stu-id="d3982-176">[Benefits for Enterprises](benefits-of-mui-explained.md): The major benefit that MUI offers for enterprises is the ability to roll out, support, and maintain the same multilingual image worldwide with a single installation.</span></span> <span data-ttu-id="d3982-177">Un'altra vittoria significativa è la possibilità di supportare desktop multilingue che offrono un'interazione senza problemi agli utenti con preferenze di lingua diverse.</span><span class="sxs-lookup"><span data-stu-id="d3982-177">Another significant win is the ability to support multilingual desktops that offer seamless interaction to users with different language preferences.</span></span>
-   <span data-ttu-id="d3982-178">[Vantaggi per gli OEM](benefits-of-mui-explained.md): il vantaggio principale per gli OEM è la singola installazione di immagini abilitata da MUI, con supporto per più linguaggi, che consente una gestione più efficace dell'inventario.</span><span class="sxs-lookup"><span data-stu-id="d3982-178">[Benefits for OEMs](benefits-of-mui-explained.md): The major benefit for OEMs is the single image installation that MUI enables, with support for multiple languages, which enables a more effective management of inventory.</span></span> <span data-ttu-id="d3982-179">Gli OEM traggono vantaggio anche dal supporto MUI per lo sviluppo di applicazioni, in quanto consentono loro di fornire applicazioni a valore aggiunto sulle proprie immagini, sfruttando al contempo l'installazione di una singola immagine, purché queste applicazioni siano abilitate per MUI.</span><span class="sxs-lookup"><span data-stu-id="d3982-179">OEMs also benefit from the MUI support for application development, as it enables them to provide value-add applications on their images while benefiting from the single image installation, as long as these applications are MUI-enabled.</span></span>

 

 




