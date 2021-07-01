---
title: Protocollo di servizi di indicizzazione del contenuto
description: Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119736"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="ea353-103">Protocollo di servizi di indicizzazione del contenuto</span><span class="sxs-lookup"><span data-stu-id="ea353-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="ea353-104">Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ea353-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ea353-105">Nelle versioni successive, usare [Windows Search.](../search/-search-3x-wds-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ea353-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="ea353-106">Specifica del protocollo, versione 0.12</span><span class="sxs-lookup"><span data-stu-id="ea353-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="ea353-107">1 Introduzione</span><span class="sxs-lookup"><span data-stu-id="ea353-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="ea353-108">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="ea353-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="ea353-109">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="ea353-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="ea353-110">1.3 Panoramica del protocollo (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="ea353-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="ea353-111">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="ea353-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="ea353-112">1.5 Prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="ea353-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="ea353-113">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="ea353-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="ea353-114">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="ea353-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="ea353-115">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="ea353-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="ea353-116">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="ea353-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="ea353-117">2 Messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="ea353-118">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="ea353-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="ea353-119">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="ea353-120">3 Dettagli del protocollo</span><span class="sxs-lookup"><span data-stu-id="ea353-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="ea353-121">3.1 Dettagli del server</span><span class="sxs-lookup"><span data-stu-id="ea353-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="ea353-122">3.2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="ea353-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="ea353-123">4 Esempi di protocollo</span><span class="sxs-lookup"><span data-stu-id="ea353-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="ea353-124">4.1 Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea353-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="ea353-125">4.2 Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ea353-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="ea353-126">5 Sicurezza</span><span class="sxs-lookup"><span data-stu-id="ea353-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="ea353-127">5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione</span><span class="sxs-lookup"><span data-stu-id="ea353-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="ea353-128">5.2 Indice dei parametri di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ea353-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="ea353-129">6 Indice del comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="ea353-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="ea353-130">Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea353-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="ea353-131">La documentazione di Workgroup Server Protocol Program (WSPP) è destinata all'uso in combinazione con la documentazione degli standard pubblici, l'arte di programmazione di rete e i concetti relativi ai sistemi distribuiti del gruppo di lavoro Windows e presuppone che il lettore abbia familiarità con il materiale di cui in questo articolo o abbia accesso immediato.</span><span class="sxs-lookup"><span data-stu-id="ea353-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="ea353-132">Una specifica del protocollo WSPP non richiede l'uso di strumenti di programmazione o ambienti di programmazione Microsoft per consentire a un licenziatato di sviluppare un'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="ea353-133">I licenziatati che hanno accesso agli strumenti e agli ambienti di programmazione Microsoft sono liberi di sfruttarli.</span><span class="sxs-lookup"><span data-stu-id="ea353-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="ea353-134">1 Introduzione</span><span class="sxs-lookup"><span data-stu-id="ea353-134">1 Introduction</span></span>

-   [<span data-ttu-id="ea353-135">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="ea353-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="ea353-136">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="ea353-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="ea353-137">1.3 Panoramica del protocollo (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="ea353-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="ea353-138">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="ea353-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="ea353-139">1.5 Prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="ea353-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="ea353-140">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="ea353-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="ea353-141">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="ea353-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="ea353-142">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="ea353-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="ea353-143">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="ea353-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="ea353-144">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="ea353-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="ea353-145">I termini seguenti sono definiti nella sezione Glossario di \[ \] MS-SYS:</span><span class="sxs-lookup"><span data-stu-id="ea353-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="ea353-146">GUID</span><span class="sxs-lookup"><span data-stu-id="ea353-146">GUID</span></span>
> -   <span data-ttu-id="ea353-147">Little Endian</span><span class="sxs-lookup"><span data-stu-id="ea353-147">Little Endian</span></span>
> -   <span data-ttu-id="ea353-148">Named Pipe</span><span class="sxs-lookup"><span data-stu-id="ea353-148">Named Pipe</span></span>
> -   <span data-ttu-id="ea353-149">Percorso</span><span class="sxs-lookup"><span data-stu-id="ea353-149">Path</span></span>

 

<span data-ttu-id="ea353-150">**Binding:** richiesta di includere una determinata **colonna** in un set **di righe restituito.**</span><span class="sxs-lookup"><span data-stu-id="ea353-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="ea353-151">**L'associazione** specifica una proprietà da includere nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="ea353-152">**Segnalibro:** marcatore che identifica in modo univoco una riga all'interno di un set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="ea353-153">**Catalogo:** unità di livello superiore dell'organizzazione nel servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="ea353-154">Rappresenta un set di documenti indicizzati su cui è possibile eseguire query usando il protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea353-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="ea353-155">**Categoria:** raggruppamento gerarchico di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="ea353-156">Ad esempio, un risultato della query contenente colonne autore e titolo può essere categorizzato in base all'autore.</span><span class="sxs-lookup"><span data-stu-id="ea353-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="ea353-157">Ogni gruppo di righe contenente lo stesso valore per author costituisce una categoria.</span><span class="sxs-lookup"><span data-stu-id="ea353-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="ea353-158">**Capitolo:** intervallo di righe **all'interno** di un set di **righe.**</span><span class="sxs-lookup"><span data-stu-id="ea353-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="ea353-159">**Colonna**: contenitore per un singolo tipo di informazioni in una **riga** .</span><span class="sxs-lookup"><span data-stu-id="ea353-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="ea353-160">Le colonne vengono mappate ai nomi delle proprietà e  specificano le proprietà usate per gli elementi dell'albero dei comandi della query **di** ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="ea353-161">**Albero dei comandi:** combinazione **di restrizioni,** **categorie** e **ordinamenti** specificati per la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="ea353-162">**Cursore:** entità usata come meccanismo per  lavorare con una  riga o un piccolo blocco di righe alla volta in un set di dati restituito in un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="ea353-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="ea353-163">Un **cursore** viene posizionato su una singola **riga all'interno** del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="ea353-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="ea353-164">Dopo aver posizionato il **cursore** su una riga, è possibile eseguire operazioni su tale riga o su un blocco **di righe** a partire da tale posizione. </span><span class="sxs-lookup"><span data-stu-id="ea353-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="ea353-165">**Handle**: token che può essere usato per identificare e accedere a **cursori,** **capitoli** e **segnalibri.**</span><span class="sxs-lookup"><span data-stu-id="ea353-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="ea353-166">**Index:** struttura persistente che contiene il contenuto di testo estratto dai file da un **servizio di indicizzazione.**</span><span class="sxs-lookup"><span data-stu-id="ea353-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="ea353-167">Include l'elenco di parole, che vengono archiviate insieme al nome file contenitore, al percorso della parola e alle **impostazioni locali.**</span><span class="sxs-lookup"><span data-stu-id="ea353-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="ea353-168">**Indicizzazione:** processo di estrazione di testo e proprietà dai file e archiviazione dei valori estratti negli indici **(per** il testo) e nella **cache** delle proprietà (per le proprietà).</span><span class="sxs-lookup"><span data-stu-id="ea353-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="ea353-169">**Servizio di indicizzazione:** servizio che crea cataloghi **indicizzati** per il contenuto e le proprietà dei file system.</span><span class="sxs-lookup"><span data-stu-id="ea353-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="ea353-170">Le applicazioni possono cercare nei cataloghi informazioni dai file nel file system.</span><span class="sxs-lookup"><span data-stu-id="ea353-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="ea353-171">**Impostazioni** locali: identificatore, come specificato \[ nell'appendice A di MS-GPSI, \] che specifica le preferenze correlate alla lingua.</span><span class="sxs-lookup"><span data-stu-id="ea353-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="ea353-172">Queste preferenze indicano la modalità di formattazione di date e ore, l'ordinamento alfabetico degli elementi, il confronto delle stringhe e così via.</span><span class="sxs-lookup"><span data-stu-id="ea353-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="ea353-173">**Query in linguaggio naturale:** query costruita usando il linguaggio umano anziché la sintassi di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="ea353-174">**Parola non** erta: parola ignorata dal servizio  di indicizzazione quando è presente nelle restrizioni specificate per la query di ricerca perché ha poco valore discriminatorio.</span><span class="sxs-lookup"><span data-stu-id="ea353-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="ea353-175">Gli esempi in inglese includono "a", "and" e "the".</span><span class="sxs-lookup"><span data-stu-id="ea353-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="ea353-176">**Cache delle proprietà:** cache delle proprietà dei file estratte da un **servizio di indicizzazione.**</span><span class="sxs-lookup"><span data-stu-id="ea353-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="ea353-177">**Indicizzazione delle proprietà:** processo  di  creazione di un indice di proprietà di tipo valore di un documento, tra cui autore, oggetto, tipo, conteggio delle parole, numero di pagine stampate e qualsiasi altra proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="ea353-178">**Restrizione:** set di condizioni che un file deve soddisfare per essere incluso nei risultati della ricerca restituiti dal servizio **di** indicizzazione in risposta a una query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="ea353-179">Una **restrizione** restringe lo stato attivo di  una query di ricerca, limitando i file che il servizio di indicizzazione includerà nei risultati della ricerca solo a quelli che soddisfano le condizioni.</span><span class="sxs-lookup"><span data-stu-id="ea353-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="ea353-180">**Riga**: raccolta di colonne **contenente** i valori delle proprietà che descrivono  un singolo file del set di file che soddisfano le restrizioni specificate nella query di ricerca inviata al servizio **di indicizzazione.**</span><span class="sxs-lookup"><span data-stu-id="ea353-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="ea353-181">**Set di righe:** set di **righe restituite** nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="ea353-182">**Ordinamento:** set di regole in una query di ricerca che definiscono l'ordinamento delle righe nel risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="ea353-183">Ogni regola è costituita da una proprietà (nome, dimensioni e così via) e da una direzione per l'ordinamento (crescente o decrescente).</span><span class="sxs-lookup"><span data-stu-id="ea353-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="ea353-184">Più regole vengono applicate in sequenza</span><span class="sxs-lookup"><span data-stu-id="ea353-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="ea353-185">**Proprietà di tipo testo:** proprietà che descrive il contenuto di un documento e ha solo testo non formattato associato al nome.</span><span class="sxs-lookup"><span data-stu-id="ea353-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="ea353-186">**Proprietà di tipo valore:** proprietà che descrive un singolo attributo di un intero documento.</span><span class="sxs-lookup"><span data-stu-id="ea353-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="ea353-187">Una proprietà di tipo valore ha un ID tipo di dati e un valore di tale tipo di dati associato al relativo nome.</span><span class="sxs-lookup"><span data-stu-id="ea353-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="ea353-188">**Radice virtuale:** percorso alternativo di una cartella.</span><span class="sxs-lookup"><span data-stu-id="ea353-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="ea353-189">Una cartella fisica può avere zero o più radici virtuali.</span><span class="sxs-lookup"><span data-stu-id="ea353-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="ea353-190">I percorsi che iniziano con una radice virtuale sono denominati percorsi virtuali.</span><span class="sxs-lookup"><span data-stu-id="ea353-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="ea353-191">Ad esempio, /server/vanityroot potrebbe essere una radice virtuale di C: \\ cartella \\ Web \\ IIS1.</span><span class="sxs-lookup"><span data-stu-id="ea353-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="ea353-192">Il file C: cartella Web IIS1default.htm un percorso virtuale di \\ \\ \\ \\ /server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="ea353-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="ea353-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** questi termini (in tutti i caratteri maiuscoli) vengono usati come descritto in \[ RFC2119. \]</span><span class="sxs-lookup"><span data-stu-id="ea353-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="ea353-194">Tutte le istruzioni di comportamento facoltativo usano MAY, SHOULD, o SHOULD NOT.</span><span class="sxs-lookup"><span data-stu-id="ea353-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="ea353-195">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="ea353-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="ea353-196">1.2.1 Riferimenti normativi</span><span class="sxs-lookup"><span data-stu-id="ea353-196">1.2.1 Normative References</span></span>

<span data-ttu-id="ea353-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="ea353-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="ea353-198">\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", giugno 2006.</span><span class="sxs-lookup"><span data-stu-id="ea353-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="ea353-199">\[MS-GPSI \] Microsoft Corporation, "Criteri di gruppo Installazione software Extension", giugno 2006.</span><span class="sxs-lookup"><span data-stu-id="ea353-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="ea353-200">\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions", maggio 2006.</span><span class="sxs-lookup"><span data-stu-id="ea353-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="ea353-201">\[MS-SYS \] Microsoft Corporation, "Panoramica del sistema v4", luglio 2006.</span><span class="sxs-lookup"><span data-stu-id="ea353-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="ea353-202">\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="ea353-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="ea353-203">\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="ea353-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="ea353-204">1.2.2 Riferimenti informativi</span><span class="sxs-lookup"><span data-stu-id="ea353-204">1.2.2 Informative References</span></span>

<span data-ttu-id="ea353-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="ea353-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="ea353-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution valori, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="ea353-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="ea353-207">1.3 Panoramica del protocollo (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="ea353-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="ea353-208">Un servizio **di indicizzazione del contenuto** consente di organizzare in modo efficiente le funzionalità estratte di una raccolta di documenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="ea353-209">Il protocollo CISP (Content Indexing Service Protocol) consente a un client di comunicare con un server che ospita un servizio di indicizzazione per eseguire query e consentire a un amministratore di gestire il server di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="ea353-210">Durante l'elaborazione dei file, un servizio di indicizzazione analizza un set di  documenti e riorganizza il contenuto in modo che le proprietà di tali documenti possano essere restituite in modo efficiente in risposta alle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="ea353-211">Una raccolta di documenti su cui è possibile eseguire query include un **catalogo** .</span><span class="sxs-lookup"><span data-stu-id="ea353-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="ea353-212">Un catalogo può contenere **un indice** (per riferimento rapido al testo) e una **cache** delle proprietà (per il recupero rapido dei valori delle proprietà).</span><span class="sxs-lookup"><span data-stu-id="ea353-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="ea353-213">Concettualmente, un catalogo è costituito da una "tabella" logica di proprietà con il testo o il valore e le impostazioni locali corrispondenti archiviate **nelle colonne** della tabella.</span><span class="sxs-lookup"><span data-stu-id="ea353-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="ea353-214">Ogni "riga" della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni "colonna" della tabella corrisponde a una proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="ea353-215">Le attività specifiche eseguite da CISP sono raggruppate in due aree funzionali:</span><span class="sxs-lookup"><span data-stu-id="ea353-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="ea353-216">Amministrazione remota dei cataloghi del servizio di indicizzazione,</span><span class="sxs-lookup"><span data-stu-id="ea353-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="ea353-217">Esecuzione di query remote dei cataloghi del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="ea353-218">1.3.1 Attività di amministrazione remota</span><span class="sxs-lookup"><span data-stu-id="ea353-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="ea353-219">CISP abilita le attività di gestione del catalogo del servizio di indicizzazione seguenti da un client:</span><span class="sxs-lookup"><span data-stu-id="ea353-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="ea353-220">Eseguire una query sullo stato corrente di un catalogo del servizio di indicizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="ea353-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="ea353-221">Aggiornare lo stato di un catalogo del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="ea353-222">Avviare il processo di indicizzazione per un particolare set di file.</span><span class="sxs-lookup"><span data-stu-id="ea353-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="ea353-223">Avviare l'ottimizzazione di un indice per migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="ea353-224">Tutte le attività di amministrazione remota seguono un semplice modello di richiesta/risposta.</span><span class="sxs-lookup"><span data-stu-id="ea353-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="ea353-225">Nel client non viene mantenuto alcuno stato per qualsiasi chiamata amministrativa e le chiamate amministrative possono essere effettuate in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="ea353-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="ea353-226">1.3.2 Esecuzione di query remote</span><span class="sxs-lookup"><span data-stu-id="ea353-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="ea353-227">CISP consente ai client di eseguire query di ricerca su un server remoto che ospita un servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="ea353-228">L'invio di una query di ricerca è un processo in più passaggi avviato dal client.</span><span class="sxs-lookup"><span data-stu-id="ea353-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="ea353-229">Attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="ea353-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="ea353-230">Il client richiede una connessione a un server che ospita un servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="ea353-231">Il client invia i parametri per la query di ricerca, che includono:</span><span class="sxs-lookup"><span data-stu-id="ea353-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="ea353-232">Restrizioni **per specificare** i documenti da includere e/o escludere dai risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="ea353-233">Ordine in cui devono essere restituiti i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="ea353-234">Colonne da restituire nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="ea353-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="ea353-235">Numero massimo di **righe** che devono essere restituite per la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="ea353-236">Tempo massimo per l'esecuzione della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="ea353-237">Dopo che il server ha riconosciuto la richiesta del client di avviare la query, il client può richiedere informazioni sullo stato della query, ma questo non è un passaggio obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea353-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="ea353-238">Il client specifica quindi le proprietà che il server deve includere nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="ea353-239">Il client richiede un set di risultati dal server e il server risponde inviando al client i valori delle proprietà per i file inclusi nei risultati per la query di ricerca del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="ea353-240">Se il valore di una proprietà è troppo grande per essere contenuto in un singolo buffer di risposta, il server non invierà la proprietà, ma imposterà lo stato della proprietà su posticipato.</span><span class="sxs-lookup"><span data-stu-id="ea353-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="ea353-241">Il client richiede quindi separatamente il valore della proprietà usando una serie di richieste per blocchi successivi del valore e quindi riprende la richiesta di altri valori.</span><span class="sxs-lookup"><span data-stu-id="ea353-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="ea353-242">Dopo che il client ha completato la query di ricerca e non richiede più risultati aggiuntivi, il client contatta il server per rilasciare la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="ea353-243">Dopo che il server ha rilasciato la query, il client può inviare una richiesta di disconnessione dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="ea353-244">La connessione viene quindi chiusa.</span><span class="sxs-lookup"><span data-stu-id="ea353-244">The connection is then closed.</span></span> <span data-ttu-id="ea353-245">In alternativa, il client può eseguire un'altra query e ripetere la sequenza dal passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="ea353-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="ea353-246">Comportamento di Windows: questo protocollo è implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea353-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="ea353-247">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="ea353-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="ea353-248">Il CISP si basa sul protocollo \[ SMB MS-SMB \] per il trasporto dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="ea353-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="ea353-249">Nessun altro protocollo dipende direttamente dal protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea353-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="ea353-250">*Comportamento di Windows: le applicazioni interagiscono in genere con un wrapper di interfaccia OLE DB \[ MSDN-OLEDB (ad esempio, un client di protocollo) e non \] direttamente con il protocollo.*</span><span class="sxs-lookup"><span data-stu-id="ea353-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="ea353-251">1.5 Prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="ea353-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="ea353-252">Si presuppone che il client abbia ottenuto il nome del server e un nome di catalogo prima che venga richiamato questo protocollo.</span><span class="sxs-lookup"><span data-stu-id="ea353-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="ea353-253">Il modo in cui un client esegue questa operazione non rientra nell'ambito di questa specifica.</span><span class="sxs-lookup"><span data-stu-id="ea353-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="ea353-254">Si presuppone anche che il client e il server hanno un'associazione di sicurezza utilizzabile con named pipe \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="ea353-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="ea353-255">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="ea353-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="ea353-256">CISP è progettato per l'esecuzione di query e la gestione dei cataloghi in un server remoto da un client.</span><span class="sxs-lookup"><span data-stu-id="ea353-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="ea353-257">CISP è deprecato in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea353-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="ea353-258">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="ea353-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="ea353-259">Questo protocollo non ha meccanismi di controllo delle versioni o negoziazione delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ea353-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="ea353-260">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="ea353-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="ea353-261">Questo protocollo usa HRESULT estendibili dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="ea353-262">I fornitori possono scegliere i propri valori per questo campo, purché il bit C (0x20000000) sia impostato come specificato nella sezione 4.1.1 di MS-SYS, a indicare che si tratta di un codice \[ \] cliente.</span><span class="sxs-lookup"><span data-stu-id="ea353-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="ea353-263">Questo protocollo usa anche i valori NTSTATUS presi dallo spazio dei numeri NTSTATUS definito in \[ MS-SYS \] .</span><span class="sxs-lookup"><span data-stu-id="ea353-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="ea353-264">I fornitori DEVONO riutilizzare questi valori con il significato indicato.</span><span class="sxs-lookup"><span data-stu-id="ea353-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="ea353-265">La scelta di qualsiasi altro valore rischia una collisione in futuro.</span><span class="sxs-lookup"><span data-stu-id="ea353-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="ea353-266">*Comportamento di Windows: Windows usa solo i valori specificati nella sezione 4.1.3 di \[ \] MS-SYS.*</span><span class="sxs-lookup"><span data-stu-id="ea353-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="ea353-267">1.8.1 ID proprietà</span><span class="sxs-lookup"><span data-stu-id="ea353-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="ea353-268">Le proprietà sono rappresentate da ID noti come ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="ea353-269">Ogni proprietà deve avere un identificatore univoco globale.</span><span class="sxs-lookup"><span data-stu-id="ea353-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="ea353-270">Questo identificatore è costituito da un **GUID** che rappresenta una raccolta di proprietà denominata set di proprietà più una stringa o un intero a 32 bit per identificare la proprietà all'interno del set.</span><span class="sxs-lookup"><span data-stu-id="ea353-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="ea353-271">Se viene usata la forma integer di ID, i valori 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE vengono considerati non validi.</span><span class="sxs-lookup"><span data-stu-id="ea353-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="ea353-272">I fornitori possono garantire che le proprietà siano definite in modo univoco inserendole in un set di proprietà definito dal proprio GUID.</span><span class="sxs-lookup"><span data-stu-id="ea353-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="ea353-273">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="ea353-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="ea353-274">Questo protocollo non ha assegnazioni di standard, ma solo assegnazioni private effettuate da Microsoft usando le procedure di allocazione specificate in altri protocolli.</span><span class="sxs-lookup"><span data-stu-id="ea353-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="ea353-275">Microsoft ha allocato questo protocollo named pipe come specificato in \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="ea353-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="ea353-276">L'assegnazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-276">The assignment is:</span></span>



| <span data-ttu-id="ea353-277">Parametro</span><span class="sxs-lookup"><span data-stu-id="ea353-277">Parameter</span></span> | <span data-ttu-id="ea353-278">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-278">Value</span></span>             | <span data-ttu-id="ea353-279">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ea353-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="ea353-280">Nome pipe</span><span class="sxs-lookup"><span data-stu-id="ea353-280">Pipe name</span></span> | <span data-ttu-id="ea353-281">\\pipe \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="ea353-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="ea353-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="ea353-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="ea353-283">2 Messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-283">2 Messages</span></span>

-   [<span data-ttu-id="ea353-284">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="ea353-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="ea353-285">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="ea353-286">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="ea353-286">2.1 Transport</span></span>

<span data-ttu-id="ea353-287">Tutti i messaggi DEVONO essere trasportati usando un named pipe, come specificato in \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="ea353-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="ea353-288">Viene usato il nome della pipe seguente:</span><span class="sxs-lookup"><span data-stu-id="ea353-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="ea353-289">\\pipe \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="ea353-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="ea353-290">Questo protocollo usa il protocollo named pipe SMB sottostante per recuperare l'identità del chiamante che ha effettuato la connessione come specificato nella sezione 2.2.8 di MS-SMB. Il client DEVE impostare SECURITY IDENTIFICATION come \[ ImpersonationLevel nella richiesta per aprire il \] \_ named pipe.</span><span class="sxs-lookup"><span data-stu-id="ea353-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="ea353-291">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-291">2.2 Message Syntax</span></span>

<span data-ttu-id="ea353-292">Diverse strutture e messaggi nelle sezioni seguenti fanno riferimento agli handle di capitolo o segnalibro.</span><span class="sxs-lookup"><span data-stu-id="ea353-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="ea353-293">Un handle è una struttura opaca lunga 32 bit che identifica in modo univoco un capitolo o un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="ea353-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="ea353-294">In genere, le applicazioni client ricevono valori di handle tramite chiamate al metodo . Tuttavia, esistono diversi valori noti che non devono essere ottenuti da un server, il cui significato è specificato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="ea353-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="ea353-295">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-295">Value</span></span>                         | <span data-ttu-id="ea353-296">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-297">Db \_ NULL \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="ea353-298">Handle di capitolo per il set di righe nonchaptered, contenente tutti i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="ea353-299">DBBMK \_ FIRST 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="ea353-300">Handle di segnalibro per un segnalibro che identifica la prima riga del set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="ea353-301">DBBMK \_ LAST 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="ea353-302">Handle di segnalibro per un segnalibro che identifica l'ultima riga nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="ea353-303">2.2.1 Strutture</span><span class="sxs-lookup"><span data-stu-id="ea353-303">2.2.1 Structures</span></span>

<span data-ttu-id="ea353-304">Questa sezione contiene informazioni dettagliate sulle strutture di dati definite e usate da CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="ea353-305">Tutti gli interi con segno a 2, 4 e 8 byte nelle strutture seguenti DEVONO essere trasferiti nell'ordine dei byte little endian.</span><span class="sxs-lookup"><span data-stu-id="ea353-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="ea353-306">Nella tabella seguente vengono riepilogate le strutture di dati definite in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="ea353-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="ea353-307">Struttura</span><span class="sxs-lookup"><span data-stu-id="ea353-307">Structure</span></span>                    | <span data-ttu-id="ea353-308">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea353-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="ea353-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="ea353-310">Contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata in una struttura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="ea353-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="ea353-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="ea353-312">Contiene una matrice multidimensionale.</span><span class="sxs-lookup"><span data-stu-id="ea353-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="ea353-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="ea353-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="ea353-314">Rappresenta i limiti per una dimensione di una matrice specificata in una struttura SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="ea353-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="ea353-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="ea353-315">CFullPropSpec</span></span>                | <span data-ttu-id="ea353-316">Contiene una specifica di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="ea353-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-317">CContentRestriction</span></span>          | <span data-ttu-id="ea353-318">Contiene una stringa di cui trovare una corrispondenza per un valore di proprietà nella cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="ea353-319">Chiave CKey</span><span class="sxs-lookup"><span data-stu-id="ea353-319">CKey</span></span>                         | <span data-ttu-id="ea353-320">Contiene un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="ea353-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="ea353-322">Contiene un valore della proprietà da associare a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="ea353-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="ea353-324">Contiene una corrispondenza di query in linguaggio naturale per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="ea353-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-325">CNodeRestriction</span></span>             | <span data-ttu-id="ea353-326">Contiene una matrice di nodi dell'albero dei comandi che specifica le restrizioni per una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="ea353-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-327">COccRestriction</span></span>              | <span data-ttu-id="ea353-328">Contiene la posizione di una parola in una frase.</span><span class="sxs-lookup"><span data-stu-id="ea353-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="ea353-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-329">CPropertyRestriction</span></span>         | <span data-ttu-id="ea353-330">Contiene un valore della proprietà da associare a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="ea353-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-331">CRangeRestriction</span></span>            | <span data-ttu-id="ea353-332">Contiene una restrizione su un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="ea353-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="ea353-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-333">CScopeRestriction</span></span>            | <span data-ttu-id="ea353-334">Contiene una restrizione sui file in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="ea353-335">CSort</span><span class="sxs-lookup"><span data-stu-id="ea353-335">CSort</span></span>                        | <span data-ttu-id="ea353-336">Identifica una colonna da ordinare.</span><span class="sxs-lookup"><span data-stu-id="ea353-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="ea353-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-337">CSynRestriction</span></span>              | <span data-ttu-id="ea353-338">Contiene una parola o i relativi sinonimi per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="ea353-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-339">CVectorRestriction</span></span>           | <span data-ttu-id="ea353-340">Contiene un'operazione OR ponderata su un nodo della struttura ad albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="ea353-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="ea353-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-341">CWordRestriction</span></span>             | <span data-ttu-id="ea353-342">Contiene una parola per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="ea353-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-343">CRestriction</span></span>                 | <span data-ttu-id="ea353-344">Contiene un nodo di un albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="ea353-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="ea353-345">CColumnSet</span></span>                   | <span data-ttu-id="ea353-346">Indica il numero di colonne da restituire.</span><span class="sxs-lookup"><span data-stu-id="ea353-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="ea353-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="ea353-347">CCategorizationSet</span></span>           | <span data-ttu-id="ea353-348">Contiene informazioni sul raggruppamento di un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="ea353-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="ea353-349">CCategorizationSpec</span></span>          | <span data-ttu-id="ea353-350">Contiene una definizione di categorie in cui verranno classificati i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="ea353-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="ea353-351">CDbColId</span></span>                     | <span data-ttu-id="ea353-352">Contiene una colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="ea353-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="ea353-353">CDbProp</span></span>                      | <span data-ttu-id="ea353-354">Contiene una proprietà .</span><span class="sxs-lookup"><span data-stu-id="ea353-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="ea353-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="ea353-355">CDbPropSet</span></span>                   | <span data-ttu-id="ea353-356">Contiene un set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="ea353-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="ea353-357">CPidMapper</span></span>                   | <span data-ttu-id="ea353-358">Contiene una matrice di ID di proprietà che specificano le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="ea353-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="ea353-359">CRowSeekAt</span></span>                   | <span data-ttu-id="ea353-360">Contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="ea353-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="ea353-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="ea353-362">Identifica il punto da cui iniziare il recupero per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="ea353-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="ea353-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="ea353-364">Identifica i segnalibri da cui recuperare le righe per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="ea353-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="ea353-365">CRowSeekNext</span></span>                 | <span data-ttu-id="ea353-366">Contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="ea353-367">Proprietà CRowset</span><span class="sxs-lookup"><span data-stu-id="ea353-367">CRowsetProperties</span></span>            | <span data-ttu-id="ea353-368">Contiene le informazioni di configurazione per una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="ea353-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="ea353-369">CSortSet</span></span>                     | <span data-ttu-id="ea353-370">Contiene l'ordinamento per una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="ea353-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="ea353-371">CTableColumn</span></span>                 | <span data-ttu-id="ea353-372">Contiene una colonna per il messaggio CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="ea353-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="ea353-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="ea353-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="ea353-374">Contiene un valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="ea353-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="ea353-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="ea353-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="ea353-376">La struttura CBaseStorageVariant contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata nella struttura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="ea353-377">0</span><span class="sxs-lookup"><span data-stu-id="ea353-377">0</span></span>

<span data-ttu-id="ea353-378">1</span><span class="sxs-lookup"><span data-stu-id="ea353-378">1</span></span>

<span data-ttu-id="ea353-379">2</span><span class="sxs-lookup"><span data-stu-id="ea353-379">2</span></span>

<span data-ttu-id="ea353-380">3</span><span class="sxs-lookup"><span data-stu-id="ea353-380">3</span></span>

<span data-ttu-id="ea353-381">4</span><span class="sxs-lookup"><span data-stu-id="ea353-381">4</span></span>

<span data-ttu-id="ea353-382">5</span><span class="sxs-lookup"><span data-stu-id="ea353-382">5</span></span>

<span data-ttu-id="ea353-383">6</span><span class="sxs-lookup"><span data-stu-id="ea353-383">6</span></span>

<span data-ttu-id="ea353-384">7</span><span class="sxs-lookup"><span data-stu-id="ea353-384">7</span></span>

<span data-ttu-id="ea353-385">8</span><span class="sxs-lookup"><span data-stu-id="ea353-385">8</span></span>

<span data-ttu-id="ea353-386">9</span><span class="sxs-lookup"><span data-stu-id="ea353-386">9</span></span>

<span data-ttu-id="ea353-387">1</span><span class="sxs-lookup"><span data-stu-id="ea353-387">1</span></span><br/> <span data-ttu-id="ea353-388">0</span><span class="sxs-lookup"><span data-stu-id="ea353-388">0</span></span><br/>

<span data-ttu-id="ea353-389">1</span><span class="sxs-lookup"><span data-stu-id="ea353-389">1</span></span>

<span data-ttu-id="ea353-390">2</span><span class="sxs-lookup"><span data-stu-id="ea353-390">2</span></span>

<span data-ttu-id="ea353-391">3</span><span class="sxs-lookup"><span data-stu-id="ea353-391">3</span></span>

<span data-ttu-id="ea353-392">4</span><span class="sxs-lookup"><span data-stu-id="ea353-392">4</span></span>

<span data-ttu-id="ea353-393">5</span><span class="sxs-lookup"><span data-stu-id="ea353-393">5</span></span>

<span data-ttu-id="ea353-394">6</span><span class="sxs-lookup"><span data-stu-id="ea353-394">6</span></span>

<span data-ttu-id="ea353-395">7</span><span class="sxs-lookup"><span data-stu-id="ea353-395">7</span></span>

<span data-ttu-id="ea353-396">8</span><span class="sxs-lookup"><span data-stu-id="ea353-396">8</span></span>

<span data-ttu-id="ea353-397">9</span><span class="sxs-lookup"><span data-stu-id="ea353-397">9</span></span>

<span data-ttu-id="ea353-398">2</span><span class="sxs-lookup"><span data-stu-id="ea353-398">2</span></span><br/> <span data-ttu-id="ea353-399">0</span><span class="sxs-lookup"><span data-stu-id="ea353-399">0</span></span><br/>

<span data-ttu-id="ea353-400">1</span><span class="sxs-lookup"><span data-stu-id="ea353-400">1</span></span>

<span data-ttu-id="ea353-401">2</span><span class="sxs-lookup"><span data-stu-id="ea353-401">2</span></span>

<span data-ttu-id="ea353-402">3</span><span class="sxs-lookup"><span data-stu-id="ea353-402">3</span></span>

<span data-ttu-id="ea353-403">4</span><span class="sxs-lookup"><span data-stu-id="ea353-403">4</span></span>

<span data-ttu-id="ea353-404">5</span><span class="sxs-lookup"><span data-stu-id="ea353-404">5</span></span>

<span data-ttu-id="ea353-405">6</span><span class="sxs-lookup"><span data-stu-id="ea353-405">6</span></span>

<span data-ttu-id="ea353-406">7</span><span class="sxs-lookup"><span data-stu-id="ea353-406">7</span></span>

<span data-ttu-id="ea353-407">8</span><span class="sxs-lookup"><span data-stu-id="ea353-407">8</span></span>

<span data-ttu-id="ea353-408">9</span><span class="sxs-lookup"><span data-stu-id="ea353-408">9</span></span>

<span data-ttu-id="ea353-409">3</span><span class="sxs-lookup"><span data-stu-id="ea353-409">3</span></span><br/> <span data-ttu-id="ea353-410">0</span><span class="sxs-lookup"><span data-stu-id="ea353-410">0</span></span><br/>

<span data-ttu-id="ea353-411">1</span><span class="sxs-lookup"><span data-stu-id="ea353-411">1</span></span>

<span data-ttu-id="ea353-412">vType</span><span class="sxs-lookup"><span data-stu-id="ea353-412">vType</span></span>

<span data-ttu-id="ea353-413">vData1</span><span class="sxs-lookup"><span data-stu-id="ea353-413">vData1</span></span>

<span data-ttu-id="ea353-414">vData2</span><span class="sxs-lookup"><span data-stu-id="ea353-414">vData2</span></span>

<span data-ttu-id="ea353-415">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-415">vValue (variable)</span></span>



 

<span data-ttu-id="ea353-416">**vType:** indicatore di tipo che indica il tipo di vValue.</span><span class="sxs-lookup"><span data-stu-id="ea353-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="ea353-417">DEVE essere uno dei valori VARENUM specificati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ea353-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="ea353-418">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-418">Value</span></span>                 | <span data-ttu-id="ea353-419">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-420">VT \_ EMPTY (0x0000)</span><span class="sxs-lookup"><span data-stu-id="ea353-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="ea353-421">vValue non è presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="ea353-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="ea353-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="ea353-423">vValue non è presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="ea353-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="ea353-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="ea353-425">Intero con segno a 1 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="ea353-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="ea353-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="ea353-427">Intero senza segno a 1 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="ea353-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="ea353-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="ea353-429">Intero con segno a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="ea353-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="ea353-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="ea353-431">Intero senza segno a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="ea353-432">VT \_ BOOL (0x000B)</span><span class="sxs-lookup"><span data-stu-id="ea353-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="ea353-433">Valore booleano; Intero a 2 byte contenente 0x0000 (FALSE) o 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="ea353-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="ea353-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="ea353-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="ea353-435">Intero con segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="ea353-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="ea353-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="ea353-437">Intero senza segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="ea353-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="ea353-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="ea353-439">Numero a virgola mobile IEEE a 32 bit, come definito in \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="ea353-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="ea353-440">VT \_ INT (0x0016)</span><span class="sxs-lookup"><span data-stu-id="ea353-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="ea353-441">Intero con segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="ea353-442">UINT \_ VT (0x0017)</span><span class="sxs-lookup"><span data-stu-id="ea353-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="ea353-443">Intero senza segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="ea353-444">ERRORE \_ VT (0x000A)</span><span class="sxs-lookup"><span data-stu-id="ea353-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="ea353-445">Intero senza segno a 4 byte contenente un HRESULT, come specificato in \[ \] MS-SYS.</span><span class="sxs-lookup"><span data-stu-id="ea353-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="ea353-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="ea353-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="ea353-447">Intero con segno a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="ea353-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="ea353-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="ea353-449">Intero senza segno a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="ea353-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="ea353-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="ea353-451">Numero a virgola mobile IEEE a 64 bit come definito in \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="ea353-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="ea353-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="ea353-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="ea353-453">Intero complementare a 8 byte a due (ridimensionato di 10.000).</span><span class="sxs-lookup"><span data-stu-id="ea353-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="ea353-454">VT \_ DATE (0x0007)</span><span class="sxs-lookup"><span data-stu-id="ea353-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="ea353-455">Numero a virgola mobile a 64 bit che rappresenta il numero di giorni a partire dalle 00.00.00 del 31 dicembre 1899 (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="ea353-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="ea353-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="ea353-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="ea353-457">Intero a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dalle 00.00.00 del 1° gennaio 1601 (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="ea353-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="ea353-458">VT \_ DECIMAL (0x000E)</span><span class="sxs-lookup"><span data-stu-id="ea353-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="ea353-459">Struttura DECIMAL come specificato nella sezione 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="ea353-460">\_CLSID VT (0x0048)</span><span class="sxs-lookup"><span data-stu-id="ea353-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="ea353-461">Valore binario a 16 byte contenente un GUID.</span><span class="sxs-lookup"><span data-stu-id="ea353-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="ea353-462">BLOB VT \_ (0x0041)</span><span class="sxs-lookup"><span data-stu-id="ea353-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="ea353-463">Numero intero senza segno a 4 byte di byte nel BLOB, seguito da tale numero di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="ea353-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="ea353-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="ea353-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="ea353-465">Numero intero senza segno a 4 byte di byte nella stringa, seguito da una stringa, come specificato di seguito in vValue.</span><span class="sxs-lookup"><span data-stu-id="ea353-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="ea353-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="ea353-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="ea353-467">Stringa ANSI con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="ea353-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="ea353-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="ea353-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="ea353-469">Stringa UNICODE Unicode con \[ \] terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="ea353-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="ea353-470">VT \_ VARIANT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="ea353-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="ea353-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="ea353-471">CBaseStorageVariant.</span></span> <span data-ttu-id="ea353-472">DEVE essere combinato con un modificatore di tipo VT \_ ARRAY o VT \_ VECTOR.</span><span class="sxs-lookup"><span data-stu-id="ea353-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="ea353-473">Nella tabella seguente vengono specificati i modificatori di tipo per vType.</span><span class="sxs-lookup"><span data-stu-id="ea353-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="ea353-474">I modificatori di tipo possono essere ORed binari con vType, per modificare il significato di vValue per indicare che si tratta di uno dei due tipi di matrice possibili.</span><span class="sxs-lookup"><span data-stu-id="ea353-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="ea353-475">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-475">Value</span></span>               | <span data-ttu-id="ea353-476">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-477">VETTORE \_ VT (0x1000)</span><span class="sxs-lookup"><span data-stu-id="ea353-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="ea353-478">Se l'indicatore di tipo viene combinato con VT VECTOR usando un operatore OR, vValue è una matrice conteggiata di \_ valori del tipo indicato.</span><span class="sxs-lookup"><span data-stu-id="ea353-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="ea353-479">Per informazioni dettagliate, vedere la sezione 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="ea353-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="ea353-480">Questo modificatore di tipo NON DEVE essere combinato con i tipi seguenti: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, VT \_ BLOB, VT \_ BLOB \_ OBJECT.</span><span class="sxs-lookup"><span data-stu-id="ea353-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="ea353-481">VT \_ ARRAY (0x2000)</span><span class="sxs-lookup"><span data-stu-id="ea353-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="ea353-482">Se l'indicatore di tipo viene combinato con VT ARRAY da un operatore OR, il valore è safeARRAY (come specificato nella sezione \_ 2.2.1.1.1.3) contenente i valori del tipo indicato.</span><span class="sxs-lookup"><span data-stu-id="ea353-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="ea353-483">Questo modificatore di tipo NON DEVE essere combinato con i tipi seguenti: VT \_ I8, \_ VT UI8, VT \_ FILETIME, \_ CLSID VT, BLOB \_ VT, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="ea353-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="ea353-484">**vData1:** quando vType è VT DECIMAL, il valore di questo campo viene specificato come campo Scale nella sezione \_ 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="ea353-485">Per tutti gli altri vType, il valore DEVE essere impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="ea353-486">**vData2:** quando vType è VT DECIMAL, il valore di questo campo viene specificato come campo Sign nella sezione \_ 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="ea353-487">Per tutti gli altri vType, il valore DEVE essere impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="ea353-488">**vValue:** valore per l'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="ea353-489">La sintassi DEVE essere come indicato nel campo vType.</span><span class="sxs-lookup"><span data-stu-id="ea353-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="ea353-490">La tabella seguente riepiloga le dimensioni per il campo vValue, a seconda del campo vType per i tipi di dati a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="ea353-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="ea353-491">La dimensione è espressa in byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-491">The size is in bytes.</span></span>



| <span data-ttu-id="ea353-492">vType</span><span class="sxs-lookup"><span data-stu-id="ea353-492">vType</span></span>                                                   | <span data-ttu-id="ea353-493">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ea353-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="ea353-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="ea353-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="ea353-495">1</span><span class="sxs-lookup"><span data-stu-id="ea353-495">1</span></span>    |
| <span data-ttu-id="ea353-496">VT \_ I2, VT \_ UI2, VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ea353-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="ea353-497">2</span><span class="sxs-lookup"><span data-stu-id="ea353-497">2</span></span>    |
| <span data-ttu-id="ea353-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, ERRORE \_ VT</span><span class="sxs-lookup"><span data-stu-id="ea353-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="ea353-499">4</span><span class="sxs-lookup"><span data-stu-id="ea353-499">4</span></span>    |
| <span data-ttu-id="ea353-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="ea353-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="ea353-501">8</span><span class="sxs-lookup"><span data-stu-id="ea353-501">8</span></span>    |
| <span data-ttu-id="ea353-502">VT \_ DECIMAL, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="ea353-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="ea353-503">16</span><span class="sxs-lookup"><span data-stu-id="ea353-503">16</span></span>   |



 

<span data-ttu-id="ea353-504">Se vType è impostato su VT \_ BLOB, VT BSTR o \_ VT \_ LPSTR, la struttura di vValue viene specificata nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="ea353-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="ea353-505">0</span><span class="sxs-lookup"><span data-stu-id="ea353-505">0</span></span>

<span data-ttu-id="ea353-506">1</span><span class="sxs-lookup"><span data-stu-id="ea353-506">1</span></span>

<span data-ttu-id="ea353-507">2</span><span class="sxs-lookup"><span data-stu-id="ea353-507">2</span></span>

<span data-ttu-id="ea353-508">3</span><span class="sxs-lookup"><span data-stu-id="ea353-508">3</span></span>

<span data-ttu-id="ea353-509">4</span><span class="sxs-lookup"><span data-stu-id="ea353-509">4</span></span>

<span data-ttu-id="ea353-510">5</span><span class="sxs-lookup"><span data-stu-id="ea353-510">5</span></span>

<span data-ttu-id="ea353-511">6</span><span class="sxs-lookup"><span data-stu-id="ea353-511">6</span></span>

<span data-ttu-id="ea353-512">7</span><span class="sxs-lookup"><span data-stu-id="ea353-512">7</span></span>

<span data-ttu-id="ea353-513">8</span><span class="sxs-lookup"><span data-stu-id="ea353-513">8</span></span>

<span data-ttu-id="ea353-514">9</span><span class="sxs-lookup"><span data-stu-id="ea353-514">9</span></span>

<span data-ttu-id="ea353-515">1</span><span class="sxs-lookup"><span data-stu-id="ea353-515">1</span></span><br/> <span data-ttu-id="ea353-516">0</span><span class="sxs-lookup"><span data-stu-id="ea353-516">0</span></span><br/>

<span data-ttu-id="ea353-517">1</span><span class="sxs-lookup"><span data-stu-id="ea353-517">1</span></span>

<span data-ttu-id="ea353-518">2</span><span class="sxs-lookup"><span data-stu-id="ea353-518">2</span></span>

<span data-ttu-id="ea353-519">3</span><span class="sxs-lookup"><span data-stu-id="ea353-519">3</span></span>

<span data-ttu-id="ea353-520">4</span><span class="sxs-lookup"><span data-stu-id="ea353-520">4</span></span>

<span data-ttu-id="ea353-521">5</span><span class="sxs-lookup"><span data-stu-id="ea353-521">5</span></span>

<span data-ttu-id="ea353-522">6</span><span class="sxs-lookup"><span data-stu-id="ea353-522">6</span></span>

<span data-ttu-id="ea353-523">7</span><span class="sxs-lookup"><span data-stu-id="ea353-523">7</span></span>

<span data-ttu-id="ea353-524">8</span><span class="sxs-lookup"><span data-stu-id="ea353-524">8</span></span>

<span data-ttu-id="ea353-525">9</span><span class="sxs-lookup"><span data-stu-id="ea353-525">9</span></span>

<span data-ttu-id="ea353-526">2</span><span class="sxs-lookup"><span data-stu-id="ea353-526">2</span></span><br/> <span data-ttu-id="ea353-527">0</span><span class="sxs-lookup"><span data-stu-id="ea353-527">0</span></span><br/>

<span data-ttu-id="ea353-528">1</span><span class="sxs-lookup"><span data-stu-id="ea353-528">1</span></span>

<span data-ttu-id="ea353-529">2</span><span class="sxs-lookup"><span data-stu-id="ea353-529">2</span></span>

<span data-ttu-id="ea353-530">3</span><span class="sxs-lookup"><span data-stu-id="ea353-530">3</span></span>

<span data-ttu-id="ea353-531">4</span><span class="sxs-lookup"><span data-stu-id="ea353-531">4</span></span>

<span data-ttu-id="ea353-532">5</span><span class="sxs-lookup"><span data-stu-id="ea353-532">5</span></span>

<span data-ttu-id="ea353-533">6</span><span class="sxs-lookup"><span data-stu-id="ea353-533">6</span></span>

<span data-ttu-id="ea353-534">7</span><span class="sxs-lookup"><span data-stu-id="ea353-534">7</span></span>

<span data-ttu-id="ea353-535">8</span><span class="sxs-lookup"><span data-stu-id="ea353-535">8</span></span>

<span data-ttu-id="ea353-536">9</span><span class="sxs-lookup"><span data-stu-id="ea353-536">9</span></span>

<span data-ttu-id="ea353-537">3</span><span class="sxs-lookup"><span data-stu-id="ea353-537">3</span></span><br/> <span data-ttu-id="ea353-538">0</span><span class="sxs-lookup"><span data-stu-id="ea353-538">0</span></span><br/>

<span data-ttu-id="ea353-539">1</span><span class="sxs-lookup"><span data-stu-id="ea353-539">1</span></span>

<span data-ttu-id="ea353-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="ea353-540">cbSize</span></span>

<span data-ttu-id="ea353-541">blobData (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="ea353-542">**cbSize:** intero senza segno a 32 bit, che indica le dimensioni del campo blobData in byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="ea353-543">Se vType è impostato su VT BSTR o \_ VT LPSTR, cbSize DEVE essere impostato su 0x00000000 quando la stringa rappresentata \_ è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="ea353-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="ea353-544">**blobData:** DEVE essere di lunghezza cbSize in byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="ea353-545">Per vType impostato su BLOB VT, questo campo è dati BLOB \_ binari opachi.</span><span class="sxs-lookup"><span data-stu-id="ea353-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="ea353-546">Per vType impostato su VT BSTR, questo campo è un set di caratteri in un set di caratteri \_ OEM selezionato.</span><span class="sxs-lookup"><span data-stu-id="ea353-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="ea353-547">Il client e il server DEVONO essere configurati per avere set di caratteri interoperabili (fuori banda del protocollo).</span><span class="sxs-lookup"><span data-stu-id="ea353-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="ea353-548">Non è necessario che sia con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="ea353-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="ea353-549">Per vType impostato su VT LPSTR, questo campo è una stringa di caratteri con terminazione Null in un set di caratteri \_ OEM selezionato.</span><span class="sxs-lookup"><span data-stu-id="ea353-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="ea353-550">Il client e il server DEVONO essere configurati per avere set di caratteri interoperabili (fuori banda del protocollo).</span><span class="sxs-lookup"><span data-stu-id="ea353-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="ea353-551">Se vType è impostato su VT \_ LPWSTR, la struttura di vValue viene specificata nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="ea353-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="ea353-552">0</span><span class="sxs-lookup"><span data-stu-id="ea353-552">0</span></span>

<span data-ttu-id="ea353-553">1</span><span class="sxs-lookup"><span data-stu-id="ea353-553">1</span></span>

<span data-ttu-id="ea353-554">2</span><span class="sxs-lookup"><span data-stu-id="ea353-554">2</span></span>

<span data-ttu-id="ea353-555">3</span><span class="sxs-lookup"><span data-stu-id="ea353-555">3</span></span>

<span data-ttu-id="ea353-556">4</span><span class="sxs-lookup"><span data-stu-id="ea353-556">4</span></span>

<span data-ttu-id="ea353-557">5</span><span class="sxs-lookup"><span data-stu-id="ea353-557">5</span></span>

<span data-ttu-id="ea353-558">6</span><span class="sxs-lookup"><span data-stu-id="ea353-558">6</span></span>

<span data-ttu-id="ea353-559">7</span><span class="sxs-lookup"><span data-stu-id="ea353-559">7</span></span>

<span data-ttu-id="ea353-560">8</span><span class="sxs-lookup"><span data-stu-id="ea353-560">8</span></span>

<span data-ttu-id="ea353-561">9</span><span class="sxs-lookup"><span data-stu-id="ea353-561">9</span></span>

<span data-ttu-id="ea353-562">1</span><span class="sxs-lookup"><span data-stu-id="ea353-562">1</span></span><br/> <span data-ttu-id="ea353-563">0</span><span class="sxs-lookup"><span data-stu-id="ea353-563">0</span></span><br/>

<span data-ttu-id="ea353-564">1</span><span class="sxs-lookup"><span data-stu-id="ea353-564">1</span></span>

<span data-ttu-id="ea353-565">2</span><span class="sxs-lookup"><span data-stu-id="ea353-565">2</span></span>

<span data-ttu-id="ea353-566">3</span><span class="sxs-lookup"><span data-stu-id="ea353-566">3</span></span>

<span data-ttu-id="ea353-567">4</span><span class="sxs-lookup"><span data-stu-id="ea353-567">4</span></span>

<span data-ttu-id="ea353-568">5</span><span class="sxs-lookup"><span data-stu-id="ea353-568">5</span></span>

<span data-ttu-id="ea353-569">6</span><span class="sxs-lookup"><span data-stu-id="ea353-569">6</span></span>

<span data-ttu-id="ea353-570">7</span><span class="sxs-lookup"><span data-stu-id="ea353-570">7</span></span>

<span data-ttu-id="ea353-571">8</span><span class="sxs-lookup"><span data-stu-id="ea353-571">8</span></span>

<span data-ttu-id="ea353-572">9</span><span class="sxs-lookup"><span data-stu-id="ea353-572">9</span></span>

<span data-ttu-id="ea353-573">2</span><span class="sxs-lookup"><span data-stu-id="ea353-573">2</span></span><br/> <span data-ttu-id="ea353-574">0</span><span class="sxs-lookup"><span data-stu-id="ea353-574">0</span></span><br/>

<span data-ttu-id="ea353-575">1</span><span class="sxs-lookup"><span data-stu-id="ea353-575">1</span></span>

<span data-ttu-id="ea353-576">2</span><span class="sxs-lookup"><span data-stu-id="ea353-576">2</span></span>

<span data-ttu-id="ea353-577">3</span><span class="sxs-lookup"><span data-stu-id="ea353-577">3</span></span>

<span data-ttu-id="ea353-578">4</span><span class="sxs-lookup"><span data-stu-id="ea353-578">4</span></span>

<span data-ttu-id="ea353-579">5</span><span class="sxs-lookup"><span data-stu-id="ea353-579">5</span></span>

<span data-ttu-id="ea353-580">6</span><span class="sxs-lookup"><span data-stu-id="ea353-580">6</span></span>

<span data-ttu-id="ea353-581">7</span><span class="sxs-lookup"><span data-stu-id="ea353-581">7</span></span>

<span data-ttu-id="ea353-582">8</span><span class="sxs-lookup"><span data-stu-id="ea353-582">8</span></span>

<span data-ttu-id="ea353-583">9</span><span class="sxs-lookup"><span data-stu-id="ea353-583">9</span></span>

<span data-ttu-id="ea353-584">3</span><span class="sxs-lookup"><span data-stu-id="ea353-584">3</span></span><br/> <span data-ttu-id="ea353-585">0</span><span class="sxs-lookup"><span data-stu-id="ea353-585">0</span></span><br/>

<span data-ttu-id="ea353-586">1</span><span class="sxs-lookup"><span data-stu-id="ea353-586">1</span></span>

<span data-ttu-id="ea353-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="ea353-587">ccLen</span></span>

<span data-ttu-id="ea353-588">string (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-588">string (variable, optional)</span></span>



 

<span data-ttu-id="ea353-589">**ccLen:** intero senza segno a 32 bit, che indica le dimensioni del campo stringa in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="ea353-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="ea353-590">DEVE essere impostato su 0x00000000 per una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="ea353-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="ea353-591">**string:** stringa Unicode con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="ea353-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="ea353-592">2.2.1.1.1 Strutture CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="ea353-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="ea353-593">Le strutture seguenti vengono usate nella struttura CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="ea353-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="ea353-594">2.2.1.1.1.1 DECIMALE</span><span class="sxs-lookup"><span data-stu-id="ea353-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="ea353-595">DECIMAL viene usato per rappresentare un valore numerico esatto con precisione fissa e scala fissa.</span><span class="sxs-lookup"><span data-stu-id="ea353-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="ea353-596">Quando vType è impostato su VT DECIMAL (0x0000E), i campi \_ vData1 e vData2 di CBaseStorageVariant DEVONO essere interpretati come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="ea353-597">**vData1:** numero di cifre a destra del separatore decimale.</span><span class="sxs-lookup"><span data-stu-id="ea353-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="ea353-598">DEVE essere compreso nell'intervallo da 0 a 28.</span><span class="sxs-lookup"><span data-stu-id="ea353-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="ea353-599">**vData2:** segno del valore numerico.</span><span class="sxs-lookup"><span data-stu-id="ea353-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="ea353-600">Impostare su 0x00 se positivo, 0x80 se negativo.</span><span class="sxs-lookup"><span data-stu-id="ea353-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="ea353-601">Il formato del campo vValue è:</span><span class="sxs-lookup"><span data-stu-id="ea353-601">The format of the vValue field is:</span></span>



<span data-ttu-id="ea353-602">0</span><span class="sxs-lookup"><span data-stu-id="ea353-602">0</span></span>

<span data-ttu-id="ea353-603">1</span><span class="sxs-lookup"><span data-stu-id="ea353-603">1</span></span>

<span data-ttu-id="ea353-604">2</span><span class="sxs-lookup"><span data-stu-id="ea353-604">2</span></span>

<span data-ttu-id="ea353-605">3</span><span class="sxs-lookup"><span data-stu-id="ea353-605">3</span></span>

<span data-ttu-id="ea353-606">4</span><span class="sxs-lookup"><span data-stu-id="ea353-606">4</span></span>

<span data-ttu-id="ea353-607">5</span><span class="sxs-lookup"><span data-stu-id="ea353-607">5</span></span>

<span data-ttu-id="ea353-608">6</span><span class="sxs-lookup"><span data-stu-id="ea353-608">6</span></span>

<span data-ttu-id="ea353-609">7</span><span class="sxs-lookup"><span data-stu-id="ea353-609">7</span></span>

<span data-ttu-id="ea353-610">8</span><span class="sxs-lookup"><span data-stu-id="ea353-610">8</span></span>

<span data-ttu-id="ea353-611">9</span><span class="sxs-lookup"><span data-stu-id="ea353-611">9</span></span>

<span data-ttu-id="ea353-612">1</span><span class="sxs-lookup"><span data-stu-id="ea353-612">1</span></span><br/> <span data-ttu-id="ea353-613">0</span><span class="sxs-lookup"><span data-stu-id="ea353-613">0</span></span><br/>

<span data-ttu-id="ea353-614">1</span><span class="sxs-lookup"><span data-stu-id="ea353-614">1</span></span>

<span data-ttu-id="ea353-615">2</span><span class="sxs-lookup"><span data-stu-id="ea353-615">2</span></span>

<span data-ttu-id="ea353-616">3</span><span class="sxs-lookup"><span data-stu-id="ea353-616">3</span></span>

<span data-ttu-id="ea353-617">4</span><span class="sxs-lookup"><span data-stu-id="ea353-617">4</span></span>

<span data-ttu-id="ea353-618">5</span><span class="sxs-lookup"><span data-stu-id="ea353-618">5</span></span>

<span data-ttu-id="ea353-619">6</span><span class="sxs-lookup"><span data-stu-id="ea353-619">6</span></span>

<span data-ttu-id="ea353-620">7</span><span class="sxs-lookup"><span data-stu-id="ea353-620">7</span></span>

<span data-ttu-id="ea353-621">8</span><span class="sxs-lookup"><span data-stu-id="ea353-621">8</span></span>

<span data-ttu-id="ea353-622">9</span><span class="sxs-lookup"><span data-stu-id="ea353-622">9</span></span>

<span data-ttu-id="ea353-623">2</span><span class="sxs-lookup"><span data-stu-id="ea353-623">2</span></span><br/> <span data-ttu-id="ea353-624">0</span><span class="sxs-lookup"><span data-stu-id="ea353-624">0</span></span><br/>

<span data-ttu-id="ea353-625">1</span><span class="sxs-lookup"><span data-stu-id="ea353-625">1</span></span>

<span data-ttu-id="ea353-626">2</span><span class="sxs-lookup"><span data-stu-id="ea353-626">2</span></span>

<span data-ttu-id="ea353-627">3</span><span class="sxs-lookup"><span data-stu-id="ea353-627">3</span></span>

<span data-ttu-id="ea353-628">4</span><span class="sxs-lookup"><span data-stu-id="ea353-628">4</span></span>

<span data-ttu-id="ea353-629">5</span><span class="sxs-lookup"><span data-stu-id="ea353-629">5</span></span>

<span data-ttu-id="ea353-630">6</span><span class="sxs-lookup"><span data-stu-id="ea353-630">6</span></span>

<span data-ttu-id="ea353-631">7</span><span class="sxs-lookup"><span data-stu-id="ea353-631">7</span></span>

<span data-ttu-id="ea353-632">8</span><span class="sxs-lookup"><span data-stu-id="ea353-632">8</span></span>

<span data-ttu-id="ea353-633">9</span><span class="sxs-lookup"><span data-stu-id="ea353-633">9</span></span>

<span data-ttu-id="ea353-634">3</span><span class="sxs-lookup"><span data-stu-id="ea353-634">3</span></span><br/> <span data-ttu-id="ea353-635">0</span><span class="sxs-lookup"><span data-stu-id="ea353-635">0</span></span><br/>

<span data-ttu-id="ea353-636">1</span><span class="sxs-lookup"><span data-stu-id="ea353-636">1</span></span>

<span data-ttu-id="ea353-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="ea353-637">Hi32</span></span>

<span data-ttu-id="ea353-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="ea353-638">Lo32</span></span>

<span data-ttu-id="ea353-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="ea353-639">Mid32</span></span>



 

<span data-ttu-id="ea353-640">**Hi32:** i 32 bit più alti dell'intero a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="ea353-641">**Lo32:** i 32 bit più bassi dell'intero a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="ea353-642">**Mid32:** 32 bit intermedi dell'intero a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="ea353-643">2.2.1.1.1.2 VETTORE \_ VT</span><span class="sxs-lookup"><span data-stu-id="ea353-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="ea353-644">VT \_ Vector viene usato per passare matrici unidimensionali.</span><span class="sxs-lookup"><span data-stu-id="ea353-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="ea353-645">0</span><span class="sxs-lookup"><span data-stu-id="ea353-645">0</span></span>

<span data-ttu-id="ea353-646">1</span><span class="sxs-lookup"><span data-stu-id="ea353-646">1</span></span>

<span data-ttu-id="ea353-647">2</span><span class="sxs-lookup"><span data-stu-id="ea353-647">2</span></span>

<span data-ttu-id="ea353-648">3</span><span class="sxs-lookup"><span data-stu-id="ea353-648">3</span></span>

<span data-ttu-id="ea353-649">4</span><span class="sxs-lookup"><span data-stu-id="ea353-649">4</span></span>

<span data-ttu-id="ea353-650">5</span><span class="sxs-lookup"><span data-stu-id="ea353-650">5</span></span>

<span data-ttu-id="ea353-651">6</span><span class="sxs-lookup"><span data-stu-id="ea353-651">6</span></span>

<span data-ttu-id="ea353-652">7</span><span class="sxs-lookup"><span data-stu-id="ea353-652">7</span></span>

<span data-ttu-id="ea353-653">8</span><span class="sxs-lookup"><span data-stu-id="ea353-653">8</span></span>

<span data-ttu-id="ea353-654">9</span><span class="sxs-lookup"><span data-stu-id="ea353-654">9</span></span>

<span data-ttu-id="ea353-655">1</span><span class="sxs-lookup"><span data-stu-id="ea353-655">1</span></span><br/> <span data-ttu-id="ea353-656">0</span><span class="sxs-lookup"><span data-stu-id="ea353-656">0</span></span><br/>

<span data-ttu-id="ea353-657">1</span><span class="sxs-lookup"><span data-stu-id="ea353-657">1</span></span>

<span data-ttu-id="ea353-658">2</span><span class="sxs-lookup"><span data-stu-id="ea353-658">2</span></span>

<span data-ttu-id="ea353-659">3</span><span class="sxs-lookup"><span data-stu-id="ea353-659">3</span></span>

<span data-ttu-id="ea353-660">4</span><span class="sxs-lookup"><span data-stu-id="ea353-660">4</span></span>

<span data-ttu-id="ea353-661">5</span><span class="sxs-lookup"><span data-stu-id="ea353-661">5</span></span>

<span data-ttu-id="ea353-662">6</span><span class="sxs-lookup"><span data-stu-id="ea353-662">6</span></span>

<span data-ttu-id="ea353-663">7</span><span class="sxs-lookup"><span data-stu-id="ea353-663">7</span></span>

<span data-ttu-id="ea353-664">8</span><span class="sxs-lookup"><span data-stu-id="ea353-664">8</span></span>

<span data-ttu-id="ea353-665">9</span><span class="sxs-lookup"><span data-stu-id="ea353-665">9</span></span>

<span data-ttu-id="ea353-666">2</span><span class="sxs-lookup"><span data-stu-id="ea353-666">2</span></span><br/> <span data-ttu-id="ea353-667">0</span><span class="sxs-lookup"><span data-stu-id="ea353-667">0</span></span><br/>

<span data-ttu-id="ea353-668">1</span><span class="sxs-lookup"><span data-stu-id="ea353-668">1</span></span>

<span data-ttu-id="ea353-669">2</span><span class="sxs-lookup"><span data-stu-id="ea353-669">2</span></span>

<span data-ttu-id="ea353-670">3</span><span class="sxs-lookup"><span data-stu-id="ea353-670">3</span></span>

<span data-ttu-id="ea353-671">4</span><span class="sxs-lookup"><span data-stu-id="ea353-671">4</span></span>

<span data-ttu-id="ea353-672">5</span><span class="sxs-lookup"><span data-stu-id="ea353-672">5</span></span>

<span data-ttu-id="ea353-673">6</span><span class="sxs-lookup"><span data-stu-id="ea353-673">6</span></span>

<span data-ttu-id="ea353-674">7</span><span class="sxs-lookup"><span data-stu-id="ea353-674">7</span></span>

<span data-ttu-id="ea353-675">8</span><span class="sxs-lookup"><span data-stu-id="ea353-675">8</span></span>

<span data-ttu-id="ea353-676">9</span><span class="sxs-lookup"><span data-stu-id="ea353-676">9</span></span>

<span data-ttu-id="ea353-677">3</span><span class="sxs-lookup"><span data-stu-id="ea353-677">3</span></span><br/> <span data-ttu-id="ea353-678">0</span><span class="sxs-lookup"><span data-stu-id="ea353-678">0</span></span><br/>

<span data-ttu-id="ea353-679">1</span><span class="sxs-lookup"><span data-stu-id="ea353-679">1</span></span>

<span data-ttu-id="ea353-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="ea353-680">vVectorElements</span></span>

<span data-ttu-id="ea353-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="ea353-681">vVectorData</span></span>



 

<span data-ttu-id="ea353-682">**vVectorElements:** intero senza segno a 32 bit, che indica il numero di elementi nel campo vVectorData.</span><span class="sxs-lookup"><span data-stu-id="ea353-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="ea353-683">**vVectorData:** matrice di elementi con un tipo indicato da vType con il 0x1000 bit cancellato.</span><span class="sxs-lookup"><span data-stu-id="ea353-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="ea353-684">Le dimensioni di un singolo elemento a lunghezza fissa possono essere ottenute dalla tabella con tipo di dati a lunghezza fissa, come specificato nella sezione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="ea353-685">La lunghezza di questo campo, in byte, può essere calcolata moltiplicando vVectorElements per le dimensioni del singolo elemento.</span><span class="sxs-lookup"><span data-stu-id="ea353-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="ea353-686">Per i tipi di dati a lunghezza variabile vVectorData contiene una sequenza di tipi semplici con marshalling consecutivo in cui il tipo è indicato da vType con il 0x1000 bit cancellato.</span><span class="sxs-lookup"><span data-stu-id="ea353-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="ea353-687">Ciò include un caso speciale indicato da vType VT \_ ARRAY \| VT \_ VARIANT (ad esempio, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="ea353-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="ea353-688">Gli elementi nel campo vVectorData DEVONO essere separati da 0 a 3 byte di riempimento in modo che ogni elemento inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice.</span><span class="sxs-lookup"><span data-stu-id="ea353-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="ea353-689">Se sono presenti byte di riempimento, il valore in essi contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="ea353-690">Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-691">Per un vType impostato su VT ARRAY VT VARIANT, il tipo per gli elementi in questa sequenza \_ \| è \_ CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="ea353-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="ea353-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="ea353-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="ea353-693">SAFEARRAY viene usato per passare matrici multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="ea353-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="ea353-694">La struttura contiene informazioni sulle dimensioni della matrice, nonché i dati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="ea353-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="ea353-695">0</span><span class="sxs-lookup"><span data-stu-id="ea353-695">0</span></span>

<span data-ttu-id="ea353-696">1</span><span class="sxs-lookup"><span data-stu-id="ea353-696">1</span></span>

<span data-ttu-id="ea353-697">2</span><span class="sxs-lookup"><span data-stu-id="ea353-697">2</span></span>

<span data-ttu-id="ea353-698">3</span><span class="sxs-lookup"><span data-stu-id="ea353-698">3</span></span>

<span data-ttu-id="ea353-699">4</span><span class="sxs-lookup"><span data-stu-id="ea353-699">4</span></span>

<span data-ttu-id="ea353-700">5</span><span class="sxs-lookup"><span data-stu-id="ea353-700">5</span></span>

<span data-ttu-id="ea353-701">6</span><span class="sxs-lookup"><span data-stu-id="ea353-701">6</span></span>

<span data-ttu-id="ea353-702">7</span><span class="sxs-lookup"><span data-stu-id="ea353-702">7</span></span>

<span data-ttu-id="ea353-703">8</span><span class="sxs-lookup"><span data-stu-id="ea353-703">8</span></span>

<span data-ttu-id="ea353-704">9</span><span class="sxs-lookup"><span data-stu-id="ea353-704">9</span></span>

<span data-ttu-id="ea353-705">1</span><span class="sxs-lookup"><span data-stu-id="ea353-705">1</span></span><br/> <span data-ttu-id="ea353-706">0</span><span class="sxs-lookup"><span data-stu-id="ea353-706">0</span></span><br/>

<span data-ttu-id="ea353-707">1</span><span class="sxs-lookup"><span data-stu-id="ea353-707">1</span></span>

<span data-ttu-id="ea353-708">2</span><span class="sxs-lookup"><span data-stu-id="ea353-708">2</span></span>

<span data-ttu-id="ea353-709">3</span><span class="sxs-lookup"><span data-stu-id="ea353-709">3</span></span>

<span data-ttu-id="ea353-710">4</span><span class="sxs-lookup"><span data-stu-id="ea353-710">4</span></span>

<span data-ttu-id="ea353-711">5</span><span class="sxs-lookup"><span data-stu-id="ea353-711">5</span></span>

<span data-ttu-id="ea353-712">6</span><span class="sxs-lookup"><span data-stu-id="ea353-712">6</span></span>

<span data-ttu-id="ea353-713">7</span><span class="sxs-lookup"><span data-stu-id="ea353-713">7</span></span>

<span data-ttu-id="ea353-714">8</span><span class="sxs-lookup"><span data-stu-id="ea353-714">8</span></span>

<span data-ttu-id="ea353-715">9</span><span class="sxs-lookup"><span data-stu-id="ea353-715">9</span></span>

<span data-ttu-id="ea353-716">2</span><span class="sxs-lookup"><span data-stu-id="ea353-716">2</span></span><br/> <span data-ttu-id="ea353-717">0</span><span class="sxs-lookup"><span data-stu-id="ea353-717">0</span></span><br/>

<span data-ttu-id="ea353-718">1</span><span class="sxs-lookup"><span data-stu-id="ea353-718">1</span></span>

<span data-ttu-id="ea353-719">2</span><span class="sxs-lookup"><span data-stu-id="ea353-719">2</span></span>

<span data-ttu-id="ea353-720">3</span><span class="sxs-lookup"><span data-stu-id="ea353-720">3</span></span>

<span data-ttu-id="ea353-721">4</span><span class="sxs-lookup"><span data-stu-id="ea353-721">4</span></span>

<span data-ttu-id="ea353-722">5</span><span class="sxs-lookup"><span data-stu-id="ea353-722">5</span></span>

<span data-ttu-id="ea353-723">6</span><span class="sxs-lookup"><span data-stu-id="ea353-723">6</span></span>

<span data-ttu-id="ea353-724">7</span><span class="sxs-lookup"><span data-stu-id="ea353-724">7</span></span>

<span data-ttu-id="ea353-725">8</span><span class="sxs-lookup"><span data-stu-id="ea353-725">8</span></span>

<span data-ttu-id="ea353-726">9</span><span class="sxs-lookup"><span data-stu-id="ea353-726">9</span></span>

<span data-ttu-id="ea353-727">3</span><span class="sxs-lookup"><span data-stu-id="ea353-727">3</span></span><br/> <span data-ttu-id="ea353-728">0</span><span class="sxs-lookup"><span data-stu-id="ea353-728">0</span></span><br/>

<span data-ttu-id="ea353-729">1</span><span class="sxs-lookup"><span data-stu-id="ea353-729">1</span></span>

<span data-ttu-id="ea353-730">cDims</span><span class="sxs-lookup"><span data-stu-id="ea353-730">cDims</span></span>

<span data-ttu-id="ea353-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="ea353-731">fFeatures</span></span>

<span data-ttu-id="ea353-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="ea353-732">cbElements</span></span>

<span data-ttu-id="ea353-733">Rgsabound (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-733">Rgsabound (variable)</span></span>

<span data-ttu-id="ea353-734">vData (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-734">vData (variable)</span></span>



 

<span data-ttu-id="ea353-735">**cDims:** intero senza segno a 16 bit, che indica il numero di dimensioni della matrice multidimensionale.</span><span class="sxs-lookup"><span data-stu-id="ea353-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="ea353-736">**fFeatures:** campo di bit a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="ea353-737">I valori rappresentano le funzionalità, definite dalle applicazioni di livello superiore e DEVONO essere ignorate.</span><span class="sxs-lookup"><span data-stu-id="ea353-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="ea353-738">**cbElements:** intero senza segno a 32 bit che specifica le dimensioni di ogni elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="ea353-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="ea353-739">**Rgsabound:** matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4, per dimensione in SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="ea353-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="ea353-740">Questa matrice ha prima la dimensione più a sinistra e la dimensione più a destra per ultima.</span><span class="sxs-lookup"><span data-stu-id="ea353-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="ea353-741">**vData:** vettore di elementi di cui è stato effettuato il marshalling di un particolare tipo, indicato dal vType dell'oggetto CBaseStorageVariant che lo contiene, con il bit 0x2000 cancellato.</span><span class="sxs-lookup"><span data-stu-id="ea353-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="ea353-742">Il marshalling di vData viene eseguito in modo analogo a VT VECTOR, come specificato nella sezione 2.2.1.1.1.2, con la differenza che il numero di elementi non viene archiviato davanti \_ al vettore.</span><span class="sxs-lookup"><span data-stu-id="ea353-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="ea353-743">Il numero di elementi viene invece calcolato moltiplicando il valore cElements con tutti i limiti di matrice sicuri definiti nel campo Rgsabound.</span><span class="sxs-lookup"><span data-stu-id="ea353-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="ea353-744">Gli elementi vengono archiviati in un vettore in ordine di dimensioni, a partire dalla dimensione più a destra.</span><span class="sxs-lookup"><span data-stu-id="ea353-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="ea353-745">Il diagramma seguente rappresenta visivamente una matrice bidimensionale di esempio.</span><span class="sxs-lookup"><span data-stu-id="ea353-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="ea353-746">La prima dimensione ha cElements uguale a 4 (rappresentato orizzontalmente) e lLbound uguale a 0 e la seconda dimensione ha cElements uguale a 2 (rappresentato verticalmente) e lLbound uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="ea353-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="ea353-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-747">0x00000001</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ea353-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-748">0x00000002</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ea353-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-749">0x00000003</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ea353-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="ea353-750">0x00000005</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="ea353-751">::row:::</span><span class="sxs-lookup"><span data-stu-id="ea353-751">::row:::</span></span>
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

<span data-ttu-id="ea353-752">Usando il diagramma precedente, vData conterrà la sequenza seguente: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (scorrere prima la dimensione più a destra e quindi incrementare la dimensione successiva).</span><span class="sxs-lookup"><span data-stu-id="ea353-752">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="ea353-753">L'oggetto Rgsabound precedente(che registra cElements e Lbound) sarà: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-753">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="ea353-754">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="ea353-754">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="ea353-755">La struttura SAFEARRAYBOUND rappresenta i limiti di una dimensione di SAFEARRAY o SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="ea353-755">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="ea353-756">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="ea353-756">Its format is:</span></span>



<span data-ttu-id="ea353-757">0</span><span class="sxs-lookup"><span data-stu-id="ea353-757">0</span></span>

<span data-ttu-id="ea353-758">1</span><span class="sxs-lookup"><span data-stu-id="ea353-758">1</span></span>

<span data-ttu-id="ea353-759">2</span><span class="sxs-lookup"><span data-stu-id="ea353-759">2</span></span>

<span data-ttu-id="ea353-760">3</span><span class="sxs-lookup"><span data-stu-id="ea353-760">3</span></span>

<span data-ttu-id="ea353-761">4</span><span class="sxs-lookup"><span data-stu-id="ea353-761">4</span></span>

<span data-ttu-id="ea353-762">5</span><span class="sxs-lookup"><span data-stu-id="ea353-762">5</span></span>

<span data-ttu-id="ea353-763">6</span><span class="sxs-lookup"><span data-stu-id="ea353-763">6</span></span>

<span data-ttu-id="ea353-764">7</span><span class="sxs-lookup"><span data-stu-id="ea353-764">7</span></span>

<span data-ttu-id="ea353-765">8</span><span class="sxs-lookup"><span data-stu-id="ea353-765">8</span></span>

<span data-ttu-id="ea353-766">9</span><span class="sxs-lookup"><span data-stu-id="ea353-766">9</span></span>

<span data-ttu-id="ea353-767">1</span><span class="sxs-lookup"><span data-stu-id="ea353-767">1</span></span><br/> <span data-ttu-id="ea353-768">0</span><span class="sxs-lookup"><span data-stu-id="ea353-768">0</span></span><br/>

<span data-ttu-id="ea353-769">1</span><span class="sxs-lookup"><span data-stu-id="ea353-769">1</span></span>

<span data-ttu-id="ea353-770">2</span><span class="sxs-lookup"><span data-stu-id="ea353-770">2</span></span>

<span data-ttu-id="ea353-771">3</span><span class="sxs-lookup"><span data-stu-id="ea353-771">3</span></span>

<span data-ttu-id="ea353-772">4</span><span class="sxs-lookup"><span data-stu-id="ea353-772">4</span></span>

<span data-ttu-id="ea353-773">5</span><span class="sxs-lookup"><span data-stu-id="ea353-773">5</span></span>

<span data-ttu-id="ea353-774">6</span><span class="sxs-lookup"><span data-stu-id="ea353-774">6</span></span>

<span data-ttu-id="ea353-775">7</span><span class="sxs-lookup"><span data-stu-id="ea353-775">7</span></span>

<span data-ttu-id="ea353-776">8</span><span class="sxs-lookup"><span data-stu-id="ea353-776">8</span></span>

<span data-ttu-id="ea353-777">9</span><span class="sxs-lookup"><span data-stu-id="ea353-777">9</span></span>

<span data-ttu-id="ea353-778">2</span><span class="sxs-lookup"><span data-stu-id="ea353-778">2</span></span><br/> <span data-ttu-id="ea353-779">0</span><span class="sxs-lookup"><span data-stu-id="ea353-779">0</span></span><br/>

<span data-ttu-id="ea353-780">1</span><span class="sxs-lookup"><span data-stu-id="ea353-780">1</span></span>

<span data-ttu-id="ea353-781">2</span><span class="sxs-lookup"><span data-stu-id="ea353-781">2</span></span>

<span data-ttu-id="ea353-782">3</span><span class="sxs-lookup"><span data-stu-id="ea353-782">3</span></span>

<span data-ttu-id="ea353-783">4</span><span class="sxs-lookup"><span data-stu-id="ea353-783">4</span></span>

<span data-ttu-id="ea353-784">5</span><span class="sxs-lookup"><span data-stu-id="ea353-784">5</span></span>

<span data-ttu-id="ea353-785">6</span><span class="sxs-lookup"><span data-stu-id="ea353-785">6</span></span>

<span data-ttu-id="ea353-786">7</span><span class="sxs-lookup"><span data-stu-id="ea353-786">7</span></span>

<span data-ttu-id="ea353-787">8</span><span class="sxs-lookup"><span data-stu-id="ea353-787">8</span></span>

<span data-ttu-id="ea353-788">9</span><span class="sxs-lookup"><span data-stu-id="ea353-788">9</span></span>

<span data-ttu-id="ea353-789">3</span><span class="sxs-lookup"><span data-stu-id="ea353-789">3</span></span><br/> <span data-ttu-id="ea353-790">0</span><span class="sxs-lookup"><span data-stu-id="ea353-790">0</span></span><br/>

<span data-ttu-id="ea353-791">1</span><span class="sxs-lookup"><span data-stu-id="ea353-791">1</span></span>

<span data-ttu-id="ea353-792">cElements</span><span class="sxs-lookup"><span data-stu-id="ea353-792">cElements</span></span>

<span data-ttu-id="ea353-793">lLbound</span><span class="sxs-lookup"><span data-stu-id="ea353-793">lLbound</span></span>



 

<span data-ttu-id="ea353-794">**cElements:** intero senza segno a 32 bit che specifica il numero di elementi nella dimensione.</span><span class="sxs-lookup"><span data-stu-id="ea353-794">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="ea353-795">**lLbound:** intero senza segno a 32 bit che specifica il limite inferiore della dimensione.</span><span class="sxs-lookup"><span data-stu-id="ea353-795">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="ea353-796">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="ea353-796">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="ea353-797">SAFEARRAY2 viene usato per passare matrici multidimensionali in SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="ea353-797">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="ea353-798">La struttura contiene informazioni sui limiti e i dati.</span><span class="sxs-lookup"><span data-stu-id="ea353-798">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="ea353-799">0</span><span class="sxs-lookup"><span data-stu-id="ea353-799">0</span></span>

<span data-ttu-id="ea353-800">1</span><span class="sxs-lookup"><span data-stu-id="ea353-800">1</span></span>

<span data-ttu-id="ea353-801">2</span><span class="sxs-lookup"><span data-stu-id="ea353-801">2</span></span>

<span data-ttu-id="ea353-802">3</span><span class="sxs-lookup"><span data-stu-id="ea353-802">3</span></span>

<span data-ttu-id="ea353-803">4</span><span class="sxs-lookup"><span data-stu-id="ea353-803">4</span></span>

<span data-ttu-id="ea353-804">5</span><span class="sxs-lookup"><span data-stu-id="ea353-804">5</span></span>

<span data-ttu-id="ea353-805">6</span><span class="sxs-lookup"><span data-stu-id="ea353-805">6</span></span>

<span data-ttu-id="ea353-806">7</span><span class="sxs-lookup"><span data-stu-id="ea353-806">7</span></span>

<span data-ttu-id="ea353-807">8</span><span class="sxs-lookup"><span data-stu-id="ea353-807">8</span></span>

<span data-ttu-id="ea353-808">9</span><span class="sxs-lookup"><span data-stu-id="ea353-808">9</span></span>

<span data-ttu-id="ea353-809">1</span><span class="sxs-lookup"><span data-stu-id="ea353-809">1</span></span><br/> <span data-ttu-id="ea353-810">0</span><span class="sxs-lookup"><span data-stu-id="ea353-810">0</span></span><br/>

<span data-ttu-id="ea353-811">1</span><span class="sxs-lookup"><span data-stu-id="ea353-811">1</span></span>

<span data-ttu-id="ea353-812">2</span><span class="sxs-lookup"><span data-stu-id="ea353-812">2</span></span>

<span data-ttu-id="ea353-813">3</span><span class="sxs-lookup"><span data-stu-id="ea353-813">3</span></span>

<span data-ttu-id="ea353-814">4</span><span class="sxs-lookup"><span data-stu-id="ea353-814">4</span></span>

<span data-ttu-id="ea353-815">5</span><span class="sxs-lookup"><span data-stu-id="ea353-815">5</span></span>

<span data-ttu-id="ea353-816">6</span><span class="sxs-lookup"><span data-stu-id="ea353-816">6</span></span>

<span data-ttu-id="ea353-817">7</span><span class="sxs-lookup"><span data-stu-id="ea353-817">7</span></span>

<span data-ttu-id="ea353-818">8</span><span class="sxs-lookup"><span data-stu-id="ea353-818">8</span></span>

<span data-ttu-id="ea353-819">9</span><span class="sxs-lookup"><span data-stu-id="ea353-819">9</span></span>

<span data-ttu-id="ea353-820">2</span><span class="sxs-lookup"><span data-stu-id="ea353-820">2</span></span><br/> <span data-ttu-id="ea353-821">0</span><span class="sxs-lookup"><span data-stu-id="ea353-821">0</span></span><br/>

<span data-ttu-id="ea353-822">1</span><span class="sxs-lookup"><span data-stu-id="ea353-822">1</span></span>

<span data-ttu-id="ea353-823">2</span><span class="sxs-lookup"><span data-stu-id="ea353-823">2</span></span>

<span data-ttu-id="ea353-824">3</span><span class="sxs-lookup"><span data-stu-id="ea353-824">3</span></span>

<span data-ttu-id="ea353-825">4</span><span class="sxs-lookup"><span data-stu-id="ea353-825">4</span></span>

<span data-ttu-id="ea353-826">5</span><span class="sxs-lookup"><span data-stu-id="ea353-826">5</span></span>

<span data-ttu-id="ea353-827">6</span><span class="sxs-lookup"><span data-stu-id="ea353-827">6</span></span>

<span data-ttu-id="ea353-828">7</span><span class="sxs-lookup"><span data-stu-id="ea353-828">7</span></span>

<span data-ttu-id="ea353-829">8</span><span class="sxs-lookup"><span data-stu-id="ea353-829">8</span></span>

<span data-ttu-id="ea353-830">9</span><span class="sxs-lookup"><span data-stu-id="ea353-830">9</span></span>

<span data-ttu-id="ea353-831">3</span><span class="sxs-lookup"><span data-stu-id="ea353-831">3</span></span><br/> <span data-ttu-id="ea353-832">0</span><span class="sxs-lookup"><span data-stu-id="ea353-832">0</span></span><br/>

<span data-ttu-id="ea353-833">1</span><span class="sxs-lookup"><span data-stu-id="ea353-833">1</span></span>

<span data-ttu-id="ea353-834">cDims</span><span class="sxs-lookup"><span data-stu-id="ea353-834">cDims</span></span>

<span data-ttu-id="ea353-835">Rgsabound (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-835">Rgsabound (variable)</span></span>

<span data-ttu-id="ea353-836">vData (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-836">vData (variable)</span></span>



 

<span data-ttu-id="ea353-837">**cDims:** intero senza segno a 32 bit, che indica il numero di dimensioni di SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="ea353-837">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="ea353-838">**Rgsabound:** matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4 per dimensione in SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="ea353-838">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="ea353-839">Questa matrice ha prima la dimensione più a sinistra e la dimensione più a destra per ultima.</span><span class="sxs-lookup"><span data-stu-id="ea353-839">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="ea353-840">**vData:** vettore di elementi di cui è stato effettuato il marshalling di un determinato tipo, indicato dal tipo dwType dell'oggetto SERIALIZEDPROPERTYVALUE contenitore, con i bit 0x2000 cancellati.</span><span class="sxs-lookup"><span data-stu-id="ea353-840">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="ea353-841">Il formato di vData è uguale a quello specificato per il campo vData di SAFEARRAY nella sezione 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="ea353-841">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="ea353-842">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="ea353-842">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="ea353-843">La struttura CFullPropSpec contiene un GUID del set di proprietà e un identificatore di proprietà per identificare in modo univoco la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-843">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="ea353-844">0</span><span class="sxs-lookup"><span data-stu-id="ea353-844">0</span></span>

<span data-ttu-id="ea353-845">1</span><span class="sxs-lookup"><span data-stu-id="ea353-845">1</span></span>

<span data-ttu-id="ea353-846">2</span><span class="sxs-lookup"><span data-stu-id="ea353-846">2</span></span>

<span data-ttu-id="ea353-847">3</span><span class="sxs-lookup"><span data-stu-id="ea353-847">3</span></span>

<span data-ttu-id="ea353-848">4</span><span class="sxs-lookup"><span data-stu-id="ea353-848">4</span></span>

<span data-ttu-id="ea353-849">5</span><span class="sxs-lookup"><span data-stu-id="ea353-849">5</span></span>

<span data-ttu-id="ea353-850">6</span><span class="sxs-lookup"><span data-stu-id="ea353-850">6</span></span>

<span data-ttu-id="ea353-851">7</span><span class="sxs-lookup"><span data-stu-id="ea353-851">7</span></span>

<span data-ttu-id="ea353-852">8</span><span class="sxs-lookup"><span data-stu-id="ea353-852">8</span></span>

<span data-ttu-id="ea353-853">9</span><span class="sxs-lookup"><span data-stu-id="ea353-853">9</span></span>

<span data-ttu-id="ea353-854">1</span><span class="sxs-lookup"><span data-stu-id="ea353-854">1</span></span><br/> <span data-ttu-id="ea353-855">0</span><span class="sxs-lookup"><span data-stu-id="ea353-855">0</span></span><br/>

<span data-ttu-id="ea353-856">1</span><span class="sxs-lookup"><span data-stu-id="ea353-856">1</span></span>

<span data-ttu-id="ea353-857">2</span><span class="sxs-lookup"><span data-stu-id="ea353-857">2</span></span>

<span data-ttu-id="ea353-858">3</span><span class="sxs-lookup"><span data-stu-id="ea353-858">3</span></span>

<span data-ttu-id="ea353-859">4</span><span class="sxs-lookup"><span data-stu-id="ea353-859">4</span></span>

<span data-ttu-id="ea353-860">5</span><span class="sxs-lookup"><span data-stu-id="ea353-860">5</span></span>

<span data-ttu-id="ea353-861">6</span><span class="sxs-lookup"><span data-stu-id="ea353-861">6</span></span>

<span data-ttu-id="ea353-862">7</span><span class="sxs-lookup"><span data-stu-id="ea353-862">7</span></span>

<span data-ttu-id="ea353-863">8</span><span class="sxs-lookup"><span data-stu-id="ea353-863">8</span></span>

<span data-ttu-id="ea353-864">9</span><span class="sxs-lookup"><span data-stu-id="ea353-864">9</span></span>

<span data-ttu-id="ea353-865">2</span><span class="sxs-lookup"><span data-stu-id="ea353-865">2</span></span><br/> <span data-ttu-id="ea353-866">0</span><span class="sxs-lookup"><span data-stu-id="ea353-866">0</span></span><br/>

<span data-ttu-id="ea353-867">1</span><span class="sxs-lookup"><span data-stu-id="ea353-867">1</span></span>

<span data-ttu-id="ea353-868">2</span><span class="sxs-lookup"><span data-stu-id="ea353-868">2</span></span>

<span data-ttu-id="ea353-869">3</span><span class="sxs-lookup"><span data-stu-id="ea353-869">3</span></span>

<span data-ttu-id="ea353-870">4</span><span class="sxs-lookup"><span data-stu-id="ea353-870">4</span></span>

<span data-ttu-id="ea353-871">5</span><span class="sxs-lookup"><span data-stu-id="ea353-871">5</span></span>

<span data-ttu-id="ea353-872">6</span><span class="sxs-lookup"><span data-stu-id="ea353-872">6</span></span>

<span data-ttu-id="ea353-873">7</span><span class="sxs-lookup"><span data-stu-id="ea353-873">7</span></span>

<span data-ttu-id="ea353-874">8</span><span class="sxs-lookup"><span data-stu-id="ea353-874">8</span></span>

<span data-ttu-id="ea353-875">9</span><span class="sxs-lookup"><span data-stu-id="ea353-875">9</span></span>

<span data-ttu-id="ea353-876">3</span><span class="sxs-lookup"><span data-stu-id="ea353-876">3</span></span><br/> <span data-ttu-id="ea353-877">0</span><span class="sxs-lookup"><span data-stu-id="ea353-877">0</span></span><br/>

<span data-ttu-id="ea353-878">1</span><span class="sxs-lookup"><span data-stu-id="ea353-878">1</span></span>

<span data-ttu-id="ea353-879">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="ea353-879">\_guidPropSet</span></span>

<span data-ttu-id="ea353-880">...</span><span class="sxs-lookup"><span data-stu-id="ea353-880">...</span></span>

<span data-ttu-id="ea353-881">...</span><span class="sxs-lookup"><span data-stu-id="ea353-881">...</span></span>

<span data-ttu-id="ea353-882">...</span><span class="sxs-lookup"><span data-stu-id="ea353-882">...</span></span>

<span data-ttu-id="ea353-883">ulKind</span><span class="sxs-lookup"><span data-stu-id="ea353-883">ulKind</span></span>

<span data-ttu-id="ea353-884">PrSpec</span><span class="sxs-lookup"><span data-stu-id="ea353-884">PrSpec</span></span>

<span data-ttu-id="ea353-885">Nome proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-885">Property name (variable)</span></span>



 

<span data-ttu-id="ea353-886">**\_ guidPropSet:** GUID del set di proprietà a cui appartiene la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-886">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="ea353-887">**ulKind:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-887">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="ea353-888">Uno dei valori seguenti, che indica il contenuto di PrSpec.</span><span class="sxs-lookup"><span data-stu-id="ea353-888">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="ea353-889">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-889">Value</span></span>                                            | <span data-ttu-id="ea353-890">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-890">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-891">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ea353-891">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="ea353-892">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-892">0x00000000</span></span><br/> | <span data-ttu-id="ea353-893">Il campo PrSpec specifica il numero di caratteri non NULL nel campo Nome proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-893">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="ea353-894">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="ea353-894">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="ea353-895">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-895">0x00000001</span></span><br/>  | <span data-ttu-id="ea353-896">Il campo PrSpec specifica l'ID proprietà (PROPID).</span><span class="sxs-lookup"><span data-stu-id="ea353-896">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="ea353-897">**PrSpec:** intero senza segno a 32 bit con un significato indicato dal campo ulKind.</span><span class="sxs-lookup"><span data-stu-id="ea353-897">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="ea353-898">**Nome proprietà:** se ulKind è impostato su PRSPEC \_ PROPID, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-898">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="ea353-899">Se ulKind è impostato su PRSPEC LPWSTR, questo campo DEVE contenere una matrice senza distinzione tra maiuscole e minuscole di caratteri Unicode PrSpec non Null, contenente il nome della \_ proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-899">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="ea353-900">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-900">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="ea353-901">La struttura CContentRestriction contiene una stringa che corrisponde a una proprietà nella cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-901">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="ea353-902">0</span><span class="sxs-lookup"><span data-stu-id="ea353-902">0</span></span>

<span data-ttu-id="ea353-903">1</span><span class="sxs-lookup"><span data-stu-id="ea353-903">1</span></span>

<span data-ttu-id="ea353-904">2</span><span class="sxs-lookup"><span data-stu-id="ea353-904">2</span></span>

<span data-ttu-id="ea353-905">3</span><span class="sxs-lookup"><span data-stu-id="ea353-905">3</span></span>

<span data-ttu-id="ea353-906">4</span><span class="sxs-lookup"><span data-stu-id="ea353-906">4</span></span>

<span data-ttu-id="ea353-907">5</span><span class="sxs-lookup"><span data-stu-id="ea353-907">5</span></span>

<span data-ttu-id="ea353-908">6</span><span class="sxs-lookup"><span data-stu-id="ea353-908">6</span></span>

<span data-ttu-id="ea353-909">7</span><span class="sxs-lookup"><span data-stu-id="ea353-909">7</span></span>

<span data-ttu-id="ea353-910">8</span><span class="sxs-lookup"><span data-stu-id="ea353-910">8</span></span>

<span data-ttu-id="ea353-911">9</span><span class="sxs-lookup"><span data-stu-id="ea353-911">9</span></span>

<span data-ttu-id="ea353-912">1</span><span class="sxs-lookup"><span data-stu-id="ea353-912">1</span></span><br/> <span data-ttu-id="ea353-913">0</span><span class="sxs-lookup"><span data-stu-id="ea353-913">0</span></span><br/>

<span data-ttu-id="ea353-914">1</span><span class="sxs-lookup"><span data-stu-id="ea353-914">1</span></span>

<span data-ttu-id="ea353-915">2</span><span class="sxs-lookup"><span data-stu-id="ea353-915">2</span></span>

<span data-ttu-id="ea353-916">3</span><span class="sxs-lookup"><span data-stu-id="ea353-916">3</span></span>

<span data-ttu-id="ea353-917">4</span><span class="sxs-lookup"><span data-stu-id="ea353-917">4</span></span>

<span data-ttu-id="ea353-918">5</span><span class="sxs-lookup"><span data-stu-id="ea353-918">5</span></span>

<span data-ttu-id="ea353-919">6</span><span class="sxs-lookup"><span data-stu-id="ea353-919">6</span></span>

<span data-ttu-id="ea353-920">7</span><span class="sxs-lookup"><span data-stu-id="ea353-920">7</span></span>

<span data-ttu-id="ea353-921">8</span><span class="sxs-lookup"><span data-stu-id="ea353-921">8</span></span>

<span data-ttu-id="ea353-922">9</span><span class="sxs-lookup"><span data-stu-id="ea353-922">9</span></span>

<span data-ttu-id="ea353-923">2</span><span class="sxs-lookup"><span data-stu-id="ea353-923">2</span></span><br/> <span data-ttu-id="ea353-924">0</span><span class="sxs-lookup"><span data-stu-id="ea353-924">0</span></span><br/>

<span data-ttu-id="ea353-925">1</span><span class="sxs-lookup"><span data-stu-id="ea353-925">1</span></span>

<span data-ttu-id="ea353-926">2</span><span class="sxs-lookup"><span data-stu-id="ea353-926">2</span></span>

<span data-ttu-id="ea353-927">3</span><span class="sxs-lookup"><span data-stu-id="ea353-927">3</span></span>

<span data-ttu-id="ea353-928">4</span><span class="sxs-lookup"><span data-stu-id="ea353-928">4</span></span>

<span data-ttu-id="ea353-929">5</span><span class="sxs-lookup"><span data-stu-id="ea353-929">5</span></span>

<span data-ttu-id="ea353-930">6</span><span class="sxs-lookup"><span data-stu-id="ea353-930">6</span></span>

<span data-ttu-id="ea353-931">7</span><span class="sxs-lookup"><span data-stu-id="ea353-931">7</span></span>

<span data-ttu-id="ea353-932">8</span><span class="sxs-lookup"><span data-stu-id="ea353-932">8</span></span>

<span data-ttu-id="ea353-933">9</span><span class="sxs-lookup"><span data-stu-id="ea353-933">9</span></span>

<span data-ttu-id="ea353-934">3</span><span class="sxs-lookup"><span data-stu-id="ea353-934">3</span></span><br/> <span data-ttu-id="ea353-935">0</span><span class="sxs-lookup"><span data-stu-id="ea353-935">0</span></span><br/>

<span data-ttu-id="ea353-936">1</span><span class="sxs-lookup"><span data-stu-id="ea353-936">1</span></span>

<span data-ttu-id="ea353-937">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-937">\_Property (variable)</span></span>

<span data-ttu-id="ea353-938">...</span><span class="sxs-lookup"><span data-stu-id="ea353-938">...</span></span>

<span data-ttu-id="ea353-939">Padding1 (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-939">Padding1 (variable)</span></span>

<span data-ttu-id="ea353-940">Cc</span><span class="sxs-lookup"><span data-stu-id="ea353-940">Cc</span></span>

<span data-ttu-id="ea353-941">\_pwcsPhrase (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-941">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="ea353-942">...</span><span class="sxs-lookup"><span data-stu-id="ea353-942">...</span></span>

<span data-ttu-id="ea353-943">Padding2 (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-943">Padding2 (variable)</span></span>

<span data-ttu-id="ea353-944">lcid</span><span class="sxs-lookup"><span data-stu-id="ea353-944">lcid</span></span>

<span data-ttu-id="ea353-945">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="ea353-945">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="ea353-946">**\_ Property:** struttura CFullPropSpec, come specificato nella sezione 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="ea353-946">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="ea353-947">Questo campo indica la proprietà su cui eseguire un'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-947">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="ea353-948">**Padding1:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-948">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="ea353-949">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ea353-949">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="ea353-950">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-950">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="ea353-951">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-951">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-952">**Cc:** intero senza segno a 32 bit che specifica il numero di caratteri nel \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="ea353-952">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="ea353-953">**\_ pwcsPhrase:** stringa Unicode non con terminazione Null che rappresenta la parola o la frase di cui trovare la corrispondenza per la proprietà .</span><span class="sxs-lookup"><span data-stu-id="ea353-953">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="ea353-954">Questo campo NON DEVE essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="ea353-954">This field MUST NOT be empty.</span></span> <span data-ttu-id="ea353-955">Il campo Cc contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="ea353-955">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="ea353-956">**Padding2:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-956">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="ea353-957">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ea353-957">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="ea353-958">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-958">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="ea353-959">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-959">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-960">**Lcid:** intero senza segno a 32 bit che indica le impostazioni locali di \_ pwcsPhrase, come specificato \[ nell'appendice A MS-GPSI. \]</span><span class="sxs-lookup"><span data-stu-id="ea353-960">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="ea353-961">**\_ ulGenerateMethod:** intero senza segno a 32 bit che specifica il metodo da usare per la generazione di forme di parole alternative</span><span class="sxs-lookup"><span data-stu-id="ea353-961">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="ea353-962">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-962">Value</span></span>                                                       | <span data-ttu-id="ea353-963">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-963">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-964">GENERARE \_ IL METODO \_ ESATTO</span><span class="sxs-lookup"><span data-stu-id="ea353-964">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="ea353-965">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-965">0x00000000</span></span><br/>    | <span data-ttu-id="ea353-966">Corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="ea353-966">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ea353-967">GENERARE IL \_ PREFISSO DEL \_ METODO</span><span class="sxs-lookup"><span data-stu-id="ea353-967">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="ea353-968">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-968">0x00000001</span></span> <br/>  | <span data-ttu-id="ea353-969">Corrispondenza del prefisso.</span><span class="sxs-lookup"><span data-stu-id="ea353-969">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ea353-970">GENERATE \_ METHOD \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="ea353-970">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="ea353-971">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-971">0x00000002</span></span><br/> | <span data-ttu-id="ea353-972">Corrisponde alle flesshe di una parola.</span><span class="sxs-lookup"><span data-stu-id="ea353-972">Matches inflections of a word.</span></span> <span data-ttu-id="ea353-973">Un'inflezione di una parola è una variante della parola radice nella stessa parte del discorso che è stata modificata in base alle regole linguistiche di una determinata lingua.</span><span class="sxs-lookup"><span data-stu-id="ea353-973">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="ea353-974">Ad esempio, le flesszioni del verbo "corsia" in inglese includono "corsia", "corsia", "gonfia" e "swam".</span><span class="sxs-lookup"><span data-stu-id="ea353-974">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="ea353-975">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="ea353-975">2.2.1.4 CKey</span></span>

<span data-ttu-id="ea353-976">La struttura CKey contiene un valore di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-976">The CKey structure contains a property value.</span></span>



<span data-ttu-id="ea353-977">0</span><span class="sxs-lookup"><span data-stu-id="ea353-977">0</span></span>

<span data-ttu-id="ea353-978">1</span><span class="sxs-lookup"><span data-stu-id="ea353-978">1</span></span>

<span data-ttu-id="ea353-979">2</span><span class="sxs-lookup"><span data-stu-id="ea353-979">2</span></span>

<span data-ttu-id="ea353-980">3</span><span class="sxs-lookup"><span data-stu-id="ea353-980">3</span></span>

<span data-ttu-id="ea353-981">4</span><span class="sxs-lookup"><span data-stu-id="ea353-981">4</span></span>

<span data-ttu-id="ea353-982">5</span><span class="sxs-lookup"><span data-stu-id="ea353-982">5</span></span>

<span data-ttu-id="ea353-983">6</span><span class="sxs-lookup"><span data-stu-id="ea353-983">6</span></span>

<span data-ttu-id="ea353-984">7</span><span class="sxs-lookup"><span data-stu-id="ea353-984">7</span></span>

<span data-ttu-id="ea353-985">8</span><span class="sxs-lookup"><span data-stu-id="ea353-985">8</span></span>

<span data-ttu-id="ea353-986">9</span><span class="sxs-lookup"><span data-stu-id="ea353-986">9</span></span>

<span data-ttu-id="ea353-987">1</span><span class="sxs-lookup"><span data-stu-id="ea353-987">1</span></span><br/> <span data-ttu-id="ea353-988">0</span><span class="sxs-lookup"><span data-stu-id="ea353-988">0</span></span><br/>

<span data-ttu-id="ea353-989">1</span><span class="sxs-lookup"><span data-stu-id="ea353-989">1</span></span>

<span data-ttu-id="ea353-990">2</span><span class="sxs-lookup"><span data-stu-id="ea353-990">2</span></span>

<span data-ttu-id="ea353-991">3</span><span class="sxs-lookup"><span data-stu-id="ea353-991">3</span></span>

<span data-ttu-id="ea353-992">4</span><span class="sxs-lookup"><span data-stu-id="ea353-992">4</span></span>

<span data-ttu-id="ea353-993">5</span><span class="sxs-lookup"><span data-stu-id="ea353-993">5</span></span>

<span data-ttu-id="ea353-994">6</span><span class="sxs-lookup"><span data-stu-id="ea353-994">6</span></span>

<span data-ttu-id="ea353-995">7</span><span class="sxs-lookup"><span data-stu-id="ea353-995">7</span></span>

<span data-ttu-id="ea353-996">8</span><span class="sxs-lookup"><span data-stu-id="ea353-996">8</span></span>

<span data-ttu-id="ea353-997">9</span><span class="sxs-lookup"><span data-stu-id="ea353-997">9</span></span>

<span data-ttu-id="ea353-998">2</span><span class="sxs-lookup"><span data-stu-id="ea353-998">2</span></span><br/> <span data-ttu-id="ea353-999">0</span><span class="sxs-lookup"><span data-stu-id="ea353-999">0</span></span><br/>

<span data-ttu-id="ea353-1000">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1000">1</span></span>

<span data-ttu-id="ea353-1001">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1001">2</span></span>

<span data-ttu-id="ea353-1002">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1002">3</span></span>

<span data-ttu-id="ea353-1003">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1003">4</span></span>

<span data-ttu-id="ea353-1004">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1004">5</span></span>

<span data-ttu-id="ea353-1005">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1005">6</span></span>

<span data-ttu-id="ea353-1006">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1006">7</span></span>

<span data-ttu-id="ea353-1007">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1007">8</span></span>

<span data-ttu-id="ea353-1008">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1008">9</span></span>

<span data-ttu-id="ea353-1009">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1009">3</span></span><br/> <span data-ttu-id="ea353-1010">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1010">0</span></span><br/>

<span data-ttu-id="ea353-1011">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1011">1</span></span>

<span data-ttu-id="ea353-1012">PROPID</span><span class="sxs-lookup"><span data-stu-id="ea353-1012">PROPID</span></span>

<span data-ttu-id="ea353-1013">Cb</span><span class="sxs-lookup"><span data-stu-id="ea353-1013">Cb</span></span>

<span data-ttu-id="ea353-1014">buf (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1014">buf (variable)</span></span>



 

<span data-ttu-id="ea353-1015">**PROPID:** intero senza segno a 32 bit che rappresenta l'ID proprietà come descritto nella sezione 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-1015">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="ea353-1016">I valori noti sono:</span><span class="sxs-lookup"><span data-stu-id="ea353-1016">Well-known values are:</span></span>



| <span data-ttu-id="ea353-1017">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1017">Value</span></span>      | <span data-ttu-id="ea353-1018">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1018">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="ea353-1019">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="ea353-1019">0xFFFFFFFF</span></span> | <span data-ttu-id="ea353-1020">Rappresenta un ID di proprietà non valido e NON DEVE essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ea353-1020">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="ea353-1021">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="ea353-1021">0xFFFFFFFE</span></span> | <span data-ttu-id="ea353-1022">Rappresenta un ID di proprietà non valido e NON DEVE essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ea353-1022">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="ea353-1023">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-1023">0x00000000</span></span> | <span data-ttu-id="ea353-1024">Rappresenta qualsiasi ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1024">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="ea353-1025">**Cb:** intero senza segno a 32 bit contenente la lunghezza di buf, in byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-1025">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="ea353-1026">**buf:** sequenza di byte che rappresenta il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1026">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="ea353-1027">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1027">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="ea353-1028">La struttura CInternalPropertyRestriction contiene un valore di proprietà da associare a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-1028">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="ea353-1029">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1029">0</span></span>

<span data-ttu-id="ea353-1030">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1030">1</span></span>

<span data-ttu-id="ea353-1031">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1031">2</span></span>

<span data-ttu-id="ea353-1032">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1032">3</span></span>

<span data-ttu-id="ea353-1033">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1033">4</span></span>

<span data-ttu-id="ea353-1034">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1034">5</span></span>

<span data-ttu-id="ea353-1035">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1035">6</span></span>

<span data-ttu-id="ea353-1036">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1036">7</span></span>

<span data-ttu-id="ea353-1037">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1037">8</span></span>

<span data-ttu-id="ea353-1038">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1038">9</span></span>

<span data-ttu-id="ea353-1039">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1039">1</span></span><br/> <span data-ttu-id="ea353-1040">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1040">0</span></span><br/>

<span data-ttu-id="ea353-1041">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1041">1</span></span>

<span data-ttu-id="ea353-1042">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1042">2</span></span>

<span data-ttu-id="ea353-1043">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1043">3</span></span>

<span data-ttu-id="ea353-1044">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1044">4</span></span>

<span data-ttu-id="ea353-1045">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1045">5</span></span>

<span data-ttu-id="ea353-1046">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1046">6</span></span>

<span data-ttu-id="ea353-1047">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1047">7</span></span>

<span data-ttu-id="ea353-1048">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1048">8</span></span>

<span data-ttu-id="ea353-1049">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1049">9</span></span>

<span data-ttu-id="ea353-1050">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1050">2</span></span><br/> <span data-ttu-id="ea353-1051">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1051">0</span></span><br/>

<span data-ttu-id="ea353-1052">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1052">1</span></span>

<span data-ttu-id="ea353-1053">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1053">2</span></span>

<span data-ttu-id="ea353-1054">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1054">3</span></span>

<span data-ttu-id="ea353-1055">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1055">4</span></span>

<span data-ttu-id="ea353-1056">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1056">5</span></span>

<span data-ttu-id="ea353-1057">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1057">6</span></span>

<span data-ttu-id="ea353-1058">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1058">7</span></span>

<span data-ttu-id="ea353-1059">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1059">8</span></span>

<span data-ttu-id="ea353-1060">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1060">9</span></span>

<span data-ttu-id="ea353-1061">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1061">3</span></span><br/> <span data-ttu-id="ea353-1062">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1062">0</span></span><br/>

<span data-ttu-id="ea353-1063">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1063">1</span></span>

<span data-ttu-id="ea353-1064">\_lop</span><span class="sxs-lookup"><span data-stu-id="ea353-1064">\_relop</span></span>

<span data-ttu-id="ea353-1065">\_pid</span><span class="sxs-lookup"><span data-stu-id="ea353-1065">\_pid</span></span>

<span data-ttu-id="ea353-1066">\_prval (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1066">\_prval (variable)</span></span>

<span data-ttu-id="ea353-1067">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="ea353-1067">restrictionPresent</span></span>

<span data-ttu-id="ea353-1068">nextRestriction (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1068">nextRestriction (variable)</span></span>



 

<span data-ttu-id="ea353-1069">**\_ relop:** intero a 32 bit che specifica la relazione da eseguire sulla proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1069">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="ea353-1070">DEVE essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-1070">MUST be one of the following values:</span></span>



| <span data-ttu-id="ea353-1071">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1071">Value</span></span>                 | <span data-ttu-id="ea353-1072">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1072">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1073">Prlt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-1073">PRLT 0x00000000</span></span>       | <span data-ttu-id="ea353-1074">Confronto minore di.</span><span class="sxs-lookup"><span data-stu-id="ea353-1074">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="ea353-1075">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-1075">PRLE 0x00000001</span></span>       | <span data-ttu-id="ea353-1076">Confronto minore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="ea353-1076">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="ea353-1077">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-1077">PRGT 0x00000002</span></span>       | <span data-ttu-id="ea353-1078">Confronto maggiore di.</span><span class="sxs-lookup"><span data-stu-id="ea353-1078">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="ea353-1079">PrGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-1079">PRGE 0x00000003</span></span>       | <span data-ttu-id="ea353-1080">Confronto maggiore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="ea353-1080">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="ea353-1081">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-1081">PREQ 0x00000004</span></span>       | <span data-ttu-id="ea353-1082">Confronto di uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="ea353-1082">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="ea353-1083">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="ea353-1083">PRNE 0x00000005</span></span>       | <span data-ttu-id="ea353-1084">Confronto diverso da uguale a .</span><span class="sxs-lookup"><span data-stu-id="ea353-1084">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="ea353-1085">PrRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="ea353-1085">PRRE 0x00000006</span></span>       | <span data-ttu-id="ea353-1086">Confronto di espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="ea353-1086">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="ea353-1087">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="ea353-1087">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="ea353-1088">AND bit per bit che restituisce l'operando destro.</span><span class="sxs-lookup"><span data-stu-id="ea353-1088">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="ea353-1089">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea353-1089">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="ea353-1090">AND bit per bit che restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="ea353-1090">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="ea353-1091">PRTutti 0x00000100</span><span class="sxs-lookup"><span data-stu-id="ea353-1091">PRAll 0x00000100</span></span>      | <span data-ttu-id="ea353-1092">L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-1092">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="ea353-1093">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="ea353-1093">PRAny 0x00000200</span></span>      | <span data-ttu-id="ea353-1094">L'operazione deve essere eseguita su una colonna di un set di righe ed è true se l'operazione è true per qualsiasi riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-1094">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="ea353-1095">**\_ pid:** intero senza segno a 32 bit che rappresenta l'ID proprietà (vedere PROPID nella sezione 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="ea353-1095">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="ea353-1096">**\_ prval:** CBaseStorageVariant contenente il valore da correlare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1096">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="ea353-1097">**restrictionPresent:** valore byte che indica se è presente il campo nextRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1097">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="ea353-1098">DEVE essere impostato su 0x00 o 0x01.</span><span class="sxs-lookup"><span data-stu-id="ea353-1098">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="ea353-1099">Se impostato su 0x01, restrictionPresent indica che è presente il campo nextRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1099">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="ea353-1100">Se impostato su 0x00, restrictionPresent indica che il campo nextRestriction non è presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-1100">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="ea353-1101">**nextRestriction:** struttura CRestriction, come specificato nella sezione 2.2.1.16, che specifica un'ulteriore restrizione.</span><span class="sxs-lookup"><span data-stu-id="ea353-1101">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="ea353-1102">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1102">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="ea353-1103">La struttura CNatLanguageRestriction contiene una corrispondenza di **query in linguaggio** naturale per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1103">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="ea353-1104">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1104">0</span></span>

<span data-ttu-id="ea353-1105">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1105">1</span></span>

<span data-ttu-id="ea353-1106">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1106">2</span></span>

<span data-ttu-id="ea353-1107">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1107">3</span></span>

<span data-ttu-id="ea353-1108">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1108">4</span></span>

<span data-ttu-id="ea353-1109">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1109">5</span></span>

<span data-ttu-id="ea353-1110">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1110">6</span></span>

<span data-ttu-id="ea353-1111">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1111">7</span></span>

<span data-ttu-id="ea353-1112">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1112">8</span></span>

<span data-ttu-id="ea353-1113">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1113">9</span></span>

<span data-ttu-id="ea353-1114">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1114">1</span></span><br/> <span data-ttu-id="ea353-1115">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1115">0</span></span><br/>

<span data-ttu-id="ea353-1116">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1116">1</span></span>

<span data-ttu-id="ea353-1117">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1117">2</span></span>

<span data-ttu-id="ea353-1118">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1118">3</span></span>

<span data-ttu-id="ea353-1119">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1119">4</span></span>

<span data-ttu-id="ea353-1120">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1120">5</span></span>

<span data-ttu-id="ea353-1121">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1121">6</span></span>

<span data-ttu-id="ea353-1122">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1122">7</span></span>

<span data-ttu-id="ea353-1123">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1123">8</span></span>

<span data-ttu-id="ea353-1124">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1124">9</span></span>

<span data-ttu-id="ea353-1125">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1125">2</span></span><br/> <span data-ttu-id="ea353-1126">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1126">0</span></span><br/>

<span data-ttu-id="ea353-1127">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1127">1</span></span>

<span data-ttu-id="ea353-1128">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1128">2</span></span>

<span data-ttu-id="ea353-1129">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1129">3</span></span>

<span data-ttu-id="ea353-1130">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1130">4</span></span>

<span data-ttu-id="ea353-1131">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1131">5</span></span>

<span data-ttu-id="ea353-1132">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1132">6</span></span>

<span data-ttu-id="ea353-1133">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1133">7</span></span>

<span data-ttu-id="ea353-1134">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1134">8</span></span>

<span data-ttu-id="ea353-1135">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1135">9</span></span>

<span data-ttu-id="ea353-1136">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1136">3</span></span><br/> <span data-ttu-id="ea353-1137">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1137">0</span></span><br/>

<span data-ttu-id="ea353-1138">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1138">1</span></span>

<span data-ttu-id="ea353-1139">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1139">\_Property (variable)</span></span>

<span data-ttu-id="ea353-1140">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1140">...</span></span>

<span data-ttu-id="ea353-1141">\_padding \_ cc (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1141">\_padding\_cc (variable)</span></span>

<span data-ttu-id="ea353-1142">Cc</span><span class="sxs-lookup"><span data-stu-id="ea353-1142">Cc</span></span>

<span data-ttu-id="ea353-1143">\_pwcsPhrase (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1143">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="ea353-1144">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1144">...</span></span>

<span data-ttu-id="ea353-1145">\_padding \_ lcid (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1145">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="ea353-1146">LCID</span><span class="sxs-lookup"><span data-stu-id="ea353-1146">Lcid</span></span>



 

<span data-ttu-id="ea353-1147">**\_ Property:** struttura CFullPropSpec, come specificato nella Sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="ea353-1147">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="ea353-1148">Questo campo indica la proprietà in cui eseguire l'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-1148">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="ea353-1149">**\_ padding \_ cc:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-1149">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="ea353-1150">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset pari a un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ea353-1150">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="ea353-1151">Se questo campo è presente (ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-1151">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="ea353-1152">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-1152">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-1153">**Cc:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-1153">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="ea353-1154">Numero di caratteri nel \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="ea353-1154">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="ea353-1155">**\_ pwcsPhrase:** stringa Unicode non con terminazione Null che rappresenta la parola o la frase di cui trovare la corrispondenza per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1155">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="ea353-1156">NON DEVE essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="ea353-1156">MUST NOT be empty.</span></span> <span data-ttu-id="ea353-1157">Il campo Cc contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="ea353-1157">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="ea353-1158">**\_ padding \_ lcid:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-1158">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="ea353-1159">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset pari a un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ea353-1159">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="ea353-1160">Se questo campo è presente (ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-1160">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="ea353-1161">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-1161">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-1162">**Lcid:** intero senza segno a 32 bit che indica le impostazioni locali \_ di pwcsPhrase, come specificato \[ nell'appendice A di MS-GPSI. \]</span><span class="sxs-lookup"><span data-stu-id="ea353-1162">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="ea353-1163">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1163">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="ea353-1164">La struttura CNodeRestriction contiene una matrice **di** nodi dell'albero dei comandi che specificano le restrizioni per la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1164">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="ea353-1165">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1165">0</span></span>

<span data-ttu-id="ea353-1166">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1166">1</span></span>

<span data-ttu-id="ea353-1167">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1167">2</span></span>

<span data-ttu-id="ea353-1168">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1168">3</span></span>

<span data-ttu-id="ea353-1169">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1169">4</span></span>

<span data-ttu-id="ea353-1170">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1170">5</span></span>

<span data-ttu-id="ea353-1171">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1171">6</span></span>

<span data-ttu-id="ea353-1172">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1172">7</span></span>

<span data-ttu-id="ea353-1173">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1173">8</span></span>

<span data-ttu-id="ea353-1174">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1174">9</span></span>

<span data-ttu-id="ea353-1175">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1175">1</span></span><br/> <span data-ttu-id="ea353-1176">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1176">0</span></span><br/>

<span data-ttu-id="ea353-1177">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1177">1</span></span>

<span data-ttu-id="ea353-1178">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1178">2</span></span>

<span data-ttu-id="ea353-1179">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1179">3</span></span>

<span data-ttu-id="ea353-1180">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1180">4</span></span>

<span data-ttu-id="ea353-1181">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1181">5</span></span>

<span data-ttu-id="ea353-1182">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1182">6</span></span>

<span data-ttu-id="ea353-1183">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1183">7</span></span>

<span data-ttu-id="ea353-1184">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1184">8</span></span>

<span data-ttu-id="ea353-1185">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1185">9</span></span>

<span data-ttu-id="ea353-1186">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1186">2</span></span><br/> <span data-ttu-id="ea353-1187">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1187">0</span></span><br/>

<span data-ttu-id="ea353-1188">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1188">1</span></span>

<span data-ttu-id="ea353-1189">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1189">2</span></span>

<span data-ttu-id="ea353-1190">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1190">3</span></span>

<span data-ttu-id="ea353-1191">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1191">4</span></span>

<span data-ttu-id="ea353-1192">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1192">5</span></span>

<span data-ttu-id="ea353-1193">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1193">6</span></span>

<span data-ttu-id="ea353-1194">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1194">7</span></span>

<span data-ttu-id="ea353-1195">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1195">8</span></span>

<span data-ttu-id="ea353-1196">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1196">9</span></span>

<span data-ttu-id="ea353-1197">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1197">3</span></span><br/> <span data-ttu-id="ea353-1198">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1198">0</span></span><br/>

<span data-ttu-id="ea353-1199">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1199">1</span></span>

<span data-ttu-id="ea353-1200">\_cNode</span><span class="sxs-lookup"><span data-stu-id="ea353-1200">\_cNode</span></span>

<span data-ttu-id="ea353-1201">\_paNode (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1201">\_paNode (variable)</span></span>



 

<span data-ttu-id="ea353-1202">**\_ cNode:** intero senza segno a 32 bit che specifica il numero di strutture CRestriction contenute nel \_ campo paNode.</span><span class="sxs-lookup"><span data-stu-id="ea353-1202">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="ea353-1203">**\_ paNode:** matrice di strutture CRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1203">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="ea353-1204">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice.</span><span class="sxs-lookup"><span data-stu-id="ea353-1204">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="ea353-1205">Se sono presenti byte di spaziatura interna, il valore che contengono è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-1205">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="ea353-1206">Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-1206">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="ea353-1207">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1207">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="ea353-1208">La struttura COccRestriction contiene la posizione di una parola in una frase.</span><span class="sxs-lookup"><span data-stu-id="ea353-1208">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="ea353-1209">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1209">0</span></span>

<span data-ttu-id="ea353-1210">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1210">1</span></span>

<span data-ttu-id="ea353-1211">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1211">2</span></span>

<span data-ttu-id="ea353-1212">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1212">3</span></span>

<span data-ttu-id="ea353-1213">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1213">4</span></span>

<span data-ttu-id="ea353-1214">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1214">5</span></span>

<span data-ttu-id="ea353-1215">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1215">6</span></span>

<span data-ttu-id="ea353-1216">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1216">7</span></span>

<span data-ttu-id="ea353-1217">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1217">8</span></span>

<span data-ttu-id="ea353-1218">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1218">9</span></span>

<span data-ttu-id="ea353-1219">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1219">1</span></span><br/> <span data-ttu-id="ea353-1220">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1220">0</span></span><br/>

<span data-ttu-id="ea353-1221">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1221">1</span></span>

<span data-ttu-id="ea353-1222">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1222">2</span></span>

<span data-ttu-id="ea353-1223">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1223">3</span></span>

<span data-ttu-id="ea353-1224">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1224">4</span></span>

<span data-ttu-id="ea353-1225">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1225">5</span></span>

<span data-ttu-id="ea353-1226">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1226">6</span></span>

<span data-ttu-id="ea353-1227">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1227">7</span></span>

<span data-ttu-id="ea353-1228">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1228">8</span></span>

<span data-ttu-id="ea353-1229">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1229">9</span></span>

<span data-ttu-id="ea353-1230">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1230">2</span></span><br/> <span data-ttu-id="ea353-1231">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1231">0</span></span><br/>

<span data-ttu-id="ea353-1232">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1232">1</span></span>

<span data-ttu-id="ea353-1233">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1233">2</span></span>

<span data-ttu-id="ea353-1234">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1234">3</span></span>

<span data-ttu-id="ea353-1235">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1235">4</span></span>

<span data-ttu-id="ea353-1236">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1236">5</span></span>

<span data-ttu-id="ea353-1237">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1237">6</span></span>

<span data-ttu-id="ea353-1238">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1238">7</span></span>

<span data-ttu-id="ea353-1239">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1239">8</span></span>

<span data-ttu-id="ea353-1240">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1240">9</span></span>

<span data-ttu-id="ea353-1241">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1241">3</span></span><br/> <span data-ttu-id="ea353-1242">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1242">0</span></span><br/>

<span data-ttu-id="ea353-1243">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1243">1</span></span>

<span data-ttu-id="ea353-1244">\_Occ</span><span class="sxs-lookup"><span data-stu-id="ea353-1244">\_occ</span></span>

<span data-ttu-id="ea353-1245">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="ea353-1245">\_cPrevNoiseWords</span></span>

<span data-ttu-id="ea353-1246">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="ea353-1246">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="ea353-1247">**\_ occ:** intero senza segno a 32 bit che specifica l'offset della parola in una stringa di query, in unità di parole.</span><span class="sxs-lookup"><span data-stu-id="ea353-1247">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="ea353-1248">Una parola, usata in questa specifica, è un'unità di lingua in tutte le impostazioni locali che hanno significato.</span><span class="sxs-lookup"><span data-stu-id="ea353-1248">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="ea353-1249">**\_ cPrevNoiseWords:** intero senza segno a 32  bit contenente il numero di parole non pronunciate che si verificano tra questa parola e la parola precedente nella frase.</span><span class="sxs-lookup"><span data-stu-id="ea353-1249">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="ea353-1250">**\_ cNextNoiseWords:** intero senza segno a 32 bit contenente il numero di parole non pronunciate che si verificano tra questa parola e la parola successiva nella frase.</span><span class="sxs-lookup"><span data-stu-id="ea353-1250">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="ea353-1251">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1251">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="ea353-1252">La struttura CPropertyRestriction contiene un valore di proprietà da associare a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-1252">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="ea353-1253">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1253">0</span></span>

<span data-ttu-id="ea353-1254">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1254">1</span></span>

<span data-ttu-id="ea353-1255">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1255">2</span></span>

<span data-ttu-id="ea353-1256">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1256">3</span></span>

<span data-ttu-id="ea353-1257">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1257">4</span></span>

<span data-ttu-id="ea353-1258">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1258">5</span></span>

<span data-ttu-id="ea353-1259">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1259">6</span></span>

<span data-ttu-id="ea353-1260">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1260">7</span></span>

<span data-ttu-id="ea353-1261">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1261">8</span></span>

<span data-ttu-id="ea353-1262">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1262">9</span></span>

<span data-ttu-id="ea353-1263">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1263">1</span></span><br/> <span data-ttu-id="ea353-1264">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1264">0</span></span><br/>

<span data-ttu-id="ea353-1265">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1265">1</span></span>

<span data-ttu-id="ea353-1266">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1266">2</span></span>

<span data-ttu-id="ea353-1267">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1267">3</span></span>

<span data-ttu-id="ea353-1268">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1268">4</span></span>

<span data-ttu-id="ea353-1269">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1269">5</span></span>

<span data-ttu-id="ea353-1270">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1270">6</span></span>

<span data-ttu-id="ea353-1271">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1271">7</span></span>

<span data-ttu-id="ea353-1272">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1272">8</span></span>

<span data-ttu-id="ea353-1273">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1273">9</span></span>

<span data-ttu-id="ea353-1274">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1274">2</span></span><br/> <span data-ttu-id="ea353-1275">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1275">0</span></span><br/>

<span data-ttu-id="ea353-1276">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1276">1</span></span>

<span data-ttu-id="ea353-1277">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1277">2</span></span>

<span data-ttu-id="ea353-1278">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1278">3</span></span>

<span data-ttu-id="ea353-1279">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1279">4</span></span>

<span data-ttu-id="ea353-1280">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1280">5</span></span>

<span data-ttu-id="ea353-1281">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1281">6</span></span>

<span data-ttu-id="ea353-1282">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1282">7</span></span>

<span data-ttu-id="ea353-1283">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1283">8</span></span>

<span data-ttu-id="ea353-1284">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1284">9</span></span>

<span data-ttu-id="ea353-1285">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1285">3</span></span><br/> <span data-ttu-id="ea353-1286">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1286">0</span></span><br/>

<span data-ttu-id="ea353-1287">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1287">1</span></span>

<span data-ttu-id="ea353-1288">\_relop</span><span class="sxs-lookup"><span data-stu-id="ea353-1288">\_relop</span></span>

<span data-ttu-id="ea353-1289">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1289">\_Property (variable)</span></span>

<span data-ttu-id="ea353-1290">\_prval (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1290">\_prval (variable)</span></span>



 

<span data-ttu-id="ea353-1291">**\_ relop:** intero senza segno a 32 bit che specifica la relazione da eseguire sulla proprietà .</span><span class="sxs-lookup"><span data-stu-id="ea353-1291">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="ea353-1292">DEVE essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-1292">MUST be one of the following values.</span></span>



| <span data-ttu-id="ea353-1293">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1293">Value</span></span>                 | <span data-ttu-id="ea353-1294">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1294">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1295">0x00000000 PRLT</span><span class="sxs-lookup"><span data-stu-id="ea353-1295">PRLT 0x00000000</span></span>       | <span data-ttu-id="ea353-1296">Confronto minore di.</span><span class="sxs-lookup"><span data-stu-id="ea353-1296">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="ea353-1297">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-1297">PRLE 0x00000001</span></span>       | <span data-ttu-id="ea353-1298">Confronto minore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="ea353-1298">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="ea353-1299">0x00000002 PRGT</span><span class="sxs-lookup"><span data-stu-id="ea353-1299">PRGT 0x00000002</span></span>       | <span data-ttu-id="ea353-1300">Confronto maggiore di.</span><span class="sxs-lookup"><span data-stu-id="ea353-1300">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="ea353-1301">Richiesta pull 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-1301">PRGE 0x00000003</span></span>       | <span data-ttu-id="ea353-1302">Confronto maggiore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="ea353-1302">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="ea353-1303">Preq 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-1303">PREQ 0x00000004</span></span>       | <span data-ttu-id="ea353-1304">Confronto di uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="ea353-1304">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="ea353-1305">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="ea353-1305">PRNE 0x00000005</span></span>       | <span data-ttu-id="ea353-1306">Confronto diverso da.</span><span class="sxs-lookup"><span data-stu-id="ea353-1306">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="ea353-1307">Richiesta pull 0x00000006</span><span class="sxs-lookup"><span data-stu-id="ea353-1307">PRRE 0x00000006</span></span>       | <span data-ttu-id="ea353-1308">Confronto di espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="ea353-1308">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="ea353-1309">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="ea353-1309">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="ea353-1310">AND bit per bit che restituisce l'operando destro.</span><span class="sxs-lookup"><span data-stu-id="ea353-1310">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="ea353-1311">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea353-1311">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="ea353-1312">AND bit per bit che restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="ea353-1312">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="ea353-1313">PRTutti 0x00000100</span><span class="sxs-lookup"><span data-stu-id="ea353-1313">PRAll 0x00000100</span></span>      | <span data-ttu-id="ea353-1314">L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-1314">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="ea353-1315">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="ea353-1315">PRAny 0x00000200</span></span>      | <span data-ttu-id="ea353-1316">L'operazione deve essere eseguita su una colonna di un set di righe ed è true se l'operazione è true per qualsiasi riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-1316">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="ea353-1317">**\_ Proprietà:** struttura CFullPropSpec, come specificato nella Sezione 2.2.1.2, che indica la proprietà su cui eseguire un'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-1317">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="ea353-1318">**\_ prval:** struttura CBaseStorageVariant, come specificato nella Sezione 2.2.1.1, contenente il valore da correlare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1318">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="ea353-1319">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1319">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="ea353-1320">La struttura CRangeRestriction contiene una restrizione per un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="ea353-1320">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="ea353-1321">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1321">0</span></span>

<span data-ttu-id="ea353-1322">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1322">1</span></span>

<span data-ttu-id="ea353-1323">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1323">2</span></span>

<span data-ttu-id="ea353-1324">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1324">3</span></span>

<span data-ttu-id="ea353-1325">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1325">4</span></span>

<span data-ttu-id="ea353-1326">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1326">5</span></span>

<span data-ttu-id="ea353-1327">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1327">6</span></span>

<span data-ttu-id="ea353-1328">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1328">7</span></span>

<span data-ttu-id="ea353-1329">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1329">8</span></span>

<span data-ttu-id="ea353-1330">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1330">9</span></span>

<span data-ttu-id="ea353-1331">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1331">1</span></span><br/> <span data-ttu-id="ea353-1332">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1332">0</span></span><br/>

<span data-ttu-id="ea353-1333">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1333">1</span></span>

<span data-ttu-id="ea353-1334">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1334">2</span></span>

<span data-ttu-id="ea353-1335">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1335">3</span></span>

<span data-ttu-id="ea353-1336">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1336">4</span></span>

<span data-ttu-id="ea353-1337">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1337">5</span></span>

<span data-ttu-id="ea353-1338">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1338">6</span></span>

<span data-ttu-id="ea353-1339">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1339">7</span></span>

<span data-ttu-id="ea353-1340">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1340">8</span></span>

<span data-ttu-id="ea353-1341">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1341">9</span></span>

<span data-ttu-id="ea353-1342">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1342">2</span></span><br/> <span data-ttu-id="ea353-1343">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1343">0</span></span><br/>

<span data-ttu-id="ea353-1344">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1344">1</span></span>

<span data-ttu-id="ea353-1345">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1345">2</span></span>

<span data-ttu-id="ea353-1346">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1346">3</span></span>

<span data-ttu-id="ea353-1347">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1347">4</span></span>

<span data-ttu-id="ea353-1348">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1348">5</span></span>

<span data-ttu-id="ea353-1349">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1349">6</span></span>

<span data-ttu-id="ea353-1350">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1350">7</span></span>

<span data-ttu-id="ea353-1351">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1351">8</span></span>

<span data-ttu-id="ea353-1352">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1352">9</span></span>

<span data-ttu-id="ea353-1353">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1353">3</span></span><br/> <span data-ttu-id="ea353-1354">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1354">0</span></span><br/>

<span data-ttu-id="ea353-1355">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1355">1</span></span>

<span data-ttu-id="ea353-1356">\_keyStart (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1356">\_keyStart (variable)</span></span>

<span data-ttu-id="ea353-1357">\_keyEnd (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1357">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="ea353-1358">**\_ keyStart:** struttura CKey, come specificato nella sezione 2.2.1.4, contenente l'inizio dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="ea353-1358">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="ea353-1359">**\_ keyEnd:** struttura CKey contenente la fine dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="ea353-1359">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="ea353-1360">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1360">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="ea353-1361">La struttura CScopeRestriction contiene una restrizione sui file in cui eseguire la ricerca</span><span class="sxs-lookup"><span data-stu-id="ea353-1361">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="ea353-1362">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1362">0</span></span>

<span data-ttu-id="ea353-1363">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1363">1</span></span>

<span data-ttu-id="ea353-1364">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1364">2</span></span>

<span data-ttu-id="ea353-1365">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1365">3</span></span>

<span data-ttu-id="ea353-1366">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1366">4</span></span>

<span data-ttu-id="ea353-1367">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1367">5</span></span>

<span data-ttu-id="ea353-1368">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1368">6</span></span>

<span data-ttu-id="ea353-1369">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1369">7</span></span>

<span data-ttu-id="ea353-1370">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1370">8</span></span>

<span data-ttu-id="ea353-1371">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1371">9</span></span>

<span data-ttu-id="ea353-1372">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1372">1</span></span><br/> <span data-ttu-id="ea353-1373">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1373">0</span></span><br/>

<span data-ttu-id="ea353-1374">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1374">1</span></span>

<span data-ttu-id="ea353-1375">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1375">2</span></span>

<span data-ttu-id="ea353-1376">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1376">3</span></span>

<span data-ttu-id="ea353-1377">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1377">4</span></span>

<span data-ttu-id="ea353-1378">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1378">5</span></span>

<span data-ttu-id="ea353-1379">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1379">6</span></span>

<span data-ttu-id="ea353-1380">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1380">7</span></span>

<span data-ttu-id="ea353-1381">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1381">8</span></span>

<span data-ttu-id="ea353-1382">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1382">9</span></span>

<span data-ttu-id="ea353-1383">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1383">2</span></span><br/> <span data-ttu-id="ea353-1384">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1384">0</span></span><br/>

<span data-ttu-id="ea353-1385">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1385">1</span></span>

<span data-ttu-id="ea353-1386">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1386">2</span></span>

<span data-ttu-id="ea353-1387">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1387">3</span></span>

<span data-ttu-id="ea353-1388">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1388">4</span></span>

<span data-ttu-id="ea353-1389">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1389">5</span></span>

<span data-ttu-id="ea353-1390">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1390">6</span></span>

<span data-ttu-id="ea353-1391">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1391">7</span></span>

<span data-ttu-id="ea353-1392">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1392">8</span></span>

<span data-ttu-id="ea353-1393">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1393">9</span></span>

<span data-ttu-id="ea353-1394">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1394">3</span></span><br/> <span data-ttu-id="ea353-1395">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1395">0</span></span><br/>

<span data-ttu-id="ea353-1396">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1396">1</span></span>

<span data-ttu-id="ea353-1397">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="ea353-1397">CcLowerPath</span></span>

<span data-ttu-id="ea353-1398">\_lowerPath (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1398">\_lowerPath (variable)</span></span>

<span data-ttu-id="ea353-1399">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1399">...</span></span>

<span data-ttu-id="ea353-1400">\_padding (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1400">\_padding ( variable)</span></span>

<span data-ttu-id="ea353-1401">\_Lunghezza</span><span class="sxs-lookup"><span data-stu-id="ea353-1401">\_length</span></span>

<span data-ttu-id="ea353-1402">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="ea353-1402">\_fRecursive</span></span>

<span data-ttu-id="ea353-1403">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="ea353-1403">\_fVirtual</span></span>



 

<span data-ttu-id="ea353-1404">**CcLowerPath:** intero senza segno a 32 bit contenente il numero di caratteri Unicode nel \_ campo lowerPath.</span><span class="sxs-lookup"><span data-stu-id="ea353-1404">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="ea353-1405">**\_ lowerPath:** stringa Unicode non con terminazione Null che rappresenta il **percorso** a cui la query deve essere limitata.</span><span class="sxs-lookup"><span data-stu-id="ea353-1405">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="ea353-1406">Il campo CcLowerPath contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="ea353-1406">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="ea353-1407">**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-1407">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="ea353-1408">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset pari a un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ea353-1408">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="ea353-1409">Se questo campo è presente (ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-1409">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="ea353-1410">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-1410">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-1411">**\_ length:** intero senza segno a 32 bit contenente la lunghezza di \_ lowerPath, in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="ea353-1411">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="ea353-1412">Deve essere lo stesso valore di CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="ea353-1412">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="ea353-1413">**\_ fRecursive:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-1413">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="ea353-1414">DEVE essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-1414">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="ea353-1415">Se impostato su 0x00000001, il server deve esaminare in modo ricorsivo tutte le sottodirectory del percorso.</span><span class="sxs-lookup"><span data-stu-id="ea353-1415">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="ea353-1416">Se impostato su 0x00000000, il server non esamina le sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="ea353-1416">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="ea353-1417">**\_ fVirtual:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-1417">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="ea353-1418">DEVE essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-1418">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="ea353-1419">Se impostato su 0x00000001, lowerPath è un percorso virtuale (Uniform Resource Locator (URL) associato a una directory fisica nel \_ file system) per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="ea353-1419">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="ea353-1420">Se impostato su 0x00000000, \_ lowerPath è un file system percorso.</span><span class="sxs-lookup"><span data-stu-id="ea353-1420">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="ea353-1421">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="ea353-1421">2.2.1.12 CSort</span></span>

<span data-ttu-id="ea353-1422">La struttura CSort identifica una colonna da ordinare.</span><span class="sxs-lookup"><span data-stu-id="ea353-1422">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="ea353-1423">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1423">0</span></span>

<span data-ttu-id="ea353-1424">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1424">1</span></span>

<span data-ttu-id="ea353-1425">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1425">2</span></span>

<span data-ttu-id="ea353-1426">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1426">3</span></span>

<span data-ttu-id="ea353-1427">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1427">4</span></span>

<span data-ttu-id="ea353-1428">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1428">5</span></span>

<span data-ttu-id="ea353-1429">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1429">6</span></span>

<span data-ttu-id="ea353-1430">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1430">7</span></span>

<span data-ttu-id="ea353-1431">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1431">8</span></span>

<span data-ttu-id="ea353-1432">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1432">9</span></span>

<span data-ttu-id="ea353-1433">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1433">1</span></span><br/> <span data-ttu-id="ea353-1434">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1434">0</span></span><br/>

<span data-ttu-id="ea353-1435">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1435">1</span></span>

<span data-ttu-id="ea353-1436">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1436">2</span></span>

<span data-ttu-id="ea353-1437">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1437">3</span></span>

<span data-ttu-id="ea353-1438">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1438">4</span></span>

<span data-ttu-id="ea353-1439">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1439">5</span></span>

<span data-ttu-id="ea353-1440">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1440">6</span></span>

<span data-ttu-id="ea353-1441">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1441">7</span></span>

<span data-ttu-id="ea353-1442">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1442">8</span></span>

<span data-ttu-id="ea353-1443">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1443">9</span></span>

<span data-ttu-id="ea353-1444">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1444">2</span></span><br/> <span data-ttu-id="ea353-1445">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1445">0</span></span><br/>

<span data-ttu-id="ea353-1446">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1446">1</span></span>

<span data-ttu-id="ea353-1447">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1447">2</span></span>

<span data-ttu-id="ea353-1448">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1448">3</span></span>

<span data-ttu-id="ea353-1449">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1449">4</span></span>

<span data-ttu-id="ea353-1450">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1450">5</span></span>

<span data-ttu-id="ea353-1451">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1451">6</span></span>

<span data-ttu-id="ea353-1452">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1452">7</span></span>

<span data-ttu-id="ea353-1453">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1453">8</span></span>

<span data-ttu-id="ea353-1454">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1454">9</span></span>

<span data-ttu-id="ea353-1455">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1455">3</span></span><br/> <span data-ttu-id="ea353-1456">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1456">0</span></span><br/>

<span data-ttu-id="ea353-1457">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1457">1</span></span>

<span data-ttu-id="ea353-1458">pidColumn</span><span class="sxs-lookup"><span data-stu-id="ea353-1458">pidColumn</span></span>

<span data-ttu-id="ea353-1459">dwOrder</span><span class="sxs-lookup"><span data-stu-id="ea353-1459">dwOrder</span></span>

<span data-ttu-id="ea353-1460">locale</span><span class="sxs-lookup"><span data-stu-id="ea353-1460">locale</span></span>



 

<span data-ttu-id="ea353-1461">**pidColumn:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-1461">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="ea353-1462">Numero della colonna in base alla quale eseguire l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="ea353-1462">The number of the column to sort by.</span></span>

<span data-ttu-id="ea353-1463">**dwOrder:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-1463">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="ea353-1464">DEVE essere uno dei valori seguenti, specificando come eseguire l'ordinamento in base alla colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-1464">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="ea353-1465">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1465">Value</span></span>                        | <span data-ttu-id="ea353-1466">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1466">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1467">QUERY \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-1467">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="ea353-1468">Le righe devono essere ordinate in ordine crescente in base ai valori nella colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="ea353-1468">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="ea353-1469">QUERY \_ DESCEND 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-1469">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="ea353-1470">Le righe devono essere ordinate in ordine decrescente in base ai valori nella colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="ea353-1470">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="ea353-1471">**locale:** intero senza segno a 32 bit che indica le impostazioni locali, come specificato \[ nell'appendice A MS-GPSI, \] della colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-1471">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="ea353-1472">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1472">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="ea353-1473">La struttura CSynRestriction contiene una parola o i relativi sinonimi per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1473">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="ea353-1474">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1474">0</span></span>

<span data-ttu-id="ea353-1475">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1475">1</span></span>

<span data-ttu-id="ea353-1476">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1476">2</span></span>

<span data-ttu-id="ea353-1477">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1477">3</span></span>

<span data-ttu-id="ea353-1478">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1478">4</span></span>

<span data-ttu-id="ea353-1479">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1479">5</span></span>

<span data-ttu-id="ea353-1480">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1480">6</span></span>

<span data-ttu-id="ea353-1481">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1481">7</span></span>

<span data-ttu-id="ea353-1482">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1482">8</span></span>

<span data-ttu-id="ea353-1483">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1483">9</span></span>

<span data-ttu-id="ea353-1484">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1484">1</span></span><br/> <span data-ttu-id="ea353-1485">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1485">0</span></span><br/>

<span data-ttu-id="ea353-1486">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1486">1</span></span>

<span data-ttu-id="ea353-1487">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1487">2</span></span>

<span data-ttu-id="ea353-1488">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1488">3</span></span>

<span data-ttu-id="ea353-1489">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1489">4</span></span>

<span data-ttu-id="ea353-1490">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1490">5</span></span>

<span data-ttu-id="ea353-1491">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1491">6</span></span>

<span data-ttu-id="ea353-1492">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1492">7</span></span>

<span data-ttu-id="ea353-1493">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1493">8</span></span>

<span data-ttu-id="ea353-1494">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1494">9</span></span>

<span data-ttu-id="ea353-1495">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1495">2</span></span><br/> <span data-ttu-id="ea353-1496">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1496">0</span></span><br/>

<span data-ttu-id="ea353-1497">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1497">1</span></span>

<span data-ttu-id="ea353-1498">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1498">2</span></span>

<span data-ttu-id="ea353-1499">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1499">3</span></span>

<span data-ttu-id="ea353-1500">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1500">4</span></span>

<span data-ttu-id="ea353-1501">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1501">5</span></span>

<span data-ttu-id="ea353-1502">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1502">6</span></span>

<span data-ttu-id="ea353-1503">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1503">7</span></span>

<span data-ttu-id="ea353-1504">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1504">8</span></span>

<span data-ttu-id="ea353-1505">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1505">9</span></span>

<span data-ttu-id="ea353-1506">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1506">3</span></span><br/> <span data-ttu-id="ea353-1507">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1507">0</span></span><br/>

<span data-ttu-id="ea353-1508">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1508">1</span></span>

<span data-ttu-id="ea353-1509">Restrizione</span><span class="sxs-lookup"><span data-stu-id="ea353-1509">Restriction</span></span>

<span data-ttu-id="ea353-1510">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1510">...</span></span>

<span data-ttu-id="ea353-1511">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1511">...</span></span>

<span data-ttu-id="ea353-1512">cKey</span><span class="sxs-lookup"><span data-stu-id="ea353-1512">cKey</span></span>

<span data-ttu-id="ea353-1513">\_keyArray (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1513">\_keyArray (variable)</span></span>

<span data-ttu-id="ea353-1514">\_isRange</span><span class="sxs-lookup"><span data-stu-id="ea353-1514">\_isRange</span></span>



 

<span data-ttu-id="ea353-1515">**Restrizione:** struttura COccRestriction che specifica la posizione della parola.</span><span class="sxs-lookup"><span data-stu-id="ea353-1515">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="ea353-1516">**cKey:** intero senza segno a 32 bit che specifica il numero di elementi nella \_ matrice keyArray.</span><span class="sxs-lookup"><span data-stu-id="ea353-1516">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="ea353-1517">**\_ keyArray:** matrice di strutture CKey che specifica una parola e i relativi sinonimi.</span><span class="sxs-lookup"><span data-stu-id="ea353-1517">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="ea353-1518">**\_ isRange:** se impostato su 0x01, le chiavi sono prefissi per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-1518">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="ea353-1519">Se impostato su 0x00, le chiavi sono valori esatti di cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-1519">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="ea353-1520">\_isRange NON DEVE essere impostato su altri valori.</span><span class="sxs-lookup"><span data-stu-id="ea353-1520">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="ea353-1521">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1521">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="ea353-1522">La struttura CVectorRestriction contiene un'operazione OR ponderata su un nodo della struttura ad albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="ea353-1522">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="ea353-1523">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1523">0</span></span>

<span data-ttu-id="ea353-1524">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1524">1</span></span>

<span data-ttu-id="ea353-1525">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1525">2</span></span>

<span data-ttu-id="ea353-1526">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1526">3</span></span>

<span data-ttu-id="ea353-1527">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1527">4</span></span>

<span data-ttu-id="ea353-1528">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1528">5</span></span>

<span data-ttu-id="ea353-1529">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1529">6</span></span>

<span data-ttu-id="ea353-1530">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1530">7</span></span>

<span data-ttu-id="ea353-1531">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1531">8</span></span>

<span data-ttu-id="ea353-1532">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1532">9</span></span>

<span data-ttu-id="ea353-1533">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1533">1</span></span><br/> <span data-ttu-id="ea353-1534">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1534">0</span></span><br/>

<span data-ttu-id="ea353-1535">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1535">1</span></span>

<span data-ttu-id="ea353-1536">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1536">2</span></span>

<span data-ttu-id="ea353-1537">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1537">3</span></span>

<span data-ttu-id="ea353-1538">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1538">4</span></span>

<span data-ttu-id="ea353-1539">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1539">5</span></span>

<span data-ttu-id="ea353-1540">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1540">6</span></span>

<span data-ttu-id="ea353-1541">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1541">7</span></span>

<span data-ttu-id="ea353-1542">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1542">8</span></span>

<span data-ttu-id="ea353-1543">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1543">9</span></span>

<span data-ttu-id="ea353-1544">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1544">2</span></span><br/> <span data-ttu-id="ea353-1545">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1545">0</span></span><br/>

<span data-ttu-id="ea353-1546">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1546">1</span></span>

<span data-ttu-id="ea353-1547">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1547">2</span></span>

<span data-ttu-id="ea353-1548">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1548">3</span></span>

<span data-ttu-id="ea353-1549">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1549">4</span></span>

<span data-ttu-id="ea353-1550">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1550">5</span></span>

<span data-ttu-id="ea353-1551">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1551">6</span></span>

<span data-ttu-id="ea353-1552">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1552">7</span></span>

<span data-ttu-id="ea353-1553">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1553">8</span></span>

<span data-ttu-id="ea353-1554">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1554">9</span></span>

<span data-ttu-id="ea353-1555">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1555">3</span></span><br/> <span data-ttu-id="ea353-1556">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1556">0</span></span><br/>

<span data-ttu-id="ea353-1557">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1557">1</span></span>

<span data-ttu-id="ea353-1558">\_pres (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1558">\_pres (variable)</span></span>

<span data-ttu-id="ea353-1559">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1559">...</span></span>

<span data-ttu-id="ea353-1560">\_padding (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1560">\_padding (variable)</span></span>

<span data-ttu-id="ea353-1561">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="ea353-1561">\_ulRankMethod</span></span>



 

<span data-ttu-id="ea353-1562">**\_ pres:** albero dei comandi CNodeRestriction su cui deve essere eseguita un'operazione OR classificata.</span><span class="sxs-lookup"><span data-stu-id="ea353-1562">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="ea353-1563">**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-1563">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="ea353-1564">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ea353-1564">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="ea353-1565">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-1565">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="ea353-1566">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-1566">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-1567">**\_ ulRankMethod:** intero senza segno a 32 bit che specifica un algoritmo di classificazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-1567">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="ea353-1568">DEVE essere impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-1568">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="ea353-1569">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1569">Value</span></span>                            | <span data-ttu-id="ea353-1570">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1570">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="ea353-1571">NUMERO \_ MINIMO DI CLASSIFICAZIONE \_ VETTORIALE 0X00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-1571">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="ea353-1572">Usare l'algoritmo \[ minimo SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="ea353-1572">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="ea353-1573">VECTOR \_ RANK \_ MAX 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-1573">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="ea353-1574">Usare l'algoritmo \[ massimo SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="ea353-1574">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="ea353-1575">VETTORE \_ RANK \_ INNER 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-1575">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="ea353-1576">Usare l'algoritmo del \[ prodotto interno \] SALTON.</span><span class="sxs-lookup"><span data-stu-id="ea353-1576">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="ea353-1577">VECTOR \_ RANK \_ DICE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-1577">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="ea353-1578">Usare l'algoritmo del \[ coefficiente Dice SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="ea353-1578">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="ea353-1579">VECTOR \_ RANK \_ E 0X00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-1579">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="ea353-1580">Usare l'algoritmo del \[ coefficiente Diffycard SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="ea353-1580">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="ea353-1581">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1581">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="ea353-1582">La struttura CWordRestriction contiene una parola per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1582">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="ea353-1583">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1583">0</span></span>

<span data-ttu-id="ea353-1584">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1584">1</span></span>

<span data-ttu-id="ea353-1585">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1585">2</span></span>

<span data-ttu-id="ea353-1586">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1586">3</span></span>

<span data-ttu-id="ea353-1587">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1587">4</span></span>

<span data-ttu-id="ea353-1588">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1588">5</span></span>

<span data-ttu-id="ea353-1589">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1589">6</span></span>

<span data-ttu-id="ea353-1590">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1590">7</span></span>

<span data-ttu-id="ea353-1591">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1591">8</span></span>

<span data-ttu-id="ea353-1592">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1592">9</span></span>

<span data-ttu-id="ea353-1593">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1593">1</span></span><br/> <span data-ttu-id="ea353-1594">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1594">0</span></span><br/>

<span data-ttu-id="ea353-1595">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1595">1</span></span>

<span data-ttu-id="ea353-1596">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1596">2</span></span>

<span data-ttu-id="ea353-1597">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1597">3</span></span>

<span data-ttu-id="ea353-1598">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1598">4</span></span>

<span data-ttu-id="ea353-1599">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1599">5</span></span>

<span data-ttu-id="ea353-1600">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1600">6</span></span>

<span data-ttu-id="ea353-1601">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1601">7</span></span>

<span data-ttu-id="ea353-1602">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1602">8</span></span>

<span data-ttu-id="ea353-1603">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1603">9</span></span>

<span data-ttu-id="ea353-1604">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1604">2</span></span><br/> <span data-ttu-id="ea353-1605">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1605">0</span></span><br/>

<span data-ttu-id="ea353-1606">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1606">1</span></span>

<span data-ttu-id="ea353-1607">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1607">2</span></span>

<span data-ttu-id="ea353-1608">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1608">3</span></span>

<span data-ttu-id="ea353-1609">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1609">4</span></span>

<span data-ttu-id="ea353-1610">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1610">5</span></span>

<span data-ttu-id="ea353-1611">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1611">6</span></span>

<span data-ttu-id="ea353-1612">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1612">7</span></span>

<span data-ttu-id="ea353-1613">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1613">8</span></span>

<span data-ttu-id="ea353-1614">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1614">9</span></span>

<span data-ttu-id="ea353-1615">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1615">3</span></span><br/> <span data-ttu-id="ea353-1616">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1616">0</span></span><br/>

<span data-ttu-id="ea353-1617">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1617">1</span></span>

<span data-ttu-id="ea353-1618">restrizione</span><span class="sxs-lookup"><span data-stu-id="ea353-1618">restriction</span></span>

<span data-ttu-id="ea353-1619">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1619">...</span></span>

<span data-ttu-id="ea353-1620">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1620">...</span></span>

<span data-ttu-id="ea353-1621">\_key (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1621">\_key (variable)</span></span>

<span data-ttu-id="ea353-1622">\_isRange</span><span class="sxs-lookup"><span data-stu-id="ea353-1622">\_isRange</span></span>



 

<span data-ttu-id="ea353-1623">**restriction:** struttura COccRestriction che specifica la posizione della parola.</span><span class="sxs-lookup"><span data-stu-id="ea353-1623">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="ea353-1624">**\_ key:** struttura CKey che specifica una parola.</span><span class="sxs-lookup"><span data-stu-id="ea353-1624">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="ea353-1625">**\_ isRange:** se impostato su 0x01, la chiave è un prefisso di cui trovare la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-1625">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="ea353-1626">Se impostato su 0x00, la chiave è un valore esatto di cui trovare la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-1626">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="ea353-1627">\_isRange NON DEVE essere impostato su qualsiasi altro valore.</span><span class="sxs-lookup"><span data-stu-id="ea353-1627">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="ea353-1628">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="ea353-1628">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="ea353-1629">La struttura CRestriction contiene un nodo di un albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1629">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="ea353-1630">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1630">0</span></span>

<span data-ttu-id="ea353-1631">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1631">1</span></span>

<span data-ttu-id="ea353-1632">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1632">2</span></span>

<span data-ttu-id="ea353-1633">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1633">3</span></span>

<span data-ttu-id="ea353-1634">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1634">4</span></span>

<span data-ttu-id="ea353-1635">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1635">5</span></span>

<span data-ttu-id="ea353-1636">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1636">6</span></span>

<span data-ttu-id="ea353-1637">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1637">7</span></span>

<span data-ttu-id="ea353-1638">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1638">8</span></span>

<span data-ttu-id="ea353-1639">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1639">9</span></span>

<span data-ttu-id="ea353-1640">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1640">1</span></span><br/> <span data-ttu-id="ea353-1641">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1641">0</span></span><br/>

<span data-ttu-id="ea353-1642">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1642">1</span></span>

<span data-ttu-id="ea353-1643">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1643">2</span></span>

<span data-ttu-id="ea353-1644">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1644">3</span></span>

<span data-ttu-id="ea353-1645">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1645">4</span></span>

<span data-ttu-id="ea353-1646">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1646">5</span></span>

<span data-ttu-id="ea353-1647">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1647">6</span></span>

<span data-ttu-id="ea353-1648">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1648">7</span></span>

<span data-ttu-id="ea353-1649">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1649">8</span></span>

<span data-ttu-id="ea353-1650">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1650">9</span></span>

<span data-ttu-id="ea353-1651">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1651">2</span></span><br/> <span data-ttu-id="ea353-1652">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1652">0</span></span><br/>

<span data-ttu-id="ea353-1653">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1653">1</span></span>

<span data-ttu-id="ea353-1654">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1654">2</span></span>

<span data-ttu-id="ea353-1655">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1655">3</span></span>

<span data-ttu-id="ea353-1656">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1656">4</span></span>

<span data-ttu-id="ea353-1657">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1657">5</span></span>

<span data-ttu-id="ea353-1658">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1658">6</span></span>

<span data-ttu-id="ea353-1659">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1659">7</span></span>

<span data-ttu-id="ea353-1660">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1660">8</span></span>

<span data-ttu-id="ea353-1661">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1661">9</span></span>

<span data-ttu-id="ea353-1662">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1662">3</span></span><br/> <span data-ttu-id="ea353-1663">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1663">0</span></span><br/>

<span data-ttu-id="ea353-1664">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1664">1</span></span>

<span data-ttu-id="ea353-1665">\_ulType</span><span class="sxs-lookup"><span data-stu-id="ea353-1665">\_ulType</span></span>

<span data-ttu-id="ea353-1666">Peso</span><span class="sxs-lookup"><span data-stu-id="ea353-1666">Weight</span></span>

<span data-ttu-id="ea353-1667">Restrizione</span><span class="sxs-lookup"><span data-stu-id="ea353-1667">Restriction</span></span>



 

<span data-ttu-id="ea353-1668">**\_ ulType:** intero senza segno a 32 bit che indica il tipo di restrizione usato per il nodo dell'albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="ea353-1668">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="ea353-1669">DEVE essere impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-1669">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="ea353-1670">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1670">Value</span></span>                    | <span data-ttu-id="ea353-1671">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1671">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1672">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-1672">RTNone 0x00000000</span></span>        | <span data-ttu-id="ea353-1673">Il nodo rappresenta una parola non erta in una query vettoriale.</span><span class="sxs-lookup"><span data-stu-id="ea353-1673">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="ea353-1674">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-1674">RTAnd 0x00000001</span></span>         | <span data-ttu-id="ea353-1675">Il nodo contiene un CNodeRestriction su cui deve essere eseguita un'operazione AND logica.</span><span class="sxs-lookup"><span data-stu-id="ea353-1675">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="ea353-1676">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-1676">RTOr 0x00000002</span></span>          | <span data-ttu-id="ea353-1677">Il nodo contiene un CNodeRestriction su cui deve essere eseguita un'operazione or logica.</span><span class="sxs-lookup"><span data-stu-id="ea353-1677">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="ea353-1678">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-1678">RTNot 0x00000003</span></span>         | <span data-ttu-id="ea353-1679">Il nodo contiene un CRestriction su cui deve essere eseguita un'operazione NOT.</span><span class="sxs-lookup"><span data-stu-id="ea353-1679">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="ea353-1680">RtContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-1680">RTContent 0x00000004</span></span>     | <span data-ttu-id="ea353-1681">Il nodo contiene un CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1681">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="ea353-1682">RtProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="ea353-1682">RTProperty 0x00000005</span></span>    | <span data-ttu-id="ea353-1683">Il nodo contiene un oggetto CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1683">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="ea353-1684">RtProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="ea353-1684">RTProximity 0x00000006</span></span>   | <span data-ttu-id="ea353-1685">Il nodo contiene un oggetto CNodeRestriction su cui deve essere eseguita una classificazione di prossimità,</span><span class="sxs-lookup"><span data-stu-id="ea353-1685">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="ea353-1686">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="ea353-1686">RTVector 0x00000007</span></span>      | <span data-ttu-id="ea353-1687">Il nodo contiene un CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1687">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="ea353-1688">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea353-1688">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="ea353-1689">Il nodo contiene un CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1689">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="ea353-1690">RtScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="ea353-1690">RTScope 0x00000009</span></span>       | <span data-ttu-id="ea353-1691">Il nodo contiene un CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1691">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="ea353-1692">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="ea353-1692">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="ea353-1693">Il nodo contiene un oggetto CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1693">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="ea353-1694">RtRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="ea353-1694">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="ea353-1695">Il nodo contiene un oggetto CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1695">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="ea353-1696">RtPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="ea353-1696">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="ea353-1697">Il nodo contiene un oggetto CNodeRestriction su cui deve essere eseguita una corrispondenza di frase.</span><span class="sxs-lookup"><span data-stu-id="ea353-1697">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="ea353-1698">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="ea353-1698">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="ea353-1699">Il nodo contiene un CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1699">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="ea353-1700">RtWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="ea353-1700">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="ea353-1701">Il nodo contiene un CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-1701">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="ea353-1702">**Weight:** intero senza segno a 32 bit che rappresenta il peso del nodo.</span><span class="sxs-lookup"><span data-stu-id="ea353-1702">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="ea353-1703">Weight indica l'importanza del nodo rispetto ad altri nodi nell'albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1703">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="ea353-1704">I valori di peso più elevati sono più importanti.</span><span class="sxs-lookup"><span data-stu-id="ea353-1704">Higher weight values are more important.</span></span>

<span data-ttu-id="ea353-1705">**Restrizione**: tipo di restrizione per il nodo dell'albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="ea353-1705">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="ea353-1706">La sintassi DEVE essere indicata dal \_ campo ulType.</span><span class="sxs-lookup"><span data-stu-id="ea353-1706">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="ea353-1707">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="ea353-1707">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="ea353-1708">La struttura CColumnSet specifica i numeri di colonna da restituire.</span><span class="sxs-lookup"><span data-stu-id="ea353-1708">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="ea353-1709">Questa struttura viene sempre usata in riferimento a una struttura CPidMapper specifica (sezione 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="ea353-1709">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="ea353-1710">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1710">0</span></span>

<span data-ttu-id="ea353-1711">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1711">1</span></span>

<span data-ttu-id="ea353-1712">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1712">2</span></span>

<span data-ttu-id="ea353-1713">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1713">3</span></span>

<span data-ttu-id="ea353-1714">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1714">4</span></span>

<span data-ttu-id="ea353-1715">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1715">5</span></span>

<span data-ttu-id="ea353-1716">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1716">6</span></span>

<span data-ttu-id="ea353-1717">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1717">7</span></span>

<span data-ttu-id="ea353-1718">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1718">8</span></span>

<span data-ttu-id="ea353-1719">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1719">9</span></span>

<span data-ttu-id="ea353-1720">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1720">1</span></span><br/> <span data-ttu-id="ea353-1721">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1721">0</span></span><br/>

<span data-ttu-id="ea353-1722">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1722">1</span></span>

<span data-ttu-id="ea353-1723">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1723">2</span></span>

<span data-ttu-id="ea353-1724">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1724">3</span></span>

<span data-ttu-id="ea353-1725">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1725">4</span></span>

<span data-ttu-id="ea353-1726">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1726">5</span></span>

<span data-ttu-id="ea353-1727">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1727">6</span></span>

<span data-ttu-id="ea353-1728">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1728">7</span></span>

<span data-ttu-id="ea353-1729">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1729">8</span></span>

<span data-ttu-id="ea353-1730">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1730">9</span></span>

<span data-ttu-id="ea353-1731">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1731">2</span></span><br/> <span data-ttu-id="ea353-1732">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1732">0</span></span><br/>

<span data-ttu-id="ea353-1733">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1733">1</span></span>

<span data-ttu-id="ea353-1734">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1734">2</span></span>

<span data-ttu-id="ea353-1735">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1735">3</span></span>

<span data-ttu-id="ea353-1736">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1736">4</span></span>

<span data-ttu-id="ea353-1737">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1737">5</span></span>

<span data-ttu-id="ea353-1738">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1738">6</span></span>

<span data-ttu-id="ea353-1739">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1739">7</span></span>

<span data-ttu-id="ea353-1740">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1740">8</span></span>

<span data-ttu-id="ea353-1741">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1741">9</span></span>

<span data-ttu-id="ea353-1742">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1742">3</span></span><br/> <span data-ttu-id="ea353-1743">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1743">0</span></span><br/>

<span data-ttu-id="ea353-1744">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1744">1</span></span>

<span data-ttu-id="ea353-1745">count</span><span class="sxs-lookup"><span data-stu-id="ea353-1745">count</span></span>

<span data-ttu-id="ea353-1746">indexes (variable)</span><span class="sxs-lookup"><span data-stu-id="ea353-1746">indexes (variable)</span></span>



 

<span data-ttu-id="ea353-1747">**count:** intero senza segno a 32 bit che specifica il numero di elementi nella matrice di indici.</span><span class="sxs-lookup"><span data-stu-id="ea353-1747">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="ea353-1748">**indexes:** matrice di interi senza segno a 4 byte che rappresentano indici in base zero nella matrice aPropSpec nella struttura CPidMapper corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ea353-1748">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="ea353-1749">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="ea353-1749">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="ea353-1750">La struttura CCategorizationSet contiene informazioni sul raggruppamento di un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1750">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="ea353-1751">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1751">0</span></span>

<span data-ttu-id="ea353-1752">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1752">1</span></span>

<span data-ttu-id="ea353-1753">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1753">2</span></span>

<span data-ttu-id="ea353-1754">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1754">3</span></span>

<span data-ttu-id="ea353-1755">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1755">4</span></span>

<span data-ttu-id="ea353-1756">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1756">5</span></span>

<span data-ttu-id="ea353-1757">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1757">6</span></span>

<span data-ttu-id="ea353-1758">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1758">7</span></span>

<span data-ttu-id="ea353-1759">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1759">8</span></span>

<span data-ttu-id="ea353-1760">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1760">9</span></span>

<span data-ttu-id="ea353-1761">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1761">1</span></span><br/> <span data-ttu-id="ea353-1762">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1762">0</span></span><br/>

<span data-ttu-id="ea353-1763">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1763">1</span></span>

<span data-ttu-id="ea353-1764">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1764">2</span></span>

<span data-ttu-id="ea353-1765">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1765">3</span></span>

<span data-ttu-id="ea353-1766">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1766">4</span></span>

<span data-ttu-id="ea353-1767">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1767">5</span></span>

<span data-ttu-id="ea353-1768">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1768">6</span></span>

<span data-ttu-id="ea353-1769">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1769">7</span></span>

<span data-ttu-id="ea353-1770">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1770">8</span></span>

<span data-ttu-id="ea353-1771">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1771">9</span></span>

<span data-ttu-id="ea353-1772">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1772">2</span></span><br/> <span data-ttu-id="ea353-1773">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1773">0</span></span><br/>

<span data-ttu-id="ea353-1774">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1774">1</span></span>

<span data-ttu-id="ea353-1775">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1775">2</span></span>

<span data-ttu-id="ea353-1776">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1776">3</span></span>

<span data-ttu-id="ea353-1777">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1777">4</span></span>

<span data-ttu-id="ea353-1778">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1778">5</span></span>

<span data-ttu-id="ea353-1779">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1779">6</span></span>

<span data-ttu-id="ea353-1780">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1780">7</span></span>

<span data-ttu-id="ea353-1781">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1781">8</span></span>

<span data-ttu-id="ea353-1782">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1782">9</span></span>

<span data-ttu-id="ea353-1783">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1783">3</span></span><br/> <span data-ttu-id="ea353-1784">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1784">0</span></span><br/>

<span data-ttu-id="ea353-1785">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1785">1</span></span>

<span data-ttu-id="ea353-1786">count</span><span class="sxs-lookup"><span data-stu-id="ea353-1786">count</span></span>

<span data-ttu-id="ea353-1787">categories (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1787">categories (variable)</span></span>



 

<span data-ttu-id="ea353-1788">**count:** intero senza segno a 32 bit contenente il numero di elementi nella matrice categories.</span><span class="sxs-lookup"><span data-stu-id="ea353-1788">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="ea353-1789">**categories:** matrice di strutture CCategorizationSpec che specificano il raggruppamento della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1789">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="ea353-1790">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="ea353-1790">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="ea353-1791">La struttura CCategorizationSpec contiene un raggruppamento per un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1791">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="ea353-1792">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1792">0</span></span>

<span data-ttu-id="ea353-1793">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1793">1</span></span>

<span data-ttu-id="ea353-1794">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1794">2</span></span>

<span data-ttu-id="ea353-1795">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1795">3</span></span>

<span data-ttu-id="ea353-1796">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1796">4</span></span>

<span data-ttu-id="ea353-1797">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1797">5</span></span>

<span data-ttu-id="ea353-1798">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1798">6</span></span>

<span data-ttu-id="ea353-1799">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1799">7</span></span>

<span data-ttu-id="ea353-1800">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1800">8</span></span>

<span data-ttu-id="ea353-1801">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1801">9</span></span>

<span data-ttu-id="ea353-1802">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1802">1</span></span><br/> <span data-ttu-id="ea353-1803">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1803">0</span></span><br/>

<span data-ttu-id="ea353-1804">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1804">1</span></span>

<span data-ttu-id="ea353-1805">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1805">2</span></span>

<span data-ttu-id="ea353-1806">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1806">3</span></span>

<span data-ttu-id="ea353-1807">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1807">4</span></span>

<span data-ttu-id="ea353-1808">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1808">5</span></span>

<span data-ttu-id="ea353-1809">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1809">6</span></span>

<span data-ttu-id="ea353-1810">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1810">7</span></span>

<span data-ttu-id="ea353-1811">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1811">8</span></span>

<span data-ttu-id="ea353-1812">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1812">9</span></span>

<span data-ttu-id="ea353-1813">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1813">2</span></span><br/> <span data-ttu-id="ea353-1814">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1814">0</span></span><br/>

<span data-ttu-id="ea353-1815">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1815">1</span></span>

<span data-ttu-id="ea353-1816">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1816">2</span></span>

<span data-ttu-id="ea353-1817">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1817">3</span></span>

<span data-ttu-id="ea353-1818">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1818">4</span></span>

<span data-ttu-id="ea353-1819">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1819">5</span></span>

<span data-ttu-id="ea353-1820">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1820">6</span></span>

<span data-ttu-id="ea353-1821">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1821">7</span></span>

<span data-ttu-id="ea353-1822">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1822">8</span></span>

<span data-ttu-id="ea353-1823">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1823">9</span></span>

<span data-ttu-id="ea353-1824">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1824">3</span></span><br/> <span data-ttu-id="ea353-1825">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1825">0</span></span><br/>

<span data-ttu-id="ea353-1826">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1826">1</span></span>

<span data-ttu-id="ea353-1827">\_csColumns (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1827">\_csColumns (variable)</span></span>

<span data-ttu-id="ea353-1828">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="ea353-1828">\_ulCategType</span></span>



 

<span data-ttu-id="ea353-1829">**\_ csColumns:** struttura CColumnSet che indica le colonne in base alle quali raggruppare la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1829">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="ea353-1830">**\_ ulCategType:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-1830">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="ea353-1831">DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-1831">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="ea353-1832">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="ea353-1832">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="ea353-1833">La struttura CDbColId contiene una colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-1833">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="ea353-1834">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1834">0</span></span>

<span data-ttu-id="ea353-1835">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1835">1</span></span>

<span data-ttu-id="ea353-1836">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1836">2</span></span>

<span data-ttu-id="ea353-1837">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1837">3</span></span>

<span data-ttu-id="ea353-1838">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1838">4</span></span>

<span data-ttu-id="ea353-1839">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1839">5</span></span>

<span data-ttu-id="ea353-1840">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1840">6</span></span>

<span data-ttu-id="ea353-1841">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1841">7</span></span>

<span data-ttu-id="ea353-1842">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1842">8</span></span>

<span data-ttu-id="ea353-1843">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1843">9</span></span>

<span data-ttu-id="ea353-1844">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1844">1</span></span><br/> <span data-ttu-id="ea353-1845">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1845">0</span></span><br/>

<span data-ttu-id="ea353-1846">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1846">1</span></span>

<span data-ttu-id="ea353-1847">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1847">2</span></span>

<span data-ttu-id="ea353-1848">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1848">3</span></span>

<span data-ttu-id="ea353-1849">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1849">4</span></span>

<span data-ttu-id="ea353-1850">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1850">5</span></span>

<span data-ttu-id="ea353-1851">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1851">6</span></span>

<span data-ttu-id="ea353-1852">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1852">7</span></span>

<span data-ttu-id="ea353-1853">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1853">8</span></span>

<span data-ttu-id="ea353-1854">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1854">9</span></span>

<span data-ttu-id="ea353-1855">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1855">2</span></span><br/> <span data-ttu-id="ea353-1856">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1856">0</span></span><br/>

<span data-ttu-id="ea353-1857">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1857">1</span></span>

<span data-ttu-id="ea353-1858">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1858">2</span></span>

<span data-ttu-id="ea353-1859">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1859">3</span></span>

<span data-ttu-id="ea353-1860">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1860">4</span></span>

<span data-ttu-id="ea353-1861">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1861">5</span></span>

<span data-ttu-id="ea353-1862">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1862">6</span></span>

<span data-ttu-id="ea353-1863">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1863">7</span></span>

<span data-ttu-id="ea353-1864">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1864">8</span></span>

<span data-ttu-id="ea353-1865">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1865">9</span></span>

<span data-ttu-id="ea353-1866">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1866">3</span></span><br/> <span data-ttu-id="ea353-1867">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1867">0</span></span><br/>

<span data-ttu-id="ea353-1868">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1868">1</span></span>

<span data-ttu-id="ea353-1869">eKind</span><span class="sxs-lookup"><span data-stu-id="ea353-1869">eKind</span></span>

<span data-ttu-id="ea353-1870">GUID</span><span class="sxs-lookup"><span data-stu-id="ea353-1870">GUID</span></span>

<span data-ttu-id="ea353-1871">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1871">...</span></span>

<span data-ttu-id="ea353-1872">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1872">...</span></span>

<span data-ttu-id="ea353-1873">...</span><span class="sxs-lookup"><span data-stu-id="ea353-1873">...</span></span>

<span data-ttu-id="ea353-1874">ulId</span><span class="sxs-lookup"><span data-stu-id="ea353-1874">ulId</span></span>

<span data-ttu-id="ea353-1875">vString (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1875">vString (variable)</span></span>



 

<span data-ttu-id="ea353-1876">**eKind:** DEVE essere impostato su uno dei valori seguenti che indica il contenuto di GUID e vValue.</span><span class="sxs-lookup"><span data-stu-id="ea353-1876">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="ea353-1877">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1877">Value</span></span>                            | <span data-ttu-id="ea353-1878">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1878">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1879">NOME GUID DBKIND \_ \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-1879">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="ea353-1880">vString contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1880">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="ea353-1881">DBKIND \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-1881">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="ea353-1882">ulId contiene un intero a 4 byte che indica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1882">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="ea353-1883">NOME \_ DBKIND PGUID \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-1883">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="ea353-1884">vString contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1884">vString contains a property name.</span></span> <span data-ttu-id="ea353-1885">Questo valore DEVE essere considerato uguale a DBKIND \_ GUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="ea353-1885">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="ea353-1886">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-1886">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="ea353-1887">ulId contiene un intero a 4 byte che indica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1887">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="ea353-1888">Questo valore DEVE corrispondere al \_ \_ PROPID GUID DBKIND.</span><span class="sxs-lookup"><span data-stu-id="ea353-1888">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="ea353-1889">**GUID: GUID** della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1889">**GUID**: The property GUID.</span></span>

<span data-ttu-id="ea353-1890">**ulId:** se eKind è \_ DBKIND GUID PROPID o DBKIND PGUID PROPID, questo campo contiene un intero senza segno, specificando \_ \_ \_ l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1890">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="ea353-1891">Se eKind è DBKIND GUID NAME o DBKIND PGUID NAME, questo campo contiene un intero senza segno che specifica il numero di caratteri Unicode contenuti nel \_ \_ campo \_ \_ vString.</span><span class="sxs-lookup"><span data-stu-id="ea353-1891">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="ea353-1892">**vString:** stringa Unicode senza terminazione Null che rappresenta il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1892">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="ea353-1893">Deve essere omesso a meno che il campo eKind non sia impostato su DBKIND \_ GUID \_ NAME o DBKIND \_ PGUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="ea353-1893">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="ea353-1894">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="ea353-1894">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="ea353-1895">La struttura CDbProp contiene una proprietà .</span><span class="sxs-lookup"><span data-stu-id="ea353-1895">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="ea353-1896">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1896">0</span></span>

<span data-ttu-id="ea353-1897">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1897">1</span></span>

<span data-ttu-id="ea353-1898">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1898">2</span></span>

<span data-ttu-id="ea353-1899">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1899">3</span></span>

<span data-ttu-id="ea353-1900">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1900">4</span></span>

<span data-ttu-id="ea353-1901">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1901">5</span></span>

<span data-ttu-id="ea353-1902">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1902">6</span></span>

<span data-ttu-id="ea353-1903">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1903">7</span></span>

<span data-ttu-id="ea353-1904">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1904">8</span></span>

<span data-ttu-id="ea353-1905">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1905">9</span></span>

<span data-ttu-id="ea353-1906">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1906">1</span></span><br/> <span data-ttu-id="ea353-1907">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1907">0</span></span><br/>

<span data-ttu-id="ea353-1908">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1908">1</span></span>

<span data-ttu-id="ea353-1909">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1909">2</span></span>

<span data-ttu-id="ea353-1910">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1910">3</span></span>

<span data-ttu-id="ea353-1911">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1911">4</span></span>

<span data-ttu-id="ea353-1912">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1912">5</span></span>

<span data-ttu-id="ea353-1913">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1913">6</span></span>

<span data-ttu-id="ea353-1914">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1914">7</span></span>

<span data-ttu-id="ea353-1915">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1915">8</span></span>

<span data-ttu-id="ea353-1916">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1916">9</span></span>

<span data-ttu-id="ea353-1917">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1917">2</span></span><br/> <span data-ttu-id="ea353-1918">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1918">0</span></span><br/>

<span data-ttu-id="ea353-1919">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1919">1</span></span>

<span data-ttu-id="ea353-1920">2</span><span class="sxs-lookup"><span data-stu-id="ea353-1920">2</span></span>

<span data-ttu-id="ea353-1921">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1921">3</span></span>

<span data-ttu-id="ea353-1922">4</span><span class="sxs-lookup"><span data-stu-id="ea353-1922">4</span></span>

<span data-ttu-id="ea353-1923">5</span><span class="sxs-lookup"><span data-stu-id="ea353-1923">5</span></span>

<span data-ttu-id="ea353-1924">6</span><span class="sxs-lookup"><span data-stu-id="ea353-1924">6</span></span>

<span data-ttu-id="ea353-1925">7</span><span class="sxs-lookup"><span data-stu-id="ea353-1925">7</span></span>

<span data-ttu-id="ea353-1926">8</span><span class="sxs-lookup"><span data-stu-id="ea353-1926">8</span></span>

<span data-ttu-id="ea353-1927">9</span><span class="sxs-lookup"><span data-stu-id="ea353-1927">9</span></span>

<span data-ttu-id="ea353-1928">3</span><span class="sxs-lookup"><span data-stu-id="ea353-1928">3</span></span><br/> <span data-ttu-id="ea353-1929">0</span><span class="sxs-lookup"><span data-stu-id="ea353-1929">0</span></span><br/>

<span data-ttu-id="ea353-1930">1</span><span class="sxs-lookup"><span data-stu-id="ea353-1930">1</span></span>

<span data-ttu-id="ea353-1931">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="ea353-1931">DBPROPID</span></span>

<span data-ttu-id="ea353-1932">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="ea353-1932">DBPROPOPTIONS</span></span>

<span data-ttu-id="ea353-1933">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="ea353-1933">DBPROPSTATUS</span></span>

<span data-ttu-id="ea353-1934">colid (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1934">colid (variable)</span></span>

<span data-ttu-id="ea353-1935">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-1935">vValue (variable)</span></span>



 

<span data-ttu-id="ea353-1936">**DBPROPID:** intero senza segno a 32 bit che indica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1936">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="ea353-1937">**DBPROPOPTIONS:** deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-1937">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="ea353-1938">**DBPROPSTATUS:** deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-1938">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="ea353-1939">**colid:** struttura CDbColId, come specificato nella sezione 2.2.1.20, che indica la colonna a cui si applica la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1939">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="ea353-1940">**vValue:** CBaseStorageVariant contenente il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-1940">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="ea353-1941">2.2.1.21.1 Proprietà</span><span class="sxs-lookup"><span data-stu-id="ea353-1941">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="ea353-1942">Questa sezione contiene informazioni dettagliate sulle proprietà usate da CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-1942">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="ea353-1943">Queste proprietà sono raggruppate in tre set di proprietà, ident2.2.1.21.1 nel campo guidPropertySet della struttura CDbPropSet (Sezione 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="ea353-1943">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="ea353-1944">Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà DBPROPSET \_ FSCIFRMWRK \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="ea353-1944">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="ea353-1945">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1945">Value</span></span>                                  | <span data-ttu-id="ea353-1946">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1946">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1947">DBPROP \_ CI CATALOG NAME \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-1947">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="ea353-1948">Specifica il nome del catalogo o dei cataloghi su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1948">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="ea353-1949">Il valore DEVE essere un \_ LPWSTR VT o VT \_ VECTOR \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ea353-1949">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="ea353-1950">DBPROP \_ CI \_ INCLUDE \_ SCOPES 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-1950">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="ea353-1951">Specifica uno o più percorsi da includere nella query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1951">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="ea353-1952">Value MUST be a VT \_ LPWSTR or a VT \_ VECTOR \| VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="ea353-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="ea353-1953">FLAG DI \_ AMBITO CI \_ DBPROP \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-1953">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="ea353-1954">Specifica la modalità di gestione dei percorsi specificati dalla proprietà DBPROP \_ CI \_ INCLUDE \_ SCOPES.</span><span class="sxs-lookup"><span data-stu-id="ea353-1954">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="ea353-1955">Il valore DEVE essere VT \_ I4 o VT \_ VECTOR \| VT \_ I4.</span><span class="sxs-lookup"><span data-stu-id="ea353-1955">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="ea353-1956">TIPO DI \_ QUERY DBPROP CI \_ \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="ea353-1956">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="ea353-1957">Specifica il tipo di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-1957">Specifies the type of query.</span></span> <span data-ttu-id="ea353-1958">CDbColId DEVE essere impostato su DB \_ NULLID.</span><span class="sxs-lookup"><span data-stu-id="ea353-1958">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="ea353-1959">Nella tabella seguente sono elencati i flag per la proprietà DBPROP \_ CI \_ SCOPE \_ FLAGS:</span><span class="sxs-lookup"><span data-stu-id="ea353-1959">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="ea353-1960">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1960">Value</span></span>                     | <span data-ttu-id="ea353-1961">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1961">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1962">QUERY \_ DEEP 0x01</span><span class="sxs-lookup"><span data-stu-id="ea353-1962">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="ea353-1963">Se impostato, indica che i file nella directory dell'ambito e in tutte le sottodirectory vengono inclusi nei risultati.</span><span class="sxs-lookup"><span data-stu-id="ea353-1963">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="ea353-1964">Se deselezionata, nei risultati vengono inclusi solo i file nella directory dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="ea353-1964">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="ea353-1965">NON DEVE essere combinato con QUERY \_ DEEP.</span><span class="sxs-lookup"><span data-stu-id="ea353-1965">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="ea353-1966">ESEGUIRE QUERY \_ \_ SUL PERCORSO VIRTUALE 0x02</span><span class="sxs-lookup"><span data-stu-id="ea353-1966">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="ea353-1967">Se impostato, indica che l'ambito è un percorso virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea353-1967">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="ea353-1968">Se è deselezionata, indica che l'ambito è una directory fisica.</span><span class="sxs-lookup"><span data-stu-id="ea353-1968">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="ea353-1969">Nella tabella seguente sono elencati i tipi di query per la proprietà DBPROP \_ CI \_ QUERY \_ TYPE:</span><span class="sxs-lookup"><span data-stu-id="ea353-1969">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="ea353-1970">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1970">Value</span></span>                     | <span data-ttu-id="ea353-1971">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1971">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1972">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-1972">CiNormal 0x00000000</span></span>       | <span data-ttu-id="ea353-1973">Una query normale.</span><span class="sxs-lookup"><span data-stu-id="ea353-1973">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="ea353-1974">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-1974">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="ea353-1975">La query richiede un elenco delle radici virtuali del catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-1975">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="ea353-1976">Questo valore richiede privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="ea353-1976">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="ea353-1977">Proprietà ci 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-1977">CiProperties 0x00000003</span></span>   | <span data-ttu-id="ea353-1978">La query richiede un elenco di tutte le proprietà supportate dal servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-1978">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="ea353-1979">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-1979">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="ea353-1980">La query è un'operazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="ea353-1980">The query is an administrative operation.</span></span> <span data-ttu-id="ea353-1981">Questo valore richiede privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="ea353-1981">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="ea353-1982">Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà \_ DBPROPSET QUERYEXT.</span><span class="sxs-lookup"><span data-stu-id="ea353-1982">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="ea353-1983">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-1983">Value</span></span>                                      | <span data-ttu-id="ea353-1984">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-1984">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-1985">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-1985">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="ea353-1986">Specifica il modo in cui il servizio di indicizzazione deve gestire le query lente.</span><span class="sxs-lookup"><span data-stu-id="ea353-1986">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="ea353-1987">Il valore DEVE essere un valore \_ BOOL VT.</span><span class="sxs-lookup"><span data-stu-id="ea353-1987">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="ea353-1988">Se TRUE, al server è consentito eseguire queste query in modo non riuscito.</span><span class="sxs-lookup"><span data-stu-id="ea353-1988">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="ea353-1989">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-1989">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="ea353-1990">Indica se il servizio di indicizzazione deve eseguire l'operazione di taglio dei risultati.</span><span class="sxs-lookup"><span data-stu-id="ea353-1990">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="ea353-1991">Se TRUE, il server deve prendere in considerazione l'esecuzione del trimming dei risultati in modo da ottimizzare il tempo di risposta al client.</span><span class="sxs-lookup"><span data-stu-id="ea353-1991">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="ea353-1992">Il valore DEVE essere un valore \_ BOOL VT.</span><span class="sxs-lookup"><span data-stu-id="ea353-1992">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="ea353-1993">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-1993">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="ea353-1994">Indica se il client supporta i tipi di dati \_ VECTOR VT.</span><span class="sxs-lookup"><span data-stu-id="ea353-1994">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="ea353-1995">Se TRUE, il client supporta VT VECTOR; se FALSE, il server deve convertire i tipi di dati \_ \_ VT VECTOR in tipi di dati VT \_ ARRAY.</span><span class="sxs-lookup"><span data-stu-id="ea353-1995">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="ea353-1996">Il valore DEVE essere un valore \_ BOOL VT.</span><span class="sxs-lookup"><span data-stu-id="ea353-1996">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="ea353-1997">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="ea353-1997">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="ea353-1998">Indica le corrispondenze di riga da restituire.</span><span class="sxs-lookup"><span data-stu-id="ea353-1998">Indicates the row matches to return.</span></span> <span data-ttu-id="ea353-1999">Se TRUE, il server deve restituire il primo set di righe corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-1999">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="ea353-2000">Se FALSE, devono essere restituite le righe corrispondenti migliori.</span><span class="sxs-lookup"><span data-stu-id="ea353-2000">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="ea353-2001">Il valore DEVE essere un valore \_ BOOL VT.</span><span class="sxs-lookup"><span data-stu-id="ea353-2001">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="ea353-2002">Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà DBPROPSET \_ CIFRMWRKCORE \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="ea353-2002">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="ea353-2003">Value/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="ea353-2003">Value / DBPROPID</span></span>                 | <span data-ttu-id="ea353-2004">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-2004">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-2005">DBPROP \_ MACHINE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-2005">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="ea353-2006">Specifica i nomi dei computer in cui deve essere elaborata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2006">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="ea353-2007">Il valore DEVE essere VT \_ BSTR o VT \_ ARRAY \| VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="ea353-2007">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="ea353-2008">DBPROP \_ CLIENT \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-2008">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="ea353-2009">Specifica una costante di connessione per il servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2009">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="ea353-2010">Il valore DEVE essere un CLSID VT \_ contenente 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="ea353-2010">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="ea353-2011">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="ea353-2011">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="ea353-2012">La struttura CDbPropSet contiene un set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-2012">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="ea353-2013">Si noti che il primo campo ha dimensioni fisse, ma potrebbe non essere allineato a un offset che rappresenta un multiplo a 4 byte dall'inizio del messaggio contenente questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ea353-2013">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="ea353-2014">Tuttavia, il campo cProperties è allineato come tale e di conseguenza il formato è illustrato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-2014">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="ea353-2015">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2015">0</span></span>

<span data-ttu-id="ea353-2016">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2016">1</span></span>

<span data-ttu-id="ea353-2017">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2017">2</span></span>

<span data-ttu-id="ea353-2018">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2018">3</span></span>

<span data-ttu-id="ea353-2019">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2019">4</span></span>

<span data-ttu-id="ea353-2020">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2020">5</span></span>

<span data-ttu-id="ea353-2021">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2021">6</span></span>

<span data-ttu-id="ea353-2022">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2022">7</span></span>

<span data-ttu-id="ea353-2023">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2023">8</span></span>

<span data-ttu-id="ea353-2024">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2024">9</span></span>

<span data-ttu-id="ea353-2025">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2025">1</span></span><br/> <span data-ttu-id="ea353-2026">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2026">0</span></span><br/>

<span data-ttu-id="ea353-2027">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2027">1</span></span>

<span data-ttu-id="ea353-2028">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2028">2</span></span>

<span data-ttu-id="ea353-2029">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2029">3</span></span>

<span data-ttu-id="ea353-2030">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2030">4</span></span>

<span data-ttu-id="ea353-2031">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2031">5</span></span>

<span data-ttu-id="ea353-2032">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2032">6</span></span>

<span data-ttu-id="ea353-2033">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2033">7</span></span>

<span data-ttu-id="ea353-2034">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2034">8</span></span>

<span data-ttu-id="ea353-2035">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2035">9</span></span>

<span data-ttu-id="ea353-2036">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2036">2</span></span><br/> <span data-ttu-id="ea353-2037">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2037">0</span></span><br/>

<span data-ttu-id="ea353-2038">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2038">1</span></span>

<span data-ttu-id="ea353-2039">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2039">2</span></span>

<span data-ttu-id="ea353-2040">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2040">3</span></span>

<span data-ttu-id="ea353-2041">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2041">4</span></span>

<span data-ttu-id="ea353-2042">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2042">5</span></span>

<span data-ttu-id="ea353-2043">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2043">6</span></span>

<span data-ttu-id="ea353-2044">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2044">7</span></span>

<span data-ttu-id="ea353-2045">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2045">8</span></span>

<span data-ttu-id="ea353-2046">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2046">9</span></span>

<span data-ttu-id="ea353-2047">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2047">3</span></span><br/> <span data-ttu-id="ea353-2048">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2048">0</span></span><br/>

<span data-ttu-id="ea353-2049">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2049">1</span></span>

<span data-ttu-id="ea353-2050">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="ea353-2050">guidPropertySet</span></span>

<span data-ttu-id="ea353-2051">...</span><span class="sxs-lookup"><span data-stu-id="ea353-2051">...</span></span>

<span data-ttu-id="ea353-2052">...</span><span class="sxs-lookup"><span data-stu-id="ea353-2052">...</span></span>

<span data-ttu-id="ea353-2053">...</span><span class="sxs-lookup"><span data-stu-id="ea353-2053">...</span></span>

<span data-ttu-id="ea353-2054">...</span><span class="sxs-lookup"><span data-stu-id="ea353-2054">...</span></span>

<span data-ttu-id="ea353-2055">\_padding (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-2055">\_padding (variable)</span></span>

<span data-ttu-id="ea353-2056">cProperties</span><span class="sxs-lookup"><span data-stu-id="ea353-2056">cProperties</span></span>

<span data-ttu-id="ea353-2057">aProps (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-2057">aProps (variable)</span></span>



 

<span data-ttu-id="ea353-2058">**guidPropertySet:** GUID che identifica il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-2058">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="ea353-2059">DEVE essere impostato sul formato binario corrispondente a uno dei valori seguenti (visualizzati nella rappresentazione di stringa), identificando il set di proprietà delle proprietà contenute nel campo aProps.</span><span class="sxs-lookup"><span data-stu-id="ea353-2059">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="ea353-2060">Valore/GUID</span><span class="sxs-lookup"><span data-stu-id="ea353-2060">Value / GUID</span></span>                                                                              | <span data-ttu-id="ea353-2061">Nome</span><span class="sxs-lookup"><span data-stu-id="ea353-2061">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="ea353-2062">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="ea353-2062">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="ea353-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="ea353-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="ea353-2064">Set di proprietà del framework dell'indice di contenuto del file system</span><span class="sxs-lookup"><span data-stu-id="ea353-2064">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="ea353-2065">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="ea353-2065">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="ea353-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="ea353-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="ea353-2067">Set di proprietà dell'estensione query</span><span class="sxs-lookup"><span data-stu-id="ea353-2067">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="ea353-2068">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="ea353-2068">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="ea353-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="ea353-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="ea353-2070">Set di proprietà core di Content Index Framework</span><span class="sxs-lookup"><span data-stu-id="ea353-2070">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="ea353-2071">**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-2071">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="ea353-2072">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset pari a un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ea353-2072">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="ea353-2073">Se questo campo è presente (ad esempio lunghezza diversa da zero), il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-2073">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="ea353-2074">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-2074">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-2075">**cProperties:** intero senza segno a 32 bit contenente il numero di elementi nella matrice aProps.</span><span class="sxs-lookup"><span data-stu-id="ea353-2075">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="ea353-2076">**aProps:** matrice di strutture CDbProp, come specificato nella sezione 0, contenente le proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-2076">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="ea353-2077">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice.</span><span class="sxs-lookup"><span data-stu-id="ea353-2077">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="ea353-2078">Se sono presenti byte di spaziatura interna, il valore che contengono è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-2078">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="ea353-2079">Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-2079">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="ea353-2080">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="ea353-2080">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="ea353-2081">La struttura CPidMapper contiene una matrice di ID di proprietà che specificano le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-2081">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="ea353-2082">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2082">0</span></span>

<span data-ttu-id="ea353-2083">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2083">1</span></span>

<span data-ttu-id="ea353-2084">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2084">2</span></span>

<span data-ttu-id="ea353-2085">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2085">3</span></span>

<span data-ttu-id="ea353-2086">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2086">4</span></span>

<span data-ttu-id="ea353-2087">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2087">5</span></span>

<span data-ttu-id="ea353-2088">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2088">6</span></span>

<span data-ttu-id="ea353-2089">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2089">7</span></span>

<span data-ttu-id="ea353-2090">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2090">8</span></span>

<span data-ttu-id="ea353-2091">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2091">9</span></span>

<span data-ttu-id="ea353-2092">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2092">1</span></span><br/> <span data-ttu-id="ea353-2093">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2093">0</span></span><br/>

<span data-ttu-id="ea353-2094">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2094">1</span></span>

<span data-ttu-id="ea353-2095">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2095">2</span></span>

<span data-ttu-id="ea353-2096">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2096">3</span></span>

<span data-ttu-id="ea353-2097">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2097">4</span></span>

<span data-ttu-id="ea353-2098">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2098">5</span></span>

<span data-ttu-id="ea353-2099">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2099">6</span></span>

<span data-ttu-id="ea353-2100">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2100">7</span></span>

<span data-ttu-id="ea353-2101">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2101">8</span></span>

<span data-ttu-id="ea353-2102">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2102">9</span></span>

<span data-ttu-id="ea353-2103">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2103">2</span></span><br/> <span data-ttu-id="ea353-2104">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2104">0</span></span><br/>

<span data-ttu-id="ea353-2105">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2105">1</span></span>

<span data-ttu-id="ea353-2106">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2106">2</span></span>

<span data-ttu-id="ea353-2107">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2107">3</span></span>

<span data-ttu-id="ea353-2108">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2108">4</span></span>

<span data-ttu-id="ea353-2109">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2109">5</span></span>

<span data-ttu-id="ea353-2110">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2110">6</span></span>

<span data-ttu-id="ea353-2111">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2111">7</span></span>

<span data-ttu-id="ea353-2112">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2112">8</span></span>

<span data-ttu-id="ea353-2113">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2113">9</span></span>

<span data-ttu-id="ea353-2114">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2114">3</span></span><br/> <span data-ttu-id="ea353-2115">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2115">0</span></span><br/>

<span data-ttu-id="ea353-2116">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2116">1</span></span>

<span data-ttu-id="ea353-2117">count</span><span class="sxs-lookup"><span data-stu-id="ea353-2117">count</span></span>

<span data-ttu-id="ea353-2118">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="ea353-2118">aPropSpec</span></span>

<span data-ttu-id="ea353-2119">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-2119">... (variable)</span></span>



 

<span data-ttu-id="ea353-2120">**count:** intero senza segno a 32 bit contenente il numero di elementi nella matrice aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="ea353-2120">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="ea353-2121">**aPropSpec:** matrice di strutture CFullPropSpec che indica le proprietà da restituire.</span><span class="sxs-lookup"><span data-stu-id="ea353-2121">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="ea353-2122">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura abbia un allineamento a 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2122">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="ea353-2123">Tali byte di spaziatura interna possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2123">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="ea353-2124">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="ea353-2124">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="ea353-2125">La struttura CRowSeekAt contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-2125">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="ea353-2126">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2126">0</span></span>

<span data-ttu-id="ea353-2127">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2127">1</span></span>

<span data-ttu-id="ea353-2128">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2128">2</span></span>

<span data-ttu-id="ea353-2129">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2129">3</span></span>

<span data-ttu-id="ea353-2130">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2130">4</span></span>

<span data-ttu-id="ea353-2131">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2131">5</span></span>

<span data-ttu-id="ea353-2132">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2132">6</span></span>

<span data-ttu-id="ea353-2133">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2133">7</span></span>

<span data-ttu-id="ea353-2134">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2134">8</span></span>

<span data-ttu-id="ea353-2135">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2135">9</span></span>

<span data-ttu-id="ea353-2136">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2136">1</span></span><br/> <span data-ttu-id="ea353-2137">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2137">0</span></span><br/>

<span data-ttu-id="ea353-2138">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2138">1</span></span>

<span data-ttu-id="ea353-2139">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2139">2</span></span>

<span data-ttu-id="ea353-2140">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2140">3</span></span>

<span data-ttu-id="ea353-2141">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2141">4</span></span>

<span data-ttu-id="ea353-2142">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2142">5</span></span>

<span data-ttu-id="ea353-2143">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2143">6</span></span>

<span data-ttu-id="ea353-2144">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2144">7</span></span>

<span data-ttu-id="ea353-2145">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2145">8</span></span>

<span data-ttu-id="ea353-2146">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2146">9</span></span>

<span data-ttu-id="ea353-2147">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2147">2</span></span><br/> <span data-ttu-id="ea353-2148">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2148">0</span></span><br/>

<span data-ttu-id="ea353-2149">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2149">1</span></span>

<span data-ttu-id="ea353-2150">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2150">2</span></span>

<span data-ttu-id="ea353-2151">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2151">3</span></span>

<span data-ttu-id="ea353-2152">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2152">4</span></span>

<span data-ttu-id="ea353-2153">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2153">5</span></span>

<span data-ttu-id="ea353-2154">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2154">6</span></span>

<span data-ttu-id="ea353-2155">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2155">7</span></span>

<span data-ttu-id="ea353-2156">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2156">8</span></span>

<span data-ttu-id="ea353-2157">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2157">9</span></span>

<span data-ttu-id="ea353-2158">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2158">3</span></span><br/> <span data-ttu-id="ea353-2159">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2159">0</span></span><br/>

<span data-ttu-id="ea353-2160">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2160">1</span></span>

<span data-ttu-id="ea353-2161">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="ea353-2161">\_hRegion</span></span>

<span data-ttu-id="ea353-2162">\_cskip</span><span class="sxs-lookup"><span data-stu-id="ea353-2162">\_cskip</span></span>

<span data-ttu-id="ea353-2163">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="ea353-2163">\_bmkOffset</span></span>



 

<span data-ttu-id="ea353-2164">**\_ hRegion:** DEVE essere impostato su 0x00000000 e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2164">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="ea353-2165">**\_ cskip:** intero senza segno a 32 bit contenente il numero di righe da ignorare nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-2165">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="ea353-2166">**\_ bmkOffset:** valore a 32 bit che  rappresenta l'handle del segnalibro che indica la posizione iniziale da cui ignorare il numero di righe specificato in cskip, prima di iniziare il \_ recupero.</span><span class="sxs-lookup"><span data-stu-id="ea353-2166">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="ea353-2167">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="ea353-2167">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="ea353-2168">La struttura CRowSeekAtRatio identifica il punto in cui iniziare il recupero per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-2168">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="ea353-2169">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2169">0</span></span>

<span data-ttu-id="ea353-2170">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2170">1</span></span>

<span data-ttu-id="ea353-2171">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2171">2</span></span>

<span data-ttu-id="ea353-2172">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2172">3</span></span>

<span data-ttu-id="ea353-2173">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2173">4</span></span>

<span data-ttu-id="ea353-2174">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2174">5</span></span>

<span data-ttu-id="ea353-2175">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2175">6</span></span>

<span data-ttu-id="ea353-2176">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2176">7</span></span>

<span data-ttu-id="ea353-2177">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2177">8</span></span>

<span data-ttu-id="ea353-2178">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2178">9</span></span>

<span data-ttu-id="ea353-2179">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2179">1</span></span><br/> <span data-ttu-id="ea353-2180">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2180">0</span></span><br/>

<span data-ttu-id="ea353-2181">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2181">1</span></span>

<span data-ttu-id="ea353-2182">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2182">2</span></span>

<span data-ttu-id="ea353-2183">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2183">3</span></span>

<span data-ttu-id="ea353-2184">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2184">4</span></span>

<span data-ttu-id="ea353-2185">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2185">5</span></span>

<span data-ttu-id="ea353-2186">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2186">6</span></span>

<span data-ttu-id="ea353-2187">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2187">7</span></span>

<span data-ttu-id="ea353-2188">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2188">8</span></span>

<span data-ttu-id="ea353-2189">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2189">9</span></span>

<span data-ttu-id="ea353-2190">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2190">2</span></span><br/> <span data-ttu-id="ea353-2191">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2191">0</span></span><br/>

<span data-ttu-id="ea353-2192">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2192">1</span></span>

<span data-ttu-id="ea353-2193">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2193">2</span></span>

<span data-ttu-id="ea353-2194">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2194">3</span></span>

<span data-ttu-id="ea353-2195">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2195">4</span></span>

<span data-ttu-id="ea353-2196">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2196">5</span></span>

<span data-ttu-id="ea353-2197">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2197">6</span></span>

<span data-ttu-id="ea353-2198">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2198">7</span></span>

<span data-ttu-id="ea353-2199">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2199">8</span></span>

<span data-ttu-id="ea353-2200">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2200">9</span></span>

<span data-ttu-id="ea353-2201">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2201">3</span></span><br/> <span data-ttu-id="ea353-2202">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2202">0</span></span><br/>

<span data-ttu-id="ea353-2203">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2203">1</span></span>

<span data-ttu-id="ea353-2204">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="ea353-2204">CiTblChapt</span></span>

<span data-ttu-id="ea353-2205">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="ea353-2205">\_hRegion</span></span>

<span data-ttu-id="ea353-2206">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="ea353-2206">\_ulNumerator</span></span>

<span data-ttu-id="ea353-2207">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="ea353-2207">\_ulDenominator</span></span>



 

<span data-ttu-id="ea353-2208">**CiTblChapt:** intero senza segno a 32 bit che indica il capitolo del set di righe da cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-2208">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="ea353-2209">**\_ hRegion:** DEVE essere impostato su 0x00000000 e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2209">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="ea353-2210">**\_ ulNumerator:** intero senza segno a 32 bit che rappresenta il numeratore del rapporto tra le righe del capitolo da cui iniziare il recupero.</span><span class="sxs-lookup"><span data-stu-id="ea353-2210">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="ea353-2211">**\_ ulDenominator:** intero senza segno a 32 bit che rappresenta il denominatore del rapporto tra le righe del capitolo da cui iniziare il recupero.</span><span class="sxs-lookup"><span data-stu-id="ea353-2211">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="ea353-2212">DEVE essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="ea353-2212">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="ea353-2213">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="ea353-2213">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="ea353-2214">La struttura CRowSeekByBookmark identifica i segnalibri da cui iniziare a recuperare le righe per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-2214">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="ea353-2215">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2215">0</span></span>

<span data-ttu-id="ea353-2216">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2216">1</span></span>

<span data-ttu-id="ea353-2217">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2217">2</span></span>

<span data-ttu-id="ea353-2218">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2218">3</span></span>

<span data-ttu-id="ea353-2219">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2219">4</span></span>

<span data-ttu-id="ea353-2220">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2220">5</span></span>

<span data-ttu-id="ea353-2221">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2221">6</span></span>

<span data-ttu-id="ea353-2222">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2222">7</span></span>

<span data-ttu-id="ea353-2223">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2223">8</span></span>

<span data-ttu-id="ea353-2224">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2224">9</span></span>

<span data-ttu-id="ea353-2225">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2225">1</span></span><br/> <span data-ttu-id="ea353-2226">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2226">0</span></span><br/>

<span data-ttu-id="ea353-2227">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2227">1</span></span>

<span data-ttu-id="ea353-2228">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2228">2</span></span>

<span data-ttu-id="ea353-2229">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2229">3</span></span>

<span data-ttu-id="ea353-2230">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2230">4</span></span>

<span data-ttu-id="ea353-2231">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2231">5</span></span>

<span data-ttu-id="ea353-2232">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2232">6</span></span>

<span data-ttu-id="ea353-2233">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2233">7</span></span>

<span data-ttu-id="ea353-2234">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2234">8</span></span>

<span data-ttu-id="ea353-2235">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2235">9</span></span>

<span data-ttu-id="ea353-2236">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2236">2</span></span><br/> <span data-ttu-id="ea353-2237">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2237">0</span></span><br/>

<span data-ttu-id="ea353-2238">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2238">1</span></span>

<span data-ttu-id="ea353-2239">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2239">2</span></span>

<span data-ttu-id="ea353-2240">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2240">3</span></span>

<span data-ttu-id="ea353-2241">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2241">4</span></span>

<span data-ttu-id="ea353-2242">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2242">5</span></span>

<span data-ttu-id="ea353-2243">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2243">6</span></span>

<span data-ttu-id="ea353-2244">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2244">7</span></span>

<span data-ttu-id="ea353-2245">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2245">8</span></span>

<span data-ttu-id="ea353-2246">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2246">9</span></span>

<span data-ttu-id="ea353-2247">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2247">3</span></span><br/> <span data-ttu-id="ea353-2248">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2248">0</span></span><br/>

<span data-ttu-id="ea353-2249">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2249">1</span></span>

<span data-ttu-id="ea353-2250">\_area hRegion</span><span class="sxs-lookup"><span data-stu-id="ea353-2250">\_hRegion</span></span>

<span data-ttu-id="ea353-2251">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="ea353-2251">\_cBookmarks</span></span>

<span data-ttu-id="ea353-2252">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="ea353-2252">\_maxRet</span></span>

<span data-ttu-id="ea353-2253">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="ea353-2253">\_cValidRet</span></span>

<span data-ttu-id="ea353-2254">\_aBookmarks (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-2254">\_aBookmarks (variable)</span></span>

<span data-ttu-id="ea353-2255">\_ascRet (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-2255">\_ascRet (variable)</span></span>



 

<span data-ttu-id="ea353-2256">**\_ hRegion:** deve essere impostato su 0x00000000 e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2256">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="ea353-2257">**\_ cBookmarks:** intero senza segno a 32 bit che rappresenta il numero di elementi in \_ una matriceBookmarks.</span><span class="sxs-lookup"><span data-stu-id="ea353-2257">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="ea353-2258">**\_ maxRet:** intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice ascRet.</span><span class="sxs-lookup"><span data-stu-id="ea353-2258">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="ea353-2259">**\_ cValidRet:** intero senza segno a 32 bit che rappresenta il numero di elementi validi nella \_ matrice ascRet.</span><span class="sxs-lookup"><span data-stu-id="ea353-2259">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="ea353-2260">Gli elementi validi sono stati definiti nella matrice, mentre gli elementi non validi non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="ea353-2260">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="ea353-2261">**\_ aBookmarks:** matrice di handle di segnalibro (ognuno rappresentato da 4 byte), ottenuto da un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-2261">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="ea353-2262">**\_ ascRet:** matrice di valori HRESULT.</span><span class="sxs-lookup"><span data-stu-id="ea353-2262">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="ea353-2263">Quando CRowSeekByBookMark viene inviato come parte della richiesta CPMGetRowsIn, il numero di voci nella matrice DEVE essere uguale a \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="ea353-2263">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="ea353-2264">Quando vengono inviati dal client, i valori DEVONO essere impostati su zero e il server DEVE ignorare il contenuto della matrice.</span><span class="sxs-lookup"><span data-stu-id="ea353-2264">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="ea353-2265">Quando vengono inviati dal server (come parte del messaggio CPMGetRowsOut), i valori nella matrice indicano lo stato del risultato per ogni recupero di riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-2265">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="ea353-2266">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="ea353-2266">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="ea353-2267">La struttura CRowSeekNext contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-2267">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="ea353-2268">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2268">0</span></span>

<span data-ttu-id="ea353-2269">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2269">1</span></span>

<span data-ttu-id="ea353-2270">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2270">2</span></span>

<span data-ttu-id="ea353-2271">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2271">3</span></span>

<span data-ttu-id="ea353-2272">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2272">4</span></span>

<span data-ttu-id="ea353-2273">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2273">5</span></span>

<span data-ttu-id="ea353-2274">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2274">6</span></span>

<span data-ttu-id="ea353-2275">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2275">7</span></span>

<span data-ttu-id="ea353-2276">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2276">8</span></span>

<span data-ttu-id="ea353-2277">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2277">9</span></span>

<span data-ttu-id="ea353-2278">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2278">1</span></span><br/> <span data-ttu-id="ea353-2279">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2279">0</span></span><br/>

<span data-ttu-id="ea353-2280">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2280">1</span></span>

<span data-ttu-id="ea353-2281">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2281">2</span></span>

<span data-ttu-id="ea353-2282">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2282">3</span></span>

<span data-ttu-id="ea353-2283">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2283">4</span></span>

<span data-ttu-id="ea353-2284">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2284">5</span></span>

<span data-ttu-id="ea353-2285">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2285">6</span></span>

<span data-ttu-id="ea353-2286">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2286">7</span></span>

<span data-ttu-id="ea353-2287">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2287">8</span></span>

<span data-ttu-id="ea353-2288">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2288">9</span></span>

<span data-ttu-id="ea353-2289">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2289">2</span></span><br/> <span data-ttu-id="ea353-2290">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2290">0</span></span><br/>

<span data-ttu-id="ea353-2291">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2291">1</span></span>

<span data-ttu-id="ea353-2292">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2292">2</span></span>

<span data-ttu-id="ea353-2293">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2293">3</span></span>

<span data-ttu-id="ea353-2294">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2294">4</span></span>

<span data-ttu-id="ea353-2295">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2295">5</span></span>

<span data-ttu-id="ea353-2296">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2296">6</span></span>

<span data-ttu-id="ea353-2297">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2297">7</span></span>

<span data-ttu-id="ea353-2298">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2298">8</span></span>

<span data-ttu-id="ea353-2299">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2299">9</span></span>

<span data-ttu-id="ea353-2300">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2300">3</span></span><br/> <span data-ttu-id="ea353-2301">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2301">0</span></span><br/>

<span data-ttu-id="ea353-2302">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2302">1</span></span>

<span data-ttu-id="ea353-2303">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="ea353-2303">CiTblChapt</span></span>

<span data-ttu-id="ea353-2304">\_area hRegion</span><span class="sxs-lookup"><span data-stu-id="ea353-2304">\_hRegion</span></span>

<span data-ttu-id="ea353-2305">\_cskip</span><span class="sxs-lookup"><span data-stu-id="ea353-2305">\_cskip</span></span>



 

<span data-ttu-id="ea353-2306">**CiTblChapt:** intero senza segno a 32 bit che specifica il capitolo del set di righe da cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-2306">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="ea353-2307">**\_ hRegion:** deve essere impostato su 0x00000000 e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2307">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="ea353-2308">**\_ cskip:** intero senza segno a 32 bit che rappresenta il numero di righe da ignorare nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-2308">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="ea353-2309">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="ea353-2309">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="ea353-2310">La struttura CRowsetProperties contiene informazioni di configurazione per una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2310">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="ea353-2311">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2311">0</span></span>

<span data-ttu-id="ea353-2312">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2312">1</span></span>

<span data-ttu-id="ea353-2313">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2313">2</span></span>

<span data-ttu-id="ea353-2314">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2314">3</span></span>

<span data-ttu-id="ea353-2315">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2315">4</span></span>

<span data-ttu-id="ea353-2316">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2316">5</span></span>

<span data-ttu-id="ea353-2317">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2317">6</span></span>

<span data-ttu-id="ea353-2318">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2318">7</span></span>

<span data-ttu-id="ea353-2319">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2319">8</span></span>

<span data-ttu-id="ea353-2320">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2320">9</span></span>

<span data-ttu-id="ea353-2321">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2321">1</span></span><br/> <span data-ttu-id="ea353-2322">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2322">0</span></span><br/>

<span data-ttu-id="ea353-2323">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2323">1</span></span>

<span data-ttu-id="ea353-2324">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2324">2</span></span>

<span data-ttu-id="ea353-2325">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2325">3</span></span>

<span data-ttu-id="ea353-2326">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2326">4</span></span>

<span data-ttu-id="ea353-2327">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2327">5</span></span>

<span data-ttu-id="ea353-2328">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2328">6</span></span>

<span data-ttu-id="ea353-2329">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2329">7</span></span>

<span data-ttu-id="ea353-2330">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2330">8</span></span>

<span data-ttu-id="ea353-2331">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2331">9</span></span>

<span data-ttu-id="ea353-2332">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2332">2</span></span><br/> <span data-ttu-id="ea353-2333">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2333">0</span></span><br/>

<span data-ttu-id="ea353-2334">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2334">1</span></span>

<span data-ttu-id="ea353-2335">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2335">2</span></span>

<span data-ttu-id="ea353-2336">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2336">3</span></span>

<span data-ttu-id="ea353-2337">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2337">4</span></span>

<span data-ttu-id="ea353-2338">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2338">5</span></span>

<span data-ttu-id="ea353-2339">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2339">6</span></span>

<span data-ttu-id="ea353-2340">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2340">7</span></span>

<span data-ttu-id="ea353-2341">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2341">8</span></span>

<span data-ttu-id="ea353-2342">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2342">9</span></span>

<span data-ttu-id="ea353-2343">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2343">3</span></span><br/> <span data-ttu-id="ea353-2344">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2344">0</span></span><br/>

<span data-ttu-id="ea353-2345">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2345">1</span></span>

<span data-ttu-id="ea353-2346">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="ea353-2346">\_uBooleanOptions</span></span>

<span data-ttu-id="ea353-2347">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="ea353-2347">\_ulMaxOpenRows</span></span>

<span data-ttu-id="ea353-2348">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="ea353-2348">\_ulMemoryUsage</span></span>

<span data-ttu-id="ea353-2349">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="ea353-2349">\_cMaxResults</span></span>

<span data-ttu-id="ea353-2350">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="ea353-2350">\_cCmdTimeout</span></span>



 

<span data-ttu-id="ea353-2351">**\_ uBooleanOptions:** i 3 bit meno significativi di questo campo DEVONO contenere uno dei tre valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-2351">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="ea353-2352">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-2352">Value</span></span>                  | <span data-ttu-id="ea353-2353">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-2353">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ea353-2354">ESequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-2354">eSequential 0x00000001</span></span> | <span data-ttu-id="ea353-2355">Il cursore può essere spostato solo in avanti.</span><span class="sxs-lookup"><span data-stu-id="ea353-2355">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="ea353-2356">ELocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-2356">eLocatable 0x00000003</span></span>  | <span data-ttu-id="ea353-2357">Il cursore può essere spostato in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2357">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="ea353-2358">EScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="ea353-2358">eScrollable 0x00000007</span></span> | <span data-ttu-id="ea353-2359">Il cursore può essere spostato in qualsiasi posizione e recuperato in qualsiasi direzione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2359">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="ea353-2360">I bit rimanenti possono essere chiari o impostati su qualsiasi combinazione dei valori seguenti logicamente or'd insieme:</span><span class="sxs-lookup"><span data-stu-id="ea353-2360">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="ea353-2361">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-2361">Value</span></span>                     | <span data-ttu-id="ea353-2362">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-2362">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-2363">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea353-2363">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="ea353-2364">Il client non attenderà il completamento dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2364">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="ea353-2365">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="ea353-2365">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="ea353-2366">Restituisce le prime righe incontrate, non le corrispondenze migliori.</span><span class="sxs-lookup"><span data-stu-id="ea353-2366">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="ea353-2367">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="ea353-2367">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="ea353-2368">Il server NON DEVE eliminare le righe fino a quando il client non viene eseguito con una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2368">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="ea353-2369">EChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="ea353-2369">eChaptered 0x00000800</span></span>     | <span data-ttu-id="ea353-2370">Il set di righe supporta i capitoli.</span><span class="sxs-lookup"><span data-stu-id="ea353-2370">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="ea353-2371">EUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="ea353-2371">eUseCI 0x00001000</span></span>         | <span data-ttu-id="ea353-2372">Rispondere solo alla query dall'indice, non dal file system.</span><span class="sxs-lookup"><span data-stu-id="ea353-2372">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="ea353-2373">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="ea353-2373">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="ea353-2374">Il servizio di indicizzazione deve prendere in considerazione l'ottimizzazione del tempo di risposta al client durante l'esecuzione della rimozione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="ea353-2374">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="ea353-2375">**\_ ulMaxOpenRows:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-2375">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="ea353-2376">Deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-2376">Must be set to 0x00000000.</span></span> <span data-ttu-id="ea353-2377">Non usato e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2377">Not used and MUST be ignored.</span></span>

<span data-ttu-id="ea353-2378">**\_ ulMemoryUsage:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-2378">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="ea353-2379">Deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="ea353-2380">Non usato e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="ea353-2381">**\_ cMaxResults:** intero senza segno a 32 bit che specifica il numero massimo di righe da restituire per la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2381">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="ea353-2382">**\_ cCmdTimeout:** intero senza segno a 32 bit che specifica il numero di secondi in cui una query deve timeout e terminare automaticamente, contando dal momento in cui la query inizia l'esecuzione nel server.</span><span class="sxs-lookup"><span data-stu-id="ea353-2382">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="ea353-2383">Il valore 0x00000000 indica che la query non deve avere un timeout.</span><span class="sxs-lookup"><span data-stu-id="ea353-2383">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="ea353-2384">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="ea353-2384">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="ea353-2385">La struttura CRowVariant contiene la parte a dimensione fissa di un tipo di dati a lunghezza variabile archiviata nel messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-2385">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="ea353-2386">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2386">0</span></span>

<span data-ttu-id="ea353-2387">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2387">1</span></span>

<span data-ttu-id="ea353-2388">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2388">2</span></span>

<span data-ttu-id="ea353-2389">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2389">3</span></span>

<span data-ttu-id="ea353-2390">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2390">4</span></span>

<span data-ttu-id="ea353-2391">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2391">5</span></span>

<span data-ttu-id="ea353-2392">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2392">6</span></span>

<span data-ttu-id="ea353-2393">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2393">7</span></span>

<span data-ttu-id="ea353-2394">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2394">8</span></span>

<span data-ttu-id="ea353-2395">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2395">9</span></span>

<span data-ttu-id="ea353-2396">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2396">1</span></span><br/> <span data-ttu-id="ea353-2397">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2397">0</span></span><br/>

<span data-ttu-id="ea353-2398">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2398">1</span></span>

<span data-ttu-id="ea353-2399">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2399">2</span></span>

<span data-ttu-id="ea353-2400">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2400">3</span></span>

<span data-ttu-id="ea353-2401">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2401">4</span></span>

<span data-ttu-id="ea353-2402">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2402">5</span></span>

<span data-ttu-id="ea353-2403">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2403">6</span></span>

<span data-ttu-id="ea353-2404">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2404">7</span></span>

<span data-ttu-id="ea353-2405">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2405">8</span></span>

<span data-ttu-id="ea353-2406">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2406">9</span></span>

<span data-ttu-id="ea353-2407">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2407">2</span></span><br/> <span data-ttu-id="ea353-2408">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2408">0</span></span><br/>

<span data-ttu-id="ea353-2409">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2409">1</span></span>

<span data-ttu-id="ea353-2410">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2410">2</span></span>

<span data-ttu-id="ea353-2411">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2411">3</span></span>

<span data-ttu-id="ea353-2412">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2412">4</span></span>

<span data-ttu-id="ea353-2413">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2413">5</span></span>

<span data-ttu-id="ea353-2414">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2414">6</span></span>

<span data-ttu-id="ea353-2415">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2415">7</span></span>

<span data-ttu-id="ea353-2416">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2416">8</span></span>

<span data-ttu-id="ea353-2417">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2417">9</span></span>

<span data-ttu-id="ea353-2418">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2418">3</span></span><br/> <span data-ttu-id="ea353-2419">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2419">0</span></span><br/>

<span data-ttu-id="ea353-2420">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2420">1</span></span>

<span data-ttu-id="ea353-2421">vType</span><span class="sxs-lookup"><span data-stu-id="ea353-2421">vType</span></span>

<span data-ttu-id="ea353-2422">reserved1</span><span class="sxs-lookup"><span data-stu-id="ea353-2422">reserved1</span></span>

<span data-ttu-id="ea353-2423">reserved2</span><span class="sxs-lookup"><span data-stu-id="ea353-2423">reserved2</span></span>

<span data-ttu-id="ea353-2424">Offset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2424">Offset (optional)</span></span>



 

<span data-ttu-id="ea353-2425">**vType:** indicatore di tipo che indica il tipo di vValue.</span><span class="sxs-lookup"><span data-stu-id="ea353-2425">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="ea353-2426">DEVE essere uno dei valori VARENUM specificati nella sezione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-2426">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="ea353-2427">**reserved1:** non usato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2427">**reserved1**: Not used.</span></span> <span data-ttu-id="ea353-2428">Il valore può essere impostato su qualsiasi valore arbitrario e deve essere ignorato alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2428">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="ea353-2429">**reserved2:** non usato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2429">**reserved2**: Not used.</span></span> <span data-ttu-id="ea353-2430">Il valore può essere impostato su qualsiasi valore arbitrario e deve essere ignorato alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2430">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="ea353-2431">**Offset:** offset di dati a lunghezza variabile,ad esempio una stringa.</span><span class="sxs-lookup"><span data-stu-id="ea353-2431">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="ea353-2432">DEVE essere un valore a 32 bit (lunghezza di 4 byte) se vengono usati offset a 32 bit (in base alle regole della sezione 2.2.3.16) o un valore a 64 byte (lunghezza di 8 byte) se vengono usati offset a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-2432">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="ea353-2433">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="ea353-2433">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="ea353-2434">La struttura CSortSet contiene l'ordinamento della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2434">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="ea353-2435">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2435">0</span></span>

<span data-ttu-id="ea353-2436">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2436">1</span></span>

<span data-ttu-id="ea353-2437">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2437">2</span></span>

<span data-ttu-id="ea353-2438">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2438">3</span></span>

<span data-ttu-id="ea353-2439">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2439">4</span></span>

<span data-ttu-id="ea353-2440">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2440">5</span></span>

<span data-ttu-id="ea353-2441">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2441">6</span></span>

<span data-ttu-id="ea353-2442">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2442">7</span></span>

<span data-ttu-id="ea353-2443">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2443">8</span></span>

<span data-ttu-id="ea353-2444">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2444">9</span></span>

<span data-ttu-id="ea353-2445">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2445">1</span></span><br/> <span data-ttu-id="ea353-2446">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2446">0</span></span><br/>

<span data-ttu-id="ea353-2447">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2447">1</span></span>

<span data-ttu-id="ea353-2448">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2448">2</span></span>

<span data-ttu-id="ea353-2449">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2449">3</span></span>

<span data-ttu-id="ea353-2450">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2450">4</span></span>

<span data-ttu-id="ea353-2451">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2451">5</span></span>

<span data-ttu-id="ea353-2452">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2452">6</span></span>

<span data-ttu-id="ea353-2453">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2453">7</span></span>

<span data-ttu-id="ea353-2454">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2454">8</span></span>

<span data-ttu-id="ea353-2455">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2455">9</span></span>

<span data-ttu-id="ea353-2456">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2456">2</span></span><br/> <span data-ttu-id="ea353-2457">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2457">0</span></span><br/>

<span data-ttu-id="ea353-2458">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2458">1</span></span>

<span data-ttu-id="ea353-2459">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2459">2</span></span>

<span data-ttu-id="ea353-2460">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2460">3</span></span>

<span data-ttu-id="ea353-2461">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2461">4</span></span>

<span data-ttu-id="ea353-2462">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2462">5</span></span>

<span data-ttu-id="ea353-2463">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2463">6</span></span>

<span data-ttu-id="ea353-2464">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2464">7</span></span>

<span data-ttu-id="ea353-2465">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2465">8</span></span>

<span data-ttu-id="ea353-2466">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2466">9</span></span>

<span data-ttu-id="ea353-2467">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2467">3</span></span><br/> <span data-ttu-id="ea353-2468">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2468">0</span></span><br/>

<span data-ttu-id="ea353-2469">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2469">1</span></span>

<span data-ttu-id="ea353-2470">Conteggio</span><span class="sxs-lookup"><span data-stu-id="ea353-2470">Count</span></span>

<span data-ttu-id="ea353-2471">sortArray (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-2471">sortArray (variable)</span></span>



 

<span data-ttu-id="ea353-2472">**count:** intero senza segno a 32 bit che specifica il numero di elementi in sortArray.</span><span class="sxs-lookup"><span data-stu-id="ea353-2472">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="ea353-2473">**sortArray:** matrice di strutture CSort che descrive l'ordine in cui ordinare i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2473">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="ea353-2474">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di riempimento in modo che ogni struttura abbia un allineamento di 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2474">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="ea353-2475">Tali byte di riempimento possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2475">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="ea353-2476">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="ea353-2476">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="ea353-2477">La struttura CTableColumn contiene una colonna di un messaggio CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2477">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="ea353-2478">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2478">0</span></span>

<span data-ttu-id="ea353-2479">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2479">1</span></span>

<span data-ttu-id="ea353-2480">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2480">2</span></span>

<span data-ttu-id="ea353-2481">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2481">3</span></span>

<span data-ttu-id="ea353-2482">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2482">4</span></span>

<span data-ttu-id="ea353-2483">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2483">5</span></span>

<span data-ttu-id="ea353-2484">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2484">6</span></span>

<span data-ttu-id="ea353-2485">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2485">7</span></span>

<span data-ttu-id="ea353-2486">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2486">8</span></span>

<span data-ttu-id="ea353-2487">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2487">9</span></span>

<span data-ttu-id="ea353-2488">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2488">1</span></span><br/> <span data-ttu-id="ea353-2489">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2489">0</span></span><br/>

<span data-ttu-id="ea353-2490">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2490">1</span></span>

<span data-ttu-id="ea353-2491">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2491">2</span></span>

<span data-ttu-id="ea353-2492">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2492">3</span></span>

<span data-ttu-id="ea353-2493">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2493">4</span></span>

<span data-ttu-id="ea353-2494">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2494">5</span></span>

<span data-ttu-id="ea353-2495">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2495">6</span></span>

<span data-ttu-id="ea353-2496">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2496">7</span></span>

<span data-ttu-id="ea353-2497">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2497">8</span></span>

<span data-ttu-id="ea353-2498">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2498">9</span></span>

<span data-ttu-id="ea353-2499">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2499">2</span></span><br/> <span data-ttu-id="ea353-2500">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2500">0</span></span><br/>

<span data-ttu-id="ea353-2501">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2501">1</span></span>

<span data-ttu-id="ea353-2502">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2502">2</span></span>

<span data-ttu-id="ea353-2503">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2503">3</span></span>

<span data-ttu-id="ea353-2504">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2504">4</span></span>

<span data-ttu-id="ea353-2505">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2505">5</span></span>

<span data-ttu-id="ea353-2506">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2506">6</span></span>

<span data-ttu-id="ea353-2507">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2507">7</span></span>

<span data-ttu-id="ea353-2508">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2508">8</span></span>

<span data-ttu-id="ea353-2509">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2509">9</span></span>

<span data-ttu-id="ea353-2510">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2510">3</span></span><br/> <span data-ttu-id="ea353-2511">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2511">0</span></span><br/>

<span data-ttu-id="ea353-2512">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2512">1</span></span>

<span data-ttu-id="ea353-2513">PropSpec</span><span class="sxs-lookup"><span data-stu-id="ea353-2513">PropSpec</span></span>

<span data-ttu-id="ea353-2514">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-2514">...(variable)</span></span>

<span data-ttu-id="ea353-2515">vType</span><span class="sxs-lookup"><span data-stu-id="ea353-2515">vType</span></span>

<span data-ttu-id="ea353-2516">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="ea353-2516">ValueUsed</span></span>

<span data-ttu-id="ea353-2517">\_padding1 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2517">\_padding1 (optional)</span></span>

<span data-ttu-id="ea353-2518">ValueOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2518">ValueOffset (optional)</span></span>

<span data-ttu-id="ea353-2519">ValueSize (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2519">ValueSize (optional)</span></span>

<span data-ttu-id="ea353-2520">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="ea353-2520">StatusUsed</span></span>

<span data-ttu-id="ea353-2521">\_padding2 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2521">\_padding2 (optional)</span></span>

<span data-ttu-id="ea353-2522">StatusOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2522">StatusOffset (optional)</span></span>

<span data-ttu-id="ea353-2523">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="ea353-2523">LengthUsed</span></span>

<span data-ttu-id="ea353-2524">\_padding3 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2524">\_padding3 (optional)</span></span>

<span data-ttu-id="ea353-2525">LengthOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2525">LengthOffset (optional)</span></span>



 

<span data-ttu-id="ea353-2526">**PropSpec:** struttura CFullPropSpec come specificato nella Sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="ea353-2526">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="ea353-2527">**vType**: specifica il tipo di valore di dati contenuto nella colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-2527">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="ea353-2528">Vedere il campo vType nella Sezione 2.2.1.1 per l'elenco di valori per questo campo.</span><span class="sxs-lookup"><span data-stu-id="ea353-2528">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="ea353-2529">**ValueUsed:** campo di un byte che DEVE essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-2529">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="ea353-2530">Se impostato su 0x01, la colonna viene trasferita all'interno della riga di dimensioni fisse.</span><span class="sxs-lookup"><span data-stu-id="ea353-2530">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="ea353-2531">Se impostato su 0x00, il valore della colonna viene trasferito nella sezione a lunghezza variabile alla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="ea353-2531">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="ea353-2532">**\_ padding1:** campo di un byte che DEVE essere inserito prima di ValueOffset se, senza di esso, ValueOffset non inizia a un offset pari dall'inizio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2532">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="ea353-2533">Il valore di questo byte è arbitrario e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2533">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="ea353-2534">Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2534">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="ea353-2535">**ValueOffset:** intero senza segno a 2 byte che specifica l'offset del valore della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-2535">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="ea353-2536">Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2536">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="ea353-2537">**ValueSize:** intero senza segno a 2 byte che specifica le dimensioni del valore della colonna in byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-2537">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="ea353-2538">Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2538">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="ea353-2539">**StatusUsed:** campo di un byte che DEVE essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-2539">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="ea353-2540">Se impostato su 0x01, lo stato della colonna viene trasferito all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-2540">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="ea353-2541">Se 0x00, lo stato della colonna non viene trasferito all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-2541">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="ea353-2542">**\_ padding2:** campo di un byte che DEVE essere inserito prima di StatusOffset se, senza di esso, il campo StatusOffset non inizia in corrispondenza di un offset pari dall'inizio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2542">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="ea353-2543">Il valore di questo byte è arbitrario e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2543">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="ea353-2544">Se StatusUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2544">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="ea353-2545">**StatusOffset:** intero senza segno a 2 byte che specifica l'offset dello stato della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-2545">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="ea353-2546">Se StatusUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2546">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="ea353-2547">**LengthUsed:** campo di un byte che DEVE essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-2547">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="ea353-2548">Se impostato su 0x01, la lunghezza della colonna viene trasferita all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-2548">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="ea353-2549">Se 0x00, la lunghezza della colonna NON DEVE essere trasferita all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-2549">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="ea353-2550">**\_ padding3:** campo di un byte che DEVE essere inserito prima di LengthOffset se, senza di esso, LengthOffset non inizia a un offset pari dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2550">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="ea353-2551">Il valore di questo byte è arbitrario e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2551">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="ea353-2552">Se LengthUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2552">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="ea353-2553">**LengthOffset:** intero senza segno a 2 byte che specifica l'offset della lunghezza della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-2553">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="ea353-2554">Se LengthUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2554">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="ea353-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="ea353-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="ea353-2556">La struttura SERIALIZEDPROPERTYVALUE contiene un valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2556">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="ea353-2557">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2557">0</span></span>

<span data-ttu-id="ea353-2558">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2558">1</span></span>

<span data-ttu-id="ea353-2559">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2559">2</span></span>

<span data-ttu-id="ea353-2560">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2560">3</span></span>

<span data-ttu-id="ea353-2561">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2561">4</span></span>

<span data-ttu-id="ea353-2562">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2562">5</span></span>

<span data-ttu-id="ea353-2563">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2563">6</span></span>

<span data-ttu-id="ea353-2564">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2564">7</span></span>

<span data-ttu-id="ea353-2565">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2565">8</span></span>

<span data-ttu-id="ea353-2566">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2566">9</span></span>

<span data-ttu-id="ea353-2567">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2567">1</span></span><br/> <span data-ttu-id="ea353-2568">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2568">0</span></span><br/>

<span data-ttu-id="ea353-2569">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2569">1</span></span>

<span data-ttu-id="ea353-2570">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2570">2</span></span>

<span data-ttu-id="ea353-2571">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2571">3</span></span>

<span data-ttu-id="ea353-2572">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2572">4</span></span>

<span data-ttu-id="ea353-2573">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2573">5</span></span>

<span data-ttu-id="ea353-2574">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2574">6</span></span>

<span data-ttu-id="ea353-2575">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2575">7</span></span>

<span data-ttu-id="ea353-2576">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2576">8</span></span>

<span data-ttu-id="ea353-2577">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2577">9</span></span>

<span data-ttu-id="ea353-2578">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2578">2</span></span><br/> <span data-ttu-id="ea353-2579">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2579">0</span></span><br/>

<span data-ttu-id="ea353-2580">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2580">1</span></span>

<span data-ttu-id="ea353-2581">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2581">2</span></span>

<span data-ttu-id="ea353-2582">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2582">3</span></span>

<span data-ttu-id="ea353-2583">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2583">4</span></span>

<span data-ttu-id="ea353-2584">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2584">5</span></span>

<span data-ttu-id="ea353-2585">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2585">6</span></span>

<span data-ttu-id="ea353-2586">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2586">7</span></span>

<span data-ttu-id="ea353-2587">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2587">8</span></span>

<span data-ttu-id="ea353-2588">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2588">9</span></span>

<span data-ttu-id="ea353-2589">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2589">3</span></span><br/> <span data-ttu-id="ea353-2590">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2590">0</span></span><br/>

<span data-ttu-id="ea353-2591">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2591">1</span></span>

<span data-ttu-id="ea353-2592">dwType</span><span class="sxs-lookup"><span data-stu-id="ea353-2592">dwType</span></span>

<span data-ttu-id="ea353-2593">rgb (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-2593">rgb (variable)</span></span>



 

<span data-ttu-id="ea353-2594">**dwType:** uno dei tipi variant, definiti nella sezione 2.2.1.1, che possono essere combinati con modificatori di tipo variant.</span><span class="sxs-lookup"><span data-stu-id="ea353-2594">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="ea353-2595">Per tutti i tipi variant, ad eccezione di quelli combinati con VT ARRAY, SERIALIZEDPROPERTYVALUE ha lo stesso layout di \_ CBaseStorageVariant, come specificato nella sezione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-2595">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="ea353-2596">Se il tipo variant viene combinato con il modificatore di tipo VT ARRAY, viene usato SAFEARRAY2, specificato nella Sezione \_ 2.2.1.2.1.1, anziché SAFEARRAY nel campo vValue di CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="ea353-2596">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="ea353-2597">**rgb:** valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2597">**rgb**: Serialized value.</span></span> <span data-ttu-id="ea353-2598">Vedere i dettagli della serializzazione per vValue nella versione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-2598">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="ea353-2599">2.2.2 Intestazioni dei messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-2599">2.2.2 Message Headers</span></span>

<span data-ttu-id="ea353-2600">Tutti i messaggi del protocollo del servizio di indicizzazione del contenuto hanno un'intestazione di 16 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-2600">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="ea353-2601">Di seguito è riportato un diagramma che mostra il formato dell'intestazione del messaggio content indexing service protocol.</span><span class="sxs-lookup"><span data-stu-id="ea353-2601">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="ea353-2602">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2602">0</span></span>

<span data-ttu-id="ea353-2603">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2603">1</span></span>

<span data-ttu-id="ea353-2604">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2604">2</span></span>

<span data-ttu-id="ea353-2605">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2605">3</span></span>

<span data-ttu-id="ea353-2606">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2606">4</span></span>

<span data-ttu-id="ea353-2607">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2607">5</span></span>

<span data-ttu-id="ea353-2608">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2608">6</span></span>

<span data-ttu-id="ea353-2609">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2609">7</span></span>

<span data-ttu-id="ea353-2610">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2610">8</span></span>

<span data-ttu-id="ea353-2611">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2611">9</span></span>

<span data-ttu-id="ea353-2612">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2612">1</span></span><br/> <span data-ttu-id="ea353-2613">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2613">0</span></span><br/>

<span data-ttu-id="ea353-2614">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2614">1</span></span>

<span data-ttu-id="ea353-2615">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2615">2</span></span>

<span data-ttu-id="ea353-2616">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2616">3</span></span>

<span data-ttu-id="ea353-2617">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2617">4</span></span>

<span data-ttu-id="ea353-2618">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2618">5</span></span>

<span data-ttu-id="ea353-2619">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2619">6</span></span>

<span data-ttu-id="ea353-2620">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2620">7</span></span>

<span data-ttu-id="ea353-2621">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2621">8</span></span>

<span data-ttu-id="ea353-2622">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2622">9</span></span>

<span data-ttu-id="ea353-2623">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2623">2</span></span><br/> <span data-ttu-id="ea353-2624">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2624">0</span></span><br/>

<span data-ttu-id="ea353-2625">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2625">1</span></span>

<span data-ttu-id="ea353-2626">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2626">2</span></span>

<span data-ttu-id="ea353-2627">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2627">3</span></span>

<span data-ttu-id="ea353-2628">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2628">4</span></span>

<span data-ttu-id="ea353-2629">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2629">5</span></span>

<span data-ttu-id="ea353-2630">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2630">6</span></span>

<span data-ttu-id="ea353-2631">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2631">7</span></span>

<span data-ttu-id="ea353-2632">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2632">8</span></span>

<span data-ttu-id="ea353-2633">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2633">9</span></span>

<span data-ttu-id="ea353-2634">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2634">3</span></span><br/> <span data-ttu-id="ea353-2635">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2635">0</span></span><br/>

<span data-ttu-id="ea353-2636">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2636">1</span></span>

<span data-ttu-id="ea353-2637">\_msg</span><span class="sxs-lookup"><span data-stu-id="ea353-2637">\_msg</span></span>

<span data-ttu-id="ea353-2638">\_Stato</span><span class="sxs-lookup"><span data-stu-id="ea353-2638">\_status</span></span>

<span data-ttu-id="ea353-2639">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="ea353-2639">\_ulChecksum</span></span>

<span data-ttu-id="ea353-2640">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="ea353-2640">\_ulReserved2</span></span>



 

<span data-ttu-id="ea353-2641">\_**msg:** intero a 32 bit che identifica il tipo di messaggio dopo l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2641">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="ea353-2642">Nella tabella seguente sono elencati i messaggi del protocollo del servizio di indicizzazione del contenuto e i valori interi specificati per ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2642">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="ea353-2643">Come illustrato nella tabella, alcuni valori identificano 2 messaggi nella tabella.</span><span class="sxs-lookup"><span data-stu-id="ea353-2643">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="ea353-2644">In questi casi il messaggio che segue l'intestazione può essere identificato dalla direzione del flusso del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2644">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="ea353-2645">Se la direzione è da client a server, viene indicato il messaggio con "In" aggiunto al nome del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2645">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="ea353-2646">Se la direzione è da server a client, viene indicato il messaggio con "Out" aggiunto al nome del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2646">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="ea353-2647">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-2647">Value</span></span>      | <span data-ttu-id="ea353-2648">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-2648">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="ea353-2649">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="ea353-2649">0x000000C8</span></span> | <span data-ttu-id="ea353-2650">CPMConnectIn o CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2650">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="ea353-2651">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="ea353-2651">0x000000C9</span></span> | <span data-ttu-id="ea353-2652">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="ea353-2652">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="ea353-2653">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="ea353-2653">0x000000CA</span></span> | <span data-ttu-id="ea353-2654">CPMCreateQueryIn o CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2654">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="ea353-2655">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="ea353-2655">0x000000CB</span></span> | <span data-ttu-id="ea353-2656">CPMFreeCursorIn o CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2656">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="ea353-2657">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="ea353-2657">0x000000CC</span></span> | <span data-ttu-id="ea353-2658">CPMGetRowsIn o CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2658">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="ea353-2659">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="ea353-2659">0x000000CD</span></span> | <span data-ttu-id="ea353-2660">CPMRatioFinishedIn o CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2660">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="ea353-2661">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="ea353-2661">0x000000CE</span></span> | <span data-ttu-id="ea353-2662">CPMCompareBmkIn o CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2662">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="ea353-2663">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="ea353-2663">0x000000CF</span></span> | <span data-ttu-id="ea353-2664">CPMGetApproximatePositionIn o CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2664">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="ea353-2665">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="ea353-2665">0x000000D0</span></span> | <span data-ttu-id="ea353-2666">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2666">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="ea353-2667">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="ea353-2667">0x000000D1</span></span> | <span data-ttu-id="ea353-2668">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="ea353-2668">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="ea353-2669">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="ea353-2669">0x000000D2</span></span> | <span data-ttu-id="ea353-2670">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2670">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="ea353-2671">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="ea353-2671">0x000000D7</span></span> | <span data-ttu-id="ea353-2672">CPMGetQueryStatusIn o CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2672">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="ea353-2673">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="ea353-2673">0x000000D9</span></span> | <span data-ttu-id="ea353-2674">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2674">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="ea353-2675">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="ea353-2675">0x000000E1</span></span> | <span data-ttu-id="ea353-2676">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2676">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="ea353-2677">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="ea353-2677">0x000000E4</span></span> | <span data-ttu-id="ea353-2678">CPMFetchValueIn o CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2678">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="ea353-2679">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="ea353-2679">0x000000E6</span></span> | <span data-ttu-id="ea353-2680">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2680">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="ea353-2681">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="ea353-2681">0x000000E7</span></span> | <span data-ttu-id="ea353-2682">CPMGetQueryStatusExIn o PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2682">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="ea353-2683">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="ea353-2683">0x000000E8</span></span> | <span data-ttu-id="ea353-2684">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2684">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="ea353-2685">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="ea353-2685">0x000000E9</span></span> | <span data-ttu-id="ea353-2686">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2686">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="ea353-2687">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="ea353-2687">0x000000EC</span></span> | <span data-ttu-id="ea353-2688">CPMSetCatStateIn o CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2688">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="ea353-2689">\_**status**: HRESULT \[ MS-SYS \] che indica lo stato dell'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea353-2689">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="ea353-2690">*Comportamento di Windows: il client imposta sempre il \_ campo di stato su 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="ea353-2690">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="ea353-2691">**\_ ulChecksum**: \_ ulChecksum MUST deve essere calcolato come specificato nella Sezione 3.2.4 per i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-2691">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="ea353-2692">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2692">CPMConnectIn</span></span>
-   <span data-ttu-id="ea353-2693">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2693">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="ea353-2694">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2694">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="ea353-2695">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2695">CPMGetRowsIn</span></span>
-   <span data-ttu-id="ea353-2696">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2696">CPMFetchValueIn</span></span>

<span data-ttu-id="ea353-2697">Per tutti gli altri messaggi, \_ ulChecksum DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-2697">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="ea353-2698">Un client DEVE ignorare il \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="ea353-2698">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="ea353-2699">**\_ ulReserved2:** DEVE essere impostato su 0 e ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-2699">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="ea353-2700">2.2.3 Messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-2700">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="ea353-2701">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2701">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="ea353-2702">Il messaggio CPMCiStateInOut contiene informazioni sullo stato del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2702">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="ea353-2703">Il formato del messaggio CPMCiStateInOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-2703">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-2704">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2704">0</span></span>

<span data-ttu-id="ea353-2705">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2705">1</span></span>

<span data-ttu-id="ea353-2706">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2706">2</span></span>

<span data-ttu-id="ea353-2707">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2707">3</span></span>

<span data-ttu-id="ea353-2708">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2708">4</span></span>

<span data-ttu-id="ea353-2709">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2709">5</span></span>

<span data-ttu-id="ea353-2710">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2710">6</span></span>

<span data-ttu-id="ea353-2711">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2711">7</span></span>

<span data-ttu-id="ea353-2712">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2712">8</span></span>

<span data-ttu-id="ea353-2713">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2713">9</span></span>

<span data-ttu-id="ea353-2714">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2714">1</span></span><br/> <span data-ttu-id="ea353-2715">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2715">0</span></span><br/>

<span data-ttu-id="ea353-2716">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2716">1</span></span>

<span data-ttu-id="ea353-2717">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2717">2</span></span>

<span data-ttu-id="ea353-2718">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2718">3</span></span>

<span data-ttu-id="ea353-2719">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2719">4</span></span>

<span data-ttu-id="ea353-2720">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2720">5</span></span>

<span data-ttu-id="ea353-2721">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2721">6</span></span>

<span data-ttu-id="ea353-2722">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2722">7</span></span>

<span data-ttu-id="ea353-2723">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2723">8</span></span>

<span data-ttu-id="ea353-2724">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2724">9</span></span>

<span data-ttu-id="ea353-2725">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2725">2</span></span><br/> <span data-ttu-id="ea353-2726">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2726">0</span></span><br/>

<span data-ttu-id="ea353-2727">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2727">1</span></span>

<span data-ttu-id="ea353-2728">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2728">2</span></span>

<span data-ttu-id="ea353-2729">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2729">3</span></span>

<span data-ttu-id="ea353-2730">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2730">4</span></span>

<span data-ttu-id="ea353-2731">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2731">5</span></span>

<span data-ttu-id="ea353-2732">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2732">6</span></span>

<span data-ttu-id="ea353-2733">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2733">7</span></span>

<span data-ttu-id="ea353-2734">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2734">8</span></span>

<span data-ttu-id="ea353-2735">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2735">9</span></span>

<span data-ttu-id="ea353-2736">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2736">3</span></span><br/> <span data-ttu-id="ea353-2737">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2737">0</span></span><br/>

<span data-ttu-id="ea353-2738">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2738">1</span></span>

<span data-ttu-id="ea353-2739">cbStruct</span><span class="sxs-lookup"><span data-stu-id="ea353-2739">cbStruct</span></span>

<span data-ttu-id="ea353-2740">cWordList</span><span class="sxs-lookup"><span data-stu-id="ea353-2740">cWordList</span></span>

<span data-ttu-id="ea353-2741">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="ea353-2741">cPersistentIndex</span></span>

<span data-ttu-id="ea353-2742">cQueries</span><span class="sxs-lookup"><span data-stu-id="ea353-2742">cQueries</span></span>

<span data-ttu-id="ea353-2743">cDocuments</span><span class="sxs-lookup"><span data-stu-id="ea353-2743">cDocuments</span></span>

<span data-ttu-id="ea353-2744">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="ea353-2744">cFreshTest</span></span>

<span data-ttu-id="ea353-2745">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="ea353-2745">dwMergeProgress</span></span>

<span data-ttu-id="ea353-2746">Tenuta</span><span class="sxs-lookup"><span data-stu-id="ea353-2746">eState</span></span>

<span data-ttu-id="ea353-2747">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="ea353-2747">cFilteredDocuments</span></span>

<span data-ttu-id="ea353-2748">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="ea353-2748">cTotalDocuments</span></span>

<span data-ttu-id="ea353-2749">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="ea353-2749">cPendingScans</span></span>

<span data-ttu-id="ea353-2750">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="ea353-2750">dwIndexSize</span></span>

<span data-ttu-id="ea353-2751">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="ea353-2751">cUniqueKeys</span></span>

<span data-ttu-id="ea353-2752">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="ea353-2752">cSecQDocuments</span></span>

<span data-ttu-id="ea353-2753">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="ea353-2753">dwPropCacheSize</span></span>



 

<span data-ttu-id="ea353-2754">**cbStruct:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-2754">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="ea353-2755">Dimensione in byte di questo messaggio (esclusa l'intestazione comune).</span><span class="sxs-lookup"><span data-stu-id="ea353-2755">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="ea353-2756">DEVE essere impostato su 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="ea353-2756">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="ea353-2757">**cWordList:** intero senza segno a 32 bit che indica il conteggio degli indici iniziali creati per i documenti indicizzati di recente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2757">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="ea353-2758">**cPersistentIndex:** intero senza segno a 32 bit che indica il conteggio degli indici persistenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-2758">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="ea353-2759">**cQueries:** intero senza segno a 32 bit che indica un numero di query in esecuzione attivamente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2759">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="ea353-2760">**cDocuments:** intero senza segno a 32 bit che indica il numero totale di documenti in attesa di essere indicizzati.</span><span class="sxs-lookup"><span data-stu-id="ea353-2760">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="ea353-2761">**cFreshTest:** intero senza segno a 32 bit che indica il numero di documenti univoci con informazioni negli indici non completamente ottimizzate per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ea353-2761">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="ea353-2762">**dwMergeProgress:** intero senza segno a 32 bit che specifica la percentuale di completamento dell'ottimizzazione completa corrente degli indici, se l'ottimizzazione è attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="ea353-2762">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="ea353-2763">DEVE essere minore o uguale a 100.</span><span class="sxs-lookup"><span data-stu-id="ea353-2763">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="ea353-2764">**eState:** stato dell'indicizzazione del contenuto specificato da una o più costanti CI \_ \_ \* STATE, definite nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ea353-2764">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="ea353-2765">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-2765">Value</span></span>                                         | <span data-ttu-id="ea353-2766">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-2766">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-2767">UNIONE \_ CI STATE SHADOW \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-2767">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="ea353-2768">Il servizio di indicizzazione sta ottimizzando alcuni indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2768">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ea353-2769">CI \_ STATE MASTER MERGE \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-2769">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="ea353-2770">Il servizio di indicizzazione è in corso di ottimizzazione completa per tutti gli indici.</span><span class="sxs-lookup"><span data-stu-id="ea353-2770">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ea353-2771">CI \_ STATE CONTENT SCAN REQUIRED \_ \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-2771">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="ea353-2772">Alcuni documenti nell'indice sono stati modificati e il servizio di indicizzazione deve determinare quali sono stati aggiunti, modificati o eliminati.</span><span class="sxs-lookup"><span data-stu-id="ea353-2772">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ea353-2773">CI \_ STATE \_ ANNEALING \_ MERGE 0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea353-2773">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="ea353-2774">Il servizio di indicizzazione sta ottimizzando gli indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2774">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="ea353-2775">Questo processo è più completo di quello identificato dal valore CI STATE SHADOW MERGE, ma non è così completo come specificato dal \_ valore CI STATE MASTER \_ \_ \_ \_ \_ MERGE.</span><span class="sxs-lookup"><span data-stu-id="ea353-2775">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="ea353-2776">Queste ottimizzazioni sono specifiche dell'implementazione in quanto dipendono dal modo in cui i dati vengono archiviati internamente. le ottimizzazioni non influiscono sul protocollo in alcun modo diverso dal tempo di risposta.</span><span class="sxs-lookup"><span data-stu-id="ea353-2776">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="ea353-2777">ANALISI \_ DELLO STATO CI \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea353-2777">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="ea353-2778">Il servizio di indicizzazione sta esaminando una directory o un set di directory per verificare se sono stati aggiunti, eliminati o aggiornati file dall'ultima volta che la directory è stata indicizzata.</span><span class="sxs-lookup"><span data-stu-id="ea353-2778">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ea353-2779">CI \_ STATE \_ RECOVERING 0x00000020</span><span class="sxs-lookup"><span data-stu-id="ea353-2779">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="ea353-2780">Il servizio viene avviato dall'ultimo stato salvato ed è in corso il ripristino.</span><span class="sxs-lookup"><span data-stu-id="ea353-2780">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ea353-2781">STATO CI \_ MEMORIA \_ INSUFFICIENTE \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="ea353-2781">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="ea353-2782">La maggior parte della memoria virtuale del server è in uso.</span><span class="sxs-lookup"><span data-stu-id="ea353-2782">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ea353-2783">CI \_ STATE HIGH IO \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="ea353-2783">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="ea353-2784">Il livello di attività di input/output (I/O) nel server è relativamente elevato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2784">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ea353-2785">CI \_ STATE MASTER MERGE \_ \_ \_ PAUSED 0x00000200</span><span class="sxs-lookup"><span data-stu-id="ea353-2785">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="ea353-2786">Il processo di ottimizzazione completa per tutti gli indici in corso è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="ea353-2786">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="ea353-2787">Questo viene fornito solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-2787">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ea353-2788">CI \_ STATE READ ONLY \_ \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="ea353-2788">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="ea353-2789">La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="ea353-2789">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="ea353-2790">Questo viene fornito solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ea353-2791">CI \_ STATE BATTERY POWER \_ \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="ea353-2791">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="ea353-2792">La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa per risparmiare la durata della batteria, ma risponde comunque alle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2792">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="ea353-2793">Questo viene fornito solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ea353-2794">CI \_ STATE USER ACTIVE \_ \_ 0x00001000</span><span class="sxs-lookup"><span data-stu-id="ea353-2794">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="ea353-2795">La parte del servizio di indicizzazione che raccoglie nuovi documenti da indicizzare è stata sospesa a causa di un'attività elevata dell'utente (tastiera o mouse), ma risponde comunque alle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2795">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="ea353-2796">Questo viene fornito solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="ea353-2797">CI \_ STATE \_ STARTING 0x00002000</span><span class="sxs-lookup"><span data-stu-id="ea353-2797">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="ea353-2798">Il servizio è in fase di avvio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2798">The service is starting.</span></span> <span data-ttu-id="ea353-2799">Le query possono essere eseguite, ma l'analisi e la notifica non sono ancora state abilitate.</span><span class="sxs-lookup"><span data-stu-id="ea353-2799">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="ea353-2800">Questo viene fornito solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-2800">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="ea353-2801">CI \_ STATE \_ READING \_ USNS 0x00004000</span><span class="sxs-lookup"><span data-stu-id="ea353-2801">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="ea353-2802">Il servizio non ha letto il log mantenuto dal file system per tenere traccia delle modifiche apportate a file o directory in un volume, pertanto l'indice potrebbe non essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2802">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="ea353-2803">**cFilteredDocuments:** intero senza segno a 32 bit che indica il numero di documenti indicizzati dall'inizio dell'indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea353-2803">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="ea353-2804">**cTotalDocuments:** intero senza segno a 32 bit che indica il numero totale di documenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ea353-2804">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="ea353-2805">**cPendingScans:** intero senza segno a 32 bit che indica il numero di operazioni di indicizzazione di alto livello in sospeso.</span><span class="sxs-lookup"><span data-stu-id="ea353-2805">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="ea353-2806">Il significato di questo valore è specifico del provider, ma è previsto che numeri più grandi indichino una maggiore quantità di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2806">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="ea353-2807">*Comportamento di Windows:* questo valore è in genere zero, tranne immediatamente dopo l'avvio dell'indicizzazione o dopo l'overflow di una coda di notifica.</span><span class="sxs-lookup"><span data-stu-id="ea353-2807">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="ea353-2808">**dwIndexSize:** intero senza segno a 32 bit che indica le dimensioni, in megabyte, dell'indice (esclusa la cache delle proprietà).</span><span class="sxs-lookup"><span data-stu-id="ea353-2808">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="ea353-2809">**cUniqueKeys:** intero senza segno a 32 bit che indica il numero approssimativo di chiavi univoche nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-2809">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="ea353-2810">**cSecQDocuments:** intero senza segno a 32 bit che indica il numero di documenti che il servizio di indicizzazione tenterà nuovamente di indicizzare a causa di un errore durante il tentativo iniziale di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2810">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="ea353-2811">**dwPropCacheSize:** intero senza segno a 32 bit che indica le dimensioni, in megabyte, della cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-2811">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="ea353-2812">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2812">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="ea353-2813">Il messaggio CPMSetCatStateIn imposta lo stato di un catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-2813">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="ea353-2814">Il formato del messaggio CPMSetCatStateIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-2814">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-2815">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2815">0</span></span>

<span data-ttu-id="ea353-2816">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2816">1</span></span>

<span data-ttu-id="ea353-2817">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2817">2</span></span>

<span data-ttu-id="ea353-2818">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2818">3</span></span>

<span data-ttu-id="ea353-2819">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2819">4</span></span>

<span data-ttu-id="ea353-2820">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2820">5</span></span>

<span data-ttu-id="ea353-2821">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2821">6</span></span>

<span data-ttu-id="ea353-2822">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2822">7</span></span>

<span data-ttu-id="ea353-2823">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2823">8</span></span>

<span data-ttu-id="ea353-2824">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2824">9</span></span>

<span data-ttu-id="ea353-2825">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2825">1</span></span><br/> <span data-ttu-id="ea353-2826">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2826">0</span></span><br/>

<span data-ttu-id="ea353-2827">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2827">1</span></span>

<span data-ttu-id="ea353-2828">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2828">2</span></span>

<span data-ttu-id="ea353-2829">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2829">3</span></span>

<span data-ttu-id="ea353-2830">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2830">4</span></span>

<span data-ttu-id="ea353-2831">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2831">5</span></span>

<span data-ttu-id="ea353-2832">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2832">6</span></span>

<span data-ttu-id="ea353-2833">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2833">7</span></span>

<span data-ttu-id="ea353-2834">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2834">8</span></span>

<span data-ttu-id="ea353-2835">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2835">9</span></span>

<span data-ttu-id="ea353-2836">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2836">2</span></span><br/> <span data-ttu-id="ea353-2837">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2837">0</span></span><br/>

<span data-ttu-id="ea353-2838">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2838">1</span></span>

<span data-ttu-id="ea353-2839">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2839">2</span></span>

<span data-ttu-id="ea353-2840">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2840">3</span></span>

<span data-ttu-id="ea353-2841">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2841">4</span></span>

<span data-ttu-id="ea353-2842">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2842">5</span></span>

<span data-ttu-id="ea353-2843">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2843">6</span></span>

<span data-ttu-id="ea353-2844">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2844">7</span></span>

<span data-ttu-id="ea353-2845">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2845">8</span></span>

<span data-ttu-id="ea353-2846">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2846">9</span></span>

<span data-ttu-id="ea353-2847">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2847">3</span></span><br/> <span data-ttu-id="ea353-2848">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2848">0</span></span><br/>

<span data-ttu-id="ea353-2849">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2849">1</span></span>

<span data-ttu-id="ea353-2850">\_partID</span><span class="sxs-lookup"><span data-stu-id="ea353-2850">\_partID</span></span>

<span data-ttu-id="ea353-2851">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="ea353-2851">\_dwNewState</span></span>

<span data-ttu-id="ea353-2852">\_CatName (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2852">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="ea353-2853">**\_ partID:** deve essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-2853">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="ea353-2854">**\_ dwNewState:** DEVE essere impostato su uno dei valori seguenti, che indica il nuovo stato del catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-2854">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="ea353-2855">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-2855">Value</span></span>                         | <span data-ttu-id="ea353-2856">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-2856">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-2857">CICAT \_ ARRESTATO 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-2857">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="ea353-2858">Il catalogo è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2858">The catalog is stopped.</span></span> <span data-ttu-id="ea353-2859">Questo stato indica che non è necessario indicizzare nuovi file e che non devono essere elaborate query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-2859">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="ea353-2860">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-2860">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="ea353-2861">Il catalogo è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ea353-2861">The catalog is read-only.</span></span> <span data-ttu-id="ea353-2862">Non è necessario indicizzare nuovi file.</span><span class="sxs-lookup"><span data-stu-id="ea353-2862">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="ea353-2863">CiCAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-2863">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="ea353-2864">Il catalogo è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="ea353-2864">The catalog is writable.</span></span> <span data-ttu-id="ea353-2865">I nuovi file possono essere indicizzati e le query di ricerca devono essere elaborate.</span><span class="sxs-lookup"><span data-stu-id="ea353-2865">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="ea353-2866">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea353-2866">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="ea353-2867">Il catalogo non è disponibile per l'esecuzione di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2867">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="ea353-2868">CICAT \_ GET \_ STATE 0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea353-2868">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="ea353-2869">Lo stato del catalogo non deve essere modificato, ma solo recuperato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2869">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="ea353-2870">CICAT \_ ALL \_ OPENED 0x00000020</span><span class="sxs-lookup"><span data-stu-id="ea353-2870">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="ea353-2871">Controllo per verificare se tutti i cataloghi sono stati avviati.</span><span class="sxs-lookup"><span data-stu-id="ea353-2871">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="ea353-2872">In questo caso, il campo dwOldState inviato nella risposta CPMSetCatStateOut a questo messaggio verrà \_ segnalato come diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="ea353-2872">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="ea353-2873">**\_ CatName:** nome del catalogo il cui stato deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2873">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="ea353-2874">Il nome DEVE essere una stringa Unicode con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="ea353-2874">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="ea353-2875">Questo campo DEVE essere omesso se \_ dwNewState è impostato su CICAT \_ ALL \_ OPENED.</span><span class="sxs-lookup"><span data-stu-id="ea353-2875">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="ea353-2876">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="ea353-2876">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="ea353-2877">Il messaggio CPMSetCatStateOut è una risposta a un messaggio CPMSetCatStateIn con lo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-2877">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="ea353-2878">Il formato del messaggio CPMSetCatStateOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-2878">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-2879">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2879">0</span></span>

<span data-ttu-id="ea353-2880">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2880">1</span></span>

<span data-ttu-id="ea353-2881">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2881">2</span></span>

<span data-ttu-id="ea353-2882">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2882">3</span></span>

<span data-ttu-id="ea353-2883">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2883">4</span></span>

<span data-ttu-id="ea353-2884">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2884">5</span></span>

<span data-ttu-id="ea353-2885">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2885">6</span></span>

<span data-ttu-id="ea353-2886">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2886">7</span></span>

<span data-ttu-id="ea353-2887">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2887">8</span></span>

<span data-ttu-id="ea353-2888">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2888">9</span></span>

<span data-ttu-id="ea353-2889">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2889">1</span></span><br/> <span data-ttu-id="ea353-2890">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2890">0</span></span><br/>

<span data-ttu-id="ea353-2891">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2891">1</span></span>

<span data-ttu-id="ea353-2892">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2892">2</span></span>

<span data-ttu-id="ea353-2893">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2893">3</span></span>

<span data-ttu-id="ea353-2894">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2894">4</span></span>

<span data-ttu-id="ea353-2895">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2895">5</span></span>

<span data-ttu-id="ea353-2896">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2896">6</span></span>

<span data-ttu-id="ea353-2897">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2897">7</span></span>

<span data-ttu-id="ea353-2898">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2898">8</span></span>

<span data-ttu-id="ea353-2899">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2899">9</span></span>

<span data-ttu-id="ea353-2900">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2900">2</span></span><br/> <span data-ttu-id="ea353-2901">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2901">0</span></span><br/>

<span data-ttu-id="ea353-2902">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2902">1</span></span>

<span data-ttu-id="ea353-2903">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2903">2</span></span>

<span data-ttu-id="ea353-2904">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2904">3</span></span>

<span data-ttu-id="ea353-2905">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2905">4</span></span>

<span data-ttu-id="ea353-2906">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2906">5</span></span>

<span data-ttu-id="ea353-2907">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2907">6</span></span>

<span data-ttu-id="ea353-2908">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2908">7</span></span>

<span data-ttu-id="ea353-2909">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2909">8</span></span>

<span data-ttu-id="ea353-2910">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2910">9</span></span>

<span data-ttu-id="ea353-2911">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2911">3</span></span><br/> <span data-ttu-id="ea353-2912">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2912">0</span></span><br/>

<span data-ttu-id="ea353-2913">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2913">1</span></span>

<span data-ttu-id="ea353-2914">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="ea353-2914">\_dwOldState</span></span>



 

<span data-ttu-id="ea353-2915">**\_ dwOldState:** uno dei valori seguenti, che indica lo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-2915">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="ea353-2916">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-2916">Value</span></span>                       | <span data-ttu-id="ea353-2917">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-2917">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="ea353-2918">CICAT \_ ARRESTATO 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-2918">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="ea353-2919">Il catalogo è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2919">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="ea353-2920">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-2920">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="ea353-2921">Il catalogo è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ea353-2921">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="ea353-2922">CiCAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-2922">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="ea353-2923">Il catalogo è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="ea353-2923">The catalog is writable.</span></span>                   |
| <span data-ttu-id="ea353-2924">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea353-2924">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="ea353-2925">Il catalogo non è disponibile per l'esecuzione di query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2925">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="ea353-2926">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2926">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="ea353-2927">Il messaggio CPMUpdateDocumentsIn indica al server di indicizzare il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2927">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="ea353-2928">Il server risponderà con l'intestazione del messaggio CPMUpdateDocumentsOut, con i risultati della richiesta contenuti nel campo dello stato \_ dell'intestazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-2928">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="ea353-2929">Il formato del messaggio CPMUpdateDocumentsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-2929">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-2930">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2930">0</span></span>

<span data-ttu-id="ea353-2931">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2931">1</span></span>

<span data-ttu-id="ea353-2932">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2932">2</span></span>

<span data-ttu-id="ea353-2933">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2933">3</span></span>

<span data-ttu-id="ea353-2934">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2934">4</span></span>

<span data-ttu-id="ea353-2935">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2935">5</span></span>

<span data-ttu-id="ea353-2936">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2936">6</span></span>

<span data-ttu-id="ea353-2937">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2937">7</span></span>

<span data-ttu-id="ea353-2938">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2938">8</span></span>

<span data-ttu-id="ea353-2939">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2939">9</span></span>

<span data-ttu-id="ea353-2940">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2940">1</span></span><br/> <span data-ttu-id="ea353-2941">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2941">0</span></span><br/>

<span data-ttu-id="ea353-2942">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2942">1</span></span>

<span data-ttu-id="ea353-2943">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2943">2</span></span>

<span data-ttu-id="ea353-2944">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2944">3</span></span>

<span data-ttu-id="ea353-2945">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2945">4</span></span>

<span data-ttu-id="ea353-2946">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2946">5</span></span>

<span data-ttu-id="ea353-2947">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2947">6</span></span>

<span data-ttu-id="ea353-2948">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2948">7</span></span>

<span data-ttu-id="ea353-2949">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2949">8</span></span>

<span data-ttu-id="ea353-2950">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2950">9</span></span>

<span data-ttu-id="ea353-2951">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2951">2</span></span><br/> <span data-ttu-id="ea353-2952">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2952">0</span></span><br/>

<span data-ttu-id="ea353-2953">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2953">1</span></span>

<span data-ttu-id="ea353-2954">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2954">2</span></span>

<span data-ttu-id="ea353-2955">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2955">3</span></span>

<span data-ttu-id="ea353-2956">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2956">4</span></span>

<span data-ttu-id="ea353-2957">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2957">5</span></span>

<span data-ttu-id="ea353-2958">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2958">6</span></span>

<span data-ttu-id="ea353-2959">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2959">7</span></span>

<span data-ttu-id="ea353-2960">8</span><span class="sxs-lookup"><span data-stu-id="ea353-2960">8</span></span>

<span data-ttu-id="ea353-2961">9</span><span class="sxs-lookup"><span data-stu-id="ea353-2961">9</span></span>

<span data-ttu-id="ea353-2962">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2962">3</span></span><br/> <span data-ttu-id="ea353-2963">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2963">0</span></span><br/>

<span data-ttu-id="ea353-2964">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2964">1</span></span>

<span data-ttu-id="ea353-2965">\_flag (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2965">\_flag (optional)</span></span>

<span data-ttu-id="ea353-2966">\_fRootPath (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2966">\_fRootPath (optional)</span></span>

<span data-ttu-id="ea353-2967">RootPath (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-2967">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="ea353-2968">**\_ flag**: tipo di aggiornamento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ea353-2968">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="ea353-2969">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-2969">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="ea353-2970">Questo campo DEVE essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-2970">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="ea353-2971">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-2971">Value</span></span>                  | <span data-ttu-id="ea353-2972">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-2972">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ea353-2973">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-2973">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="ea353-2974">È necessario eseguire un aggiornamento incrementale.</span><span class="sxs-lookup"><span data-stu-id="ea353-2974">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="ea353-2975">UPD \_ FULL 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-2975">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="ea353-2976">È necessario eseguire un aggiornamento completo.</span><span class="sxs-lookup"><span data-stu-id="ea353-2976">A full update is to be performed.</span></span>         |
| <span data-ttu-id="ea353-2977">UPD \_ INIT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-2977">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="ea353-2978">Deve essere eseguita una nuova inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-2978">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="ea353-2979">**\_ fRootPath:** valore booleano che indica se il campo RootPath specifica un percorso in cui eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ea353-2979">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="ea353-2980">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-2980">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="ea353-2981">Questo campo DEVE essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-2981">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="ea353-2982">Se impostato su 0x00000001, un percorso in cui eseguire l'aggiornamento viene incluso in RootPath.</span><span class="sxs-lookup"><span data-stu-id="ea353-2982">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="ea353-2983">Se impostato su 0x00000000, l'aggiornamento deve essere eseguito in tutti i percorsi indicizzati.</span><span class="sxs-lookup"><span data-stu-id="ea353-2983">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="ea353-2984">**RootPath:** nome del percorso da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ea353-2984">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="ea353-2985">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-2985">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="ea353-2986">Il nome DEVE essere una stringa Unicode con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="ea353-2986">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="ea353-2987">Questo campo DEVE essere omesso se \_ fRootPath è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-2987">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="ea353-2988">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="ea353-2988">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="ea353-2989">Il messaggio CPMForceMergeIn richiede a un server di eseguire la manutenzione necessaria per migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-2989">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="ea353-2990">Il server risponderà con l'intestazione del messaggio CPMForceMergeIn, con i risultati della richiesta contenuti nel \_ campo dello stato.</span><span class="sxs-lookup"><span data-stu-id="ea353-2990">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="ea353-2991">Il formato del messaggio CPMForceMergeIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-2991">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-2992">0</span><span class="sxs-lookup"><span data-stu-id="ea353-2992">0</span></span>

<span data-ttu-id="ea353-2993">1</span><span class="sxs-lookup"><span data-stu-id="ea353-2993">1</span></span>

<span data-ttu-id="ea353-2994">2</span><span class="sxs-lookup"><span data-stu-id="ea353-2994">2</span></span>

<span data-ttu-id="ea353-2995">3</span><span class="sxs-lookup"><span data-stu-id="ea353-2995">3</span></span>

<span data-ttu-id="ea353-2996">4</span><span class="sxs-lookup"><span data-stu-id="ea353-2996">4</span></span>

<span data-ttu-id="ea353-2997">5</span><span class="sxs-lookup"><span data-stu-id="ea353-2997">5</span></span>

<span data-ttu-id="ea353-2998">6</span><span class="sxs-lookup"><span data-stu-id="ea353-2998">6</span></span>

<span data-ttu-id="ea353-2999">7</span><span class="sxs-lookup"><span data-stu-id="ea353-2999">7</span></span>

<span data-ttu-id="ea353-3000">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3000">8</span></span>

<span data-ttu-id="ea353-3001">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3001">9</span></span>

<span data-ttu-id="ea353-3002">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3002">1</span></span><br/> <span data-ttu-id="ea353-3003">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3003">0</span></span><br/>

<span data-ttu-id="ea353-3004">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3004">1</span></span>

<span data-ttu-id="ea353-3005">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3005">2</span></span>

<span data-ttu-id="ea353-3006">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3006">3</span></span>

<span data-ttu-id="ea353-3007">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3007">4</span></span>

<span data-ttu-id="ea353-3008">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3008">5</span></span>

<span data-ttu-id="ea353-3009">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3009">6</span></span>

<span data-ttu-id="ea353-3010">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3010">7</span></span>

<span data-ttu-id="ea353-3011">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3011">8</span></span>

<span data-ttu-id="ea353-3012">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3012">9</span></span>

<span data-ttu-id="ea353-3013">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3013">2</span></span><br/> <span data-ttu-id="ea353-3014">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3014">0</span></span><br/>

<span data-ttu-id="ea353-3015">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3015">1</span></span>

<span data-ttu-id="ea353-3016">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3016">2</span></span>

<span data-ttu-id="ea353-3017">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3017">3</span></span>

<span data-ttu-id="ea353-3018">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3018">4</span></span>

<span data-ttu-id="ea353-3019">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3019">5</span></span>

<span data-ttu-id="ea353-3020">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3020">6</span></span>

<span data-ttu-id="ea353-3021">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3021">7</span></span>

<span data-ttu-id="ea353-3022">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3022">8</span></span>

<span data-ttu-id="ea353-3023">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3023">9</span></span>

<span data-ttu-id="ea353-3024">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3024">3</span></span><br/> <span data-ttu-id="ea353-3025">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3025">0</span></span><br/>

<span data-ttu-id="ea353-3026">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3026">1</span></span>

<span data-ttu-id="ea353-3027">\_partID (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3027">\_partID (optional)</span></span>



 

<span data-ttu-id="ea353-3028">**\_ partID:** questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3028">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="ea353-3029">Quando questo campo è presente, DEVE essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-3029">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="ea353-3030">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3030">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="ea353-3031">Il messaggio CPMConnectIn avvia una sessione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3031">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="ea353-3032">Il formato del messaggio CPMConnectIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3032">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3033">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3033">0</span></span>

<span data-ttu-id="ea353-3034">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3034">1</span></span>

<span data-ttu-id="ea353-3035">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3035">2</span></span>

<span data-ttu-id="ea353-3036">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3036">3</span></span>

<span data-ttu-id="ea353-3037">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3037">4</span></span>

<span data-ttu-id="ea353-3038">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3038">5</span></span>

<span data-ttu-id="ea353-3039">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3039">6</span></span>

<span data-ttu-id="ea353-3040">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3040">7</span></span>

<span data-ttu-id="ea353-3041">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3041">8</span></span>

<span data-ttu-id="ea353-3042">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3042">9</span></span>

<span data-ttu-id="ea353-3043">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3043">1</span></span><br/> <span data-ttu-id="ea353-3044">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3044">0</span></span><br/>

<span data-ttu-id="ea353-3045">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3045">1</span></span>

<span data-ttu-id="ea353-3046">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3046">2</span></span>

<span data-ttu-id="ea353-3047">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3047">3</span></span>

<span data-ttu-id="ea353-3048">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3048">4</span></span>

<span data-ttu-id="ea353-3049">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3049">5</span></span>

<span data-ttu-id="ea353-3050">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3050">6</span></span>

<span data-ttu-id="ea353-3051">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3051">7</span></span>

<span data-ttu-id="ea353-3052">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3052">8</span></span>

<span data-ttu-id="ea353-3053">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3053">9</span></span>

<span data-ttu-id="ea353-3054">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3054">2</span></span><br/> <span data-ttu-id="ea353-3055">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3055">0</span></span><br/>

<span data-ttu-id="ea353-3056">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3056">1</span></span>

<span data-ttu-id="ea353-3057">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3057">2</span></span>

<span data-ttu-id="ea353-3058">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3058">3</span></span>

<span data-ttu-id="ea353-3059">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3059">4</span></span>

<span data-ttu-id="ea353-3060">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3060">5</span></span>

<span data-ttu-id="ea353-3061">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3061">6</span></span>

<span data-ttu-id="ea353-3062">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3062">7</span></span>

<span data-ttu-id="ea353-3063">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3063">8</span></span>

<span data-ttu-id="ea353-3064">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3064">9</span></span>

<span data-ttu-id="ea353-3065">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3065">3</span></span><br/> <span data-ttu-id="ea353-3066">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3066">0</span></span><br/>

<span data-ttu-id="ea353-3067">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3067">1</span></span>

<span data-ttu-id="ea353-3068">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="ea353-3068">\_iClientVersion</span></span>

<span data-ttu-id="ea353-3069">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="ea353-3069">\_fClientIsRemote</span></span>

<span data-ttu-id="ea353-3070">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="ea353-3070">\_cbBlob1</span></span>

<span data-ttu-id="ea353-3071">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="ea353-3071">\_cbBlob2</span></span>

<span data-ttu-id="ea353-3072">\_Imbottitura</span><span class="sxs-lookup"><span data-stu-id="ea353-3072">\_padding</span></span>

<span data-ttu-id="ea353-3073">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3073">...</span></span>

<span data-ttu-id="ea353-3074">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3074">...</span></span>

<span data-ttu-id="ea353-3075">MachineName</span><span class="sxs-lookup"><span data-stu-id="ea353-3075">MachineName</span></span>

<span data-ttu-id="ea353-3076">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3076">... (variable)</span></span>

<span data-ttu-id="ea353-3077">Nome utente</span><span class="sxs-lookup"><span data-stu-id="ea353-3077">UserName</span></span>

<span data-ttu-id="ea353-3078">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3078">... (variable)</span></span>

<span data-ttu-id="ea353-3079">\_paddingcPropSets (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3079">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="ea353-3080">cPropSets</span><span class="sxs-lookup"><span data-stu-id="ea353-3080">cPropSets</span></span>

<span data-ttu-id="ea353-3081">PropertySet1 (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3081">PropertySet1 (variable)</span></span>

<span data-ttu-id="ea353-3082">PropertySet2 (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3082">PropertySet2 (variable)</span></span>

<span data-ttu-id="ea353-3083">\_paddingExtPropset (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3083">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="ea353-3084">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="ea353-3084">cExtPropSet</span></span>

<span data-ttu-id="ea353-3085">aPropertySets (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3085">aPropertySets (variable)</span></span>



 

<span data-ttu-id="ea353-3086">**\_ iClientVersion:** intero a 32 bit che indica se il server deve convalidare il valore di checksum specificato nel campo ulChecksum delle intestazioni dei messaggi inviati \_ dal client.</span><span class="sxs-lookup"><span data-stu-id="ea353-3086">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="ea353-3087">Se il campo iClientVersion è impostato su 0x00000008 o versione successiva, il server DEVE convalidare il valore del campo \_ \_ ulChecksum per i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-3087">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="ea353-3088">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3088">CPMConnectIn</span></span>
-   <span data-ttu-id="ea353-3089">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3089">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="ea353-3090">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3090">CPMFetchValueIn</span></span>
-   <span data-ttu-id="ea353-3091">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3091">CPMGetRowsIn</span></span>
-   <span data-ttu-id="ea353-3092">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3092">CPMSetBindingsIn</span></span>

<span data-ttu-id="ea353-3093">Per informazioni dettagliate sul modo in cui il server convalida il valore specificato dal client nel campo ulChecksum per i messaggi elencati in precedenza, vedere La sezione 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="ea353-3093">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="ea353-3094">Se il valore è maggiore 0x00000008, si presuppone che il client sia in grado di gestire offset a 64 bit nei messaggi CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-3094">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="ea353-3095">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="ea353-3095">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="ea353-3096">*Comportamento di Windows: nei client Windows, iClientVersion è impostato come segue:*</span><span class="sxs-lookup"><span data-stu-id="ea353-3096">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="ea353-3097">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-3097">Value</span></span>      | <span data-ttu-id="ea353-3098">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-3098">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="ea353-3099">0x00000005</span><span class="sxs-lookup"><span data-stu-id="ea353-3099">0x00000005</span></span> | <span data-ttu-id="ea353-3100">Il sistema operativo client è Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ea353-3100">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="ea353-3101">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea353-3101">0x00000008</span></span> | <span data-ttu-id="ea353-3102">Il sistema operativo client è Windows XP a 32 bit o Windows Server 2003 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-3102">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="ea353-3103">0x00010008</span><span class="sxs-lookup"><span data-stu-id="ea353-3103">0x00010008</span></span> | <span data-ttu-id="ea353-3104">Il sistema operativo client è Windows XP a 64 bit o Windows Server 2003 a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-3104">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="ea353-3105">\_**fClientIsRemote:** valore booleano che indica se il client è in esecuzione in un computer diverso dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3105">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="ea353-3106">DEVE essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-3106">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="ea353-3107">\_**cbBlob1:** intero senza segno a 32 bit che indica le dimensioni in byte dei campi cPropSet, PropertySet1 e PropertySet2 combinati.</span><span class="sxs-lookup"><span data-stu-id="ea353-3107">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="ea353-3108">\_**cbBlob2:** intero senza segno a 32 bit che indica le dimensioni in byte dei campi cExPropSet e aPropertySet, combinati.</span><span class="sxs-lookup"><span data-stu-id="ea353-3108">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="ea353-3109">\_**padding:** 12 byte di spaziatura interna che possono contenere valori arbitrari e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-3109">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="ea353-3110">**MachineName:** nome del computer del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-3110">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="ea353-3111">La stringa del nome DEVE essere una matrice con terminazione Null di meno di 512 caratteri Unicode, incluso il carattere di terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="ea353-3111">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="ea353-3112">**UserName:** stringa che rappresenta il nome utente della persona che esegue l'applicazione che ha richiamato questo protocollo.</span><span class="sxs-lookup"><span data-stu-id="ea353-3112">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="ea353-3113">La stringa del nome DEVE essere una matrice con terminazione Null di meno di 512 caratteri Unicode se concatenata con MachineName.</span><span class="sxs-lookup"><span data-stu-id="ea353-3113">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="ea353-3114">**\_ paddingcPropSets:** questo campo DEVE avere una lunghezza da 0 a 7 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-3114">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="ea353-3115">Il numero di byte DEVE essere il numero necessario per rendere l'offset in byte del campo cPropSets dall'inizio del messaggio che contiene questa struttura è un multiplo di 8.</span><span class="sxs-lookup"><span data-stu-id="ea353-3115">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="ea353-3116">Il valore dei byte può essere qualsiasi valore arbitrario e DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-3116">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-3117">**cPropSets:** intero senza segno a 32 bit che indica il numero di strutture CDbPropSet che segue questo campo.</span><span class="sxs-lookup"><span data-stu-id="ea353-3117">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="ea353-3118">Questo valore DEVE essere impostato su 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="ea353-3118">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="ea353-3119">**PropertySet1:** struttura CDbPropSet con guidPropertySet contenente DBPROPSET \_ FSCIFRMWRK EXT (vedere la sezione \_ 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="ea353-3119">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="ea353-3120">**PropertySet2:** struttura CDbPropSet con guidPropertySet contenente DBPROPSET \_ CIFRMWRKCORE EXT (vedere la sezione \_ 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="ea353-3120">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="ea353-3121">\_**PaddingExtPropset:** questo campo DEVE avere una lunghezza da 0 a 7 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-3121">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="ea353-3122">Il numero di byte DEVE essere il numero necessario per rendere l'offset in byte del campo cExtPropSets dall'inizio del messaggio che contiene questa struttura è un multiplo di 8.</span><span class="sxs-lookup"><span data-stu-id="ea353-3122">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="ea353-3123">Il valore dei byte può essere qualsiasi valore arbitrario e DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-3123">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-3124">**cExtPropSet:** intero senza segno a 32 bit che indica il numero di strutture CDbPropSet che segue questo campo.</span><span class="sxs-lookup"><span data-stu-id="ea353-3124">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="ea353-3125">**aPropertySets:** matrice di strutture CDbPropSet che specificano altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-3125">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="ea353-3126">Il numero di elementi in questa matrice DEVE essere uguale a cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="ea353-3126">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="ea353-3127">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="ea353-3127">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="ea353-3128">Il messaggio CPMConnectOut contiene una risposta a un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-3128">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="ea353-3129">Il formato del messaggio CPMConnectOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3129">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-3130">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3130">0</span></span>

<span data-ttu-id="ea353-3131">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3131">1</span></span>

<span data-ttu-id="ea353-3132">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3132">2</span></span>

<span data-ttu-id="ea353-3133">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3133">3</span></span>

<span data-ttu-id="ea353-3134">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3134">4</span></span>

<span data-ttu-id="ea353-3135">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3135">5</span></span>

<span data-ttu-id="ea353-3136">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3136">6</span></span>

<span data-ttu-id="ea353-3137">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3137">7</span></span>

<span data-ttu-id="ea353-3138">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3138">8</span></span>

<span data-ttu-id="ea353-3139">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3139">9</span></span>

<span data-ttu-id="ea353-3140">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3140">1</span></span><br/> <span data-ttu-id="ea353-3141">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3141">0</span></span><br/>

<span data-ttu-id="ea353-3142">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3142">1</span></span>

<span data-ttu-id="ea353-3143">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3143">2</span></span>

<span data-ttu-id="ea353-3144">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3144">3</span></span>

<span data-ttu-id="ea353-3145">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3145">4</span></span>

<span data-ttu-id="ea353-3146">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3146">5</span></span>

<span data-ttu-id="ea353-3147">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3147">6</span></span>

<span data-ttu-id="ea353-3148">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3148">7</span></span>

<span data-ttu-id="ea353-3149">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3149">8</span></span>

<span data-ttu-id="ea353-3150">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3150">9</span></span>

<span data-ttu-id="ea353-3151">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3151">2</span></span><br/> <span data-ttu-id="ea353-3152">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3152">0</span></span><br/>

<span data-ttu-id="ea353-3153">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3153">1</span></span>

<span data-ttu-id="ea353-3154">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3154">2</span></span>

<span data-ttu-id="ea353-3155">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3155">3</span></span>

<span data-ttu-id="ea353-3156">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3156">4</span></span>

<span data-ttu-id="ea353-3157">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3157">5</span></span>

<span data-ttu-id="ea353-3158">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3158">6</span></span>

<span data-ttu-id="ea353-3159">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3159">7</span></span>

<span data-ttu-id="ea353-3160">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3160">8</span></span>

<span data-ttu-id="ea353-3161">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3161">9</span></span>

<span data-ttu-id="ea353-3162">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3162">3</span></span><br/> <span data-ttu-id="ea353-3163">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3163">0</span></span><br/>

<span data-ttu-id="ea353-3164">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3164">1</span></span>

<span data-ttu-id="ea353-3165">\_Serverversion</span><span class="sxs-lookup"><span data-stu-id="ea353-3165">\_serverVersion</span></span>

<span data-ttu-id="ea353-3166">\_reserved (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3166">\_reserved (variable)</span></span>



 

<span data-ttu-id="ea353-3167">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="ea353-3167">**\_serverVersion**:</span></span>

<span data-ttu-id="ea353-3168">Intero a 32 bit che indica se il server può supportare offset a 64 *bit.*</span><span class="sxs-lookup"><span data-stu-id="ea353-3168">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="ea353-3169">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="ea353-3169">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="ea353-3170">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-3170">Value</span></span>      | <span data-ttu-id="ea353-3171">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-3171">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="ea353-3172">0x00000007</span><span class="sxs-lookup"><span data-stu-id="ea353-3172">0x00000007</span></span> | <span data-ttu-id="ea353-3173">Il server può inviare solo offset a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-3173">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="ea353-3174">0x00010007</span><span class="sxs-lookup"><span data-stu-id="ea353-3174">0x00010007</span></span> | <span data-ttu-id="ea353-3175">Il server può inviare offset a 32 o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-3175">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="ea353-3176">**\_ reserved**: riservato.</span><span class="sxs-lookup"><span data-stu-id="ea353-3176">**\_reserved**: Reserved.</span></span> <span data-ttu-id="ea353-3177">Il server PUÒ inviare un numero arbitrario di valori arbitrari e il client DEVE ignorare questi valori, se presenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-3177">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="ea353-3178">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3178">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="ea353-3179">Il messaggio CPMCreateQueryIn crea una nuova query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3179">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="ea353-3180">Il formato del messaggio CPMCreateQueryIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3180">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3181">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3181">0</span></span>

<span data-ttu-id="ea353-3182">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3182">1</span></span>

<span data-ttu-id="ea353-3183">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3183">2</span></span>

<span data-ttu-id="ea353-3184">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3184">3</span></span>

<span data-ttu-id="ea353-3185">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3185">4</span></span>

<span data-ttu-id="ea353-3186">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3186">5</span></span>

<span data-ttu-id="ea353-3187">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3187">6</span></span>

<span data-ttu-id="ea353-3188">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3188">7</span></span>

<span data-ttu-id="ea353-3189">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3189">8</span></span>

<span data-ttu-id="ea353-3190">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3190">9</span></span>

<span data-ttu-id="ea353-3191">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3191">1</span></span><br/> <span data-ttu-id="ea353-3192">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3192">0</span></span><br/>

<span data-ttu-id="ea353-3193">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3193">1</span></span>

<span data-ttu-id="ea353-3194">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3194">2</span></span>

<span data-ttu-id="ea353-3195">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3195">3</span></span>

<span data-ttu-id="ea353-3196">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3196">4</span></span>

<span data-ttu-id="ea353-3197">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3197">5</span></span>

<span data-ttu-id="ea353-3198">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3198">6</span></span>

<span data-ttu-id="ea353-3199">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3199">7</span></span>

<span data-ttu-id="ea353-3200">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3200">8</span></span>

<span data-ttu-id="ea353-3201">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3201">9</span></span>

<span data-ttu-id="ea353-3202">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3202">2</span></span><br/> <span data-ttu-id="ea353-3203">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3203">0</span></span><br/>

<span data-ttu-id="ea353-3204">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3204">1</span></span>

<span data-ttu-id="ea353-3205">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3205">2</span></span>

<span data-ttu-id="ea353-3206">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3206">3</span></span>

<span data-ttu-id="ea353-3207">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3207">4</span></span>

<span data-ttu-id="ea353-3208">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3208">5</span></span>

<span data-ttu-id="ea353-3209">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3209">6</span></span>

<span data-ttu-id="ea353-3210">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3210">7</span></span>

<span data-ttu-id="ea353-3211">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3211">8</span></span>

<span data-ttu-id="ea353-3212">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3212">9</span></span>

<span data-ttu-id="ea353-3213">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3213">3</span></span><br/> <span data-ttu-id="ea353-3214">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3214">0</span></span><br/>

<span data-ttu-id="ea353-3215">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3215">1</span></span>

<span data-ttu-id="ea353-3216">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ea353-3216">Size</span></span>

<span data-ttu-id="ea353-3217">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="ea353-3217">CColumnSetPresent</span></span>

<span data-ttu-id="ea353-3218">ColumnSet (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3218">ColumnSet (optional)</span></span>

<span data-ttu-id="ea353-3219">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3219">... (variable)</span></span>

<span data-ttu-id="ea353-3220">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="ea353-3220">CRestrictionPresent.</span></span>

<span data-ttu-id="ea353-3221">Restrizione (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3221">Restriction (optional)</span></span>

<span data-ttu-id="ea353-3222">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3222">... (variable)</span></span>

<span data-ttu-id="ea353-3223">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="ea353-3223">CSortSetPresent</span></span>

<span data-ttu-id="ea353-3224">SortSet (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3224">SortSet (optional)</span></span>

<span data-ttu-id="ea353-3225">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3225">... (variable)</span></span>

<span data-ttu-id="ea353-3226">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="ea353-3226">CCategorizationSetPresent</span></span>

<span data-ttu-id="ea353-3227">CategorizationSet (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3227">CategorizationSet (optional)</span></span>

<span data-ttu-id="ea353-3228">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3228">... (variable)</span></span>

<span data-ttu-id="ea353-3229">Proprietà RowSet</span><span class="sxs-lookup"><span data-stu-id="ea353-3229">RowSetProperties</span></span>

<span data-ttu-id="ea353-3230">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3230">...</span></span>

<span data-ttu-id="ea353-3231">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3231">...</span></span>

<span data-ttu-id="ea353-3232">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3232">...</span></span>

<span data-ttu-id="ea353-3233">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3233">...</span></span>

<span data-ttu-id="ea353-3234">PidMapper (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3234">PidMapper (variable)</span></span>



 

<span data-ttu-id="ea353-3235">**Size:** intero senza segno a 32 bit che indica il numero di byte dall'inizio di questo campo alla fine del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-3235">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="ea353-3236">**CColumnSetPresent:** campo byte che indica se il campo ColumnSet è presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3236">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="ea353-3237">Questo campo DEVE essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-3237">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="ea353-3238">Se impostato su 0x01 il campo CColumnSet DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3238">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="ea353-3239">Se impostato su 0x00, DEVE essere assente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3239">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="ea353-3240">**ColumnSet:** struttura CColumnSet contenente i numeri di colonna in cui devono essere restituite le proprietà di CPidMapper.</span><span class="sxs-lookup"><span data-stu-id="ea353-3240">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="ea353-3241">**CRestrictionPresent:** campo byte che indica se il campo Restriction è presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3241">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="ea353-3242">Se impostato su un valore diverso da zero, il campo Restriction deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3242">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="ea353-3243">Se impostato su 0x00, Restriction DEVE essere assente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3243">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="ea353-3244">**Restrizione:** struttura CRestriction contenente l'albero dei comandi della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3244">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="ea353-3245">**CSortSetPresent:** campo byte che indica se il campo SortSet è presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3245">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="ea353-3246">Se impostato su un valore diverso da zero, il campo SortSet DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3246">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="ea353-3247">Se impostato su 0x00, SortSet DEVE essere assente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3247">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="ea353-3248">**SortSet:** struttura CSortSet che indica l'ordinamento della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3248">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="ea353-3249">**CCategorizationSetPresent:** campo byte che indica se il campo CCategorizationSet è presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3249">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="ea353-3250">Se impostato su un valore diverso da zero, il campo CCategorizationSet DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3250">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="ea353-3251">Se impostato su 0x00, CCategorizationSet DEVE essere assente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3251">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="ea353-3252">**CCategorizationSet:** struttura CCategorizationSet che contiene i gruppi per la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3252">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="ea353-3253">**RowSetProperties:** struttura CRowsetProperties che fornisce informazioni di configurazione per la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3253">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="ea353-3254">**PidMapper:** struttura CPidMapper contenente le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3254">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="ea353-3255">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="ea353-3255">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="ea353-3256">Il messaggio CPMCreateQueryOut contiene una risposta a un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-3256">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="ea353-3257">Il formato del messaggio CPMCreateQueryOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3257">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-3258">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3258">0</span></span>

<span data-ttu-id="ea353-3259">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3259">1</span></span>

<span data-ttu-id="ea353-3260">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3260">2</span></span>

<span data-ttu-id="ea353-3261">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3261">3</span></span>

<span data-ttu-id="ea353-3262">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3262">4</span></span>

<span data-ttu-id="ea353-3263">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3263">5</span></span>

<span data-ttu-id="ea353-3264">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3264">6</span></span>

<span data-ttu-id="ea353-3265">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3265">7</span></span>

<span data-ttu-id="ea353-3266">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3266">8</span></span>

<span data-ttu-id="ea353-3267">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3267">9</span></span>

<span data-ttu-id="ea353-3268">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3268">1</span></span><br/> <span data-ttu-id="ea353-3269">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3269">0</span></span><br/>

<span data-ttu-id="ea353-3270">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3270">1</span></span>

<span data-ttu-id="ea353-3271">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3271">2</span></span>

<span data-ttu-id="ea353-3272">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3272">3</span></span>

<span data-ttu-id="ea353-3273">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3273">4</span></span>

<span data-ttu-id="ea353-3274">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3274">5</span></span>

<span data-ttu-id="ea353-3275">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3275">6</span></span>

<span data-ttu-id="ea353-3276">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3276">7</span></span>

<span data-ttu-id="ea353-3277">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3277">8</span></span>

<span data-ttu-id="ea353-3278">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3278">9</span></span>

<span data-ttu-id="ea353-3279">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3279">2</span></span><br/> <span data-ttu-id="ea353-3280">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3280">0</span></span><br/>

<span data-ttu-id="ea353-3281">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3281">1</span></span>

<span data-ttu-id="ea353-3282">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3282">2</span></span>

<span data-ttu-id="ea353-3283">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3283">3</span></span>

<span data-ttu-id="ea353-3284">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3284">4</span></span>

<span data-ttu-id="ea353-3285">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3285">5</span></span>

<span data-ttu-id="ea353-3286">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3286">6</span></span>

<span data-ttu-id="ea353-3287">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3287">7</span></span>

<span data-ttu-id="ea353-3288">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3288">8</span></span>

<span data-ttu-id="ea353-3289">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3289">9</span></span>

<span data-ttu-id="ea353-3290">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3290">3</span></span><br/> <span data-ttu-id="ea353-3291">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3291">0</span></span><br/>

<span data-ttu-id="ea353-3292">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3292">1</span></span>

<span data-ttu-id="ea353-3293">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="ea353-3293">\_fTrueSequential</span></span>

<span data-ttu-id="ea353-3294">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="ea353-3294">\_fWorkIdUnique</span></span>

<span data-ttu-id="ea353-3295">aCursors</span><span class="sxs-lookup"><span data-stu-id="ea353-3295">aCursors</span></span>



 

<span data-ttu-id="ea353-3296">**\_ fTrueSequential:** valore booleano informativo che indica se è possibile che la query fornisca risultati più velocemente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3296">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="ea353-3297">Se impostato su 0x00000001 per la query fornita in CPMCreateQueryIn, il server può usare l'indice in modo che i risultati della query possano essere recapitati più velocemente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3297">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="ea353-3298">Se impostato su 0x00000000, si verifica una latenza maggiore nel recapito dei risultati delle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3298">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="ea353-3299">NON DEVE essere impostato su nessun altro valore.</span><span class="sxs-lookup"><span data-stu-id="ea353-3299">MUST not be set to any other value.</span></span>

<span data-ttu-id="ea353-3300">**\_ fWorkIdUnique:** valore booleano che indica se gli identificatori di documento a cui puntano i cursori sono univoci in tutti i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3300">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="ea353-3301">Se impostato su 0x00000001, gli identificatori sono univoci.</span><span class="sxs-lookup"><span data-stu-id="ea353-3301">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="ea353-3302">Se impostato su 0x00000000, sono univoci solo in tutto il set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3302">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="ea353-3303">**aCursors:** matrice di interi senza segno a 32 bit che rappresentano gli handle ai cursori, con il numero di elementi uguale al numero di categorie nel campo CategorizationSet del messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-3303">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="ea353-3304">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3304">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="ea353-3305">Il messaggio CPMGetQueryStatusIn richiede lo stato di una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3305">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="ea353-3306">Il formato del messaggio CPMGetQueryStatusIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3306">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3307">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3307">0</span></span>

<span data-ttu-id="ea353-3308">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3308">1</span></span>

<span data-ttu-id="ea353-3309">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3309">2</span></span>

<span data-ttu-id="ea353-3310">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3310">3</span></span>

<span data-ttu-id="ea353-3311">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3311">4</span></span>

<span data-ttu-id="ea353-3312">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3312">5</span></span>

<span data-ttu-id="ea353-3313">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3313">6</span></span>

<span data-ttu-id="ea353-3314">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3314">7</span></span>

<span data-ttu-id="ea353-3315">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3315">8</span></span>

<span data-ttu-id="ea353-3316">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3316">9</span></span>

<span data-ttu-id="ea353-3317">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3317">1</span></span><br/> <span data-ttu-id="ea353-3318">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3318">0</span></span><br/>

<span data-ttu-id="ea353-3319">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3319">1</span></span>

<span data-ttu-id="ea353-3320">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3320">2</span></span>

<span data-ttu-id="ea353-3321">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3321">3</span></span>

<span data-ttu-id="ea353-3322">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3322">4</span></span>

<span data-ttu-id="ea353-3323">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3323">5</span></span>

<span data-ttu-id="ea353-3324">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3324">6</span></span>

<span data-ttu-id="ea353-3325">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3325">7</span></span>

<span data-ttu-id="ea353-3326">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3326">8</span></span>

<span data-ttu-id="ea353-3327">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3327">9</span></span>

<span data-ttu-id="ea353-3328">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3328">2</span></span><br/> <span data-ttu-id="ea353-3329">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3329">0</span></span><br/>

<span data-ttu-id="ea353-3330">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3330">1</span></span>

<span data-ttu-id="ea353-3331">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3331">2</span></span>

<span data-ttu-id="ea353-3332">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3332">3</span></span>

<span data-ttu-id="ea353-3333">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3333">4</span></span>

<span data-ttu-id="ea353-3334">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3334">5</span></span>

<span data-ttu-id="ea353-3335">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3335">6</span></span>

<span data-ttu-id="ea353-3336">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3336">7</span></span>

<span data-ttu-id="ea353-3337">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3337">8</span></span>

<span data-ttu-id="ea353-3338">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3338">9</span></span>

<span data-ttu-id="ea353-3339">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3339">3</span></span><br/> <span data-ttu-id="ea353-3340">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3340">0</span></span><br/>

<span data-ttu-id="ea353-3341">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3341">1</span></span>

<span data-ttu-id="ea353-3342">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="ea353-3342">\_hCursor</span></span>



 

<span data-ttu-id="ea353-3343">**\_ hCursor:** intero senza segno a 32 bit che rappresenta l'handle dal messaggio CPMCreateQueryOut che identifica la query per cui recuperare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="ea353-3343">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="ea353-3344">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="ea353-3344">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="ea353-3345">Il messaggio CPMGetQueryStatusOut risponde a un messaggio CPMGetQueryStatusIn con lo stato della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3345">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="ea353-3346">Il formato del messaggio CPMGetQueryStatusOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3346">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-3347">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3347">0</span></span>

<span data-ttu-id="ea353-3348">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3348">1</span></span>

<span data-ttu-id="ea353-3349">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3349">2</span></span>

<span data-ttu-id="ea353-3350">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3350">3</span></span>

<span data-ttu-id="ea353-3351">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3351">4</span></span>

<span data-ttu-id="ea353-3352">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3352">5</span></span>

<span data-ttu-id="ea353-3353">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3353">6</span></span>

<span data-ttu-id="ea353-3354">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3354">7</span></span>

<span data-ttu-id="ea353-3355">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3355">8</span></span>

<span data-ttu-id="ea353-3356">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3356">9</span></span>

<span data-ttu-id="ea353-3357">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3357">1</span></span><br/> <span data-ttu-id="ea353-3358">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3358">0</span></span><br/>

<span data-ttu-id="ea353-3359">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3359">1</span></span>

<span data-ttu-id="ea353-3360">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3360">2</span></span>

<span data-ttu-id="ea353-3361">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3361">3</span></span>

<span data-ttu-id="ea353-3362">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3362">4</span></span>

<span data-ttu-id="ea353-3363">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3363">5</span></span>

<span data-ttu-id="ea353-3364">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3364">6</span></span>

<span data-ttu-id="ea353-3365">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3365">7</span></span>

<span data-ttu-id="ea353-3366">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3366">8</span></span>

<span data-ttu-id="ea353-3367">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3367">9</span></span>

<span data-ttu-id="ea353-3368">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3368">2</span></span><br/> <span data-ttu-id="ea353-3369">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3369">0</span></span><br/>

<span data-ttu-id="ea353-3370">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3370">1</span></span>

<span data-ttu-id="ea353-3371">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3371">2</span></span>

<span data-ttu-id="ea353-3372">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3372">3</span></span>

<span data-ttu-id="ea353-3373">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3373">4</span></span>

<span data-ttu-id="ea353-3374">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3374">5</span></span>

<span data-ttu-id="ea353-3375">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3375">6</span></span>

<span data-ttu-id="ea353-3376">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3376">7</span></span>

<span data-ttu-id="ea353-3377">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3377">8</span></span>

<span data-ttu-id="ea353-3378">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3378">9</span></span>

<span data-ttu-id="ea353-3379">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3379">3</span></span><br/> <span data-ttu-id="ea353-3380">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3380">0</span></span><br/>

<span data-ttu-id="ea353-3381">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3381">1</span></span>

<span data-ttu-id="ea353-3382">\_Stato</span><span class="sxs-lookup"><span data-stu-id="ea353-3382">\_Status</span></span>



 

<span data-ttu-id="ea353-3383">**\_ Stato:** maschera di bit dei valori definiti nelle tabelle seguenti, che descrive la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3383">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="ea353-3384">Nella tabella seguente sono elencati i \_ \* valori STAT ottenuti eseguendo un'operazione AND bit per bit \_ su Status con 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="ea353-3384">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="ea353-3385">Il risultato DEVE essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-3385">The result MUST be one of the following:</span></span>



| <span data-ttu-id="ea353-3386">Costante</span><span class="sxs-lookup"><span data-stu-id="ea353-3386">Constant</span></span>                 | <span data-ttu-id="ea353-3387">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-3387">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-3388">STAT \_ BUSY 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-3388">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="ea353-3389">La query asincrona è ancora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ea353-3389">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="ea353-3390">Errore STAT \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-3390">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="ea353-3391">La query è in uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-3391">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="ea353-3392">STAT \_ DONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-3392">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="ea353-3393">La query è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ea353-3393">The query is complete.</span></span>                                                            |
| <span data-ttu-id="ea353-3394">Aggiornamento STAT \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-3394">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="ea353-3395">La query è stata completata, ma gli aggiornamenti hanno come risultato un calcolo aggiuntivo delle query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3395">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="ea353-3396">Nella tabella seguente sono elencati i bit STAT \_ \* aggiuntivi che possono essere impostati in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3396">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="ea353-3397">Costante</span><span class="sxs-lookup"><span data-stu-id="ea353-3397">Constant</span></span>                                    | <span data-ttu-id="ea353-3398">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-3398">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea353-3399">STAT \_ NOISE \_ WORDS 0x00000010</span><span class="sxs-lookup"><span data-stu-id="ea353-3399">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="ea353-3400">Le parole non consentite sono state sostituite da caratteri jolly nella query sul contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea353-3400">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="ea353-3401">CONTENUTO \_ STAT \_ \_ NON AGGIORNATO \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="ea353-3401">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="ea353-3402">I risultati della query potrebbero non essere corretti perché la query ha modificato, ma non indicizzato, i file.</span><span class="sxs-lookup"><span data-stu-id="ea353-3402">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="ea353-3403">AGGIORNAMENTO STAT \_ \_ INCOMPLETO 0x00000040</span><span class="sxs-lookup"><span data-stu-id="ea353-3403">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="ea353-3404">I risultati della query potrebbero non essere corretti perché la query ha modificato e indicizzato nuovamente i file il cui contenuto non è stato incluso.</span><span class="sxs-lookup"><span data-stu-id="ea353-3404">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="ea353-3405">STAT \_ CONTENT \_ QUERY \_ INCOMPLETE 0x00000080</span><span class="sxs-lookup"><span data-stu-id="ea353-3405">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="ea353-3406">La query sul contenuto era troppo complessa per essere completata o richiedeva l'enumerazione invece di usare l'indice di contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea353-3406">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="ea353-3407">LIMITE DI \_ TEMPO \_ STAT \_ SUPERATO 0X00000100</span><span class="sxs-lookup"><span data-stu-id="ea353-3407">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="ea353-3408">I risultati della query potrebbero non essere corretti perché il tempo di esecuzione della query ha raggiunto il tempo massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="ea353-3408">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="ea353-3409">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3409">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="ea353-3410">Il messaggio CPMGetQueryStatusExIn richiede lo stato di una query e informazioni aggiuntive, ad esempio il numero di documenti indicizzati, il numero di documenti rimanenti da indicizzare e così via.</span><span class="sxs-lookup"><span data-stu-id="ea353-3410">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="ea353-3411">Il formato del messaggio CPMGetQueryStatusExIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3411">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3412">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3412">0</span></span>

<span data-ttu-id="ea353-3413">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3413">1</span></span>

<span data-ttu-id="ea353-3414">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3414">2</span></span>

<span data-ttu-id="ea353-3415">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3415">3</span></span>

<span data-ttu-id="ea353-3416">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3416">4</span></span>

<span data-ttu-id="ea353-3417">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3417">5</span></span>

<span data-ttu-id="ea353-3418">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3418">6</span></span>

<span data-ttu-id="ea353-3419">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3419">7</span></span>

<span data-ttu-id="ea353-3420">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3420">8</span></span>

<span data-ttu-id="ea353-3421">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3421">9</span></span>

<span data-ttu-id="ea353-3422">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3422">1</span></span><br/> <span data-ttu-id="ea353-3423">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3423">0</span></span><br/>

<span data-ttu-id="ea353-3424">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3424">1</span></span>

<span data-ttu-id="ea353-3425">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3425">2</span></span>

<span data-ttu-id="ea353-3426">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3426">3</span></span>

<span data-ttu-id="ea353-3427">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3427">4</span></span>

<span data-ttu-id="ea353-3428">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3428">5</span></span>

<span data-ttu-id="ea353-3429">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3429">6</span></span>

<span data-ttu-id="ea353-3430">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3430">7</span></span>

<span data-ttu-id="ea353-3431">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3431">8</span></span>

<span data-ttu-id="ea353-3432">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3432">9</span></span>

<span data-ttu-id="ea353-3433">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3433">2</span></span><br/> <span data-ttu-id="ea353-3434">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3434">0</span></span><br/>

<span data-ttu-id="ea353-3435">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3435">1</span></span>

<span data-ttu-id="ea353-3436">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3436">2</span></span>

<span data-ttu-id="ea353-3437">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3437">3</span></span>

<span data-ttu-id="ea353-3438">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3438">4</span></span>

<span data-ttu-id="ea353-3439">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3439">5</span></span>

<span data-ttu-id="ea353-3440">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3440">6</span></span>

<span data-ttu-id="ea353-3441">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3441">7</span></span>

<span data-ttu-id="ea353-3442">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3442">8</span></span>

<span data-ttu-id="ea353-3443">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3443">9</span></span>

<span data-ttu-id="ea353-3444">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3444">3</span></span><br/> <span data-ttu-id="ea353-3445">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3445">0</span></span><br/>

<span data-ttu-id="ea353-3446">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3446">1</span></span>

<span data-ttu-id="ea353-3447">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="ea353-3447">\_hCursor</span></span>

<span data-ttu-id="ea353-3448">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="ea353-3448">\_bmk</span></span>



 

<span data-ttu-id="ea353-3449">**\_ hCursor:** valore a 32 bit che rappresenta l'handle dal messaggio CPMCreateQueryOut che identifica la query per cui recuperare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="ea353-3449">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="ea353-3450">**\_ bmk:** valore a 32 bit che indica l'handle di un segnalibro di cui recuperare la posizione.</span><span class="sxs-lookup"><span data-stu-id="ea353-3450">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="ea353-3451">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="ea353-3451">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="ea353-3452">Il messaggio CPMGetQueryStatusExOut risponde a un messaggio CPMGetQueryStatusExIn con lo stato della query e altre informazioni sullo stato, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3452">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="ea353-3453">Il formato del messaggio CPMGetQueryStatusExOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3453">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-3454">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3454">0</span></span>

<span data-ttu-id="ea353-3455">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3455">1</span></span>

<span data-ttu-id="ea353-3456">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3456">2</span></span>

<span data-ttu-id="ea353-3457">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3457">3</span></span>

<span data-ttu-id="ea353-3458">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3458">4</span></span>

<span data-ttu-id="ea353-3459">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3459">5</span></span>

<span data-ttu-id="ea353-3460">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3460">6</span></span>

<span data-ttu-id="ea353-3461">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3461">7</span></span>

<span data-ttu-id="ea353-3462">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3462">8</span></span>

<span data-ttu-id="ea353-3463">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3463">9</span></span>

<span data-ttu-id="ea353-3464">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3464">1</span></span><br/> <span data-ttu-id="ea353-3465">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3465">0</span></span><br/>

<span data-ttu-id="ea353-3466">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3466">1</span></span>

<span data-ttu-id="ea353-3467">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3467">2</span></span>

<span data-ttu-id="ea353-3468">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3468">3</span></span>

<span data-ttu-id="ea353-3469">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3469">4</span></span>

<span data-ttu-id="ea353-3470">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3470">5</span></span>

<span data-ttu-id="ea353-3471">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3471">6</span></span>

<span data-ttu-id="ea353-3472">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3472">7</span></span>

<span data-ttu-id="ea353-3473">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3473">8</span></span>

<span data-ttu-id="ea353-3474">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3474">9</span></span>

<span data-ttu-id="ea353-3475">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3475">2</span></span><br/> <span data-ttu-id="ea353-3476">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3476">0</span></span><br/>

<span data-ttu-id="ea353-3477">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3477">1</span></span>

<span data-ttu-id="ea353-3478">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3478">2</span></span>

<span data-ttu-id="ea353-3479">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3479">3</span></span>

<span data-ttu-id="ea353-3480">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3480">4</span></span>

<span data-ttu-id="ea353-3481">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3481">5</span></span>

<span data-ttu-id="ea353-3482">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3482">6</span></span>

<span data-ttu-id="ea353-3483">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3483">7</span></span>

<span data-ttu-id="ea353-3484">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3484">8</span></span>

<span data-ttu-id="ea353-3485">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3485">9</span></span>

<span data-ttu-id="ea353-3486">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3486">3</span></span><br/> <span data-ttu-id="ea353-3487">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3487">0</span></span><br/>

<span data-ttu-id="ea353-3488">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3488">1</span></span>

<span data-ttu-id="ea353-3489">\_Stato</span><span class="sxs-lookup"><span data-stu-id="ea353-3489">\_Status</span></span>

<span data-ttu-id="ea353-3490">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="ea353-3490">\_cFilteredDocuments</span></span>

<span data-ttu-id="ea353-3491">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="ea353-3491">\_cDocumentsToFilter</span></span>

<span data-ttu-id="ea353-3492">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="ea353-3492">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="ea353-3493">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="ea353-3493">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="ea353-3494">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="ea353-3494">\_iRowBmk</span></span>

<span data-ttu-id="ea353-3495">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="ea353-3495">\_cRowsTotal</span></span>



 

<span data-ttu-id="ea353-3496">**\_ Stato:** uno dei dati STAT \_ \* i valori specificati nella sezione 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="ea353-3496">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="ea353-3497">**\_ cFilteredDocuments:** intero senza segno a 32 bit che indica il numero di documenti indicizzati</span><span class="sxs-lookup"><span data-stu-id="ea353-3497">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="ea353-3498">**\_ cDocumentsToFilter:** intero senza segno a 32 bit che indica il numero di documenti ancora da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="ea353-3498">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="ea353-3499">**\_ dwRatioFinishedDenominator:** intero senza segno a 32 bit che indica il denominatore del rapporto tra i documenti che la query ha completato l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-3499">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="ea353-3500">**\_ dwRatioFinishedNumerator:** intero senza segno a 32 bit che indica il numeratore del rapporto tra i documenti che la query ha completato l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-3500">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="ea353-3501">**\_ iRowBmk:** intero senza segno a 32 bit che indica la posizione approssimativa del segnalibro nel set di righe in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3501">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="ea353-3502">**\_ cRowsTotal:** intero senza segno a 32 bit che specifica il numero totale di righe nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3502">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="ea353-3503">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3503">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="ea353-3504">Il messaggio CPMSetBindingsIn richiede l'associazione di colonne a un set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3504">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="ea353-3505">Il server risponderà al messaggio di richiesta CPMSetBindingsIn usando la sezione di intestazione del messaggio CPMBindingsIn con i risultati della richiesta contenuta nel campo \_ status.</span><span class="sxs-lookup"><span data-stu-id="ea353-3505">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="ea353-3506">Il formato del messaggio CPMSetBindingsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3506">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3507">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3507">0</span></span>

<span data-ttu-id="ea353-3508">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3508">1</span></span>

<span data-ttu-id="ea353-3509">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3509">2</span></span>

<span data-ttu-id="ea353-3510">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3510">3</span></span>

<span data-ttu-id="ea353-3511">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3511">4</span></span>

<span data-ttu-id="ea353-3512">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3512">5</span></span>

<span data-ttu-id="ea353-3513">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3513">6</span></span>

<span data-ttu-id="ea353-3514">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3514">7</span></span>

<span data-ttu-id="ea353-3515">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3515">8</span></span>

<span data-ttu-id="ea353-3516">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3516">9</span></span>

<span data-ttu-id="ea353-3517">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3517">1</span></span><br/> <span data-ttu-id="ea353-3518">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3518">0</span></span><br/>

<span data-ttu-id="ea353-3519">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3519">1</span></span>

<span data-ttu-id="ea353-3520">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3520">2</span></span>

<span data-ttu-id="ea353-3521">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3521">3</span></span>

<span data-ttu-id="ea353-3522">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3522">4</span></span>

<span data-ttu-id="ea353-3523">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3523">5</span></span>

<span data-ttu-id="ea353-3524">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3524">6</span></span>

<span data-ttu-id="ea353-3525">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3525">7</span></span>

<span data-ttu-id="ea353-3526">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3526">8</span></span>

<span data-ttu-id="ea353-3527">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3527">9</span></span>

<span data-ttu-id="ea353-3528">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3528">2</span></span><br/> <span data-ttu-id="ea353-3529">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3529">0</span></span><br/>

<span data-ttu-id="ea353-3530">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3530">1</span></span>

<span data-ttu-id="ea353-3531">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3531">2</span></span>

<span data-ttu-id="ea353-3532">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3532">3</span></span>

<span data-ttu-id="ea353-3533">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3533">4</span></span>

<span data-ttu-id="ea353-3534">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3534">5</span></span>

<span data-ttu-id="ea353-3535">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3535">6</span></span>

<span data-ttu-id="ea353-3536">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3536">7</span></span>

<span data-ttu-id="ea353-3537">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3537">8</span></span>

<span data-ttu-id="ea353-3538">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3538">9</span></span>

<span data-ttu-id="ea353-3539">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3539">3</span></span><br/> <span data-ttu-id="ea353-3540">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3540">0</span></span><br/>

<span data-ttu-id="ea353-3541">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3541">1</span></span>

<span data-ttu-id="ea353-3542">\_hCursor (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3542">\_hCursor (optional)</span></span>

<span data-ttu-id="ea353-3543">\_cbRow (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3543">\_cbRow (optional)</span></span>

<span data-ttu-id="ea353-3544">\_cbBindingDesc (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3544">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="ea353-3545">\_dummy (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3545">\_dummy (optional)</span></span>

<span data-ttu-id="ea353-3546">cColumns (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3546">cColumns (optional)</span></span>

<span data-ttu-id="ea353-3547">aColumns (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-3547">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="ea353-3548">**\_ hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la riga per cui impostare le associazioni.</span><span class="sxs-lookup"><span data-stu-id="ea353-3548">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="ea353-3549">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3549">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="ea353-3550">**\_ cbRow:** intero senza segno a 32 bit che indica le dimensioni, in byte, di una riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-3550">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="ea353-3551">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3551">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="ea353-3552">**\_ cbBindingDesc:** intero senza segno a 32 bit che indica la lunghezza, in byte, dei campi che segue \_ il campo fittizio.</span><span class="sxs-lookup"><span data-stu-id="ea353-3552">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="ea353-3553">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3553">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="ea353-3554">**\_ dummy:** questo campo è inutilizzato e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ea353-3554">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="ea353-3555">Può essere impostato su qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-3555">It can be set to any arbitrary value.</span></span> <span data-ttu-id="ea353-3556">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="ea353-3557">**cColumns:** intero senza segno a 32 bit che indica il numero di elementi nella matrice aColumns.</span><span class="sxs-lookup"><span data-stu-id="ea353-3557">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="ea353-3558">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3558">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="ea353-3559">**aColumns:** matrice delle strutture CTableColumn che descrivono le colonne di una riga nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3559">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="ea353-3560">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3560">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="ea353-3561">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura abbia un allineamento a 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-3561">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="ea353-3562">Tali byte di spaziatura interna possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="ea353-3562">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="ea353-3563">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3563">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="ea353-3564">Il messaggio CPMGetRowsIn richiede righe da una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3564">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="ea353-3565">Il formato del messaggio CPMGetRowsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3565">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3566">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3566">0</span></span>

<span data-ttu-id="ea353-3567">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3567">1</span></span>

<span data-ttu-id="ea353-3568">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3568">2</span></span>

<span data-ttu-id="ea353-3569">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3569">3</span></span>

<span data-ttu-id="ea353-3570">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3570">4</span></span>

<span data-ttu-id="ea353-3571">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3571">5</span></span>

<span data-ttu-id="ea353-3572">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3572">6</span></span>

<span data-ttu-id="ea353-3573">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3573">7</span></span>

<span data-ttu-id="ea353-3574">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3574">8</span></span>

<span data-ttu-id="ea353-3575">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3575">9</span></span>

<span data-ttu-id="ea353-3576">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3576">1</span></span><br/> <span data-ttu-id="ea353-3577">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3577">0</span></span><br/>

<span data-ttu-id="ea353-3578">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3578">1</span></span>

<span data-ttu-id="ea353-3579">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3579">2</span></span>

<span data-ttu-id="ea353-3580">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3580">3</span></span>

<span data-ttu-id="ea353-3581">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3581">4</span></span>

<span data-ttu-id="ea353-3582">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3582">5</span></span>

<span data-ttu-id="ea353-3583">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3583">6</span></span>

<span data-ttu-id="ea353-3584">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3584">7</span></span>

<span data-ttu-id="ea353-3585">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3585">8</span></span>

<span data-ttu-id="ea353-3586">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3586">9</span></span>

<span data-ttu-id="ea353-3587">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3587">2</span></span><br/> <span data-ttu-id="ea353-3588">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3588">0</span></span><br/>

<span data-ttu-id="ea353-3589">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3589">1</span></span>

<span data-ttu-id="ea353-3590">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3590">2</span></span>

<span data-ttu-id="ea353-3591">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3591">3</span></span>

<span data-ttu-id="ea353-3592">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3592">4</span></span>

<span data-ttu-id="ea353-3593">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3593">5</span></span>

<span data-ttu-id="ea353-3594">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3594">6</span></span>

<span data-ttu-id="ea353-3595">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3595">7</span></span>

<span data-ttu-id="ea353-3596">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3596">8</span></span>

<span data-ttu-id="ea353-3597">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3597">9</span></span>

<span data-ttu-id="ea353-3598">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3598">3</span></span><br/> <span data-ttu-id="ea353-3599">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3599">0</span></span><br/>

<span data-ttu-id="ea353-3600">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3600">1</span></span>

<span data-ttu-id="ea353-3601">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="ea353-3601">\_hCursor</span></span>

<span data-ttu-id="ea353-3602">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="ea353-3602">\_cRowsToTransfer</span></span>

<span data-ttu-id="ea353-3603">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="ea353-3603">\_cbRowWidth</span></span>

<span data-ttu-id="ea353-3604">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="ea353-3604">\_cbSeek</span></span>

<span data-ttu-id="ea353-3605">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="ea353-3605">\_cbReserved</span></span>

<span data-ttu-id="ea353-3606">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="ea353-3606">\_cbReadBuffer</span></span>

<span data-ttu-id="ea353-3607">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="ea353-3607">\_ulClientBase</span></span>

<span data-ttu-id="ea353-3608">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="ea353-3608">\_fBwdFetch</span></span>

<span data-ttu-id="ea353-3609">eType</span><span class="sxs-lookup"><span data-stu-id="ea353-3609">eType</span></span>

<span data-ttu-id="ea353-3610">\_chapt</span><span class="sxs-lookup"><span data-stu-id="ea353-3610">\_chapt</span></span>

<span data-ttu-id="ea353-3611">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="ea353-3611">SeekDescription</span></span>

<span data-ttu-id="ea353-3612">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3612">...</span></span>

<span data-ttu-id="ea353-3613">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3613">... (variable)</span></span>



 

<span data-ttu-id="ea353-3614">**\_ hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3614">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="ea353-3615">**\_ cRowsToTransfer:** intero senza segno a 32 bit che indica il numero massimo di righe che il client vuole ricevere in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-3615">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="ea353-3616">**\_ cbRowWidth:** intero senza segno a 32 bit che indica la lunghezza di una riga, in byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-3616">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="ea353-3617">**\_ cbSeek:** intero senza segno a 32 bit che indica le dimensioni del messaggio che iniziano con eType.</span><span class="sxs-lookup"><span data-stu-id="ea353-3617">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="ea353-3618">**\_ cbReserved:** intero senza segno a 32 bit che indica le dimensioni, in byte, di un messaggio CPMGetRowsOut (senza i campi Rows e SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="ea353-3618">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="ea353-3619">Questo valore in questo campo viene aggiunto al valore del campo cbSeek e quindi deve essere usato per calcolare l'offset del campo Rows nel messaggio \_ CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-3619">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="ea353-3620">**\_ cbReadBuffer:** intero senza segno a 32 bit che DEVE essere impostato sul valore massimo di cbRowWidth o 1000 volte il valore di \_ \_ cRowsToTransfer, arrotondato al multiplo di 512 byte più vicino.</span><span class="sxs-lookup"><span data-stu-id="ea353-3620">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="ea353-3621">Il valore NON DEVE superare 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="ea353-3621">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="ea353-3622">**\_ ulClientBase:** intero senza segno a 32 bit che indica il valore di base da utilizzare per i calcoli del puntatore nel buffer di riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-3622">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="ea353-3623">Se vengono usati offset a 64 bit, il campo reserved2 dell'intestazione del messaggio viene usato come i 32 bit superiori e ulClientBase come i 32 bit inferiori di un valore \_ a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-3623">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="ea353-3624">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="ea353-3624">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="ea353-3625">**\_ fBwdFetch:** intero senza segno a 32 bit che indica l'ordine in cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3625">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="ea353-3626">Se impostato su 0x00000001, le righe devono essere recuperate in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="ea353-3626">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="ea353-3627">Se impostato su 0x00000000, le righe devono essere recuperate in avanti.</span><span class="sxs-lookup"><span data-stu-id="ea353-3627">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="ea353-3628">NON DEVE essere impostato su altri valori.</span><span class="sxs-lookup"><span data-stu-id="ea353-3628">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="ea353-3629">**eType:** intero senza segno a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ea353-3629">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="ea353-3630">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-3630">Value</span></span>                         | <span data-ttu-id="ea353-3631">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-3631">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="ea353-3632">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-3632">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="ea353-3633">SeekDescription contiene una struttura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="ea353-3633">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="ea353-3634">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-3634">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="ea353-3635">SeekDescription contiene una struttura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="ea353-3635">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="ea353-3636">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-3636">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="ea353-3637">SeekDescription contiene una struttura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="ea353-3637">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="ea353-3638">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-3638">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="ea353-3639">SeekDescription contiene una struttura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="ea353-3639">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="ea353-3640">**\_ chapt:** valore a 32 bit che rappresenta l'handle del capitolo del set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3640">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="ea353-3641">**SeekDescription:** questo campo DEVE contenere una struttura del tipo indicato dal valore eType.</span><span class="sxs-lookup"><span data-stu-id="ea353-3641">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="ea353-3642">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="ea353-3642">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="ea353-3643">Il messaggio CPMGetRowsOut risponde a un messaggio CPMGetRowsIn con le righe di una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3643">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="ea353-3644">I server DEVONO formattare gli offset per i tipi di dati a lunghezza variabile nel campo Righe come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ea353-3644">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="ea353-3645">Il client ha indicato che si tratta di un sistema a 32 bit (0x00000008 o inferiore nel campo iClientVersion di CPMConnectIn): gli offset sono numeri interi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-3645">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="ea353-3646">Il client ha indicato che si tratta di un sistema a 64 bit ( iClientVersion > 0x00000008 in CPMConnectIn) e Il server ha indicato che si tratta di un sistema a 32 bit ( serverVersion impostato su \_ 0x00000007 in CPMConnectOut): gli offset sono interi a \_ 32 bit</span><span class="sxs-lookup"><span data-stu-id="ea353-3646">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="ea353-3647">Il client ha indicato che si tratta di un sistema a 64 bit ( iClientVersion > 0x00000008 in CPMConnectIn) e il server ha indicato che si tratta di un sistema a 64 bit ( serverVersion impostato su \_ 0x00010007 in CPMConnectOut): gli offset sono interi a \_ 64 bit</span><span class="sxs-lookup"><span data-stu-id="ea353-3647">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="ea353-3648">Il formato del messaggio CPMGetRowsOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3648">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-3649">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3649">0</span></span>

<span data-ttu-id="ea353-3650">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3650">1</span></span>

<span data-ttu-id="ea353-3651">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3651">2</span></span>

<span data-ttu-id="ea353-3652">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3652">3</span></span>

<span data-ttu-id="ea353-3653">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3653">4</span></span>

<span data-ttu-id="ea353-3654">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3654">5</span></span>

<span data-ttu-id="ea353-3655">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3655">6</span></span>

<span data-ttu-id="ea353-3656">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3656">7</span></span>

<span data-ttu-id="ea353-3657">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3657">8</span></span>

<span data-ttu-id="ea353-3658">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3658">9</span></span>

<span data-ttu-id="ea353-3659">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3659">1</span></span><br/> <span data-ttu-id="ea353-3660">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3660">0</span></span><br/>

<span data-ttu-id="ea353-3661">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3661">1</span></span>

<span data-ttu-id="ea353-3662">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3662">2</span></span>

<span data-ttu-id="ea353-3663">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3663">3</span></span>

<span data-ttu-id="ea353-3664">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3664">4</span></span>

<span data-ttu-id="ea353-3665">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3665">5</span></span>

<span data-ttu-id="ea353-3666">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3666">6</span></span>

<span data-ttu-id="ea353-3667">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3667">7</span></span>

<span data-ttu-id="ea353-3668">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3668">8</span></span>

<span data-ttu-id="ea353-3669">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3669">9</span></span>

<span data-ttu-id="ea353-3670">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3670">2</span></span><br/> <span data-ttu-id="ea353-3671">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3671">0</span></span><br/>

<span data-ttu-id="ea353-3672">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3672">1</span></span>

<span data-ttu-id="ea353-3673">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3673">2</span></span>

<span data-ttu-id="ea353-3674">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3674">3</span></span>

<span data-ttu-id="ea353-3675">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3675">4</span></span>

<span data-ttu-id="ea353-3676">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3676">5</span></span>

<span data-ttu-id="ea353-3677">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3677">6</span></span>

<span data-ttu-id="ea353-3678">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3678">7</span></span>

<span data-ttu-id="ea353-3679">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3679">8</span></span>

<span data-ttu-id="ea353-3680">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3680">9</span></span>

<span data-ttu-id="ea353-3681">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3681">3</span></span><br/> <span data-ttu-id="ea353-3682">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3682">0</span></span><br/>

<span data-ttu-id="ea353-3683">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3683">1</span></span>

<span data-ttu-id="ea353-3684">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="ea353-3684">\_cRowsReturned</span></span>

<span data-ttu-id="ea353-3685">eType</span><span class="sxs-lookup"><span data-stu-id="ea353-3685">eType</span></span>

<span data-ttu-id="ea353-3686">\_chapt</span><span class="sxs-lookup"><span data-stu-id="ea353-3686">\_chapt</span></span>

<span data-ttu-id="ea353-3687">SeekDescription (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3687">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="ea353-3688">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3688">...</span></span>

<span data-ttu-id="ea353-3689">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3689">...</span></span>

<span data-ttu-id="ea353-3690">paddingRows (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3690">paddingRows (optional, variable)</span></span>

<span data-ttu-id="ea353-3691">Righe</span><span class="sxs-lookup"><span data-stu-id="ea353-3691">Rows</span></span>



 

<span data-ttu-id="ea353-3692">**\_ cRowsReturned:** intero senza segno a 32 bit che indica il numero di righe restituite in Rows.</span><span class="sxs-lookup"><span data-stu-id="ea353-3692">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="ea353-3693">**eType:** intero senza segno a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione rowseek da eseguire</span><span class="sxs-lookup"><span data-stu-id="ea353-3693">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="ea353-3694">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-3694">Value</span></span>                         | <span data-ttu-id="ea353-3695">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-3695">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="ea353-3696">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-3696">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="ea353-3697">Nessun seekdescription, ignorare il campo SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="ea353-3697">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="ea353-3698">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-3698">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="ea353-3699">SeekDescription contiene una struttura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="ea353-3699">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="ea353-3700">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-3700">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="ea353-3701">SeekDescription contiene una struttura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="ea353-3701">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="ea353-3702">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-3702">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="ea353-3703">SeekDescription contiene una struttura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="ea353-3703">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="ea353-3704">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-3704">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="ea353-3705">SeekDescription contiene una struttura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="ea353-3705">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="ea353-3706">**\_ chapt:** valore a 32 bit che rappresenta l'handle del capitolo del set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3706">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="ea353-3707">**SeekDescription:** questo campo DEVE contenere una struttura del tipo indicato dal campo eType.</span><span class="sxs-lookup"><span data-stu-id="ea353-3707">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="ea353-3708">**paddingRows:** questo campo DEVE essere di lunghezza sufficiente (da 0 a cbReserved-1 byte) per riempire il campo Rows per l'offset cbReserved dall'inizio di un messaggio, dove cbReserved è il valore nel \_ \_ messaggio \_ CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-3708">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="ea353-3709">I byte di riempimento usati in questo campo possono essere qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-3709">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="ea353-3710">Questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-3710">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="ea353-3711">**Righe:** i dati delle righe vengono formattati in base alle informazioni sulla colonna nel messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3711">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="ea353-3712">Le righe DEVONO essere archiviate in avanti (ad esempio, la riga 1 prima della riga 2).</span><span class="sxs-lookup"><span data-stu-id="ea353-3712">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="ea353-3713">Le colonne a dimensione fissa DEVONO essere archiviate in corrispondenza degli offset specificati dal messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3713">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="ea353-3714">Le colonne a dimensione variabile (ad esempio, stringhe) DEVONO essere archiviate come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-3714">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="ea353-3715">I dati della variabile stessa (ad esempio, la stringa) vengono archiviati vicino alla fine del buffer in ordine decrescente(ad esempio, la raccolta di tutti i dati delle variabili per la riga 1 si trova alla fine, la riga 2 più vicina e così via).</span><span class="sxs-lookup"><span data-stu-id="ea353-3715">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="ea353-3716">L'area a dimensione fissa (all'inizio del buffer di riga) DEVE contenere un CRowVariant per ogni colonna, archiviato in corrispondenza dell'offset specificato nel messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3716">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="ea353-3717">vType DEVE contenere il tipo di dati ,ad esempio VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="ea353-3717">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="ea353-3718">Se, come determinato dalle regole all'inizio di questa sezione, vengono usati offset a 32 bit, il campo Offset in CRowVariant DEVE contenere un valore a 32 bit che rappresenta l'offset dei dati delle variabili dall'inizio del messaggio CPMGetRowsOut, più il valore di ulClientBase specificato nel messaggio \_ CPMGetRowsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3718">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="ea353-3719">Se vengono usati offset a 64 bit, il campo Offset in CRowVariant DEVE contenere un valore a 64 bit che rappresenta l'offset dall'inizio del messaggio CPMGetRowsOut, aggiunto a un valore a 64 bit composto usando ulClientBase come minimo \_ a 32 bit e \_ ulReserved2 come 32 bit alti.</span><span class="sxs-lookup"><span data-stu-id="ea353-3719">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="ea353-3720">Ad esempio, se nel messaggio CPMSetBindingsIn sono specificate due colonne: Size (VT \_ I4) e Title (VT \_ LPWSTR) e ulClientBase da CPMGetRowsIn 0x10000 verranno visualizzate due righe come indicato di \_ seguito.</span><span class="sxs-lookup"><span data-stu-id="ea353-3720">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="ea353-3721">La sezione contrassegnata in grigio è la parte a lunghezza fissa del buffer.</span><span class="sxs-lookup"><span data-stu-id="ea353-3721">The section marked in grey is the fixed-length part of the buffer.</span></span>

![Esempio di messaggio cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="ea353-3723">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3723">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="ea353-3724">Il messaggio CPMRatioFinishedIn richiede la percentuale di completamento di una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3724">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="ea353-3725">Il formato del messaggio CPMRatioFinishedIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3725">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3726">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3726">0</span></span>

<span data-ttu-id="ea353-3727">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3727">1</span></span>

<span data-ttu-id="ea353-3728">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3728">2</span></span>

<span data-ttu-id="ea353-3729">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3729">3</span></span>

<span data-ttu-id="ea353-3730">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3730">4</span></span>

<span data-ttu-id="ea353-3731">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3731">5</span></span>

<span data-ttu-id="ea353-3732">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3732">6</span></span>

<span data-ttu-id="ea353-3733">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3733">7</span></span>

<span data-ttu-id="ea353-3734">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3734">8</span></span>

<span data-ttu-id="ea353-3735">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3735">9</span></span>

<span data-ttu-id="ea353-3736">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3736">1</span></span><br/> <span data-ttu-id="ea353-3737">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3737">0</span></span><br/>

<span data-ttu-id="ea353-3738">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3738">1</span></span>

<span data-ttu-id="ea353-3739">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3739">2</span></span>

<span data-ttu-id="ea353-3740">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3740">3</span></span>

<span data-ttu-id="ea353-3741">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3741">4</span></span>

<span data-ttu-id="ea353-3742">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3742">5</span></span>

<span data-ttu-id="ea353-3743">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3743">6</span></span>

<span data-ttu-id="ea353-3744">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3744">7</span></span>

<span data-ttu-id="ea353-3745">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3745">8</span></span>

<span data-ttu-id="ea353-3746">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3746">9</span></span>

<span data-ttu-id="ea353-3747">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3747">2</span></span><br/> <span data-ttu-id="ea353-3748">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3748">0</span></span><br/>

<span data-ttu-id="ea353-3749">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3749">1</span></span>

<span data-ttu-id="ea353-3750">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3750">2</span></span>

<span data-ttu-id="ea353-3751">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3751">3</span></span>

<span data-ttu-id="ea353-3752">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3752">4</span></span>

<span data-ttu-id="ea353-3753">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3753">5</span></span>

<span data-ttu-id="ea353-3754">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3754">6</span></span>

<span data-ttu-id="ea353-3755">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3755">7</span></span>

<span data-ttu-id="ea353-3756">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3756">8</span></span>

<span data-ttu-id="ea353-3757">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3757">9</span></span>

<span data-ttu-id="ea353-3758">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3758">3</span></span><br/> <span data-ttu-id="ea353-3759">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3759">0</span></span><br/>

<span data-ttu-id="ea353-3760">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3760">1</span></span>

<span data-ttu-id="ea353-3761">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="ea353-3761">\_hCursor</span></span>

<span data-ttu-id="ea353-3762">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="ea353-3762">\_fQuick</span></span>



 

<span data-ttu-id="ea353-3763">**\_ hCursor:** handle del messaggio CPMCreateQueryOut che identifica la query per cui richiedere informazioni di completamento.</span><span class="sxs-lookup"><span data-stu-id="ea353-3763">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="ea353-3764">**\_ fQuick:** DEVE essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-3764">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="ea353-3765">Non usato e DEVE essere ignorato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-3765">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="ea353-3766">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="ea353-3766">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="ea353-3767">Il messaggio CPMRatioFinishedOut risponde a un messaggio CPMRatioFinishedIn con il rapporto di completamento di una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3767">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="ea353-3768">Il formato del messaggio CPMRatioFinishedOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3768">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-3769">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3769">0</span></span>

<span data-ttu-id="ea353-3770">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3770">1</span></span>

<span data-ttu-id="ea353-3771">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3771">2</span></span>

<span data-ttu-id="ea353-3772">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3772">3</span></span>

<span data-ttu-id="ea353-3773">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3773">4</span></span>

<span data-ttu-id="ea353-3774">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3774">5</span></span>

<span data-ttu-id="ea353-3775">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3775">6</span></span>

<span data-ttu-id="ea353-3776">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3776">7</span></span>

<span data-ttu-id="ea353-3777">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3777">8</span></span>

<span data-ttu-id="ea353-3778">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3778">9</span></span>

<span data-ttu-id="ea353-3779">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3779">1</span></span><br/> <span data-ttu-id="ea353-3780">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3780">0</span></span><br/>

<span data-ttu-id="ea353-3781">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3781">1</span></span>

<span data-ttu-id="ea353-3782">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3782">2</span></span>

<span data-ttu-id="ea353-3783">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3783">3</span></span>

<span data-ttu-id="ea353-3784">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3784">4</span></span>

<span data-ttu-id="ea353-3785">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3785">5</span></span>

<span data-ttu-id="ea353-3786">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3786">6</span></span>

<span data-ttu-id="ea353-3787">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3787">7</span></span>

<span data-ttu-id="ea353-3788">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3788">8</span></span>

<span data-ttu-id="ea353-3789">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3789">9</span></span>

<span data-ttu-id="ea353-3790">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3790">2</span></span><br/> <span data-ttu-id="ea353-3791">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3791">0</span></span><br/>

<span data-ttu-id="ea353-3792">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3792">1</span></span>

<span data-ttu-id="ea353-3793">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3793">2</span></span>

<span data-ttu-id="ea353-3794">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3794">3</span></span>

<span data-ttu-id="ea353-3795">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3795">4</span></span>

<span data-ttu-id="ea353-3796">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3796">5</span></span>

<span data-ttu-id="ea353-3797">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3797">6</span></span>

<span data-ttu-id="ea353-3798">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3798">7</span></span>

<span data-ttu-id="ea353-3799">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3799">8</span></span>

<span data-ttu-id="ea353-3800">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3800">9</span></span>

<span data-ttu-id="ea353-3801">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3801">3</span></span><br/> <span data-ttu-id="ea353-3802">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3802">0</span></span><br/>

<span data-ttu-id="ea353-3803">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3803">1</span></span>

<span data-ttu-id="ea353-3804">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="ea353-3804">\_ ulNumerator</span></span>

<span data-ttu-id="ea353-3805">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="ea353-3805">\_ulDenominator</span></span>

<span data-ttu-id="ea353-3806">\_Corvi</span><span class="sxs-lookup"><span data-stu-id="ea353-3806">\_cRows</span></span>

<span data-ttu-id="ea353-3807">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="ea353-3807">\_fNewRows</span></span>



 

<span data-ttu-id="ea353-3808">**\_ ulNumerator:** intero senza segno a 32 bit che indica il numeratore del rapporto di completamento in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3808">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="ea353-3809">**\_ ulDenominator:** intero senza segno a 32 bit che indica il denominatore del rapporto di completamento in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3809">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="ea353-3810">DEVE essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="ea353-3810">MUST be greater than zero.</span></span>

<span data-ttu-id="ea353-3811">**\_ cRows:** intero senza segno a 32 bit che indica il numero totale di righe per la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3811">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="ea353-3812">**\_ fNewRows:** valore booleano che indica se sono disponibili nuove righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3812">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="ea353-3813">Il valore 0x00000001 indica che nel set di righe sono disponibili nuove righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3813">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="ea353-3814">Il valore 0x00000000 indica che il set di righe non contiene nuove righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3814">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="ea353-3815">Questo campo NON DEVE essere impostato su altri valori.</span><span class="sxs-lookup"><span data-stu-id="ea353-3815">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="ea353-3816">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3816">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="ea353-3817">Il messaggio CPMFetchValueIn richiede un valore di proprietà troppo grande per essere restituito in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3817">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="ea353-3818">Come specificato nella sezione 3.2.4.2.5, questo messaggio viene inviato ripetutamente per recuperare tutti i byte della proprietà, aggiornando cbSoFar per ognuno, fino a quando il campo fMoreExists del messaggio \_ \_ CPMFetchValueOut non è impostato su **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="ea353-3818">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="ea353-3819">Il formato del messaggio CPMFetchValueIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3819">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3820">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3820">0</span></span>

<span data-ttu-id="ea353-3821">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3821">1</span></span>

<span data-ttu-id="ea353-3822">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3822">2</span></span>

<span data-ttu-id="ea353-3823">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3823">3</span></span>

<span data-ttu-id="ea353-3824">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3824">4</span></span>

<span data-ttu-id="ea353-3825">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3825">5</span></span>

<span data-ttu-id="ea353-3826">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3826">6</span></span>

<span data-ttu-id="ea353-3827">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3827">7</span></span>

<span data-ttu-id="ea353-3828">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3828">8</span></span>

<span data-ttu-id="ea353-3829">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3829">9</span></span>

<span data-ttu-id="ea353-3830">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3830">1</span></span><br/> <span data-ttu-id="ea353-3831">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3831">0</span></span><br/>

<span data-ttu-id="ea353-3832">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3832">1</span></span>

<span data-ttu-id="ea353-3833">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3833">2</span></span>

<span data-ttu-id="ea353-3834">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3834">3</span></span>

<span data-ttu-id="ea353-3835">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3835">4</span></span>

<span data-ttu-id="ea353-3836">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3836">5</span></span>

<span data-ttu-id="ea353-3837">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3837">6</span></span>

<span data-ttu-id="ea353-3838">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3838">7</span></span>

<span data-ttu-id="ea353-3839">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3839">8</span></span>

<span data-ttu-id="ea353-3840">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3840">9</span></span>

<span data-ttu-id="ea353-3841">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3841">2</span></span><br/> <span data-ttu-id="ea353-3842">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3842">0</span></span><br/>

<span data-ttu-id="ea353-3843">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3843">1</span></span>

<span data-ttu-id="ea353-3844">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3844">2</span></span>

<span data-ttu-id="ea353-3845">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3845">3</span></span>

<span data-ttu-id="ea353-3846">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3846">4</span></span>

<span data-ttu-id="ea353-3847">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3847">5</span></span>

<span data-ttu-id="ea353-3848">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3848">6</span></span>

<span data-ttu-id="ea353-3849">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3849">7</span></span>

<span data-ttu-id="ea353-3850">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3850">8</span></span>

<span data-ttu-id="ea353-3851">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3851">9</span></span>

<span data-ttu-id="ea353-3852">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3852">3</span></span><br/> <span data-ttu-id="ea353-3853">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3853">0</span></span><br/>

<span data-ttu-id="ea353-3854">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3854">1</span></span>

<span data-ttu-id="ea353-3855">\_Wid</span><span class="sxs-lookup"><span data-stu-id="ea353-3855">\_wid</span></span>

<span data-ttu-id="ea353-3856">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="ea353-3856">\_cbSoFar</span></span>

<span data-ttu-id="ea353-3857">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="ea353-3857">\_cbPropSpec</span></span>

<span data-ttu-id="ea353-3858">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="ea353-3858">\_cbChunk</span></span>

<span data-ttu-id="ea353-3859">PropSpec (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3859">PropSpec (variable)</span></span>

<span data-ttu-id="ea353-3860">...</span><span class="sxs-lookup"><span data-stu-id="ea353-3860">...</span></span>

<span data-ttu-id="ea353-3861">\_padding (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3861">\_padding (variable)</span></span>



 

<span data-ttu-id="ea353-3862">**\_ wid:** intero senza segno a 32 bit contenente informazioni sull'ID del documento che identifica il documento per cui deve essere recuperata una proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-3862">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="ea353-3863">**\_ cbSoFar:** intero senza segno a 32 bit contenente il numero di byte trasferiti in precedenza per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-3863">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="ea353-3864">DEVE essere impostato su 0x00000000 nel primo messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-3864">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="ea353-3865">**\_ cbPropSpec:** intero senza segno a 32 bit contenente le dimensioni del campo PropSpec, in byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-3865">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="ea353-3866">**\_ cbChunk:** intero senza segno a 32 bit contenente il numero massimo di byte che il mittente può accettare in un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-3866">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="ea353-3867">*Comportamento di Windows: questo campo è impostato su 0x00004000 per tutte le versioni di Windows.*</span><span class="sxs-lookup"><span data-stu-id="ea353-3867">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="ea353-3868">**PropSpec:** struttura CFullPropSpec che specifica la proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ea353-3868">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="ea353-3869">**\_ padding:** questo campo DEVE essere della lunghezza necessaria (da 0 a 3 byte) per riempire il messaggio fino a un multiplo di 4 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-3869">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="ea353-3870">Il valore dei byte di riempimento può essere qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-3870">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="ea353-3871">Questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="ea353-3871">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="ea353-3872">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="ea353-3872">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="ea353-3873">Il messaggio CPMFetchValueOut risponde a un messaggio CPMFetchValueIn con un valore di proprietà da una query precedente.</span><span class="sxs-lookup"><span data-stu-id="ea353-3873">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="ea353-3874">Come specificato nella sezione 3.1.5.2.8, questo messaggio viene inviato dopo ogni messaggio CPMFetchValueIn fino al trasferimento di tutti i byte della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-3874">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="ea353-3875">Il formato del messaggio CPMFetchValueOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3875">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-3876">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3876">0</span></span>

<span data-ttu-id="ea353-3877">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3877">1</span></span>

<span data-ttu-id="ea353-3878">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3878">2</span></span>

<span data-ttu-id="ea353-3879">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3879">3</span></span>

<span data-ttu-id="ea353-3880">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3880">4</span></span>

<span data-ttu-id="ea353-3881">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3881">5</span></span>

<span data-ttu-id="ea353-3882">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3882">6</span></span>

<span data-ttu-id="ea353-3883">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3883">7</span></span>

<span data-ttu-id="ea353-3884">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3884">8</span></span>

<span data-ttu-id="ea353-3885">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3885">9</span></span>

<span data-ttu-id="ea353-3886">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3886">1</span></span><br/> <span data-ttu-id="ea353-3887">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3887">0</span></span><br/>

<span data-ttu-id="ea353-3888">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3888">1</span></span>

<span data-ttu-id="ea353-3889">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3889">2</span></span>

<span data-ttu-id="ea353-3890">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3890">3</span></span>

<span data-ttu-id="ea353-3891">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3891">4</span></span>

<span data-ttu-id="ea353-3892">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3892">5</span></span>

<span data-ttu-id="ea353-3893">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3893">6</span></span>

<span data-ttu-id="ea353-3894">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3894">7</span></span>

<span data-ttu-id="ea353-3895">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3895">8</span></span>

<span data-ttu-id="ea353-3896">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3896">9</span></span>

<span data-ttu-id="ea353-3897">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3897">2</span></span><br/> <span data-ttu-id="ea353-3898">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3898">0</span></span><br/>

<span data-ttu-id="ea353-3899">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3899">1</span></span>

<span data-ttu-id="ea353-3900">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3900">2</span></span>

<span data-ttu-id="ea353-3901">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3901">3</span></span>

<span data-ttu-id="ea353-3902">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3902">4</span></span>

<span data-ttu-id="ea353-3903">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3903">5</span></span>

<span data-ttu-id="ea353-3904">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3904">6</span></span>

<span data-ttu-id="ea353-3905">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3905">7</span></span>

<span data-ttu-id="ea353-3906">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3906">8</span></span>

<span data-ttu-id="ea353-3907">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3907">9</span></span>

<span data-ttu-id="ea353-3908">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3908">3</span></span><br/> <span data-ttu-id="ea353-3909">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3909">0</span></span><br/>

<span data-ttu-id="ea353-3910">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3910">1</span></span>

<span data-ttu-id="ea353-3911">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="ea353-3911">\_cbValue</span></span>

<span data-ttu-id="ea353-3912">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="ea353-3912">\_fMoreExists</span></span>

<span data-ttu-id="ea353-3913">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="ea353-3913">\_fValueExists</span></span>

<span data-ttu-id="ea353-3914">vType</span><span class="sxs-lookup"><span data-stu-id="ea353-3914">vType</span></span>

<span data-ttu-id="ea353-3915">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="ea353-3915">vValue (variable)</span></span>



 

<span data-ttu-id="ea353-3916">**\_ cbValue:** intero senza segno a 32 bit contenente le dimensioni totali, in byte in vValue.</span><span class="sxs-lookup"><span data-stu-id="ea353-3916">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="ea353-3917">**\_ fMoreExists:** valore booleano che indica se sono disponibili altri messaggi CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-3917">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="ea353-3918">Se impostato su 0x00000001, sono presenti altri messaggi CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-3918">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="ea353-3919">Se impostato su 0x00000000, non sono disponibili messaggi CPMFetchValueOut aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="ea353-3919">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="ea353-3920">**\_ fValueExists:** valore booleano che indica se è presente un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-3920">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="ea353-3921">Se impostato su 0x00000001, esiste un valore per la proprietà .</span><span class="sxs-lookup"><span data-stu-id="ea353-3921">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="ea353-3922">Se impostato su 0x00000000, non esiste un valore per la proprietà .</span><span class="sxs-lookup"><span data-stu-id="ea353-3922">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="ea353-3923">**vType:** valore dell'enumerazione VARENUM, vedere la sezione 2.2.1.1 per informazioni dettagliate, che descrivono il tipo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-3923">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="ea353-3924">**vValue:** parte di una matrice di byte contenente una struttura SERIALIZEDPROPERTYVALUE come specificato nella sezione 2.2.1.32, dove l'offset dell'inizio della parte è il valore \_ di cbSoFar in CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-3924">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="ea353-3925">La lunghezza della parte, indicata dal campo cbValue, DEVE essere uguale al valore di \_ \_ cbChunk in CPMFetchValueIn se fMoreExists è impostato su 0x00000001 e DEVE essere minore o uguale al valore di \_ cbChunk in caso \_ contrario.</span><span class="sxs-lookup"><span data-stu-id="ea353-3925">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="ea353-3926">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="ea353-3926">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="ea353-3927">Il messaggio CPMGetNotify richiede che il client voglia ricevere una notifica delle modifiche al set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-3927">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="ea353-3928">Il messaggio NON DEVE includere un corpo. solo l'intestazione del messaggio, come specificato nella sezione 2.2.2, deve essere inviata.</span><span class="sxs-lookup"><span data-stu-id="ea353-3928">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="ea353-3929">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="ea353-3929">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="ea353-3930">Il messaggio CPMSendNotifyOut notifica al client una modifica ai risultati di una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3930">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="ea353-3931">Questo messaggio viene inviato solo quando si verifica una modifica.</span><span class="sxs-lookup"><span data-stu-id="ea353-3931">This message is only sent when a change occurs.</span></span> <span data-ttu-id="ea353-3932">Il formato del messaggio CPMSendNotifyOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3932">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-3933">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3933">0</span></span>

<span data-ttu-id="ea353-3934">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3934">1</span></span>

<span data-ttu-id="ea353-3935">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3935">2</span></span>

<span data-ttu-id="ea353-3936">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3936">3</span></span>

<span data-ttu-id="ea353-3937">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3937">4</span></span>

<span data-ttu-id="ea353-3938">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3938">5</span></span>

<span data-ttu-id="ea353-3939">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3939">6</span></span>

<span data-ttu-id="ea353-3940">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3940">7</span></span>

<span data-ttu-id="ea353-3941">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3941">8</span></span>

<span data-ttu-id="ea353-3942">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3942">9</span></span>

<span data-ttu-id="ea353-3943">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3943">1</span></span><br/> <span data-ttu-id="ea353-3944">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3944">0</span></span><br/>

<span data-ttu-id="ea353-3945">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3945">1</span></span>

<span data-ttu-id="ea353-3946">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3946">2</span></span>

<span data-ttu-id="ea353-3947">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3947">3</span></span>

<span data-ttu-id="ea353-3948">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3948">4</span></span>

<span data-ttu-id="ea353-3949">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3949">5</span></span>

<span data-ttu-id="ea353-3950">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3950">6</span></span>

<span data-ttu-id="ea353-3951">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3951">7</span></span>

<span data-ttu-id="ea353-3952">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3952">8</span></span>

<span data-ttu-id="ea353-3953">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3953">9</span></span>

<span data-ttu-id="ea353-3954">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3954">2</span></span><br/> <span data-ttu-id="ea353-3955">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3955">0</span></span><br/>

<span data-ttu-id="ea353-3956">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3956">1</span></span>

<span data-ttu-id="ea353-3957">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3957">2</span></span>

<span data-ttu-id="ea353-3958">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3958">3</span></span>

<span data-ttu-id="ea353-3959">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3959">4</span></span>

<span data-ttu-id="ea353-3960">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3960">5</span></span>

<span data-ttu-id="ea353-3961">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3961">6</span></span>

<span data-ttu-id="ea353-3962">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3962">7</span></span>

<span data-ttu-id="ea353-3963">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3963">8</span></span>

<span data-ttu-id="ea353-3964">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3964">9</span></span>

<span data-ttu-id="ea353-3965">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3965">3</span></span><br/> <span data-ttu-id="ea353-3966">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3966">0</span></span><br/>

<span data-ttu-id="ea353-3967">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3967">1</span></span>

<span data-ttu-id="ea353-3968">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="ea353-3968">\_watchNotify</span></span>



 

<span data-ttu-id="ea353-3969">**\_ watchNotify:** modifica alla query.</span><span class="sxs-lookup"><span data-stu-id="ea353-3969">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="ea353-3970">DEVE essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-3970">It MUST be one of the following values:</span></span>



| <span data-ttu-id="ea353-3971">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-3971">Value</span></span>                                     | <span data-ttu-id="ea353-3972">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-3972">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="ea353-3973">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-3973">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="ea353-3974">Il numero di righe nel set di righe della query è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="ea353-3974">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="ea353-3975">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-3975">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="ea353-3976">La query è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ea353-3976">The query has completed.</span></span>                            |
| <span data-ttu-id="ea353-3977">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-3977">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="ea353-3978">La query è stata rieseguiti.</span><span class="sxs-lookup"><span data-stu-id="ea353-3978">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="ea353-3979">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="ea353-3979">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="ea353-3980">Il messaggio CPMGetApproximatePositionIn richiede la posizione approssimativa di un segnalibro in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-3980">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="ea353-3981">Il formato del messaggio CPMGetApproximatePositionIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-3981">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-3982">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3982">0</span></span>

<span data-ttu-id="ea353-3983">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3983">1</span></span>

<span data-ttu-id="ea353-3984">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3984">2</span></span>

<span data-ttu-id="ea353-3985">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3985">3</span></span>

<span data-ttu-id="ea353-3986">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3986">4</span></span>

<span data-ttu-id="ea353-3987">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3987">5</span></span>

<span data-ttu-id="ea353-3988">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3988">6</span></span>

<span data-ttu-id="ea353-3989">7</span><span class="sxs-lookup"><span data-stu-id="ea353-3989">7</span></span>

<span data-ttu-id="ea353-3990">8</span><span class="sxs-lookup"><span data-stu-id="ea353-3990">8</span></span>

<span data-ttu-id="ea353-3991">9</span><span class="sxs-lookup"><span data-stu-id="ea353-3991">9</span></span>

<span data-ttu-id="ea353-3992">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3992">1</span></span><br/> <span data-ttu-id="ea353-3993">0</span><span class="sxs-lookup"><span data-stu-id="ea353-3993">0</span></span><br/>

<span data-ttu-id="ea353-3994">1</span><span class="sxs-lookup"><span data-stu-id="ea353-3994">1</span></span>

<span data-ttu-id="ea353-3995">2</span><span class="sxs-lookup"><span data-stu-id="ea353-3995">2</span></span>

<span data-ttu-id="ea353-3996">3</span><span class="sxs-lookup"><span data-stu-id="ea353-3996">3</span></span>

<span data-ttu-id="ea353-3997">4</span><span class="sxs-lookup"><span data-stu-id="ea353-3997">4</span></span>

<span data-ttu-id="ea353-3998">5</span><span class="sxs-lookup"><span data-stu-id="ea353-3998">5</span></span>

<span data-ttu-id="ea353-3999">6</span><span class="sxs-lookup"><span data-stu-id="ea353-3999">6</span></span>

<span data-ttu-id="ea353-4000">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4000">7</span></span>

<span data-ttu-id="ea353-4001">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4001">8</span></span>

<span data-ttu-id="ea353-4002">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4002">9</span></span>

<span data-ttu-id="ea353-4003">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4003">2</span></span><br/> <span data-ttu-id="ea353-4004">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4004">0</span></span><br/>

<span data-ttu-id="ea353-4005">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4005">1</span></span>

<span data-ttu-id="ea353-4006">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4006">2</span></span>

<span data-ttu-id="ea353-4007">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4007">3</span></span>

<span data-ttu-id="ea353-4008">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4008">4</span></span>

<span data-ttu-id="ea353-4009">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4009">5</span></span>

<span data-ttu-id="ea353-4010">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4010">6</span></span>

<span data-ttu-id="ea353-4011">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4011">7</span></span>

<span data-ttu-id="ea353-4012">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4012">8</span></span>

<span data-ttu-id="ea353-4013">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4013">9</span></span>

<span data-ttu-id="ea353-4014">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4014">3</span></span><br/> <span data-ttu-id="ea353-4015">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4015">0</span></span><br/>

<span data-ttu-id="ea353-4016">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4016">1</span></span>

<span data-ttu-id="ea353-4017">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="ea353-4017">\_hCursor</span></span>

<span data-ttu-id="ea353-4018">\_chapt</span><span class="sxs-lookup"><span data-stu-id="ea353-4018">\_chapt</span></span>

<span data-ttu-id="ea353-4019">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="ea353-4019">\_bmk</span></span>



 

<span data-ttu-id="ea353-4020">**\_ hCursor:** valore a 32 bit che rappresenta il cursore di query ottenuto da CPMCreateQueryOut per il set di righe contenente il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="ea353-4020">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="ea353-4021">**\_ chapt:** valore a 32 bit che rappresenta l'handle per il capitolo contenente il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="ea353-4021">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="ea353-4022">**\_ bmk:** valore a 32 bit che rappresenta l'handle del segnalibro per il quale recuperare la posizione approssimativa.</span><span class="sxs-lookup"><span data-stu-id="ea353-4022">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="ea353-4023">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4023">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="ea353-4024">Il messaggio CPMGetApproximatePositionOut risponde a un messaggio CPMGetApproximatePositionIn che descrive la posizione approssimativa del segnalibro nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4024">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="ea353-4025">Il formato del messaggio CPMGetApproximatePositionOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-4025">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-4026">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4026">0</span></span>

<span data-ttu-id="ea353-4027">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4027">1</span></span>

<span data-ttu-id="ea353-4028">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4028">2</span></span>

<span data-ttu-id="ea353-4029">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4029">3</span></span>

<span data-ttu-id="ea353-4030">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4030">4</span></span>

<span data-ttu-id="ea353-4031">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4031">5</span></span>

<span data-ttu-id="ea353-4032">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4032">6</span></span>

<span data-ttu-id="ea353-4033">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4033">7</span></span>

<span data-ttu-id="ea353-4034">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4034">8</span></span>

<span data-ttu-id="ea353-4035">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4035">9</span></span>

<span data-ttu-id="ea353-4036">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4036">1</span></span><br/> <span data-ttu-id="ea353-4037">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4037">0</span></span><br/>

<span data-ttu-id="ea353-4038">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4038">1</span></span>

<span data-ttu-id="ea353-4039">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4039">2</span></span>

<span data-ttu-id="ea353-4040">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4040">3</span></span>

<span data-ttu-id="ea353-4041">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4041">4</span></span>

<span data-ttu-id="ea353-4042">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4042">5</span></span>

<span data-ttu-id="ea353-4043">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4043">6</span></span>

<span data-ttu-id="ea353-4044">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4044">7</span></span>

<span data-ttu-id="ea353-4045">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4045">8</span></span>

<span data-ttu-id="ea353-4046">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4046">9</span></span>

<span data-ttu-id="ea353-4047">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4047">2</span></span><br/> <span data-ttu-id="ea353-4048">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4048">0</span></span><br/>

<span data-ttu-id="ea353-4049">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4049">1</span></span>

<span data-ttu-id="ea353-4050">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4050">2</span></span>

<span data-ttu-id="ea353-4051">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4051">3</span></span>

<span data-ttu-id="ea353-4052">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4052">4</span></span>

<span data-ttu-id="ea353-4053">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4053">5</span></span>

<span data-ttu-id="ea353-4054">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4054">6</span></span>

<span data-ttu-id="ea353-4055">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4055">7</span></span>

<span data-ttu-id="ea353-4056">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4056">8</span></span>

<span data-ttu-id="ea353-4057">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4057">9</span></span>

<span data-ttu-id="ea353-4058">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4058">3</span></span><br/> <span data-ttu-id="ea353-4059">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4059">0</span></span><br/>

<span data-ttu-id="ea353-4060">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4060">1</span></span>

<span data-ttu-id="ea353-4061">\_numerator</span><span class="sxs-lookup"><span data-stu-id="ea353-4061">\_numerator</span></span>

<span data-ttu-id="ea353-4062">\_denominator</span><span class="sxs-lookup"><span data-stu-id="ea353-4062">\_denominator</span></span>



 

<span data-ttu-id="ea353-4063">**\_ numeratore:** intero senza segno a 32 bit contenente il numero di riga del segnalibro nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-4063">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="ea353-4064">Se non sono presenti righe, questo campo DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4064">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="ea353-4065">**\_ denominator:** intero senza segno a 32 bit contenente il numero di righe nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-4065">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="ea353-4066">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4066">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="ea353-4067">Il messaggio CPMCompareBmkIn richiede un confronto tra due segnalibri in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4067">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="ea353-4068">Il formato del messaggio CPMCompareBmkIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-4068">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-4069">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4069">0</span></span>

<span data-ttu-id="ea353-4070">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4070">1</span></span>

<span data-ttu-id="ea353-4071">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4071">2</span></span>

<span data-ttu-id="ea353-4072">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4072">3</span></span>

<span data-ttu-id="ea353-4073">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4073">4</span></span>

<span data-ttu-id="ea353-4074">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4074">5</span></span>

<span data-ttu-id="ea353-4075">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4075">6</span></span>

<span data-ttu-id="ea353-4076">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4076">7</span></span>

<span data-ttu-id="ea353-4077">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4077">8</span></span>

<span data-ttu-id="ea353-4078">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4078">9</span></span>

<span data-ttu-id="ea353-4079">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4079">1</span></span><br/> <span data-ttu-id="ea353-4080">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4080">0</span></span><br/>

<span data-ttu-id="ea353-4081">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4081">1</span></span>

<span data-ttu-id="ea353-4082">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4082">2</span></span>

<span data-ttu-id="ea353-4083">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4083">3</span></span>

<span data-ttu-id="ea353-4084">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4084">4</span></span>

<span data-ttu-id="ea353-4085">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4085">5</span></span>

<span data-ttu-id="ea353-4086">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4086">6</span></span>

<span data-ttu-id="ea353-4087">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4087">7</span></span>

<span data-ttu-id="ea353-4088">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4088">8</span></span>

<span data-ttu-id="ea353-4089">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4089">9</span></span>

<span data-ttu-id="ea353-4090">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4090">2</span></span><br/> <span data-ttu-id="ea353-4091">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4091">0</span></span><br/>

<span data-ttu-id="ea353-4092">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4092">1</span></span>

<span data-ttu-id="ea353-4093">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4093">2</span></span>

<span data-ttu-id="ea353-4094">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4094">3</span></span>

<span data-ttu-id="ea353-4095">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4095">4</span></span>

<span data-ttu-id="ea353-4096">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4096">5</span></span>

<span data-ttu-id="ea353-4097">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4097">6</span></span>

<span data-ttu-id="ea353-4098">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4098">7</span></span>

<span data-ttu-id="ea353-4099">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4099">8</span></span>

<span data-ttu-id="ea353-4100">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4100">9</span></span>

<span data-ttu-id="ea353-4101">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4101">3</span></span><br/> <span data-ttu-id="ea353-4102">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4102">0</span></span><br/>

<span data-ttu-id="ea353-4103">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4103">1</span></span>

<span data-ttu-id="ea353-4104">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="ea353-4104">\_hCursor</span></span>

<span data-ttu-id="ea353-4105">\_chapt</span><span class="sxs-lookup"><span data-stu-id="ea353-4105">\_chapt</span></span>

<span data-ttu-id="ea353-4106">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="ea353-4106">\_bmkFirst</span></span>

<span data-ttu-id="ea353-4107">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="ea353-4107">\_bmkSecond</span></span>



 

<span data-ttu-id="ea353-4108">\_**hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut per il set di righe contenente i segnalibri.</span><span class="sxs-lookup"><span data-stu-id="ea353-4108">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="ea353-4109">\_**chapt:** valore a 32 bit che rappresenta l'handle del capitolo contenente i segnalibri da confrontare.</span><span class="sxs-lookup"><span data-stu-id="ea353-4109">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="ea353-4110">\_**bmkFirst:** valore a 32 bit che rappresenta l'handle al primo segnalibro da confrontare.</span><span class="sxs-lookup"><span data-stu-id="ea353-4110">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="ea353-4111">\_**bmkSecond:** valore a 32 bit che rappresenta l'handle per il secondo segnalibro da confrontare.</span><span class="sxs-lookup"><span data-stu-id="ea353-4111">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="ea353-4112">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4112">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="ea353-4113">Il messaggio CPMCompareBmkOut risponde a un messaggio CPMCompareBmkIn con il confronto dei due segnalibri nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4113">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="ea353-4114">Il formato del messaggio CPMCompareBmkOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-4114">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-4115">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4115">0</span></span>

<span data-ttu-id="ea353-4116">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4116">1</span></span>

<span data-ttu-id="ea353-4117">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4117">2</span></span>

<span data-ttu-id="ea353-4118">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4118">3</span></span>

<span data-ttu-id="ea353-4119">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4119">4</span></span>

<span data-ttu-id="ea353-4120">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4120">5</span></span>

<span data-ttu-id="ea353-4121">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4121">6</span></span>

<span data-ttu-id="ea353-4122">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4122">7</span></span>

<span data-ttu-id="ea353-4123">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4123">8</span></span>

<span data-ttu-id="ea353-4124">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4124">9</span></span>

<span data-ttu-id="ea353-4125">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4125">1</span></span><br/> <span data-ttu-id="ea353-4126">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4126">0</span></span><br/>

<span data-ttu-id="ea353-4127">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4127">1</span></span>

<span data-ttu-id="ea353-4128">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4128">2</span></span>

<span data-ttu-id="ea353-4129">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4129">3</span></span>

<span data-ttu-id="ea353-4130">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4130">4</span></span>

<span data-ttu-id="ea353-4131">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4131">5</span></span>

<span data-ttu-id="ea353-4132">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4132">6</span></span>

<span data-ttu-id="ea353-4133">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4133">7</span></span>

<span data-ttu-id="ea353-4134">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4134">8</span></span>

<span data-ttu-id="ea353-4135">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4135">9</span></span>

<span data-ttu-id="ea353-4136">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4136">2</span></span><br/> <span data-ttu-id="ea353-4137">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4137">0</span></span><br/>

<span data-ttu-id="ea353-4138">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4138">1</span></span>

<span data-ttu-id="ea353-4139">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4139">2</span></span>

<span data-ttu-id="ea353-4140">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4140">3</span></span>

<span data-ttu-id="ea353-4141">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4141">4</span></span>

<span data-ttu-id="ea353-4142">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4142">5</span></span>

<span data-ttu-id="ea353-4143">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4143">6</span></span>

<span data-ttu-id="ea353-4144">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4144">7</span></span>

<span data-ttu-id="ea353-4145">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4145">8</span></span>

<span data-ttu-id="ea353-4146">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4146">9</span></span>

<span data-ttu-id="ea353-4147">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4147">3</span></span><br/> <span data-ttu-id="ea353-4148">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4148">0</span></span><br/>

<span data-ttu-id="ea353-4149">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4149">1</span></span>

<span data-ttu-id="ea353-4150">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="ea353-4150">\_dwComparison</span></span>



 

<span data-ttu-id="ea353-4151">\_**dwComparison:** uno dei valori seguenti, che indica le posizioni relative dei due segnalibri nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4151">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="ea353-4152">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-4152">Value</span></span>                               | <span data-ttu-id="ea353-4153">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-4153">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ea353-4154">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-4154">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="ea353-4155">Il primo segnalibro viene posizionato prima del secondo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4155">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="ea353-4156">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea353-4156">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="ea353-4157">Il primo segnalibro ha la stessa posizione del secondo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4157">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="ea353-4158">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea353-4158">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="ea353-4159">Il primo segnalibro viene posizionato dopo il secondo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4159">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="ea353-4160">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea353-4160">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="ea353-4161">Il primo segnalibro non ha la stessa posizione del secondo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4161">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="ea353-4162">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea353-4162">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="ea353-4163">Il primo segnalibro non è confrontabile con il secondo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4163">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="ea353-4164">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4164">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="ea353-4165">Il messaggio CPMRestartPositionIn sposta la posizione di recupero di un cursore all'inizio del capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4165">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="ea353-4166">Come specificato nella sezione 3.1.5.2.12, il server risponderà usando lo stesso messaggio, con i risultati della richiesta contenuti nel campo \_ stato dell'intestazione CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-4166">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="ea353-4167">Il formato del messaggio CPMRestartPositionIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-4167">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-4168">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4168">0</span></span>

<span data-ttu-id="ea353-4169">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4169">1</span></span>

<span data-ttu-id="ea353-4170">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4170">2</span></span>

<span data-ttu-id="ea353-4171">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4171">3</span></span>

<span data-ttu-id="ea353-4172">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4172">4</span></span>

<span data-ttu-id="ea353-4173">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4173">5</span></span>

<span data-ttu-id="ea353-4174">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4174">6</span></span>

<span data-ttu-id="ea353-4175">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4175">7</span></span>

<span data-ttu-id="ea353-4176">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4176">8</span></span>

<span data-ttu-id="ea353-4177">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4177">9</span></span>

<span data-ttu-id="ea353-4178">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4178">1</span></span><br/> <span data-ttu-id="ea353-4179">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4179">0</span></span><br/>

<span data-ttu-id="ea353-4180">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4180">1</span></span>

<span data-ttu-id="ea353-4181">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4181">2</span></span>

<span data-ttu-id="ea353-4182">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4182">3</span></span>

<span data-ttu-id="ea353-4183">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4183">4</span></span>

<span data-ttu-id="ea353-4184">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4184">5</span></span>

<span data-ttu-id="ea353-4185">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4185">6</span></span>

<span data-ttu-id="ea353-4186">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4186">7</span></span>

<span data-ttu-id="ea353-4187">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4187">8</span></span>

<span data-ttu-id="ea353-4188">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4188">9</span></span>

<span data-ttu-id="ea353-4189">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4189">2</span></span><br/> <span data-ttu-id="ea353-4190">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4190">0</span></span><br/>

<span data-ttu-id="ea353-4191">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4191">1</span></span>

<span data-ttu-id="ea353-4192">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4192">2</span></span>

<span data-ttu-id="ea353-4193">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4193">3</span></span>

<span data-ttu-id="ea353-4194">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4194">4</span></span>

<span data-ttu-id="ea353-4195">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4195">5</span></span>

<span data-ttu-id="ea353-4196">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4196">6</span></span>

<span data-ttu-id="ea353-4197">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4197">7</span></span>

<span data-ttu-id="ea353-4198">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4198">8</span></span>

<span data-ttu-id="ea353-4199">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4199">9</span></span>

<span data-ttu-id="ea353-4200">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4200">3</span></span><br/> <span data-ttu-id="ea353-4201">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4201">0</span></span><br/>

<span data-ttu-id="ea353-4202">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4202">1</span></span>

<span data-ttu-id="ea353-4203">\_hCursor (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-4203">\_hCursor (optional)</span></span>

<span data-ttu-id="ea353-4204">\_chapt (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="ea353-4204">\_chapt (optional)</span></span>



 

<span data-ttu-id="ea353-4205">**\_ hCursor:** valore a 32 bit che rappresenta l'handle, ottenuto da un messaggio CPMCreateQueryOut, che identifica la query per cui riavviare la posizione.</span><span class="sxs-lookup"><span data-stu-id="ea353-4205">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="ea353-4206">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4206">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="ea353-4207">**\_ chapt:** valore a 32 bit che rappresenta l'handle di un capitolo da cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-4207">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="ea353-4208">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4208">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="ea353-4209">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4209">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="ea353-4210">Il messaggio CPMFreeCursorIn richiede il rilascio di un cursore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4210">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="ea353-4211">Il formato del messaggio CPMFreeCursorIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-4211">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="ea353-4212">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4212">0</span></span>

<span data-ttu-id="ea353-4213">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4213">1</span></span>

<span data-ttu-id="ea353-4214">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4214">2</span></span>

<span data-ttu-id="ea353-4215">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4215">3</span></span>

<span data-ttu-id="ea353-4216">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4216">4</span></span>

<span data-ttu-id="ea353-4217">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4217">5</span></span>

<span data-ttu-id="ea353-4218">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4218">6</span></span>

<span data-ttu-id="ea353-4219">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4219">7</span></span>

<span data-ttu-id="ea353-4220">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4220">8</span></span>

<span data-ttu-id="ea353-4221">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4221">9</span></span>

<span data-ttu-id="ea353-4222">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4222">1</span></span><br/> <span data-ttu-id="ea353-4223">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4223">0</span></span><br/>

<span data-ttu-id="ea353-4224">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4224">1</span></span>

<span data-ttu-id="ea353-4225">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4225">2</span></span>

<span data-ttu-id="ea353-4226">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4226">3</span></span>

<span data-ttu-id="ea353-4227">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4227">4</span></span>

<span data-ttu-id="ea353-4228">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4228">5</span></span>

<span data-ttu-id="ea353-4229">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4229">6</span></span>

<span data-ttu-id="ea353-4230">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4230">7</span></span>

<span data-ttu-id="ea353-4231">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4231">8</span></span>

<span data-ttu-id="ea353-4232">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4232">9</span></span>

<span data-ttu-id="ea353-4233">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4233">2</span></span><br/> <span data-ttu-id="ea353-4234">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4234">0</span></span><br/>

<span data-ttu-id="ea353-4235">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4235">1</span></span>

<span data-ttu-id="ea353-4236">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4236">2</span></span>

<span data-ttu-id="ea353-4237">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4237">3</span></span>

<span data-ttu-id="ea353-4238">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4238">4</span></span>

<span data-ttu-id="ea353-4239">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4239">5</span></span>

<span data-ttu-id="ea353-4240">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4240">6</span></span>

<span data-ttu-id="ea353-4241">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4241">7</span></span>

<span data-ttu-id="ea353-4242">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4242">8</span></span>

<span data-ttu-id="ea353-4243">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4243">9</span></span>

<span data-ttu-id="ea353-4244">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4244">3</span></span><br/> <span data-ttu-id="ea353-4245">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4245">0</span></span><br/>

<span data-ttu-id="ea353-4246">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4246">1</span></span>

<span data-ttu-id="ea353-4247">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="ea353-4247">\_hCursor</span></span>



 

<span data-ttu-id="ea353-4248">**\_ hCursor:** valore a 32 bit che rappresenta l'handle del cursore dal messaggio CPMCreateQueryOut da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="ea353-4248">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="ea353-4249">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4249">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="ea353-4250">Il messaggio CPMFreeCursorOut risponde a un messaggio CPMFreeCursorIn con i risultati del salvataggio di un cursore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4250">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="ea353-4251">Il formato del messaggio CPMFreeCursorOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="ea353-4251">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="ea353-4252">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4252">0</span></span>

<span data-ttu-id="ea353-4253">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4253">1</span></span>

<span data-ttu-id="ea353-4254">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4254">2</span></span>

<span data-ttu-id="ea353-4255">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4255">3</span></span>

<span data-ttu-id="ea353-4256">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4256">4</span></span>

<span data-ttu-id="ea353-4257">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4257">5</span></span>

<span data-ttu-id="ea353-4258">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4258">6</span></span>

<span data-ttu-id="ea353-4259">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4259">7</span></span>

<span data-ttu-id="ea353-4260">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4260">8</span></span>

<span data-ttu-id="ea353-4261">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4261">9</span></span>

<span data-ttu-id="ea353-4262">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4262">1</span></span><br/> <span data-ttu-id="ea353-4263">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4263">0</span></span><br/>

<span data-ttu-id="ea353-4264">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4264">1</span></span>

<span data-ttu-id="ea353-4265">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4265">2</span></span>

<span data-ttu-id="ea353-4266">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4266">3</span></span>

<span data-ttu-id="ea353-4267">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4267">4</span></span>

<span data-ttu-id="ea353-4268">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4268">5</span></span>

<span data-ttu-id="ea353-4269">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4269">6</span></span>

<span data-ttu-id="ea353-4270">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4270">7</span></span>

<span data-ttu-id="ea353-4271">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4271">8</span></span>

<span data-ttu-id="ea353-4272">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4272">9</span></span>

<span data-ttu-id="ea353-4273">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4273">2</span></span><br/> <span data-ttu-id="ea353-4274">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4274">0</span></span><br/>

<span data-ttu-id="ea353-4275">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4275">1</span></span>

<span data-ttu-id="ea353-4276">2</span><span class="sxs-lookup"><span data-stu-id="ea353-4276">2</span></span>

<span data-ttu-id="ea353-4277">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4277">3</span></span>

<span data-ttu-id="ea353-4278">4</span><span class="sxs-lookup"><span data-stu-id="ea353-4278">4</span></span>

<span data-ttu-id="ea353-4279">5</span><span class="sxs-lookup"><span data-stu-id="ea353-4279">5</span></span>

<span data-ttu-id="ea353-4280">6</span><span class="sxs-lookup"><span data-stu-id="ea353-4280">6</span></span>

<span data-ttu-id="ea353-4281">7</span><span class="sxs-lookup"><span data-stu-id="ea353-4281">7</span></span>

<span data-ttu-id="ea353-4282">8</span><span class="sxs-lookup"><span data-stu-id="ea353-4282">8</span></span>

<span data-ttu-id="ea353-4283">9</span><span class="sxs-lookup"><span data-stu-id="ea353-4283">9</span></span>

<span data-ttu-id="ea353-4284">3</span><span class="sxs-lookup"><span data-stu-id="ea353-4284">3</span></span><br/> <span data-ttu-id="ea353-4285">0</span><span class="sxs-lookup"><span data-stu-id="ea353-4285">0</span></span><br/>

<span data-ttu-id="ea353-4286">1</span><span class="sxs-lookup"><span data-stu-id="ea353-4286">1</span></span>

<span data-ttu-id="ea353-4287">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="ea353-4287">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="ea353-4288">**\_ cCursorsRemaining:** intero senza segno a 32 bit che indica il numero di cursori ancora in uso per la query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4288">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="ea353-4289">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="ea353-4289">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="ea353-4290">Il messaggio CPMDisconnect termina la connessione con il server</span><span class="sxs-lookup"><span data-stu-id="ea353-4290">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="ea353-4291">Il messaggio NON DEVE includere un corpo. deve essere inviata solo l'intestazione del messaggio, come specificato nella sezione 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="ea353-4291">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="ea353-4292">2.2.4 Errori</span><span class="sxs-lookup"><span data-stu-id="ea353-4292">2.2.4 Errors</span></span>

<span data-ttu-id="ea353-4293">Tutti i messaggi del protocollo del servizio di indicizzazione del contenuto DEVONO 0x00000000 se l'operazione ha esito positivo; In caso contrario, restituiscono un codice di errore diverso da zero a 32 bit che può essere un valore HRESULT o NTSTATUS (vedere la sezione 1.8).</span><span class="sxs-lookup"><span data-stu-id="ea353-4293">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="ea353-4294">Se un buffer è troppo piccolo per adattarsi a un risultato, deve essere restituito il codice di stato STATUS \_ INSUFFICIENT RESOURCES (0xC0000009A) e l'operazione non riuscita deve essere ritentata con un buffer più \_ grande.</span><span class="sxs-lookup"><span data-stu-id="ea353-4294">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="ea353-4295">Tutti gli altri valori di errore DEVONO essere considerati uguali.</span><span class="sxs-lookup"><span data-stu-id="ea353-4295">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="ea353-4296">Si noti che attualmente gli spazi di numerazione HRESULT e NTSTATUS non si sovrappongono se non con valori di significato identico, ma anche se dovevano essere conflitti in futuro, non causerebbe problemi di protocollo purché il valore per STATUS \_ RISORSE \_ INSUFFICIENTI rimane univoca, poiché tutti gli altri valori di errore vengono considerati uguali.</span><span class="sxs-lookup"><span data-stu-id="ea353-4296">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="ea353-4297">3 Dettagli del protocollo</span><span class="sxs-lookup"><span data-stu-id="ea353-4297">3 Protocol Details</span></span>

-   [<span data-ttu-id="ea353-4298">3.1 Dettagli server</span><span class="sxs-lookup"><span data-stu-id="ea353-4298">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="ea353-4299">3.2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="ea353-4299">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="ea353-4300">Le richieste di messaggi CISP per l'esecuzione di query in remoto nei cataloghi del servizio di indicizzazione non richiedono alcuna sequenza specifica.</span><span class="sxs-lookup"><span data-stu-id="ea353-4300">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="ea353-4301">È tuttavia consigliabile che il livello superiore rispetti una sequenza di messaggi significativa, ad esempio per i messaggi ricevuti da questa sequenza o con dati non validi, il server risponderà con un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4301">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="ea353-4302">Alcuni messaggi dipendono anche dal livello superiore che fornisce dati validi ricevuti nei messaggi in precedenza nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="ea353-4302">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="ea353-4303">Una sequenza di messaggi tipica per una query semplice da un client a un computer remoto è illustrata nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4303">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![sequenza di messaggi per query semplice](images/protocoldetails.jpg)

<span data-ttu-id="ea353-4305">I messaggi rappresentati nel diagramma precedente rappresentano un subset di tutti i messaggi CISP usati per l'esecuzione di query su un catalogo del servizio di indicizzazione remoto.</span><span class="sxs-lookup"><span data-stu-id="ea353-4305">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="ea353-4306">3.1 Dettagli server</span><span class="sxs-lookup"><span data-stu-id="ea353-4306">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="ea353-4307">3.1.1 Modello di dati astratto</span><span class="sxs-lookup"><span data-stu-id="ea353-4307">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="ea353-4308">La sezione seguente specifica i dati e lo stato gestiti dal server CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-4308">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="ea353-4309">I dati forniti qui sono per facilitare la spiegazione del comportamento del protocollo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4309">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="ea353-4310">Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il comportamento esterno sia coerente con quello descritto in questo documento.</span><span class="sxs-lookup"><span data-stu-id="ea353-4310">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="ea353-4311">Un servizio di indicizzazione che implementa CISP DEVE mantenere gli elementi di dati astratti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4311">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="ea353-4312">Elenco dei client connessi al server</span><span class="sxs-lookup"><span data-stu-id="ea353-4312">The list of clients connected to the server</span></span>
-   <span data-ttu-id="ea353-4313">Informazioni su ogni client, tra cui:</span><span class="sxs-lookup"><span data-stu-id="ea353-4313">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="ea353-4314">Versione del client (come indicato nel messaggio CPMConnectIn specificato nella sezione 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="ea353-4314">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="ea353-4315">Catalogo associato al client (tramite un messaggio CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="ea353-4315">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="ea353-4316">Proprietà client aggiuntive, come specificato nella sezione 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-4316">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="ea353-4317">Query di ricerca del client</span><span class="sxs-lookup"><span data-stu-id="ea353-4317">Client's search query</span></span>
    -   <span data-ttu-id="ea353-4318">Elenco di handle di cursore per la query e la posizione nel set di risultati per ogni handle.</span><span class="sxs-lookup"><span data-stu-id="ea353-4318">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="ea353-4319">Set corrente di associazioni</span><span class="sxs-lookup"><span data-stu-id="ea353-4319">Current set of bindings</span></span>
    -   <span data-ttu-id="ea353-4320">Stato corrente della query che include (per ogni cursore):</span><span class="sxs-lookup"><span data-stu-id="ea353-4320">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="ea353-4321">Numero di righe nel risultato della query</span><span class="sxs-lookup"><span data-stu-id="ea353-4321">Number of rows in query result</span></span>
        -   <span data-ttu-id="ea353-4322">Numeratore e denominatore del completamento delle query</span><span class="sxs-lookup"><span data-stu-id="ea353-4322">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="ea353-4323">Ultimo numero di righe, segnalato dal messaggio CPMRatioFinishedOut più recente per questo cursore</span><span class="sxs-lookup"><span data-stu-id="ea353-4323">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="ea353-4324">Se la query viene monitorata dal server per le modifiche nei risultati della query e se viene monitorata, cosa è cambiato nei risultati della query dall'ultima volta che è stata segnalata al client da CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4324">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="ea353-4325">Elenco di handle di capitolo, serviti da questa query a un client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4325">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="ea353-4326">Elenco di handle di segnalibro per ogni cursore, serviti da questa query a un client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4326">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="ea353-4327">Stato corrente del servizio di indicizzazione, che può essere "non inizializzato", "in esecuzione" o "in fase di arresto".</span><span class="sxs-lookup"><span data-stu-id="ea353-4327">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="ea353-4328">Si noti che la maggior parte del server di ora è in stato "in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="ea353-4328">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="ea353-4329">Di seguito è riportato il diagramma della macchina a stati per il server:</span><span class="sxs-lookup"><span data-stu-id="ea353-4329">Following is the state machine diagram for the server:</span></span>

    ![diagramma della macchina a stati del server del servizio di indicizzazione](images/abstractdatamodel.jpg)

-   <span data-ttu-id="ea353-4331">Informazioni per catalogo: numero di documenti indicizzati, dimensioni dell'indice, numero di chiavi univoche e così via (vedere la sezione 2.2.3.1 per l'elenco completo), stato (che corrisponde ai valori di dwNewState nella sezione 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="ea353-4331">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="ea353-4332">Per ogni lingua supportata, un database di varianti di parole come descritto nella sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="ea353-4332">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="ea353-4333">3.1.2 Timer</span><span class="sxs-lookup"><span data-stu-id="ea353-4333">3.1.2 Timers</span></span>

<span data-ttu-id="ea353-4334">Non sono necessari timer di protocollo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4334">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="ea353-4335">3.1.3 Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="ea353-4335">3.1.3 Initialization</span></span>

<span data-ttu-id="ea353-4336">Al momento dell'inizializzazione, il server DEVE impostare lo stato su "non inizializzato" e avviare l'ascolto dei messaggi named pipe specificato nella sezione 1.9.</span><span class="sxs-lookup"><span data-stu-id="ea353-4336">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="ea353-4337">Dopo aver eseguito qualsiasi altra inizializzazione interna, deve passare allo stato "in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="ea353-4337">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="ea353-4338">3.1.4 Eventi attivati di livello più alto</span><span class="sxs-lookup"><span data-stu-id="ea353-4338">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="ea353-4339">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="ea353-4339">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="ea353-4340">3.1.5 Regole di elaborazione e sequenziazione dei messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-4340">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="ea353-4341">Ogni volta che si verifica un errore durante l'elaborazione di un messaggio inviato da un client, il server DEVE segnalare un errore al client nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ea353-4341">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="ea353-4342">Interrompere l'elaborazione del messaggio inviato dal client</span><span class="sxs-lookup"><span data-stu-id="ea353-4342">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="ea353-4343">Rispondere con l'intestazione del messaggio (solo) del messaggio inviato dal client, mantenendo \_ intatto il campo msg.</span><span class="sxs-lookup"><span data-stu-id="ea353-4343">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="ea353-4344">Impostare il \_ campo dello stato sul valore del codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4344">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="ea353-4345">Quando arriva un messaggio, il server DEVE controllare il valore del campo msg per verificare se è un tipo noto (vedere la sezione \_ 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="ea353-4345">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="ea353-4346">Se il tipo non è noto, deve segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4346">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="ea353-4347">Il server DEVE quindi convalidare il \_ valore del campo ulChecksum se il tipo di messaggio è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4347">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="ea353-4348">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="ea353-4348">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="ea353-4349">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="ea353-4349">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="ea353-4350">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="ea353-4350">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="ea353-4351">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="ea353-4351">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="ea353-4352">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="ea353-4352">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="ea353-4353">Per convalidare il valore del campo ulChecksum, il server DEVE controllare il valore specificato nel \_ campo \_ iClientVersion nel messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4353">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="ea353-4354">Se il campo iClientVersion non è impostato su 0x00000008 e il campo ulChecksum non è impostato su 0x00000000, il server DEVE segnalare un errore \_ \_ STATUS INVALID PARAMETER \_ \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4354">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="ea353-4355">Il server NON DEVE convalidare il campo ulChecksum per i client e imposta il campo iClientVersion su un valore minore \_ \_ di 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="ea353-4355">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="ea353-4356">Se il valore del campo iClientVersionfield è 0x00000008 o superiore, il server DEVE convalidare che il campo ulChecksum sia stato calcolato come specificato nella sezione \_ \_ 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="ea353-4356">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="ea353-4357">Se il \_ valore ulChecksum non è valido, il server DEVE segnalare un errore STATUS \_ INVALID PARAMETER \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4357">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="ea353-4358">Successivamente, il server controlla in quale stato si trova.</span><span class="sxs-lookup"><span data-stu-id="ea353-4358">Next, the server checks which state is it in.</span></span> <span data-ttu-id="ea353-4359">Se lo stato è "non inizializzato", il server DEVE segnalare un errore CI \_ E \_ NOT \_ INITIALIZED (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="ea353-4359">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="ea353-4360">Se lo stato è "arresto" il server DEVE segnalare un errore CI \_ E \_ SHUTDOWN (0x80041812).</span><span class="sxs-lookup"><span data-stu-id="ea353-4360">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="ea353-4361">Dopo che un'intestazione è stata determinata come valida e il server è in stato di "esecuzione", è necessario eseguire un'ulteriore elaborazione specifica del messaggio come specificato nelle sottosezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-4361">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="ea353-4362">3.1.5.1 Gestione remota del catalogo del servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="ea353-4362">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="ea353-4363">3.1.5.1.1 Ricezione di una richiesta CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4363">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="ea353-4364">Quando il server riceve una richiesta di messaggio CPMCIStateInOut dal client, il server DEVE prima controllare se il client è in un elenco di client connessi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4364">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="ea353-4365">Se il client non è presente nell'elenco, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4365">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="ea353-4366">In caso contrario, DEVE rispondere al client con un messaggio CPMCIStateInOut, inserendo le informazioni sul catalogo associato del client, come specificato nella sezione 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-4366">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="ea353-4367">3.1.5.1.2 Ricezione di una richiesta CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4367">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="ea353-4368">Quando il server riceve una richiesta di messaggio CPMSetCatStateIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4368">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4369">Verificare che il client abbia accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4369">Check that client has administrative access.</span></span> <span data-ttu-id="ea353-4370">Se il client non ha accesso amministrativo, il server DEVE segnalare un errore STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="ea353-4370">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="ea353-4371">Se dwNewState non è uguale a CICAT ALL OPENED, modificare lo stato del catalogo specificato nel campo CatName come specificato dal \_ \_ campo \_ \_ dwNewState.</span><span class="sxs-lookup"><span data-stu-id="ea353-4371">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="ea353-4372">Per altre informazioni, vedere la sezione 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="ea353-4372">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="ea353-4373">Se il server non individua un catalogo con il nome specificato nel campo CatName, il server DEVE restituire un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4373">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4374">Rispondere al client con un messaggio CPMSetCatStateOut, in cui \_ dwOldState DEVE essere impostato sullo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4374">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="ea353-4375">Se dwNewState è uguale a CICAT ALL OPENED, il server DEVE controllare lo stato di tutti i cataloghi e, se tutti sono avviati, DEVE impostare dwOldState su 0x00000001 e in caso contrario impostare \_ \_ \_ \_ \_ dwOldState su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4375">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="ea353-4376">3.1.5.1.3 Ricezione di una richiesta CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4376">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="ea353-4377">Quando il server riceve una richiesta di messaggio CPMUpdateDocumentsIn, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4377">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4378">Controllare se il client è in un elenco di client connessi (a cui è associato un catalogo).</span><span class="sxs-lookup"><span data-stu-id="ea353-4378">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="ea353-4379">Se il client non è presente nell'elenco, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4379">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4380">Verificare che il client abbia accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4380">Check that client has administrative access.</span></span> <span data-ttu-id="ea353-4381">Se il client non ha accesso amministrativo al server, il server DEVE segnalare un errore STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="ea353-4381">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="ea353-4382">Avviare il processo di indicizzazione del percorso specificato dal client, eseguendo un'analisi completa o incrementale, a seconda del valore del campo flag nel messaggio \_ CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4382">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="ea353-4383">Se il percorso non è stato indicizzato in precedenza, deve essere aggiunto alla raccolta di percorsi indicizzati e viene eseguita un'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="ea353-4383">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="ea353-4384">Se viene specificato un valore non valido del campo flag, il server DEVE agire come se il flag fosse impostato su \_ \_ UPD \_ INIT ed eseguire un'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="ea353-4384">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="ea353-4385">Questa operazione DEVE essere eseguita nel catalogo associato al client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4385">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="ea353-4386">Rispondere al client con l'intestazione del messaggio per CPMUpdateDocumentsIn e impostare il campo dello stato sui \_ risultati della richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea353-4386">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="ea353-4387">3.1.5.1.4 Ricezione di una richiesta CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4387">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="ea353-4388">Quando il server riceve una richiesta di messaggio CPMForceMergeIn, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4388">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4389">Controllare se il client è in un elenco di client connessi (a cui è associato un catalogo).</span><span class="sxs-lookup"><span data-stu-id="ea353-4389">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="ea353-4390">Se il client non è presente nell'elenco, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4390">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4391">Verificare che il client abbia accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4391">Check that client has administrative access.</span></span> <span data-ttu-id="ea353-4392">Se il client non ha accesso amministrativo, il server DEVE segnalare un errore STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="ea353-4392">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="ea353-4393">Avviare qualsiasi processo di manutenzione necessario per migliorare le prestazioni delle query in un catalogo, associato al client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4393">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="ea353-4394">Rispondere al client con un'intestazione di messaggio per CPMForceMergeIn e impostare il campo dello stato sui \_ risultati della richiesta.</span><span class="sxs-lookup"><span data-stu-id="ea353-4394">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="ea353-4395">Si noti che il processo di manutenzione è asincrono e può continuare dopo che il client ha ricevuto il messaggio di risposta.</span><span class="sxs-lookup"><span data-stu-id="ea353-4395">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="ea353-4396">Questo processo non influisce direttamente sul protocollo in alcun modo (oltre al tempo di risposta).</span><span class="sxs-lookup"><span data-stu-id="ea353-4396">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="ea353-4397">3.1.5.2 Query del servizio di indicizzazione remoto</span><span class="sxs-lookup"><span data-stu-id="ea353-4397">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="ea353-4398">3.1.5.2.1 Ricezione di una richiesta CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4398">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="ea353-4399">Quando il server riceve una richiesta CPMConnectIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4399">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4400">Controllare se il client è presente nell'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4400">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="ea353-4401">In questo caso, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4401">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4402">Verifica se il catalogo specificato esiste e non è in stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="ea353-4402">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="ea353-4403">Se questo non è il caso, il server DEVE segnalare un errore CI \_ E \_ NO CATALOG \_ (0x8004181D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4403">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="ea353-4404">Aggiungere il client all'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4404">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="ea353-4405">Associare il catalogo al client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4405">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="ea353-4406">Archiviare le informazioni passate nel messaggio CPMConnectIn (ad esempio nome del catalogo, versione client e così via) nello stato client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4406">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="ea353-4407">Rispondere al client con un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4407">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="ea353-4408">3.1.5.2.2 Ricezione di una richiesta CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4408">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="ea353-4409">Quando il server riceve una richiesta di messaggio CPMCreateQueryIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4409">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4410">Controllare se il client è presente nell'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4410">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="ea353-4411">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4411">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4412">Controllare se al client è già associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4412">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="ea353-4413">In questo caso, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4413">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4414">Controllare se il catalogo associato al client è nello stato che consente l'elaborazione delle query (CICAT \_ READONLY o CICAT \_ WRITABLE).</span><span class="sxs-lookup"><span data-stu-id="ea353-4414">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="ea353-4415">In caso contrario, il server DEVE segnalare un errore QUERY \_ S \_ NO QUERY \_ (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="ea353-4415">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="ea353-4416">Analizzare il set di restrizioni, gli ordinamenti e i raggruppamenti specificati nella query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4416">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="ea353-4417">Se il server rileva un errore, deve segnalare un errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="ea353-4417">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="ea353-4418">Se questo passaggio non riesce per qualsiasi altro motivo, il server DEVE segnalare l'errore rilevato.</span><span class="sxs-lookup"><span data-stu-id="ea353-4418">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="ea353-4419">Per informazioni sugli errori di query del servizio di indicizzazione, vedere \[ MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="ea353-4419">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="ea353-4420">Salvare la query di ricerca nello stato per il client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4420">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="ea353-4421">Eseguire le operazioni di preparazione necessarie per gestire le righe a un client e associare la query agli handle di cursore appropriati (a seconda delle informazioni passate nel messaggio CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="ea353-4421">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="ea353-4422">Aggiungere tali handle all'elenco di handle di cursore del client e inizializzare elenchi di handle di capitolo e segnalibri.</span><span class="sxs-lookup"><span data-stu-id="ea353-4422">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="ea353-4423">Inizializzare l'elenco di handle di capitolo per ogni cursore in questa query al database \_ NULL \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="ea353-4423">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="ea353-4424">Inizializzare l'elenco di handle di segnalibro per ogni cursore in questa query su un set di DBBMK \_ FIRST e DBBMK \_ LAST.</span><span class="sxs-lookup"><span data-stu-id="ea353-4424">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="ea353-4425">Contrassegnare la query come non monitorata per le modifiche.</span><span class="sxs-lookup"><span data-stu-id="ea353-4425">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="ea353-4426">Inizializzare il numero di righe sul numero attualmente calcolato di righe (che può essere 0 se la query non ha avviato l'esecuzione o un numero se la query è in un processo di esecuzione) e inizializzare il numeratore e il denominatore del completamento della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4426">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="ea353-4427">Rispondere al client con un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4427">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="ea353-4428">3.1.5.2.3 Ricezione di una richiesta CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4428">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="ea353-4429">Quando il server riceve una richiesta di messaggio CPMGetQueryStatusIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4429">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4430">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4430">Check if the client has query associated with it.</span></span> <span data-ttu-id="ea353-4431">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4431">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4432">Controllare se l'handle del cursore è in un elenco di handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4432">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="ea353-4433">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4433">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4434">Preparare un messaggio CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4434">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="ea353-4435">Il server DEVE recuperare lo stato della query corrente e impostarlo nel campo \_ QStatus (vedere 2.2.3.11 per i valori possibili).</span><span class="sxs-lookup"><span data-stu-id="ea353-4435">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="ea353-4436">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4436">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="ea353-4437">Rispondere al client con il messaggio CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4437">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="ea353-4438">3.1.5.2.4 Ricezione di una richiesta CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4438">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="ea353-4439">Quando il server riceve una richiesta di messaggio CPMGetQueryStatusExIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4439">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4440">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4440">Check if the client has a query associated with it.</span></span> <span data-ttu-id="ea353-4441">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4441">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4442">Controllare se l'handle di cursore passato è in un elenco di handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4442">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="ea353-4443">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4443">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4444">Preparare un messaggio CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4444">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="ea353-4445">Il server DEVE recuperare lo stato corrente della query e lo stato della query e impostare QStatus (vedere 2.2.3.11 per i valori \_ possibili), dwRatioFinishedDenominator e \_ dwRatioFinishedNumerator rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4445">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="ea353-4446">Deve quindi impostare il numero di righe nei risultati della query su \_ cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="ea353-4446">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="ea353-4447">Se questo passaggio ha esito negativo per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4447">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="ea353-4448">Recuperare informazioni sul catalogo del client e \_ compilare cFilteredDocuments e \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="ea353-4448">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="ea353-4449">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4449">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="ea353-4450">Recuperare la posizione del segnalibro indicato dall'handle nel campo bmk e compilare il campo iRowBmk rimanente nel messaggio \_ \_ CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4450">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="ea353-4451">Se questo passaggio ha esito negativo per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4451">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="ea353-4452">Rispondere al client con il messaggio CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4452">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="ea353-4453">3.1.5.2.5 Ricezione di una richiesta CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4453">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="ea353-4454">Quando il server riceve una richiesta di messaggio CPMRatioFinishedIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4454">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4455">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4455">Check if the client has query associated with it.</span></span> <span data-ttu-id="ea353-4456">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4456">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4457">Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4457">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="ea353-4458">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4458">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4459">Preparare un messaggio CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4459">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="ea353-4460">Il server DEVE recuperare lo stato della query del client e compilare i campi \_ ulNumerator, \_ ulDenominator \_ e cRows.</span><span class="sxs-lookup"><span data-stu-id="ea353-4460">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="ea353-4461">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4461">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="ea353-4462">Se cRows è uguale all'ultimo numero segnalato di righe per la query, impostare \_ fNewRows su 0x00000000, in caso contrario impostarlo \_ su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-4462">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="ea353-4463">Aggiornare l'ultimo numero segnalato di righe per questa query al valore \_ di cRows.</span><span class="sxs-lookup"><span data-stu-id="ea353-4463">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="ea353-4464">Rispondere al client con il messaggio CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4464">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="ea353-4465">3.1.5.2.6 Ricezione di una richiesta CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4465">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="ea353-4466">Quando il server riceve una richiesta di messaggio CPMSetBindingsIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4466">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4467">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4467">Check if the client has a query associated with it.</span></span> <span data-ttu-id="ea353-4468">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4468">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4469">Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4469">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="ea353-4470">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4470">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4471">Verificare che le informazioni sulle associazioni siano valide (ad esempio, la colonna specifica almeno il valore, la lunghezza o lo stato da restituire; nessuna sovrapposizione nelle associazioni per valore, lunghezza o stato; e valore, lunghezza e stato si adattano alle dimensioni della riga specificate) e, in caso contrario, segnalare un errore \_ DB E \_ BADBINDINFO (0x80040E08).</span><span class="sxs-lookup"><span data-stu-id="ea353-4471">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="ea353-4472">Salvare le informazioni di associazione associate alle colonne specificate nel campo aColumns.</span><span class="sxs-lookup"><span data-stu-id="ea353-4472">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="ea353-4473">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4473">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="ea353-4474">Rispondere al client con un'intestazione del messaggio (solo) con msg impostato su CPMSetBindingsIn e stato impostato sui risultati \_ \_ dell'associazione specificata.</span><span class="sxs-lookup"><span data-stu-id="ea353-4474">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="ea353-4475">3.1.5.2.7 Ricezione di una richiesta CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4475">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="ea353-4476">Quando il server riceve una richiesta di messaggio CPMGetRowsIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4476">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4477">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4477">Check if the client has query associated with it.</span></span> <span data-ttu-id="ea353-4478">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4478">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4479">Controllare se l'handle di cursore passato è in athelist degli handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4479">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="ea353-4480">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4480">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4481">Controllare se il client ha un set corrente di associazioni.</span><span class="sxs-lookup"><span data-stu-id="ea353-4481">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="ea353-4482">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4482">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4483">Preparare un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4483">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="ea353-4484">Il server DEVE posizionare il cursore nei risultati della query come indicato dalla descrizione della ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-4484">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="ea353-4485">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4485">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="ea353-4486">Recuperare tutte le righe che si adattano a un buffer, le cui dimensioni sono indicate da cbReadBuffer, ma non più di quanto indicato \_ da \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="ea353-4486">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="ea353-4487">Quando si recuperano righe, il server DEVE confrontare il tipo di valore della proprietà di ogni colonna selezionata con il tipo specificato nel set corrente di associazioni del client (sezione 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="ea353-4487">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="ea353-4488">Se il tipo nell'associazione non è VT VARIANT, il server DEVE tentare di convertire il valore della proprietà della colonna \_ in tale tipo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4488">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="ea353-4489">In caso contrario, se il flag DBPROP USEEXTENDEDDBTYPES è impostato nel set di proprietà DBPROPSET QUERYEXT del client o se il valore della proprietà della colonna non è un \_ tipo VT VECTOR, il valore della proprietà DEVE essere restituito nel \_ \_ tipo normale.</span><span class="sxs-lookup"><span data-stu-id="ea353-4489">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="ea353-4490">In caso contrario, il server deve tentare di convertirlo in un tipo VT ARRAY come \_ \_ \_ segue: VT \_ I8, VT \_ UI8, VT FILETIME e gli elementi di matrice \_ CLSID VT \_ non possono essere convertiti e hanno invece esito negativo. Gli elementi della matrice \_ VT LPSTR e VT LPWSTR DEVONO essere convertiti in VT BSTR. Gli elementi di matrice di tutti gli altri tipi \_ \_ DEVONO rimanere invariati.</span><span class="sxs-lookup"><span data-stu-id="ea353-4490">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="ea353-4491">Infine, se le colonne di riga contengono handle di capitolo o segnalibri, il server DEVE aggiornare gli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-4491">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="ea353-4492">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4492">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="ea353-4493">Archiviare il numero effettivo di righe recuperate in \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="ea353-4493">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="ea353-4494">Copiare il campo della descrizione della ricerca e del capitolo da CPMGetRowsIn in un messaggio CPMGetRowsOut da inviare.</span><span class="sxs-lookup"><span data-stu-id="ea353-4494">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="ea353-4495">Archiviare le righe recuperate nel campo Righe (vedere la nota sul byte di stato sotto e la sezione 2.2.3.16 nella struttura del campo Righe).</span><span class="sxs-lookup"><span data-stu-id="ea353-4495">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="ea353-4496">Rispondere al client con il messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4496">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="ea353-4497">Nota sul campo byte di stato:</span><span class="sxs-lookup"><span data-stu-id="ea353-4497">Note on status byte field:</span></span>

<span data-ttu-id="ea353-4498">Se StatusUsed è impostato su 0x01 nella colonna CTableColumn del messaggio CPMSetBindingIn per la colonna, il server DEVE impostare il byte di stato (che si trova in StatusOffset dall'inizio della riga) per questa colonna su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4498">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="ea353-4499">Valore</span><span class="sxs-lookup"><span data-stu-id="ea353-4499">Value</span></span> | <span data-ttu-id="ea353-4500">Significato</span><span class="sxs-lookup"><span data-stu-id="ea353-4500">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="ea353-4501">0x00</span><span class="sxs-lookup"><span data-stu-id="ea353-4501">0x00</span></span>  | <span data-ttu-id="ea353-4502">StatusOK</span><span class="sxs-lookup"><span data-stu-id="ea353-4502">StatusOK</span></span>       |
| <span data-ttu-id="ea353-4503">0x01</span><span class="sxs-lookup"><span data-stu-id="ea353-4503">0x01</span></span>  | <span data-ttu-id="ea353-4504">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="ea353-4504">StatusDeferred</span></span> |
| <span data-ttu-id="ea353-4505">0x02</span><span class="sxs-lookup"><span data-stu-id="ea353-4505">0x02</span></span>  | <span data-ttu-id="ea353-4506">StatusNull</span><span class="sxs-lookup"><span data-stu-id="ea353-4506">StatusNull</span></span>     |



 

<span data-ttu-id="ea353-4507">Se il valore della proprietà è assente per questa riga, il server DEVE impostare il byte di stato su StatusNull.</span><span class="sxs-lookup"><span data-stu-id="ea353-4507">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="ea353-4508">Se il valore è troppo grande per essere trasferito nel messaggio CPMGetRowsOut, il server DEVE impostare il byte di stato su StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="ea353-4508">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="ea353-4509">In caso contrario, il server DEVE impostare il byte di stato su StatusOK.</span><span class="sxs-lookup"><span data-stu-id="ea353-4509">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="ea353-4510">3.1.5.2.8 Ricezione di una richiesta CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4510">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="ea353-4511">Quando il server riceve una richiesta di messaggio CPMFetchValueIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4511">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4512">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4512">Check if the client has query associated with it.</span></span> <span data-ttu-id="ea353-4513">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4513">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4514">Preparare un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4514">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="ea353-4515">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4515">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="ea353-4516">Trovare il documento indicato dal campo wid e verificare se l'ID proprietà per questo documento (in seguito indicato come "valore della proprietà") indicato dalla struttura PropSpec è disponibile per \_ questo client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4516">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="ea353-4517">Se questo valore non è disponibile, il server DEVE impostare fValueExists su 0x00000000 e in caso contrario impostare \_ \_ fValueExists su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-4517">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="ea353-4518">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="ea353-4519">Se \_ fValueExists è uguale a 0x00000001 il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4519">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="ea353-4520">Serializzare il valore della proprietà in una struttura SERIALIZEDPROPERTYVALUE e copiare, a partire \_ dall'offset cbSoFar, al massimo byte cbChunk (ma non oltre la fine della proprietà serializzata) nel campo \_ vValue.</span><span class="sxs-lookup"><span data-stu-id="ea353-4520">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="ea353-4521">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4521">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="ea353-4522">Impostare \_ cbValue sul numero di byte copiati nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4522">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="ea353-4523">Impostare vType sul tipo di proprietà del valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-4523">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="ea353-4524">Se la lunghezza della proprietà serializzata è maggiore di \_ cbSoFar aggiunta a \_ cbValue, impostare fMoreExists su 0x00000001, in caso contrario impostarla su \_ 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4524">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="ea353-4525">Rispondere al client con il messaggio CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4525">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="ea353-4526">3.1.5.2.9 Ricezione di una richiesta CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="ea353-4526">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="ea353-4527">Quando il server riceve un messaggio CPMGetNotify da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4527">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4528">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4528">Check if the client has query associated with it.</span></span> <span data-ttu-id="ea353-4529">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4529">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4530">Se non sono state apportate modifiche al set di risultati della query dopo l'ultimo messaggio CPMSendNotifyOut per questo client o se la query non è attualmente monitorata per le modifiche nel set di risultati, il server DEVE rispondere con il messaggio CPMGetNotify e iniziare a monitorare la query per le modifiche nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="ea353-4530">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="ea353-4531">Se in un secondo momento è presente una modifica nel set di risultati della query, il server DEVE inviare esattamente un messaggio CPMSendNotifyOut al client e DEVE specificare la modifica nel campo \_ watchNotify.</span><span class="sxs-lookup"><span data-stu-id="ea353-4531">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="ea353-4532">Se sono state apportate modifiche al set di risultati della query dopo l'ultimo messaggio CPMSendNotifyOut, il server DEVE rispondere con CPMSendNotifyOut e DEVE specificare la modifica nel campo \_ watchNotify.</span><span class="sxs-lookup"><span data-stu-id="ea353-4532">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="ea353-4533">Si noti che, nel caso di molte modifiche ai risultati della query, DBWATCHNOTIFY ROWSCHANGED ha la priorità ,ad esempio, se la query è stata eseguita, eseguita di nuovo e quindi il numero di righe modificate e la query è stata eseguita di nuovo, l'evento segnalato sarà \_ DBWATCHNOTIFY \_ ROWSCHANGED.</span><span class="sxs-lookup"><span data-stu-id="ea353-4533">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="ea353-4534">3.1.5.2.10 Ricezione di una richiesta CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4534">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="ea353-4535">Quando il server riceve una richiesta di messaggio CPMGetApproximatePositionIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4535">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4536">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4536">Check if the client has a query associated with it.</span></span> <span data-ttu-id="ea353-4537">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4537">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4538">Controllare se l'handle del cursore, l'handle del capitolo e l'handle del segnalibro passati si trova negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-4538">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="ea353-4539">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4539">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4540">Trovare una riga associata all'handle del segnalibro nei risultati della query e approssimare la posizione della riga nel set di righe, a cui fa riferimento l'handle del capitolo, e determinare il numeratore e il denominatore per la posizione.</span><span class="sxs-lookup"><span data-stu-id="ea353-4540">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="ea353-4541">Si noti che quando l'handle del capitolo è DB \_ NULL HCHAPTER, il capitolo corrispondente è il set di righe \_ principale della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4541">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="ea353-4542">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4542">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="ea353-4543">Rispondere al client con un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4543">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="ea353-4544">3.1.5.2.11 Ricezione di una richiesta CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4544">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="ea353-4545">Quando il server riceve una richiesta di messaggio CPMCompareBmkIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4545">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4546">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4546">Check if the client has a query associated with it.</span></span> <span data-ttu-id="ea353-4547">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4547">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4548">Controllare se l'handle del cursore, l'handle del capitolo e gli handle dei segnalibri passati sono presenti negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-4548">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="ea353-4549">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4549">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4550">Preparare un messaggio CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4550">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="ea353-4551">Se gli handle dei segnalibri sono uguali, \_ dwComparison MUST è impostato su DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="ea353-4551">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="ea353-4552">In caso contrario, se uno degli handle di segnalibri è DBBMK FIRST o \_ DBBMK \_ LAST, \_ dwComparison DEVE essere impostato su DBCOMPARE \_ NE.</span><span class="sxs-lookup"><span data-stu-id="ea353-4552">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="ea353-4553">In caso contrario, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4553">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="ea353-4554">Trovare le righe a cui fa riferimento ogni handle di segnalibro nei risultati della query</span><span class="sxs-lookup"><span data-stu-id="ea353-4554">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="ea353-4555">Se una delle righe non si trova nel capitolo indicato dall'handle del capitolo in CPMCompareBmkIn, \_ dwComparison DEVE essere impostato su DBCOMPARE \_ NOTCOMPARABLE.</span><span class="sxs-lookup"><span data-stu-id="ea353-4555">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="ea353-4556">In caso contrario, quando entrambe le righe sono nello stesso capitolo, il server DEVE approssimare una posizione di tali righe nel set di righe a cui fa riferimento l'handle di questo capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4556">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="ea353-4557">DEVE quindi confrontare i valori di posizione e impostare dwComparison su DBCOMPARE LT se la posizione della prima riga è minore della posizione della seconda riga; in caso \_ \_ \_ contrario, dwComparison MUST deve essere impostato su DBCOMPARE \_ GT.</span><span class="sxs-lookup"><span data-stu-id="ea353-4557">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="ea353-4558">Rispondere al client con il messaggio CPMCompareBmkOut compilato.</span><span class="sxs-lookup"><span data-stu-id="ea353-4558">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="ea353-4559">3.1.5.2.12 Ricezione di una richiesta CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4559">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="ea353-4560">Quando il server riceve la richiesta di messaggio CPMRestartPositionIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4560">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4561">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4561">Check if the client has a query associated with it.</span></span> <span data-ttu-id="ea353-4562">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4562">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4563">Controllare se l'handle del cursore e l'handle di capitolo passati si trova negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-4563">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="ea353-4564">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4564">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4565">Spostare il cursore all'inizio del capitolo, identificato dall'handle del capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4565">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="ea353-4566">Si noti che quando l'handle del capitolo è DB \_ NULL HCHAPTER, il capitolo corrispondente è il set di righe \_ principale della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4566">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="ea353-4567">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4567">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="ea353-4568">Rispondere al client con un messaggio CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4568">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="ea353-4569">3.1.5.2.13 Ricezione di una richiesta CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4569">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="ea353-4570">Quando il server riceve una richiesta di messaggio CPMFreeCursorIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4570">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4571">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4571">Check if the client has a query associated with it.</span></span> <span data-ttu-id="ea353-4572">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="ea353-4572">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="ea353-4573">Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4573">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="ea353-4574">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="ea353-4574">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="ea353-4575">Rilasciare il cursore e le risorse associate (vedere la sezione 3.1.1 per l'elenco completo) per questo handle di cursore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4575">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="ea353-4576">Rimuovere il cursore dall'elenco di cursori per il client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4576">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="ea353-4577">Rispondere con un messaggio CPMFreeCursorOut, impostando il campo \_ cCursorsRemaining con il numero di cursori rimanenti.</span><span class="sxs-lookup"><span data-stu-id="ea353-4577">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="ea353-4578">nell'elenco di questo client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4578">in this client's list.</span></span>
-   <span data-ttu-id="ea353-4579">Se non sono presenti altri cursori per questo client, il server DEVE rilasciare la query e le risorse associate (vedere la sezione 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="ea353-4579">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="ea353-4580">3.1.5.2.14 Ricezione di una richiesta CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="ea353-4580">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="ea353-4581">Quando il server riceve una richiesta di messaggio CPMDisconnect dal client, il server DEVE rimuovere il client dall'elenco dei client connessi e rilasciare tutte le risorse associate al client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4581">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="ea353-4582">3.1.6 Eventi timer</span><span class="sxs-lookup"><span data-stu-id="ea353-4582">3.1.6 Timer Events</span></span>

<span data-ttu-id="ea353-4583">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="ea353-4583">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="ea353-4584">3.1.7 Altri eventi locali</span><span class="sxs-lookup"><span data-stu-id="ea353-4584">3.1.7 Other Local Events</span></span>

<span data-ttu-id="ea353-4585">Quando il server viene arrestato, deve prima passare allo stato di arresto.</span><span class="sxs-lookup"><span data-stu-id="ea353-4585">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="ea353-4586">Deve quindi arrestare l'ascolto della pipe, eseguire qualsiasi altra attività di arresto specifica dell'implementazione e quindi passare allo stato "arrestato".</span><span class="sxs-lookup"><span data-stu-id="ea353-4586">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="ea353-4587">3.2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="ea353-4587">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="ea353-4588">3.2.1 Modello di dati astratto</span><span class="sxs-lookup"><span data-stu-id="ea353-4588">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="ea353-4589">La sezione seguente specifica i dati e lo stato gestiti dal client Content Indexing Service Protocol.</span><span class="sxs-lookup"><span data-stu-id="ea353-4589">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="ea353-4590">I dati forniti sono per facilitare la spiegazione del comportamento del protocollo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4590">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="ea353-4591">Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il comportamento esterno sia coerente con quello descritto in questo documento.</span><span class="sxs-lookup"><span data-stu-id="ea353-4591">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="ea353-4592">Un client ha lo stato astratto seguente:</span><span class="sxs-lookup"><span data-stu-id="ea353-4592">A client has the following abstract state:</span></span>

-   <span data-ttu-id="ea353-4593">**Ultimo messaggio inviato:** copia dell'ultimo messaggio inviato al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4593">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="ea353-4594">**Valore proprietà corrente:** valore parziale di una proprietà "posticipata", che è in corso di recupero.</span><span class="sxs-lookup"><span data-stu-id="ea353-4594">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="ea353-4595">**Byte correnti ricevuti:** numero di byte ricevuti finora per il valore della proprietà corrente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4595">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="ea353-4596">**Stato connessione named pipe:** connessione al server</span><span class="sxs-lookup"><span data-stu-id="ea353-4596">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="ea353-4597">3.2.2 Timer</span><span class="sxs-lookup"><span data-stu-id="ea353-4597">3.2.2 Timers</span></span>

<span data-ttu-id="ea353-4598">Non sono necessari timer di protocollo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4598">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="ea353-4599">3.2.3 Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="ea353-4599">3.2.3 Initialization</span></span>

<span data-ttu-id="ea353-4600">Non viene eseguita alcuna azione fino a quando non viene ricevuta una richiesta di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4600">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="ea353-4601">3.2.4 Higher-Layer eventi attivati</span><span class="sxs-lookup"><span data-stu-id="ea353-4601">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="ea353-4602">Quando una richiesta viene ricevuta da un livello superiore, il client DEVE creare una connessione named pipe al server usando i dettagli specificati nella sezione 2.1.</span><span class="sxs-lookup"><span data-stu-id="ea353-4602">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="ea353-4603">Se non è possibile eseguire questa operazione, la richiesta di livello superiore DEVE non essere riuscita.</span><span class="sxs-lookup"><span data-stu-id="ea353-4603">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="ea353-4604">In caso di errore di connessione, è quindi responsabilità del livello superiore riprovare, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="ea353-4604">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="ea353-4605">Un'intestazione DEVE essere pre-impieto con i campi impostati come specificato nella sezione 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="ea353-4605">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="ea353-4606">Per i messaggi specificati come che richiedono un checksum diverso da zero, il \_ valore ulChecksum DEVE essere calcolato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4606">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="ea353-4607">Il contenuto del messaggio dopo il campo ulReserved2 nell'intestazione del messaggio DEVE essere interpretato come una sequenza di interi \_ a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-4607">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="ea353-4608">Il client DEVE calcolare la somma dei valori numerici specificati da questi numeri interi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4608">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="ea353-4609">Calcolare l'XOR bit per bit di questo valore con 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="ea353-4609">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="ea353-4610">Sottrarre il valore specificato da \_ msg dal valore restituito da XOR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-4610">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="ea353-4611">3.2.4.1 Gestione remota del catalogo del servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="ea353-4611">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="ea353-4612">Ogni messaggio viene attivato da una richiesta dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4612">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="ea353-4613">Non esiste alcuna sequenza di messaggi applicata dal client per le richieste di messaggi CISP per la gestione remota dei cataloghi, ma (ad eccezione di un messaggio CPMSetCatStateIn) il server risponderà con esito positivo solo se il client precedentemente connesso tramite un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4613">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="ea353-4614">3.2.4.1.1 Invio di una richiesta CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4614">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="ea353-4615">In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMCiStateInOut quando richiede informazioni sui servizi di indicizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4615">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="ea353-4616">Quando viene richiesto di inviare questo messaggio, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4616">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4617">Inviare un messaggio CPMCiStateInOut come specificato nella sezione 2.2.3.1 al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4617">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="ea353-4618">Attendere la ricezione del messaggio CPMCiStateInOut dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4618">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="ea353-4619">Segnalare il valore del campo di stato della risposta e, in caso di esito positivo, la struttura informativo \_ torna al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4619">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="ea353-4620">3.2.4.1.2 Invio di una richiesta CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4620">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="ea353-4621">In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMSetCatStateIn quando sono necessarie informazioni su un catalogo o su tutti i cataloghi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4621">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="ea353-4622">Per questo messaggio il livello superiore deve fornire al client del protocollo un valore per \_ dwNewState e, se necessario, il nome del catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4622">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="ea353-4623">Quando viene richiesto di inviare questo messaggio, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4623">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4624">Inviare un messaggio CPMSetCatStateIn come specificato nella versione 2.2.3.2 al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4624">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="ea353-4625">Attendere la ricezione di un messaggio CPMSetCatStateOut dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4625">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="ea353-4626">Segnalare il valore del campo status della risposta e, se ha avuto esito \_ positivo, \_ dwOldState torna al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4626">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="ea353-4627">3.2.4.1.3 Invio di una richiesta CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4627">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="ea353-4628">Il livello superiore richiede in genere di inviare questo messaggio quando è necessario aggiornare i documenti nel percorso esistente o aggiungere un nuovo percorso di file all'indice.</span><span class="sxs-lookup"><span data-stu-id="ea353-4628">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="ea353-4629">Il livello superiore è quindi quello di fornire il percorso e il tipo di un'analisi, specificata come nella sezione 2.2.3.4 in cui un aggiornamento incrementale o completo è destinato ai percorsi esistenti e la nuova inizializzazione è destinata ai nuovi percorsi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4629">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="ea353-4630">Per soddisfare la richiesta di livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4630">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4631">Inviare un messaggio CPMUpdateDocumentsIn come specificato nella sezione 2.2.3.4 al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4631">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="ea353-4632">Attendere la ricezione del messaggio CPMUpdateDocumentsIn dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4632">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="ea353-4633">Segnalare il valore del \_ campo di stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4633">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="ea353-4634">3.2.4.1.4 Invio di una richiesta CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4634">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="ea353-4635">In genere, il livello superiore richiede di inviare questo messaggio quando è necessario migliorare le prestazioni delle query o fa parte della manutenzione pianificata del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-4635">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="ea353-4636">Per gestire il livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4636">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4637">Inviare il messaggio CPMForceMergeIn come specificato dalla sezione 2.2.3.5 al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4637">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="ea353-4638">Attendere la ricezione di un messaggio CPMUpdateDocumentsIn dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4638">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="ea353-4639">Segnalare il valore del \_ campo di stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4639">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="ea353-4640">3.2.4.2 Messaggi di query del catalogo del servizio di indicizzazione remota</span><span class="sxs-lookup"><span data-stu-id="ea353-4640">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="ea353-4641">Ad eccezione di CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, esiste una relazione uno-a-uno tra i messaggi CISP e le richieste di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4641">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="ea353-4642">Per le due eccezioni indicate in precedenza, possono essere generati più messaggi dal client per soddisfare i requisiti di dimensione o per recuperare una proprietà completa.</span><span class="sxs-lookup"><span data-stu-id="ea353-4642">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="ea353-4643">Il livello superiore tiene in genere traccia di tutte le informazioni specifiche della query (ad esempio gli handle di cursore aperti, i valori validi per gli handle di segnalibro e capitolo, i valori wid per i valori delle proprietà posticipate e così via) e tiene traccia anche se il client si trova in uno stato connesso, ma questo non viene applicato in alcun modo dal client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4643">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="ea353-4644">A scopo illustrativo, la parte client del diagramma nella sezione 3 illustra questa sequenza per una query semplice del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-4644">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="ea353-4645">3.2.4.2.1 Invio di una richiesta CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4645">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="ea353-4646">Questo messaggio è in genere la prima richiesta dal livello superiore (come se il client non fosse connesso, il server avrà esito negativo per la maggior parte dei messaggi ad eccezione di CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="ea353-4646">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="ea353-4647">Il livello superiore fornisce al client del protocollo le informazioni necessarie per la connessione.</span><span class="sxs-lookup"><span data-stu-id="ea353-4647">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="ea353-4648">Per soddisfare il livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4648">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4649">Compilare il messaggio usando le informazioni fornite dal client di livello superiore (vedere la sezione 2.2.3.6) in \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 e aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="ea353-4649">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="ea353-4650">Impostare \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet e cExtPropSet come specificato nella versione 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="ea353-4650">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="ea353-4651">Impostare il checksum nel \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="ea353-4651">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="ea353-4652">Inviare il messaggio CPMConnectIn al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4652">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="ea353-4653">Attendere la ricezione di un messaggio CPMConnectOut dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4653">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="ea353-4654">Segnalare il valore del campo status della risposta e, se ha avuto esito \_ positivo, \_ serverVersion torna al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4654">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="ea353-4655">Per scopi informativi, è previsto che i livelli superiori eseereranno in genere le azioni seguenti al completamento della connessione, ma queste non vengono applicate dal client CISP:</span><span class="sxs-lookup"><span data-stu-id="ea353-4655">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="ea353-4656">Usare i messaggi di gestione del catalogo del servizio di indicizzazione remota per le attività amministrative</span><span class="sxs-lookup"><span data-stu-id="ea353-4656">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="ea353-4657">Usare una richiesta CPMCreateQueryIn per creare una query di ricerca allo scopo di recuperare i risultati dal catalogo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4657">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="ea353-4658">3.2.4.2.2 Invio di una richiesta CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4658">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="ea353-4659">Il livello superiore in genere fornirà informazioni per la creazione della query dopo la connessione del client del protocollo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4659">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="ea353-4660">Il livello superiore fornisce al client un set di restrizioni, un set di colonne, regole di ordinamento e set di categorizzazione (ognuna delle quali può essere omessa), proprietà del set di righe e struttura del mapper di ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea353-4660">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="ea353-4661">Quando questa richiesta viene ricevuta da un livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4661">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4662">Preparare un oggetto CPMCreateQueryOut come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="ea353-4662">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="ea353-4663">Se è presente un set di colonne, impostare CColumnsSetPreset su 0x01 e compilare il campo ColumnsSet.</span><span class="sxs-lookup"><span data-stu-id="ea353-4663">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="ea353-4664">Se sono presenti restrizioni, impostare CRestrictionPresent su 0x01 e compilare il campo Restrizione.</span><span class="sxs-lookup"><span data-stu-id="ea353-4664">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="ea353-4665">Se è presente un set di ordinamento, compilare il campo SortSet.</span><span class="sxs-lookup"><span data-stu-id="ea353-4665">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="ea353-4666">Se è presente un set di categorizzazione, impostare CSortSetPresent su 0x01 e compilare il campo CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="ea353-4666">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="ea353-4667">Impostare il resto dei campi come specificato nella versione 2.2.3.8</span><span class="sxs-lookup"><span data-stu-id="ea353-4667">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="ea353-4668">Calcolare \_ il campo ulCheckSum nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="ea353-4668">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="ea353-4669">Inviare il messaggio CPMCreateQueryIn al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4669">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="ea353-4670">Attendere la ricezione del messaggio CPMCreateQueryOut (vedere i dettagli nella sezione 3.2.5.1.1), rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4670">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="ea353-4671">Segnalare il valore del campo di stato della risposta e, se ha avuto esito positivo, la matrice di handle di cursore e i valori booleani informativi (come specificato \_ nella 2.2.3.9) di nuovo al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4671">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="ea353-4672">3.2.4.2.3 Invio di una richiesta CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4672">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="ea353-4673">In genere, il livello superiore imposta le associazioni per ogni colonna da restituire nelle righe quando ha già un handle di cursore valido (dopo aver ricevuto correttamente CPMCreateQueryOut, vedere la sezione 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="ea353-4673">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="ea353-4674">Maggiore è il valore previsto per fornire una matrice di strutture CTableColumn, come specificato nella Sezione 2.2.4.31, per il campo aColumns e un handle di cursore valido.</span><span class="sxs-lookup"><span data-stu-id="ea353-4674">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="ea353-4675">Quando questa richiesta viene ricevuta dal livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4675">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4676">Calcolare il numero di strutture CTableColumn nella matrice aColumns e impostare il campo cColumns su questo valore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4676">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="ea353-4677">Calcolare le dimensioni totali in byte dei campi cColumns e aColumns e impostare il campo \_ cbBindingDesc su questo valore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4677">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="ea353-4678">Impostare i campi specificati nel messaggio CPMSetBindingsIn ai valori forniti dal livello applicazione superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4678">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="ea353-4679">Impostare il \_ campo ulChecksum sul valore calcolato come specificato nella Sezione 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="ea353-4679">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="ea353-4680">Inviare il messaggio CPMSetBindignsIn completato al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4680">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="ea353-4681">Attendere la ricezione di un messaggio CPMSetBindingsIn dal server, rimuovendo altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4681">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="ea353-4682">Indicare lo stato \_ dal campo di stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4682">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="ea353-4683">Per scopi informativi, è previsto che i livelli superiori in genere richiedono a un client di inviare un messaggio CPMGetRowsIn, ma questo non viene applicato dal protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ea353-4683">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="ea353-4684">3.2.4.2.4 Invio di una richiesta CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4684">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="ea353-4685">Quando il livello superiore sta per ricevere informazioni sulle righe, fornirà al client del protocollo un cursore e un handle di capitolo validi e fornirà una descrizione di ricerca appropriata.</span><span class="sxs-lookup"><span data-stu-id="ea353-4685">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="ea353-4686">In genere, è previsto che un livello superiore esegui questa operazione quando ha un cursore e/o un handle di capitolo validi e le associazioni sono state impostate con il messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4686">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="ea353-4687">Per accedere al set di righe in un capitolo, il livello superiore è usare l'handle di capitolo ricevuto dal server in un messaggio CPMGetRowsOut precedente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4687">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="ea353-4688">Quando questa richiesta viene ricevuta dal livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4688">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4689">Determinare il valore intero senza segno da specificare per il \_ campo cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="ea353-4689">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="ea353-4690">Per determinare questo valore, il client DEVE prendere il valore massimo dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4690">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="ea353-4691">Mille volte il valore del campo \_ c RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="ea353-4691">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="ea353-4692">Valore di \_ cbRowWidth, arrotondato al multiplo di 512 byte più vicino.</span><span class="sxs-lookup"><span data-stu-id="ea353-4692">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="ea353-4693">Prendere il valore più alto di questi due valori, fino al limite di 16.000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4693">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="ea353-4694">Nei casi in cui una singola riga è maggiore di 16.000, il server non può restituire risultati a questa query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4694">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="ea353-4695">Specificare una base client per i dati di riga di dimensioni variabili nello spazio indirizzi del client nel \_ campo ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="ea353-4695">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="ea353-4696">*Comportamento di Windows: per un client a 32 bit che parla con un server a 32 bit o un client a 64 bit che parla con un server a 64 bit, questo valore è impostato su un indirizzo di memoria del buffer ricevente nel processo dell'applicazione. Ciò consente ai puntatori ricevuti nel campo Rows di CPMGetRowsOut di essere puntatori di memoria corretti in un processo dell'applicazione client. In caso contrario, è impostato su 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="ea353-4696">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="ea353-4697">Calcolare le dimensioni della descrizione della ricerca e impostarla nel \_ campo cbSeek.</span><span class="sxs-lookup"><span data-stu-id="ea353-4697">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="ea353-4698">Impostare il valore di cbReserved (che fungerebbe da offset per l'inizio delle righe) sul valore \_ cbSeek più 0x14.</span><span class="sxs-lookup"><span data-stu-id="ea353-4698">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="ea353-4699">Inviare un messaggio CPMConnectIn come specificato nella versione 2.2.3.15 al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4699">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="ea353-4700">3.2.4.2.5 Invio di una richiesta CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4700">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="ea353-4701">Se il client riceve una risposta CPMGetRowsOut dal server con il campo Status della colonna impostato su StatusDeferred (0x01), significa che il valore della proprietà non è stato incluso nel campo Rows del messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4701">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="ea353-4702">In questo caso il livello superiore richiede in genere al client del protocollo di recuperare il valore tramite il messaggio CPMFetchValueIn e fornisce il valore PropSpec e wid per una proprietà posticipata, che il client del protocollo DEVE usare nel primo messaggio \_ CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4702">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="ea353-4703">Se si tratta del primo messaggio CPMFetchValueIn inviato dal client per richiedere la proprietà specificata, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4703">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4704">Impostare tutti i campi in un messaggio come specificato nella sezione 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="ea353-4704">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="ea353-4705">Impostare \_ cbSoFar su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4705">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="ea353-4706">Impostare Byte correnti ricevuti su 0.</span><span class="sxs-lookup"><span data-stu-id="ea353-4706">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="ea353-4707">Inviare il messaggio CPMFetchValueIn al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4707">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="ea353-4708">3.2.4.2.6 Invio di una richiesta CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="ea353-4708">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="ea353-4709">Quando il livello superiore non usa più la query di ricerca, può rilasciare le risorse nel server richiedendo al client di inviare un messaggio CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4709">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="ea353-4710">Quando questa richiesta viene ricevuta, il client DEVE inviare un messaggio CPMFreeCursorIn come specificato in 2.2.3.28 al server, contenente l'handle specificato dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4710">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="ea353-4711">3.2.4.2.7 Invio di un messaggio CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="ea353-4711">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="ea353-4712">Se il livello superiore non dispone di altre query per il servizio di indicizzazione, per liberare più risorse del server, l'applicazione può richiedere che il client invii un messaggio CPMDisconnect al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4712">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="ea353-4713">Quando questa query viene ricevuta, il client DEVE inviare semplicemente il messaggio come richiesto.</span><span class="sxs-lookup"><span data-stu-id="ea353-4713">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="ea353-4714">Non è disponibile alcuna risposta a questo messaggio dal server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4714">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="ea353-4715">3.2.5 Regole di elaborazione e sequenziazione dei messaggi</span><span class="sxs-lookup"><span data-stu-id="ea353-4715">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="ea353-4716">Quando il client riceve una risposta di messaggio dal server, il client DEVE usare l'ultimo messaggio inviato per determinare se il messaggio ricevuto dal server è quello previsto dal client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4716">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="ea353-4717">Tutti i messaggi con \_ il campo msg diverso da quello in Ultimo messaggio di invio DEVONO essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="ea353-4717">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="ea353-4718">3.2.5.1 Ricezione di una risposta CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4718">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="ea353-4719">Quando il client riceve una risposta di messaggio CPMCreateQueryOut dal server, il client DEVE restituire lo stato e (se lo stato ha esito positivo) i valori di handle del cursore tornano al \_ livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4719">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="ea353-4720">Eventuali altre azioni sono fino al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4720">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="ea353-4721">Poiché il livello superiore è a conoscenza della struttura delle query, nel messaggio CPMCreateOueryOut verrà sempre restituito il numero corretto di handle di cursore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4721">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="ea353-4722">Gli handle di cursore vengono restituiti nell'ordine seguente: il primo handle è per il set di righe nonchaptered, il secondo per il primo set di righe in capitoli (ovvero il raggruppamento dei risultati in base alla prima categoria specificata nel campo CategorizationSet del messaggio CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="ea353-4722">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="ea353-4723">Per scopi informativi, è previsto che i livelli superiori possano eseguire le azioni seguenti, ma non vengono applicate dal client CISP:</span><span class="sxs-lookup"><span data-stu-id="ea353-4723">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="ea353-4724">Usare CPMSetBindingsIn per impostare associazioni per singole colonne ed eseguire eventuali azioni successive sul percorso della query</span><span class="sxs-lookup"><span data-stu-id="ea353-4724">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="ea353-4725">Usare CPMGetQueryStatusIn per controllare lo stato di esecuzione di una query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4725">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="ea353-4726">Usare CPMRatioFinishedIn per richiedere la percentuale di completamento della query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4726">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="ea353-4727">3.2.5.2 Ricezione di una risposta CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4727">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="ea353-4728">Quando il client riceve una risposta di messaggio CPMGetRowsOut dal server, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4728">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4729">Controllare se il \_ campo dello stato nell'intestazione indica esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4729">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="ea353-4730">Se il \_ valore di stato è STATUS BUFFER TOO SMALL \_ (0xC0000023), il client DEVE controllare lo stato Ultimo messaggio \_ \_ inviato.</span><span class="sxs-lookup"><span data-stu-id="ea353-4730">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="ea353-4731">Se non contiene un messaggio CPMGetRowsIn, il messaggio ricevuto DEVE essere ignorato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4731">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="ea353-4732">In caso contrario, il client DEVE inviare al server un nuovo messaggio CPMGetRowsIn con tutti i campi identici a quello archiviato, ad eccezione del fatto che cbReadBuffer DEVE essere aumentato di 512 (ma non maggiore di \_ 0x4000).</span><span class="sxs-lookup"><span data-stu-id="ea353-4732">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="ea353-4733">Se status è STATUS BUFFER TOO SMALL (0xC0000023) e Last Message Sent ha già \_ \_ \_ \_ \_ cbReadBuffer uguale 0x4000 il client DEVE segnalare l'errore fino al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4733">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="ea353-4734">Se il \_ valore di stato è qualsiasi altro valore di errore, il client DEVE indicare l'errore fino al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4734">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="ea353-4735">Se il valore di stato indica l'esito positivo, i risultati DEVONO essere indicati fino al livello superiore che richiede le informazioni e altre azioni sono fino \_ al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4735">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="ea353-4736">Per scopi informativi, è previsto che i livelli superiori eseecutori in genere esecutori delle azioni seguenti, ma non vengono applicati dal client Content Indexing Service Protocol:</span><span class="sxs-lookup"><span data-stu-id="ea353-4736">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="ea353-4737">Se i valori nelle righe rappresentano gli ID documento, gli handle di capitolo o segnalibro del livello superiore in genere li archivieranno per l'uso nelle operazioni successive che coinvolgono ID documento, handle di capitolo o segnalibro validi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4737">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="ea353-4738">Il livello superiore in genere archivia o visualizza o usa in altro modo i dati dei valori di riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-4738">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="ea353-4739">Per i valori contrassegnati come livello superiore posticipato, recupererà il valore usando i messaggi CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4739">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="ea353-4740">Anche la descrizione della ricerca viene restituita al livello superiore e può essere riutilizzata o esaminata dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4740">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="ea353-4741">A scopo informativo, se il livello superiore ha richiesto handle per i capitoli e i segnalibri ricevuti nelle righe, è possibile eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4741">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="ea353-4742">Usare CPMGetQueryStatusExIn per controllare lo stato di esecuzione di una query, nonché informazioni aggiuntive sullo stato, ad esempio il numero di documenti filtrati, i documenti rimanenti da filtrare, il rapporto tra i documenti elaborati dalla query, il numero totale di righe nella query e la posizione del segnalibro nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-4742">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="ea353-4743">Usare CPMGetNotify per richiedere che il server invii una notifica al client delle modifiche al set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-4743">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="ea353-4744">Usare CPMGetApproximatePositionIn per richiedere la posizione approssimativa di un segnalibro in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4744">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="ea353-4745">Usare CPMCompareBmkIn per richiedere un confronto tra due segnalibri in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4745">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="ea353-4746">Usare CPMRestartPositionIn per il server per modificare la posizione del cursore all'inizio del set di righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-4746">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="ea353-4747">3.2.5.3 Ricezione di una risposta CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4747">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="ea353-4748">Quando il client riceve una risposta di messaggio CPMGetRowsOut dal server, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4748">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="ea353-4749">Controllare se il \_ campo dello stato nell'intestazione indica esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4749">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="ea353-4750">In caso di errore, inviare una notifica al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4750">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="ea353-4751">In caso contrario, continuare di seguito.</span><span class="sxs-lookup"><span data-stu-id="ea353-4751">Otherwise, continue below.</span></span>
-   <span data-ttu-id="ea353-4752">Controllare fValueExist e se impostato su 0x00000000 notificare al livello \_ superiore che il valore non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="ea353-4752">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="ea353-4753">In caso contrario, \_ aggiungere i byte cbValue da vValue al valore della proprietà corrente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4753">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="ea353-4754">Se fMoreExists è impostato su 0x00000001 incrementare i byte correnti ricevuti da cbValue e inviare un \_ \_ \_ \_ messaggio CPMFetchValueIn al server, impostando cbSoFar sul valore di Byte correnti \_ ricevuti, cbPropSpec su zero e \_ \_ cbChunk sulla dimensione del buffer desiderata dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4754">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="ea353-4755">Se fMoreExists è impostato su 0x00000000 quindi indicare il valore della proprietà da Valore proprietà \_ corrente al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4755">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="ea353-4756">3.2.5.4 Ricezione di una risposta CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="ea353-4756">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="ea353-4757">Quando il client riceve una risposta di messaggio CPMFreeCursorOut dal server, il client DEVE restituire il valore \_ cCursorsRemaining al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="ea353-4757">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="ea353-4758">Le informazioni seguenti vengono fornite solo a scopo informativo e non vengono applicate dal client CISP.</span><span class="sxs-lookup"><span data-stu-id="ea353-4758">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="ea353-4759">Si prevede che il livello superiore tenga traccia degli handle di cursore e non usi quelli che sono già stati liberati.</span><span class="sxs-lookup"><span data-stu-id="ea353-4759">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="ea353-4760">Quando il numero di cCursorsRemaining è uguale a 0x00000000, il livello superiore può usare la connessione per specificare un'altra query (usando un \_ messaggio CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="ea353-4760">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="ea353-4761">3.2.6 Eventi timer</span><span class="sxs-lookup"><span data-stu-id="ea353-4761">3.2.6 Timer Events</span></span>

<span data-ttu-id="ea353-4762">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="ea353-4762">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="ea353-4763">3.2.7 Altri eventi locali</span><span class="sxs-lookup"><span data-stu-id="ea353-4763">3.2.7 Other Local Events</span></span>

<span data-ttu-id="ea353-4764">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="ea353-4764">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="ea353-4765">4 Esempi di protocollo</span><span class="sxs-lookup"><span data-stu-id="ea353-4765">4 Protocol Examples</span></span>

-   [<span data-ttu-id="ea353-4766">4.1 Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea353-4766">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="ea353-4767">4.2 Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ea353-4767">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="ea353-4768">4.1 Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea353-4768">4.1 Example 1</span></span>

<span data-ttu-id="ea353-4769">Nell'esempio seguente si consideri uno scenario in cui l'utente JOHN nel computer A vuole ottenere le dimensioni dei file che contengono la parola "Microsoft" dal set di documenti archiviati nel server X nel catalogo SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="ea353-4769">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="ea353-4770">Si supponga che nel computer A sia in esecuzione un sistema operativo Windows XP a 32 bit e nel computer X sia in esecuzione un sistema operativo Windows Server 2003 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ea353-4770">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="ea353-4771">L'utente avvia un'applicazione di ricerca e immette la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="ea353-4771">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="ea353-4772">L'applicazione a sua volta passa la query di ricerca al client del protocollo.</span><span class="sxs-lookup"><span data-stu-id="ea353-4772">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="ea353-4773">Il client del protocollo stabilisce una connessione con il server di indicizzazione X. Il client del protocollo usa named pipe \\ pipe \\ CI \_ SKADS per connettersi al server X tramite SMB.</span><span class="sxs-lookup"><span data-stu-id="ea353-4773">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="ea353-4774">Il client del protocollo prepara quindi un messaggio CPMConnectIn con i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4774">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="ea353-4775">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4775">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4776">**\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4776">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="ea353-4777">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4777">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="ea353-4778">**\_ ulChecksum** contiene il checksum, calcolato come specificato nella sezione 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="ea353-4778">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="ea353-4779">**\_ ulReserved2 è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4779">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="ea353-4780">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4780">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4781">**\_ iClientVersion è** impostato su 0x00000008, a indicare che il server deve convalidare il campo checksum.</span><span class="sxs-lookup"><span data-stu-id="ea353-4781">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="ea353-4782">**\_ fClientIsRemote** è impostato su 0x00000001, che indica che il server è un server remoto.</span><span class="sxs-lookup"><span data-stu-id="ea353-4782">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="ea353-4783">**\_ cbBlob1** è impostato sulla dimensione, in byte, dei campi cPropSet, PropertySet1 e PropertySet2 combinati.</span><span class="sxs-lookup"><span data-stu-id="ea353-4783">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="ea353-4784">**\_ cbBlob2 è** impostato su 0x00000004 (ovvero nessun set di proprietà aggiuntivo).</span><span class="sxs-lookup"><span data-stu-id="ea353-4784">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="ea353-4785">**MachineName** è impostato su A.</span><span class="sxs-lookup"><span data-stu-id="ea353-4785">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="ea353-4786">**UserName** è impostato su JOHN.</span><span class="sxs-lookup"><span data-stu-id="ea353-4786">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="ea353-4787">**cPropSets** è impostato su 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="ea353-4787">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="ea353-4788">**Il campo PropertySet1** è di tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="ea353-4788">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="ea353-4789">La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4789">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="ea353-4790">Il campo **GuidPropSet** è impostato su A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="ea353-4790">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="ea353-4791">**Il campo cProperties** è impostato su 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="ea353-4791">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="ea353-4792">**Un campo aProps** è una matrice di strutture CDbProp.</span><span class="sxs-lookup"><span data-stu-id="ea353-4792">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="ea353-4793">Per **l'elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="ea353-4793">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="ea353-4794">**PropId** è impostato su 0x00000002 (DBPROP \_ CI \_ CATALOG \_ NAME).</span><span class="sxs-lookup"><span data-stu-id="ea353-4794">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="ea353-4795">**DBPROPOPTIONS è** impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4795">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="ea353-4796">**DBPROPSTATUS è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4796">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4797">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4797">For the **ColId** element:</span></span>
                -   <span data-ttu-id="ea353-4798">**eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID)</span><span class="sxs-lookup"><span data-stu-id="ea353-4798">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="ea353-4799">**IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-4799">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="ea353-4800">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4800">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4801">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4801">For the **vValue** element:</span></span>
                -   <span data-ttu-id="ea353-4802">**vType** è impostato su 0x001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="ea353-4802">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="ea353-4803">**vValue** è impostato su "SYSTEM", il nome del catalogo desiderato.</span><span class="sxs-lookup"><span data-stu-id="ea353-4803">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="ea353-4804">Per **l'elemento aProps \[ 1: \]**</span><span class="sxs-lookup"><span data-stu-id="ea353-4804">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="ea353-4805">**PropId** è impostato su 0x00000007 (DBPROP \_ CI \_ QUERY \_ TYPE)</span><span class="sxs-lookup"><span data-stu-id="ea353-4805">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="ea353-4806">**DBPROPOPTIONS è** impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4806">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="ea353-4807">**DBPROPSTATUS è** impostato su0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4807">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4808">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4808">For the **ColId** element:</span></span>
                -   <span data-ttu-id="ea353-4809">**eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID).</span><span class="sxs-lookup"><span data-stu-id="ea353-4809">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="ea353-4810">**IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-4810">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="ea353-4811">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4811">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4812">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4812">For the **vValue** element:</span></span>
                -   <span data-ttu-id="ea353-4813">**vType** è impostato su 0x0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="ea353-4813">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="ea353-4814">**vValue** è impostato su 0x00000000 (CiNormal), ovvero si tratta di una query normale.</span><span class="sxs-lookup"><span data-stu-id="ea353-4814">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="ea353-4815">Per **l'elemento aProps \[ 2: \]**</span><span class="sxs-lookup"><span data-stu-id="ea353-4815">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="ea353-4816">**PropId** è impostato su 0x00000004 (DBPROP \_ CI \_ SCOPE \_ FLAGS).</span><span class="sxs-lookup"><span data-stu-id="ea353-4816">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="ea353-4817">**DBPROPOPTIONS è** impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4817">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="ea353-4818">**DBPROPSTATUS è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4818">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4819">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4819">For the **ColId** element:</span></span>
                -   <span data-ttu-id="ea353-4820">**eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID).</span><span class="sxs-lookup"><span data-stu-id="ea353-4820">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="ea353-4821">**IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-4821">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="ea353-4822">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4822">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4823">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4823">For the **vValue** element:</span></span>
                -   <span data-ttu-id="ea353-4824">**vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="ea353-4824">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="ea353-4825">**vValue:** 0x00000001/0x00000001 (un elemento con valore 1), ovvero le sottocartelle di ricerca</span><span class="sxs-lookup"><span data-stu-id="ea353-4825">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="ea353-4826">Per **l'elemento aProps \[ 3: \]**</span><span class="sxs-lookup"><span data-stu-id="ea353-4826">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="ea353-4827">**PropId:** 0x00000003 (DBPROP \_ CI \_ INCLUDE \_ SCOPES)</span><span class="sxs-lookup"><span data-stu-id="ea353-4827">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="ea353-4828">**DBPROPOPTIONS:** 0x0000000</span><span class="sxs-lookup"><span data-stu-id="ea353-4828">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="ea353-4829">**DBPROPSTATUS:** 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-4829">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="ea353-4830">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4830">For the **ColId** element:</span></span>
                -   <span data-ttu-id="ea353-4831">**eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID).</span><span class="sxs-lookup"><span data-stu-id="ea353-4831">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="ea353-4832">**IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-4832">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="ea353-4833">**ulID** è impostato su 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-4833">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="ea353-4834">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4834">For the **vValue** element:</span></span>
                -   <span data-ttu-id="ea353-4835">**vType** è impostato su 0x101F (VT \_ VECTOR \| VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="ea353-4835">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="ea353-4836">**vValue** è impostato su 0x00000001/0x00000002 / " " (un elemento con una stringa con terminazione \\ Null di 2 caratteri), ovvero l'ambito radice.</span><span class="sxs-lookup"><span data-stu-id="ea353-4836">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="ea353-4837">Il **campo PropertySet2** è di tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="ea353-4837">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="ea353-4838">La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4838">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="ea353-4839">**GuidPropSet** è impostato su AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="ea353-4839">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="ea353-4840">**Il campo cProperties** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-4840">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="ea353-4841">Il **campo aProps** è una matrice di strutture CDbProp.</span><span class="sxs-lookup"><span data-stu-id="ea353-4841">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="ea353-4842">Per **l'elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="ea353-4842">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="ea353-4843">**PropId** è impostato su 0x00000002 (DBPROP \_ MACHINE).</span><span class="sxs-lookup"><span data-stu-id="ea353-4843">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="ea353-4844">**DBPROPOPTIONS è** impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4844">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="ea353-4845">**DBPROPSTATUS è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4845">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4846">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4846">For the **ColId** element:</span></span>
                -   <span data-ttu-id="ea353-4847">**eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID),</span><span class="sxs-lookup"><span data-stu-id="ea353-4847">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="ea353-4848">**IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-4848">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="ea353-4849">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4849">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4850">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="ea353-4850">For **vValue** element:</span></span>
                -   <span data-ttu-id="ea353-4851">**vType:** 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="ea353-4851">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="ea353-4852">**vValue**: 0x04 /"X" (4 byte/stringa Unicode con terminazione Null), ovvero "X" -name di un server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4852">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="ea353-4853">**Il campo cExtPropSet** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4853">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="ea353-4854">**La matrice aPropertySets** non esiste.</span><span class="sxs-lookup"><span data-stu-id="ea353-4854">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="ea353-4855">I vari campi di riempimento vengono compilati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ea353-4855">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="ea353-4856">Il messaggio viene inviato al server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4856">The message is sent to the server.</span></span>

4.  <span data-ttu-id="ea353-4857">Il server verifica che **\_ ulChecksum** sia corretto, verifica che l'utente sia autorizzato a effettuare questa richiesta e risponde con un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4857">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="ea353-4858">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4858">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4859">**\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4859">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="ea353-4860">**\_ status** è impostato su 0x0000000 che indica SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="ea353-4860">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="ea353-4861">**\_ ulChecksum** è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="ea353-4861">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="ea353-4862">**\_ ulReserved2 è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4862">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="ea353-4863">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4863">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4864">**\_ il campo serverVersion** è impostato 0x00000007 (Windows XP a 32 bit o Windows Server 2003 a 32 bit).</span><span class="sxs-lookup"><span data-stu-id="ea353-4864">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="ea353-4865">**\_ I** campi riservati vengono compilati con dati arbitrari.</span><span class="sxs-lookup"><span data-stu-id="ea353-4865">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="ea353-4866">Il client prepara un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4866">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="ea353-4867">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4867">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4868">**\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4868">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="ea353-4869">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4869">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="ea353-4870">**\_ ulChecksum** contiene il checksum, calcolato in base alla versione 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="ea353-4870">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="ea353-4871">**\_ ulReserved2 è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4871">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="ea353-4872">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4872">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4873">**Il** campo Dimensioni è impostato sulla dimensione del resto del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-4873">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="ea353-4874">**Il campo CColumnSetPresent** è impostato su 0x01.</span><span class="sxs-lookup"><span data-stu-id="ea353-4874">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="ea353-4875">**Il campo ColumnSet** è di tipo CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="ea353-4875">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="ea353-4876">La struttura CColumnSet che comprende questo campo viene impostata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4876">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="ea353-4877">**\_ Il** campo count è impostato su 0x00000001 che indica che viene restituita una colonna.</span><span class="sxs-lookup"><span data-stu-id="ea353-4877">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="ea353-4878">**La matrice indexes** 0x00000000 che indica la prima voce in \_ un oggettoPropSpec.</span><span class="sxs-lookup"><span data-stu-id="ea353-4878">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="ea353-4879">**Il campo CRestrictionPresent** è impostato su 0x01 che indica che il **campo Restriction** è presente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4879">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="ea353-4880">**Il** campo Restriction è di tipo CRestriction ed è impostato su:</span><span class="sxs-lookup"><span data-stu-id="ea353-4880">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="ea353-4881">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="ea353-4881">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="ea353-4882">**\_ weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4882">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="ea353-4883">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="ea353-4883">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="ea353-4884">**\_ La** proprietà è impostata sul GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC PROPID) /0x13 che rappresenta il corpo \_ del documento.</span><span class="sxs-lookup"><span data-stu-id="ea353-4884">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="ea353-4885">**\_ Cc** è impostato su 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="ea353-4885">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="ea353-4886">**\_ pwcsphrase** è impostato sulla stringa "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="ea353-4886">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="ea353-4887">**\_ lcid** è impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="ea353-4887">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="ea353-4888">**\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="ea353-4888">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="ea353-4889">**CSortPresent è** impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-4889">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="ea353-4890">**CCategorizationSetPresent** è impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-4890">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="ea353-4891">**RowSetProperties viene** impostato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4891">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="ea353-4892">**\_ uBooleanOptions** è impostato su 0x00000001 (sequenziale).</span><span class="sxs-lookup"><span data-stu-id="ea353-4892">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="ea353-4893">**\_ ulMaxOpenRows** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4893">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="ea353-4894">**\_ ulMemoryUsage** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4894">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="ea353-4895">\_**cMaxResults è** impostato su 0x00000100 (restituisce al massimo 256 righe).</span><span class="sxs-lookup"><span data-stu-id="ea353-4895">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="ea353-4896">**\_ cCmdTimeOut** è impostato su 0x00000000 (mai timeout).</span><span class="sxs-lookup"><span data-stu-id="ea353-4896">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="ea353-4897">**PidMapper** è impostato su:</span><span class="sxs-lookup"><span data-stu-id="ea353-4897">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="ea353-4898">**\_ count** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-4898">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="ea353-4899">**\_ aPropSpec** è impostato sul GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0x00000001 (per PRSPEC PROPID) / 0x0000000c che rappresenta la proprietà delle dimensioni \_ del file di Windows.</span><span class="sxs-lookup"><span data-stu-id="ea353-4899">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="ea353-4900">Il server lo elabora e risponde con un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4900">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="ea353-4901">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4901">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4902">**\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4902">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="ea353-4903">**\_ status** è impostato su SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="ea353-4903">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="ea353-4904">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="ea353-4904">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="ea353-4905">**\_ ulReserved2 è** impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="ea353-4905">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="ea353-4906">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4906">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4907">**\_ fTrueSeqeuntial** è impostato su 0x00000000, a indicare che la query può usare un indice.</span><span class="sxs-lookup"><span data-stu-id="ea353-4907">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="ea353-4908">**\_ fWorkIdUnique** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-4908">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="ea353-4909">La **matrice aCursors** contiene un solo elemento, che rappresenta un handle di cursore per questa query.</span><span class="sxs-lookup"><span data-stu-id="ea353-4909">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="ea353-4910">Il valore dipende dallo stato del server.</span><span class="sxs-lookup"><span data-stu-id="ea353-4910">The value depends on the state of the server.</span></span> <span data-ttu-id="ea353-4911">Si supponga che il valore restituito sia 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="ea353-4911">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="ea353-4912">Il client esegui un messaggio di richiesta CPMSetBindingsIn per definire il formato di una riga.</span><span class="sxs-lookup"><span data-stu-id="ea353-4912">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="ea353-4913">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4913">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4914">**\_ msg** è impostato su 0x000000D0, a indicare che si tratta di un messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4914">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="ea353-4915">**\_ status** è impostato su SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="ea353-4915">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="ea353-4916">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="ea353-4916">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="ea353-4917">**\_ ulReserved2 è** impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="ea353-4917">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="ea353-4918">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4918">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4919">**\_ hCursor** è impostato su 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="ea353-4919">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="ea353-4920">**\_ cbRow è** impostato su 0x10 (sufficientemente grande da adattarsi alle colonne).</span><span class="sxs-lookup"><span data-stu-id="ea353-4920">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="ea353-4921">**\_ cbBindingDesc** è impostato sulla dimensione dei campi **\_ cColumns** **\_ e aColumns** combinati.</span><span class="sxs-lookup"><span data-stu-id="ea353-4921">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="ea353-4922">**\_ cColumns** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-4922">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="ea353-4923">**\_ La matrice aColumns** è impostata in modo da contenere una struttura CTableColumn contenente:</span><span class="sxs-lookup"><span data-stu-id="ea353-4923">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="ea353-4924">**\_ PropSpec** è impostato sul GUID b725f130-47ef-101a-a5-f1-02608c9eebatt / 0x00000001 (per PRSPEC PROPID) / 0x0000000c che rappresenta la proprietà delle dimensioni \_ del file di Windows.</span><span class="sxs-lookup"><span data-stu-id="ea353-4924">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="ea353-4925">**\_ vType** è impostato su 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="ea353-4925">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="ea353-4926">**\_ ValueUsed** è impostato su 0x01 (colonna trasferita nella riga).</span><span class="sxs-lookup"><span data-stu-id="ea353-4926">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="ea353-4927">**\_ ValueOffset** è impostato su 0x0002 (all'inizio della riga).</span><span class="sxs-lookup"><span data-stu-id="ea353-4927">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="ea353-4928">**\_ ValueSize è** impostato su 0x08 (dimensioni di un'interfaccia utente VT8). \_</span><span class="sxs-lookup"><span data-stu-id="ea353-4928">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="ea353-4929">**\_ StatusUsed** è impostato su 0x01.</span><span class="sxs-lookup"><span data-stu-id="ea353-4929">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="ea353-4930">**\_ StatusOffset** è impostato su 0x0A.</span><span class="sxs-lookup"><span data-stu-id="ea353-4930">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="ea353-4931">**\_ LengthUsed** è impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="ea353-4931">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="ea353-4932">Il server lo elabora e risponde con un messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4932">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="ea353-4933">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4933">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4934">**\_ msg** è impostato su 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="ea353-4934">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="ea353-4935">**\_ status** è impostato su SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="ea353-4935">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="ea353-4936">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="ea353-4936">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="ea353-4937">**\_ ulReserved2** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="ea353-4937">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="ea353-4938">Il client genera un messaggio di richiesta CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4938">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="ea353-4939">Si supponga che il client sia pronto ad accettare 100 righe a questo punto e le voglia in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="ea353-4939">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="ea353-4940">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4940">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4941">**\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="ea353-4941">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="ea353-4942">**\_ status** è impostato su 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ea353-4942">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="ea353-4943">**\_ ulChecksum** contiene il checksum, calcolato in base alla sezione 0.</span><span class="sxs-lookup"><span data-stu-id="ea353-4943">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="ea353-4944">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4944">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="ea353-4945">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4945">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4946">**\_ hCursor** è impostato su 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="ea353-4946">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="ea353-4947">**\_ cRowsToTransfer** è impostato su 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="ea353-4947">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="ea353-4948">**\_ cRowWidth** è impostato su 0x00000010 (da associazioni).</span><span class="sxs-lookup"><span data-stu-id="ea353-4948">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="ea353-4949">**\_ cbSeek** è impostato su 0x14 le dimensioni dei campi eType, chapt e \_ CRowSeekNext combinati.</span><span class="sxs-lookup"><span data-stu-id="ea353-4949">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="ea353-4950">**\_ cbReserved è** impostato su 0x18 (0x14 più \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="ea353-4950">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="ea353-4951">**\_ cbReadBuffer** è impostato su 0x800 (0x64 0x10 arrotondato al multiplo \* successivo di 0x200).</span><span class="sxs-lookup"><span data-stu-id="ea353-4951">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="ea353-4952">**\_ ulClientBase** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4952">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="ea353-4953">**\_ fBwdfetch** è impostato su 0x00000000 che indica che le righe devono essere recuperate in avanti.</span><span class="sxs-lookup"><span data-stu-id="ea353-4953">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="ea353-4954">**eType** è impostato su 0x0000001 che indica che il client vuole le righe successive.</span><span class="sxs-lookup"><span data-stu-id="ea353-4954">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="ea353-4955">**\_ chapt** è impostato su 0 (non su un risultato in capitolo).</span><span class="sxs-lookup"><span data-stu-id="ea353-4955">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="ea353-4956">**SeekDescription** è impostato su CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="ea353-4956">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="ea353-4957">La struttura CRowSeekNext contiene i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea353-4957">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="ea353-4958">**CiTblChapt** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4958">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="ea353-4959">**\_ hRegion** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4959">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="ea353-4960">**\_ cSkip** è impostato su 0, a indicare che il client non vuole ignorare le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-4960">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="ea353-4961">Il server lo elabora e risponde con un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4961">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="ea353-4962">Si supponga che il server ha trovato 100 documenti contenenti la parola "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="ea353-4962">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="ea353-4963">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4963">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4964">**\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="ea353-4964">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="ea353-4965">**\_ status** è impostato su SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="ea353-4965">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="ea353-4966">**\_ ulChecksum** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4966">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="ea353-4967">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4967">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="ea353-4968">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4968">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4969">**\_ CRowsReturned** è impostato su 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="ea353-4969">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="ea353-4970">**eType** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="ea353-4970">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="ea353-4971">**\_ chapt** è impostato su 0x00000000 (non un risultato in capitolo).</span><span class="sxs-lookup"><span data-stu-id="ea353-4971">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="ea353-4972">**SeekDescription** contiene una struttura CRowSeekNext, popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4972">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="ea353-4973">**CiTblChapt** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4973">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="ea353-4974">**\_ hRegion** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4974">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="ea353-4975">**\_ cSkip** è impostato su 0, a indicare che il client non vuole ignorare le righe.</span><span class="sxs-lookup"><span data-stu-id="ea353-4975">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="ea353-4976">**Le** righe contengono le dimensioni dei 100 documenti che contengono la parola "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="ea353-4976">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="ea353-4977">Poiché si tratta di dati di dimensioni fisse, è semplicemente strutturato come elenco di interi senza segno a 100 byte a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="ea353-4977">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="ea353-4978">Il client invia un messaggio CPMDisconnect per terminare la connessione.</span><span class="sxs-lookup"><span data-stu-id="ea353-4978">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="ea353-4979">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="ea353-4979">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="ea353-4980">**\_ msg** è impostato su 0x000000C9, a indicare che si tratta di un messaggio CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="ea353-4980">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="ea353-4981">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4981">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="ea353-4982">**\_ ulChecksum** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4982">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="ea353-4983">Il server elabora il messaggio e rimuove tutto lo stato del client.</span><span class="sxs-lookup"><span data-stu-id="ea353-4983">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="ea353-4984">4.2 Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ea353-4984">4.2 Example 2</span></span>

<span data-ttu-id="ea353-4985">Nell'esempio precedente la query era piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="ea353-4985">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="ea353-4986">Si consideri ora una query leggermente più complessa.</span><span class="sxs-lookup"><span data-stu-id="ea353-4986">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="ea353-4987">Si supponga che l'utente voglia recuperare le dimensioni dei documenti che contengono entrambe le parole seguenti: "Microsoft" e "Office".</span><span class="sxs-lookup"><span data-stu-id="ea353-4987">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="ea353-4988">Questa impostazione viene specificata modificando il campo Restriction contenuto nel messaggio CPMCreateQueryIn inviato nel passaggio 5 come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ea353-4988">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="ea353-4989">Il **campo Restriction** è di tipo CRestriction ed è impostato su:</span><span class="sxs-lookup"><span data-stu-id="ea353-4989">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="ea353-4990">**\_ ulType** è impostato su 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="ea353-4990">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="ea353-4991">**\_ weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4991">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="ea353-4992">Il resto del campo contiene una struttura CNodeRestriction:</span><span class="sxs-lookup"><span data-stu-id="ea353-4992">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="ea353-4993">**\_ cNode** è impostato su 0x00000002, a indicare che nella matrice paNode sono presenti due nodi.</span><span class="sxs-lookup"><span data-stu-id="ea353-4993">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="ea353-4994">Il **\_ campo paNode** è una matrice di due strutture CRestriction.</span><span class="sxs-lookup"><span data-stu-id="ea353-4994">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="ea353-4995">**\_ paNode \[ \] 0** contiene:</span><span class="sxs-lookup"><span data-stu-id="ea353-4995">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="ea353-4996">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="ea353-4996">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="ea353-4997">**\_ weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-4997">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-4998">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="ea353-4998">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="ea353-4999">**\_ La** proprietà è impostata su GUID b725f130-47ef-101a-a5f1-02608c9eeebac/0x00000001 (per \_ PRSPEC PROPID) /0x13.</span><span class="sxs-lookup"><span data-stu-id="ea353-4999">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="ea353-5000">**\_ Cc** è impostato su 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="ea353-5000">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="ea353-5001">**\_ pwcsphrase** è impostato sulla stringa "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="ea353-5001">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="ea353-5002">**\_ lcid** è impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="ea353-5002">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="ea353-5003">**\_ ulGenerateMethod è** impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="ea353-5003">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="ea353-5004">**\_ paNode \[ \] 1** contiene:</span><span class="sxs-lookup"><span data-stu-id="ea353-5004">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="ea353-5005">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="ea353-5005">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="ea353-5006">**\_ weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ea353-5006">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="ea353-5007">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="ea353-5007">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="ea353-5008">**\_ La** proprietà è impostata su GUID b725f130-47ef-101a-a5f1-02608c9eeebac/0x00000001 (per \_ PRSPEC PROPID) /0x13.</span><span class="sxs-lookup"><span data-stu-id="ea353-5008">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="ea353-5009">**\_ Cc** è impostato su 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="ea353-5009">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="ea353-5010">**\_ pwcsphrase** è impostato sulla stringa "Office".</span><span class="sxs-lookup"><span data-stu-id="ea353-5010">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="ea353-5011">**\_ lcid** è impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="ea353-5011">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="ea353-5012">**\_ ulGenerateMethod è** impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="ea353-5012">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="ea353-5013">5 Sicurezza</span><span class="sxs-lookup"><span data-stu-id="ea353-5013">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="ea353-5014">5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione</span><span class="sxs-lookup"><span data-stu-id="ea353-5014">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="ea353-5015">Implementazioni di indicizzazione che indicizzano il contenuto protetto devono considerare l'uso del contesto utente fornito da SMB MS-SMB per tagliare i risultati della ricerca e restituire solo quelli accessibili \[ \] al chiamante.</span><span class="sxs-lookup"><span data-stu-id="ea353-5015">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="ea353-5016">5.2 Indice dei parametri di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ea353-5016">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="ea353-5017">Parametro di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ea353-5017">Security Parameter</span></span>  | <span data-ttu-id="ea353-5018">Sezione</span><span class="sxs-lookup"><span data-stu-id="ea353-5018">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="ea353-5019">Livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="ea353-5019">Impersonation level</span></span> | <span data-ttu-id="ea353-5020">2.1</span><span class="sxs-lookup"><span data-stu-id="ea353-5020">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="ea353-5021">6 Indice del comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="ea353-5021">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="ea353-5022">Comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="ea353-5022">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="ea353-5023">Sezione</span><span class="sxs-lookup"><span data-stu-id="ea353-5023">Section</span></span>   | <span data-ttu-id="ea353-5024">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ea353-5024">Windows 2000</span></span> | <span data-ttu-id="ea353-5025">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea353-5025">Windows XP</span></span> | <span data-ttu-id="ea353-5026">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea353-5026">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="ea353-5027">Questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea353-5027">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="ea353-5028">1.3.2</span><span class="sxs-lookup"><span data-stu-id="ea353-5028">1.3.2</span></span>     | <span data-ttu-id="ea353-5029">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5029">X</span></span>            | <span data-ttu-id="ea353-5030">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5030">X</span></span>          | <span data-ttu-id="ea353-5031">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5031">X</span></span>                   |
| <span data-ttu-id="ea353-5032">Le applicazioni in genere interagiscono con un wrapper OLE DB interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ea353-5032">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="ea353-5033">1.4</span><span class="sxs-lookup"><span data-stu-id="ea353-5033">1.4</span></span>       | <span data-ttu-id="ea353-5034">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5034">X</span></span>            | <span data-ttu-id="ea353-5035">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5035">X</span></span>          | <span data-ttu-id="ea353-5036">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5036">X</span></span>                   |
| <span data-ttu-id="ea353-5037">Valori NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="ea353-5037">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="ea353-5038">1.8</span><span class="sxs-lookup"><span data-stu-id="ea353-5038">1.8</span></span>       | <span data-ttu-id="ea353-5039">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5039">X</span></span>            | <span data-ttu-id="ea353-5040">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5040">X</span></span>          | <span data-ttu-id="ea353-5041">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5041">X</span></span>                   |
| <span data-ttu-id="ea353-5042">Il client imposta il \_ campo dello stato in ogni intestazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ea353-5042">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="ea353-5043">2.2.2</span><span class="sxs-lookup"><span data-stu-id="ea353-5043">2.2.2</span></span>     | <span data-ttu-id="ea353-5044">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5044">X</span></span>            | <span data-ttu-id="ea353-5045">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5045">X</span></span>          | <span data-ttu-id="ea353-5046">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5046">X</span></span>                   |
| <span data-ttu-id="ea353-5047">Il valore di cPendingScans è in genere zero</span><span class="sxs-lookup"><span data-stu-id="ea353-5047">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="ea353-5048">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="ea353-5048">2.2.3.1</span></span>   | <span data-ttu-id="ea353-5049">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5049">X</span></span>            | <span data-ttu-id="ea353-5050">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5050">X</span></span>          | <span data-ttu-id="ea353-5051">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5051">X</span></span>                   |
| <span data-ttu-id="ea353-5052">Valore iClientVersion</span><span class="sxs-lookup"><span data-stu-id="ea353-5052">iClientVersion value</span></span>                                                                              | <span data-ttu-id="ea353-5053">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="ea353-5053">2.2.3.6</span></span>   | <span data-ttu-id="ea353-5054">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5054">X</span></span>            | <span data-ttu-id="ea353-5055">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5055">X</span></span>          | <span data-ttu-id="ea353-5056">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5056">X</span></span>                   |
| <span data-ttu-id="ea353-5057">\_Valore cbChunk</span><span class="sxs-lookup"><span data-stu-id="ea353-5057">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="ea353-5058">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="ea353-5058">2.2.3.19</span></span>  | <span data-ttu-id="ea353-5059">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5059">X</span></span>            | <span data-ttu-id="ea353-5060">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5060">X</span></span>          | <span data-ttu-id="ea353-5061">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5061">X</span></span>                   |
| <span data-ttu-id="ea353-5062">Indirizzi di memoria a 32 bit e a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ea353-5062">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="ea353-5063">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="ea353-5063">3.2.4.2.4</span></span> | <span data-ttu-id="ea353-5064">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5064">X</span></span>            | <span data-ttu-id="ea353-5065">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5065">X</span></span>          | <span data-ttu-id="ea353-5066">X</span><span class="sxs-lookup"><span data-stu-id="ea353-5066">X</span></span>                   |



 

 

 





