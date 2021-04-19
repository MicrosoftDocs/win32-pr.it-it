---
title: Protocollo di servizi di indicizzazione del contenuto
description: Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5265d9d8c802b278b4349ef4b8248b068dc7edc4
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492293"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="cb188-103">Protocollo di servizi di indicizzazione del contenuto</span><span class="sxs-lookup"><span data-stu-id="cb188-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="cb188-104">Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cb188-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cb188-105">Nelle versioni successive, usare [Windows Search.](../search/-search-3x-wds-overview.md)</span><span class="sxs-lookup"><span data-stu-id="cb188-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="cb188-106">Specifica del protocollo, versione 0.12</span><span class="sxs-lookup"><span data-stu-id="cb188-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="cb188-107">1 Introduzione</span><span class="sxs-lookup"><span data-stu-id="cb188-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="cb188-108">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="cb188-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="cb188-109">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="cb188-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="cb188-110">1.3 Panoramica del protocollo (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="cb188-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="cb188-111">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="cb188-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="cb188-112">1.5 Prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="cb188-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="cb188-113">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="cb188-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="cb188-114">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="cb188-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="cb188-115">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="cb188-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="cb188-116">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="cb188-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="cb188-117">2 Messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="cb188-118">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="cb188-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="cb188-119">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="cb188-120">3 Dettagli del protocollo</span><span class="sxs-lookup"><span data-stu-id="cb188-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="cb188-121">3.1 Dettagli del server</span><span class="sxs-lookup"><span data-stu-id="cb188-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="cb188-122">3.2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="cb188-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="cb188-123">4 Esempi di protocollo</span><span class="sxs-lookup"><span data-stu-id="cb188-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="cb188-124">4.1 Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb188-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="cb188-125">4.2 Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cb188-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="cb188-126">5 Sicurezza</span><span class="sxs-lookup"><span data-stu-id="cb188-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="cb188-127">5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione</span><span class="sxs-lookup"><span data-stu-id="cb188-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="cb188-128">5.2 Indice dei parametri di sicurezza</span><span class="sxs-lookup"><span data-stu-id="cb188-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="cb188-129">6 Indice del comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="cb188-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="cb188-130">Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="cb188-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cb188-131">La documentazione di Workgroup Server Protocol Program (WSPP) è destinata all'uso in combinazione con la documentazione degli standard pubblici, l'arte di programmazione di rete e i concetti relativi ai sistemi distribuiti del gruppo di lavoro Windows e presuppone che il lettore abbia familiarità con il materiale di cui si tratta o abbia accesso immediato.</span><span class="sxs-lookup"><span data-stu-id="cb188-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="cb188-132">Una specifica del protocollo WSPP non richiede l'uso di strumenti di programmazione o ambienti di programmazione Microsoft per consentire a un licenziatato di sviluppare un'implementazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="cb188-133">I licenziatati che hanno accesso agli strumenti e agli ambienti di programmazione Microsoft sono liberi di sfruttarli.</span><span class="sxs-lookup"><span data-stu-id="cb188-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="cb188-134">1 Introduzione</span><span class="sxs-lookup"><span data-stu-id="cb188-134">1 Introduction</span></span>

-   [<span data-ttu-id="cb188-135">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="cb188-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="cb188-136">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="cb188-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="cb188-137">1.3 Panoramica del protocollo (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="cb188-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="cb188-138">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="cb188-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="cb188-139">1.5 Prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="cb188-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="cb188-140">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="cb188-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="cb188-141">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="cb188-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="cb188-142">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="cb188-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="cb188-143">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="cb188-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="cb188-144">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="cb188-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="cb188-145">I termini seguenti sono definiti nella sezione Glossario di \[ \] MS-SYS:</span><span class="sxs-lookup"><span data-stu-id="cb188-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="cb188-146">GUID</span><span class="sxs-lookup"><span data-stu-id="cb188-146">GUID</span></span>
> -   <span data-ttu-id="cb188-147">Little Endian</span><span class="sxs-lookup"><span data-stu-id="cb188-147">Little Endian</span></span>
> -   <span data-ttu-id="cb188-148">Named Pipe</span><span class="sxs-lookup"><span data-stu-id="cb188-148">Named Pipe</span></span>
> -   <span data-ttu-id="cb188-149">Percorso</span><span class="sxs-lookup"><span data-stu-id="cb188-149">Path</span></span>

 

<span data-ttu-id="cb188-150">**Binding:** richiesta di includere una determinata **colonna** in un set **di righe restituito.**</span><span class="sxs-lookup"><span data-stu-id="cb188-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="cb188-151">**L'associazione** specifica una proprietà da includere nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="cb188-152">**Segnalibro:** marcatore che identifica in modo univoco una riga all'interno di un set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="cb188-153">**Catalogo:** unità di livello superiore dell'organizzazione nel servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="cb188-154">Rappresenta un set di documenti indicizzati su cui è possibile eseguire query usando il protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="cb188-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cb188-155">**Categoria:** raggruppamento gerarchico di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="cb188-156">Ad esempio, un risultato della query contenente le colonne autore e titolo può essere categorizzato in base all'autore.</span><span class="sxs-lookup"><span data-stu-id="cb188-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="cb188-157">Ogni gruppo di righe contenente lo stesso valore per author costituisce una categoria.</span><span class="sxs-lookup"><span data-stu-id="cb188-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="cb188-158">**Capitolo:** intervallo di righe **all'interno** di un set di **righe.**</span><span class="sxs-lookup"><span data-stu-id="cb188-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="cb188-159">**Column:** contenitore per un singolo tipo di informazioni in una **riga** .</span><span class="sxs-lookup"><span data-stu-id="cb188-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="cb188-160">Le colonne vengono mappate ai nomi delle proprietà e  specificano le proprietà usate per gli elementi dell'albero dei comandi della query **di** ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="cb188-161">**Albero dei comandi:** combinazione **di restrizioni,** **categorie** e **ordinamenti** specificati per la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="cb188-162">**Cursore:** entità usata come meccanismo per  lavorare con una  riga o un piccolo blocco di righe alla volta in un set di dati restituito in un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="cb188-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="cb188-163">Un **cursore** viene posizionato su una singola **riga all'interno** del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="cb188-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="cb188-164">Dopo aver posizionato il **cursore** su una riga, è possibile eseguire operazioni su tale riga o su un blocco **di righe** a partire da tale posizione. </span><span class="sxs-lookup"><span data-stu-id="cb188-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="cb188-165">**Handle**: token che può essere usato per identificare e accedere a **cursori,** **capitoli** e **segnalibri.**</span><span class="sxs-lookup"><span data-stu-id="cb188-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="cb188-166">**Index:** struttura persistente che contiene il contenuto di testo estratto dai file da un **servizio di indicizzazione.**</span><span class="sxs-lookup"><span data-stu-id="cb188-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="cb188-167">Include l'elenco di parole, che vengono archiviate insieme al nome file contenitore, al percorso della parola e alle **impostazioni locali.**</span><span class="sxs-lookup"><span data-stu-id="cb188-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="cb188-168">**Indicizzazione:** processo di estrazione di testo e proprietà dai file e archiviazione dei valori estratti negli indici **(per** il testo) e nella **cache** delle proprietà (per le proprietà).</span><span class="sxs-lookup"><span data-stu-id="cb188-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="cb188-169">**Servizio di indicizzazione:** servizio che crea cataloghi **indicizzati** per il contenuto e le proprietà dei file system.</span><span class="sxs-lookup"><span data-stu-id="cb188-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="cb188-170">Le applicazioni possono cercare nei cataloghi informazioni dai file nel file system.</span><span class="sxs-lookup"><span data-stu-id="cb188-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="cb188-171">**Impostazioni** locali: identificatore, come specificato \[ nell'appendice A di MS-GPSI, \] che specifica le preferenze correlate alla lingua.</span><span class="sxs-lookup"><span data-stu-id="cb188-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="cb188-172">Queste preferenze indicano la modalità di formattazione di date e ore, l'ordinamento alfabetico degli elementi, il confronto delle stringhe e così via.</span><span class="sxs-lookup"><span data-stu-id="cb188-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="cb188-173">**Query in linguaggio naturale:** query costruita usando il linguaggio umano anziché la sintassi di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="cb188-174">**Parola non** erta: parola ignorata dal servizio  di indicizzazione quando è presente nelle restrizioni specificate per la query di ricerca perché ha poco valore discriminatorio.</span><span class="sxs-lookup"><span data-stu-id="cb188-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="cb188-175">Gli esempi in inglese includono "a", "and" e "the".</span><span class="sxs-lookup"><span data-stu-id="cb188-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="cb188-176">**Cache delle proprietà:** cache delle proprietà dei file estratte da un **servizio di indicizzazione.**</span><span class="sxs-lookup"><span data-stu-id="cb188-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="cb188-177">**Indicizzazione delle proprietà:** processo  di  creazione di un indice di proprietà di tipo valore di un documento, tra cui autore, oggetto, tipo, conteggio delle parole, numero di pagine stampate e qualsiasi altra proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="cb188-178">**Restrizione:** set di condizioni che un file deve soddisfare per essere incluso nei risultati della ricerca restituiti dal servizio **di** indicizzazione in risposta a una query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="cb188-179">Una **restrizione** restringe lo stato attivo di  una query di ricerca, limitando i file che il servizio di indicizzazione includerà nei risultati della ricerca solo a quelli che soddisfano le condizioni.</span><span class="sxs-lookup"><span data-stu-id="cb188-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="cb188-180">**Riga**: raccolta di colonne **contenente** i valori delle proprietà che descrivono  un singolo file del set di file che soddisfano le restrizioni specificate nella query di ricerca inviata al servizio **di indicizzazione.**</span><span class="sxs-lookup"><span data-stu-id="cb188-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="cb188-181">**Set di righe:** set di **righe restituite** nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="cb188-182">**Ordinamento:** set di regole in una query di ricerca che definiscono l'ordinamento delle righe nel risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="cb188-183">Ogni regola è costituita da una proprietà (nome, dimensioni e così via) e da una direzione per l'ordinamento (crescente o decrescente).</span><span class="sxs-lookup"><span data-stu-id="cb188-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="cb188-184">Più regole vengono applicate in sequenza</span><span class="sxs-lookup"><span data-stu-id="cb188-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="cb188-185">**Proprietà di tipo testo:** proprietà che descrive il contenuto di un documento e al nome è associato solo testo non formattato.</span><span class="sxs-lookup"><span data-stu-id="cb188-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="cb188-186">**Proprietà di tipo valore:** proprietà che descrive un singolo attributo di un intero documento.</span><span class="sxs-lookup"><span data-stu-id="cb188-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="cb188-187">Una proprietà di tipo valore ha un ID del tipo di dati e un valore di tale tipo di dati associato al nome.</span><span class="sxs-lookup"><span data-stu-id="cb188-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="cb188-188">**Virtual Root**(Radice virtuale): percorso alternativo di una cartella.</span><span class="sxs-lookup"><span data-stu-id="cb188-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="cb188-189">Una cartella fisica può avere zero o più radici virtuali.</span><span class="sxs-lookup"><span data-stu-id="cb188-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="cb188-190">I percorsi che iniziano con una radice virtuale sono detti percorsi virtuali.</span><span class="sxs-lookup"><span data-stu-id="cb188-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="cb188-191">Ad esempio, /server/vanityroot potrebbe essere una radice virtuale di C: \\ cartella \\ Web \\ IIS1.</span><span class="sxs-lookup"><span data-stu-id="cb188-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="cb188-192">Il file C: cartella Web IIS1default.htm il percorso virtuale \\ \\ \\ \\ /server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="cb188-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="cb188-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** questi termini (in maiuscolo) vengono usati come descritto in \[ RFC2119. \]</span><span class="sxs-lookup"><span data-stu-id="cb188-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="cb188-194">Tutte le istruzioni di comportamento facoltativo usano MAY, SHOULD, o SHOULD NOT.</span><span class="sxs-lookup"><span data-stu-id="cb188-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="cb188-195">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="cb188-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="cb188-196">1.2.1 Riferimenti normativi</span><span class="sxs-lookup"><span data-stu-id="cb188-196">1.2.1 Normative References</span></span>

<span data-ttu-id="cb188-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, ottobre 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="cb188-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="cb188-198">\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", giugno 2006.</span><span class="sxs-lookup"><span data-stu-id="cb188-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="cb188-199">\[MS-GPSI \] Microsoft Corporation, "Criteri di gruppo Installazione software Extension", giugno 2006.</span><span class="sxs-lookup"><span data-stu-id="cb188-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="cb188-200">\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions", maggio 2006.</span><span class="sxs-lookup"><span data-stu-id="cb188-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="cb188-201">\[MS-SYS \] Microsoft Corporation, "System Overview v4", July 2006.</span><span class="sxs-lookup"><span data-stu-id="cb188-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="cb188-202">\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="cb188-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="cb188-203">\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="cb188-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="cb188-204">1.2.2 Riferimenti informativi</span><span class="sxs-lookup"><span data-stu-id="cb188-204">1.2.2 Informative References</span></span>

<span data-ttu-id="cb188-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="cb188-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="cb188-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution valori, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="cb188-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="cb188-207">1.3 Panoramica del protocollo (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="cb188-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="cb188-208">Un servizio **di indicizzazione del contenuto** consente di organizzare in modo efficiente le funzionalità estratte di una raccolta di documenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="cb188-209">Il protocollo CISP (Content Indexing Service Protocol) consente a un client di comunicare con un server che ospita un servizio di indicizzazione per eseguire query e consentire a un amministratore di gestire il server di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="cb188-210">Durante l'elaborazione dei file, un servizio di indicizzazione analizza un set di  documenti e riorganizza il contenuto in modo che le proprietà di tali documenti possano essere restituite in modo efficiente in risposta alle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="cb188-211">Una raccolta di documenti su cui è possibile eseguire query include un **catalogo** .</span><span class="sxs-lookup"><span data-stu-id="cb188-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="cb188-212">Un catalogo può contenere **un indice** (per riferimento rapido al testo) e una **cache** delle proprietà (per il recupero rapido dei valori delle proprietà).</span><span class="sxs-lookup"><span data-stu-id="cb188-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="cb188-213">Concettualmente, un catalogo è costituito da una "tabella" logica di proprietà con il testo o il valore e le impostazioni locali corrispondenti archiviate **nelle colonne** della tabella.</span><span class="sxs-lookup"><span data-stu-id="cb188-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="cb188-214">Ogni "riga" della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni "colonna" della tabella corrisponde a una proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="cb188-215">Le attività specifiche eseguite da CISP sono raggruppate in due aree funzionali:</span><span class="sxs-lookup"><span data-stu-id="cb188-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="cb188-216">Amministrazione remota dei cataloghi del servizio di indicizzazione,</span><span class="sxs-lookup"><span data-stu-id="cb188-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="cb188-217">Esecuzione di query remote dei cataloghi del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="cb188-218">1.3.1 Attività di amministrazione remota</span><span class="sxs-lookup"><span data-stu-id="cb188-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="cb188-219">CISP abilita le attività di gestione del catalogo del servizio di indicizzazione seguenti da un client:</span><span class="sxs-lookup"><span data-stu-id="cb188-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="cb188-220">Eseguire una query sullo stato corrente di un catalogo del servizio di indicizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="cb188-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="cb188-221">Aggiornare lo stato di un catalogo del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="cb188-222">Avviare il processo di indicizzazione per un particolare set di file.</span><span class="sxs-lookup"><span data-stu-id="cb188-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="cb188-223">Avviare l'ottimizzazione di un indice per migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="cb188-224">Tutte le attività di amministrazione remota seguono un semplice modello di richiesta/risposta.</span><span class="sxs-lookup"><span data-stu-id="cb188-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="cb188-225">Nel client non viene mantenuto alcuno stato per qualsiasi chiamata amministrativa e le chiamate amministrative possono essere effettuate in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="cb188-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="cb188-226">1.3.2 Esecuzione di query remote</span><span class="sxs-lookup"><span data-stu-id="cb188-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="cb188-227">CISP consente ai client di eseguire query di ricerca su un server remoto che ospita un servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="cb188-228">L'invio di una query di ricerca è un processo in più passaggi avviato dal client.</span><span class="sxs-lookup"><span data-stu-id="cb188-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="cb188-229">Attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="cb188-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="cb188-230">Il client richiede una connessione a un server che ospita un servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="cb188-231">Il client invia i parametri per la query di ricerca, che includono:</span><span class="sxs-lookup"><span data-stu-id="cb188-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="cb188-232">Restrizioni **per specificare** quali documenti includere e/o escludere dai risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="cb188-233">Ordine in cui devono essere restituiti i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="cb188-234">Colonne da restituire nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="cb188-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="cb188-235">Numero massimo di **righe che** devono essere restituite per la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="cb188-236">Tempo massimo per l'esecuzione della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="cb188-237">Dopo che il server ha confermato la richiesta del client di avviare la query, il client può richiedere informazioni sullo stato della query, ma questo non è un passaggio obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cb188-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="cb188-238">Il client specifica quindi le proprietà che il server deve includere nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="cb188-239">Il client richiede un set di risultati al server e il server risponde inviando al client i valori delle proprietà per i file inclusi nei risultati per la query di ricerca del client.</span><span class="sxs-lookup"><span data-stu-id="cb188-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="cb188-240">Se il valore di una proprietà è troppo grande per essere contenuto in un singolo buffer di risposta, il server non invierà la proprietà, ma imposterà lo stato della proprietà su posticipato.</span><span class="sxs-lookup"><span data-stu-id="cb188-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="cb188-241">Il client richiede quindi il valore della proprietà separatamente usando una serie di richieste per i blocchi successivi del valore e quindi riprende la richiesta di altri valori.</span><span class="sxs-lookup"><span data-stu-id="cb188-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="cb188-242">Dopo che il client ha completato la query di ricerca e non richiede più risultati aggiuntivi, il client contatta il server per rilasciare la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="cb188-243">Dopo che il server ha rilasciato la query, il client può inviare una richiesta di disconnessione dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="cb188-244">La connessione viene quindi chiusa.</span><span class="sxs-lookup"><span data-stu-id="cb188-244">The connection is then closed.</span></span> <span data-ttu-id="cb188-245">In alternativa, il client può eseguire un'altra query e ripetere la sequenza del passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="cb188-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="cb188-246">Comportamento di Windows: questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb188-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="cb188-247">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="cb188-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="cb188-248">Il CISP si basa sul protocollo \[ SMB MS-SMB \] per il trasporto dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="cb188-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="cb188-249">Nessun altro protocollo dipende direttamente dal protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="cb188-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cb188-250">*Comportamento di Windows: le applicazioni interagiscono in genere con un wrapper di interfaccia OLE DB \[ MSDN-OLEDB (ad esempio, un client di protocollo) e non \] direttamente con il protocollo.*</span><span class="sxs-lookup"><span data-stu-id="cb188-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="cb188-251">1.5 Prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="cb188-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="cb188-252">Si presuppone che il client abbia ottenuto il nome del server e un nome di catalogo prima che venga richiamato questo protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb188-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="cb188-253">Il modo in cui un client esegue questa operazione non rientra nell'ambito di questa specifica.</span><span class="sxs-lookup"><span data-stu-id="cb188-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="cb188-254">Si presuppone anche che il client e il server hanno un'associazione di sicurezza utilizzabile con named pipe \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="cb188-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="cb188-255">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="cb188-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="cb188-256">CISP è progettato per l'esecuzione di query e la gestione dei cataloghi in un server remoto da un client.</span><span class="sxs-lookup"><span data-stu-id="cb188-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="cb188-257">CISP è deprecato in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb188-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="cb188-258">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="cb188-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="cb188-259">Questo protocollo non ha meccanismi di controllo delle versioni o negoziazione delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="cb188-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="cb188-260">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="cb188-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="cb188-261">Questo protocollo usa HRESULT estendibili dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="cb188-262">I fornitori possono scegliere i propri valori per questo campo, purché il bit C (0x20000000) sia impostato come specificato nella sezione 4.1.1 di MS-SYS, a indicare che si tratta di un codice \[ \] cliente.</span><span class="sxs-lookup"><span data-stu-id="cb188-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="cb188-263">Questo protocollo usa anche i valori NTSTATUS presi dallo spazio dei numeri NTSTATUS definito in \[ MS-SYS \] .</span><span class="sxs-lookup"><span data-stu-id="cb188-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="cb188-264">I fornitori DEVONO riutilizzare questi valori con il significato indicato.</span><span class="sxs-lookup"><span data-stu-id="cb188-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="cb188-265">La scelta di qualsiasi altro valore corre il rischio di collisione in futuro.</span><span class="sxs-lookup"><span data-stu-id="cb188-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="cb188-266">*Comportamento di Windows: Windows usa solo i valori specificati nella sezione 4.1.3 di \[ \] MS-SYS.*</span><span class="sxs-lookup"><span data-stu-id="cb188-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="cb188-267">1.8.1 ID proprietà</span><span class="sxs-lookup"><span data-stu-id="cb188-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="cb188-268">Le proprietà sono rappresentate da ID noti come ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="cb188-269">Ogni proprietà deve avere un identificatore univoco globale.</span><span class="sxs-lookup"><span data-stu-id="cb188-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="cb188-270">Questo identificatore è costituito da un **GUID** che rappresenta una raccolta di proprietà denominata set di proprietà più una stringa o un intero a 32 bit per identificare la proprietà all'interno del set.</span><span class="sxs-lookup"><span data-stu-id="cb188-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="cb188-271">Se viene usato il formato intero di ID, i valori 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE sono considerati non validi.</span><span class="sxs-lookup"><span data-stu-id="cb188-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="cb188-272">I fornitori possono garantire che le relative proprietà siano definite in modo univoco inserendole in un set di proprietà definito dal proprio GUID.</span><span class="sxs-lookup"><span data-stu-id="cb188-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="cb188-273">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="cb188-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="cb188-274">Questo protocollo non ha assegnazioni di standard, ma solo assegnazioni private effettuate da Microsoft tramite procedure di allocazione specificate in altri protocolli.</span><span class="sxs-lookup"><span data-stu-id="cb188-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="cb188-275">Microsoft ha allocato questo protocollo named pipe come specificato in \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="cb188-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="cb188-276">L'assegnazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-276">The assignment is:</span></span>



| <span data-ttu-id="cb188-277">Parametro</span><span class="sxs-lookup"><span data-stu-id="cb188-277">Parameter</span></span> | <span data-ttu-id="cb188-278">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-278">Value</span></span>             | <span data-ttu-id="cb188-279">Riferimento</span><span class="sxs-lookup"><span data-stu-id="cb188-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="cb188-280">Nome pipe</span><span class="sxs-lookup"><span data-stu-id="cb188-280">Pipe name</span></span> | <span data-ttu-id="cb188-281">\\pipe \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="cb188-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="cb188-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="cb188-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="cb188-283">2 Messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-283">2 Messages</span></span>

-   [<span data-ttu-id="cb188-284">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="cb188-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="cb188-285">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="cb188-286">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="cb188-286">2.1 Transport</span></span>

<span data-ttu-id="cb188-287">Tutti i messaggi DEVONO essere trasportati usando named pipe, come specificato in \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="cb188-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="cb188-288">Viene usato il nome della pipe seguente:</span><span class="sxs-lookup"><span data-stu-id="cb188-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="cb188-289">\\pipe \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="cb188-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="cb188-290">Questo protocollo usa il protocollo named pipe SMB sottostante per recuperare l'identità del chiamante che ha effettuato la connessione come specificato nella sezione 2.2.8 di MS-SMB. Il client DEVE impostare SECURITY IDENTIFICATION come \[ ImpersonationLevel nella richiesta per aprire il \] \_ named pipe.</span><span class="sxs-lookup"><span data-stu-id="cb188-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="cb188-291">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-291">2.2 Message Syntax</span></span>

<span data-ttu-id="cb188-292">Diverse strutture e messaggi nelle sezioni seguenti fanno riferimento agli handle di capitolo o segnalibro.</span><span class="sxs-lookup"><span data-stu-id="cb188-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="cb188-293">Un handle è una struttura opaca lunga a 32 bit che identifica in modo univoco un capitolo o un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="cb188-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="cb188-294">In genere, le applicazioni client ricevono valori di handle tramite chiamate al metodo . tuttavia esistono diversi valori noti che non devono essere ottenuti da un server, il cui significato è specificato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="cb188-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="cb188-295">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-295">Value</span></span>                         | <span data-ttu-id="cb188-296">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-297">Db \_ NULL \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="cb188-298">Handle di capitolo per il set di righe non scambiato, contenente tutti i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="cb188-299">DBBMK \_ FIRST 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="cb188-300">Handle di segnalibro per un segnalibro che identifica la prima riga nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="cb188-301">DBBMK \_ LAST 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="cb188-302">Handle di segnalibro per un segnalibro che identifica l'ultima riga nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="cb188-303">2.2.1 Strutture</span><span class="sxs-lookup"><span data-stu-id="cb188-303">2.2.1 Structures</span></span>

<span data-ttu-id="cb188-304">In questa sezione vengono fornite informazioni dettagliate sulle strutture di dati definite e usate da CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="cb188-305">Tutti gli interi con segno a 2, 4 e 8 byte e senza segno nelle strutture seguenti DEVONO essere trasferiti in ordine di byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="cb188-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="cb188-306">La tabella seguente riepiloga le strutture di dati definite in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="cb188-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="cb188-307">Struttura</span><span class="sxs-lookup"><span data-stu-id="cb188-307">Structure</span></span>                    | <span data-ttu-id="cb188-308">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb188-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="cb188-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="cb188-310">Contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata in una struttura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="cb188-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="cb188-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="cb188-312">Contiene una matrice multidimensionale.</span><span class="sxs-lookup"><span data-stu-id="cb188-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="cb188-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="cb188-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="cb188-314">Rappresenta i limiti per una dimensione di una matrice specificata in una struttura SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="cb188-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="cb188-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="cb188-315">CFullPropSpec</span></span>                | <span data-ttu-id="cb188-316">Contiene una specifica di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="cb188-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-317">CContentRestriction</span></span>          | <span data-ttu-id="cb188-318">Contiene una stringa di cui trovare la corrispondenza per un valore di proprietà nella cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="cb188-319">CKey</span><span class="sxs-lookup"><span data-stu-id="cb188-319">CKey</span></span>                         | <span data-ttu-id="cb188-320">Contiene un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="cb188-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="cb188-322">Contiene un valore della proprietà da associare a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="cb188-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="cb188-324">Contiene una corrispondenza di query in linguaggio naturale per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="cb188-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-325">CNodeRestriction</span></span>             | <span data-ttu-id="cb188-326">Contiene una matrice di nodi dell'albero dei comandi che specifica le restrizioni per una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="cb188-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-327">COccRestriction</span></span>              | <span data-ttu-id="cb188-328">Contiene la posizione di una parola in una frase.</span><span class="sxs-lookup"><span data-stu-id="cb188-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="cb188-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-329">CPropertyRestriction</span></span>         | <span data-ttu-id="cb188-330">Contiene un valore della proprietà da associare a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="cb188-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-331">CRangeRestriction</span></span>            | <span data-ttu-id="cb188-332">Contiene una restrizione su un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="cb188-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="cb188-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-333">CScopeRestriction</span></span>            | <span data-ttu-id="cb188-334">Contiene una restrizione sui file in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="cb188-335">CSort</span><span class="sxs-lookup"><span data-stu-id="cb188-335">CSort</span></span>                        | <span data-ttu-id="cb188-336">Identifica una colonna da ordinare.</span><span class="sxs-lookup"><span data-stu-id="cb188-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="cb188-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-337">CSynRestriction</span></span>              | <span data-ttu-id="cb188-338">Contiene una parola o i relativi sinonimi per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="cb188-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-339">CVectorRestriction</span></span>           | <span data-ttu-id="cb188-340">Contiene un'operazione OR ponderata su un nodo della struttura ad albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="cb188-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="cb188-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-341">CWordRestriction</span></span>             | <span data-ttu-id="cb188-342">Contiene una parola per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="cb188-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-343">CRestriction</span></span>                 | <span data-ttu-id="cb188-344">Contiene un nodo di un albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="cb188-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="cb188-345">CColumnSet</span></span>                   | <span data-ttu-id="cb188-346">Indica il numero di colonne da restituire.</span><span class="sxs-lookup"><span data-stu-id="cb188-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="cb188-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="cb188-347">CCategorizationSet</span></span>           | <span data-ttu-id="cb188-348">Contiene informazioni sul raggruppamento di un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="cb188-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="cb188-349">CCategorizationSpec</span></span>          | <span data-ttu-id="cb188-350">Contiene una definizione di categorie in cui verranno categorizzati i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="cb188-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="cb188-351">CDbColId</span></span>                     | <span data-ttu-id="cb188-352">Contiene una colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="cb188-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="cb188-353">CDbProp</span></span>                      | <span data-ttu-id="cb188-354">Contiene una proprietà .</span><span class="sxs-lookup"><span data-stu-id="cb188-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="cb188-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="cb188-355">CDbPropSet</span></span>                   | <span data-ttu-id="cb188-356">Contiene un set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="cb188-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="cb188-357">CPidMapper</span></span>                   | <span data-ttu-id="cb188-358">Contiene una matrice di ID proprietà che specificano le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="cb188-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="cb188-359">CRowSeekAt</span></span>                   | <span data-ttu-id="cb188-360">Contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="cb188-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="cb188-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="cb188-362">Identifica il punto in cui iniziare il recupero per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="cb188-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="cb188-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="cb188-364">Identifica i segnalibri da cui recuperare le righe per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="cb188-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="cb188-365">CRowSeekNext</span></span>                 | <span data-ttu-id="cb188-366">Contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="cb188-367">Proprietà CRowset</span><span class="sxs-lookup"><span data-stu-id="cb188-367">CRowsetProperties</span></span>            | <span data-ttu-id="cb188-368">Contiene le informazioni di configurazione per una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="cb188-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="cb188-369">CSortSet</span></span>                     | <span data-ttu-id="cb188-370">Contiene l'ordinamento per una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="cb188-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="cb188-371">CTableColumn</span></span>                 | <span data-ttu-id="cb188-372">Contiene una colonna per il messaggio CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="cb188-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="cb188-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="cb188-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="cb188-374">Contiene un valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="cb188-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="cb188-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="cb188-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="cb188-376">La struttura CBaseStorageVariant contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata nella struttura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="cb188-377">0</span><span class="sxs-lookup"><span data-stu-id="cb188-377">0</span></span>

<span data-ttu-id="cb188-378">1</span><span class="sxs-lookup"><span data-stu-id="cb188-378">1</span></span>

<span data-ttu-id="cb188-379">2</span><span class="sxs-lookup"><span data-stu-id="cb188-379">2</span></span>

<span data-ttu-id="cb188-380">3</span><span class="sxs-lookup"><span data-stu-id="cb188-380">3</span></span>

<span data-ttu-id="cb188-381">4</span><span class="sxs-lookup"><span data-stu-id="cb188-381">4</span></span>

<span data-ttu-id="cb188-382">5</span><span class="sxs-lookup"><span data-stu-id="cb188-382">5</span></span>

<span data-ttu-id="cb188-383">6</span><span class="sxs-lookup"><span data-stu-id="cb188-383">6</span></span>

<span data-ttu-id="cb188-384">7</span><span class="sxs-lookup"><span data-stu-id="cb188-384">7</span></span>

<span data-ttu-id="cb188-385">8</span><span class="sxs-lookup"><span data-stu-id="cb188-385">8</span></span>

<span data-ttu-id="cb188-386">9</span><span class="sxs-lookup"><span data-stu-id="cb188-386">9</span></span>

<span data-ttu-id="cb188-387">1</span><span class="sxs-lookup"><span data-stu-id="cb188-387">1</span></span><br/> <span data-ttu-id="cb188-388">0</span><span class="sxs-lookup"><span data-stu-id="cb188-388">0</span></span><br/>

<span data-ttu-id="cb188-389">1</span><span class="sxs-lookup"><span data-stu-id="cb188-389">1</span></span>

<span data-ttu-id="cb188-390">2</span><span class="sxs-lookup"><span data-stu-id="cb188-390">2</span></span>

<span data-ttu-id="cb188-391">3</span><span class="sxs-lookup"><span data-stu-id="cb188-391">3</span></span>

<span data-ttu-id="cb188-392">4</span><span class="sxs-lookup"><span data-stu-id="cb188-392">4</span></span>

<span data-ttu-id="cb188-393">5</span><span class="sxs-lookup"><span data-stu-id="cb188-393">5</span></span>

<span data-ttu-id="cb188-394">6</span><span class="sxs-lookup"><span data-stu-id="cb188-394">6</span></span>

<span data-ttu-id="cb188-395">7</span><span class="sxs-lookup"><span data-stu-id="cb188-395">7</span></span>

<span data-ttu-id="cb188-396">8</span><span class="sxs-lookup"><span data-stu-id="cb188-396">8</span></span>

<span data-ttu-id="cb188-397">9</span><span class="sxs-lookup"><span data-stu-id="cb188-397">9</span></span>

<span data-ttu-id="cb188-398">2</span><span class="sxs-lookup"><span data-stu-id="cb188-398">2</span></span><br/> <span data-ttu-id="cb188-399">0</span><span class="sxs-lookup"><span data-stu-id="cb188-399">0</span></span><br/>

<span data-ttu-id="cb188-400">1</span><span class="sxs-lookup"><span data-stu-id="cb188-400">1</span></span>

<span data-ttu-id="cb188-401">2</span><span class="sxs-lookup"><span data-stu-id="cb188-401">2</span></span>

<span data-ttu-id="cb188-402">3</span><span class="sxs-lookup"><span data-stu-id="cb188-402">3</span></span>

<span data-ttu-id="cb188-403">4</span><span class="sxs-lookup"><span data-stu-id="cb188-403">4</span></span>

<span data-ttu-id="cb188-404">5</span><span class="sxs-lookup"><span data-stu-id="cb188-404">5</span></span>

<span data-ttu-id="cb188-405">6</span><span class="sxs-lookup"><span data-stu-id="cb188-405">6</span></span>

<span data-ttu-id="cb188-406">7</span><span class="sxs-lookup"><span data-stu-id="cb188-406">7</span></span>

<span data-ttu-id="cb188-407">8</span><span class="sxs-lookup"><span data-stu-id="cb188-407">8</span></span>

<span data-ttu-id="cb188-408">9</span><span class="sxs-lookup"><span data-stu-id="cb188-408">9</span></span>

<span data-ttu-id="cb188-409">3</span><span class="sxs-lookup"><span data-stu-id="cb188-409">3</span></span><br/> <span data-ttu-id="cb188-410">0</span><span class="sxs-lookup"><span data-stu-id="cb188-410">0</span></span><br/>

<span data-ttu-id="cb188-411">1</span><span class="sxs-lookup"><span data-stu-id="cb188-411">1</span></span>

<span data-ttu-id="cb188-412">vType</span><span class="sxs-lookup"><span data-stu-id="cb188-412">vType</span></span>

<span data-ttu-id="cb188-413">vData1</span><span class="sxs-lookup"><span data-stu-id="cb188-413">vData1</span></span>

<span data-ttu-id="cb188-414">vData2</span><span class="sxs-lookup"><span data-stu-id="cb188-414">vData2</span></span>

<span data-ttu-id="cb188-415">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-415">vValue (variable)</span></span>



 

<span data-ttu-id="cb188-416">**vType:** indicatore di tipo che indica il tipo di vValue.</span><span class="sxs-lookup"><span data-stu-id="cb188-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="cb188-417">DEVE essere uno dei valori VARENUM specificati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cb188-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="cb188-418">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-418">Value</span></span>                 | <span data-ttu-id="cb188-419">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-420">VT \_ EMPTY (0x0000)</span><span class="sxs-lookup"><span data-stu-id="cb188-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="cb188-421">vValue non è presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="cb188-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="cb188-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="cb188-423">vValue non è presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="cb188-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="cb188-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="cb188-425">Intero con segno a 1 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cb188-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="cb188-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="cb188-427">Intero senza segno a 1 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cb188-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="cb188-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="cb188-429">Intero con segno a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cb188-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="cb188-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="cb188-431">Intero senza segno a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cb188-432">VT \_ BOOL (0x000B)</span><span class="sxs-lookup"><span data-stu-id="cb188-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="cb188-433">Valore booleano. Intero a 2 byte contenente 0x0000 (FALSE) o 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="cb188-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="cb188-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="cb188-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="cb188-435">Intero con segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cb188-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="cb188-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="cb188-437">Intero senza segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cb188-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="cb188-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="cb188-439">Numero a virgola mobile IEEE a 32 bit, come definito in \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="cb188-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="cb188-440">VT \_ INT (0x0016)</span><span class="sxs-lookup"><span data-stu-id="cb188-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="cb188-441">Intero con segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cb188-442">UINT \_ VT (0x0017)</span><span class="sxs-lookup"><span data-stu-id="cb188-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="cb188-443">Intero senza segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cb188-444">ERRORE \_ VT (0x000A)</span><span class="sxs-lookup"><span data-stu-id="cb188-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="cb188-445">Intero senza segno a 4 byte contenente un HRESULT, come specificato in \[ MS-SYS \] .</span><span class="sxs-lookup"><span data-stu-id="cb188-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="cb188-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="cb188-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="cb188-447">Intero con segno a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="cb188-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="cb188-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="cb188-449">Intero senza segno a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="cb188-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="cb188-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="cb188-451">Numero a virgola mobile IEEE a 64 bit come definito in \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="cb188-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="cb188-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="cb188-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="cb188-453">Intero complementare a 8 byte a due (ridimensionato di 10.000).</span><span class="sxs-lookup"><span data-stu-id="cb188-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="cb188-454">VT \_ DATE (0x0007)</span><span class="sxs-lookup"><span data-stu-id="cb188-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="cb188-455">Numero a virgola mobile a 64 bit che rappresenta il numero di giorni a partire dalle 00.00.00 del 31 dicembre 1899 (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="cb188-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="cb188-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="cb188-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="cb188-457">Intero a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dalle 00.00.00 del 1° gennaio 1601 (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="cb188-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="cb188-458">VT \_ DECIMAL (0x000E)</span><span class="sxs-lookup"><span data-stu-id="cb188-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="cb188-459">Struttura DECIMAL come specificato nella sezione 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="cb188-460">\_CLSID VT (0x0048)</span><span class="sxs-lookup"><span data-stu-id="cb188-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="cb188-461">Valore binario a 16 byte contenente un GUID.</span><span class="sxs-lookup"><span data-stu-id="cb188-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="cb188-462">BLOB VT \_ (0x0041)</span><span class="sxs-lookup"><span data-stu-id="cb188-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="cb188-463">Numero intero senza segno a 4 byte di byte nel BLOB, seguito da tale numero di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="cb188-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="cb188-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="cb188-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="cb188-465">Numero intero senza segno a 4 byte di byte nella stringa, seguito da una stringa, come specificato di seguito in vValue.</span><span class="sxs-lookup"><span data-stu-id="cb188-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="cb188-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="cb188-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="cb188-467">Stringa ANSI con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="cb188-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="cb188-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="cb188-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="cb188-469">Stringa UNICODE Unicode con \[ \] terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="cb188-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="cb188-470">VT \_ VARIANT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="cb188-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="cb188-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cb188-471">CBaseStorageVariant.</span></span> <span data-ttu-id="cb188-472">DEVE essere combinato con un modificatore di tipo VT \_ ARRAY o VT \_ VECTOR.</span><span class="sxs-lookup"><span data-stu-id="cb188-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="cb188-473">Nella tabella seguente vengono specificati i modificatori di tipo per vType.</span><span class="sxs-lookup"><span data-stu-id="cb188-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="cb188-474">I modificatori di tipo possono essere ORed binari con vType, per modificare il significato di vValue per indicare che si tratta di uno dei due tipi di matrice possibili.</span><span class="sxs-lookup"><span data-stu-id="cb188-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="cb188-475">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-475">Value</span></span>               | <span data-ttu-id="cb188-476">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-477">VETTORE VT \_ (0x1000)</span><span class="sxs-lookup"><span data-stu-id="cb188-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="cb188-478">Se l'indicatore di tipo viene combinato con VT VECTOR usando un operatore OR, vValue è una matrice conteggiata di \_ valori del tipo indicato.</span><span class="sxs-lookup"><span data-stu-id="cb188-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="cb188-479">Per informazioni dettagliate, vedere la sezione 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="cb188-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="cb188-480">Questo modificatore di tipo NON DEVE essere combinato con i tipi seguenti: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, BLOB VT, \_ VT \_ BLOB \_ OBJECT.</span><span class="sxs-lookup"><span data-stu-id="cb188-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="cb188-481">VT \_ ARRAY (0x2000)</span><span class="sxs-lookup"><span data-stu-id="cb188-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="cb188-482">Se l'indicatore di tipo viene combinato con VT ARRAY da un operatore OR, il valore è safeARRAY (come specificato nella sezione \_ 2.2.1.1.1.3) contenente i valori del tipo indicato.</span><span class="sxs-lookup"><span data-stu-id="cb188-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="cb188-483">Questo modificatore di tipo NON DEVE essere combinato con i tipi seguenti: VT \_ I8, \_ VT UI8, VT \_ FILETIME, \_ CLSID VT, BLOB \_ VT, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="cb188-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="cb188-484">**vData1:** quando vType è VT DECIMAL, il valore di questo campo viene specificato come campo Scale nella sezione \_ 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="cb188-485">Per tutti gli altri vTypes, il valore DEVE essere impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="cb188-486">**vData2:** quando vType è VT DECIMAL, il valore di questo campo viene specificato come campo Segno nella sezione \_ 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="cb188-487">Per tutti gli altri vTypes, il valore DEVE essere impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="cb188-488">**vValue:** valore per l'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="cb188-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="cb188-489">La sintassi DEVE essere come indicato nel campo vType.</span><span class="sxs-lookup"><span data-stu-id="cb188-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="cb188-490">La tabella seguente riepiloga le dimensioni per il campo vValue, a seconda del campo vType per i tipi di dati a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="cb188-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="cb188-491">Le dimensioni sono in byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-491">The size is in bytes.</span></span>



| <span data-ttu-id="cb188-492">vType</span><span class="sxs-lookup"><span data-stu-id="cb188-492">vType</span></span>                                                   | <span data-ttu-id="cb188-493">Dimensione</span><span class="sxs-lookup"><span data-stu-id="cb188-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="cb188-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="cb188-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="cb188-495">1</span><span class="sxs-lookup"><span data-stu-id="cb188-495">1</span></span>    |
| <span data-ttu-id="cb188-496">VT \_ I2, VT \_ UI2, VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="cb188-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="cb188-497">2</span><span class="sxs-lookup"><span data-stu-id="cb188-497">2</span></span>    |
| <span data-ttu-id="cb188-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, ERRORE VT \_</span><span class="sxs-lookup"><span data-stu-id="cb188-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="cb188-499">4</span><span class="sxs-lookup"><span data-stu-id="cb188-499">4</span></span>    |
| <span data-ttu-id="cb188-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="cb188-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="cb188-501">8</span><span class="sxs-lookup"><span data-stu-id="cb188-501">8</span></span>    |
| <span data-ttu-id="cb188-502">VT \_ DECIMAL, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="cb188-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="cb188-503">16</span><span class="sxs-lookup"><span data-stu-id="cb188-503">16</span></span>   |



 

<span data-ttu-id="cb188-504">Se vType è impostato su VT \_ BLOB, VT BSTR o \_ VT \_ LPSTR, la struttura di vValue viene specificata nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="cb188-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="cb188-505">0</span><span class="sxs-lookup"><span data-stu-id="cb188-505">0</span></span>

<span data-ttu-id="cb188-506">1</span><span class="sxs-lookup"><span data-stu-id="cb188-506">1</span></span>

<span data-ttu-id="cb188-507">2</span><span class="sxs-lookup"><span data-stu-id="cb188-507">2</span></span>

<span data-ttu-id="cb188-508">3</span><span class="sxs-lookup"><span data-stu-id="cb188-508">3</span></span>

<span data-ttu-id="cb188-509">4</span><span class="sxs-lookup"><span data-stu-id="cb188-509">4</span></span>

<span data-ttu-id="cb188-510">5</span><span class="sxs-lookup"><span data-stu-id="cb188-510">5</span></span>

<span data-ttu-id="cb188-511">6</span><span class="sxs-lookup"><span data-stu-id="cb188-511">6</span></span>

<span data-ttu-id="cb188-512">7</span><span class="sxs-lookup"><span data-stu-id="cb188-512">7</span></span>

<span data-ttu-id="cb188-513">8</span><span class="sxs-lookup"><span data-stu-id="cb188-513">8</span></span>

<span data-ttu-id="cb188-514">9</span><span class="sxs-lookup"><span data-stu-id="cb188-514">9</span></span>

<span data-ttu-id="cb188-515">1</span><span class="sxs-lookup"><span data-stu-id="cb188-515">1</span></span><br/> <span data-ttu-id="cb188-516">0</span><span class="sxs-lookup"><span data-stu-id="cb188-516">0</span></span><br/>

<span data-ttu-id="cb188-517">1</span><span class="sxs-lookup"><span data-stu-id="cb188-517">1</span></span>

<span data-ttu-id="cb188-518">2</span><span class="sxs-lookup"><span data-stu-id="cb188-518">2</span></span>

<span data-ttu-id="cb188-519">3</span><span class="sxs-lookup"><span data-stu-id="cb188-519">3</span></span>

<span data-ttu-id="cb188-520">4</span><span class="sxs-lookup"><span data-stu-id="cb188-520">4</span></span>

<span data-ttu-id="cb188-521">5</span><span class="sxs-lookup"><span data-stu-id="cb188-521">5</span></span>

<span data-ttu-id="cb188-522">6</span><span class="sxs-lookup"><span data-stu-id="cb188-522">6</span></span>

<span data-ttu-id="cb188-523">7</span><span class="sxs-lookup"><span data-stu-id="cb188-523">7</span></span>

<span data-ttu-id="cb188-524">8</span><span class="sxs-lookup"><span data-stu-id="cb188-524">8</span></span>

<span data-ttu-id="cb188-525">9</span><span class="sxs-lookup"><span data-stu-id="cb188-525">9</span></span>

<span data-ttu-id="cb188-526">2</span><span class="sxs-lookup"><span data-stu-id="cb188-526">2</span></span><br/> <span data-ttu-id="cb188-527">0</span><span class="sxs-lookup"><span data-stu-id="cb188-527">0</span></span><br/>

<span data-ttu-id="cb188-528">1</span><span class="sxs-lookup"><span data-stu-id="cb188-528">1</span></span>

<span data-ttu-id="cb188-529">2</span><span class="sxs-lookup"><span data-stu-id="cb188-529">2</span></span>

<span data-ttu-id="cb188-530">3</span><span class="sxs-lookup"><span data-stu-id="cb188-530">3</span></span>

<span data-ttu-id="cb188-531">4</span><span class="sxs-lookup"><span data-stu-id="cb188-531">4</span></span>

<span data-ttu-id="cb188-532">5</span><span class="sxs-lookup"><span data-stu-id="cb188-532">5</span></span>

<span data-ttu-id="cb188-533">6</span><span class="sxs-lookup"><span data-stu-id="cb188-533">6</span></span>

<span data-ttu-id="cb188-534">7</span><span class="sxs-lookup"><span data-stu-id="cb188-534">7</span></span>

<span data-ttu-id="cb188-535">8</span><span class="sxs-lookup"><span data-stu-id="cb188-535">8</span></span>

<span data-ttu-id="cb188-536">9</span><span class="sxs-lookup"><span data-stu-id="cb188-536">9</span></span>

<span data-ttu-id="cb188-537">3</span><span class="sxs-lookup"><span data-stu-id="cb188-537">3</span></span><br/> <span data-ttu-id="cb188-538">0</span><span class="sxs-lookup"><span data-stu-id="cb188-538">0</span></span><br/>

<span data-ttu-id="cb188-539">1</span><span class="sxs-lookup"><span data-stu-id="cb188-539">1</span></span>

<span data-ttu-id="cb188-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="cb188-540">cbSize</span></span>

<span data-ttu-id="cb188-541">blobData (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="cb188-542">**cbSize:** intero senza segno a 32 bit, che indica le dimensioni del campo blobData in byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="cb188-543">Se vType è impostato su VT BSTR o \_ VT LPSTR, cbSize DEVE essere impostato su 0x00000000 quando la stringa rappresentata \_ è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="cb188-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="cb188-544">**blobData:** DEVE essere di lunghezza cbSize in byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="cb188-545">Per vType impostato su BLOB VT, questo campo è dati BLOB \_ binari opachi.</span><span class="sxs-lookup"><span data-stu-id="cb188-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="cb188-546">Per vType impostato su VT BSTR, questo campo è un set di caratteri in un set di caratteri \_ OEM selezionato.</span><span class="sxs-lookup"><span data-stu-id="cb188-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="cb188-547">Il client e il server DEVONO essere configurati per avere set di caratteri interoperabili (fuori banda del protocollo).</span><span class="sxs-lookup"><span data-stu-id="cb188-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="cb188-548">Non è necessario che sia con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="cb188-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="cb188-549">Per vType impostato su VT LPSTR, questo campo è una stringa di caratteri con terminazione Null in un set di caratteri \_ OEM selezionato.</span><span class="sxs-lookup"><span data-stu-id="cb188-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="cb188-550">Il client e il server DEVONO essere configurati per avere set di caratteri interoperabili (fuori banda del protocollo).</span><span class="sxs-lookup"><span data-stu-id="cb188-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="cb188-551">Se vType è impostato su VT \_ LPWSTR, la struttura di vValue viene specificata nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="cb188-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="cb188-552">0</span><span class="sxs-lookup"><span data-stu-id="cb188-552">0</span></span>

<span data-ttu-id="cb188-553">1</span><span class="sxs-lookup"><span data-stu-id="cb188-553">1</span></span>

<span data-ttu-id="cb188-554">2</span><span class="sxs-lookup"><span data-stu-id="cb188-554">2</span></span>

<span data-ttu-id="cb188-555">3</span><span class="sxs-lookup"><span data-stu-id="cb188-555">3</span></span>

<span data-ttu-id="cb188-556">4</span><span class="sxs-lookup"><span data-stu-id="cb188-556">4</span></span>

<span data-ttu-id="cb188-557">5</span><span class="sxs-lookup"><span data-stu-id="cb188-557">5</span></span>

<span data-ttu-id="cb188-558">6</span><span class="sxs-lookup"><span data-stu-id="cb188-558">6</span></span>

<span data-ttu-id="cb188-559">7</span><span class="sxs-lookup"><span data-stu-id="cb188-559">7</span></span>

<span data-ttu-id="cb188-560">8</span><span class="sxs-lookup"><span data-stu-id="cb188-560">8</span></span>

<span data-ttu-id="cb188-561">9</span><span class="sxs-lookup"><span data-stu-id="cb188-561">9</span></span>

<span data-ttu-id="cb188-562">1</span><span class="sxs-lookup"><span data-stu-id="cb188-562">1</span></span><br/> <span data-ttu-id="cb188-563">0</span><span class="sxs-lookup"><span data-stu-id="cb188-563">0</span></span><br/>

<span data-ttu-id="cb188-564">1</span><span class="sxs-lookup"><span data-stu-id="cb188-564">1</span></span>

<span data-ttu-id="cb188-565">2</span><span class="sxs-lookup"><span data-stu-id="cb188-565">2</span></span>

<span data-ttu-id="cb188-566">3</span><span class="sxs-lookup"><span data-stu-id="cb188-566">3</span></span>

<span data-ttu-id="cb188-567">4</span><span class="sxs-lookup"><span data-stu-id="cb188-567">4</span></span>

<span data-ttu-id="cb188-568">5</span><span class="sxs-lookup"><span data-stu-id="cb188-568">5</span></span>

<span data-ttu-id="cb188-569">6</span><span class="sxs-lookup"><span data-stu-id="cb188-569">6</span></span>

<span data-ttu-id="cb188-570">7</span><span class="sxs-lookup"><span data-stu-id="cb188-570">7</span></span>

<span data-ttu-id="cb188-571">8</span><span class="sxs-lookup"><span data-stu-id="cb188-571">8</span></span>

<span data-ttu-id="cb188-572">9</span><span class="sxs-lookup"><span data-stu-id="cb188-572">9</span></span>

<span data-ttu-id="cb188-573">2</span><span class="sxs-lookup"><span data-stu-id="cb188-573">2</span></span><br/> <span data-ttu-id="cb188-574">0</span><span class="sxs-lookup"><span data-stu-id="cb188-574">0</span></span><br/>

<span data-ttu-id="cb188-575">1</span><span class="sxs-lookup"><span data-stu-id="cb188-575">1</span></span>

<span data-ttu-id="cb188-576">2</span><span class="sxs-lookup"><span data-stu-id="cb188-576">2</span></span>

<span data-ttu-id="cb188-577">3</span><span class="sxs-lookup"><span data-stu-id="cb188-577">3</span></span>

<span data-ttu-id="cb188-578">4</span><span class="sxs-lookup"><span data-stu-id="cb188-578">4</span></span>

<span data-ttu-id="cb188-579">5</span><span class="sxs-lookup"><span data-stu-id="cb188-579">5</span></span>

<span data-ttu-id="cb188-580">6</span><span class="sxs-lookup"><span data-stu-id="cb188-580">6</span></span>

<span data-ttu-id="cb188-581">7</span><span class="sxs-lookup"><span data-stu-id="cb188-581">7</span></span>

<span data-ttu-id="cb188-582">8</span><span class="sxs-lookup"><span data-stu-id="cb188-582">8</span></span>

<span data-ttu-id="cb188-583">9</span><span class="sxs-lookup"><span data-stu-id="cb188-583">9</span></span>

<span data-ttu-id="cb188-584">3</span><span class="sxs-lookup"><span data-stu-id="cb188-584">3</span></span><br/> <span data-ttu-id="cb188-585">0</span><span class="sxs-lookup"><span data-stu-id="cb188-585">0</span></span><br/>

<span data-ttu-id="cb188-586">1</span><span class="sxs-lookup"><span data-stu-id="cb188-586">1</span></span>

<span data-ttu-id="cb188-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="cb188-587">ccLen</span></span>

<span data-ttu-id="cb188-588">string (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-588">string (variable, optional)</span></span>



 

<span data-ttu-id="cb188-589">**ccLen:** intero senza segno a 32 bit, che indica le dimensioni del campo stringa in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb188-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="cb188-590">DEVE essere impostato su 0x00000000 per una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="cb188-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="cb188-591">**string:** stringa Unicode con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="cb188-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="cb188-592">2.2.1.1.1 Strutture CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="cb188-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="cb188-593">Le strutture seguenti vengono usate nella struttura CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cb188-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="cb188-594">2.2.1.1.1.1 DECIMALE</span><span class="sxs-lookup"><span data-stu-id="cb188-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="cb188-595">DECIMAL viene usato per rappresentare un valore numerico esatto con precisione fissa e scala fissa.</span><span class="sxs-lookup"><span data-stu-id="cb188-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="cb188-596">Quando vType è impostato su VT DECIMAL (0x0000E), i campi \_ vData1 e vData2 di CBaseStorageVariant DEVONO essere interpretati come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="cb188-597">**vData1:** numero di cifre a destra del separatore decimale.</span><span class="sxs-lookup"><span data-stu-id="cb188-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="cb188-598">DEVE essere compreso nell'intervallo da 0 a 28.</span><span class="sxs-lookup"><span data-stu-id="cb188-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="cb188-599">**vData2:** segno del valore numerico.</span><span class="sxs-lookup"><span data-stu-id="cb188-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="cb188-600">Impostare su 0x00 se positivo, 0x80 se negativo.</span><span class="sxs-lookup"><span data-stu-id="cb188-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="cb188-601">Il formato del campo vValue è:</span><span class="sxs-lookup"><span data-stu-id="cb188-601">The format of the vValue field is:</span></span>



<span data-ttu-id="cb188-602">0</span><span class="sxs-lookup"><span data-stu-id="cb188-602">0</span></span>

<span data-ttu-id="cb188-603">1</span><span class="sxs-lookup"><span data-stu-id="cb188-603">1</span></span>

<span data-ttu-id="cb188-604">2</span><span class="sxs-lookup"><span data-stu-id="cb188-604">2</span></span>

<span data-ttu-id="cb188-605">3</span><span class="sxs-lookup"><span data-stu-id="cb188-605">3</span></span>

<span data-ttu-id="cb188-606">4</span><span class="sxs-lookup"><span data-stu-id="cb188-606">4</span></span>

<span data-ttu-id="cb188-607">5</span><span class="sxs-lookup"><span data-stu-id="cb188-607">5</span></span>

<span data-ttu-id="cb188-608">6</span><span class="sxs-lookup"><span data-stu-id="cb188-608">6</span></span>

<span data-ttu-id="cb188-609">7</span><span class="sxs-lookup"><span data-stu-id="cb188-609">7</span></span>

<span data-ttu-id="cb188-610">8</span><span class="sxs-lookup"><span data-stu-id="cb188-610">8</span></span>

<span data-ttu-id="cb188-611">9</span><span class="sxs-lookup"><span data-stu-id="cb188-611">9</span></span>

<span data-ttu-id="cb188-612">1</span><span class="sxs-lookup"><span data-stu-id="cb188-612">1</span></span><br/> <span data-ttu-id="cb188-613">0</span><span class="sxs-lookup"><span data-stu-id="cb188-613">0</span></span><br/>

<span data-ttu-id="cb188-614">1</span><span class="sxs-lookup"><span data-stu-id="cb188-614">1</span></span>

<span data-ttu-id="cb188-615">2</span><span class="sxs-lookup"><span data-stu-id="cb188-615">2</span></span>

<span data-ttu-id="cb188-616">3</span><span class="sxs-lookup"><span data-stu-id="cb188-616">3</span></span>

<span data-ttu-id="cb188-617">4</span><span class="sxs-lookup"><span data-stu-id="cb188-617">4</span></span>

<span data-ttu-id="cb188-618">5</span><span class="sxs-lookup"><span data-stu-id="cb188-618">5</span></span>

<span data-ttu-id="cb188-619">6</span><span class="sxs-lookup"><span data-stu-id="cb188-619">6</span></span>

<span data-ttu-id="cb188-620">7</span><span class="sxs-lookup"><span data-stu-id="cb188-620">7</span></span>

<span data-ttu-id="cb188-621">8</span><span class="sxs-lookup"><span data-stu-id="cb188-621">8</span></span>

<span data-ttu-id="cb188-622">9</span><span class="sxs-lookup"><span data-stu-id="cb188-622">9</span></span>

<span data-ttu-id="cb188-623">2</span><span class="sxs-lookup"><span data-stu-id="cb188-623">2</span></span><br/> <span data-ttu-id="cb188-624">0</span><span class="sxs-lookup"><span data-stu-id="cb188-624">0</span></span><br/>

<span data-ttu-id="cb188-625">1</span><span class="sxs-lookup"><span data-stu-id="cb188-625">1</span></span>

<span data-ttu-id="cb188-626">2</span><span class="sxs-lookup"><span data-stu-id="cb188-626">2</span></span>

<span data-ttu-id="cb188-627">3</span><span class="sxs-lookup"><span data-stu-id="cb188-627">3</span></span>

<span data-ttu-id="cb188-628">4</span><span class="sxs-lookup"><span data-stu-id="cb188-628">4</span></span>

<span data-ttu-id="cb188-629">5</span><span class="sxs-lookup"><span data-stu-id="cb188-629">5</span></span>

<span data-ttu-id="cb188-630">6</span><span class="sxs-lookup"><span data-stu-id="cb188-630">6</span></span>

<span data-ttu-id="cb188-631">7</span><span class="sxs-lookup"><span data-stu-id="cb188-631">7</span></span>

<span data-ttu-id="cb188-632">8</span><span class="sxs-lookup"><span data-stu-id="cb188-632">8</span></span>

<span data-ttu-id="cb188-633">9</span><span class="sxs-lookup"><span data-stu-id="cb188-633">9</span></span>

<span data-ttu-id="cb188-634">3</span><span class="sxs-lookup"><span data-stu-id="cb188-634">3</span></span><br/> <span data-ttu-id="cb188-635">0</span><span class="sxs-lookup"><span data-stu-id="cb188-635">0</span></span><br/>

<span data-ttu-id="cb188-636">1</span><span class="sxs-lookup"><span data-stu-id="cb188-636">1</span></span>

<span data-ttu-id="cb188-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="cb188-637">Hi32</span></span>

<span data-ttu-id="cb188-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="cb188-638">Lo32</span></span>

<span data-ttu-id="cb188-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="cb188-639">Mid32</span></span>



 

<span data-ttu-id="cb188-640">**Hi32:** i 32 bit più alti dell'intero a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="cb188-641">**Lo32:** i 32 bit più bassi dell'intero a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="cb188-642">**Mid32:** i 32 bit intermedi dell'intero a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="cb188-643">2.2.1.1.1.2 VETTORE \_ VT</span><span class="sxs-lookup"><span data-stu-id="cb188-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="cb188-644">VT \_ Vector viene usato per passare matrici unidimensionali.</span><span class="sxs-lookup"><span data-stu-id="cb188-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="cb188-645">0</span><span class="sxs-lookup"><span data-stu-id="cb188-645">0</span></span>

<span data-ttu-id="cb188-646">1</span><span class="sxs-lookup"><span data-stu-id="cb188-646">1</span></span>

<span data-ttu-id="cb188-647">2</span><span class="sxs-lookup"><span data-stu-id="cb188-647">2</span></span>

<span data-ttu-id="cb188-648">3</span><span class="sxs-lookup"><span data-stu-id="cb188-648">3</span></span>

<span data-ttu-id="cb188-649">4</span><span class="sxs-lookup"><span data-stu-id="cb188-649">4</span></span>

<span data-ttu-id="cb188-650">5</span><span class="sxs-lookup"><span data-stu-id="cb188-650">5</span></span>

<span data-ttu-id="cb188-651">6</span><span class="sxs-lookup"><span data-stu-id="cb188-651">6</span></span>

<span data-ttu-id="cb188-652">7</span><span class="sxs-lookup"><span data-stu-id="cb188-652">7</span></span>

<span data-ttu-id="cb188-653">8</span><span class="sxs-lookup"><span data-stu-id="cb188-653">8</span></span>

<span data-ttu-id="cb188-654">9</span><span class="sxs-lookup"><span data-stu-id="cb188-654">9</span></span>

<span data-ttu-id="cb188-655">1</span><span class="sxs-lookup"><span data-stu-id="cb188-655">1</span></span><br/> <span data-ttu-id="cb188-656">0</span><span class="sxs-lookup"><span data-stu-id="cb188-656">0</span></span><br/>

<span data-ttu-id="cb188-657">1</span><span class="sxs-lookup"><span data-stu-id="cb188-657">1</span></span>

<span data-ttu-id="cb188-658">2</span><span class="sxs-lookup"><span data-stu-id="cb188-658">2</span></span>

<span data-ttu-id="cb188-659">3</span><span class="sxs-lookup"><span data-stu-id="cb188-659">3</span></span>

<span data-ttu-id="cb188-660">4</span><span class="sxs-lookup"><span data-stu-id="cb188-660">4</span></span>

<span data-ttu-id="cb188-661">5</span><span class="sxs-lookup"><span data-stu-id="cb188-661">5</span></span>

<span data-ttu-id="cb188-662">6</span><span class="sxs-lookup"><span data-stu-id="cb188-662">6</span></span>

<span data-ttu-id="cb188-663">7</span><span class="sxs-lookup"><span data-stu-id="cb188-663">7</span></span>

<span data-ttu-id="cb188-664">8</span><span class="sxs-lookup"><span data-stu-id="cb188-664">8</span></span>

<span data-ttu-id="cb188-665">9</span><span class="sxs-lookup"><span data-stu-id="cb188-665">9</span></span>

<span data-ttu-id="cb188-666">2</span><span class="sxs-lookup"><span data-stu-id="cb188-666">2</span></span><br/> <span data-ttu-id="cb188-667">0</span><span class="sxs-lookup"><span data-stu-id="cb188-667">0</span></span><br/>

<span data-ttu-id="cb188-668">1</span><span class="sxs-lookup"><span data-stu-id="cb188-668">1</span></span>

<span data-ttu-id="cb188-669">2</span><span class="sxs-lookup"><span data-stu-id="cb188-669">2</span></span>

<span data-ttu-id="cb188-670">3</span><span class="sxs-lookup"><span data-stu-id="cb188-670">3</span></span>

<span data-ttu-id="cb188-671">4</span><span class="sxs-lookup"><span data-stu-id="cb188-671">4</span></span>

<span data-ttu-id="cb188-672">5</span><span class="sxs-lookup"><span data-stu-id="cb188-672">5</span></span>

<span data-ttu-id="cb188-673">6</span><span class="sxs-lookup"><span data-stu-id="cb188-673">6</span></span>

<span data-ttu-id="cb188-674">7</span><span class="sxs-lookup"><span data-stu-id="cb188-674">7</span></span>

<span data-ttu-id="cb188-675">8</span><span class="sxs-lookup"><span data-stu-id="cb188-675">8</span></span>

<span data-ttu-id="cb188-676">9</span><span class="sxs-lookup"><span data-stu-id="cb188-676">9</span></span>

<span data-ttu-id="cb188-677">3</span><span class="sxs-lookup"><span data-stu-id="cb188-677">3</span></span><br/> <span data-ttu-id="cb188-678">0</span><span class="sxs-lookup"><span data-stu-id="cb188-678">0</span></span><br/>

<span data-ttu-id="cb188-679">1</span><span class="sxs-lookup"><span data-stu-id="cb188-679">1</span></span>

<span data-ttu-id="cb188-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="cb188-680">vVectorElements</span></span>

<span data-ttu-id="cb188-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="cb188-681">vVectorData</span></span>



 

<span data-ttu-id="cb188-682">**vVectorElements:** intero senza segno a 32 bit, che indica il numero di elementi nel campo vVectorData.</span><span class="sxs-lookup"><span data-stu-id="cb188-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="cb188-683">**vVectorData:** matrice di elementi con un tipo indicato da vType con il 0x1000 bit cancellato.</span><span class="sxs-lookup"><span data-stu-id="cb188-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="cb188-684">Le dimensioni di un singolo elemento a lunghezza fissa possono essere ottenute dalla tabella con tipo di dati a lunghezza fissa, come specificato nella sezione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="cb188-685">La lunghezza di questo campo, in byte, può essere calcolata moltiplicando vVectorElements per le dimensioni del singolo elemento.</span><span class="sxs-lookup"><span data-stu-id="cb188-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="cb188-686">Per i tipi di dati a lunghezza variabile vVectorData contiene una sequenza di tipi semplici con marshalling consecutivo in cui il tipo è indicato da vType con 0x1000 bit cancellato.</span><span class="sxs-lookup"><span data-stu-id="cb188-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="cb188-687">Ciò include un caso speciale indicato da vType VT \_ ARRAY \| VT \_ VARIANT (ad esempio, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="cb188-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="cb188-688">Gli elementi nel campo vVectorData DEVONO essere separati da 0 a 3 byte di riempimento in modo che ogni elemento inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice.</span><span class="sxs-lookup"><span data-stu-id="cb188-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cb188-689">Se sono presenti byte di riempimento, il valore in essi contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cb188-690">Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-691">Per un vType impostato su VT ARRAY VT VARIANT, il tipo per gli elementi in questa sequenza \_ \| è \_ CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cb188-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="cb188-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="cb188-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="cb188-693">SAFEARRAY viene usato per passare matrici multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="cb188-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="cb188-694">La struttura contiene informazioni sulle dimensioni della matrice, nonché i dati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="cb188-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="cb188-695">0</span><span class="sxs-lookup"><span data-stu-id="cb188-695">0</span></span>

<span data-ttu-id="cb188-696">1</span><span class="sxs-lookup"><span data-stu-id="cb188-696">1</span></span>

<span data-ttu-id="cb188-697">2</span><span class="sxs-lookup"><span data-stu-id="cb188-697">2</span></span>

<span data-ttu-id="cb188-698">3</span><span class="sxs-lookup"><span data-stu-id="cb188-698">3</span></span>

<span data-ttu-id="cb188-699">4</span><span class="sxs-lookup"><span data-stu-id="cb188-699">4</span></span>

<span data-ttu-id="cb188-700">5</span><span class="sxs-lookup"><span data-stu-id="cb188-700">5</span></span>

<span data-ttu-id="cb188-701">6</span><span class="sxs-lookup"><span data-stu-id="cb188-701">6</span></span>

<span data-ttu-id="cb188-702">7</span><span class="sxs-lookup"><span data-stu-id="cb188-702">7</span></span>

<span data-ttu-id="cb188-703">8</span><span class="sxs-lookup"><span data-stu-id="cb188-703">8</span></span>

<span data-ttu-id="cb188-704">9</span><span class="sxs-lookup"><span data-stu-id="cb188-704">9</span></span>

<span data-ttu-id="cb188-705">1</span><span class="sxs-lookup"><span data-stu-id="cb188-705">1</span></span><br/> <span data-ttu-id="cb188-706">0</span><span class="sxs-lookup"><span data-stu-id="cb188-706">0</span></span><br/>

<span data-ttu-id="cb188-707">1</span><span class="sxs-lookup"><span data-stu-id="cb188-707">1</span></span>

<span data-ttu-id="cb188-708">2</span><span class="sxs-lookup"><span data-stu-id="cb188-708">2</span></span>

<span data-ttu-id="cb188-709">3</span><span class="sxs-lookup"><span data-stu-id="cb188-709">3</span></span>

<span data-ttu-id="cb188-710">4</span><span class="sxs-lookup"><span data-stu-id="cb188-710">4</span></span>

<span data-ttu-id="cb188-711">5</span><span class="sxs-lookup"><span data-stu-id="cb188-711">5</span></span>

<span data-ttu-id="cb188-712">6</span><span class="sxs-lookup"><span data-stu-id="cb188-712">6</span></span>

<span data-ttu-id="cb188-713">7</span><span class="sxs-lookup"><span data-stu-id="cb188-713">7</span></span>

<span data-ttu-id="cb188-714">8</span><span class="sxs-lookup"><span data-stu-id="cb188-714">8</span></span>

<span data-ttu-id="cb188-715">9</span><span class="sxs-lookup"><span data-stu-id="cb188-715">9</span></span>

<span data-ttu-id="cb188-716">2</span><span class="sxs-lookup"><span data-stu-id="cb188-716">2</span></span><br/> <span data-ttu-id="cb188-717">0</span><span class="sxs-lookup"><span data-stu-id="cb188-717">0</span></span><br/>

<span data-ttu-id="cb188-718">1</span><span class="sxs-lookup"><span data-stu-id="cb188-718">1</span></span>

<span data-ttu-id="cb188-719">2</span><span class="sxs-lookup"><span data-stu-id="cb188-719">2</span></span>

<span data-ttu-id="cb188-720">3</span><span class="sxs-lookup"><span data-stu-id="cb188-720">3</span></span>

<span data-ttu-id="cb188-721">4</span><span class="sxs-lookup"><span data-stu-id="cb188-721">4</span></span>

<span data-ttu-id="cb188-722">5</span><span class="sxs-lookup"><span data-stu-id="cb188-722">5</span></span>

<span data-ttu-id="cb188-723">6</span><span class="sxs-lookup"><span data-stu-id="cb188-723">6</span></span>

<span data-ttu-id="cb188-724">7</span><span class="sxs-lookup"><span data-stu-id="cb188-724">7</span></span>

<span data-ttu-id="cb188-725">8</span><span class="sxs-lookup"><span data-stu-id="cb188-725">8</span></span>

<span data-ttu-id="cb188-726">9</span><span class="sxs-lookup"><span data-stu-id="cb188-726">9</span></span>

<span data-ttu-id="cb188-727">3</span><span class="sxs-lookup"><span data-stu-id="cb188-727">3</span></span><br/> <span data-ttu-id="cb188-728">0</span><span class="sxs-lookup"><span data-stu-id="cb188-728">0</span></span><br/>

<span data-ttu-id="cb188-729">1</span><span class="sxs-lookup"><span data-stu-id="cb188-729">1</span></span>

<span data-ttu-id="cb188-730">cDims</span><span class="sxs-lookup"><span data-stu-id="cb188-730">cDims</span></span>

<span data-ttu-id="cb188-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="cb188-731">fFeatures</span></span>

<span data-ttu-id="cb188-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="cb188-732">cbElements</span></span>

<span data-ttu-id="cb188-733">Rgsabound (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-733">Rgsabound (variable)</span></span>

<span data-ttu-id="cb188-734">vData (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-734">vData (variable)</span></span>



 

<span data-ttu-id="cb188-735">**cDims:** intero senza segno a 16 bit, che indica il numero di dimensioni della matrice multidimensionale.</span><span class="sxs-lookup"><span data-stu-id="cb188-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="cb188-736">**fFeatures:** campo di bit a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="cb188-737">I valori rappresentano le funzionalità definite dalle applicazioni di livello superiore e DEVONO essere ignorate.</span><span class="sxs-lookup"><span data-stu-id="cb188-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="cb188-738">**cbElements:** intero senza segno a 32 bit che specifica le dimensioni di ogni elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="cb188-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="cb188-739">**Rgsabound:** matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4, per dimensione in SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="cb188-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="cb188-740">Questa matrice ha prima la dimensione più a sinistra e la dimensione più a destra per ultima.</span><span class="sxs-lookup"><span data-stu-id="cb188-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="cb188-741">**vData:** vettore di elementi di cui è stato effettuato il marshalling di un determinato tipo, indicato dal tipo vType dell'oggetto CBaseStorageVariant contenitore, con il bit 0x2000 cancellato.</span><span class="sxs-lookup"><span data-stu-id="cb188-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="cb188-742">Il marshalling di vData viene eseguito in modo analogo a VT VECTOR, come specificato nella Sezione 2.2.1.1.1.2, con la differenza che il numero di elementi non viene archiviato davanti al \_ vettore.</span><span class="sxs-lookup"><span data-stu-id="cb188-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="cb188-743">Il numero di elementi viene invece calcolato moltiplicando il valore cElements con tutti i limiti di matrice sicuri nel campo Rgsabound.</span><span class="sxs-lookup"><span data-stu-id="cb188-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="cb188-744">Gli elementi vengono archiviati in un vettore in ordine di dimensioni, che iniziano con la dimensione più a destra.</span><span class="sxs-lookup"><span data-stu-id="cb188-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="cb188-745">Il diagramma seguente rappresenta visivamente una matrice bidimensionale di esempio.</span><span class="sxs-lookup"><span data-stu-id="cb188-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="cb188-746">La prima dimensione ha cElements uguale a 4 (rappresentato orizzontalmente) e lLbound uguale a 0 e la seconda dimensione ha cElements uguale a 2 (rappresentato verticalmente) e lLbound uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="cb188-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="cb188-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-747">0x00000001</span></span> | <span data-ttu-id="cb188-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-748">0x00000002</span></span> | <span data-ttu-id="cb188-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-749">0x00000003</span></span> | <span data-ttu-id="cb188-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cb188-750">0x00000005</span></span> |
| <span data-ttu-id="cb188-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb188-751">0x00000007</span></span> | <span data-ttu-id="cb188-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="cb188-752">0x00000011</span></span> | <span data-ttu-id="cb188-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="cb188-753">0x00000013</span></span> | <span data-ttu-id="cb188-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="cb188-754">0x00000017</span></span> |



 

<span data-ttu-id="cb188-755">Usando il diagramma precedente, vData conterrà la sequenza seguente: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (scorrere prima la dimensione più a destra, quindi incrementare la dimensione successiva).</span><span class="sxs-lookup"><span data-stu-id="cb188-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="cb188-756">L'oggetto Rgsabound precedente (che registra cElements e Lbound) sarà: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="cb188-757">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="cb188-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="cb188-758">La struttura SAFEARRAYBOUND rappresenta i limiti di una dimensione di SAFEARRAY o SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="cb188-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="cb188-759">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="cb188-759">Its format is:</span></span>



<span data-ttu-id="cb188-760">0</span><span class="sxs-lookup"><span data-stu-id="cb188-760">0</span></span>

<span data-ttu-id="cb188-761">1</span><span class="sxs-lookup"><span data-stu-id="cb188-761">1</span></span>

<span data-ttu-id="cb188-762">2</span><span class="sxs-lookup"><span data-stu-id="cb188-762">2</span></span>

<span data-ttu-id="cb188-763">3</span><span class="sxs-lookup"><span data-stu-id="cb188-763">3</span></span>

<span data-ttu-id="cb188-764">4</span><span class="sxs-lookup"><span data-stu-id="cb188-764">4</span></span>

<span data-ttu-id="cb188-765">5</span><span class="sxs-lookup"><span data-stu-id="cb188-765">5</span></span>

<span data-ttu-id="cb188-766">6</span><span class="sxs-lookup"><span data-stu-id="cb188-766">6</span></span>

<span data-ttu-id="cb188-767">7</span><span class="sxs-lookup"><span data-stu-id="cb188-767">7</span></span>

<span data-ttu-id="cb188-768">8</span><span class="sxs-lookup"><span data-stu-id="cb188-768">8</span></span>

<span data-ttu-id="cb188-769">9</span><span class="sxs-lookup"><span data-stu-id="cb188-769">9</span></span>

<span data-ttu-id="cb188-770">1</span><span class="sxs-lookup"><span data-stu-id="cb188-770">1</span></span><br/> <span data-ttu-id="cb188-771">0</span><span class="sxs-lookup"><span data-stu-id="cb188-771">0</span></span><br/>

<span data-ttu-id="cb188-772">1</span><span class="sxs-lookup"><span data-stu-id="cb188-772">1</span></span>

<span data-ttu-id="cb188-773">2</span><span class="sxs-lookup"><span data-stu-id="cb188-773">2</span></span>

<span data-ttu-id="cb188-774">3</span><span class="sxs-lookup"><span data-stu-id="cb188-774">3</span></span>

<span data-ttu-id="cb188-775">4</span><span class="sxs-lookup"><span data-stu-id="cb188-775">4</span></span>

<span data-ttu-id="cb188-776">5</span><span class="sxs-lookup"><span data-stu-id="cb188-776">5</span></span>

<span data-ttu-id="cb188-777">6</span><span class="sxs-lookup"><span data-stu-id="cb188-777">6</span></span>

<span data-ttu-id="cb188-778">7</span><span class="sxs-lookup"><span data-stu-id="cb188-778">7</span></span>

<span data-ttu-id="cb188-779">8</span><span class="sxs-lookup"><span data-stu-id="cb188-779">8</span></span>

<span data-ttu-id="cb188-780">9</span><span class="sxs-lookup"><span data-stu-id="cb188-780">9</span></span>

<span data-ttu-id="cb188-781">2</span><span class="sxs-lookup"><span data-stu-id="cb188-781">2</span></span><br/> <span data-ttu-id="cb188-782">0</span><span class="sxs-lookup"><span data-stu-id="cb188-782">0</span></span><br/>

<span data-ttu-id="cb188-783">1</span><span class="sxs-lookup"><span data-stu-id="cb188-783">1</span></span>

<span data-ttu-id="cb188-784">2</span><span class="sxs-lookup"><span data-stu-id="cb188-784">2</span></span>

<span data-ttu-id="cb188-785">3</span><span class="sxs-lookup"><span data-stu-id="cb188-785">3</span></span>

<span data-ttu-id="cb188-786">4</span><span class="sxs-lookup"><span data-stu-id="cb188-786">4</span></span>

<span data-ttu-id="cb188-787">5</span><span class="sxs-lookup"><span data-stu-id="cb188-787">5</span></span>

<span data-ttu-id="cb188-788">6</span><span class="sxs-lookup"><span data-stu-id="cb188-788">6</span></span>

<span data-ttu-id="cb188-789">7</span><span class="sxs-lookup"><span data-stu-id="cb188-789">7</span></span>

<span data-ttu-id="cb188-790">8</span><span class="sxs-lookup"><span data-stu-id="cb188-790">8</span></span>

<span data-ttu-id="cb188-791">9</span><span class="sxs-lookup"><span data-stu-id="cb188-791">9</span></span>

<span data-ttu-id="cb188-792">3</span><span class="sxs-lookup"><span data-stu-id="cb188-792">3</span></span><br/> <span data-ttu-id="cb188-793">0</span><span class="sxs-lookup"><span data-stu-id="cb188-793">0</span></span><br/>

<span data-ttu-id="cb188-794">1</span><span class="sxs-lookup"><span data-stu-id="cb188-794">1</span></span>

<span data-ttu-id="cb188-795">cElements</span><span class="sxs-lookup"><span data-stu-id="cb188-795">cElements</span></span>

<span data-ttu-id="cb188-796">lLbound</span><span class="sxs-lookup"><span data-stu-id="cb188-796">lLbound</span></span>



 

<span data-ttu-id="cb188-797">**cElements:** intero senza segno a 32 bit che specifica il numero di elementi nella dimensione.</span><span class="sxs-lookup"><span data-stu-id="cb188-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="cb188-798">**lLbound:** intero senza segno a 32 bit che specifica il limite inferiore della dimensione.</span><span class="sxs-lookup"><span data-stu-id="cb188-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="cb188-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="cb188-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="cb188-800">SAFEARRAY2 viene usato per passare matrici multidimensionali in SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="cb188-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="cb188-801">La struttura contiene informazioni sui limiti e i dati.</span><span class="sxs-lookup"><span data-stu-id="cb188-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="cb188-802">0</span><span class="sxs-lookup"><span data-stu-id="cb188-802">0</span></span>

<span data-ttu-id="cb188-803">1</span><span class="sxs-lookup"><span data-stu-id="cb188-803">1</span></span>

<span data-ttu-id="cb188-804">2</span><span class="sxs-lookup"><span data-stu-id="cb188-804">2</span></span>

<span data-ttu-id="cb188-805">3</span><span class="sxs-lookup"><span data-stu-id="cb188-805">3</span></span>

<span data-ttu-id="cb188-806">4</span><span class="sxs-lookup"><span data-stu-id="cb188-806">4</span></span>

<span data-ttu-id="cb188-807">5</span><span class="sxs-lookup"><span data-stu-id="cb188-807">5</span></span>

<span data-ttu-id="cb188-808">6</span><span class="sxs-lookup"><span data-stu-id="cb188-808">6</span></span>

<span data-ttu-id="cb188-809">7</span><span class="sxs-lookup"><span data-stu-id="cb188-809">7</span></span>

<span data-ttu-id="cb188-810">8</span><span class="sxs-lookup"><span data-stu-id="cb188-810">8</span></span>

<span data-ttu-id="cb188-811">9</span><span class="sxs-lookup"><span data-stu-id="cb188-811">9</span></span>

<span data-ttu-id="cb188-812">1</span><span class="sxs-lookup"><span data-stu-id="cb188-812">1</span></span><br/> <span data-ttu-id="cb188-813">0</span><span class="sxs-lookup"><span data-stu-id="cb188-813">0</span></span><br/>

<span data-ttu-id="cb188-814">1</span><span class="sxs-lookup"><span data-stu-id="cb188-814">1</span></span>

<span data-ttu-id="cb188-815">2</span><span class="sxs-lookup"><span data-stu-id="cb188-815">2</span></span>

<span data-ttu-id="cb188-816">3</span><span class="sxs-lookup"><span data-stu-id="cb188-816">3</span></span>

<span data-ttu-id="cb188-817">4</span><span class="sxs-lookup"><span data-stu-id="cb188-817">4</span></span>

<span data-ttu-id="cb188-818">5</span><span class="sxs-lookup"><span data-stu-id="cb188-818">5</span></span>

<span data-ttu-id="cb188-819">6</span><span class="sxs-lookup"><span data-stu-id="cb188-819">6</span></span>

<span data-ttu-id="cb188-820">7</span><span class="sxs-lookup"><span data-stu-id="cb188-820">7</span></span>

<span data-ttu-id="cb188-821">8</span><span class="sxs-lookup"><span data-stu-id="cb188-821">8</span></span>

<span data-ttu-id="cb188-822">9</span><span class="sxs-lookup"><span data-stu-id="cb188-822">9</span></span>

<span data-ttu-id="cb188-823">2</span><span class="sxs-lookup"><span data-stu-id="cb188-823">2</span></span><br/> <span data-ttu-id="cb188-824">0</span><span class="sxs-lookup"><span data-stu-id="cb188-824">0</span></span><br/>

<span data-ttu-id="cb188-825">1</span><span class="sxs-lookup"><span data-stu-id="cb188-825">1</span></span>

<span data-ttu-id="cb188-826">2</span><span class="sxs-lookup"><span data-stu-id="cb188-826">2</span></span>

<span data-ttu-id="cb188-827">3</span><span class="sxs-lookup"><span data-stu-id="cb188-827">3</span></span>

<span data-ttu-id="cb188-828">4</span><span class="sxs-lookup"><span data-stu-id="cb188-828">4</span></span>

<span data-ttu-id="cb188-829">5</span><span class="sxs-lookup"><span data-stu-id="cb188-829">5</span></span>

<span data-ttu-id="cb188-830">6</span><span class="sxs-lookup"><span data-stu-id="cb188-830">6</span></span>

<span data-ttu-id="cb188-831">7</span><span class="sxs-lookup"><span data-stu-id="cb188-831">7</span></span>

<span data-ttu-id="cb188-832">8</span><span class="sxs-lookup"><span data-stu-id="cb188-832">8</span></span>

<span data-ttu-id="cb188-833">9</span><span class="sxs-lookup"><span data-stu-id="cb188-833">9</span></span>

<span data-ttu-id="cb188-834">3</span><span class="sxs-lookup"><span data-stu-id="cb188-834">3</span></span><br/> <span data-ttu-id="cb188-835">0</span><span class="sxs-lookup"><span data-stu-id="cb188-835">0</span></span><br/>

<span data-ttu-id="cb188-836">1</span><span class="sxs-lookup"><span data-stu-id="cb188-836">1</span></span>

<span data-ttu-id="cb188-837">cDims</span><span class="sxs-lookup"><span data-stu-id="cb188-837">cDims</span></span>

<span data-ttu-id="cb188-838">Rgsabound (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-838">Rgsabound (variable)</span></span>

<span data-ttu-id="cb188-839">vData (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-839">vData (variable)</span></span>



 

<span data-ttu-id="cb188-840">**cDims:** intero senza segno a 32 bit, che indica il numero di dimensioni di SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="cb188-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="cb188-841">**Rgsabound:** matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4 per dimensione in SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="cb188-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="cb188-842">Questa matrice ha prima la dimensione più a sinistra e la dimensione più a destra per ultima.</span><span class="sxs-lookup"><span data-stu-id="cb188-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="cb188-843">**vData:** vettore di elementi di cui è stato effettuato il marshalling di un particolare tipo, indicato da dwType dell'oggetto SERIALIZEDPROPERTYVALUE contenitore, con i bit 0x2000 cancellati.</span><span class="sxs-lookup"><span data-stu-id="cb188-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="cb188-844">Il formato di vData corrisponde a quello specificato per il campo vData di SAFEARRAY nella sezione 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="cb188-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="cb188-845">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="cb188-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="cb188-846">La struttura CFullPropSpec contiene un GUID del set di proprietà e un identificatore di proprietà per identificare in modo univoco la proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="cb188-847">0</span><span class="sxs-lookup"><span data-stu-id="cb188-847">0</span></span>

<span data-ttu-id="cb188-848">1</span><span class="sxs-lookup"><span data-stu-id="cb188-848">1</span></span>

<span data-ttu-id="cb188-849">2</span><span class="sxs-lookup"><span data-stu-id="cb188-849">2</span></span>

<span data-ttu-id="cb188-850">3</span><span class="sxs-lookup"><span data-stu-id="cb188-850">3</span></span>

<span data-ttu-id="cb188-851">4</span><span class="sxs-lookup"><span data-stu-id="cb188-851">4</span></span>

<span data-ttu-id="cb188-852">5</span><span class="sxs-lookup"><span data-stu-id="cb188-852">5</span></span>

<span data-ttu-id="cb188-853">6</span><span class="sxs-lookup"><span data-stu-id="cb188-853">6</span></span>

<span data-ttu-id="cb188-854">7</span><span class="sxs-lookup"><span data-stu-id="cb188-854">7</span></span>

<span data-ttu-id="cb188-855">8</span><span class="sxs-lookup"><span data-stu-id="cb188-855">8</span></span>

<span data-ttu-id="cb188-856">9</span><span class="sxs-lookup"><span data-stu-id="cb188-856">9</span></span>

<span data-ttu-id="cb188-857">1</span><span class="sxs-lookup"><span data-stu-id="cb188-857">1</span></span><br/> <span data-ttu-id="cb188-858">0</span><span class="sxs-lookup"><span data-stu-id="cb188-858">0</span></span><br/>

<span data-ttu-id="cb188-859">1</span><span class="sxs-lookup"><span data-stu-id="cb188-859">1</span></span>

<span data-ttu-id="cb188-860">2</span><span class="sxs-lookup"><span data-stu-id="cb188-860">2</span></span>

<span data-ttu-id="cb188-861">3</span><span class="sxs-lookup"><span data-stu-id="cb188-861">3</span></span>

<span data-ttu-id="cb188-862">4</span><span class="sxs-lookup"><span data-stu-id="cb188-862">4</span></span>

<span data-ttu-id="cb188-863">5</span><span class="sxs-lookup"><span data-stu-id="cb188-863">5</span></span>

<span data-ttu-id="cb188-864">6</span><span class="sxs-lookup"><span data-stu-id="cb188-864">6</span></span>

<span data-ttu-id="cb188-865">7</span><span class="sxs-lookup"><span data-stu-id="cb188-865">7</span></span>

<span data-ttu-id="cb188-866">8</span><span class="sxs-lookup"><span data-stu-id="cb188-866">8</span></span>

<span data-ttu-id="cb188-867">9</span><span class="sxs-lookup"><span data-stu-id="cb188-867">9</span></span>

<span data-ttu-id="cb188-868">2</span><span class="sxs-lookup"><span data-stu-id="cb188-868">2</span></span><br/> <span data-ttu-id="cb188-869">0</span><span class="sxs-lookup"><span data-stu-id="cb188-869">0</span></span><br/>

<span data-ttu-id="cb188-870">1</span><span class="sxs-lookup"><span data-stu-id="cb188-870">1</span></span>

<span data-ttu-id="cb188-871">2</span><span class="sxs-lookup"><span data-stu-id="cb188-871">2</span></span>

<span data-ttu-id="cb188-872">3</span><span class="sxs-lookup"><span data-stu-id="cb188-872">3</span></span>

<span data-ttu-id="cb188-873">4</span><span class="sxs-lookup"><span data-stu-id="cb188-873">4</span></span>

<span data-ttu-id="cb188-874">5</span><span class="sxs-lookup"><span data-stu-id="cb188-874">5</span></span>

<span data-ttu-id="cb188-875">6</span><span class="sxs-lookup"><span data-stu-id="cb188-875">6</span></span>

<span data-ttu-id="cb188-876">7</span><span class="sxs-lookup"><span data-stu-id="cb188-876">7</span></span>

<span data-ttu-id="cb188-877">8</span><span class="sxs-lookup"><span data-stu-id="cb188-877">8</span></span>

<span data-ttu-id="cb188-878">9</span><span class="sxs-lookup"><span data-stu-id="cb188-878">9</span></span>

<span data-ttu-id="cb188-879">3</span><span class="sxs-lookup"><span data-stu-id="cb188-879">3</span></span><br/> <span data-ttu-id="cb188-880">0</span><span class="sxs-lookup"><span data-stu-id="cb188-880">0</span></span><br/>

<span data-ttu-id="cb188-881">1</span><span class="sxs-lookup"><span data-stu-id="cb188-881">1</span></span>

<span data-ttu-id="cb188-882">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="cb188-882">\_guidPropSet</span></span>

<span data-ttu-id="cb188-883">...</span><span class="sxs-lookup"><span data-stu-id="cb188-883">...</span></span>

<span data-ttu-id="cb188-884">...</span><span class="sxs-lookup"><span data-stu-id="cb188-884">...</span></span>

<span data-ttu-id="cb188-885">...</span><span class="sxs-lookup"><span data-stu-id="cb188-885">...</span></span>

<span data-ttu-id="cb188-886">ulKind</span><span class="sxs-lookup"><span data-stu-id="cb188-886">ulKind</span></span>

<span data-ttu-id="cb188-887">PrSpec</span><span class="sxs-lookup"><span data-stu-id="cb188-887">PrSpec</span></span>

<span data-ttu-id="cb188-888">Nome proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-888">Property name (variable)</span></span>



 

<span data-ttu-id="cb188-889">**\_ guidPropSet:** GUID del set di proprietà a cui appartiene la proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="cb188-890">**ulKind:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cb188-891">Uno dei valori seguenti, che indica il contenuto di PrSpec.</span><span class="sxs-lookup"><span data-stu-id="cb188-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="cb188-892">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-892">Value</span></span>                                            | <span data-ttu-id="cb188-893">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-894">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="cb188-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="cb188-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-895">0x00000000</span></span><br/> | <span data-ttu-id="cb188-896">Il campo PrSpec specifica il numero di caratteri non NULL nel campo Nome proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="cb188-897">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="cb188-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="cb188-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-898">0x00000001</span></span><br/>  | <span data-ttu-id="cb188-899">Il campo PrSpec specifica l'ID proprietà (PROPID).</span><span class="sxs-lookup"><span data-stu-id="cb188-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="cb188-900">**PrSpec:** intero senza segno a 32 bit con un significato indicato dal campo ulKind.</span><span class="sxs-lookup"><span data-stu-id="cb188-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="cb188-901">**Nome proprietà:** se ulKind è impostato su PRSPEC \_ PROPID, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="cb188-902">Se ulKind è impostato su PRSPEC LPWSTR, questo campo DEVE contenere una matrice senza distinzione tra maiuscole e minuscole di caratteri Unicode PrSpec non Null, contenente il nome della \_ proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="cb188-903">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="cb188-904">La struttura CContentRestriction contiene una stringa che corrisponde a una proprietà nella cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="cb188-905">0</span><span class="sxs-lookup"><span data-stu-id="cb188-905">0</span></span>

<span data-ttu-id="cb188-906">1</span><span class="sxs-lookup"><span data-stu-id="cb188-906">1</span></span>

<span data-ttu-id="cb188-907">2</span><span class="sxs-lookup"><span data-stu-id="cb188-907">2</span></span>

<span data-ttu-id="cb188-908">3</span><span class="sxs-lookup"><span data-stu-id="cb188-908">3</span></span>

<span data-ttu-id="cb188-909">4</span><span class="sxs-lookup"><span data-stu-id="cb188-909">4</span></span>

<span data-ttu-id="cb188-910">5</span><span class="sxs-lookup"><span data-stu-id="cb188-910">5</span></span>

<span data-ttu-id="cb188-911">6</span><span class="sxs-lookup"><span data-stu-id="cb188-911">6</span></span>

<span data-ttu-id="cb188-912">7</span><span class="sxs-lookup"><span data-stu-id="cb188-912">7</span></span>

<span data-ttu-id="cb188-913">8</span><span class="sxs-lookup"><span data-stu-id="cb188-913">8</span></span>

<span data-ttu-id="cb188-914">9</span><span class="sxs-lookup"><span data-stu-id="cb188-914">9</span></span>

<span data-ttu-id="cb188-915">1</span><span class="sxs-lookup"><span data-stu-id="cb188-915">1</span></span><br/> <span data-ttu-id="cb188-916">0</span><span class="sxs-lookup"><span data-stu-id="cb188-916">0</span></span><br/>

<span data-ttu-id="cb188-917">1</span><span class="sxs-lookup"><span data-stu-id="cb188-917">1</span></span>

<span data-ttu-id="cb188-918">2</span><span class="sxs-lookup"><span data-stu-id="cb188-918">2</span></span>

<span data-ttu-id="cb188-919">3</span><span class="sxs-lookup"><span data-stu-id="cb188-919">3</span></span>

<span data-ttu-id="cb188-920">4</span><span class="sxs-lookup"><span data-stu-id="cb188-920">4</span></span>

<span data-ttu-id="cb188-921">5</span><span class="sxs-lookup"><span data-stu-id="cb188-921">5</span></span>

<span data-ttu-id="cb188-922">6</span><span class="sxs-lookup"><span data-stu-id="cb188-922">6</span></span>

<span data-ttu-id="cb188-923">7</span><span class="sxs-lookup"><span data-stu-id="cb188-923">7</span></span>

<span data-ttu-id="cb188-924">8</span><span class="sxs-lookup"><span data-stu-id="cb188-924">8</span></span>

<span data-ttu-id="cb188-925">9</span><span class="sxs-lookup"><span data-stu-id="cb188-925">9</span></span>

<span data-ttu-id="cb188-926">2</span><span class="sxs-lookup"><span data-stu-id="cb188-926">2</span></span><br/> <span data-ttu-id="cb188-927">0</span><span class="sxs-lookup"><span data-stu-id="cb188-927">0</span></span><br/>

<span data-ttu-id="cb188-928">1</span><span class="sxs-lookup"><span data-stu-id="cb188-928">1</span></span>

<span data-ttu-id="cb188-929">2</span><span class="sxs-lookup"><span data-stu-id="cb188-929">2</span></span>

<span data-ttu-id="cb188-930">3</span><span class="sxs-lookup"><span data-stu-id="cb188-930">3</span></span>

<span data-ttu-id="cb188-931">4</span><span class="sxs-lookup"><span data-stu-id="cb188-931">4</span></span>

<span data-ttu-id="cb188-932">5</span><span class="sxs-lookup"><span data-stu-id="cb188-932">5</span></span>

<span data-ttu-id="cb188-933">6</span><span class="sxs-lookup"><span data-stu-id="cb188-933">6</span></span>

<span data-ttu-id="cb188-934">7</span><span class="sxs-lookup"><span data-stu-id="cb188-934">7</span></span>

<span data-ttu-id="cb188-935">8</span><span class="sxs-lookup"><span data-stu-id="cb188-935">8</span></span>

<span data-ttu-id="cb188-936">9</span><span class="sxs-lookup"><span data-stu-id="cb188-936">9</span></span>

<span data-ttu-id="cb188-937">3</span><span class="sxs-lookup"><span data-stu-id="cb188-937">3</span></span><br/> <span data-ttu-id="cb188-938">0</span><span class="sxs-lookup"><span data-stu-id="cb188-938">0</span></span><br/>

<span data-ttu-id="cb188-939">1</span><span class="sxs-lookup"><span data-stu-id="cb188-939">1</span></span>

<span data-ttu-id="cb188-940">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-940">\_Property (variable)</span></span>

<span data-ttu-id="cb188-941">...</span><span class="sxs-lookup"><span data-stu-id="cb188-941">...</span></span>

<span data-ttu-id="cb188-942">Padding1 (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-942">Padding1 (variable)</span></span>

<span data-ttu-id="cb188-943">Cc</span><span class="sxs-lookup"><span data-stu-id="cb188-943">Cc</span></span>

<span data-ttu-id="cb188-944">\_pwcsPhrase (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="cb188-945">...</span><span class="sxs-lookup"><span data-stu-id="cb188-945">...</span></span>

<span data-ttu-id="cb188-946">Padding2 (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-946">Padding2 (variable)</span></span>

<span data-ttu-id="cb188-947">lcid</span><span class="sxs-lookup"><span data-stu-id="cb188-947">lcid</span></span>

<span data-ttu-id="cb188-948">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="cb188-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="cb188-949">**\_ Property:** struttura CFullPropSpec, come specificato nella Sezione 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="cb188-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="cb188-950">Questo campo indica la proprietà su cui eseguire un'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="cb188-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="cb188-951">**Padding1:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cb188-952">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cb188-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cb188-953">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cb188-954">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-955">**Cc:** intero senza segno a 32 bit che specifica il numero di caratteri nel \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="cb188-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="cb188-956">**\_ pwcsPhrase:** stringa Unicode non con terminazione Null che rappresenta la parola o la frase di cui trovare la corrispondenza per la proprietà .</span><span class="sxs-lookup"><span data-stu-id="cb188-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="cb188-957">Questo campo NON DEVE essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="cb188-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="cb188-958">Il campo Cc contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="cb188-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="cb188-959">**Padding2:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cb188-960">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cb188-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cb188-961">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cb188-962">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-963">**Lcid:** intero senza segno a 32 bit che indica le impostazioni locali di \_ pwcsPhrase, come specificato \[ nell'appendice A MS-GPSI. \]</span><span class="sxs-lookup"><span data-stu-id="cb188-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="cb188-964">**\_ ulGenerateMethod:** intero senza segno a 32 bit che specifica il metodo da usare per la generazione di forme di parole alternative</span><span class="sxs-lookup"><span data-stu-id="cb188-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="cb188-965">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-965">Value</span></span>                                                       | <span data-ttu-id="cb188-966">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-967">GENERARE \_ IL METODO \_ ESATTO</span><span class="sxs-lookup"><span data-stu-id="cb188-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="cb188-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-968">0x00000000</span></span><br/>    | <span data-ttu-id="cb188-969">Corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="cb188-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cb188-970">GENERARE IL \_ PREFISSO DEL \_ METODO</span><span class="sxs-lookup"><span data-stu-id="cb188-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="cb188-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-971">0x00000001</span></span> <br/>  | <span data-ttu-id="cb188-972">Corrispondenza del prefisso.</span><span class="sxs-lookup"><span data-stu-id="cb188-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cb188-973">GENERATE \_ METHOD \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="cb188-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="cb188-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-974">0x00000002</span></span><br/> | <span data-ttu-id="cb188-975">Corrisponde alle flesshe di una parola.</span><span class="sxs-lookup"><span data-stu-id="cb188-975">Matches inflections of a word.</span></span> <span data-ttu-id="cb188-976">Un'inflessione di una parola è una variante della parola radice nella stessa parte del parlato che è stata modificata in base alle regole linguistiche di una determinata lingua.</span><span class="sxs-lookup"><span data-stu-id="cb188-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="cb188-977">Ad esempio, le flesshe del verbo "swim" in inglese includono "swim", "swims", "swims", "swim" e "swam".</span><span class="sxs-lookup"><span data-stu-id="cb188-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="cb188-978">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="cb188-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="cb188-979">La struttura CKey contiene un valore di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="cb188-980">0</span><span class="sxs-lookup"><span data-stu-id="cb188-980">0</span></span>

<span data-ttu-id="cb188-981">1</span><span class="sxs-lookup"><span data-stu-id="cb188-981">1</span></span>

<span data-ttu-id="cb188-982">2</span><span class="sxs-lookup"><span data-stu-id="cb188-982">2</span></span>

<span data-ttu-id="cb188-983">3</span><span class="sxs-lookup"><span data-stu-id="cb188-983">3</span></span>

<span data-ttu-id="cb188-984">4</span><span class="sxs-lookup"><span data-stu-id="cb188-984">4</span></span>

<span data-ttu-id="cb188-985">5</span><span class="sxs-lookup"><span data-stu-id="cb188-985">5</span></span>

<span data-ttu-id="cb188-986">6</span><span class="sxs-lookup"><span data-stu-id="cb188-986">6</span></span>

<span data-ttu-id="cb188-987">7</span><span class="sxs-lookup"><span data-stu-id="cb188-987">7</span></span>

<span data-ttu-id="cb188-988">8</span><span class="sxs-lookup"><span data-stu-id="cb188-988">8</span></span>

<span data-ttu-id="cb188-989">9</span><span class="sxs-lookup"><span data-stu-id="cb188-989">9</span></span>

<span data-ttu-id="cb188-990">1</span><span class="sxs-lookup"><span data-stu-id="cb188-990">1</span></span><br/> <span data-ttu-id="cb188-991">0</span><span class="sxs-lookup"><span data-stu-id="cb188-991">0</span></span><br/>

<span data-ttu-id="cb188-992">1</span><span class="sxs-lookup"><span data-stu-id="cb188-992">1</span></span>

<span data-ttu-id="cb188-993">2</span><span class="sxs-lookup"><span data-stu-id="cb188-993">2</span></span>

<span data-ttu-id="cb188-994">3</span><span class="sxs-lookup"><span data-stu-id="cb188-994">3</span></span>

<span data-ttu-id="cb188-995">4</span><span class="sxs-lookup"><span data-stu-id="cb188-995">4</span></span>

<span data-ttu-id="cb188-996">5</span><span class="sxs-lookup"><span data-stu-id="cb188-996">5</span></span>

<span data-ttu-id="cb188-997">6</span><span class="sxs-lookup"><span data-stu-id="cb188-997">6</span></span>

<span data-ttu-id="cb188-998">7</span><span class="sxs-lookup"><span data-stu-id="cb188-998">7</span></span>

<span data-ttu-id="cb188-999">8</span><span class="sxs-lookup"><span data-stu-id="cb188-999">8</span></span>

<span data-ttu-id="cb188-1000">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1000">9</span></span>

<span data-ttu-id="cb188-1001">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1001">2</span></span><br/> <span data-ttu-id="cb188-1002">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1002">0</span></span><br/>

<span data-ttu-id="cb188-1003">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1003">1</span></span>

<span data-ttu-id="cb188-1004">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1004">2</span></span>

<span data-ttu-id="cb188-1005">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1005">3</span></span>

<span data-ttu-id="cb188-1006">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1006">4</span></span>

<span data-ttu-id="cb188-1007">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1007">5</span></span>

<span data-ttu-id="cb188-1008">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1008">6</span></span>

<span data-ttu-id="cb188-1009">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1009">7</span></span>

<span data-ttu-id="cb188-1010">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1010">8</span></span>

<span data-ttu-id="cb188-1011">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1011">9</span></span>

<span data-ttu-id="cb188-1012">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1012">3</span></span><br/> <span data-ttu-id="cb188-1013">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1013">0</span></span><br/>

<span data-ttu-id="cb188-1014">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1014">1</span></span>

<span data-ttu-id="cb188-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="cb188-1015">PROPID</span></span>

<span data-ttu-id="cb188-1016">Cb</span><span class="sxs-lookup"><span data-stu-id="cb188-1016">Cb</span></span>

<span data-ttu-id="cb188-1017">buf (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1017">buf (variable)</span></span>



 

<span data-ttu-id="cb188-1018">**PROPID:** intero senza segno a 32 bit che rappresenta l'ID proprietà come descritto nella sezione 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="cb188-1019">I valori noti sono:</span><span class="sxs-lookup"><span data-stu-id="cb188-1019">Well-known values are:</span></span>



| <span data-ttu-id="cb188-1020">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1020">Value</span></span>      | <span data-ttu-id="cb188-1021">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="cb188-1022">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="cb188-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="cb188-1023">Rappresenta un ID di proprietà non valido e NON DEVE essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cb188-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="cb188-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="cb188-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="cb188-1025">Rappresenta un ID di proprietà non valido e NON DEVE essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cb188-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="cb188-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-1026">0x00000000</span></span> | <span data-ttu-id="cb188-1027">Rappresenta qualsiasi ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="cb188-1028">**Cb:** intero senza segno a 32 bit contenente la lunghezza di buf, in byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="cb188-1029">**buf:** sequenza di byte che rappresenta il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="cb188-1030">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="cb188-1031">La struttura CInternalPropertyRestriction contiene un valore di proprietà da associare a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="cb188-1032">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1032">0</span></span>

<span data-ttu-id="cb188-1033">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1033">1</span></span>

<span data-ttu-id="cb188-1034">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1034">2</span></span>

<span data-ttu-id="cb188-1035">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1035">3</span></span>

<span data-ttu-id="cb188-1036">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1036">4</span></span>

<span data-ttu-id="cb188-1037">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1037">5</span></span>

<span data-ttu-id="cb188-1038">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1038">6</span></span>

<span data-ttu-id="cb188-1039">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1039">7</span></span>

<span data-ttu-id="cb188-1040">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1040">8</span></span>

<span data-ttu-id="cb188-1041">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1041">9</span></span>

<span data-ttu-id="cb188-1042">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1042">1</span></span><br/> <span data-ttu-id="cb188-1043">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1043">0</span></span><br/>

<span data-ttu-id="cb188-1044">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1044">1</span></span>

<span data-ttu-id="cb188-1045">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1045">2</span></span>

<span data-ttu-id="cb188-1046">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1046">3</span></span>

<span data-ttu-id="cb188-1047">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1047">4</span></span>

<span data-ttu-id="cb188-1048">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1048">5</span></span>

<span data-ttu-id="cb188-1049">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1049">6</span></span>

<span data-ttu-id="cb188-1050">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1050">7</span></span>

<span data-ttu-id="cb188-1051">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1051">8</span></span>

<span data-ttu-id="cb188-1052">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1052">9</span></span>

<span data-ttu-id="cb188-1053">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1053">2</span></span><br/> <span data-ttu-id="cb188-1054">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1054">0</span></span><br/>

<span data-ttu-id="cb188-1055">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1055">1</span></span>

<span data-ttu-id="cb188-1056">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1056">2</span></span>

<span data-ttu-id="cb188-1057">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1057">3</span></span>

<span data-ttu-id="cb188-1058">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1058">4</span></span>

<span data-ttu-id="cb188-1059">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1059">5</span></span>

<span data-ttu-id="cb188-1060">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1060">6</span></span>

<span data-ttu-id="cb188-1061">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1061">7</span></span>

<span data-ttu-id="cb188-1062">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1062">8</span></span>

<span data-ttu-id="cb188-1063">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1063">9</span></span>

<span data-ttu-id="cb188-1064">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1064">3</span></span><br/> <span data-ttu-id="cb188-1065">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1065">0</span></span><br/>

<span data-ttu-id="cb188-1066">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1066">1</span></span>

<span data-ttu-id="cb188-1067">\_lop</span><span class="sxs-lookup"><span data-stu-id="cb188-1067">\_relop</span></span>

<span data-ttu-id="cb188-1068">\_pid</span><span class="sxs-lookup"><span data-stu-id="cb188-1068">\_pid</span></span>

<span data-ttu-id="cb188-1069">\_prval (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1069">\_prval (variable)</span></span>

<span data-ttu-id="cb188-1070">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="cb188-1070">restrictionPresent</span></span>

<span data-ttu-id="cb188-1071">nextRestriction (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="cb188-1072">**\_ relop:** intero a 32 bit che specifica la relazione da eseguire sulla proprietà .</span><span class="sxs-lookup"><span data-stu-id="cb188-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="cb188-1073">DEVE essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="cb188-1074">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1074">Value</span></span>                 | <span data-ttu-id="cb188-1075">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1076">0x00000000 PRLT</span><span class="sxs-lookup"><span data-stu-id="cb188-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="cb188-1077">Confronto minore di.</span><span class="sxs-lookup"><span data-stu-id="cb188-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="cb188-1078">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="cb188-1079">Confronto minore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="cb188-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="cb188-1080">0x00000002 PRGT</span><span class="sxs-lookup"><span data-stu-id="cb188-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="cb188-1081">Confronto maggiore di.</span><span class="sxs-lookup"><span data-stu-id="cb188-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="cb188-1082">Richiesta pull 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="cb188-1083">Confronto maggiore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="cb188-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="cb188-1084">Preq 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="cb188-1085">Confronto di uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="cb188-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="cb188-1086">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="cb188-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="cb188-1087">Confronto diverso da.</span><span class="sxs-lookup"><span data-stu-id="cb188-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="cb188-1088">Richiesta pull 0x00000006</span><span class="sxs-lookup"><span data-stu-id="cb188-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="cb188-1089">Confronto di espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="cb188-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="cb188-1090">PrAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb188-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="cb188-1091">AND bit per bit che restituisce l'operando destro.</span><span class="sxs-lookup"><span data-stu-id="cb188-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="cb188-1092">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb188-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="cb188-1093">AND bit per bit che restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cb188-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="cb188-1094">PRTutti 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cb188-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="cb188-1095">L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="cb188-1096">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cb188-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="cb188-1097">L'operazione deve essere eseguita su una colonna di un set di righe ed è true se l'operazione è true per qualsiasi riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="cb188-1098">**\_ pid:** intero senza segno a 32 bit che rappresenta l'ID proprietà (vedere PROPID nella sezione 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="cb188-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="cb188-1099">**\_ prval:** CBaseStorageVariant contenente il valore da correlare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="cb188-1100">**restrictionPresent:** valore byte che indica se è presente il campo nextRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="cb188-1101">DEVE essere impostato su 0x00 o 0x01.</span><span class="sxs-lookup"><span data-stu-id="cb188-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="cb188-1102">Se impostato su 0x01, restrictionPresent indica che è presente il campo nextRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="cb188-1103">Se impostato su 0x00, restrictionPresent indica che il campo nextRestriction non è presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="cb188-1104">**nextRestriction:** struttura CRestriction, come specificato nella sezione 2.2.1.16, che specifica un'ulteriore restrizione.</span><span class="sxs-lookup"><span data-stu-id="cb188-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="cb188-1105">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="cb188-1106">La struttura CNatLanguageRestriction contiene una corrispondenza di **query in linguaggio** naturale per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="cb188-1107">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1107">0</span></span>

<span data-ttu-id="cb188-1108">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1108">1</span></span>

<span data-ttu-id="cb188-1109">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1109">2</span></span>

<span data-ttu-id="cb188-1110">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1110">3</span></span>

<span data-ttu-id="cb188-1111">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1111">4</span></span>

<span data-ttu-id="cb188-1112">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1112">5</span></span>

<span data-ttu-id="cb188-1113">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1113">6</span></span>

<span data-ttu-id="cb188-1114">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1114">7</span></span>

<span data-ttu-id="cb188-1115">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1115">8</span></span>

<span data-ttu-id="cb188-1116">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1116">9</span></span>

<span data-ttu-id="cb188-1117">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1117">1</span></span><br/> <span data-ttu-id="cb188-1118">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1118">0</span></span><br/>

<span data-ttu-id="cb188-1119">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1119">1</span></span>

<span data-ttu-id="cb188-1120">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1120">2</span></span>

<span data-ttu-id="cb188-1121">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1121">3</span></span>

<span data-ttu-id="cb188-1122">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1122">4</span></span>

<span data-ttu-id="cb188-1123">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1123">5</span></span>

<span data-ttu-id="cb188-1124">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1124">6</span></span>

<span data-ttu-id="cb188-1125">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1125">7</span></span>

<span data-ttu-id="cb188-1126">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1126">8</span></span>

<span data-ttu-id="cb188-1127">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1127">9</span></span>

<span data-ttu-id="cb188-1128">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1128">2</span></span><br/> <span data-ttu-id="cb188-1129">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1129">0</span></span><br/>

<span data-ttu-id="cb188-1130">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1130">1</span></span>

<span data-ttu-id="cb188-1131">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1131">2</span></span>

<span data-ttu-id="cb188-1132">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1132">3</span></span>

<span data-ttu-id="cb188-1133">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1133">4</span></span>

<span data-ttu-id="cb188-1134">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1134">5</span></span>

<span data-ttu-id="cb188-1135">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1135">6</span></span>

<span data-ttu-id="cb188-1136">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1136">7</span></span>

<span data-ttu-id="cb188-1137">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1137">8</span></span>

<span data-ttu-id="cb188-1138">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1138">9</span></span>

<span data-ttu-id="cb188-1139">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1139">3</span></span><br/> <span data-ttu-id="cb188-1140">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1140">0</span></span><br/>

<span data-ttu-id="cb188-1141">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1141">1</span></span>

<span data-ttu-id="cb188-1142">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1142">\_Property (variable)</span></span>

<span data-ttu-id="cb188-1143">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1143">...</span></span>

<span data-ttu-id="cb188-1144">\_padding \_ cc (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="cb188-1145">Cc</span><span class="sxs-lookup"><span data-stu-id="cb188-1145">Cc</span></span>

<span data-ttu-id="cb188-1146">\_pwcsPhrase (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="cb188-1147">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1147">...</span></span>

<span data-ttu-id="cb188-1148">\_padding \_ lcid (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="cb188-1149">LCID</span><span class="sxs-lookup"><span data-stu-id="cb188-1149">Lcid</span></span>



 

<span data-ttu-id="cb188-1150">**\_ Property:** struttura CFullPropSpec, come specificato nella Sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="cb188-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="cb188-1151">Questo campo indica la proprietà su cui eseguire l'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="cb188-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="cb188-1152">**\_ padding \_ cc:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cb188-1153">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cb188-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cb188-1154">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cb188-1155">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-1156">**Cc:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cb188-1157">Numero di caratteri nel \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="cb188-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="cb188-1158">**\_ pwcsPhrase:** stringa Unicode non con terminazione Null che rappresenta la parola o la frase di cui trovare la corrispondenza per la proprietà .</span><span class="sxs-lookup"><span data-stu-id="cb188-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="cb188-1159">NON DEVE essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="cb188-1159">MUST NOT be empty.</span></span> <span data-ttu-id="cb188-1160">Il campo Cc contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="cb188-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="cb188-1161">**\_ padding \_ lcid:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cb188-1162">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cb188-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cb188-1163">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cb188-1164">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-1165">**Lcid:** intero senza segno a 32 bit che indica le impostazioni locali di \_ pwcsPhrase, come specificato \[ nell'appendice A MS-GPSI. \]</span><span class="sxs-lookup"><span data-stu-id="cb188-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="cb188-1166">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="cb188-1167">La struttura CNodeRestriction contiene una matrice di **nodi** dell'albero dei comandi che specificano le restrizioni per la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="cb188-1168">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1168">0</span></span>

<span data-ttu-id="cb188-1169">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1169">1</span></span>

<span data-ttu-id="cb188-1170">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1170">2</span></span>

<span data-ttu-id="cb188-1171">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1171">3</span></span>

<span data-ttu-id="cb188-1172">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1172">4</span></span>

<span data-ttu-id="cb188-1173">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1173">5</span></span>

<span data-ttu-id="cb188-1174">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1174">6</span></span>

<span data-ttu-id="cb188-1175">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1175">7</span></span>

<span data-ttu-id="cb188-1176">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1176">8</span></span>

<span data-ttu-id="cb188-1177">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1177">9</span></span>

<span data-ttu-id="cb188-1178">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1178">1</span></span><br/> <span data-ttu-id="cb188-1179">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1179">0</span></span><br/>

<span data-ttu-id="cb188-1180">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1180">1</span></span>

<span data-ttu-id="cb188-1181">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1181">2</span></span>

<span data-ttu-id="cb188-1182">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1182">3</span></span>

<span data-ttu-id="cb188-1183">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1183">4</span></span>

<span data-ttu-id="cb188-1184">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1184">5</span></span>

<span data-ttu-id="cb188-1185">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1185">6</span></span>

<span data-ttu-id="cb188-1186">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1186">7</span></span>

<span data-ttu-id="cb188-1187">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1187">8</span></span>

<span data-ttu-id="cb188-1188">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1188">9</span></span>

<span data-ttu-id="cb188-1189">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1189">2</span></span><br/> <span data-ttu-id="cb188-1190">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1190">0</span></span><br/>

<span data-ttu-id="cb188-1191">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1191">1</span></span>

<span data-ttu-id="cb188-1192">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1192">2</span></span>

<span data-ttu-id="cb188-1193">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1193">3</span></span>

<span data-ttu-id="cb188-1194">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1194">4</span></span>

<span data-ttu-id="cb188-1195">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1195">5</span></span>

<span data-ttu-id="cb188-1196">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1196">6</span></span>

<span data-ttu-id="cb188-1197">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1197">7</span></span>

<span data-ttu-id="cb188-1198">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1198">8</span></span>

<span data-ttu-id="cb188-1199">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1199">9</span></span>

<span data-ttu-id="cb188-1200">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1200">3</span></span><br/> <span data-ttu-id="cb188-1201">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1201">0</span></span><br/>

<span data-ttu-id="cb188-1202">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1202">1</span></span>

<span data-ttu-id="cb188-1203">\_cNode</span><span class="sxs-lookup"><span data-stu-id="cb188-1203">\_cNode</span></span>

<span data-ttu-id="cb188-1204">\_paNode (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="cb188-1205">**\_ cNode:** intero senza segno a 32 bit che specifica il numero di strutture CRestriction contenute nel \_ campo paNode.</span><span class="sxs-lookup"><span data-stu-id="cb188-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="cb188-1206">**\_ paNode:** matrice di strutture CRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="cb188-1207">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice.</span><span class="sxs-lookup"><span data-stu-id="cb188-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cb188-1208">Se sono presenti byte di spaziatura interna, il valore che contengono è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cb188-1209">Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="cb188-1210">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="cb188-1211">La struttura COccRestriction contiene la posizione di una parola in una frase.</span><span class="sxs-lookup"><span data-stu-id="cb188-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="cb188-1212">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1212">0</span></span>

<span data-ttu-id="cb188-1213">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1213">1</span></span>

<span data-ttu-id="cb188-1214">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1214">2</span></span>

<span data-ttu-id="cb188-1215">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1215">3</span></span>

<span data-ttu-id="cb188-1216">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1216">4</span></span>

<span data-ttu-id="cb188-1217">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1217">5</span></span>

<span data-ttu-id="cb188-1218">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1218">6</span></span>

<span data-ttu-id="cb188-1219">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1219">7</span></span>

<span data-ttu-id="cb188-1220">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1220">8</span></span>

<span data-ttu-id="cb188-1221">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1221">9</span></span>

<span data-ttu-id="cb188-1222">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1222">1</span></span><br/> <span data-ttu-id="cb188-1223">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1223">0</span></span><br/>

<span data-ttu-id="cb188-1224">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1224">1</span></span>

<span data-ttu-id="cb188-1225">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1225">2</span></span>

<span data-ttu-id="cb188-1226">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1226">3</span></span>

<span data-ttu-id="cb188-1227">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1227">4</span></span>

<span data-ttu-id="cb188-1228">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1228">5</span></span>

<span data-ttu-id="cb188-1229">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1229">6</span></span>

<span data-ttu-id="cb188-1230">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1230">7</span></span>

<span data-ttu-id="cb188-1231">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1231">8</span></span>

<span data-ttu-id="cb188-1232">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1232">9</span></span>

<span data-ttu-id="cb188-1233">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1233">2</span></span><br/> <span data-ttu-id="cb188-1234">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1234">0</span></span><br/>

<span data-ttu-id="cb188-1235">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1235">1</span></span>

<span data-ttu-id="cb188-1236">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1236">2</span></span>

<span data-ttu-id="cb188-1237">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1237">3</span></span>

<span data-ttu-id="cb188-1238">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1238">4</span></span>

<span data-ttu-id="cb188-1239">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1239">5</span></span>

<span data-ttu-id="cb188-1240">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1240">6</span></span>

<span data-ttu-id="cb188-1241">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1241">7</span></span>

<span data-ttu-id="cb188-1242">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1242">8</span></span>

<span data-ttu-id="cb188-1243">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1243">9</span></span>

<span data-ttu-id="cb188-1244">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1244">3</span></span><br/> <span data-ttu-id="cb188-1245">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1245">0</span></span><br/>

<span data-ttu-id="cb188-1246">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1246">1</span></span>

<span data-ttu-id="cb188-1247">\_Occ</span><span class="sxs-lookup"><span data-stu-id="cb188-1247">\_occ</span></span>

<span data-ttu-id="cb188-1248">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="cb188-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="cb188-1249">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="cb188-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="cb188-1250">**\_ occ:** intero senza segno a 32 bit che specifica l'offset della parola in una stringa di query, in unità di parole.</span><span class="sxs-lookup"><span data-stu-id="cb188-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="cb188-1251">Una parola, usata in questa specifica, è un'unità di lingua in tutte le impostazioni locali che hanno significato.</span><span class="sxs-lookup"><span data-stu-id="cb188-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="cb188-1252">**\_ cPrevNoiseWords:** intero senza segno a 32  bit contenente il numero di parole non erre presenti tra questa parola e la parola precedente nella frase.</span><span class="sxs-lookup"><span data-stu-id="cb188-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="cb188-1253">**\_ cNextNoiseWords:** intero senza segno a 32 bit contenente il numero di parole non erre presenti tra questa parola e la parola successiva nella frase.</span><span class="sxs-lookup"><span data-stu-id="cb188-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="cb188-1254">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="cb188-1255">La struttura CPropertyRestriction contiene un valore di proprietà da associare a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="cb188-1256">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1256">0</span></span>

<span data-ttu-id="cb188-1257">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1257">1</span></span>

<span data-ttu-id="cb188-1258">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1258">2</span></span>

<span data-ttu-id="cb188-1259">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1259">3</span></span>

<span data-ttu-id="cb188-1260">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1260">4</span></span>

<span data-ttu-id="cb188-1261">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1261">5</span></span>

<span data-ttu-id="cb188-1262">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1262">6</span></span>

<span data-ttu-id="cb188-1263">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1263">7</span></span>

<span data-ttu-id="cb188-1264">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1264">8</span></span>

<span data-ttu-id="cb188-1265">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1265">9</span></span>

<span data-ttu-id="cb188-1266">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1266">1</span></span><br/> <span data-ttu-id="cb188-1267">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1267">0</span></span><br/>

<span data-ttu-id="cb188-1268">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1268">1</span></span>

<span data-ttu-id="cb188-1269">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1269">2</span></span>

<span data-ttu-id="cb188-1270">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1270">3</span></span>

<span data-ttu-id="cb188-1271">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1271">4</span></span>

<span data-ttu-id="cb188-1272">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1272">5</span></span>

<span data-ttu-id="cb188-1273">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1273">6</span></span>

<span data-ttu-id="cb188-1274">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1274">7</span></span>

<span data-ttu-id="cb188-1275">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1275">8</span></span>

<span data-ttu-id="cb188-1276">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1276">9</span></span>

<span data-ttu-id="cb188-1277">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1277">2</span></span><br/> <span data-ttu-id="cb188-1278">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1278">0</span></span><br/>

<span data-ttu-id="cb188-1279">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1279">1</span></span>

<span data-ttu-id="cb188-1280">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1280">2</span></span>

<span data-ttu-id="cb188-1281">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1281">3</span></span>

<span data-ttu-id="cb188-1282">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1282">4</span></span>

<span data-ttu-id="cb188-1283">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1283">5</span></span>

<span data-ttu-id="cb188-1284">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1284">6</span></span>

<span data-ttu-id="cb188-1285">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1285">7</span></span>

<span data-ttu-id="cb188-1286">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1286">8</span></span>

<span data-ttu-id="cb188-1287">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1287">9</span></span>

<span data-ttu-id="cb188-1288">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1288">3</span></span><br/> <span data-ttu-id="cb188-1289">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1289">0</span></span><br/>

<span data-ttu-id="cb188-1290">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1290">1</span></span>

<span data-ttu-id="cb188-1291">\_lop</span><span class="sxs-lookup"><span data-stu-id="cb188-1291">\_relop</span></span>

<span data-ttu-id="cb188-1292">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1292">\_Property (variable)</span></span>

<span data-ttu-id="cb188-1293">\_prval (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="cb188-1294">**\_ relop:** intero senza segno a 32 bit che specifica la relazione da eseguire sulla proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="cb188-1295">DEVE essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="cb188-1296">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1296">Value</span></span>                 | <span data-ttu-id="cb188-1297">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1298">0x00000000 PRLT</span><span class="sxs-lookup"><span data-stu-id="cb188-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="cb188-1299">Confronto minore di.</span><span class="sxs-lookup"><span data-stu-id="cb188-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="cb188-1300">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="cb188-1301">Confronto minore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="cb188-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="cb188-1302">0x00000002 PRGT</span><span class="sxs-lookup"><span data-stu-id="cb188-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="cb188-1303">Confronto maggiore di.</span><span class="sxs-lookup"><span data-stu-id="cb188-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="cb188-1304">Richiesta pull 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="cb188-1305">Confronto maggiore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="cb188-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="cb188-1306">Preq 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="cb188-1307">Confronto di uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="cb188-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="cb188-1308">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="cb188-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="cb188-1309">Confronto diverso da.</span><span class="sxs-lookup"><span data-stu-id="cb188-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="cb188-1310">Richiesta pull 0x00000006</span><span class="sxs-lookup"><span data-stu-id="cb188-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="cb188-1311">Confronto di espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="cb188-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="cb188-1312">PrAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb188-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="cb188-1313">AND bit per bit che restituisce l'operando destro.</span><span class="sxs-lookup"><span data-stu-id="cb188-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="cb188-1314">PrSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb188-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="cb188-1315">AND bit per bit che restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cb188-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="cb188-1316">PrAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cb188-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="cb188-1317">L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="cb188-1318">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cb188-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="cb188-1319">L'operazione deve essere eseguita su una colonna di un set di righe ed è true se l'operazione è true per qualsiasi riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="cb188-1320">**\_ Proprietà:** struttura CFullPropSpec, come specificato nella Sezione 2.2.1.2, che indica la proprietà su cui eseguire un'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="cb188-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="cb188-1321">**\_ prval:** struttura CBaseStorageVariant, come specificato nella Sezione 2.2.1.1, contenente il valore da correlare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="cb188-1322">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="cb188-1323">La struttura CRangeRestriction contiene una restrizione per un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="cb188-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="cb188-1324">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1324">0</span></span>

<span data-ttu-id="cb188-1325">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1325">1</span></span>

<span data-ttu-id="cb188-1326">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1326">2</span></span>

<span data-ttu-id="cb188-1327">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1327">3</span></span>

<span data-ttu-id="cb188-1328">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1328">4</span></span>

<span data-ttu-id="cb188-1329">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1329">5</span></span>

<span data-ttu-id="cb188-1330">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1330">6</span></span>

<span data-ttu-id="cb188-1331">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1331">7</span></span>

<span data-ttu-id="cb188-1332">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1332">8</span></span>

<span data-ttu-id="cb188-1333">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1333">9</span></span>

<span data-ttu-id="cb188-1334">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1334">1</span></span><br/> <span data-ttu-id="cb188-1335">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1335">0</span></span><br/>

<span data-ttu-id="cb188-1336">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1336">1</span></span>

<span data-ttu-id="cb188-1337">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1337">2</span></span>

<span data-ttu-id="cb188-1338">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1338">3</span></span>

<span data-ttu-id="cb188-1339">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1339">4</span></span>

<span data-ttu-id="cb188-1340">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1340">5</span></span>

<span data-ttu-id="cb188-1341">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1341">6</span></span>

<span data-ttu-id="cb188-1342">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1342">7</span></span>

<span data-ttu-id="cb188-1343">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1343">8</span></span>

<span data-ttu-id="cb188-1344">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1344">9</span></span>

<span data-ttu-id="cb188-1345">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1345">2</span></span><br/> <span data-ttu-id="cb188-1346">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1346">0</span></span><br/>

<span data-ttu-id="cb188-1347">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1347">1</span></span>

<span data-ttu-id="cb188-1348">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1348">2</span></span>

<span data-ttu-id="cb188-1349">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1349">3</span></span>

<span data-ttu-id="cb188-1350">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1350">4</span></span>

<span data-ttu-id="cb188-1351">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1351">5</span></span>

<span data-ttu-id="cb188-1352">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1352">6</span></span>

<span data-ttu-id="cb188-1353">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1353">7</span></span>

<span data-ttu-id="cb188-1354">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1354">8</span></span>

<span data-ttu-id="cb188-1355">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1355">9</span></span>

<span data-ttu-id="cb188-1356">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1356">3</span></span><br/> <span data-ttu-id="cb188-1357">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1357">0</span></span><br/>

<span data-ttu-id="cb188-1358">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1358">1</span></span>

<span data-ttu-id="cb188-1359">\_keyStart (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="cb188-1360">\_keyEnd (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="cb188-1361">**\_ keyStart:** struttura CKey, come specificato nella sezione 2.2.1.4, contenente l'inizio dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="cb188-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="cb188-1362">**\_ keyEnd:** struttura CKey contenente la fine dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="cb188-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="cb188-1363">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="cb188-1364">La struttura CScopeRestriction contiene una restrizione sui file in cui eseguire la ricerca</span><span class="sxs-lookup"><span data-stu-id="cb188-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="cb188-1365">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1365">0</span></span>

<span data-ttu-id="cb188-1366">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1366">1</span></span>

<span data-ttu-id="cb188-1367">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1367">2</span></span>

<span data-ttu-id="cb188-1368">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1368">3</span></span>

<span data-ttu-id="cb188-1369">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1369">4</span></span>

<span data-ttu-id="cb188-1370">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1370">5</span></span>

<span data-ttu-id="cb188-1371">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1371">6</span></span>

<span data-ttu-id="cb188-1372">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1372">7</span></span>

<span data-ttu-id="cb188-1373">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1373">8</span></span>

<span data-ttu-id="cb188-1374">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1374">9</span></span>

<span data-ttu-id="cb188-1375">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1375">1</span></span><br/> <span data-ttu-id="cb188-1376">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1376">0</span></span><br/>

<span data-ttu-id="cb188-1377">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1377">1</span></span>

<span data-ttu-id="cb188-1378">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1378">2</span></span>

<span data-ttu-id="cb188-1379">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1379">3</span></span>

<span data-ttu-id="cb188-1380">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1380">4</span></span>

<span data-ttu-id="cb188-1381">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1381">5</span></span>

<span data-ttu-id="cb188-1382">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1382">6</span></span>

<span data-ttu-id="cb188-1383">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1383">7</span></span>

<span data-ttu-id="cb188-1384">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1384">8</span></span>

<span data-ttu-id="cb188-1385">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1385">9</span></span>

<span data-ttu-id="cb188-1386">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1386">2</span></span><br/> <span data-ttu-id="cb188-1387">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1387">0</span></span><br/>

<span data-ttu-id="cb188-1388">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1388">1</span></span>

<span data-ttu-id="cb188-1389">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1389">2</span></span>

<span data-ttu-id="cb188-1390">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1390">3</span></span>

<span data-ttu-id="cb188-1391">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1391">4</span></span>

<span data-ttu-id="cb188-1392">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1392">5</span></span>

<span data-ttu-id="cb188-1393">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1393">6</span></span>

<span data-ttu-id="cb188-1394">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1394">7</span></span>

<span data-ttu-id="cb188-1395">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1395">8</span></span>

<span data-ttu-id="cb188-1396">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1396">9</span></span>

<span data-ttu-id="cb188-1397">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1397">3</span></span><br/> <span data-ttu-id="cb188-1398">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1398">0</span></span><br/>

<span data-ttu-id="cb188-1399">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1399">1</span></span>

<span data-ttu-id="cb188-1400">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="cb188-1400">CcLowerPath</span></span>

<span data-ttu-id="cb188-1401">\_lowerPath (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="cb188-1402">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1402">...</span></span>

<span data-ttu-id="cb188-1403">\_padding (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1403">\_padding ( variable)</span></span>

<span data-ttu-id="cb188-1404">\_Lunghezza</span><span class="sxs-lookup"><span data-stu-id="cb188-1404">\_length</span></span>

<span data-ttu-id="cb188-1405">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="cb188-1405">\_fRecursive</span></span>

<span data-ttu-id="cb188-1406">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="cb188-1406">\_fVirtual</span></span>



 

<span data-ttu-id="cb188-1407">**CcLowerPath:** intero senza segno a 32 bit contenente il numero di caratteri Unicode nel \_ campo lowerPath.</span><span class="sxs-lookup"><span data-stu-id="cb188-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="cb188-1408">**\_ lowerPath:** stringa Unicode non con terminazione Null che rappresenta il **percorso** a cui la query deve essere limitata.</span><span class="sxs-lookup"><span data-stu-id="cb188-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="cb188-1409">Il campo CcLowerPath contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="cb188-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="cb188-1410">**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cb188-1411">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cb188-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cb188-1412">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cb188-1413">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-1414">**\_ length:** intero senza segno a 32 bit contenente la lunghezza di \_ lowerPath, in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb188-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="cb188-1415">Deve essere lo stesso valore di CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="cb188-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="cb188-1416">**\_ fRecursive:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cb188-1417">DEVE essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cb188-1418">Se impostato su 0x00000001, il server deve esaminare in modo ricorsivo tutte le sottodirectory del percorso.</span><span class="sxs-lookup"><span data-stu-id="cb188-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="cb188-1419">Se impostato su 0x00000000, il server non esamina le sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="cb188-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="cb188-1420">**\_ fVirtual:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cb188-1421">DEVE essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cb188-1422">Se impostato su 0x00000001, lowerPath è un percorso virtuale (l'Uniform Resource Locator (URL) associato a una directory fisica nel file system) per \_ un sito Web.</span><span class="sxs-lookup"><span data-stu-id="cb188-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="cb188-1423">Se impostato su 0x00000000, \_ lowerPath è un file system percorso.</span><span class="sxs-lookup"><span data-stu-id="cb188-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="cb188-1424">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="cb188-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="cb188-1425">La struttura CSort identifica una colonna da ordinare.</span><span class="sxs-lookup"><span data-stu-id="cb188-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="cb188-1426">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1426">0</span></span>

<span data-ttu-id="cb188-1427">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1427">1</span></span>

<span data-ttu-id="cb188-1428">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1428">2</span></span>

<span data-ttu-id="cb188-1429">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1429">3</span></span>

<span data-ttu-id="cb188-1430">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1430">4</span></span>

<span data-ttu-id="cb188-1431">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1431">5</span></span>

<span data-ttu-id="cb188-1432">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1432">6</span></span>

<span data-ttu-id="cb188-1433">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1433">7</span></span>

<span data-ttu-id="cb188-1434">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1434">8</span></span>

<span data-ttu-id="cb188-1435">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1435">9</span></span>

<span data-ttu-id="cb188-1436">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1436">1</span></span><br/> <span data-ttu-id="cb188-1437">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1437">0</span></span><br/>

<span data-ttu-id="cb188-1438">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1438">1</span></span>

<span data-ttu-id="cb188-1439">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1439">2</span></span>

<span data-ttu-id="cb188-1440">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1440">3</span></span>

<span data-ttu-id="cb188-1441">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1441">4</span></span>

<span data-ttu-id="cb188-1442">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1442">5</span></span>

<span data-ttu-id="cb188-1443">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1443">6</span></span>

<span data-ttu-id="cb188-1444">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1444">7</span></span>

<span data-ttu-id="cb188-1445">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1445">8</span></span>

<span data-ttu-id="cb188-1446">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1446">9</span></span>

<span data-ttu-id="cb188-1447">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1447">2</span></span><br/> <span data-ttu-id="cb188-1448">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1448">0</span></span><br/>

<span data-ttu-id="cb188-1449">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1449">1</span></span>

<span data-ttu-id="cb188-1450">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1450">2</span></span>

<span data-ttu-id="cb188-1451">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1451">3</span></span>

<span data-ttu-id="cb188-1452">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1452">4</span></span>

<span data-ttu-id="cb188-1453">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1453">5</span></span>

<span data-ttu-id="cb188-1454">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1454">6</span></span>

<span data-ttu-id="cb188-1455">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1455">7</span></span>

<span data-ttu-id="cb188-1456">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1456">8</span></span>

<span data-ttu-id="cb188-1457">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1457">9</span></span>

<span data-ttu-id="cb188-1458">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1458">3</span></span><br/> <span data-ttu-id="cb188-1459">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1459">0</span></span><br/>

<span data-ttu-id="cb188-1460">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1460">1</span></span>

<span data-ttu-id="cb188-1461">pidColumn</span><span class="sxs-lookup"><span data-stu-id="cb188-1461">pidColumn</span></span>

<span data-ttu-id="cb188-1462">dwOrder</span><span class="sxs-lookup"><span data-stu-id="cb188-1462">dwOrder</span></span>

<span data-ttu-id="cb188-1463">locale</span><span class="sxs-lookup"><span data-stu-id="cb188-1463">locale</span></span>



 

<span data-ttu-id="cb188-1464">**pidColumn:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cb188-1465">Numero della colonna in base alla quale eseguire l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="cb188-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="cb188-1466">**dwOrder:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cb188-1467">DEVE essere uno dei valori seguenti, specificando come eseguire l'ordinamento in base alla colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="cb188-1468">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1468">Value</span></span>                        | <span data-ttu-id="cb188-1469">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1470">QUERY \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="cb188-1471">Le righe devono essere ordinate in ordine crescente in base ai valori nella colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="cb188-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="cb188-1472">QUERY \_ DESCEND 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="cb188-1473">Le righe devono essere ordinate in ordine decrescente in base ai valori nella colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="cb188-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="cb188-1474">**locale:** intero senza segno a 32 bit che indica le impostazioni locali, come specificato \[ nell'appendice A MS-GPSI, \] della colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="cb188-1475">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="cb188-1476">La struttura CSynRestriction contiene una parola o i relativi sinonimi per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="cb188-1477">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1477">0</span></span>

<span data-ttu-id="cb188-1478">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1478">1</span></span>

<span data-ttu-id="cb188-1479">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1479">2</span></span>

<span data-ttu-id="cb188-1480">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1480">3</span></span>

<span data-ttu-id="cb188-1481">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1481">4</span></span>

<span data-ttu-id="cb188-1482">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1482">5</span></span>

<span data-ttu-id="cb188-1483">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1483">6</span></span>

<span data-ttu-id="cb188-1484">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1484">7</span></span>

<span data-ttu-id="cb188-1485">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1485">8</span></span>

<span data-ttu-id="cb188-1486">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1486">9</span></span>

<span data-ttu-id="cb188-1487">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1487">1</span></span><br/> <span data-ttu-id="cb188-1488">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1488">0</span></span><br/>

<span data-ttu-id="cb188-1489">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1489">1</span></span>

<span data-ttu-id="cb188-1490">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1490">2</span></span>

<span data-ttu-id="cb188-1491">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1491">3</span></span>

<span data-ttu-id="cb188-1492">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1492">4</span></span>

<span data-ttu-id="cb188-1493">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1493">5</span></span>

<span data-ttu-id="cb188-1494">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1494">6</span></span>

<span data-ttu-id="cb188-1495">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1495">7</span></span>

<span data-ttu-id="cb188-1496">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1496">8</span></span>

<span data-ttu-id="cb188-1497">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1497">9</span></span>

<span data-ttu-id="cb188-1498">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1498">2</span></span><br/> <span data-ttu-id="cb188-1499">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1499">0</span></span><br/>

<span data-ttu-id="cb188-1500">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1500">1</span></span>

<span data-ttu-id="cb188-1501">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1501">2</span></span>

<span data-ttu-id="cb188-1502">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1502">3</span></span>

<span data-ttu-id="cb188-1503">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1503">4</span></span>

<span data-ttu-id="cb188-1504">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1504">5</span></span>

<span data-ttu-id="cb188-1505">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1505">6</span></span>

<span data-ttu-id="cb188-1506">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1506">7</span></span>

<span data-ttu-id="cb188-1507">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1507">8</span></span>

<span data-ttu-id="cb188-1508">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1508">9</span></span>

<span data-ttu-id="cb188-1509">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1509">3</span></span><br/> <span data-ttu-id="cb188-1510">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1510">0</span></span><br/>

<span data-ttu-id="cb188-1511">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1511">1</span></span>

<span data-ttu-id="cb188-1512">Restrizione</span><span class="sxs-lookup"><span data-stu-id="cb188-1512">Restriction</span></span>

<span data-ttu-id="cb188-1513">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1513">...</span></span>

<span data-ttu-id="cb188-1514">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1514">...</span></span>

<span data-ttu-id="cb188-1515">cKey</span><span class="sxs-lookup"><span data-stu-id="cb188-1515">cKey</span></span>

<span data-ttu-id="cb188-1516">\_keyArray (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="cb188-1517">\_isRange</span><span class="sxs-lookup"><span data-stu-id="cb188-1517">\_isRange</span></span>



 

<span data-ttu-id="cb188-1518">**Restrizione:** struttura COccRestriction che specifica la posizione della parola.</span><span class="sxs-lookup"><span data-stu-id="cb188-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="cb188-1519">**cKey:** intero senza segno a 32 bit che specifica il numero di elementi nella \_ matrice keyArray.</span><span class="sxs-lookup"><span data-stu-id="cb188-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="cb188-1520">**\_ keyArray:** matrice di strutture CKey che specifica una parola e i relativi sinonimi.</span><span class="sxs-lookup"><span data-stu-id="cb188-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="cb188-1521">**\_ isRange:** se impostato su 0x01, le chiavi sono prefissi per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="cb188-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="cb188-1522">Se impostato su 0x00, le chiavi corrispondono esattamente ai valori.</span><span class="sxs-lookup"><span data-stu-id="cb188-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="cb188-1523">\_isRange NON DEVE essere impostato su altri valori.</span><span class="sxs-lookup"><span data-stu-id="cb188-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="cb188-1524">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="cb188-1525">La struttura CVectorRestriction contiene un'operazione OR ponderata su un nodo della struttura ad albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="cb188-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="cb188-1526">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1526">0</span></span>

<span data-ttu-id="cb188-1527">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1527">1</span></span>

<span data-ttu-id="cb188-1528">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1528">2</span></span>

<span data-ttu-id="cb188-1529">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1529">3</span></span>

<span data-ttu-id="cb188-1530">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1530">4</span></span>

<span data-ttu-id="cb188-1531">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1531">5</span></span>

<span data-ttu-id="cb188-1532">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1532">6</span></span>

<span data-ttu-id="cb188-1533">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1533">7</span></span>

<span data-ttu-id="cb188-1534">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1534">8</span></span>

<span data-ttu-id="cb188-1535">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1535">9</span></span>

<span data-ttu-id="cb188-1536">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1536">1</span></span><br/> <span data-ttu-id="cb188-1537">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1537">0</span></span><br/>

<span data-ttu-id="cb188-1538">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1538">1</span></span>

<span data-ttu-id="cb188-1539">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1539">2</span></span>

<span data-ttu-id="cb188-1540">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1540">3</span></span>

<span data-ttu-id="cb188-1541">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1541">4</span></span>

<span data-ttu-id="cb188-1542">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1542">5</span></span>

<span data-ttu-id="cb188-1543">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1543">6</span></span>

<span data-ttu-id="cb188-1544">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1544">7</span></span>

<span data-ttu-id="cb188-1545">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1545">8</span></span>

<span data-ttu-id="cb188-1546">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1546">9</span></span>

<span data-ttu-id="cb188-1547">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1547">2</span></span><br/> <span data-ttu-id="cb188-1548">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1548">0</span></span><br/>

<span data-ttu-id="cb188-1549">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1549">1</span></span>

<span data-ttu-id="cb188-1550">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1550">2</span></span>

<span data-ttu-id="cb188-1551">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1551">3</span></span>

<span data-ttu-id="cb188-1552">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1552">4</span></span>

<span data-ttu-id="cb188-1553">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1553">5</span></span>

<span data-ttu-id="cb188-1554">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1554">6</span></span>

<span data-ttu-id="cb188-1555">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1555">7</span></span>

<span data-ttu-id="cb188-1556">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1556">8</span></span>

<span data-ttu-id="cb188-1557">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1557">9</span></span>

<span data-ttu-id="cb188-1558">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1558">3</span></span><br/> <span data-ttu-id="cb188-1559">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1559">0</span></span><br/>

<span data-ttu-id="cb188-1560">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1560">1</span></span>

<span data-ttu-id="cb188-1561">\_pres (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1561">\_pres (variable)</span></span>

<span data-ttu-id="cb188-1562">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1562">...</span></span>

<span data-ttu-id="cb188-1563">\_padding (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1563">\_padding (variable)</span></span>

<span data-ttu-id="cb188-1564">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="cb188-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="cb188-1565">**\_ pres:** albero dei comandi CNodeRestriction su cui deve essere eseguita un'operazione OR classificata.</span><span class="sxs-lookup"><span data-stu-id="cb188-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="cb188-1566">**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cb188-1567">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cb188-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cb188-1568">Se questo campo è presente,ad esempio una lunghezza diversa da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cb188-1569">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-1570">**\_ ulRankMethod:** intero senza segno a 32 bit che specifica un algoritmo di classificazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="cb188-1571">DEVE essere impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="cb188-1572">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1572">Value</span></span>                            | <span data-ttu-id="cb188-1573">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="cb188-1574">NUMERO \_ MINIMO DI CLASSIFICAZIONE \_ VETTORIALE 0X00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="cb188-1575">Usare l'algoritmo \[ minimo SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cb188-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="cb188-1576">VECTOR \_ RANK \_ MAX 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="cb188-1577">Usare l'algoritmo \[ massimo SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cb188-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="cb188-1578">VETTORE \_ RANK \_ INNER 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="cb188-1579">Usare l'algoritmo del \[ prodotto interno \] SALTON.</span><span class="sxs-lookup"><span data-stu-id="cb188-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="cb188-1580">VECTOR \_ RANK \_ DICE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="cb188-1581">Usare l'algoritmo del \[ coefficiente Dice SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cb188-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="cb188-1582">VECTOR \_ RANK \_ E 0X00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="cb188-1583">Usare l'algoritmo di coefficiente \[ Jaccard SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cb188-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="cb188-1584">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="cb188-1585">La struttura CWordRestriction contiene una parola per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="cb188-1586">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1586">0</span></span>

<span data-ttu-id="cb188-1587">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1587">1</span></span>

<span data-ttu-id="cb188-1588">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1588">2</span></span>

<span data-ttu-id="cb188-1589">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1589">3</span></span>

<span data-ttu-id="cb188-1590">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1590">4</span></span>

<span data-ttu-id="cb188-1591">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1591">5</span></span>

<span data-ttu-id="cb188-1592">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1592">6</span></span>

<span data-ttu-id="cb188-1593">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1593">7</span></span>

<span data-ttu-id="cb188-1594">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1594">8</span></span>

<span data-ttu-id="cb188-1595">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1595">9</span></span>

<span data-ttu-id="cb188-1596">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1596">1</span></span><br/> <span data-ttu-id="cb188-1597">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1597">0</span></span><br/>

<span data-ttu-id="cb188-1598">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1598">1</span></span>

<span data-ttu-id="cb188-1599">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1599">2</span></span>

<span data-ttu-id="cb188-1600">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1600">3</span></span>

<span data-ttu-id="cb188-1601">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1601">4</span></span>

<span data-ttu-id="cb188-1602">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1602">5</span></span>

<span data-ttu-id="cb188-1603">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1603">6</span></span>

<span data-ttu-id="cb188-1604">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1604">7</span></span>

<span data-ttu-id="cb188-1605">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1605">8</span></span>

<span data-ttu-id="cb188-1606">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1606">9</span></span>

<span data-ttu-id="cb188-1607">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1607">2</span></span><br/> <span data-ttu-id="cb188-1608">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1608">0</span></span><br/>

<span data-ttu-id="cb188-1609">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1609">1</span></span>

<span data-ttu-id="cb188-1610">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1610">2</span></span>

<span data-ttu-id="cb188-1611">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1611">3</span></span>

<span data-ttu-id="cb188-1612">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1612">4</span></span>

<span data-ttu-id="cb188-1613">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1613">5</span></span>

<span data-ttu-id="cb188-1614">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1614">6</span></span>

<span data-ttu-id="cb188-1615">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1615">7</span></span>

<span data-ttu-id="cb188-1616">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1616">8</span></span>

<span data-ttu-id="cb188-1617">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1617">9</span></span>

<span data-ttu-id="cb188-1618">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1618">3</span></span><br/> <span data-ttu-id="cb188-1619">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1619">0</span></span><br/>

<span data-ttu-id="cb188-1620">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1620">1</span></span>

<span data-ttu-id="cb188-1621">restrizione</span><span class="sxs-lookup"><span data-stu-id="cb188-1621">restriction</span></span>

<span data-ttu-id="cb188-1622">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1622">...</span></span>

<span data-ttu-id="cb188-1623">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1623">...</span></span>

<span data-ttu-id="cb188-1624">\_key (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1624">\_key (variable)</span></span>

<span data-ttu-id="cb188-1625">\_isRange</span><span class="sxs-lookup"><span data-stu-id="cb188-1625">\_isRange</span></span>



 

<span data-ttu-id="cb188-1626">**restriction:** struttura COccRestriction che specifica la posizione della parola.</span><span class="sxs-lookup"><span data-stu-id="cb188-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="cb188-1627">**\_ key:** struttura CKey che specifica una parola.</span><span class="sxs-lookup"><span data-stu-id="cb188-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="cb188-1628">**\_ isRange:** se impostato su 0x01, la chiave è un prefisso per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="cb188-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="cb188-1629">Se impostato su 0x00, la chiave è un valore esatto di cui trovare la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="cb188-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="cb188-1630">\_isRange NON DEVE essere impostato su qualsiasi altro valore.</span><span class="sxs-lookup"><span data-stu-id="cb188-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="cb188-1631">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="cb188-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="cb188-1632">La struttura CRestriction contiene un nodo di un albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="cb188-1633">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1633">0</span></span>

<span data-ttu-id="cb188-1634">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1634">1</span></span>

<span data-ttu-id="cb188-1635">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1635">2</span></span>

<span data-ttu-id="cb188-1636">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1636">3</span></span>

<span data-ttu-id="cb188-1637">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1637">4</span></span>

<span data-ttu-id="cb188-1638">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1638">5</span></span>

<span data-ttu-id="cb188-1639">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1639">6</span></span>

<span data-ttu-id="cb188-1640">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1640">7</span></span>

<span data-ttu-id="cb188-1641">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1641">8</span></span>

<span data-ttu-id="cb188-1642">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1642">9</span></span>

<span data-ttu-id="cb188-1643">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1643">1</span></span><br/> <span data-ttu-id="cb188-1644">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1644">0</span></span><br/>

<span data-ttu-id="cb188-1645">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1645">1</span></span>

<span data-ttu-id="cb188-1646">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1646">2</span></span>

<span data-ttu-id="cb188-1647">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1647">3</span></span>

<span data-ttu-id="cb188-1648">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1648">4</span></span>

<span data-ttu-id="cb188-1649">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1649">5</span></span>

<span data-ttu-id="cb188-1650">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1650">6</span></span>

<span data-ttu-id="cb188-1651">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1651">7</span></span>

<span data-ttu-id="cb188-1652">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1652">8</span></span>

<span data-ttu-id="cb188-1653">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1653">9</span></span>

<span data-ttu-id="cb188-1654">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1654">2</span></span><br/> <span data-ttu-id="cb188-1655">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1655">0</span></span><br/>

<span data-ttu-id="cb188-1656">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1656">1</span></span>

<span data-ttu-id="cb188-1657">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1657">2</span></span>

<span data-ttu-id="cb188-1658">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1658">3</span></span>

<span data-ttu-id="cb188-1659">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1659">4</span></span>

<span data-ttu-id="cb188-1660">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1660">5</span></span>

<span data-ttu-id="cb188-1661">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1661">6</span></span>

<span data-ttu-id="cb188-1662">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1662">7</span></span>

<span data-ttu-id="cb188-1663">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1663">8</span></span>

<span data-ttu-id="cb188-1664">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1664">9</span></span>

<span data-ttu-id="cb188-1665">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1665">3</span></span><br/> <span data-ttu-id="cb188-1666">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1666">0</span></span><br/>

<span data-ttu-id="cb188-1667">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1667">1</span></span>

<span data-ttu-id="cb188-1668">\_ulType</span><span class="sxs-lookup"><span data-stu-id="cb188-1668">\_ulType</span></span>

<span data-ttu-id="cb188-1669">Peso</span><span class="sxs-lookup"><span data-stu-id="cb188-1669">Weight</span></span>

<span data-ttu-id="cb188-1670">Restrizione</span><span class="sxs-lookup"><span data-stu-id="cb188-1670">Restriction</span></span>



 

<span data-ttu-id="cb188-1671">**\_ ulType:** intero senza segno a 32 bit che indica il tipo di restrizione usato per il nodo dell'albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="cb188-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="cb188-1672">DEVE essere impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="cb188-1673">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1673">Value</span></span>                    | <span data-ttu-id="cb188-1674">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1675">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="cb188-1676">Il nodo rappresenta una parola non erta in una query vettoriale.</span><span class="sxs-lookup"><span data-stu-id="cb188-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="cb188-1677">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="cb188-1678">Il nodo contiene un CNodeRestriction su cui deve essere eseguita un'operazione AND logica.</span><span class="sxs-lookup"><span data-stu-id="cb188-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="cb188-1679">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="cb188-1680">Il nodo contiene un oggetto CNodeRestriction su cui deve essere eseguita un'operazione OR logica.</span><span class="sxs-lookup"><span data-stu-id="cb188-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="cb188-1681">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="cb188-1682">Il nodo contiene un oggetto CRestriction su cui deve essere eseguita un'operazione NOT.</span><span class="sxs-lookup"><span data-stu-id="cb188-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="cb188-1683">RtContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="cb188-1684">Il nodo contiene un elemento CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="cb188-1685">Proprietà RTProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="cb188-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="cb188-1686">Il nodo contiene un oggetto CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="cb188-1687">RtProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="cb188-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="cb188-1688">Il nodo contiene un oggetto CNodeRestriction su cui deve essere eseguita una classificazione di prossimità,</span><span class="sxs-lookup"><span data-stu-id="cb188-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="cb188-1689">RtVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb188-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="cb188-1690">Il nodo contiene un oggetto CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="cb188-1691">RtNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb188-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="cb188-1692">Il nodo contiene un oggetto CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="cb188-1693">RtScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="cb188-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="cb188-1694">Il nodo contiene un oggetto CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="cb188-1695">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="cb188-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="cb188-1696">Il nodo contiene un oggetto CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="cb188-1697">RtRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="cb188-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="cb188-1698">Il nodo contiene un oggetto CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="cb188-1699">RtPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="cb188-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="cb188-1700">Il nodo contiene un oggetto CNodeRestriction su cui deve essere eseguita una corrispondenza di frase.</span><span class="sxs-lookup"><span data-stu-id="cb188-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="cb188-1701">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="cb188-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="cb188-1702">Il nodo contiene un CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="cb188-1703">RtWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="cb188-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="cb188-1704">Il nodo contiene un CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="cb188-1705">**Weight:** intero senza segno a 32 bit che rappresenta il peso del nodo.</span><span class="sxs-lookup"><span data-stu-id="cb188-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="cb188-1706">Weight indica l'importanza del nodo rispetto ad altri nodi nell'albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="cb188-1707">I valori di peso più elevati sono più importanti.</span><span class="sxs-lookup"><span data-stu-id="cb188-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="cb188-1708">**Restrizione**: tipo di restrizione per il nodo dell'albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="cb188-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="cb188-1709">La sintassi DEVE essere come indicato dal \_ campo ulType.</span><span class="sxs-lookup"><span data-stu-id="cb188-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="cb188-1710">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="cb188-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="cb188-1711">La struttura CColumnSet specifica i numeri di colonna da restituire.</span><span class="sxs-lookup"><span data-stu-id="cb188-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="cb188-1712">Questa struttura viene sempre usata in riferimento a una struttura CPidMapper specifica (sezione 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="cb188-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="cb188-1713">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1713">0</span></span>

<span data-ttu-id="cb188-1714">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1714">1</span></span>

<span data-ttu-id="cb188-1715">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1715">2</span></span>

<span data-ttu-id="cb188-1716">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1716">3</span></span>

<span data-ttu-id="cb188-1717">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1717">4</span></span>

<span data-ttu-id="cb188-1718">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1718">5</span></span>

<span data-ttu-id="cb188-1719">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1719">6</span></span>

<span data-ttu-id="cb188-1720">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1720">7</span></span>

<span data-ttu-id="cb188-1721">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1721">8</span></span>

<span data-ttu-id="cb188-1722">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1722">9</span></span>

<span data-ttu-id="cb188-1723">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1723">1</span></span><br/> <span data-ttu-id="cb188-1724">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1724">0</span></span><br/>

<span data-ttu-id="cb188-1725">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1725">1</span></span>

<span data-ttu-id="cb188-1726">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1726">2</span></span>

<span data-ttu-id="cb188-1727">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1727">3</span></span>

<span data-ttu-id="cb188-1728">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1728">4</span></span>

<span data-ttu-id="cb188-1729">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1729">5</span></span>

<span data-ttu-id="cb188-1730">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1730">6</span></span>

<span data-ttu-id="cb188-1731">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1731">7</span></span>

<span data-ttu-id="cb188-1732">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1732">8</span></span>

<span data-ttu-id="cb188-1733">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1733">9</span></span>

<span data-ttu-id="cb188-1734">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1734">2</span></span><br/> <span data-ttu-id="cb188-1735">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1735">0</span></span><br/>

<span data-ttu-id="cb188-1736">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1736">1</span></span>

<span data-ttu-id="cb188-1737">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1737">2</span></span>

<span data-ttu-id="cb188-1738">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1738">3</span></span>

<span data-ttu-id="cb188-1739">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1739">4</span></span>

<span data-ttu-id="cb188-1740">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1740">5</span></span>

<span data-ttu-id="cb188-1741">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1741">6</span></span>

<span data-ttu-id="cb188-1742">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1742">7</span></span>

<span data-ttu-id="cb188-1743">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1743">8</span></span>

<span data-ttu-id="cb188-1744">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1744">9</span></span>

<span data-ttu-id="cb188-1745">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1745">3</span></span><br/> <span data-ttu-id="cb188-1746">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1746">0</span></span><br/>

<span data-ttu-id="cb188-1747">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1747">1</span></span>

<span data-ttu-id="cb188-1748">count</span><span class="sxs-lookup"><span data-stu-id="cb188-1748">count</span></span>

<span data-ttu-id="cb188-1749">indexes (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1749">indexes (variable)</span></span>



 

<span data-ttu-id="cb188-1750">**count:** intero senza segno a 32 bit che specifica il numero di elementi nella matrice di indici.</span><span class="sxs-lookup"><span data-stu-id="cb188-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="cb188-1751">**indexes:** matrice di interi senza segno a 4 byte che rappresentano indici in base zero nella matrice aPropSpec nella struttura CPidMapper corrispondente.</span><span class="sxs-lookup"><span data-stu-id="cb188-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="cb188-1752">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="cb188-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="cb188-1753">La struttura CCategorizationSet contiene informazioni sul raggruppamento di un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="cb188-1754">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1754">0</span></span>

<span data-ttu-id="cb188-1755">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1755">1</span></span>

<span data-ttu-id="cb188-1756">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1756">2</span></span>

<span data-ttu-id="cb188-1757">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1757">3</span></span>

<span data-ttu-id="cb188-1758">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1758">4</span></span>

<span data-ttu-id="cb188-1759">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1759">5</span></span>

<span data-ttu-id="cb188-1760">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1760">6</span></span>

<span data-ttu-id="cb188-1761">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1761">7</span></span>

<span data-ttu-id="cb188-1762">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1762">8</span></span>

<span data-ttu-id="cb188-1763">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1763">9</span></span>

<span data-ttu-id="cb188-1764">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1764">1</span></span><br/> <span data-ttu-id="cb188-1765">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1765">0</span></span><br/>

<span data-ttu-id="cb188-1766">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1766">1</span></span>

<span data-ttu-id="cb188-1767">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1767">2</span></span>

<span data-ttu-id="cb188-1768">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1768">3</span></span>

<span data-ttu-id="cb188-1769">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1769">4</span></span>

<span data-ttu-id="cb188-1770">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1770">5</span></span>

<span data-ttu-id="cb188-1771">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1771">6</span></span>

<span data-ttu-id="cb188-1772">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1772">7</span></span>

<span data-ttu-id="cb188-1773">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1773">8</span></span>

<span data-ttu-id="cb188-1774">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1774">9</span></span>

<span data-ttu-id="cb188-1775">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1775">2</span></span><br/> <span data-ttu-id="cb188-1776">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1776">0</span></span><br/>

<span data-ttu-id="cb188-1777">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1777">1</span></span>

<span data-ttu-id="cb188-1778">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1778">2</span></span>

<span data-ttu-id="cb188-1779">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1779">3</span></span>

<span data-ttu-id="cb188-1780">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1780">4</span></span>

<span data-ttu-id="cb188-1781">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1781">5</span></span>

<span data-ttu-id="cb188-1782">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1782">6</span></span>

<span data-ttu-id="cb188-1783">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1783">7</span></span>

<span data-ttu-id="cb188-1784">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1784">8</span></span>

<span data-ttu-id="cb188-1785">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1785">9</span></span>

<span data-ttu-id="cb188-1786">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1786">3</span></span><br/> <span data-ttu-id="cb188-1787">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1787">0</span></span><br/>

<span data-ttu-id="cb188-1788">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1788">1</span></span>

<span data-ttu-id="cb188-1789">count</span><span class="sxs-lookup"><span data-stu-id="cb188-1789">count</span></span>

<span data-ttu-id="cb188-1790">categories (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1790">categories (variable)</span></span>



 

<span data-ttu-id="cb188-1791">**count**: intero senza segno a 32 bit contenente il numero di elementi nella matrice categories.</span><span class="sxs-lookup"><span data-stu-id="cb188-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="cb188-1792">**categories:** matrice di strutture CCategorizationSpec che specificano il raggruppamento della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="cb188-1793">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="cb188-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="cb188-1794">La struttura CCategorizationSpec contiene un raggruppamento per un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="cb188-1795">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1795">0</span></span>

<span data-ttu-id="cb188-1796">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1796">1</span></span>

<span data-ttu-id="cb188-1797">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1797">2</span></span>

<span data-ttu-id="cb188-1798">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1798">3</span></span>

<span data-ttu-id="cb188-1799">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1799">4</span></span>

<span data-ttu-id="cb188-1800">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1800">5</span></span>

<span data-ttu-id="cb188-1801">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1801">6</span></span>

<span data-ttu-id="cb188-1802">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1802">7</span></span>

<span data-ttu-id="cb188-1803">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1803">8</span></span>

<span data-ttu-id="cb188-1804">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1804">9</span></span>

<span data-ttu-id="cb188-1805">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1805">1</span></span><br/> <span data-ttu-id="cb188-1806">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1806">0</span></span><br/>

<span data-ttu-id="cb188-1807">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1807">1</span></span>

<span data-ttu-id="cb188-1808">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1808">2</span></span>

<span data-ttu-id="cb188-1809">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1809">3</span></span>

<span data-ttu-id="cb188-1810">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1810">4</span></span>

<span data-ttu-id="cb188-1811">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1811">5</span></span>

<span data-ttu-id="cb188-1812">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1812">6</span></span>

<span data-ttu-id="cb188-1813">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1813">7</span></span>

<span data-ttu-id="cb188-1814">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1814">8</span></span>

<span data-ttu-id="cb188-1815">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1815">9</span></span>

<span data-ttu-id="cb188-1816">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1816">2</span></span><br/> <span data-ttu-id="cb188-1817">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1817">0</span></span><br/>

<span data-ttu-id="cb188-1818">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1818">1</span></span>

<span data-ttu-id="cb188-1819">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1819">2</span></span>

<span data-ttu-id="cb188-1820">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1820">3</span></span>

<span data-ttu-id="cb188-1821">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1821">4</span></span>

<span data-ttu-id="cb188-1822">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1822">5</span></span>

<span data-ttu-id="cb188-1823">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1823">6</span></span>

<span data-ttu-id="cb188-1824">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1824">7</span></span>

<span data-ttu-id="cb188-1825">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1825">8</span></span>

<span data-ttu-id="cb188-1826">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1826">9</span></span>

<span data-ttu-id="cb188-1827">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1827">3</span></span><br/> <span data-ttu-id="cb188-1828">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1828">0</span></span><br/>

<span data-ttu-id="cb188-1829">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1829">1</span></span>

<span data-ttu-id="cb188-1830">\_csColumns (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="cb188-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="cb188-1831">\_ulCategType</span></span>



 

<span data-ttu-id="cb188-1832">**\_ csColumns:** struttura CColumnSet che indica le colonne in base alle quali raggruppare la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="cb188-1833">**\_ ulCategType:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cb188-1834">DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="cb188-1835">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="cb188-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="cb188-1836">La struttura CDbColId contiene una colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="cb188-1837">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1837">0</span></span>

<span data-ttu-id="cb188-1838">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1838">1</span></span>

<span data-ttu-id="cb188-1839">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1839">2</span></span>

<span data-ttu-id="cb188-1840">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1840">3</span></span>

<span data-ttu-id="cb188-1841">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1841">4</span></span>

<span data-ttu-id="cb188-1842">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1842">5</span></span>

<span data-ttu-id="cb188-1843">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1843">6</span></span>

<span data-ttu-id="cb188-1844">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1844">7</span></span>

<span data-ttu-id="cb188-1845">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1845">8</span></span>

<span data-ttu-id="cb188-1846">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1846">9</span></span>

<span data-ttu-id="cb188-1847">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1847">1</span></span><br/> <span data-ttu-id="cb188-1848">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1848">0</span></span><br/>

<span data-ttu-id="cb188-1849">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1849">1</span></span>

<span data-ttu-id="cb188-1850">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1850">2</span></span>

<span data-ttu-id="cb188-1851">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1851">3</span></span>

<span data-ttu-id="cb188-1852">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1852">4</span></span>

<span data-ttu-id="cb188-1853">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1853">5</span></span>

<span data-ttu-id="cb188-1854">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1854">6</span></span>

<span data-ttu-id="cb188-1855">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1855">7</span></span>

<span data-ttu-id="cb188-1856">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1856">8</span></span>

<span data-ttu-id="cb188-1857">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1857">9</span></span>

<span data-ttu-id="cb188-1858">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1858">2</span></span><br/> <span data-ttu-id="cb188-1859">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1859">0</span></span><br/>

<span data-ttu-id="cb188-1860">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1860">1</span></span>

<span data-ttu-id="cb188-1861">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1861">2</span></span>

<span data-ttu-id="cb188-1862">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1862">3</span></span>

<span data-ttu-id="cb188-1863">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1863">4</span></span>

<span data-ttu-id="cb188-1864">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1864">5</span></span>

<span data-ttu-id="cb188-1865">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1865">6</span></span>

<span data-ttu-id="cb188-1866">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1866">7</span></span>

<span data-ttu-id="cb188-1867">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1867">8</span></span>

<span data-ttu-id="cb188-1868">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1868">9</span></span>

<span data-ttu-id="cb188-1869">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1869">3</span></span><br/> <span data-ttu-id="cb188-1870">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1870">0</span></span><br/>

<span data-ttu-id="cb188-1871">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1871">1</span></span>

<span data-ttu-id="cb188-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="cb188-1872">eKind</span></span>

<span data-ttu-id="cb188-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="cb188-1873">GUID</span></span>

<span data-ttu-id="cb188-1874">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1874">...</span></span>

<span data-ttu-id="cb188-1875">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1875">...</span></span>

<span data-ttu-id="cb188-1876">...</span><span class="sxs-lookup"><span data-stu-id="cb188-1876">...</span></span>

<span data-ttu-id="cb188-1877">ulId</span><span class="sxs-lookup"><span data-stu-id="cb188-1877">ulId</span></span>

<span data-ttu-id="cb188-1878">vString (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1878">vString (variable)</span></span>



 

<span data-ttu-id="cb188-1879">**eKind:** DEVE essere impostato su uno dei valori seguenti che indica il contenuto di GUID e vValue.</span><span class="sxs-lookup"><span data-stu-id="cb188-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="cb188-1880">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1880">Value</span></span>                            | <span data-ttu-id="cb188-1881">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1882">NOME GUID DBKIND \_ \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="cb188-1883">vString contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="cb188-1884">DBKIND \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="cb188-1885">ulId contiene un intero a 4 byte che indica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="cb188-1886">NOME \_ DBKIND PGUID \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="cb188-1887">vString contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1887">vString contains a property name.</span></span> <span data-ttu-id="cb188-1888">Questo valore DEVE essere considerato uguale a DBKIND \_ GUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="cb188-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="cb188-1889">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="cb188-1890">ulId contiene un numero intero a 4 byte che indica l'ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="cb188-1891">Questo valore DEVE essere uguale a DBKIND \_ GUID \_ PROPID.</span><span class="sxs-lookup"><span data-stu-id="cb188-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="cb188-1892">**GUID: GUID** della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="cb188-1893">**ulId:** se eKind è \_ DBKIND GUID PROPID o DBKIND PGUID PROPID, questo campo contiene un intero senza segno, specificando \_ \_ \_ l'ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="cb188-1894">Se eKind è DBKIND GUID NAME o DBKIND PGUID NAME, questo campo contiene un intero senza segno che specifica il numero di caratteri \_ Unicode contenuti nel campo \_ \_ \_ vString.</span><span class="sxs-lookup"><span data-stu-id="cb188-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="cb188-1895">**vString:** stringa Unicode non con terminazione Null che rappresenta il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="cb188-1896">Deve essere omesso a meno che il campo eKind non sia impostato su DBKIND \_ GUID \_ NAME o DBKIND \_ PGUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="cb188-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="cb188-1897">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="cb188-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="cb188-1898">La struttura CDbProp contiene una proprietà .</span><span class="sxs-lookup"><span data-stu-id="cb188-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="cb188-1899">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1899">0</span></span>

<span data-ttu-id="cb188-1900">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1900">1</span></span>

<span data-ttu-id="cb188-1901">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1901">2</span></span>

<span data-ttu-id="cb188-1902">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1902">3</span></span>

<span data-ttu-id="cb188-1903">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1903">4</span></span>

<span data-ttu-id="cb188-1904">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1904">5</span></span>

<span data-ttu-id="cb188-1905">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1905">6</span></span>

<span data-ttu-id="cb188-1906">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1906">7</span></span>

<span data-ttu-id="cb188-1907">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1907">8</span></span>

<span data-ttu-id="cb188-1908">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1908">9</span></span>

<span data-ttu-id="cb188-1909">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1909">1</span></span><br/> <span data-ttu-id="cb188-1910">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1910">0</span></span><br/>

<span data-ttu-id="cb188-1911">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1911">1</span></span>

<span data-ttu-id="cb188-1912">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1912">2</span></span>

<span data-ttu-id="cb188-1913">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1913">3</span></span>

<span data-ttu-id="cb188-1914">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1914">4</span></span>

<span data-ttu-id="cb188-1915">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1915">5</span></span>

<span data-ttu-id="cb188-1916">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1916">6</span></span>

<span data-ttu-id="cb188-1917">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1917">7</span></span>

<span data-ttu-id="cb188-1918">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1918">8</span></span>

<span data-ttu-id="cb188-1919">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1919">9</span></span>

<span data-ttu-id="cb188-1920">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1920">2</span></span><br/> <span data-ttu-id="cb188-1921">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1921">0</span></span><br/>

<span data-ttu-id="cb188-1922">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1922">1</span></span>

<span data-ttu-id="cb188-1923">2</span><span class="sxs-lookup"><span data-stu-id="cb188-1923">2</span></span>

<span data-ttu-id="cb188-1924">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1924">3</span></span>

<span data-ttu-id="cb188-1925">4</span><span class="sxs-lookup"><span data-stu-id="cb188-1925">4</span></span>

<span data-ttu-id="cb188-1926">5</span><span class="sxs-lookup"><span data-stu-id="cb188-1926">5</span></span>

<span data-ttu-id="cb188-1927">6</span><span class="sxs-lookup"><span data-stu-id="cb188-1927">6</span></span>

<span data-ttu-id="cb188-1928">7</span><span class="sxs-lookup"><span data-stu-id="cb188-1928">7</span></span>

<span data-ttu-id="cb188-1929">8</span><span class="sxs-lookup"><span data-stu-id="cb188-1929">8</span></span>

<span data-ttu-id="cb188-1930">9</span><span class="sxs-lookup"><span data-stu-id="cb188-1930">9</span></span>

<span data-ttu-id="cb188-1931">3</span><span class="sxs-lookup"><span data-stu-id="cb188-1931">3</span></span><br/> <span data-ttu-id="cb188-1932">0</span><span class="sxs-lookup"><span data-stu-id="cb188-1932">0</span></span><br/>

<span data-ttu-id="cb188-1933">1</span><span class="sxs-lookup"><span data-stu-id="cb188-1933">1</span></span>

<span data-ttu-id="cb188-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="cb188-1934">DBPROPID</span></span>

<span data-ttu-id="cb188-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="cb188-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="cb188-1936">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="cb188-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="cb188-1937">colid (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1937">colid (variable)</span></span>

<span data-ttu-id="cb188-1938">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-1938">vValue (variable)</span></span>



 

<span data-ttu-id="cb188-1939">**DBPROPID:** intero senza segno a 32 bit che indica l'ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="cb188-1940">**DBPROPOPTIONS:** DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cb188-1941">**DBPROPSTATUS:** DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cb188-1942">**colid:** struttura CDbColId, come specificato nella sezione 2.2.1.20, che indica la colonna a cui si applica la proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="cb188-1943">**vValue:** CBaseStorageVariant contenente il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="cb188-1944">2.2.1.21.1 Proprietà</span><span class="sxs-lookup"><span data-stu-id="cb188-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="cb188-1945">Questa sezione contiene informazioni dettagliate sulle proprietà usate da CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="cb188-1946">Queste proprietà sono raggruppate in tre set di proprietà, ident2.2.1.21.1 nel campo guidPropertySet della struttura CDbPropSet (Sezione 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="cb188-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="cb188-1947">Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà DBPROPSET \_ FSCIFRMWRK \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="cb188-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="cb188-1948">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1948">Value</span></span>                                  | <span data-ttu-id="cb188-1949">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1950">DBPROP \_ CI CATALOG NAME \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="cb188-1951">Specifica il nome del catalogo o dei cataloghi su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="cb188-1952">Il valore DEVE essere un \_ LPWSTR VT o VT \_ VECTOR \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="cb188-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="cb188-1953">DBPROP \_ CI \_ INCLUDE \_ SCOPES 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="cb188-1954">Specifica uno o più percorsi da includere nella query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="cb188-1955">Il valore DEVE essere un \_ LPWSTR VT o VT \_ VECTOR \| VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="cb188-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="cb188-1956">FLAG DI \_ AMBITO CI \_ DBPROP \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="cb188-1957">Specifica la modalità di gestione dei percorsi specificati dalla proprietà DBPROP \_ CI \_ INCLUDE \_ SCOPES.</span><span class="sxs-lookup"><span data-stu-id="cb188-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="cb188-1958">Il valore DEVE essere VT \_ I4 o VT \_ VECTOR \| VT \_ I4.</span><span class="sxs-lookup"><span data-stu-id="cb188-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="cb188-1959">TIPO DI \_ QUERY DBPROP CI \_ \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb188-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="cb188-1960">Specifica il tipo di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1960">Specifies the type of query.</span></span> <span data-ttu-id="cb188-1961">CDbColId DEVE essere impostato su DB \_ NULLID.</span><span class="sxs-lookup"><span data-stu-id="cb188-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="cb188-1962">Nella tabella seguente sono elencati i flag per la proprietà DBPROP \_ CI \_ SCOPE \_ FLAGS:</span><span class="sxs-lookup"><span data-stu-id="cb188-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="cb188-1963">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1963">Value</span></span>                     | <span data-ttu-id="cb188-1964">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1965">QUERY \_ DEEP 0x01</span><span class="sxs-lookup"><span data-stu-id="cb188-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="cb188-1966">Se impostato, indica che i file nella directory dell'ambito e in tutte le sottodirectory vengono inclusi nei risultati.</span><span class="sxs-lookup"><span data-stu-id="cb188-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="cb188-1967">Se l'opzione è deselezionata, nei risultati vengono inclusi solo i file nella directory dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="cb188-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="cb188-1968">NON DEVE essere combinato con QUERY \_ DEEP.</span><span class="sxs-lookup"><span data-stu-id="cb188-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="cb188-1969">ESEGUIRE QUERY \_ \_ SUL PERCORSO VIRTUALE 0x02</span><span class="sxs-lookup"><span data-stu-id="cb188-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="cb188-1970">Se impostato, indica che l'ambito è un percorso virtuale.</span><span class="sxs-lookup"><span data-stu-id="cb188-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="cb188-1971">Se è deselezionata, indica che l'ambito è una directory fisica.</span><span class="sxs-lookup"><span data-stu-id="cb188-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="cb188-1972">Nella tabella seguente sono elencati i tipi di query per la proprietà DBPROP \_ CI \_ QUERY \_ TYPE:</span><span class="sxs-lookup"><span data-stu-id="cb188-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="cb188-1973">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1973">Value</span></span>                     | <span data-ttu-id="cb188-1974">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1975">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="cb188-1976">Query normale.</span><span class="sxs-lookup"><span data-stu-id="cb188-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="cb188-1977">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="cb188-1978">La query richiede un elenco delle radici virtuali del catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="cb188-1979">Questo valore richiede privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="cb188-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="cb188-1980">Proprietà CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="cb188-1981">La query richiede un elenco di tutte le proprietà supportate dal servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="cb188-1982">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="cb188-1983">La query è un'operazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="cb188-1983">The query is an administrative operation.</span></span> <span data-ttu-id="cb188-1984">Questo valore richiede privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="cb188-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="cb188-1985">Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà \_ DBPROPSET QUERYEXT.</span><span class="sxs-lookup"><span data-stu-id="cb188-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="cb188-1986">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-1986">Value</span></span>                                      | <span data-ttu-id="cb188-1987">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-1988">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="cb188-1989">Specifica la modalità di gestione delle query lente da parte del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="cb188-1990">Il valore DEVE essere un valore \_ BOOL VT.</span><span class="sxs-lookup"><span data-stu-id="cb188-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="cb188-1991">Se TRUE, al server è consentito l'esito negativo di queste query.</span><span class="sxs-lookup"><span data-stu-id="cb188-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="cb188-1992">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="cb188-1993">Indica se il servizio di indicizzazione deve eseguire l'operazione di taglio dei risultati.</span><span class="sxs-lookup"><span data-stu-id="cb188-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="cb188-1994">Se TRUE, il server deve prendere in considerazione l'esecuzione del trimming dei risultati in modo da ottimizzare il tempo di risposta al client.</span><span class="sxs-lookup"><span data-stu-id="cb188-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="cb188-1995">Il valore DEVE essere un valore \_ BOOL VT.</span><span class="sxs-lookup"><span data-stu-id="cb188-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="cb188-1996">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="cb188-1997">Indica se il client supporta i tipi di dati \_ VECTOR VT.</span><span class="sxs-lookup"><span data-stu-id="cb188-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="cb188-1998">Se TRUE, il client supporta VT VECTOR; se FALSE, il server deve convertire i tipi di dati \_ VT \_ VECTOR in tipi di dati VT \_ ARRAY.</span><span class="sxs-lookup"><span data-stu-id="cb188-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="cb188-1999">Il valore DEVE essere un valore \_ BOOL VT.</span><span class="sxs-lookup"><span data-stu-id="cb188-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="cb188-2000">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb188-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="cb188-2001">Indica le corrispondenze di riga da restituire.</span><span class="sxs-lookup"><span data-stu-id="cb188-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="cb188-2002">Se TRUE, il server deve restituire il primo set di righe corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="cb188-2003">Se FALSE, devono essere restituite le righe corrispondenti migliori.</span><span class="sxs-lookup"><span data-stu-id="cb188-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="cb188-2004">Il valore DEVE essere un valore \_ BOOL VT.</span><span class="sxs-lookup"><span data-stu-id="cb188-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="cb188-2005">Nella tabella seguente sono elencate le proprietà che fanno parte del set di proprietà DBPROPSET \_ CIFRMWRKCORE \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="cb188-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="cb188-2006">Value/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="cb188-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="cb188-2007">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-2008">DBPROP \_ MACHINE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="cb188-2009">Specifica i nomi dei computer in cui deve essere elaborata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="cb188-2010">Il valore DEVE essere VT \_ BSTR o VT \_ ARRAY \| VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="cb188-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="cb188-2011">DBPROP \_ CLIENT \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="cb188-2012">Specifica una costante di connessione per il servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="cb188-2013">Il valore DEVE essere un CLSID VT \_ contenente 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="cb188-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="cb188-2014">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="cb188-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="cb188-2015">La struttura CDbPropSet contiene un set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="cb188-2016">Si noti che il primo campo ha dimensioni fisse, ma potrebbe non essere allineato a un offset che è un multiplo di 4 byte dall'inizio del messaggio contenente questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cb188-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="cb188-2017">Tuttavia, il campo cProperties è allineato come tale e di conseguenza il formato è illustrato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="cb188-2018">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2018">0</span></span>

<span data-ttu-id="cb188-2019">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2019">1</span></span>

<span data-ttu-id="cb188-2020">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2020">2</span></span>

<span data-ttu-id="cb188-2021">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2021">3</span></span>

<span data-ttu-id="cb188-2022">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2022">4</span></span>

<span data-ttu-id="cb188-2023">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2023">5</span></span>

<span data-ttu-id="cb188-2024">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2024">6</span></span>

<span data-ttu-id="cb188-2025">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2025">7</span></span>

<span data-ttu-id="cb188-2026">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2026">8</span></span>

<span data-ttu-id="cb188-2027">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2027">9</span></span>

<span data-ttu-id="cb188-2028">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2028">1</span></span><br/> <span data-ttu-id="cb188-2029">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2029">0</span></span><br/>

<span data-ttu-id="cb188-2030">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2030">1</span></span>

<span data-ttu-id="cb188-2031">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2031">2</span></span>

<span data-ttu-id="cb188-2032">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2032">3</span></span>

<span data-ttu-id="cb188-2033">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2033">4</span></span>

<span data-ttu-id="cb188-2034">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2034">5</span></span>

<span data-ttu-id="cb188-2035">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2035">6</span></span>

<span data-ttu-id="cb188-2036">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2036">7</span></span>

<span data-ttu-id="cb188-2037">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2037">8</span></span>

<span data-ttu-id="cb188-2038">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2038">9</span></span>

<span data-ttu-id="cb188-2039">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2039">2</span></span><br/> <span data-ttu-id="cb188-2040">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2040">0</span></span><br/>

<span data-ttu-id="cb188-2041">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2041">1</span></span>

<span data-ttu-id="cb188-2042">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2042">2</span></span>

<span data-ttu-id="cb188-2043">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2043">3</span></span>

<span data-ttu-id="cb188-2044">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2044">4</span></span>

<span data-ttu-id="cb188-2045">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2045">5</span></span>

<span data-ttu-id="cb188-2046">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2046">6</span></span>

<span data-ttu-id="cb188-2047">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2047">7</span></span>

<span data-ttu-id="cb188-2048">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2048">8</span></span>

<span data-ttu-id="cb188-2049">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2049">9</span></span>

<span data-ttu-id="cb188-2050">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2050">3</span></span><br/> <span data-ttu-id="cb188-2051">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2051">0</span></span><br/>

<span data-ttu-id="cb188-2052">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2052">1</span></span>

<span data-ttu-id="cb188-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="cb188-2053">guidPropertySet</span></span>

<span data-ttu-id="cb188-2054">...</span><span class="sxs-lookup"><span data-stu-id="cb188-2054">...</span></span>

<span data-ttu-id="cb188-2055">...</span><span class="sxs-lookup"><span data-stu-id="cb188-2055">...</span></span>

<span data-ttu-id="cb188-2056">...</span><span class="sxs-lookup"><span data-stu-id="cb188-2056">...</span></span>

<span data-ttu-id="cb188-2057">...</span><span class="sxs-lookup"><span data-stu-id="cb188-2057">...</span></span>

<span data-ttu-id="cb188-2058">\_padding (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-2058">\_padding (variable)</span></span>

<span data-ttu-id="cb188-2059">cProperties</span><span class="sxs-lookup"><span data-stu-id="cb188-2059">cProperties</span></span>

<span data-ttu-id="cb188-2060">aProps (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-2060">aProps (variable)</span></span>



 

<span data-ttu-id="cb188-2061">**guidPropertySet:** GUID che identifica il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="cb188-2062">DEVE essere impostato sul formato binario corrispondente a uno dei valori seguenti (visualizzati nella rappresentazione di stringa), identificando il set di proprietà delle proprietà contenute nel campo aProps.</span><span class="sxs-lookup"><span data-stu-id="cb188-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="cb188-2063">Valore/GUID</span><span class="sxs-lookup"><span data-stu-id="cb188-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="cb188-2064">Nome</span><span class="sxs-lookup"><span data-stu-id="cb188-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="cb188-2065">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="cb188-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="cb188-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="cb188-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="cb188-2067">Set di proprietà del framework dell'indice di contenuto del file system</span><span class="sxs-lookup"><span data-stu-id="cb188-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="cb188-2068">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="cb188-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="cb188-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="cb188-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="cb188-2070">Set di proprietà dell'estensione query</span><span class="sxs-lookup"><span data-stu-id="cb188-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="cb188-2071">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="cb188-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="cb188-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="cb188-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="cb188-2073">Content Index Framework Core Property Set</span><span class="sxs-lookup"><span data-stu-id="cb188-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="cb188-2074">**\_ padding:** questo campo DEVE avere una lunghezza da 0 a 3 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cb188-2075">La lunghezza di questo campo DEVE essere tale che il campo seguente inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa struttura.</span><span class="sxs-lookup"><span data-stu-id="cb188-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cb188-2076">Se questo campo è presente(ad esempio, lunghezza diversa da zero), il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cb188-2077">Il contenuto di questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-2078">**cProperties:** intero senza segno a 32 bit contenente il numero di elementi nella matrice aProps.</span><span class="sxs-lookup"><span data-stu-id="cb188-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="cb188-2079">**aProps:** matrice di strutture CDbProp, come specificato nella sezione 0, contenente le proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="cb188-2080">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di riempimento in modo che ogni struttura inizi in corrispondenza di un offset che è un multiplo di 4 byte dall'inizio del messaggio che contiene questa matrice.</span><span class="sxs-lookup"><span data-stu-id="cb188-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cb188-2081">Se sono presenti byte di riempimento, il valore in essi contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cb188-2082">Il contenuto dei byte di riempimento DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="cb188-2083">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="cb188-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="cb188-2084">La struttura CPidMapper contiene una matrice di ID proprietà che specificano le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="cb188-2085">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2085">0</span></span>

<span data-ttu-id="cb188-2086">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2086">1</span></span>

<span data-ttu-id="cb188-2087">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2087">2</span></span>

<span data-ttu-id="cb188-2088">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2088">3</span></span>

<span data-ttu-id="cb188-2089">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2089">4</span></span>

<span data-ttu-id="cb188-2090">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2090">5</span></span>

<span data-ttu-id="cb188-2091">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2091">6</span></span>

<span data-ttu-id="cb188-2092">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2092">7</span></span>

<span data-ttu-id="cb188-2093">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2093">8</span></span>

<span data-ttu-id="cb188-2094">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2094">9</span></span>

<span data-ttu-id="cb188-2095">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2095">1</span></span><br/> <span data-ttu-id="cb188-2096">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2096">0</span></span><br/>

<span data-ttu-id="cb188-2097">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2097">1</span></span>

<span data-ttu-id="cb188-2098">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2098">2</span></span>

<span data-ttu-id="cb188-2099">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2099">3</span></span>

<span data-ttu-id="cb188-2100">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2100">4</span></span>

<span data-ttu-id="cb188-2101">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2101">5</span></span>

<span data-ttu-id="cb188-2102">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2102">6</span></span>

<span data-ttu-id="cb188-2103">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2103">7</span></span>

<span data-ttu-id="cb188-2104">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2104">8</span></span>

<span data-ttu-id="cb188-2105">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2105">9</span></span>

<span data-ttu-id="cb188-2106">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2106">2</span></span><br/> <span data-ttu-id="cb188-2107">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2107">0</span></span><br/>

<span data-ttu-id="cb188-2108">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2108">1</span></span>

<span data-ttu-id="cb188-2109">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2109">2</span></span>

<span data-ttu-id="cb188-2110">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2110">3</span></span>

<span data-ttu-id="cb188-2111">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2111">4</span></span>

<span data-ttu-id="cb188-2112">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2112">5</span></span>

<span data-ttu-id="cb188-2113">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2113">6</span></span>

<span data-ttu-id="cb188-2114">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2114">7</span></span>

<span data-ttu-id="cb188-2115">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2115">8</span></span>

<span data-ttu-id="cb188-2116">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2116">9</span></span>

<span data-ttu-id="cb188-2117">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2117">3</span></span><br/> <span data-ttu-id="cb188-2118">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2118">0</span></span><br/>

<span data-ttu-id="cb188-2119">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2119">1</span></span>

<span data-ttu-id="cb188-2120">count</span><span class="sxs-lookup"><span data-stu-id="cb188-2120">count</span></span>

<span data-ttu-id="cb188-2121">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="cb188-2121">aPropSpec</span></span>

<span data-ttu-id="cb188-2122">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-2122">... (variable)</span></span>



 

<span data-ttu-id="cb188-2123">**count:** intero senza segno a 32 bit contenente il numero di elementi nella matrice aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="cb188-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="cb188-2124">**aPropSpec:** matrice di strutture CFullPropSpec che indica le proprietà da restituire.</span><span class="sxs-lookup"><span data-stu-id="cb188-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="cb188-2125">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di riempimento in modo che ogni struttura abbia un allineamento a 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cb188-2126">Tali byte di riempimento possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="cb188-2127">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="cb188-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="cb188-2128">La struttura CRowSeekAt contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cb188-2129">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2129">0</span></span>

<span data-ttu-id="cb188-2130">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2130">1</span></span>

<span data-ttu-id="cb188-2131">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2131">2</span></span>

<span data-ttu-id="cb188-2132">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2132">3</span></span>

<span data-ttu-id="cb188-2133">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2133">4</span></span>

<span data-ttu-id="cb188-2134">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2134">5</span></span>

<span data-ttu-id="cb188-2135">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2135">6</span></span>

<span data-ttu-id="cb188-2136">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2136">7</span></span>

<span data-ttu-id="cb188-2137">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2137">8</span></span>

<span data-ttu-id="cb188-2138">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2138">9</span></span>

<span data-ttu-id="cb188-2139">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2139">1</span></span><br/> <span data-ttu-id="cb188-2140">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2140">0</span></span><br/>

<span data-ttu-id="cb188-2141">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2141">1</span></span>

<span data-ttu-id="cb188-2142">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2142">2</span></span>

<span data-ttu-id="cb188-2143">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2143">3</span></span>

<span data-ttu-id="cb188-2144">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2144">4</span></span>

<span data-ttu-id="cb188-2145">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2145">5</span></span>

<span data-ttu-id="cb188-2146">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2146">6</span></span>

<span data-ttu-id="cb188-2147">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2147">7</span></span>

<span data-ttu-id="cb188-2148">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2148">8</span></span>

<span data-ttu-id="cb188-2149">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2149">9</span></span>

<span data-ttu-id="cb188-2150">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2150">2</span></span><br/> <span data-ttu-id="cb188-2151">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2151">0</span></span><br/>

<span data-ttu-id="cb188-2152">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2152">1</span></span>

<span data-ttu-id="cb188-2153">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2153">2</span></span>

<span data-ttu-id="cb188-2154">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2154">3</span></span>

<span data-ttu-id="cb188-2155">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2155">4</span></span>

<span data-ttu-id="cb188-2156">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2156">5</span></span>

<span data-ttu-id="cb188-2157">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2157">6</span></span>

<span data-ttu-id="cb188-2158">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2158">7</span></span>

<span data-ttu-id="cb188-2159">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2159">8</span></span>

<span data-ttu-id="cb188-2160">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2160">9</span></span>

<span data-ttu-id="cb188-2161">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2161">3</span></span><br/> <span data-ttu-id="cb188-2162">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2162">0</span></span><br/>

<span data-ttu-id="cb188-2163">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2163">1</span></span>

<span data-ttu-id="cb188-2164">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cb188-2164">\_hRegion</span></span>

<span data-ttu-id="cb188-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="cb188-2165">\_cskip</span></span>

<span data-ttu-id="cb188-2166">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="cb188-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="cb188-2167">**\_ hRegion:** DEVE essere impostato su 0x00000000 e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cb188-2168">**\_ cskip:** intero senza segno a 32 bit contenente il numero di righe da ignorare nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="cb188-2169">**\_ bmkOffset:** valore a 32 bit che  rappresenta l'handle del segnalibro che indica la posizione iniziale da cui ignorare il numero di righe specificato in cskip, prima di iniziare il \_ recupero.</span><span class="sxs-lookup"><span data-stu-id="cb188-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="cb188-2170">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="cb188-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="cb188-2171">La struttura CRowSeekAtRatio identifica il punto in cui iniziare il recupero per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cb188-2172">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2172">0</span></span>

<span data-ttu-id="cb188-2173">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2173">1</span></span>

<span data-ttu-id="cb188-2174">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2174">2</span></span>

<span data-ttu-id="cb188-2175">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2175">3</span></span>

<span data-ttu-id="cb188-2176">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2176">4</span></span>

<span data-ttu-id="cb188-2177">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2177">5</span></span>

<span data-ttu-id="cb188-2178">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2178">6</span></span>

<span data-ttu-id="cb188-2179">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2179">7</span></span>

<span data-ttu-id="cb188-2180">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2180">8</span></span>

<span data-ttu-id="cb188-2181">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2181">9</span></span>

<span data-ttu-id="cb188-2182">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2182">1</span></span><br/> <span data-ttu-id="cb188-2183">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2183">0</span></span><br/>

<span data-ttu-id="cb188-2184">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2184">1</span></span>

<span data-ttu-id="cb188-2185">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2185">2</span></span>

<span data-ttu-id="cb188-2186">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2186">3</span></span>

<span data-ttu-id="cb188-2187">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2187">4</span></span>

<span data-ttu-id="cb188-2188">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2188">5</span></span>

<span data-ttu-id="cb188-2189">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2189">6</span></span>

<span data-ttu-id="cb188-2190">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2190">7</span></span>

<span data-ttu-id="cb188-2191">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2191">8</span></span>

<span data-ttu-id="cb188-2192">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2192">9</span></span>

<span data-ttu-id="cb188-2193">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2193">2</span></span><br/> <span data-ttu-id="cb188-2194">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2194">0</span></span><br/>

<span data-ttu-id="cb188-2195">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2195">1</span></span>

<span data-ttu-id="cb188-2196">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2196">2</span></span>

<span data-ttu-id="cb188-2197">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2197">3</span></span>

<span data-ttu-id="cb188-2198">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2198">4</span></span>

<span data-ttu-id="cb188-2199">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2199">5</span></span>

<span data-ttu-id="cb188-2200">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2200">6</span></span>

<span data-ttu-id="cb188-2201">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2201">7</span></span>

<span data-ttu-id="cb188-2202">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2202">8</span></span>

<span data-ttu-id="cb188-2203">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2203">9</span></span>

<span data-ttu-id="cb188-2204">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2204">3</span></span><br/> <span data-ttu-id="cb188-2205">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2205">0</span></span><br/>

<span data-ttu-id="cb188-2206">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2206">1</span></span>

<span data-ttu-id="cb188-2207">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="cb188-2207">CiTblChapt</span></span>

<span data-ttu-id="cb188-2208">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cb188-2208">\_hRegion</span></span>

<span data-ttu-id="cb188-2209">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="cb188-2209">\_ulNumerator</span></span>

<span data-ttu-id="cb188-2210">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="cb188-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="cb188-2211">**CiTblChapt:** intero senza segno a 32 bit che indica il capitolo del set di righe da cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="cb188-2212">**\_ hRegion:** DEVE essere impostato su 0x00000000 e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cb188-2213">**\_ ulNumerator:** intero senza segno a 32 bit che rappresenta il numeratore del rapporto tra le righe del capitolo da cui iniziare il recupero.</span><span class="sxs-lookup"><span data-stu-id="cb188-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="cb188-2214">**\_ ulDenominator:** intero senza segno a 32 bit che rappresenta il denominatore del rapporto tra le righe del capitolo da cui iniziare il recupero.</span><span class="sxs-lookup"><span data-stu-id="cb188-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="cb188-2215">DEVE essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="cb188-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="cb188-2216">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="cb188-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="cb188-2217">La struttura CRowSeekByBookmark identifica i segnalibri da cui iniziare a recuperare le righe per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cb188-2218">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2218">0</span></span>

<span data-ttu-id="cb188-2219">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2219">1</span></span>

<span data-ttu-id="cb188-2220">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2220">2</span></span>

<span data-ttu-id="cb188-2221">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2221">3</span></span>

<span data-ttu-id="cb188-2222">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2222">4</span></span>

<span data-ttu-id="cb188-2223">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2223">5</span></span>

<span data-ttu-id="cb188-2224">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2224">6</span></span>

<span data-ttu-id="cb188-2225">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2225">7</span></span>

<span data-ttu-id="cb188-2226">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2226">8</span></span>

<span data-ttu-id="cb188-2227">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2227">9</span></span>

<span data-ttu-id="cb188-2228">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2228">1</span></span><br/> <span data-ttu-id="cb188-2229">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2229">0</span></span><br/>

<span data-ttu-id="cb188-2230">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2230">1</span></span>

<span data-ttu-id="cb188-2231">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2231">2</span></span>

<span data-ttu-id="cb188-2232">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2232">3</span></span>

<span data-ttu-id="cb188-2233">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2233">4</span></span>

<span data-ttu-id="cb188-2234">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2234">5</span></span>

<span data-ttu-id="cb188-2235">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2235">6</span></span>

<span data-ttu-id="cb188-2236">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2236">7</span></span>

<span data-ttu-id="cb188-2237">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2237">8</span></span>

<span data-ttu-id="cb188-2238">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2238">9</span></span>

<span data-ttu-id="cb188-2239">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2239">2</span></span><br/> <span data-ttu-id="cb188-2240">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2240">0</span></span><br/>

<span data-ttu-id="cb188-2241">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2241">1</span></span>

<span data-ttu-id="cb188-2242">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2242">2</span></span>

<span data-ttu-id="cb188-2243">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2243">3</span></span>

<span data-ttu-id="cb188-2244">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2244">4</span></span>

<span data-ttu-id="cb188-2245">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2245">5</span></span>

<span data-ttu-id="cb188-2246">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2246">6</span></span>

<span data-ttu-id="cb188-2247">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2247">7</span></span>

<span data-ttu-id="cb188-2248">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2248">8</span></span>

<span data-ttu-id="cb188-2249">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2249">9</span></span>

<span data-ttu-id="cb188-2250">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2250">3</span></span><br/> <span data-ttu-id="cb188-2251">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2251">0</span></span><br/>

<span data-ttu-id="cb188-2252">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2252">1</span></span>

<span data-ttu-id="cb188-2253">\_area hRegion</span><span class="sxs-lookup"><span data-stu-id="cb188-2253">\_hRegion</span></span>

<span data-ttu-id="cb188-2254">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="cb188-2254">\_cBookmarks</span></span>

<span data-ttu-id="cb188-2255">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="cb188-2255">\_maxRet</span></span>

<span data-ttu-id="cb188-2256">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="cb188-2256">\_cValidRet</span></span>

<span data-ttu-id="cb188-2257">\_aBookmarks (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="cb188-2258">\_ascRet (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="cb188-2259">**\_ hRegion:** deve essere impostato su 0x00000000 e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cb188-2260">**\_ cBookmarks:** intero senza segno a 32 bit che rappresenta il numero di elementi in \_ una matriceBookmarks.</span><span class="sxs-lookup"><span data-stu-id="cb188-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="cb188-2261">**\_ maxRet:** intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice ascRet.</span><span class="sxs-lookup"><span data-stu-id="cb188-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="cb188-2262">**\_ cValidRet:** intero senza segno a 32 bit che rappresenta il numero di elementi validi nella \_ matrice ascRet.</span><span class="sxs-lookup"><span data-stu-id="cb188-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="cb188-2263">Gli elementi validi sono stati definiti nella matrice, mentre gli elementi non validi non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="cb188-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="cb188-2264">**\_ aBookmarks:** matrice di handle di segnalibro (ognuno rappresentato da 4 byte), ottenuto da un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="cb188-2265">**\_ ascRet:** matrice di valori HRESULT.</span><span class="sxs-lookup"><span data-stu-id="cb188-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="cb188-2266">Quando CRowSeekByBookMark viene inviato come parte della richiesta CPMGetRowsIn, il numero di voci nella matrice DEVE essere uguale a \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="cb188-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="cb188-2267">Quando vengono inviati dal client, i valori DEVONO essere impostati su zero e il server DEVE ignorare il contenuto della matrice.</span><span class="sxs-lookup"><span data-stu-id="cb188-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="cb188-2268">Quando vengono inviati dal server (come parte del messaggio CPMGetRowsOut), i valori nella matrice indicano lo stato del risultato per ogni recupero di riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="cb188-2269">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="cb188-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="cb188-2270">La struttura CRowSeekNext contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cb188-2271">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2271">0</span></span>

<span data-ttu-id="cb188-2272">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2272">1</span></span>

<span data-ttu-id="cb188-2273">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2273">2</span></span>

<span data-ttu-id="cb188-2274">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2274">3</span></span>

<span data-ttu-id="cb188-2275">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2275">4</span></span>

<span data-ttu-id="cb188-2276">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2276">5</span></span>

<span data-ttu-id="cb188-2277">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2277">6</span></span>

<span data-ttu-id="cb188-2278">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2278">7</span></span>

<span data-ttu-id="cb188-2279">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2279">8</span></span>

<span data-ttu-id="cb188-2280">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2280">9</span></span>

<span data-ttu-id="cb188-2281">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2281">1</span></span><br/> <span data-ttu-id="cb188-2282">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2282">0</span></span><br/>

<span data-ttu-id="cb188-2283">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2283">1</span></span>

<span data-ttu-id="cb188-2284">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2284">2</span></span>

<span data-ttu-id="cb188-2285">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2285">3</span></span>

<span data-ttu-id="cb188-2286">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2286">4</span></span>

<span data-ttu-id="cb188-2287">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2287">5</span></span>

<span data-ttu-id="cb188-2288">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2288">6</span></span>

<span data-ttu-id="cb188-2289">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2289">7</span></span>

<span data-ttu-id="cb188-2290">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2290">8</span></span>

<span data-ttu-id="cb188-2291">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2291">9</span></span>

<span data-ttu-id="cb188-2292">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2292">2</span></span><br/> <span data-ttu-id="cb188-2293">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2293">0</span></span><br/>

<span data-ttu-id="cb188-2294">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2294">1</span></span>

<span data-ttu-id="cb188-2295">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2295">2</span></span>

<span data-ttu-id="cb188-2296">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2296">3</span></span>

<span data-ttu-id="cb188-2297">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2297">4</span></span>

<span data-ttu-id="cb188-2298">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2298">5</span></span>

<span data-ttu-id="cb188-2299">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2299">6</span></span>

<span data-ttu-id="cb188-2300">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2300">7</span></span>

<span data-ttu-id="cb188-2301">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2301">8</span></span>

<span data-ttu-id="cb188-2302">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2302">9</span></span>

<span data-ttu-id="cb188-2303">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2303">3</span></span><br/> <span data-ttu-id="cb188-2304">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2304">0</span></span><br/>

<span data-ttu-id="cb188-2305">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2305">1</span></span>

<span data-ttu-id="cb188-2306">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="cb188-2306">CiTblChapt</span></span>

<span data-ttu-id="cb188-2307">\_area hRegion</span><span class="sxs-lookup"><span data-stu-id="cb188-2307">\_hRegion</span></span>

<span data-ttu-id="cb188-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="cb188-2308">\_cskip</span></span>



 

<span data-ttu-id="cb188-2309">**CiTblChapt:** intero senza segno a 32 bit che specifica il capitolo del set di righe da cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="cb188-2310">**\_ hRegion:** DEVE essere impostato su 0x00000000 e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cb188-2311">**\_ cskip:** intero senza segno a 32 bit che rappresenta il numero di righe da ignorare nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="cb188-2312">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="cb188-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="cb188-2313">La struttura CRowsetProperties contiene informazioni di configurazione per una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="cb188-2314">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2314">0</span></span>

<span data-ttu-id="cb188-2315">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2315">1</span></span>

<span data-ttu-id="cb188-2316">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2316">2</span></span>

<span data-ttu-id="cb188-2317">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2317">3</span></span>

<span data-ttu-id="cb188-2318">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2318">4</span></span>

<span data-ttu-id="cb188-2319">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2319">5</span></span>

<span data-ttu-id="cb188-2320">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2320">6</span></span>

<span data-ttu-id="cb188-2321">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2321">7</span></span>

<span data-ttu-id="cb188-2322">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2322">8</span></span>

<span data-ttu-id="cb188-2323">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2323">9</span></span>

<span data-ttu-id="cb188-2324">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2324">1</span></span><br/> <span data-ttu-id="cb188-2325">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2325">0</span></span><br/>

<span data-ttu-id="cb188-2326">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2326">1</span></span>

<span data-ttu-id="cb188-2327">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2327">2</span></span>

<span data-ttu-id="cb188-2328">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2328">3</span></span>

<span data-ttu-id="cb188-2329">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2329">4</span></span>

<span data-ttu-id="cb188-2330">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2330">5</span></span>

<span data-ttu-id="cb188-2331">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2331">6</span></span>

<span data-ttu-id="cb188-2332">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2332">7</span></span>

<span data-ttu-id="cb188-2333">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2333">8</span></span>

<span data-ttu-id="cb188-2334">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2334">9</span></span>

<span data-ttu-id="cb188-2335">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2335">2</span></span><br/> <span data-ttu-id="cb188-2336">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2336">0</span></span><br/>

<span data-ttu-id="cb188-2337">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2337">1</span></span>

<span data-ttu-id="cb188-2338">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2338">2</span></span>

<span data-ttu-id="cb188-2339">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2339">3</span></span>

<span data-ttu-id="cb188-2340">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2340">4</span></span>

<span data-ttu-id="cb188-2341">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2341">5</span></span>

<span data-ttu-id="cb188-2342">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2342">6</span></span>

<span data-ttu-id="cb188-2343">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2343">7</span></span>

<span data-ttu-id="cb188-2344">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2344">8</span></span>

<span data-ttu-id="cb188-2345">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2345">9</span></span>

<span data-ttu-id="cb188-2346">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2346">3</span></span><br/> <span data-ttu-id="cb188-2347">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2347">0</span></span><br/>

<span data-ttu-id="cb188-2348">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2348">1</span></span>

<span data-ttu-id="cb188-2349">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="cb188-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="cb188-2350">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="cb188-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="cb188-2351">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="cb188-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="cb188-2352">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="cb188-2352">\_cMaxResults</span></span>

<span data-ttu-id="cb188-2353">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="cb188-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="cb188-2354">**\_ uBooleanOptions:** i 3 bit meno significativi di questo campo DEVONO contenere uno dei tre valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="cb188-2355">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-2355">Value</span></span>                  | <span data-ttu-id="cb188-2356">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cb188-2357">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="cb188-2358">Il cursore può essere spostato solo in avanti.</span><span class="sxs-lookup"><span data-stu-id="cb188-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="cb188-2359">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="cb188-2360">Il cursore può essere spostato in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="cb188-2361">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb188-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="cb188-2362">Il cursore può essere spostato in qualsiasi posizione e recuperato in qualsiasi direzione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="cb188-2363">I bit rimanenti possono essere chiari o impostati su qualsiasi combinazione dei valori seguenti in modo logico OR'd insieme:</span><span class="sxs-lookup"><span data-stu-id="cb188-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="cb188-2364">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-2364">Value</span></span>                     | <span data-ttu-id="cb188-2365">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-2366">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb188-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="cb188-2367">Il client non attenderà il completamento dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="cb188-2368">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cb188-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="cb188-2369">Restituisce le prime righe incontrate, non le corrispondenze migliori.</span><span class="sxs-lookup"><span data-stu-id="cb188-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="cb188-2370">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cb188-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="cb188-2371">Il server NON DEVE eliminare le righe fino a quando il client non viene eseguito con una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="cb188-2372">EChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="cb188-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="cb188-2373">Il set di righe supporta i capitoli.</span><span class="sxs-lookup"><span data-stu-id="cb188-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="cb188-2374">EUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="cb188-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="cb188-2375">Rispondere solo alla query dall'indice, non dal file system.</span><span class="sxs-lookup"><span data-stu-id="cb188-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="cb188-2376">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="cb188-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="cb188-2377">Il servizio di indicizzazione deve prendere in considerazione l'ottimizzazione del tempo di risposta al client durante l'esecuzione della rimozione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="cb188-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="cb188-2378">**\_ ulMaxOpenRows:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="cb188-2379">Deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="cb188-2380">Non usato e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="cb188-2381">**\_ ulMemoryUsage:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="cb188-2382">Deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="cb188-2383">Non usato e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="cb188-2384">**\_ cMaxResults:** intero senza segno a 32 bit che specifica il numero massimo di righe da restituire per la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="cb188-2385">**\_ cCmdTimeout:** intero senza segno a 32 bit che specifica il numero di secondi durante i quali una query deve timeout e terminare automaticamente, contando dal momento in cui la query inizia l'esecuzione nel server.</span><span class="sxs-lookup"><span data-stu-id="cb188-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="cb188-2386">Il valore 0x00000000 indica che la query non deve avere un timeout.</span><span class="sxs-lookup"><span data-stu-id="cb188-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="cb188-2387">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="cb188-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="cb188-2388">La struttura CRowVariant contiene la parte di dimensioni fisse di un tipo di dati a lunghezza variabile archiviata nel messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="cb188-2389">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2389">0</span></span>

<span data-ttu-id="cb188-2390">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2390">1</span></span>

<span data-ttu-id="cb188-2391">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2391">2</span></span>

<span data-ttu-id="cb188-2392">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2392">3</span></span>

<span data-ttu-id="cb188-2393">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2393">4</span></span>

<span data-ttu-id="cb188-2394">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2394">5</span></span>

<span data-ttu-id="cb188-2395">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2395">6</span></span>

<span data-ttu-id="cb188-2396">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2396">7</span></span>

<span data-ttu-id="cb188-2397">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2397">8</span></span>

<span data-ttu-id="cb188-2398">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2398">9</span></span>

<span data-ttu-id="cb188-2399">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2399">1</span></span><br/> <span data-ttu-id="cb188-2400">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2400">0</span></span><br/>

<span data-ttu-id="cb188-2401">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2401">1</span></span>

<span data-ttu-id="cb188-2402">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2402">2</span></span>

<span data-ttu-id="cb188-2403">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2403">3</span></span>

<span data-ttu-id="cb188-2404">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2404">4</span></span>

<span data-ttu-id="cb188-2405">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2405">5</span></span>

<span data-ttu-id="cb188-2406">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2406">6</span></span>

<span data-ttu-id="cb188-2407">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2407">7</span></span>

<span data-ttu-id="cb188-2408">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2408">8</span></span>

<span data-ttu-id="cb188-2409">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2409">9</span></span>

<span data-ttu-id="cb188-2410">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2410">2</span></span><br/> <span data-ttu-id="cb188-2411">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2411">0</span></span><br/>

<span data-ttu-id="cb188-2412">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2412">1</span></span>

<span data-ttu-id="cb188-2413">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2413">2</span></span>

<span data-ttu-id="cb188-2414">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2414">3</span></span>

<span data-ttu-id="cb188-2415">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2415">4</span></span>

<span data-ttu-id="cb188-2416">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2416">5</span></span>

<span data-ttu-id="cb188-2417">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2417">6</span></span>

<span data-ttu-id="cb188-2418">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2418">7</span></span>

<span data-ttu-id="cb188-2419">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2419">8</span></span>

<span data-ttu-id="cb188-2420">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2420">9</span></span>

<span data-ttu-id="cb188-2421">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2421">3</span></span><br/> <span data-ttu-id="cb188-2422">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2422">0</span></span><br/>

<span data-ttu-id="cb188-2423">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2423">1</span></span>

<span data-ttu-id="cb188-2424">vType</span><span class="sxs-lookup"><span data-stu-id="cb188-2424">vType</span></span>

<span data-ttu-id="cb188-2425">reserved1</span><span class="sxs-lookup"><span data-stu-id="cb188-2425">reserved1</span></span>

<span data-ttu-id="cb188-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="cb188-2426">reserved2</span></span>

<span data-ttu-id="cb188-2427">Offset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2427">Offset (optional)</span></span>



 

<span data-ttu-id="cb188-2428">**vType:** indicatore di tipo che indica il tipo di vValue.</span><span class="sxs-lookup"><span data-stu-id="cb188-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="cb188-2429">DEVE essere uno dei valori VARENUM specificati nella sezione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="cb188-2430">**reserved1:** non usato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="cb188-2431">Il valore può essere impostato su qualsiasi valore arbitrario e deve essere ignorato alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="cb188-2432">**reserved2:** non usato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="cb188-2433">Il valore può essere impostato su qualsiasi valore arbitrario e deve essere ignorato alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="cb188-2434">**Offset**: offset per i dati a lunghezza variabile (ad esempio, una stringa).</span><span class="sxs-lookup"><span data-stu-id="cb188-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="cb188-2435">DEVE essere un valore a 32 bit (4 byte) se vengono usati offset a 32 bit (in base alle regole nella sezione 2.2.3.16) o un valore a 64 byte (lunghezza 8 byte) se vengono usati offset a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="cb188-2436">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="cb188-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="cb188-2437">La struttura CSortSet contiene l'ordinamento della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="cb188-2438">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2438">0</span></span>

<span data-ttu-id="cb188-2439">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2439">1</span></span>

<span data-ttu-id="cb188-2440">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2440">2</span></span>

<span data-ttu-id="cb188-2441">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2441">3</span></span>

<span data-ttu-id="cb188-2442">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2442">4</span></span>

<span data-ttu-id="cb188-2443">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2443">5</span></span>

<span data-ttu-id="cb188-2444">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2444">6</span></span>

<span data-ttu-id="cb188-2445">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2445">7</span></span>

<span data-ttu-id="cb188-2446">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2446">8</span></span>

<span data-ttu-id="cb188-2447">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2447">9</span></span>

<span data-ttu-id="cb188-2448">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2448">1</span></span><br/> <span data-ttu-id="cb188-2449">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2449">0</span></span><br/>

<span data-ttu-id="cb188-2450">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2450">1</span></span>

<span data-ttu-id="cb188-2451">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2451">2</span></span>

<span data-ttu-id="cb188-2452">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2452">3</span></span>

<span data-ttu-id="cb188-2453">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2453">4</span></span>

<span data-ttu-id="cb188-2454">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2454">5</span></span>

<span data-ttu-id="cb188-2455">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2455">6</span></span>

<span data-ttu-id="cb188-2456">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2456">7</span></span>

<span data-ttu-id="cb188-2457">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2457">8</span></span>

<span data-ttu-id="cb188-2458">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2458">9</span></span>

<span data-ttu-id="cb188-2459">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2459">2</span></span><br/> <span data-ttu-id="cb188-2460">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2460">0</span></span><br/>

<span data-ttu-id="cb188-2461">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2461">1</span></span>

<span data-ttu-id="cb188-2462">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2462">2</span></span>

<span data-ttu-id="cb188-2463">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2463">3</span></span>

<span data-ttu-id="cb188-2464">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2464">4</span></span>

<span data-ttu-id="cb188-2465">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2465">5</span></span>

<span data-ttu-id="cb188-2466">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2466">6</span></span>

<span data-ttu-id="cb188-2467">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2467">7</span></span>

<span data-ttu-id="cb188-2468">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2468">8</span></span>

<span data-ttu-id="cb188-2469">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2469">9</span></span>

<span data-ttu-id="cb188-2470">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2470">3</span></span><br/> <span data-ttu-id="cb188-2471">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2471">0</span></span><br/>

<span data-ttu-id="cb188-2472">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2472">1</span></span>

<span data-ttu-id="cb188-2473">Conteggio</span><span class="sxs-lookup"><span data-stu-id="cb188-2473">Count</span></span>

<span data-ttu-id="cb188-2474">sortArray (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="cb188-2475">**count:** intero senza segno a 32 bit che specifica il numero di elementi in sortArray.</span><span class="sxs-lookup"><span data-stu-id="cb188-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="cb188-2476">**sortArray:** matrice di strutture CSort che descrive l'ordine in cui ordinare i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="cb188-2477">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura abbia un allineamento a 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cb188-2478">Tali byte di spaziatura interna possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="cb188-2479">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="cb188-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="cb188-2480">La struttura CTableColumn contiene una colonna di un messaggio CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="cb188-2481">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2481">0</span></span>

<span data-ttu-id="cb188-2482">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2482">1</span></span>

<span data-ttu-id="cb188-2483">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2483">2</span></span>

<span data-ttu-id="cb188-2484">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2484">3</span></span>

<span data-ttu-id="cb188-2485">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2485">4</span></span>

<span data-ttu-id="cb188-2486">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2486">5</span></span>

<span data-ttu-id="cb188-2487">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2487">6</span></span>

<span data-ttu-id="cb188-2488">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2488">7</span></span>

<span data-ttu-id="cb188-2489">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2489">8</span></span>

<span data-ttu-id="cb188-2490">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2490">9</span></span>

<span data-ttu-id="cb188-2491">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2491">1</span></span><br/> <span data-ttu-id="cb188-2492">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2492">0</span></span><br/>

<span data-ttu-id="cb188-2493">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2493">1</span></span>

<span data-ttu-id="cb188-2494">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2494">2</span></span>

<span data-ttu-id="cb188-2495">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2495">3</span></span>

<span data-ttu-id="cb188-2496">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2496">4</span></span>

<span data-ttu-id="cb188-2497">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2497">5</span></span>

<span data-ttu-id="cb188-2498">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2498">6</span></span>

<span data-ttu-id="cb188-2499">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2499">7</span></span>

<span data-ttu-id="cb188-2500">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2500">8</span></span>

<span data-ttu-id="cb188-2501">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2501">9</span></span>

<span data-ttu-id="cb188-2502">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2502">2</span></span><br/> <span data-ttu-id="cb188-2503">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2503">0</span></span><br/>

<span data-ttu-id="cb188-2504">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2504">1</span></span>

<span data-ttu-id="cb188-2505">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2505">2</span></span>

<span data-ttu-id="cb188-2506">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2506">3</span></span>

<span data-ttu-id="cb188-2507">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2507">4</span></span>

<span data-ttu-id="cb188-2508">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2508">5</span></span>

<span data-ttu-id="cb188-2509">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2509">6</span></span>

<span data-ttu-id="cb188-2510">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2510">7</span></span>

<span data-ttu-id="cb188-2511">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2511">8</span></span>

<span data-ttu-id="cb188-2512">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2512">9</span></span>

<span data-ttu-id="cb188-2513">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2513">3</span></span><br/> <span data-ttu-id="cb188-2514">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2514">0</span></span><br/>

<span data-ttu-id="cb188-2515">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2515">1</span></span>

<span data-ttu-id="cb188-2516">PropSpec</span><span class="sxs-lookup"><span data-stu-id="cb188-2516">PropSpec</span></span>

<span data-ttu-id="cb188-2517">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-2517">...(variable)</span></span>

<span data-ttu-id="cb188-2518">vType</span><span class="sxs-lookup"><span data-stu-id="cb188-2518">vType</span></span>

<span data-ttu-id="cb188-2519">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="cb188-2519">ValueUsed</span></span>

<span data-ttu-id="cb188-2520">\_padding1 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="cb188-2521">ValueOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="cb188-2522">ValueSize (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2522">ValueSize (optional)</span></span>

<span data-ttu-id="cb188-2523">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="cb188-2523">StatusUsed</span></span>

<span data-ttu-id="cb188-2524">\_padding2 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="cb188-2525">StatusOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="cb188-2526">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="cb188-2526">LengthUsed</span></span>

<span data-ttu-id="cb188-2527">\_padding3 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="cb188-2528">LengthOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="cb188-2529">**PropSpec:** struttura CFullPropSpec come specificato nella sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="cb188-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="cb188-2530">**vType**: specifica il tipo di valore di dati contenuto nella colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="cb188-2531">Vedere il campo vType nella sezione 2.2.1.1 per l'elenco dei valori per questo campo.</span><span class="sxs-lookup"><span data-stu-id="cb188-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="cb188-2532">**ValueUsed:** campo a un byte che deve essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cb188-2533">Se impostato su 0x01, la colonna viene trasferita all'interno della riga a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="cb188-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="cb188-2534">Se impostato su 0x00, il valore della colonna viene trasferito nella sezione a lunghezza variabile alla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="cb188-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="cb188-2535">**\_ padding1:** campo di un byte che DEVE essere inserito prima di ValueOffset se, senza di esso, ValueOffset non inizia a un offset pari dall'inizio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="cb188-2536">Il valore di questo byte è arbitrario e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cb188-2537">Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cb188-2538">**ValueOffset:** intero senza segno a 2 byte che specifica l'offset del valore della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="cb188-2539">Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cb188-2540">**ValueSize:** intero senza segno a 2 byte che specifica le dimensioni in byte del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="cb188-2541">Se ValueUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cb188-2542">**StatusUsed:** campo di un byte che DEVE essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cb188-2543">Se impostato su 0x01, lo stato della colonna viene trasferito all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="cb188-2544">Se 0x00, lo stato della colonna non viene trasferito all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="cb188-2545">**\_ padding2:** campo di un byte che DEVE essere inserito prima di StatusOffset se, senza di esso, il campo StatusOffset non inizia in corrispondenza di un offset pari dall'inizio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="cb188-2546">Il valore di questo byte è arbitrario e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cb188-2547">Se StatusUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cb188-2548">**StatusOffset:** intero senza segno a 2 byte che specifica l'offset dello stato della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="cb188-2549">Se StatusUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cb188-2550">**LengthUsed:** campo di un byte che DEVE essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cb188-2551">Se impostato su 0x01, la lunghezza della colonna viene trasferita all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="cb188-2552">Se 0x00, la lunghezza della colonna NON DEVE essere trasferita all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="cb188-2553">**\_ padding3:** campo di un byte che DEVE essere inserito prima di LengthOffset se, senza di esso, LengthOffset non inizia a un offset pari dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="cb188-2554">Il valore di questo byte è arbitrario e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cb188-2555">Se LengthUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cb188-2556">**LengthOffset:** intero senza segno a 2 byte che specifica l'offset della lunghezza della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="cb188-2557">Se LengthUsed è impostato su 0x00, questo campo NON DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="cb188-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="cb188-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="cb188-2559">La struttura SERIALIZEDPROPERTYVALUE contiene un valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="cb188-2560">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2560">0</span></span>

<span data-ttu-id="cb188-2561">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2561">1</span></span>

<span data-ttu-id="cb188-2562">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2562">2</span></span>

<span data-ttu-id="cb188-2563">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2563">3</span></span>

<span data-ttu-id="cb188-2564">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2564">4</span></span>

<span data-ttu-id="cb188-2565">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2565">5</span></span>

<span data-ttu-id="cb188-2566">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2566">6</span></span>

<span data-ttu-id="cb188-2567">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2567">7</span></span>

<span data-ttu-id="cb188-2568">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2568">8</span></span>

<span data-ttu-id="cb188-2569">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2569">9</span></span>

<span data-ttu-id="cb188-2570">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2570">1</span></span><br/> <span data-ttu-id="cb188-2571">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2571">0</span></span><br/>

<span data-ttu-id="cb188-2572">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2572">1</span></span>

<span data-ttu-id="cb188-2573">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2573">2</span></span>

<span data-ttu-id="cb188-2574">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2574">3</span></span>

<span data-ttu-id="cb188-2575">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2575">4</span></span>

<span data-ttu-id="cb188-2576">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2576">5</span></span>

<span data-ttu-id="cb188-2577">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2577">6</span></span>

<span data-ttu-id="cb188-2578">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2578">7</span></span>

<span data-ttu-id="cb188-2579">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2579">8</span></span>

<span data-ttu-id="cb188-2580">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2580">9</span></span>

<span data-ttu-id="cb188-2581">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2581">2</span></span><br/> <span data-ttu-id="cb188-2582">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2582">0</span></span><br/>

<span data-ttu-id="cb188-2583">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2583">1</span></span>

<span data-ttu-id="cb188-2584">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2584">2</span></span>

<span data-ttu-id="cb188-2585">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2585">3</span></span>

<span data-ttu-id="cb188-2586">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2586">4</span></span>

<span data-ttu-id="cb188-2587">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2587">5</span></span>

<span data-ttu-id="cb188-2588">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2588">6</span></span>

<span data-ttu-id="cb188-2589">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2589">7</span></span>

<span data-ttu-id="cb188-2590">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2590">8</span></span>

<span data-ttu-id="cb188-2591">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2591">9</span></span>

<span data-ttu-id="cb188-2592">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2592">3</span></span><br/> <span data-ttu-id="cb188-2593">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2593">0</span></span><br/>

<span data-ttu-id="cb188-2594">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2594">1</span></span>

<span data-ttu-id="cb188-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="cb188-2595">dwType</span></span>

<span data-ttu-id="cb188-2596">rgb (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-2596">rgb (variable)</span></span>



 

<span data-ttu-id="cb188-2597">**dwType:** uno dei tipi variant, definito nella sezione 2.2.1.1, che può essere combinato con modificatori di tipo variant.</span><span class="sxs-lookup"><span data-stu-id="cb188-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="cb188-2598">Per tutti i tipi variant, ad eccezione di quelli combinati con VT ARRAY, SERIALIZEDPROPERTYVALUE ha lo stesso layout di CBaseStorageVariant, come specificato nella sezione \_ 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="cb188-2599">Se il tipo variant viene combinato con il modificatore di tipo VT ARRAY, viene usato SAFEARRAY2, specificato nella sezione \_ 2.2.1.2.1.1, anziché SAFEARRAY nel campo vValue di CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cb188-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="cb188-2600">**rgb:** valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="cb188-2601">Vedere i dettagli della serializzazione per vValue nella versione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="cb188-2602">2.2.2 Intestazioni dei messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="cb188-2603">Tutti i messaggi content indexing service protocol hanno un'intestazione di 16 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="cb188-2604">Di seguito è riportato un diagramma che mostra il formato di intestazione del messaggio Content Indexing Service Protocol.</span><span class="sxs-lookup"><span data-stu-id="cb188-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="cb188-2605">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2605">0</span></span>

<span data-ttu-id="cb188-2606">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2606">1</span></span>

<span data-ttu-id="cb188-2607">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2607">2</span></span>

<span data-ttu-id="cb188-2608">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2608">3</span></span>

<span data-ttu-id="cb188-2609">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2609">4</span></span>

<span data-ttu-id="cb188-2610">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2610">5</span></span>

<span data-ttu-id="cb188-2611">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2611">6</span></span>

<span data-ttu-id="cb188-2612">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2612">7</span></span>

<span data-ttu-id="cb188-2613">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2613">8</span></span>

<span data-ttu-id="cb188-2614">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2614">9</span></span>

<span data-ttu-id="cb188-2615">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2615">1</span></span><br/> <span data-ttu-id="cb188-2616">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2616">0</span></span><br/>

<span data-ttu-id="cb188-2617">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2617">1</span></span>

<span data-ttu-id="cb188-2618">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2618">2</span></span>

<span data-ttu-id="cb188-2619">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2619">3</span></span>

<span data-ttu-id="cb188-2620">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2620">4</span></span>

<span data-ttu-id="cb188-2621">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2621">5</span></span>

<span data-ttu-id="cb188-2622">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2622">6</span></span>

<span data-ttu-id="cb188-2623">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2623">7</span></span>

<span data-ttu-id="cb188-2624">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2624">8</span></span>

<span data-ttu-id="cb188-2625">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2625">9</span></span>

<span data-ttu-id="cb188-2626">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2626">2</span></span><br/> <span data-ttu-id="cb188-2627">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2627">0</span></span><br/>

<span data-ttu-id="cb188-2628">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2628">1</span></span>

<span data-ttu-id="cb188-2629">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2629">2</span></span>

<span data-ttu-id="cb188-2630">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2630">3</span></span>

<span data-ttu-id="cb188-2631">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2631">4</span></span>

<span data-ttu-id="cb188-2632">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2632">5</span></span>

<span data-ttu-id="cb188-2633">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2633">6</span></span>

<span data-ttu-id="cb188-2634">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2634">7</span></span>

<span data-ttu-id="cb188-2635">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2635">8</span></span>

<span data-ttu-id="cb188-2636">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2636">9</span></span>

<span data-ttu-id="cb188-2637">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2637">3</span></span><br/> <span data-ttu-id="cb188-2638">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2638">0</span></span><br/>

<span data-ttu-id="cb188-2639">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2639">1</span></span>

<span data-ttu-id="cb188-2640">\_Msg</span><span class="sxs-lookup"><span data-stu-id="cb188-2640">\_msg</span></span>

<span data-ttu-id="cb188-2641">\_Stato</span><span class="sxs-lookup"><span data-stu-id="cb188-2641">\_status</span></span>

<span data-ttu-id="cb188-2642">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="cb188-2642">\_ulChecksum</span></span>

<span data-ttu-id="cb188-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="cb188-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="cb188-2644">\_**msg:** intero a 32 bit che identifica il tipo di messaggio dopo l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="cb188-2645">Nella tabella seguente sono elencati i messaggi del protocollo del servizio di indicizzazione del contenuto e i valori interi specificati per ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="cb188-2646">Come illustrato nella tabella, alcuni valori identificano 2 messaggi nella tabella.</span><span class="sxs-lookup"><span data-stu-id="cb188-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="cb188-2647">In questi casi il messaggio che segue l'intestazione può essere identificato dalla direzione del flusso del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="cb188-2648">Se la direzione è da client a server, viene indicato il messaggio con "In" aggiunto al nome del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="cb188-2649">Se la direzione è da server a client, viene indicato il messaggio con "Out" aggiunto al nome del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="cb188-2650">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-2650">Value</span></span>      | <span data-ttu-id="cb188-2651">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="cb188-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="cb188-2652">0x000000C8</span></span> | <span data-ttu-id="cb188-2653">CPMConnectIn o CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="cb188-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="cb188-2654">0x000000C9</span></span> | <span data-ttu-id="cb188-2655">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cb188-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="cb188-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="cb188-2656">0x000000CA</span></span> | <span data-ttu-id="cb188-2657">CPMCreateQueryIn o CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="cb188-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="cb188-2658">0x000000CB</span></span> | <span data-ttu-id="cb188-2659">CPMFreeCursorIn o CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="cb188-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="cb188-2660">0x000000CC</span></span> | <span data-ttu-id="cb188-2661">CPMGetRowsIn o CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="cb188-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="cb188-2662">0x000000CD</span></span> | <span data-ttu-id="cb188-2663">CPMRatioFinishedIn o CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="cb188-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="cb188-2664">0x000000CE</span></span> | <span data-ttu-id="cb188-2665">CPMCompareBmkIn o CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="cb188-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="cb188-2666">0x000000CF</span></span> | <span data-ttu-id="cb188-2667">CPMGetApproximatePositionIn o CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="cb188-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="cb188-2668">0x000000D0</span></span> | <span data-ttu-id="cb188-2669">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="cb188-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="cb188-2670">0x000000D1</span></span> | <span data-ttu-id="cb188-2671">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="cb188-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="cb188-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="cb188-2672">0x000000D2</span></span> | <span data-ttu-id="cb188-2673">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="cb188-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="cb188-2674">0x000000D7</span></span> | <span data-ttu-id="cb188-2675">CPMGetQueryStatusIn o CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="cb188-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="cb188-2676">0x000000D9</span></span> | <span data-ttu-id="cb188-2677">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="cb188-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="cb188-2678">0x000000E1</span></span> | <span data-ttu-id="cb188-2679">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="cb188-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="cb188-2680">0x000000E4</span></span> | <span data-ttu-id="cb188-2681">CPMFetchValueIn o CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="cb188-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="cb188-2682">0x000000E6</span></span> | <span data-ttu-id="cb188-2683">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="cb188-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="cb188-2684">0x000000E7</span></span> | <span data-ttu-id="cb188-2685">CPMGetQueryStatusExIn o PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="cb188-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="cb188-2686">0x000000E8</span></span> | <span data-ttu-id="cb188-2687">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="cb188-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="cb188-2688">0x000000E9</span></span> | <span data-ttu-id="cb188-2689">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="cb188-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="cb188-2690">0x000000EC</span></span> | <span data-ttu-id="cb188-2691">CPMSetCatStateIn o CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="cb188-2692">\_**status**: HRESULT \[ MS-SYS \] che indica lo stato dell'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="cb188-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="cb188-2693">*Comportamento di Windows: il client imposta sempre il \_ campo di stato su 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="cb188-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="cb188-2694">**\_ ulChecksum:** \_ ulChecksum MUST deve essere calcolato come specificato nella Sezione 3.2.4 per i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="cb188-2695">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="cb188-2696">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="cb188-2697">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="cb188-2698">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="cb188-2699">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="cb188-2700">Per tutti gli altri messaggi, \_ ulChecksum DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="cb188-2701">Un client DEVE ignorare il \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="cb188-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="cb188-2702">**\_ ulReserved2:** DEVE essere impostato su 0 e ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="cb188-2703">2.2.3 Messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="cb188-2704">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="cb188-2705">Il messaggio CPMCiStateInOut contiene informazioni sullo stato del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="cb188-2706">Il formato del messaggio CPMCiStateInOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-2707">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2707">0</span></span>

<span data-ttu-id="cb188-2708">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2708">1</span></span>

<span data-ttu-id="cb188-2709">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2709">2</span></span>

<span data-ttu-id="cb188-2710">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2710">3</span></span>

<span data-ttu-id="cb188-2711">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2711">4</span></span>

<span data-ttu-id="cb188-2712">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2712">5</span></span>

<span data-ttu-id="cb188-2713">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2713">6</span></span>

<span data-ttu-id="cb188-2714">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2714">7</span></span>

<span data-ttu-id="cb188-2715">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2715">8</span></span>

<span data-ttu-id="cb188-2716">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2716">9</span></span>

<span data-ttu-id="cb188-2717">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2717">1</span></span><br/> <span data-ttu-id="cb188-2718">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2718">0</span></span><br/>

<span data-ttu-id="cb188-2719">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2719">1</span></span>

<span data-ttu-id="cb188-2720">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2720">2</span></span>

<span data-ttu-id="cb188-2721">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2721">3</span></span>

<span data-ttu-id="cb188-2722">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2722">4</span></span>

<span data-ttu-id="cb188-2723">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2723">5</span></span>

<span data-ttu-id="cb188-2724">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2724">6</span></span>

<span data-ttu-id="cb188-2725">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2725">7</span></span>

<span data-ttu-id="cb188-2726">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2726">8</span></span>

<span data-ttu-id="cb188-2727">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2727">9</span></span>

<span data-ttu-id="cb188-2728">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2728">2</span></span><br/> <span data-ttu-id="cb188-2729">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2729">0</span></span><br/>

<span data-ttu-id="cb188-2730">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2730">1</span></span>

<span data-ttu-id="cb188-2731">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2731">2</span></span>

<span data-ttu-id="cb188-2732">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2732">3</span></span>

<span data-ttu-id="cb188-2733">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2733">4</span></span>

<span data-ttu-id="cb188-2734">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2734">5</span></span>

<span data-ttu-id="cb188-2735">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2735">6</span></span>

<span data-ttu-id="cb188-2736">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2736">7</span></span>

<span data-ttu-id="cb188-2737">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2737">8</span></span>

<span data-ttu-id="cb188-2738">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2738">9</span></span>

<span data-ttu-id="cb188-2739">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2739">3</span></span><br/> <span data-ttu-id="cb188-2740">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2740">0</span></span><br/>

<span data-ttu-id="cb188-2741">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2741">1</span></span>

<span data-ttu-id="cb188-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="cb188-2742">cbStruct</span></span>

<span data-ttu-id="cb188-2743">cWordList</span><span class="sxs-lookup"><span data-stu-id="cb188-2743">cWordList</span></span>

<span data-ttu-id="cb188-2744">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="cb188-2744">cPersistentIndex</span></span>

<span data-ttu-id="cb188-2745">cQueries</span><span class="sxs-lookup"><span data-stu-id="cb188-2745">cQueries</span></span>

<span data-ttu-id="cb188-2746">cDocuments</span><span class="sxs-lookup"><span data-stu-id="cb188-2746">cDocuments</span></span>

<span data-ttu-id="cb188-2747">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="cb188-2747">cFreshTest</span></span>

<span data-ttu-id="cb188-2748">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="cb188-2748">dwMergeProgress</span></span>

<span data-ttu-id="cb188-2749">Tenuta</span><span class="sxs-lookup"><span data-stu-id="cb188-2749">eState</span></span>

<span data-ttu-id="cb188-2750">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="cb188-2750">cFilteredDocuments</span></span>

<span data-ttu-id="cb188-2751">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="cb188-2751">cTotalDocuments</span></span>

<span data-ttu-id="cb188-2752">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="cb188-2752">cPendingScans</span></span>

<span data-ttu-id="cb188-2753">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="cb188-2753">dwIndexSize</span></span>

<span data-ttu-id="cb188-2754">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="cb188-2754">cUniqueKeys</span></span>

<span data-ttu-id="cb188-2755">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="cb188-2755">cSecQDocuments</span></span>

<span data-ttu-id="cb188-2756">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="cb188-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="cb188-2757">**cbStruct:** intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cb188-2758">Dimensione in byte di questo messaggio (esclusa l'intestazione comune).</span><span class="sxs-lookup"><span data-stu-id="cb188-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="cb188-2759">DEVE essere impostato su 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="cb188-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="cb188-2760">**cWordList:** intero senza segno a 32 bit che indica il conteggio degli indici iniziali creati per i documenti indicizzati di recente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="cb188-2761">**cPersistentIndex:** intero senza segno a 32 bit che indica il conteggio degli indici persistenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="cb188-2762">**cQueries:** intero senza segno a 32 bit che indica un numero di query in esecuzione attivamente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="cb188-2763">**cDocuments:** intero senza segno a 32 bit che indica il numero totale di documenti in attesa di essere indicizzati.</span><span class="sxs-lookup"><span data-stu-id="cb188-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="cb188-2764">**cFreshTest:** intero senza segno a 32 bit che indica il numero di documenti univoci con informazioni negli indici non completamente ottimizzate per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="cb188-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="cb188-2765">**dwMergeProgress:** intero senza segno a 32 bit che specifica la percentuale di completamento dell'ottimizzazione completa corrente degli indici, se l'ottimizzazione è attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="cb188-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="cb188-2766">DEVE essere minore o uguale a 100.</span><span class="sxs-lookup"><span data-stu-id="cb188-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="cb188-2767">**eState:** stato dell'indicizzazione del contenuto specificato da una o più costanti CI \_ \_ \* STATE, definite nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cb188-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="cb188-2768">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-2768">Value</span></span>                                         | <span data-ttu-id="cb188-2769">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-2770">UNIONE \_ CI STATE SHADOW \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="cb188-2771">Il servizio di indicizzazione sta ottimizzando alcuni indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="cb188-2772">CI \_ STATE MASTER MERGE \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="cb188-2773">Il servizio di indicizzazione è in corso di ottimizzazione completa per tutti gli indici.</span><span class="sxs-lookup"><span data-stu-id="cb188-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cb188-2774">CI \_ STATE CONTENT SCAN REQUIRED \_ \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="cb188-2775">Alcuni documenti nell'indice sono stati modificati e il servizio di indicizzazione deve determinare quali sono stati aggiunti, modificati o eliminati.</span><span class="sxs-lookup"><span data-stu-id="cb188-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cb188-2776">CI \_ STATE \_ ANNEALING \_ MERGE 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb188-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="cb188-2777">Il servizio di indicizzazione sta ottimizzando gli indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="cb188-2778">Questo processo è più completo di quello identificato dal valore CI STATE SHADOW MERGE, ma non è così completo come specificato dal \_ valore CI STATE MASTER \_ \_ \_ \_ \_ MERGE.</span><span class="sxs-lookup"><span data-stu-id="cb188-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="cb188-2779">Queste ottimizzazioni sono specifiche dell'implementazione in quanto dipendono dal modo in cui i dati vengono archiviati internamente. le ottimizzazioni non influiscono sul protocollo in alcun modo diverso dal tempo di risposta.</span><span class="sxs-lookup"><span data-stu-id="cb188-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="cb188-2780">ANALISI \_ DELLO STATO CI \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb188-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="cb188-2781">Il servizio di indicizzazione sta esaminando una directory o un set di directory per verificare se sono stati aggiunti, eliminati o aggiornati file dall'ultima indicizzazione della directory.</span><span class="sxs-lookup"><span data-stu-id="cb188-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cb188-2782">CI \_ STATE \_ RECOVERING 0x00000020</span><span class="sxs-lookup"><span data-stu-id="cb188-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="cb188-2783">Il servizio viene avviato dall'ultimo stato salvato ed è in corso il ripristino.</span><span class="sxs-lookup"><span data-stu-id="cb188-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cb188-2784">STATO CI \_ MEMORIA \_ INSUFFICIENTE \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cb188-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="cb188-2785">La maggior parte della memoria virtuale del server è in uso.</span><span class="sxs-lookup"><span data-stu-id="cb188-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cb188-2786">CI \_ STATE HIGH IO \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cb188-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="cb188-2787">Il livello di attività di input/output (I/O) nel server è relativamente elevato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="cb188-2788">CI \_ STATE MASTER MERGE \_ \_ \_ PAUSED 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cb188-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="cb188-2789">Il processo di ottimizzazione completa per tutti gli indici in corso è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="cb188-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="cb188-2790">Questo viene fornito solo a scopo informativo e non influisce sul CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cb188-2791">CI \_ STATE READ ONLY \_ \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="cb188-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="cb188-2792">La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="cb188-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="cb188-2793">Questo viene fornito solo a scopo informativo e non influisce sul CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="cb188-2794">CI \_ STATE BATTERY POWER \_ \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="cb188-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="cb188-2795">La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa per risparmiare la durata della batteria, ma risponde comunque alle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="cb188-2796">Questo viene fornito solo a scopo informativo e non influisce sul CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cb188-2797">CI \_ STATE USER ACTIVE \_ \_ 0x00001000</span><span class="sxs-lookup"><span data-stu-id="cb188-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="cb188-2798">La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa a causa dell'elevata attività dell'utente (tastiera o mouse), ma risponde comunque alle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="cb188-2799">Questo viene fornito solo a scopo informativo e non influisce sul CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="cb188-2800">CI \_ STATE \_ STARTING 0x00002000</span><span class="sxs-lookup"><span data-stu-id="cb188-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="cb188-2801">Il servizio è in fase di avvio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2801">The service is starting.</span></span> <span data-ttu-id="cb188-2802">Le query possono essere eseguite, ma l'analisi e la notifica non sono ancora state abilitate.</span><span class="sxs-lookup"><span data-stu-id="cb188-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="cb188-2803">Questo viene fornito solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cb188-2804">CI \_ STATE \_ READING \_ USNS 0x00004000</span><span class="sxs-lookup"><span data-stu-id="cb188-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="cb188-2805">Il servizio non ha letto il log mantenuto dal file system per tenere traccia delle modifiche apportate a file o directory in un volume, pertanto l'indice potrebbe non essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="cb188-2806">**cFilteredDocuments:** intero senza segno a 32 bit che indica il numero di documenti indicizzati dall'inizio dell'indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="cb188-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="cb188-2807">**cTotalDocuments:** intero senza segno a 32 bit che indica il numero totale di documenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="cb188-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="cb188-2808">**cPendingScans:** intero senza segno a 32 bit che indica il numero di operazioni di indicizzazione di alto livello in sospeso.</span><span class="sxs-lookup"><span data-stu-id="cb188-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="cb188-2809">Il significato di questo valore è specifico del provider, ma è previsto che numeri più grandi indichino una maggiore quantità di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="cb188-2810">*Comportamento di Windows:* questo valore è in genere zero, tranne immediatamente dopo l'avvio dell'indicizzazione o dopo l'overflow di una coda di notifica.</span><span class="sxs-lookup"><span data-stu-id="cb188-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="cb188-2811">**dwIndexSize:** intero senza segno a 32 bit che indica le dimensioni, in megabyte, dell'indice (esclusa la cache delle proprietà).</span><span class="sxs-lookup"><span data-stu-id="cb188-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="cb188-2812">**cUniqueKeys:** intero senza segno a 32 bit che indica il numero approssimativo di chiavi univoche nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="cb188-2813">**cSecQDocuments:** intero senza segno a 32 bit che indica il numero di documenti che il servizio di indicizzazione tenterà nuovamente di indicizzare a causa di un errore durante il tentativo iniziale di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="cb188-2814">**dwPropCacheSize:** intero senza segno a 32 bit che indica le dimensioni, in megabyte, della cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="cb188-2815">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="cb188-2816">Il messaggio CPMSetCatStateIn imposta lo stato di un catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="cb188-2817">Il formato del messaggio CPMSetCatStateIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-2818">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2818">0</span></span>

<span data-ttu-id="cb188-2819">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2819">1</span></span>

<span data-ttu-id="cb188-2820">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2820">2</span></span>

<span data-ttu-id="cb188-2821">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2821">3</span></span>

<span data-ttu-id="cb188-2822">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2822">4</span></span>

<span data-ttu-id="cb188-2823">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2823">5</span></span>

<span data-ttu-id="cb188-2824">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2824">6</span></span>

<span data-ttu-id="cb188-2825">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2825">7</span></span>

<span data-ttu-id="cb188-2826">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2826">8</span></span>

<span data-ttu-id="cb188-2827">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2827">9</span></span>

<span data-ttu-id="cb188-2828">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2828">1</span></span><br/> <span data-ttu-id="cb188-2829">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2829">0</span></span><br/>

<span data-ttu-id="cb188-2830">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2830">1</span></span>

<span data-ttu-id="cb188-2831">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2831">2</span></span>

<span data-ttu-id="cb188-2832">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2832">3</span></span>

<span data-ttu-id="cb188-2833">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2833">4</span></span>

<span data-ttu-id="cb188-2834">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2834">5</span></span>

<span data-ttu-id="cb188-2835">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2835">6</span></span>

<span data-ttu-id="cb188-2836">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2836">7</span></span>

<span data-ttu-id="cb188-2837">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2837">8</span></span>

<span data-ttu-id="cb188-2838">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2838">9</span></span>

<span data-ttu-id="cb188-2839">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2839">2</span></span><br/> <span data-ttu-id="cb188-2840">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2840">0</span></span><br/>

<span data-ttu-id="cb188-2841">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2841">1</span></span>

<span data-ttu-id="cb188-2842">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2842">2</span></span>

<span data-ttu-id="cb188-2843">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2843">3</span></span>

<span data-ttu-id="cb188-2844">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2844">4</span></span>

<span data-ttu-id="cb188-2845">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2845">5</span></span>

<span data-ttu-id="cb188-2846">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2846">6</span></span>

<span data-ttu-id="cb188-2847">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2847">7</span></span>

<span data-ttu-id="cb188-2848">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2848">8</span></span>

<span data-ttu-id="cb188-2849">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2849">9</span></span>

<span data-ttu-id="cb188-2850">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2850">3</span></span><br/> <span data-ttu-id="cb188-2851">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2851">0</span></span><br/>

<span data-ttu-id="cb188-2852">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2852">1</span></span>

<span data-ttu-id="cb188-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="cb188-2853">\_partID</span></span>

<span data-ttu-id="cb188-2854">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="cb188-2854">\_dwNewState</span></span>

<span data-ttu-id="cb188-2855">\_CatName (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="cb188-2856">**\_ partID:** DEVE essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="cb188-2857">**\_ dwNewState:** DEVE essere impostato su uno dei valori seguenti, che indica il nuovo stato del catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="cb188-2858">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-2858">Value</span></span>                         | <span data-ttu-id="cb188-2859">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-2860">CICAT \_ ARRESTATO 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="cb188-2861">Il catalogo è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2861">The catalog is stopped.</span></span> <span data-ttu-id="cb188-2862">Questo stato indica che non è necessario indicizzare nuovi file e che non devono essere elaborate query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="cb188-2863">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="cb188-2864">Il catalogo è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cb188-2864">The catalog is read-only.</span></span> <span data-ttu-id="cb188-2865">Non è necessario indicizzare nuovi file.</span><span class="sxs-lookup"><span data-stu-id="cb188-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="cb188-2866">CiCAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="cb188-2867">Il catalogo è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="cb188-2867">The catalog is writable.</span></span> <span data-ttu-id="cb188-2868">I nuovi file possono essere indicizzati e le query di ricerca devono essere elaborate.</span><span class="sxs-lookup"><span data-stu-id="cb188-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="cb188-2869">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb188-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="cb188-2870">Il catalogo non è disponibile per l'esecuzione di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="cb188-2871">CICAT \_ GET \_ STATE 0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb188-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="cb188-2872">Lo stato del catalogo non deve essere modificato, ma solo recuperato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="cb188-2873">CICAT \_ ALL \_ OPENED 0x00000020</span><span class="sxs-lookup"><span data-stu-id="cb188-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="cb188-2874">Un controllo per verificare se tutti i cataloghi sono stati avviati.</span><span class="sxs-lookup"><span data-stu-id="cb188-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="cb188-2875">In questo caso, il campo dwOldState inviato nella risposta CPMSetCatStateOut a questo messaggio verrà \_ segnalato come diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cb188-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="cb188-2876">**\_ CatName:** nome del catalogo il cui stato deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="cb188-2877">Il nome DEVE essere una stringa Unicode con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="cb188-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="cb188-2878">Questo campo DEVE essere omesso se \_ dwNewState è impostato su CICAT \_ ALL \_ OPENED.</span><span class="sxs-lookup"><span data-stu-id="cb188-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="cb188-2879">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="cb188-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="cb188-2880">Il messaggio CPMSetCatStateOut è una risposta a un messaggio CPMSetCatStateIn con lo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="cb188-2881">Il formato del messaggio CPMSetCatStateOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-2882">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2882">0</span></span>

<span data-ttu-id="cb188-2883">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2883">1</span></span>

<span data-ttu-id="cb188-2884">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2884">2</span></span>

<span data-ttu-id="cb188-2885">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2885">3</span></span>

<span data-ttu-id="cb188-2886">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2886">4</span></span>

<span data-ttu-id="cb188-2887">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2887">5</span></span>

<span data-ttu-id="cb188-2888">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2888">6</span></span>

<span data-ttu-id="cb188-2889">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2889">7</span></span>

<span data-ttu-id="cb188-2890">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2890">8</span></span>

<span data-ttu-id="cb188-2891">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2891">9</span></span>

<span data-ttu-id="cb188-2892">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2892">1</span></span><br/> <span data-ttu-id="cb188-2893">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2893">0</span></span><br/>

<span data-ttu-id="cb188-2894">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2894">1</span></span>

<span data-ttu-id="cb188-2895">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2895">2</span></span>

<span data-ttu-id="cb188-2896">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2896">3</span></span>

<span data-ttu-id="cb188-2897">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2897">4</span></span>

<span data-ttu-id="cb188-2898">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2898">5</span></span>

<span data-ttu-id="cb188-2899">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2899">6</span></span>

<span data-ttu-id="cb188-2900">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2900">7</span></span>

<span data-ttu-id="cb188-2901">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2901">8</span></span>

<span data-ttu-id="cb188-2902">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2902">9</span></span>

<span data-ttu-id="cb188-2903">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2903">2</span></span><br/> <span data-ttu-id="cb188-2904">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2904">0</span></span><br/>

<span data-ttu-id="cb188-2905">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2905">1</span></span>

<span data-ttu-id="cb188-2906">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2906">2</span></span>

<span data-ttu-id="cb188-2907">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2907">3</span></span>

<span data-ttu-id="cb188-2908">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2908">4</span></span>

<span data-ttu-id="cb188-2909">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2909">5</span></span>

<span data-ttu-id="cb188-2910">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2910">6</span></span>

<span data-ttu-id="cb188-2911">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2911">7</span></span>

<span data-ttu-id="cb188-2912">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2912">8</span></span>

<span data-ttu-id="cb188-2913">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2913">9</span></span>

<span data-ttu-id="cb188-2914">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2914">3</span></span><br/> <span data-ttu-id="cb188-2915">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2915">0</span></span><br/>

<span data-ttu-id="cb188-2916">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2916">1</span></span>

<span data-ttu-id="cb188-2917">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="cb188-2917">\_dwOldState</span></span>



 

<span data-ttu-id="cb188-2918">**\_ dwOldState:** uno dei valori seguenti, che indica lo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="cb188-2919">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-2919">Value</span></span>                       | <span data-ttu-id="cb188-2920">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="cb188-2921">CICAT \_ ARRESTATO 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="cb188-2922">Il catalogo è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="cb188-2923">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="cb188-2924">Il catalogo è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cb188-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="cb188-2925">CICAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="cb188-2926">Il catalogo è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="cb188-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="cb188-2927">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb188-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="cb188-2928">Il catalogo non è disponibile per l'esecuzione di query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="cb188-2929">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="cb188-2930">Il messaggio CPMUpdateDocumentsIn indica al server di indicizzare il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="cb188-2931">Il server risponderà con l'intestazione del messaggio CPMUpdateDocumentsOut, con i risultati della richiesta contenuti nel campo dello stato \_ dell'intestazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="cb188-2932">Il formato del messaggio CPMUpdateDocumentsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-2933">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2933">0</span></span>

<span data-ttu-id="cb188-2934">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2934">1</span></span>

<span data-ttu-id="cb188-2935">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2935">2</span></span>

<span data-ttu-id="cb188-2936">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2936">3</span></span>

<span data-ttu-id="cb188-2937">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2937">4</span></span>

<span data-ttu-id="cb188-2938">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2938">5</span></span>

<span data-ttu-id="cb188-2939">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2939">6</span></span>

<span data-ttu-id="cb188-2940">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2940">7</span></span>

<span data-ttu-id="cb188-2941">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2941">8</span></span>

<span data-ttu-id="cb188-2942">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2942">9</span></span>

<span data-ttu-id="cb188-2943">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2943">1</span></span><br/> <span data-ttu-id="cb188-2944">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2944">0</span></span><br/>

<span data-ttu-id="cb188-2945">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2945">1</span></span>

<span data-ttu-id="cb188-2946">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2946">2</span></span>

<span data-ttu-id="cb188-2947">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2947">3</span></span>

<span data-ttu-id="cb188-2948">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2948">4</span></span>

<span data-ttu-id="cb188-2949">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2949">5</span></span>

<span data-ttu-id="cb188-2950">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2950">6</span></span>

<span data-ttu-id="cb188-2951">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2951">7</span></span>

<span data-ttu-id="cb188-2952">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2952">8</span></span>

<span data-ttu-id="cb188-2953">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2953">9</span></span>

<span data-ttu-id="cb188-2954">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2954">2</span></span><br/> <span data-ttu-id="cb188-2955">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2955">0</span></span><br/>

<span data-ttu-id="cb188-2956">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2956">1</span></span>

<span data-ttu-id="cb188-2957">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2957">2</span></span>

<span data-ttu-id="cb188-2958">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2958">3</span></span>

<span data-ttu-id="cb188-2959">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2959">4</span></span>

<span data-ttu-id="cb188-2960">5</span><span class="sxs-lookup"><span data-stu-id="cb188-2960">5</span></span>

<span data-ttu-id="cb188-2961">6</span><span class="sxs-lookup"><span data-stu-id="cb188-2961">6</span></span>

<span data-ttu-id="cb188-2962">7</span><span class="sxs-lookup"><span data-stu-id="cb188-2962">7</span></span>

<span data-ttu-id="cb188-2963">8</span><span class="sxs-lookup"><span data-stu-id="cb188-2963">8</span></span>

<span data-ttu-id="cb188-2964">9</span><span class="sxs-lookup"><span data-stu-id="cb188-2964">9</span></span>

<span data-ttu-id="cb188-2965">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2965">3</span></span><br/> <span data-ttu-id="cb188-2966">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2966">0</span></span><br/>

<span data-ttu-id="cb188-2967">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2967">1</span></span>

<span data-ttu-id="cb188-2968">\_flag (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2968">\_flag (optional)</span></span>

<span data-ttu-id="cb188-2969">\_fRootPath (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="cb188-2970">RootPath (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="cb188-2971">**\_ flag**: tipo di aggiornamento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="cb188-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="cb188-2972">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cb188-2973">Questo campo DEVE essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="cb188-2974">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-2974">Value</span></span>                  | <span data-ttu-id="cb188-2975">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="cb188-2976">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="cb188-2977">È necessario eseguire un aggiornamento incrementale.</span><span class="sxs-lookup"><span data-stu-id="cb188-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="cb188-2978">UPD \_ FULL 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="cb188-2979">È necessario eseguire un aggiornamento completo.</span><span class="sxs-lookup"><span data-stu-id="cb188-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="cb188-2980">UPD \_ INIT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="cb188-2981">Deve essere eseguita una nuova inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="cb188-2982">**\_ fRootPath:** valore booleano che indica se il campo RootPath specifica un percorso in cui eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="cb188-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="cb188-2983">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cb188-2984">Questo campo DEVE essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cb188-2985">Se impostato su 0x00000001, un percorso in cui eseguire l'aggiornamento viene incluso in RootPath.</span><span class="sxs-lookup"><span data-stu-id="cb188-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="cb188-2986">Se impostato su 0x00000000, l'aggiornamento deve essere eseguito in tutti i percorsi indicizzati.</span><span class="sxs-lookup"><span data-stu-id="cb188-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="cb188-2987">**RootPath:** nome del percorso da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="cb188-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="cb188-2988">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cb188-2989">Il nome DEVE essere una stringa Unicode con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="cb188-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="cb188-2990">Questo campo DEVE essere omesso se \_ fRootPath è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="cb188-2991">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cb188-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="cb188-2992">Il messaggio CPMForceMergeIn richiede a un server di eseguire la manutenzione necessaria per migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="cb188-2993">Il server risponderà con l'intestazione del messaggio CPMForceMergeIn, con i risultati della richiesta contenuti nel \_ campo dello stato.</span><span class="sxs-lookup"><span data-stu-id="cb188-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="cb188-2994">Il formato del messaggio CPMForceMergeIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-2995">0</span><span class="sxs-lookup"><span data-stu-id="cb188-2995">0</span></span>

<span data-ttu-id="cb188-2996">1</span><span class="sxs-lookup"><span data-stu-id="cb188-2996">1</span></span>

<span data-ttu-id="cb188-2997">2</span><span class="sxs-lookup"><span data-stu-id="cb188-2997">2</span></span>

<span data-ttu-id="cb188-2998">3</span><span class="sxs-lookup"><span data-stu-id="cb188-2998">3</span></span>

<span data-ttu-id="cb188-2999">4</span><span class="sxs-lookup"><span data-stu-id="cb188-2999">4</span></span>

<span data-ttu-id="cb188-3000">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3000">5</span></span>

<span data-ttu-id="cb188-3001">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3001">6</span></span>

<span data-ttu-id="cb188-3002">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3002">7</span></span>

<span data-ttu-id="cb188-3003">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3003">8</span></span>

<span data-ttu-id="cb188-3004">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3004">9</span></span>

<span data-ttu-id="cb188-3005">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3005">1</span></span><br/> <span data-ttu-id="cb188-3006">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3006">0</span></span><br/>

<span data-ttu-id="cb188-3007">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3007">1</span></span>

<span data-ttu-id="cb188-3008">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3008">2</span></span>

<span data-ttu-id="cb188-3009">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3009">3</span></span>

<span data-ttu-id="cb188-3010">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3010">4</span></span>

<span data-ttu-id="cb188-3011">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3011">5</span></span>

<span data-ttu-id="cb188-3012">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3012">6</span></span>

<span data-ttu-id="cb188-3013">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3013">7</span></span>

<span data-ttu-id="cb188-3014">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3014">8</span></span>

<span data-ttu-id="cb188-3015">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3015">9</span></span>

<span data-ttu-id="cb188-3016">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3016">2</span></span><br/> <span data-ttu-id="cb188-3017">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3017">0</span></span><br/>

<span data-ttu-id="cb188-3018">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3018">1</span></span>

<span data-ttu-id="cb188-3019">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3019">2</span></span>

<span data-ttu-id="cb188-3020">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3020">3</span></span>

<span data-ttu-id="cb188-3021">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3021">4</span></span>

<span data-ttu-id="cb188-3022">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3022">5</span></span>

<span data-ttu-id="cb188-3023">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3023">6</span></span>

<span data-ttu-id="cb188-3024">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3024">7</span></span>

<span data-ttu-id="cb188-3025">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3025">8</span></span>

<span data-ttu-id="cb188-3026">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3026">9</span></span>

<span data-ttu-id="cb188-3027">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3027">3</span></span><br/> <span data-ttu-id="cb188-3028">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3028">0</span></span><br/>

<span data-ttu-id="cb188-3029">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3029">1</span></span>

<span data-ttu-id="cb188-3030">\_partID (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="cb188-3031">**\_ partID:** questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cb188-3032">Quando questo campo è presente, DEVE essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="cb188-3033">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="cb188-3034">Il messaggio CPMConnectIn avvia una sessione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="cb188-3035">Il formato del messaggio CPMConnectIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3036">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3036">0</span></span>

<span data-ttu-id="cb188-3037">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3037">1</span></span>

<span data-ttu-id="cb188-3038">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3038">2</span></span>

<span data-ttu-id="cb188-3039">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3039">3</span></span>

<span data-ttu-id="cb188-3040">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3040">4</span></span>

<span data-ttu-id="cb188-3041">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3041">5</span></span>

<span data-ttu-id="cb188-3042">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3042">6</span></span>

<span data-ttu-id="cb188-3043">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3043">7</span></span>

<span data-ttu-id="cb188-3044">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3044">8</span></span>

<span data-ttu-id="cb188-3045">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3045">9</span></span>

<span data-ttu-id="cb188-3046">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3046">1</span></span><br/> <span data-ttu-id="cb188-3047">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3047">0</span></span><br/>

<span data-ttu-id="cb188-3048">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3048">1</span></span>

<span data-ttu-id="cb188-3049">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3049">2</span></span>

<span data-ttu-id="cb188-3050">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3050">3</span></span>

<span data-ttu-id="cb188-3051">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3051">4</span></span>

<span data-ttu-id="cb188-3052">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3052">5</span></span>

<span data-ttu-id="cb188-3053">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3053">6</span></span>

<span data-ttu-id="cb188-3054">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3054">7</span></span>

<span data-ttu-id="cb188-3055">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3055">8</span></span>

<span data-ttu-id="cb188-3056">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3056">9</span></span>

<span data-ttu-id="cb188-3057">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3057">2</span></span><br/> <span data-ttu-id="cb188-3058">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3058">0</span></span><br/>

<span data-ttu-id="cb188-3059">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3059">1</span></span>

<span data-ttu-id="cb188-3060">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3060">2</span></span>

<span data-ttu-id="cb188-3061">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3061">3</span></span>

<span data-ttu-id="cb188-3062">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3062">4</span></span>

<span data-ttu-id="cb188-3063">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3063">5</span></span>

<span data-ttu-id="cb188-3064">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3064">6</span></span>

<span data-ttu-id="cb188-3065">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3065">7</span></span>

<span data-ttu-id="cb188-3066">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3066">8</span></span>

<span data-ttu-id="cb188-3067">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3067">9</span></span>

<span data-ttu-id="cb188-3068">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3068">3</span></span><br/> <span data-ttu-id="cb188-3069">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3069">0</span></span><br/>

<span data-ttu-id="cb188-3070">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3070">1</span></span>

<span data-ttu-id="cb188-3071">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="cb188-3071">\_iClientVersion</span></span>

<span data-ttu-id="cb188-3072">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="cb188-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="cb188-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="cb188-3073">\_cbBlob1</span></span>

<span data-ttu-id="cb188-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="cb188-3074">\_cbBlob2</span></span>

<span data-ttu-id="cb188-3075">\_Imbottitura</span><span class="sxs-lookup"><span data-stu-id="cb188-3075">\_padding</span></span>

<span data-ttu-id="cb188-3076">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3076">...</span></span>

<span data-ttu-id="cb188-3077">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3077">...</span></span>

<span data-ttu-id="cb188-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="cb188-3078">MachineName</span></span>

<span data-ttu-id="cb188-3079">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3079">... (variable)</span></span>

<span data-ttu-id="cb188-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="cb188-3080">UserName</span></span>

<span data-ttu-id="cb188-3081">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3081">... (variable)</span></span>

<span data-ttu-id="cb188-3082">\_paddingcPropSets (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="cb188-3083">cPropSets</span><span class="sxs-lookup"><span data-stu-id="cb188-3083">cPropSets</span></span>

<span data-ttu-id="cb188-3084">PropertySet1 (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="cb188-3085">PropertySet2 (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="cb188-3086">\_paddingExtPropset (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="cb188-3087">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="cb188-3087">cExtPropSet</span></span>

<span data-ttu-id="cb188-3088">aPropertySets (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="cb188-3089">**\_ iClientVersion:** intero a 32 bit che indica se il server deve convalidare il valore di checksum specificato nel campo ulChecksum delle intestazioni dei messaggi inviati \_ dal client.</span><span class="sxs-lookup"><span data-stu-id="cb188-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="cb188-3090">Se il campo iClientVersion è impostato su 0x00000008 o versione successiva, il server DEVE convalidare il valore del campo \_ \_ ulChecksum per i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="cb188-3091">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="cb188-3092">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="cb188-3093">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="cb188-3094">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="cb188-3095">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="cb188-3096">Per informazioni dettagliate sul modo in cui il server convalida il valore specificato dal client nel campo ulChecksum per i messaggi elencati in precedenza, vedere la sezione 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="cb188-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="cb188-3097">Se il valore è maggiore 0x00000008, si presuppone che il client sia in grado di gestire gli offset a 64 bit nei messaggi CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="cb188-3098">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="cb188-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="cb188-3099">*Comportamento di Windows: nei client Windows, iClientVersion viene impostato come segue:*</span><span class="sxs-lookup"><span data-stu-id="cb188-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="cb188-3100">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-3100">Value</span></span>      | <span data-ttu-id="cb188-3101">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="cb188-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cb188-3102">0x00000005</span></span> | <span data-ttu-id="cb188-3103">Il sistema operativo client è Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cb188-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="cb188-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb188-3104">0x00000008</span></span> | <span data-ttu-id="cb188-3105">Il sistema operativo client è Windows XP a 32 bit o Windows Server 2003 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="cb188-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="cb188-3106">0x00010008</span></span> | <span data-ttu-id="cb188-3107">Il sistema operativo client è Windows XP a 64 bit o Windows Server 2003 a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="cb188-3108">\_**fClientIsRemote:** valore booleano che indica se il client è in esecuzione in un computer diverso dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="cb188-3109">DEVE essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="cb188-3110">\_**cbBlob1:** intero senza segno a 32 bit che indica le dimensioni in byte dei campi cPropSet, PropertySet1 e PropertySet2 combinati.</span><span class="sxs-lookup"><span data-stu-id="cb188-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="cb188-3111">\_**cbBlob2:** intero senza segno a 32 bit che indica le dimensioni in byte dei campi cExPropSet e aPropertySet, combinati.</span><span class="sxs-lookup"><span data-stu-id="cb188-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="cb188-3112">\_**padding:** 12 byte di spaziatura interna che possono contenere valori arbitrari e DEVE essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="cb188-3113">**MachineName:** nome del computer del client.</span><span class="sxs-lookup"><span data-stu-id="cb188-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="cb188-3114">La stringa del nome DEVE essere una matrice con terminazione Null di meno di 512 caratteri Unicode, incluso il carattere di terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="cb188-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="cb188-3115">**UserName:** stringa che rappresenta il nome utente della persona che esegue l'applicazione che ha richiamato questo protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb188-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="cb188-3116">La stringa del nome DEVE essere una matrice con terminazione Null di meno di 512 caratteri Unicode se concatenata con MachineName.</span><span class="sxs-lookup"><span data-stu-id="cb188-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="cb188-3117">**\_ paddingcPropSets:** questo campo DEVE avere una lunghezza da 0 a 7 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="cb188-3118">Il numero di byte DEVE essere il numero necessario per rendere l'offset in byte del campo cPropSets dall'inizio del messaggio che contiene questa struttura è un multiplo di 8.</span><span class="sxs-lookup"><span data-stu-id="cb188-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="cb188-3119">Il valore dei byte può essere qualsiasi valore arbitrario e DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-3120">**cPropSets:** intero senza segno a 32 bit che indica il numero di strutture CDbPropSet che segue questo campo.</span><span class="sxs-lookup"><span data-stu-id="cb188-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="cb188-3121">Questo valore DEVE essere impostato su 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="cb188-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="cb188-3122">**PropertySet1:** struttura CDbPropSet con guidPropertySet contenente DBPROPSET \_ FSCIFRMWRK EXT (vedere la sezione \_ 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="cb188-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="cb188-3123">**PropertySet2:** struttura CDbPropSet con guidPropertySet contenente DBPROPSET \_ CIFRMWRKCORE EXT (vedere la sezione \_ 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="cb188-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="cb188-3124">\_**PaddingExtPropset:** questo campo DEVE avere una lunghezza da 0 a 7 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="cb188-3125">Il numero di byte DEVE essere il numero necessario per rendere l'offset in byte del campo cExtPropSets dall'inizio del messaggio che contiene questa struttura è un multiplo di 8.</span><span class="sxs-lookup"><span data-stu-id="cb188-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="cb188-3126">Il valore dei byte può essere qualsiasi valore arbitrario e DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-3127">**cExtPropSet:** intero senza segno a 32 bit che indica il numero di strutture CDbPropSet che segue questo campo.</span><span class="sxs-lookup"><span data-stu-id="cb188-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="cb188-3128">**aPropertySets:** matrice di strutture CDbPropSet che specificano altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="cb188-3129">Il numero di elementi in questa matrice DEVE essere uguale a cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="cb188-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="cb188-3130">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="cb188-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="cb188-3131">Il messaggio CPMConnectOut contiene una risposta a un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="cb188-3132">Il formato del messaggio CPMConnectOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-3133">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3133">0</span></span>

<span data-ttu-id="cb188-3134">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3134">1</span></span>

<span data-ttu-id="cb188-3135">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3135">2</span></span>

<span data-ttu-id="cb188-3136">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3136">3</span></span>

<span data-ttu-id="cb188-3137">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3137">4</span></span>

<span data-ttu-id="cb188-3138">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3138">5</span></span>

<span data-ttu-id="cb188-3139">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3139">6</span></span>

<span data-ttu-id="cb188-3140">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3140">7</span></span>

<span data-ttu-id="cb188-3141">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3141">8</span></span>

<span data-ttu-id="cb188-3142">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3142">9</span></span>

<span data-ttu-id="cb188-3143">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3143">1</span></span><br/> <span data-ttu-id="cb188-3144">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3144">0</span></span><br/>

<span data-ttu-id="cb188-3145">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3145">1</span></span>

<span data-ttu-id="cb188-3146">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3146">2</span></span>

<span data-ttu-id="cb188-3147">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3147">3</span></span>

<span data-ttu-id="cb188-3148">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3148">4</span></span>

<span data-ttu-id="cb188-3149">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3149">5</span></span>

<span data-ttu-id="cb188-3150">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3150">6</span></span>

<span data-ttu-id="cb188-3151">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3151">7</span></span>

<span data-ttu-id="cb188-3152">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3152">8</span></span>

<span data-ttu-id="cb188-3153">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3153">9</span></span>

<span data-ttu-id="cb188-3154">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3154">2</span></span><br/> <span data-ttu-id="cb188-3155">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3155">0</span></span><br/>

<span data-ttu-id="cb188-3156">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3156">1</span></span>

<span data-ttu-id="cb188-3157">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3157">2</span></span>

<span data-ttu-id="cb188-3158">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3158">3</span></span>

<span data-ttu-id="cb188-3159">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3159">4</span></span>

<span data-ttu-id="cb188-3160">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3160">5</span></span>

<span data-ttu-id="cb188-3161">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3161">6</span></span>

<span data-ttu-id="cb188-3162">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3162">7</span></span>

<span data-ttu-id="cb188-3163">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3163">8</span></span>

<span data-ttu-id="cb188-3164">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3164">9</span></span>

<span data-ttu-id="cb188-3165">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3165">3</span></span><br/> <span data-ttu-id="cb188-3166">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3166">0</span></span><br/>

<span data-ttu-id="cb188-3167">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3167">1</span></span>

<span data-ttu-id="cb188-3168">\_Serverversion</span><span class="sxs-lookup"><span data-stu-id="cb188-3168">\_serverVersion</span></span>

<span data-ttu-id="cb188-3169">\_reserved (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="cb188-3170">**\_ serverVersion:**</span><span class="sxs-lookup"><span data-stu-id="cb188-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="cb188-3171">Intero a 32 bit che indica se il server può supportare offset a 64 *bit.*</span><span class="sxs-lookup"><span data-stu-id="cb188-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="cb188-3172">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="cb188-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="cb188-3173">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-3173">Value</span></span>      | <span data-ttu-id="cb188-3174">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="cb188-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb188-3175">0x00000007</span></span> | <span data-ttu-id="cb188-3176">Il server può inviare solo offset a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="cb188-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="cb188-3177">0x00010007</span></span> | <span data-ttu-id="cb188-3178">Il server può inviare offset a 32 o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="cb188-3179">**\_ reserved:** riservato.</span><span class="sxs-lookup"><span data-stu-id="cb188-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="cb188-3180">Il server PUÒ inviare un numero arbitrario di valori arbitrari e il client DEVE ignorare questi valori, se presenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="cb188-3181">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="cb188-3182">Il messaggio CPMCreateQueryIn crea una nuova query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="cb188-3183">Il formato del messaggio CPMCreateQueryIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3184">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3184">0</span></span>

<span data-ttu-id="cb188-3185">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3185">1</span></span>

<span data-ttu-id="cb188-3186">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3186">2</span></span>

<span data-ttu-id="cb188-3187">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3187">3</span></span>

<span data-ttu-id="cb188-3188">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3188">4</span></span>

<span data-ttu-id="cb188-3189">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3189">5</span></span>

<span data-ttu-id="cb188-3190">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3190">6</span></span>

<span data-ttu-id="cb188-3191">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3191">7</span></span>

<span data-ttu-id="cb188-3192">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3192">8</span></span>

<span data-ttu-id="cb188-3193">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3193">9</span></span>

<span data-ttu-id="cb188-3194">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3194">1</span></span><br/> <span data-ttu-id="cb188-3195">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3195">0</span></span><br/>

<span data-ttu-id="cb188-3196">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3196">1</span></span>

<span data-ttu-id="cb188-3197">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3197">2</span></span>

<span data-ttu-id="cb188-3198">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3198">3</span></span>

<span data-ttu-id="cb188-3199">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3199">4</span></span>

<span data-ttu-id="cb188-3200">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3200">5</span></span>

<span data-ttu-id="cb188-3201">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3201">6</span></span>

<span data-ttu-id="cb188-3202">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3202">7</span></span>

<span data-ttu-id="cb188-3203">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3203">8</span></span>

<span data-ttu-id="cb188-3204">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3204">9</span></span>

<span data-ttu-id="cb188-3205">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3205">2</span></span><br/> <span data-ttu-id="cb188-3206">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3206">0</span></span><br/>

<span data-ttu-id="cb188-3207">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3207">1</span></span>

<span data-ttu-id="cb188-3208">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3208">2</span></span>

<span data-ttu-id="cb188-3209">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3209">3</span></span>

<span data-ttu-id="cb188-3210">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3210">4</span></span>

<span data-ttu-id="cb188-3211">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3211">5</span></span>

<span data-ttu-id="cb188-3212">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3212">6</span></span>

<span data-ttu-id="cb188-3213">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3213">7</span></span>

<span data-ttu-id="cb188-3214">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3214">8</span></span>

<span data-ttu-id="cb188-3215">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3215">9</span></span>

<span data-ttu-id="cb188-3216">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3216">3</span></span><br/> <span data-ttu-id="cb188-3217">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3217">0</span></span><br/>

<span data-ttu-id="cb188-3218">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3218">1</span></span>

<span data-ttu-id="cb188-3219">Dimensione</span><span class="sxs-lookup"><span data-stu-id="cb188-3219">Size</span></span>

<span data-ttu-id="cb188-3220">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="cb188-3220">CColumnSetPresent</span></span>

<span data-ttu-id="cb188-3221">ColumnSet (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="cb188-3222">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3222">... (variable)</span></span>

<span data-ttu-id="cb188-3223">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="cb188-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="cb188-3224">Restrizione (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3224">Restriction (optional)</span></span>

<span data-ttu-id="cb188-3225">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3225">... (variable)</span></span>

<span data-ttu-id="cb188-3226">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="cb188-3226">CSortSetPresent</span></span>

<span data-ttu-id="cb188-3227">SortSet (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3227">SortSet (optional)</span></span>

<span data-ttu-id="cb188-3228">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3228">... (variable)</span></span>

<span data-ttu-id="cb188-3229">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="cb188-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="cb188-3230">CategorizationSet (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="cb188-3231">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3231">... (variable)</span></span>

<span data-ttu-id="cb188-3232">Proprietà RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="cb188-3232">RowSetProperties</span></span>

<span data-ttu-id="cb188-3233">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3233">...</span></span>

<span data-ttu-id="cb188-3234">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3234">...</span></span>

<span data-ttu-id="cb188-3235">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3235">...</span></span>

<span data-ttu-id="cb188-3236">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3236">...</span></span>

<span data-ttu-id="cb188-3237">PidMapper (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="cb188-3238">**Size:** intero senza segno a 32 bit che indica il numero di byte dall'inizio di questo campo alla fine del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="cb188-3239">**CColumnSetPresent:** campo byte che indica se il campo ColumnSet è presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="cb188-3240">Questo campo DEVE essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cb188-3241">Se impostato su 0x01 il campo CColumnSet DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="cb188-3242">Se impostato su 0x00, DEVE essere assente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="cb188-3243">**ColumnSet:** struttura CColumnSet contenente i numeri di colonna in cui devono essere restituite le proprietà di CPidMapper.</span><span class="sxs-lookup"><span data-stu-id="cb188-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="cb188-3244">**CRestrictionPresent:** campo byte che indica se il campo Restriction è presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="cb188-3245">Se impostato su un valore diverso da zero, il campo Restrizione DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="cb188-3246">Se impostato su 0x00, Restriction MUST essere assente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="cb188-3247">**Restrizione:** struttura CRestriction contenente l'albero dei comandi della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="cb188-3248">**CSortSetPresent:** campo byte che indica se il campo SortSet è presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="cb188-3249">Se impostato su un valore diverso da zero, il campo SortSet DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="cb188-3250">Se impostato su 0x00, SortSet DEVE essere assente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="cb188-3251">**SortSet:** struttura CSortSet che indica l'ordinamento della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="cb188-3252">**CCategorizationSetPresent:** campo di byte che indica se il campo CCategorizationSet è presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="cb188-3253">Se impostato su un valore diverso da zero, il campo CCategorizationSet DEVE essere presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="cb188-3254">Se impostato su 0x00, CCategorizationSet DEVE essere assente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="cb188-3255">**CCategorizationSet:** struttura CCategorizationSet che contiene i gruppi per la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="cb188-3256">**RowSetProperties:** struttura CRowsetProperties che fornisce informazioni di configurazione per la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="cb188-3257">**PidMapper:** struttura CPidMapper contenente le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="cb188-3258">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="cb188-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="cb188-3259">Il messaggio CPMCreateQueryOut contiene una risposta a un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="cb188-3260">Il formato del messaggio CPMCreateQueryOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-3261">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3261">0</span></span>

<span data-ttu-id="cb188-3262">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3262">1</span></span>

<span data-ttu-id="cb188-3263">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3263">2</span></span>

<span data-ttu-id="cb188-3264">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3264">3</span></span>

<span data-ttu-id="cb188-3265">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3265">4</span></span>

<span data-ttu-id="cb188-3266">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3266">5</span></span>

<span data-ttu-id="cb188-3267">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3267">6</span></span>

<span data-ttu-id="cb188-3268">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3268">7</span></span>

<span data-ttu-id="cb188-3269">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3269">8</span></span>

<span data-ttu-id="cb188-3270">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3270">9</span></span>

<span data-ttu-id="cb188-3271">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3271">1</span></span><br/> <span data-ttu-id="cb188-3272">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3272">0</span></span><br/>

<span data-ttu-id="cb188-3273">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3273">1</span></span>

<span data-ttu-id="cb188-3274">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3274">2</span></span>

<span data-ttu-id="cb188-3275">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3275">3</span></span>

<span data-ttu-id="cb188-3276">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3276">4</span></span>

<span data-ttu-id="cb188-3277">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3277">5</span></span>

<span data-ttu-id="cb188-3278">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3278">6</span></span>

<span data-ttu-id="cb188-3279">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3279">7</span></span>

<span data-ttu-id="cb188-3280">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3280">8</span></span>

<span data-ttu-id="cb188-3281">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3281">9</span></span>

<span data-ttu-id="cb188-3282">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3282">2</span></span><br/> <span data-ttu-id="cb188-3283">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3283">0</span></span><br/>

<span data-ttu-id="cb188-3284">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3284">1</span></span>

<span data-ttu-id="cb188-3285">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3285">2</span></span>

<span data-ttu-id="cb188-3286">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3286">3</span></span>

<span data-ttu-id="cb188-3287">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3287">4</span></span>

<span data-ttu-id="cb188-3288">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3288">5</span></span>

<span data-ttu-id="cb188-3289">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3289">6</span></span>

<span data-ttu-id="cb188-3290">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3290">7</span></span>

<span data-ttu-id="cb188-3291">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3291">8</span></span>

<span data-ttu-id="cb188-3292">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3292">9</span></span>

<span data-ttu-id="cb188-3293">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3293">3</span></span><br/> <span data-ttu-id="cb188-3294">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3294">0</span></span><br/>

<span data-ttu-id="cb188-3295">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3295">1</span></span>

<span data-ttu-id="cb188-3296">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="cb188-3296">\_fTrueSequential</span></span>

<span data-ttu-id="cb188-3297">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="cb188-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="cb188-3298">aCursors</span><span class="sxs-lookup"><span data-stu-id="cb188-3298">aCursors</span></span>



 

<span data-ttu-id="cb188-3299">**\_ fTrueSequential:** valore booleano informativo che indica se è possibile che la query fornisca risultati più velocemente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="cb188-3300">Se impostato su 0x00000001 per la query fornita in CPMCreateQueryIn, il server può usare l'indice in modo che i risultati della query possano essere recapitati più velocemente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="cb188-3301">Se impostato su 0x00000000, si verifica una latenza maggiore nel recapito dei risultati delle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="cb188-3302">NON DEVE essere impostato su nessun altro valore.</span><span class="sxs-lookup"><span data-stu-id="cb188-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="cb188-3303">**\_ fWorkIdUnique:** valore booleano che indica se gli identificatori di documento a cui puntano i cursori sono univoci nei risultati della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="cb188-3304">Se impostato su 0x00000001, gli identificatori sono univoci.</span><span class="sxs-lookup"><span data-stu-id="cb188-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="cb188-3305">Se impostato su 0x00000000, sono univoci solo in tutto il set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="cb188-3306">**aCursors:** matrice di interi senza segno a 32 bit che rappresentano gli handle per i cursori, con il numero di elementi uguale al numero di categorie nel campo CategorizationSet del messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="cb188-3307">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="cb188-3308">Il messaggio CPMGetQueryStatusIn richiede lo stato di una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="cb188-3309">Il formato del messaggio CPMGetQueryStatusIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3310">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3310">0</span></span>

<span data-ttu-id="cb188-3311">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3311">1</span></span>

<span data-ttu-id="cb188-3312">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3312">2</span></span>

<span data-ttu-id="cb188-3313">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3313">3</span></span>

<span data-ttu-id="cb188-3314">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3314">4</span></span>

<span data-ttu-id="cb188-3315">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3315">5</span></span>

<span data-ttu-id="cb188-3316">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3316">6</span></span>

<span data-ttu-id="cb188-3317">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3317">7</span></span>

<span data-ttu-id="cb188-3318">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3318">8</span></span>

<span data-ttu-id="cb188-3319">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3319">9</span></span>

<span data-ttu-id="cb188-3320">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3320">1</span></span><br/> <span data-ttu-id="cb188-3321">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3321">0</span></span><br/>

<span data-ttu-id="cb188-3322">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3322">1</span></span>

<span data-ttu-id="cb188-3323">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3323">2</span></span>

<span data-ttu-id="cb188-3324">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3324">3</span></span>

<span data-ttu-id="cb188-3325">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3325">4</span></span>

<span data-ttu-id="cb188-3326">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3326">5</span></span>

<span data-ttu-id="cb188-3327">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3327">6</span></span>

<span data-ttu-id="cb188-3328">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3328">7</span></span>

<span data-ttu-id="cb188-3329">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3329">8</span></span>

<span data-ttu-id="cb188-3330">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3330">9</span></span>

<span data-ttu-id="cb188-3331">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3331">2</span></span><br/> <span data-ttu-id="cb188-3332">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3332">0</span></span><br/>

<span data-ttu-id="cb188-3333">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3333">1</span></span>

<span data-ttu-id="cb188-3334">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3334">2</span></span>

<span data-ttu-id="cb188-3335">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3335">3</span></span>

<span data-ttu-id="cb188-3336">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3336">4</span></span>

<span data-ttu-id="cb188-3337">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3337">5</span></span>

<span data-ttu-id="cb188-3338">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3338">6</span></span>

<span data-ttu-id="cb188-3339">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3339">7</span></span>

<span data-ttu-id="cb188-3340">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3340">8</span></span>

<span data-ttu-id="cb188-3341">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3341">9</span></span>

<span data-ttu-id="cb188-3342">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3342">3</span></span><br/> <span data-ttu-id="cb188-3343">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3343">0</span></span><br/>

<span data-ttu-id="cb188-3344">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3344">1</span></span>

<span data-ttu-id="cb188-3345">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cb188-3345">\_hCursor</span></span>



 

<span data-ttu-id="cb188-3346">**\_ hCursor:** intero senza segno a 32 bit che rappresenta l'handle dal messaggio CPMCreateQueryOut che identifica la query per cui recuperare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="cb188-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="cb188-3347">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="cb188-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="cb188-3348">Il messaggio CPMGetQueryStatusOut risponde a un messaggio CPMGetQueryStatusIn con lo stato della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="cb188-3349">Il formato del messaggio CPMGetQueryStatusOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-3350">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3350">0</span></span>

<span data-ttu-id="cb188-3351">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3351">1</span></span>

<span data-ttu-id="cb188-3352">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3352">2</span></span>

<span data-ttu-id="cb188-3353">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3353">3</span></span>

<span data-ttu-id="cb188-3354">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3354">4</span></span>

<span data-ttu-id="cb188-3355">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3355">5</span></span>

<span data-ttu-id="cb188-3356">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3356">6</span></span>

<span data-ttu-id="cb188-3357">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3357">7</span></span>

<span data-ttu-id="cb188-3358">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3358">8</span></span>

<span data-ttu-id="cb188-3359">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3359">9</span></span>

<span data-ttu-id="cb188-3360">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3360">1</span></span><br/> <span data-ttu-id="cb188-3361">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3361">0</span></span><br/>

<span data-ttu-id="cb188-3362">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3362">1</span></span>

<span data-ttu-id="cb188-3363">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3363">2</span></span>

<span data-ttu-id="cb188-3364">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3364">3</span></span>

<span data-ttu-id="cb188-3365">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3365">4</span></span>

<span data-ttu-id="cb188-3366">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3366">5</span></span>

<span data-ttu-id="cb188-3367">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3367">6</span></span>

<span data-ttu-id="cb188-3368">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3368">7</span></span>

<span data-ttu-id="cb188-3369">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3369">8</span></span>

<span data-ttu-id="cb188-3370">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3370">9</span></span>

<span data-ttu-id="cb188-3371">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3371">2</span></span><br/> <span data-ttu-id="cb188-3372">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3372">0</span></span><br/>

<span data-ttu-id="cb188-3373">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3373">1</span></span>

<span data-ttu-id="cb188-3374">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3374">2</span></span>

<span data-ttu-id="cb188-3375">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3375">3</span></span>

<span data-ttu-id="cb188-3376">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3376">4</span></span>

<span data-ttu-id="cb188-3377">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3377">5</span></span>

<span data-ttu-id="cb188-3378">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3378">6</span></span>

<span data-ttu-id="cb188-3379">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3379">7</span></span>

<span data-ttu-id="cb188-3380">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3380">8</span></span>

<span data-ttu-id="cb188-3381">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3381">9</span></span>

<span data-ttu-id="cb188-3382">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3382">3</span></span><br/> <span data-ttu-id="cb188-3383">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3383">0</span></span><br/>

<span data-ttu-id="cb188-3384">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3384">1</span></span>

<span data-ttu-id="cb188-3385">\_Stato</span><span class="sxs-lookup"><span data-stu-id="cb188-3385">\_Status</span></span>



 

<span data-ttu-id="cb188-3386">**\_ Stato:** maschera di bit dei valori definiti nelle tabelle seguenti che descrive la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="cb188-3387">Nella tabella seguente sono elencati i valori STAT \_ \* ottenuti eseguendo un'operazione AND bit per bit \_ su Status con 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="cb188-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="cb188-3388">Il risultato DEVE essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="cb188-3389">Costante</span><span class="sxs-lookup"><span data-stu-id="cb188-3389">Constant</span></span>                 | <span data-ttu-id="cb188-3390">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-3391">STAT \_ BUSY 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="cb188-3392">La query asincrona è ancora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cb188-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="cb188-3393">Errore STAT \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="cb188-3394">La query è in uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="cb188-3395">STAT \_ DONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="cb188-3396">La query è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cb188-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="cb188-3397">Aggiornamento STAT \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="cb188-3398">La query è stata completata, ma gli aggiornamenti hanno come risultato un calcolo aggiuntivo delle query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="cb188-3399">Nella tabella seguente sono elencati i bit STAT \_ \* aggiuntivi che possono essere impostati in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="cb188-3400">Costante</span><span class="sxs-lookup"><span data-stu-id="cb188-3400">Constant</span></span>                                    | <span data-ttu-id="cb188-3401">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb188-3402">STAT \_ NOISE \_ WORDS 0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb188-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="cb188-3403">Le parole non consentite sono state sostituite da caratteri jolly nella query sul contenuto.</span><span class="sxs-lookup"><span data-stu-id="cb188-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="cb188-3404">CONTENUTO \_ STAT \_ \_ NON AGGIORNATO \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="cb188-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="cb188-3405">I risultati della query potrebbero non essere corretti perché la query ha modificato, ma non indicizzato, i file.</span><span class="sxs-lookup"><span data-stu-id="cb188-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="cb188-3406">AGGIORNAMENTO STAT \_ \_ INCOMPLETO 0x00000040</span><span class="sxs-lookup"><span data-stu-id="cb188-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="cb188-3407">I risultati della query potrebbero non essere corretti perché la query ha modificato e indicizzato nuovamente i file il cui contenuto non è stato incluso.</span><span class="sxs-lookup"><span data-stu-id="cb188-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="cb188-3408">STAT \_ CONTENT \_ QUERY \_ INCOMPLETE 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cb188-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="cb188-3409">La query sul contenuto era troppo complessa per il completamento o l'enumerazione richiesta invece dell'uso dell'indice di contenuto.</span><span class="sxs-lookup"><span data-stu-id="cb188-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="cb188-3410">LIMITE DI \_ TEMPO \_ STAT \_ SUPERATO 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cb188-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="cb188-3411">I risultati della query potrebbero non essere corretti perché il tempo di esecuzione della query ha raggiunto il tempo massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="cb188-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="cb188-3412">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="cb188-3413">Il messaggio CPMGetQueryStatusExIn richiede lo stato di una query e informazioni aggiuntive, ad esempio il numero di documenti indicizzati, il numero di documenti rimanenti da indicizzare e così via.</span><span class="sxs-lookup"><span data-stu-id="cb188-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="cb188-3414">Il formato del messaggio CPMGetQueryStatusExIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3415">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3415">0</span></span>

<span data-ttu-id="cb188-3416">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3416">1</span></span>

<span data-ttu-id="cb188-3417">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3417">2</span></span>

<span data-ttu-id="cb188-3418">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3418">3</span></span>

<span data-ttu-id="cb188-3419">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3419">4</span></span>

<span data-ttu-id="cb188-3420">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3420">5</span></span>

<span data-ttu-id="cb188-3421">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3421">6</span></span>

<span data-ttu-id="cb188-3422">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3422">7</span></span>

<span data-ttu-id="cb188-3423">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3423">8</span></span>

<span data-ttu-id="cb188-3424">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3424">9</span></span>

<span data-ttu-id="cb188-3425">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3425">1</span></span><br/> <span data-ttu-id="cb188-3426">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3426">0</span></span><br/>

<span data-ttu-id="cb188-3427">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3427">1</span></span>

<span data-ttu-id="cb188-3428">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3428">2</span></span>

<span data-ttu-id="cb188-3429">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3429">3</span></span>

<span data-ttu-id="cb188-3430">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3430">4</span></span>

<span data-ttu-id="cb188-3431">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3431">5</span></span>

<span data-ttu-id="cb188-3432">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3432">6</span></span>

<span data-ttu-id="cb188-3433">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3433">7</span></span>

<span data-ttu-id="cb188-3434">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3434">8</span></span>

<span data-ttu-id="cb188-3435">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3435">9</span></span>

<span data-ttu-id="cb188-3436">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3436">2</span></span><br/> <span data-ttu-id="cb188-3437">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3437">0</span></span><br/>

<span data-ttu-id="cb188-3438">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3438">1</span></span>

<span data-ttu-id="cb188-3439">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3439">2</span></span>

<span data-ttu-id="cb188-3440">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3440">3</span></span>

<span data-ttu-id="cb188-3441">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3441">4</span></span>

<span data-ttu-id="cb188-3442">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3442">5</span></span>

<span data-ttu-id="cb188-3443">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3443">6</span></span>

<span data-ttu-id="cb188-3444">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3444">7</span></span>

<span data-ttu-id="cb188-3445">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3445">8</span></span>

<span data-ttu-id="cb188-3446">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3446">9</span></span>

<span data-ttu-id="cb188-3447">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3447">3</span></span><br/> <span data-ttu-id="cb188-3448">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3448">0</span></span><br/>

<span data-ttu-id="cb188-3449">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3449">1</span></span>

<span data-ttu-id="cb188-3450">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cb188-3450">\_hCursor</span></span>

<span data-ttu-id="cb188-3451">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="cb188-3451">\_bmk</span></span>



 

<span data-ttu-id="cb188-3452">**\_ hCursor:** valore a 32 bit che rappresenta l'handle dal messaggio CPMCreateQueryOut che identifica la query per cui recuperare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="cb188-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="cb188-3453">**\_ bmk:** valore a 32 bit che indica l'handle di un segnalibro la cui posizione deve essere recuperata.</span><span class="sxs-lookup"><span data-stu-id="cb188-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="cb188-3454">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="cb188-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="cb188-3455">Il messaggio CPMGetQueryStatusExOut risponde a un messaggio CPMGetQueryStatusExIn con lo stato della query e altre informazioni sullo stato, come descritto nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="cb188-3456">Il formato del messaggio CPMGetQueryStatusExOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-3457">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3457">0</span></span>

<span data-ttu-id="cb188-3458">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3458">1</span></span>

<span data-ttu-id="cb188-3459">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3459">2</span></span>

<span data-ttu-id="cb188-3460">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3460">3</span></span>

<span data-ttu-id="cb188-3461">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3461">4</span></span>

<span data-ttu-id="cb188-3462">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3462">5</span></span>

<span data-ttu-id="cb188-3463">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3463">6</span></span>

<span data-ttu-id="cb188-3464">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3464">7</span></span>

<span data-ttu-id="cb188-3465">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3465">8</span></span>

<span data-ttu-id="cb188-3466">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3466">9</span></span>

<span data-ttu-id="cb188-3467">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3467">1</span></span><br/> <span data-ttu-id="cb188-3468">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3468">0</span></span><br/>

<span data-ttu-id="cb188-3469">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3469">1</span></span>

<span data-ttu-id="cb188-3470">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3470">2</span></span>

<span data-ttu-id="cb188-3471">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3471">3</span></span>

<span data-ttu-id="cb188-3472">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3472">4</span></span>

<span data-ttu-id="cb188-3473">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3473">5</span></span>

<span data-ttu-id="cb188-3474">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3474">6</span></span>

<span data-ttu-id="cb188-3475">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3475">7</span></span>

<span data-ttu-id="cb188-3476">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3476">8</span></span>

<span data-ttu-id="cb188-3477">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3477">9</span></span>

<span data-ttu-id="cb188-3478">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3478">2</span></span><br/> <span data-ttu-id="cb188-3479">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3479">0</span></span><br/>

<span data-ttu-id="cb188-3480">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3480">1</span></span>

<span data-ttu-id="cb188-3481">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3481">2</span></span>

<span data-ttu-id="cb188-3482">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3482">3</span></span>

<span data-ttu-id="cb188-3483">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3483">4</span></span>

<span data-ttu-id="cb188-3484">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3484">5</span></span>

<span data-ttu-id="cb188-3485">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3485">6</span></span>

<span data-ttu-id="cb188-3486">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3486">7</span></span>

<span data-ttu-id="cb188-3487">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3487">8</span></span>

<span data-ttu-id="cb188-3488">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3488">9</span></span>

<span data-ttu-id="cb188-3489">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3489">3</span></span><br/> <span data-ttu-id="cb188-3490">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3490">0</span></span><br/>

<span data-ttu-id="cb188-3491">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3491">1</span></span>

<span data-ttu-id="cb188-3492">\_Stato</span><span class="sxs-lookup"><span data-stu-id="cb188-3492">\_Status</span></span>

<span data-ttu-id="cb188-3493">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="cb188-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="cb188-3494">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="cb188-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="cb188-3495">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="cb188-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="cb188-3496">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="cb188-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="cb188-3497">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="cb188-3497">\_iRowBmk</span></span>

<span data-ttu-id="cb188-3498">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="cb188-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="cb188-3499">**\_ Stato:** uno dei dati STAT \_ \* i valori specificati nella Sezione 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="cb188-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="cb188-3500">**\_ cFilteredDocuments:** intero senza segno a 32 bit che indica il numero di documenti indicizzati</span><span class="sxs-lookup"><span data-stu-id="cb188-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="cb188-3501">**\_ cDocumentsToFilter:** intero senza segno a 32 bit che indica il numero di documenti ancora da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="cb188-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="cb188-3502">**\_ dwRatioFinishedDenominator:** intero senza segno a 32 bit che indica il denominatore del rapporto tra i documenti che la query ha terminato l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="cb188-3503">**\_ dwRatioFinishedNumerator:** intero senza segno a 32 bit che indica il numeratore del rapporto tra i documenti che la query ha terminato l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="cb188-3504">**\_ iRowBmk:** intero senza segno a 32 bit che indica la posizione approssimativa del segnalibro nel set di righe in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="cb188-3505">**\_ cRowsTotal:** intero senza segno a 32 bit che specifica il numero totale di righe nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="cb188-3506">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="cb188-3507">Il messaggio CPMSetBindingsIn richiede l'associazione di colonne a un set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="cb188-3508">Il server risponderà al messaggio di richiesta CPMSetBindingsIn usando la sezione di intestazione del messaggio CPMBindingsIn con i risultati della richiesta contenuta nel \_ campo status.</span><span class="sxs-lookup"><span data-stu-id="cb188-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="cb188-3509">Il formato del messaggio CPMSetBindingsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3510">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3510">0</span></span>

<span data-ttu-id="cb188-3511">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3511">1</span></span>

<span data-ttu-id="cb188-3512">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3512">2</span></span>

<span data-ttu-id="cb188-3513">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3513">3</span></span>

<span data-ttu-id="cb188-3514">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3514">4</span></span>

<span data-ttu-id="cb188-3515">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3515">5</span></span>

<span data-ttu-id="cb188-3516">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3516">6</span></span>

<span data-ttu-id="cb188-3517">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3517">7</span></span>

<span data-ttu-id="cb188-3518">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3518">8</span></span>

<span data-ttu-id="cb188-3519">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3519">9</span></span>

<span data-ttu-id="cb188-3520">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3520">1</span></span><br/> <span data-ttu-id="cb188-3521">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3521">0</span></span><br/>

<span data-ttu-id="cb188-3522">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3522">1</span></span>

<span data-ttu-id="cb188-3523">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3523">2</span></span>

<span data-ttu-id="cb188-3524">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3524">3</span></span>

<span data-ttu-id="cb188-3525">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3525">4</span></span>

<span data-ttu-id="cb188-3526">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3526">5</span></span>

<span data-ttu-id="cb188-3527">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3527">6</span></span>

<span data-ttu-id="cb188-3528">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3528">7</span></span>

<span data-ttu-id="cb188-3529">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3529">8</span></span>

<span data-ttu-id="cb188-3530">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3530">9</span></span>

<span data-ttu-id="cb188-3531">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3531">2</span></span><br/> <span data-ttu-id="cb188-3532">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3532">0</span></span><br/>

<span data-ttu-id="cb188-3533">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3533">1</span></span>

<span data-ttu-id="cb188-3534">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3534">2</span></span>

<span data-ttu-id="cb188-3535">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3535">3</span></span>

<span data-ttu-id="cb188-3536">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3536">4</span></span>

<span data-ttu-id="cb188-3537">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3537">5</span></span>

<span data-ttu-id="cb188-3538">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3538">6</span></span>

<span data-ttu-id="cb188-3539">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3539">7</span></span>

<span data-ttu-id="cb188-3540">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3540">8</span></span>

<span data-ttu-id="cb188-3541">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3541">9</span></span>

<span data-ttu-id="cb188-3542">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3542">3</span></span><br/> <span data-ttu-id="cb188-3543">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3543">0</span></span><br/>

<span data-ttu-id="cb188-3544">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3544">1</span></span>

<span data-ttu-id="cb188-3545">\_hCursor (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="cb188-3546">\_cbRow (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="cb188-3547">\_cbBindingDesc (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="cb188-3548">\_fittizio (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3548">\_dummy (optional)</span></span>

<span data-ttu-id="cb188-3549">cColumns (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3549">cColumns (optional)</span></span>

<span data-ttu-id="cb188-3550">aColumns (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="cb188-3551">**\_ hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la riga per cui impostare le associazioni.</span><span class="sxs-lookup"><span data-stu-id="cb188-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="cb188-3552">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cb188-3553">**\_ cbRow:** intero senza segno a 32 bit che indica le dimensioni, in byte, di una riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="cb188-3554">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cb188-3555">**\_ cbBindingDesc:** intero senza segno a 32 bit che indica la lunghezza, in byte, dei campi che segue \_ il campo fittizio.</span><span class="sxs-lookup"><span data-stu-id="cb188-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="cb188-3556">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cb188-3557">**\_ fittizio:** questo campo non è usato e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="cb188-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="cb188-3558">Può essere impostato su qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="cb188-3559">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cb188-3560">**cColumns:** intero senza segno a 32 bit che indica il numero di elementi nella matrice aColumns.</span><span class="sxs-lookup"><span data-stu-id="cb188-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="cb188-3561">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cb188-3562">**aColumns:** matrice delle strutture CTableColumn che descrivono le colonne di una riga nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="cb188-3563">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cb188-3564">Le strutture nella matrice DEVONO essere separate da 0 a 3 byte di spaziatura interna in modo che ogni struttura abbia un allineamento a 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cb188-3565">Tali byte di spaziatura interna possono essere qualsiasi valore arbitrario e DEVONO essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="cb188-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="cb188-3566">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="cb188-3567">Il messaggio CPMGetRowsIn richiede righe da una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="cb188-3568">Il formato del messaggio CPMGetRowsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3569">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3569">0</span></span>

<span data-ttu-id="cb188-3570">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3570">1</span></span>

<span data-ttu-id="cb188-3571">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3571">2</span></span>

<span data-ttu-id="cb188-3572">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3572">3</span></span>

<span data-ttu-id="cb188-3573">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3573">4</span></span>

<span data-ttu-id="cb188-3574">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3574">5</span></span>

<span data-ttu-id="cb188-3575">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3575">6</span></span>

<span data-ttu-id="cb188-3576">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3576">7</span></span>

<span data-ttu-id="cb188-3577">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3577">8</span></span>

<span data-ttu-id="cb188-3578">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3578">9</span></span>

<span data-ttu-id="cb188-3579">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3579">1</span></span><br/> <span data-ttu-id="cb188-3580">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3580">0</span></span><br/>

<span data-ttu-id="cb188-3581">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3581">1</span></span>

<span data-ttu-id="cb188-3582">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3582">2</span></span>

<span data-ttu-id="cb188-3583">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3583">3</span></span>

<span data-ttu-id="cb188-3584">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3584">4</span></span>

<span data-ttu-id="cb188-3585">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3585">5</span></span>

<span data-ttu-id="cb188-3586">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3586">6</span></span>

<span data-ttu-id="cb188-3587">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3587">7</span></span>

<span data-ttu-id="cb188-3588">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3588">8</span></span>

<span data-ttu-id="cb188-3589">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3589">9</span></span>

<span data-ttu-id="cb188-3590">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3590">2</span></span><br/> <span data-ttu-id="cb188-3591">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3591">0</span></span><br/>

<span data-ttu-id="cb188-3592">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3592">1</span></span>

<span data-ttu-id="cb188-3593">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3593">2</span></span>

<span data-ttu-id="cb188-3594">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3594">3</span></span>

<span data-ttu-id="cb188-3595">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3595">4</span></span>

<span data-ttu-id="cb188-3596">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3596">5</span></span>

<span data-ttu-id="cb188-3597">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3597">6</span></span>

<span data-ttu-id="cb188-3598">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3598">7</span></span>

<span data-ttu-id="cb188-3599">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3599">8</span></span>

<span data-ttu-id="cb188-3600">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3600">9</span></span>

<span data-ttu-id="cb188-3601">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3601">3</span></span><br/> <span data-ttu-id="cb188-3602">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3602">0</span></span><br/>

<span data-ttu-id="cb188-3603">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3603">1</span></span>

<span data-ttu-id="cb188-3604">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cb188-3604">\_hCursor</span></span>

<span data-ttu-id="cb188-3605">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="cb188-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="cb188-3606">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="cb188-3606">\_cbRowWidth</span></span>

<span data-ttu-id="cb188-3607">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="cb188-3607">\_cbSeek</span></span>

<span data-ttu-id="cb188-3608">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="cb188-3608">\_cbReserved</span></span>

<span data-ttu-id="cb188-3609">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="cb188-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="cb188-3610">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="cb188-3610">\_ulClientBase</span></span>

<span data-ttu-id="cb188-3611">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="cb188-3611">\_fBwdFetch</span></span>

<span data-ttu-id="cb188-3612">eType</span><span class="sxs-lookup"><span data-stu-id="cb188-3612">eType</span></span>

<span data-ttu-id="cb188-3613">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cb188-3613">\_chapt</span></span>

<span data-ttu-id="cb188-3614">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="cb188-3614">SeekDescription</span></span>

<span data-ttu-id="cb188-3615">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3615">...</span></span>

<span data-ttu-id="cb188-3616">... (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3616">... (variable)</span></span>



 

<span data-ttu-id="cb188-3617">**\_ hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="cb188-3618">**\_ cRowsToTransfer:** intero senza segno a 32 bit che indica il numero massimo di righe che il client vuole ricevere in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="cb188-3619">**\_ cbRowWidth:** intero senza segno a 32 bit che indica la lunghezza di una riga, in byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="cb188-3620">**\_ cbSeek:** intero senza segno a 32 bit che indica la dimensione del messaggio che inizia con eType.</span><span class="sxs-lookup"><span data-stu-id="cb188-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="cb188-3621">**\_ cbReserved:** intero senza segno a 32 bit che indica le dimensioni, in byte, di un messaggio CPMGetRowsOut (senza i campi Rows e SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="cb188-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="cb188-3622">Questo valore in questo campo viene aggiunto al valore del campo cbSeek e quindi deve essere usato per calcolare l'offset del campo Rows nel messaggio \_ CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="cb188-3623">**\_ cbReadBuffer:** intero senza segno a 32 bit che DEVE essere impostato sul valore massimo di cbRowWidth o 1000 volte il valore di \_ cRowsToTransfer, arrotondato al multiplo di \_ 512 byte più vicino.</span><span class="sxs-lookup"><span data-stu-id="cb188-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="cb188-3624">Il valore NON DEVE superare 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="cb188-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="cb188-3625">**\_ ulClientBase:** intero senza segno a 32 bit che indica il valore di base da usare per i calcoli del puntatore nel buffer di riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="cb188-3626">Se vengono usati offset a 64 bit, il campo reserved2 dell'intestazione del messaggio viene usato come 32 bit superiori e ulClientBase come 32 bit inferiori di un valore \_ a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="cb188-3627">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="cb188-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="cb188-3628">**\_ fBwdFetch:** intero senza segno a 32 bit che indica l'ordine in cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="cb188-3629">Se impostato su 0x00000001, le righe devono essere recuperate in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="cb188-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="cb188-3630">Se impostato su 0x00000000, le righe devono essere recuperate in avanti.</span><span class="sxs-lookup"><span data-stu-id="cb188-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="cb188-3631">NON DEVE essere impostato su altri valori.</span><span class="sxs-lookup"><span data-stu-id="cb188-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="cb188-3632">**eType:** intero senza segno a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="cb188-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="cb188-3633">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-3633">Value</span></span>                         | <span data-ttu-id="cb188-3634">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="cb188-3635">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="cb188-3636">SeekDescription contiene una struttura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="cb188-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="cb188-3637">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="cb188-3638">SeekDescription contiene una struttura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="cb188-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="cb188-3639">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="cb188-3640">SeekDescription contiene una struttura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="cb188-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="cb188-3641">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="cb188-3642">SeekDescription contiene una struttura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="cb188-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="cb188-3643">**\_ chapt:** valore a 32 bit che rappresenta l'handle del capitolo del set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="cb188-3644">**SeekDescription:** questo campo DEVE contenere una struttura del tipo indicato dal valore eType.</span><span class="sxs-lookup"><span data-stu-id="cb188-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="cb188-3645">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="cb188-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="cb188-3646">Il messaggio CPMGetRowsOut risponde a un messaggio CPMGetRowsIn con le righe di una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="cb188-3647">I server DEVONO formattare gli offset ai tipi di dati a lunghezza variabile nel campo Righe come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="cb188-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="cb188-3648">Il client ha indicato che si tratta di un sistema a 32 bit (0x00000008 o meno nel campo iClientVersion di CPMConnectIn): gli offset sono numeri interi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="cb188-3649">Il client ha indicato che si tratta di un sistema a 64 bit ( iClientVersion > 0x00000008 in CPMConnectIn) e Il server ha indicato che si tratta di un sistema a 32 bit ( serverVersion impostato su \_ 0x00000007 in CPMConnectOut): gli offset sono numeri interi a \_ 32 bit</span><span class="sxs-lookup"><span data-stu-id="cb188-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="cb188-3650">Il client ha indicato che si tratta di un sistema a 64 bit ( iClientVersion > 0x00000008 in CPMConnectIn) e Il server ha indicato che si tratta di un sistema a 64 bit ( serverVersion impostato su \_ 0x00010007 in CPMConnectOut): gli offset sono numeri interi a \_ 64 bit</span><span class="sxs-lookup"><span data-stu-id="cb188-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="cb188-3651">Il formato del messaggio CPMGetRowsOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-3652">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3652">0</span></span>

<span data-ttu-id="cb188-3653">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3653">1</span></span>

<span data-ttu-id="cb188-3654">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3654">2</span></span>

<span data-ttu-id="cb188-3655">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3655">3</span></span>

<span data-ttu-id="cb188-3656">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3656">4</span></span>

<span data-ttu-id="cb188-3657">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3657">5</span></span>

<span data-ttu-id="cb188-3658">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3658">6</span></span>

<span data-ttu-id="cb188-3659">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3659">7</span></span>

<span data-ttu-id="cb188-3660">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3660">8</span></span>

<span data-ttu-id="cb188-3661">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3661">9</span></span>

<span data-ttu-id="cb188-3662">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3662">1</span></span><br/> <span data-ttu-id="cb188-3663">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3663">0</span></span><br/>

<span data-ttu-id="cb188-3664">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3664">1</span></span>

<span data-ttu-id="cb188-3665">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3665">2</span></span>

<span data-ttu-id="cb188-3666">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3666">3</span></span>

<span data-ttu-id="cb188-3667">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3667">4</span></span>

<span data-ttu-id="cb188-3668">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3668">5</span></span>

<span data-ttu-id="cb188-3669">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3669">6</span></span>

<span data-ttu-id="cb188-3670">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3670">7</span></span>

<span data-ttu-id="cb188-3671">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3671">8</span></span>

<span data-ttu-id="cb188-3672">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3672">9</span></span>

<span data-ttu-id="cb188-3673">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3673">2</span></span><br/> <span data-ttu-id="cb188-3674">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3674">0</span></span><br/>

<span data-ttu-id="cb188-3675">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3675">1</span></span>

<span data-ttu-id="cb188-3676">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3676">2</span></span>

<span data-ttu-id="cb188-3677">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3677">3</span></span>

<span data-ttu-id="cb188-3678">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3678">4</span></span>

<span data-ttu-id="cb188-3679">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3679">5</span></span>

<span data-ttu-id="cb188-3680">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3680">6</span></span>

<span data-ttu-id="cb188-3681">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3681">7</span></span>

<span data-ttu-id="cb188-3682">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3682">8</span></span>

<span data-ttu-id="cb188-3683">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3683">9</span></span>

<span data-ttu-id="cb188-3684">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3684">3</span></span><br/> <span data-ttu-id="cb188-3685">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3685">0</span></span><br/>

<span data-ttu-id="cb188-3686">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3686">1</span></span>

<span data-ttu-id="cb188-3687">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="cb188-3687">\_cRowsReturned</span></span>

<span data-ttu-id="cb188-3688">eType</span><span class="sxs-lookup"><span data-stu-id="cb188-3688">eType</span></span>

<span data-ttu-id="cb188-3689">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cb188-3689">\_chapt</span></span>

<span data-ttu-id="cb188-3690">SeekDescription (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="cb188-3691">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3691">...</span></span>

<span data-ttu-id="cb188-3692">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3692">...</span></span>

<span data-ttu-id="cb188-3693">paddingRows (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="cb188-3694">Righe</span><span class="sxs-lookup"><span data-stu-id="cb188-3694">Rows</span></span>



 

<span data-ttu-id="cb188-3695">**\_ cRowsReturned:** intero senza segno a 32 bit che indica il numero di righe restituite in Rows.</span><span class="sxs-lookup"><span data-stu-id="cb188-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="cb188-3696">**eType:** intero senza segno a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione rowseek da eseguire</span><span class="sxs-lookup"><span data-stu-id="cb188-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="cb188-3697">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-3697">Value</span></span>                         | <span data-ttu-id="cb188-3698">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="cb188-3699">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="cb188-3700">No SeekDescription, ignora il campo SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="cb188-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="cb188-3701">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="cb188-3702">SeekDescription contiene una struttura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="cb188-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="cb188-3703">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="cb188-3704">SeekDescription contiene una struttura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="cb188-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="cb188-3705">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="cb188-3706">SeekDescription contiene una struttura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="cb188-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="cb188-3707">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="cb188-3708">SeekDescription contiene una struttura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="cb188-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="cb188-3709">**\_ chapt:** valore a 32 bit che rappresenta l'handle del capitolo del set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="cb188-3710">**SeekDescription:** questo campo DEVE contenere una struttura del tipo indicato dal campo eType.</span><span class="sxs-lookup"><span data-stu-id="cb188-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="cb188-3711">**paddingRows:** questo campo DEVE essere di lunghezza sufficiente (da 0 a cbReserved-1 byte) per riempire il campo Rows per l'offset cbReserved dall'inizio di un messaggio, dove cbReserved è il valore nel messaggio \_ \_ \_ CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="cb188-3712">I byte di riempimento usati in questo campo possono essere qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="cb188-3713">Questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cb188-3714">**Righe:** i dati delle righe vengono formattati in base alle informazioni sulla colonna nel messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="cb188-3715">Le righe DEVONO essere archiviate in avanti (ad esempio, la riga 1 prima della riga 2).</span><span class="sxs-lookup"><span data-stu-id="cb188-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="cb188-3716">Le colonne a dimensione fissa DEVONO essere archiviate in corrispondenza degli offset specificati dal messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="cb188-3717">Le colonne a dimensione variabile (ad esempio, stringhe) DEVONO essere archiviate come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="cb188-3718">I dati della variabile stessa (ad esempio, la stringa) vengono archiviati vicino alla fine del buffer in ordine decrescente(ad esempio, la raccolta di tutti i dati delle variabili per la riga 1 si trova alla fine, la riga 2 più vicina e così via).</span><span class="sxs-lookup"><span data-stu-id="cb188-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="cb188-3719">L'area a dimensione fissa (all'inizio del buffer di riga) DEVE contenere un CRowVariant per ogni colonna, archiviato in corrispondenza dell'offset specificato nel messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="cb188-3720">vType DEVE contenere il tipo di dati ,ad esempio VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="cb188-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="cb188-3721">Se, come determinato dalle regole all'inizio di questa sezione, vengono usati offset a 32 bit, il campo Offset in CRowVariant MUST contiene un valore a 32 bit che rappresenta l'offset dei dati della variabile dall'inizio del messaggio CPMGetRowsOut, oltre al valore di ulClientBase specificato nel messaggio \_ CPMGetRowsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="cb188-3722">Se vengono usati offset a 64 bit, il campo Offset in CRowVariant MUST contiene un valore a 64 bit che rappresenta l'offset dall'inizio del messaggio CPMGetRowsOut, aggiunto a un valore a 64 bit composto usando ulClientBase come minimo \_ a 32 bit e ulReserved2 come valori a \_ 32 bit alti.</span><span class="sxs-lookup"><span data-stu-id="cb188-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="cb188-3723">Ad esempio, se il messaggio CPMSetBindingsIn ha specificato due colonne Size (VT \_ I4) e Title (VT \_ LPWSTR) e \_ ulClientBase da CPMGetRowsIn è 0x10000, due righe verranno visualizzate come segue.</span><span class="sxs-lookup"><span data-stu-id="cb188-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="cb188-3724">La sezione contrassegnata in grigio è la parte a lunghezza fissa del buffer.</span><span class="sxs-lookup"><span data-stu-id="cb188-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![Esempio di messaggio cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="cb188-3726">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="cb188-3727">Il messaggio CPMRatioFinishedIn richiede la percentuale di completamento di una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="cb188-3728">Il formato del messaggio CPMRatioFinishedIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3729">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3729">0</span></span>

<span data-ttu-id="cb188-3730">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3730">1</span></span>

<span data-ttu-id="cb188-3731">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3731">2</span></span>

<span data-ttu-id="cb188-3732">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3732">3</span></span>

<span data-ttu-id="cb188-3733">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3733">4</span></span>

<span data-ttu-id="cb188-3734">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3734">5</span></span>

<span data-ttu-id="cb188-3735">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3735">6</span></span>

<span data-ttu-id="cb188-3736">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3736">7</span></span>

<span data-ttu-id="cb188-3737">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3737">8</span></span>

<span data-ttu-id="cb188-3738">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3738">9</span></span>

<span data-ttu-id="cb188-3739">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3739">1</span></span><br/> <span data-ttu-id="cb188-3740">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3740">0</span></span><br/>

<span data-ttu-id="cb188-3741">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3741">1</span></span>

<span data-ttu-id="cb188-3742">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3742">2</span></span>

<span data-ttu-id="cb188-3743">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3743">3</span></span>

<span data-ttu-id="cb188-3744">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3744">4</span></span>

<span data-ttu-id="cb188-3745">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3745">5</span></span>

<span data-ttu-id="cb188-3746">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3746">6</span></span>

<span data-ttu-id="cb188-3747">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3747">7</span></span>

<span data-ttu-id="cb188-3748">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3748">8</span></span>

<span data-ttu-id="cb188-3749">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3749">9</span></span>

<span data-ttu-id="cb188-3750">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3750">2</span></span><br/> <span data-ttu-id="cb188-3751">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3751">0</span></span><br/>

<span data-ttu-id="cb188-3752">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3752">1</span></span>

<span data-ttu-id="cb188-3753">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3753">2</span></span>

<span data-ttu-id="cb188-3754">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3754">3</span></span>

<span data-ttu-id="cb188-3755">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3755">4</span></span>

<span data-ttu-id="cb188-3756">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3756">5</span></span>

<span data-ttu-id="cb188-3757">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3757">6</span></span>

<span data-ttu-id="cb188-3758">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3758">7</span></span>

<span data-ttu-id="cb188-3759">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3759">8</span></span>

<span data-ttu-id="cb188-3760">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3760">9</span></span>

<span data-ttu-id="cb188-3761">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3761">3</span></span><br/> <span data-ttu-id="cb188-3762">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3762">0</span></span><br/>

<span data-ttu-id="cb188-3763">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3763">1</span></span>

<span data-ttu-id="cb188-3764">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cb188-3764">\_hCursor</span></span>

<span data-ttu-id="cb188-3765">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="cb188-3765">\_fQuick</span></span>



 

<span data-ttu-id="cb188-3766">**\_ hCursor:** handle del messaggio CPMCreateQueryOut che identifica la query per cui richiedere informazioni di completamento.</span><span class="sxs-lookup"><span data-stu-id="cb188-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="cb188-3767">**\_ fQuick:** DEVE essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="cb188-3768">Non usato e DEVE essere ignorato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="cb188-3769">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="cb188-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="cb188-3770">Il messaggio CPMRatioFinishedOut risponde a un messaggio CPMRatioFinishedIn con il rapporto di completamento di una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="cb188-3771">Il formato del messaggio CPMRatioFinishedOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-3772">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3772">0</span></span>

<span data-ttu-id="cb188-3773">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3773">1</span></span>

<span data-ttu-id="cb188-3774">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3774">2</span></span>

<span data-ttu-id="cb188-3775">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3775">3</span></span>

<span data-ttu-id="cb188-3776">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3776">4</span></span>

<span data-ttu-id="cb188-3777">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3777">5</span></span>

<span data-ttu-id="cb188-3778">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3778">6</span></span>

<span data-ttu-id="cb188-3779">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3779">7</span></span>

<span data-ttu-id="cb188-3780">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3780">8</span></span>

<span data-ttu-id="cb188-3781">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3781">9</span></span>

<span data-ttu-id="cb188-3782">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3782">1</span></span><br/> <span data-ttu-id="cb188-3783">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3783">0</span></span><br/>

<span data-ttu-id="cb188-3784">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3784">1</span></span>

<span data-ttu-id="cb188-3785">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3785">2</span></span>

<span data-ttu-id="cb188-3786">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3786">3</span></span>

<span data-ttu-id="cb188-3787">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3787">4</span></span>

<span data-ttu-id="cb188-3788">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3788">5</span></span>

<span data-ttu-id="cb188-3789">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3789">6</span></span>

<span data-ttu-id="cb188-3790">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3790">7</span></span>

<span data-ttu-id="cb188-3791">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3791">8</span></span>

<span data-ttu-id="cb188-3792">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3792">9</span></span>

<span data-ttu-id="cb188-3793">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3793">2</span></span><br/> <span data-ttu-id="cb188-3794">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3794">0</span></span><br/>

<span data-ttu-id="cb188-3795">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3795">1</span></span>

<span data-ttu-id="cb188-3796">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3796">2</span></span>

<span data-ttu-id="cb188-3797">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3797">3</span></span>

<span data-ttu-id="cb188-3798">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3798">4</span></span>

<span data-ttu-id="cb188-3799">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3799">5</span></span>

<span data-ttu-id="cb188-3800">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3800">6</span></span>

<span data-ttu-id="cb188-3801">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3801">7</span></span>

<span data-ttu-id="cb188-3802">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3802">8</span></span>

<span data-ttu-id="cb188-3803">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3803">9</span></span>

<span data-ttu-id="cb188-3804">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3804">3</span></span><br/> <span data-ttu-id="cb188-3805">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3805">0</span></span><br/>

<span data-ttu-id="cb188-3806">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3806">1</span></span>

<span data-ttu-id="cb188-3807">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="cb188-3807">\_ ulNumerator</span></span>

<span data-ttu-id="cb188-3808">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="cb188-3808">\_ulDenominator</span></span>

<span data-ttu-id="cb188-3809">\_Corvi</span><span class="sxs-lookup"><span data-stu-id="cb188-3809">\_cRows</span></span>

<span data-ttu-id="cb188-3810">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="cb188-3810">\_fNewRows</span></span>



 

<span data-ttu-id="cb188-3811">**\_ ulNumerator:** intero senza segno a 32 bit che indica il numeratore del rapporto di completamento in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="cb188-3812">**\_ ulDenominator:** intero senza segno a 32 bit che indica il denominatore del rapporto di completamento in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="cb188-3813">DEVE essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="cb188-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="cb188-3814">**\_ cRows:** intero senza segno a 32 bit che indica il numero totale di righe per la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="cb188-3815">**\_ fNewRows:** valore booleano che indica se sono disponibili nuove righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="cb188-3816">Il valore 0x00000001 indica che nel set di righe sono disponibili nuove righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="cb188-3817">Il valore 0x00000000 indica che il set di righe non contiene nuove righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="cb188-3818">Questo campo NON DEVE essere impostato su altri valori.</span><span class="sxs-lookup"><span data-stu-id="cb188-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="cb188-3819">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="cb188-3820">Il messaggio CPMFetchValueIn richiede un valore della proprietà troppo grande per essere restituito in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="cb188-3821">Come specificato nella sezione 3.2.4.2.5, questo messaggio viene inviato ripetutamente per recuperare tutti i byte della proprietà, aggiornando cbSoFar per ognuno, fino a quando il campo fMoreExists del messaggio \_ \_ CPMFetchValueOut non è impostato su **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="cb188-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="cb188-3822">Il formato del messaggio CPMFetchValueIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3823">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3823">0</span></span>

<span data-ttu-id="cb188-3824">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3824">1</span></span>

<span data-ttu-id="cb188-3825">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3825">2</span></span>

<span data-ttu-id="cb188-3826">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3826">3</span></span>

<span data-ttu-id="cb188-3827">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3827">4</span></span>

<span data-ttu-id="cb188-3828">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3828">5</span></span>

<span data-ttu-id="cb188-3829">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3829">6</span></span>

<span data-ttu-id="cb188-3830">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3830">7</span></span>

<span data-ttu-id="cb188-3831">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3831">8</span></span>

<span data-ttu-id="cb188-3832">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3832">9</span></span>

<span data-ttu-id="cb188-3833">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3833">1</span></span><br/> <span data-ttu-id="cb188-3834">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3834">0</span></span><br/>

<span data-ttu-id="cb188-3835">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3835">1</span></span>

<span data-ttu-id="cb188-3836">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3836">2</span></span>

<span data-ttu-id="cb188-3837">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3837">3</span></span>

<span data-ttu-id="cb188-3838">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3838">4</span></span>

<span data-ttu-id="cb188-3839">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3839">5</span></span>

<span data-ttu-id="cb188-3840">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3840">6</span></span>

<span data-ttu-id="cb188-3841">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3841">7</span></span>

<span data-ttu-id="cb188-3842">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3842">8</span></span>

<span data-ttu-id="cb188-3843">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3843">9</span></span>

<span data-ttu-id="cb188-3844">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3844">2</span></span><br/> <span data-ttu-id="cb188-3845">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3845">0</span></span><br/>

<span data-ttu-id="cb188-3846">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3846">1</span></span>

<span data-ttu-id="cb188-3847">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3847">2</span></span>

<span data-ttu-id="cb188-3848">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3848">3</span></span>

<span data-ttu-id="cb188-3849">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3849">4</span></span>

<span data-ttu-id="cb188-3850">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3850">5</span></span>

<span data-ttu-id="cb188-3851">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3851">6</span></span>

<span data-ttu-id="cb188-3852">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3852">7</span></span>

<span data-ttu-id="cb188-3853">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3853">8</span></span>

<span data-ttu-id="cb188-3854">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3854">9</span></span>

<span data-ttu-id="cb188-3855">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3855">3</span></span><br/> <span data-ttu-id="cb188-3856">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3856">0</span></span><br/>

<span data-ttu-id="cb188-3857">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3857">1</span></span>

<span data-ttu-id="cb188-3858">\_Wid</span><span class="sxs-lookup"><span data-stu-id="cb188-3858">\_wid</span></span>

<span data-ttu-id="cb188-3859">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="cb188-3859">\_cbSoFar</span></span>

<span data-ttu-id="cb188-3860">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="cb188-3860">\_cbPropSpec</span></span>

<span data-ttu-id="cb188-3861">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="cb188-3861">\_cbChunk</span></span>

<span data-ttu-id="cb188-3862">PropSpec (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3862">PropSpec (variable)</span></span>

<span data-ttu-id="cb188-3863">...</span><span class="sxs-lookup"><span data-stu-id="cb188-3863">...</span></span>

<span data-ttu-id="cb188-3864">\_padding (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="cb188-3865">**\_ wid:** intero senza segno a 32 bit contenente informazioni sull'ID documento che identifica il documento per cui deve essere recuperata una proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-3865">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="cb188-3866">**\_ cbSoFar:** intero senza segno a 32 bit contenente il numero di byte trasferiti in precedenza per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="cb188-3867">DEVE essere impostato su 0x00000000 nel primo messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="cb188-3868">**\_ cbPropSpec:** intero senza segno a 32 bit contenente le dimensioni del campo PropSpec, in byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="cb188-3869">**\_ cbChunk:** intero senza segno a 32 bit contenente il numero massimo di byte che il mittente può accettare in un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="cb188-3870">*Comportamento di Windows: questo campo è impostato su 0x00004000 per tutte le versioni di Windows.*</span><span class="sxs-lookup"><span data-stu-id="cb188-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="cb188-3871">**PropSpec:** struttura CFullPropSpec che specifica la proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="cb188-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="cb188-3872">**\_ padding:** questo campo DEVE essere della lunghezza necessaria (da 0 a 3 byte) per riempire il messaggio su un multiplo di 4 byte di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="cb188-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="cb188-3873">Il valore dei byte di spaziatura interna può essere qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="cb188-3874">Questo campo DEVE essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cb188-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="cb188-3875">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cb188-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="cb188-3876">Il messaggio CPMFetchValueOut risponde a un messaggio CPMFetchValueIn con un valore di proprietà di una query precedente.</span><span class="sxs-lookup"><span data-stu-id="cb188-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="cb188-3877">Come specificato nella sezione 3.1.5.2.8, questo messaggio viene inviato dopo ogni messaggio CPMFetchValueIn fino al trasferimento di tutti i byte della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="cb188-3878">Il formato del messaggio CPMFetchValueOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-3879">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3879">0</span></span>

<span data-ttu-id="cb188-3880">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3880">1</span></span>

<span data-ttu-id="cb188-3881">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3881">2</span></span>

<span data-ttu-id="cb188-3882">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3882">3</span></span>

<span data-ttu-id="cb188-3883">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3883">4</span></span>

<span data-ttu-id="cb188-3884">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3884">5</span></span>

<span data-ttu-id="cb188-3885">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3885">6</span></span>

<span data-ttu-id="cb188-3886">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3886">7</span></span>

<span data-ttu-id="cb188-3887">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3887">8</span></span>

<span data-ttu-id="cb188-3888">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3888">9</span></span>

<span data-ttu-id="cb188-3889">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3889">1</span></span><br/> <span data-ttu-id="cb188-3890">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3890">0</span></span><br/>

<span data-ttu-id="cb188-3891">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3891">1</span></span>

<span data-ttu-id="cb188-3892">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3892">2</span></span>

<span data-ttu-id="cb188-3893">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3893">3</span></span>

<span data-ttu-id="cb188-3894">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3894">4</span></span>

<span data-ttu-id="cb188-3895">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3895">5</span></span>

<span data-ttu-id="cb188-3896">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3896">6</span></span>

<span data-ttu-id="cb188-3897">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3897">7</span></span>

<span data-ttu-id="cb188-3898">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3898">8</span></span>

<span data-ttu-id="cb188-3899">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3899">9</span></span>

<span data-ttu-id="cb188-3900">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3900">2</span></span><br/> <span data-ttu-id="cb188-3901">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3901">0</span></span><br/>

<span data-ttu-id="cb188-3902">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3902">1</span></span>

<span data-ttu-id="cb188-3903">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3903">2</span></span>

<span data-ttu-id="cb188-3904">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3904">3</span></span>

<span data-ttu-id="cb188-3905">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3905">4</span></span>

<span data-ttu-id="cb188-3906">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3906">5</span></span>

<span data-ttu-id="cb188-3907">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3907">6</span></span>

<span data-ttu-id="cb188-3908">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3908">7</span></span>

<span data-ttu-id="cb188-3909">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3909">8</span></span>

<span data-ttu-id="cb188-3910">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3910">9</span></span>

<span data-ttu-id="cb188-3911">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3911">3</span></span><br/> <span data-ttu-id="cb188-3912">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3912">0</span></span><br/>

<span data-ttu-id="cb188-3913">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3913">1</span></span>

<span data-ttu-id="cb188-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="cb188-3914">\_cbValue</span></span>

<span data-ttu-id="cb188-3915">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="cb188-3915">\_fMoreExists</span></span>

<span data-ttu-id="cb188-3916">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="cb188-3916">\_fValueExists</span></span>

<span data-ttu-id="cb188-3917">vType</span><span class="sxs-lookup"><span data-stu-id="cb188-3917">vType</span></span>

<span data-ttu-id="cb188-3918">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="cb188-3918">vValue (variable)</span></span>



 

<span data-ttu-id="cb188-3919">**\_ cbValue:** intero senza segno a 32 bit contenente le dimensioni totali, in byte in vValue.</span><span class="sxs-lookup"><span data-stu-id="cb188-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="cb188-3920">**\_ fMoreExists:** valore booleano che indica se sono disponibili messaggi CPMFetchValueOut aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="cb188-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="cb188-3921">Se impostato su 0x00000001, sono presenti altri messaggi CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="cb188-3922">Se impostato su 0x00000000, non sono disponibili altri messaggi CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="cb188-3923">**\_ fValueExists:** valore booleano che indica se è presente un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="cb188-3924">Se impostato su 0x00000001, esiste un valore per la proprietà .</span><span class="sxs-lookup"><span data-stu-id="cb188-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="cb188-3925">Se impostato su 0x00000000, non esiste un valore per la proprietà .</span><span class="sxs-lookup"><span data-stu-id="cb188-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="cb188-3926">**vType:** valore dell'enumerazione VARENUM, vedere la sezione 2.2.1.1 per informazioni dettagliate, che descrivono il tipo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="cb188-3927">**vValue:** parte di una matrice di byte contenente una struttura SERIALIZEDPROPERTYVALUE come specificato nella sezione 2.2.1.32, dove l'offset dell'inizio della parte è il valore \_ di cbSoFar in CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="cb188-3928">La lunghezza della parte, indicata dal campo cbValue, DEVE essere uguale al valore di \_ \_ cbChunk in CPMFetchValueIn se fMoreExists è impostato su 0x00000001 e DEVE essere minore o uguale al valore di \_ cbChunk in caso \_ contrario.</span><span class="sxs-lookup"><span data-stu-id="cb188-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="cb188-3929">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="cb188-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="cb188-3930">Il messaggio CPMGetNotify richiede che il client voglia ricevere una notifica delle modifiche al set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="cb188-3931">Il messaggio NON DEVE includere un corpo. solo l'intestazione del messaggio, come specificato nella sezione 2.2.2, deve essere inviata.</span><span class="sxs-lookup"><span data-stu-id="cb188-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="cb188-3932">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="cb188-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="cb188-3933">Il messaggio CPMSendNotifyOut notifica al client una modifica ai risultati di una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="cb188-3934">Questo messaggio viene inviato solo quando si verifica una modifica.</span><span class="sxs-lookup"><span data-stu-id="cb188-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="cb188-3935">Il formato del messaggio CPMSendNotifyOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-3936">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3936">0</span></span>

<span data-ttu-id="cb188-3937">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3937">1</span></span>

<span data-ttu-id="cb188-3938">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3938">2</span></span>

<span data-ttu-id="cb188-3939">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3939">3</span></span>

<span data-ttu-id="cb188-3940">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3940">4</span></span>

<span data-ttu-id="cb188-3941">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3941">5</span></span>

<span data-ttu-id="cb188-3942">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3942">6</span></span>

<span data-ttu-id="cb188-3943">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3943">7</span></span>

<span data-ttu-id="cb188-3944">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3944">8</span></span>

<span data-ttu-id="cb188-3945">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3945">9</span></span>

<span data-ttu-id="cb188-3946">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3946">1</span></span><br/> <span data-ttu-id="cb188-3947">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3947">0</span></span><br/>

<span data-ttu-id="cb188-3948">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3948">1</span></span>

<span data-ttu-id="cb188-3949">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3949">2</span></span>

<span data-ttu-id="cb188-3950">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3950">3</span></span>

<span data-ttu-id="cb188-3951">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3951">4</span></span>

<span data-ttu-id="cb188-3952">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3952">5</span></span>

<span data-ttu-id="cb188-3953">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3953">6</span></span>

<span data-ttu-id="cb188-3954">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3954">7</span></span>

<span data-ttu-id="cb188-3955">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3955">8</span></span>

<span data-ttu-id="cb188-3956">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3956">9</span></span>

<span data-ttu-id="cb188-3957">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3957">2</span></span><br/> <span data-ttu-id="cb188-3958">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3958">0</span></span><br/>

<span data-ttu-id="cb188-3959">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3959">1</span></span>

<span data-ttu-id="cb188-3960">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3960">2</span></span>

<span data-ttu-id="cb188-3961">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3961">3</span></span>

<span data-ttu-id="cb188-3962">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3962">4</span></span>

<span data-ttu-id="cb188-3963">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3963">5</span></span>

<span data-ttu-id="cb188-3964">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3964">6</span></span>

<span data-ttu-id="cb188-3965">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3965">7</span></span>

<span data-ttu-id="cb188-3966">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3966">8</span></span>

<span data-ttu-id="cb188-3967">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3967">9</span></span>

<span data-ttu-id="cb188-3968">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3968">3</span></span><br/> <span data-ttu-id="cb188-3969">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3969">0</span></span><br/>

<span data-ttu-id="cb188-3970">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3970">1</span></span>

<span data-ttu-id="cb188-3971">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="cb188-3971">\_watchNotify</span></span>



 

<span data-ttu-id="cb188-3972">**\_ watchNotify:** modifica alla query.</span><span class="sxs-lookup"><span data-stu-id="cb188-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="cb188-3973">DEVE essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="cb188-3974">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-3974">Value</span></span>                                     | <span data-ttu-id="cb188-3975">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="cb188-3976">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="cb188-3977">Il numero di righe nel set di righe della query è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="cb188-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="cb188-3978">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="cb188-3979">La query è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cb188-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="cb188-3980">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="cb188-3981">La query è stata rieseguiti.</span><span class="sxs-lookup"><span data-stu-id="cb188-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="cb188-3982">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="cb188-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="cb188-3983">Il messaggio CPMGetApproximatePositionIn richiede la posizione approssimativa di un segnalibro in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="cb188-3984">Il formato del messaggio CPMGetApproximatePositionIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-3985">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3985">0</span></span>

<span data-ttu-id="cb188-3986">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3986">1</span></span>

<span data-ttu-id="cb188-3987">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3987">2</span></span>

<span data-ttu-id="cb188-3988">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3988">3</span></span>

<span data-ttu-id="cb188-3989">4</span><span class="sxs-lookup"><span data-stu-id="cb188-3989">4</span></span>

<span data-ttu-id="cb188-3990">5</span><span class="sxs-lookup"><span data-stu-id="cb188-3990">5</span></span>

<span data-ttu-id="cb188-3991">6</span><span class="sxs-lookup"><span data-stu-id="cb188-3991">6</span></span>

<span data-ttu-id="cb188-3992">7</span><span class="sxs-lookup"><span data-stu-id="cb188-3992">7</span></span>

<span data-ttu-id="cb188-3993">8</span><span class="sxs-lookup"><span data-stu-id="cb188-3993">8</span></span>

<span data-ttu-id="cb188-3994">9</span><span class="sxs-lookup"><span data-stu-id="cb188-3994">9</span></span>

<span data-ttu-id="cb188-3995">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3995">1</span></span><br/> <span data-ttu-id="cb188-3996">0</span><span class="sxs-lookup"><span data-stu-id="cb188-3996">0</span></span><br/>

<span data-ttu-id="cb188-3997">1</span><span class="sxs-lookup"><span data-stu-id="cb188-3997">1</span></span>

<span data-ttu-id="cb188-3998">2</span><span class="sxs-lookup"><span data-stu-id="cb188-3998">2</span></span>

<span data-ttu-id="cb188-3999">3</span><span class="sxs-lookup"><span data-stu-id="cb188-3999">3</span></span>

<span data-ttu-id="cb188-4000">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4000">4</span></span>

<span data-ttu-id="cb188-4001">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4001">5</span></span>

<span data-ttu-id="cb188-4002">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4002">6</span></span>

<span data-ttu-id="cb188-4003">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4003">7</span></span>

<span data-ttu-id="cb188-4004">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4004">8</span></span>

<span data-ttu-id="cb188-4005">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4005">9</span></span>

<span data-ttu-id="cb188-4006">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4006">2</span></span><br/> <span data-ttu-id="cb188-4007">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4007">0</span></span><br/>

<span data-ttu-id="cb188-4008">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4008">1</span></span>

<span data-ttu-id="cb188-4009">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4009">2</span></span>

<span data-ttu-id="cb188-4010">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4010">3</span></span>

<span data-ttu-id="cb188-4011">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4011">4</span></span>

<span data-ttu-id="cb188-4012">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4012">5</span></span>

<span data-ttu-id="cb188-4013">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4013">6</span></span>

<span data-ttu-id="cb188-4014">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4014">7</span></span>

<span data-ttu-id="cb188-4015">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4015">8</span></span>

<span data-ttu-id="cb188-4016">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4016">9</span></span>

<span data-ttu-id="cb188-4017">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4017">3</span></span><br/> <span data-ttu-id="cb188-4018">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4018">0</span></span><br/>

<span data-ttu-id="cb188-4019">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4019">1</span></span>

<span data-ttu-id="cb188-4020">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cb188-4020">\_hCursor</span></span>

<span data-ttu-id="cb188-4021">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cb188-4021">\_chapt</span></span>

<span data-ttu-id="cb188-4022">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="cb188-4022">\_bmk</span></span>



 

<span data-ttu-id="cb188-4023">**\_ hCursor:** valore a 32 bit che rappresenta il cursore di query ottenuto da CPMCreateQueryOut per il set di righe contenente il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="cb188-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="cb188-4024">**\_ chapt:** valore a 32 bit che rappresenta l'handle del capitolo contenente il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="cb188-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="cb188-4025">**\_ bmk:** valore a 32 bit che rappresenta l'handle del segnalibro per il quale recuperare la posizione approssimativa.</span><span class="sxs-lookup"><span data-stu-id="cb188-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="cb188-4026">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="cb188-4027">Il messaggio CPMGetApproximatePositionOut risponde a un messaggio CPMGetApproximatePositionIn che descrive la posizione approssimativa del segnalibro nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="cb188-4028">Il formato del messaggio CPMGetApproximatePositionOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-4029">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4029">0</span></span>

<span data-ttu-id="cb188-4030">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4030">1</span></span>

<span data-ttu-id="cb188-4031">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4031">2</span></span>

<span data-ttu-id="cb188-4032">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4032">3</span></span>

<span data-ttu-id="cb188-4033">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4033">4</span></span>

<span data-ttu-id="cb188-4034">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4034">5</span></span>

<span data-ttu-id="cb188-4035">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4035">6</span></span>

<span data-ttu-id="cb188-4036">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4036">7</span></span>

<span data-ttu-id="cb188-4037">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4037">8</span></span>

<span data-ttu-id="cb188-4038">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4038">9</span></span>

<span data-ttu-id="cb188-4039">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4039">1</span></span><br/> <span data-ttu-id="cb188-4040">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4040">0</span></span><br/>

<span data-ttu-id="cb188-4041">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4041">1</span></span>

<span data-ttu-id="cb188-4042">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4042">2</span></span>

<span data-ttu-id="cb188-4043">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4043">3</span></span>

<span data-ttu-id="cb188-4044">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4044">4</span></span>

<span data-ttu-id="cb188-4045">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4045">5</span></span>

<span data-ttu-id="cb188-4046">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4046">6</span></span>

<span data-ttu-id="cb188-4047">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4047">7</span></span>

<span data-ttu-id="cb188-4048">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4048">8</span></span>

<span data-ttu-id="cb188-4049">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4049">9</span></span>

<span data-ttu-id="cb188-4050">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4050">2</span></span><br/> <span data-ttu-id="cb188-4051">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4051">0</span></span><br/>

<span data-ttu-id="cb188-4052">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4052">1</span></span>

<span data-ttu-id="cb188-4053">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4053">2</span></span>

<span data-ttu-id="cb188-4054">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4054">3</span></span>

<span data-ttu-id="cb188-4055">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4055">4</span></span>

<span data-ttu-id="cb188-4056">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4056">5</span></span>

<span data-ttu-id="cb188-4057">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4057">6</span></span>

<span data-ttu-id="cb188-4058">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4058">7</span></span>

<span data-ttu-id="cb188-4059">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4059">8</span></span>

<span data-ttu-id="cb188-4060">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4060">9</span></span>

<span data-ttu-id="cb188-4061">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4061">3</span></span><br/> <span data-ttu-id="cb188-4062">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4062">0</span></span><br/>

<span data-ttu-id="cb188-4063">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4063">1</span></span>

<span data-ttu-id="cb188-4064">\_numerator</span><span class="sxs-lookup"><span data-stu-id="cb188-4064">\_numerator</span></span>

<span data-ttu-id="cb188-4065">\_denominator</span><span class="sxs-lookup"><span data-stu-id="cb188-4065">\_denominator</span></span>



 

<span data-ttu-id="cb188-4066">**\_ numeratore:** intero senza segno a 32 bit contenente il numero di riga del segnalibro nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="cb188-4067">Se non sono presenti righe, questo campo DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cb188-4068">**\_ denominator**: intero senza segno a 32 bit contenente il numero di righe nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="cb188-4069">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="cb188-4070">Il messaggio CPMCompareBmkIn richiede un confronto tra due segnalibri in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="cb188-4071">Il formato del messaggio CPMCompareBmkIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-4072">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4072">0</span></span>

<span data-ttu-id="cb188-4073">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4073">1</span></span>

<span data-ttu-id="cb188-4074">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4074">2</span></span>

<span data-ttu-id="cb188-4075">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4075">3</span></span>

<span data-ttu-id="cb188-4076">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4076">4</span></span>

<span data-ttu-id="cb188-4077">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4077">5</span></span>

<span data-ttu-id="cb188-4078">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4078">6</span></span>

<span data-ttu-id="cb188-4079">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4079">7</span></span>

<span data-ttu-id="cb188-4080">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4080">8</span></span>

<span data-ttu-id="cb188-4081">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4081">9</span></span>

<span data-ttu-id="cb188-4082">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4082">1</span></span><br/> <span data-ttu-id="cb188-4083">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4083">0</span></span><br/>

<span data-ttu-id="cb188-4084">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4084">1</span></span>

<span data-ttu-id="cb188-4085">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4085">2</span></span>

<span data-ttu-id="cb188-4086">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4086">3</span></span>

<span data-ttu-id="cb188-4087">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4087">4</span></span>

<span data-ttu-id="cb188-4088">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4088">5</span></span>

<span data-ttu-id="cb188-4089">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4089">6</span></span>

<span data-ttu-id="cb188-4090">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4090">7</span></span>

<span data-ttu-id="cb188-4091">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4091">8</span></span>

<span data-ttu-id="cb188-4092">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4092">9</span></span>

<span data-ttu-id="cb188-4093">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4093">2</span></span><br/> <span data-ttu-id="cb188-4094">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4094">0</span></span><br/>

<span data-ttu-id="cb188-4095">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4095">1</span></span>

<span data-ttu-id="cb188-4096">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4096">2</span></span>

<span data-ttu-id="cb188-4097">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4097">3</span></span>

<span data-ttu-id="cb188-4098">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4098">4</span></span>

<span data-ttu-id="cb188-4099">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4099">5</span></span>

<span data-ttu-id="cb188-4100">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4100">6</span></span>

<span data-ttu-id="cb188-4101">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4101">7</span></span>

<span data-ttu-id="cb188-4102">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4102">8</span></span>

<span data-ttu-id="cb188-4103">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4103">9</span></span>

<span data-ttu-id="cb188-4104">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4104">3</span></span><br/> <span data-ttu-id="cb188-4105">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4105">0</span></span><br/>

<span data-ttu-id="cb188-4106">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4106">1</span></span>

<span data-ttu-id="cb188-4107">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cb188-4107">\_hCursor</span></span>

<span data-ttu-id="cb188-4108">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cb188-4108">\_chapt</span></span>

<span data-ttu-id="cb188-4109">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="cb188-4109">\_bmkFirst</span></span>

<span data-ttu-id="cb188-4110">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="cb188-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="cb188-4111">\_**hCursor:** valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut per il set di righe contenente i segnalibri.</span><span class="sxs-lookup"><span data-stu-id="cb188-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="cb188-4112">\_**chapt:** valore a 32 bit che rappresenta l'handle del capitolo contenente i segnalibri da confrontare.</span><span class="sxs-lookup"><span data-stu-id="cb188-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="cb188-4113">\_**bmkFirst:** valore a 32 bit che rappresenta l'handle del primo segnalibro da confrontare.</span><span class="sxs-lookup"><span data-stu-id="cb188-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="cb188-4114">\_**bmkSecond:** valore a 32 bit che rappresenta l'handle al secondo segnalibro da confrontare.</span><span class="sxs-lookup"><span data-stu-id="cb188-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="cb188-4115">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="cb188-4116">Il messaggio CPMCompareBmkOut risponde a un messaggio CPMCompareBmkIn con il confronto dei due segnalibri nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="cb188-4117">Il formato del messaggio CPMCompareBmkOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-4118">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4118">0</span></span>

<span data-ttu-id="cb188-4119">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4119">1</span></span>

<span data-ttu-id="cb188-4120">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4120">2</span></span>

<span data-ttu-id="cb188-4121">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4121">3</span></span>

<span data-ttu-id="cb188-4122">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4122">4</span></span>

<span data-ttu-id="cb188-4123">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4123">5</span></span>

<span data-ttu-id="cb188-4124">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4124">6</span></span>

<span data-ttu-id="cb188-4125">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4125">7</span></span>

<span data-ttu-id="cb188-4126">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4126">8</span></span>

<span data-ttu-id="cb188-4127">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4127">9</span></span>

<span data-ttu-id="cb188-4128">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4128">1</span></span><br/> <span data-ttu-id="cb188-4129">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4129">0</span></span><br/>

<span data-ttu-id="cb188-4130">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4130">1</span></span>

<span data-ttu-id="cb188-4131">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4131">2</span></span>

<span data-ttu-id="cb188-4132">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4132">3</span></span>

<span data-ttu-id="cb188-4133">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4133">4</span></span>

<span data-ttu-id="cb188-4134">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4134">5</span></span>

<span data-ttu-id="cb188-4135">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4135">6</span></span>

<span data-ttu-id="cb188-4136">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4136">7</span></span>

<span data-ttu-id="cb188-4137">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4137">8</span></span>

<span data-ttu-id="cb188-4138">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4138">9</span></span>

<span data-ttu-id="cb188-4139">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4139">2</span></span><br/> <span data-ttu-id="cb188-4140">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4140">0</span></span><br/>

<span data-ttu-id="cb188-4141">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4141">1</span></span>

<span data-ttu-id="cb188-4142">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4142">2</span></span>

<span data-ttu-id="cb188-4143">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4143">3</span></span>

<span data-ttu-id="cb188-4144">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4144">4</span></span>

<span data-ttu-id="cb188-4145">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4145">5</span></span>

<span data-ttu-id="cb188-4146">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4146">6</span></span>

<span data-ttu-id="cb188-4147">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4147">7</span></span>

<span data-ttu-id="cb188-4148">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4148">8</span></span>

<span data-ttu-id="cb188-4149">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4149">9</span></span>

<span data-ttu-id="cb188-4150">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4150">3</span></span><br/> <span data-ttu-id="cb188-4151">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4151">0</span></span><br/>

<span data-ttu-id="cb188-4152">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4152">1</span></span>

<span data-ttu-id="cb188-4153">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="cb188-4153">\_dwComparison</span></span>



 

<span data-ttu-id="cb188-4154">\_**dwComparison:** uno dei valori seguenti, che indica le posizioni relative dei due segnalibri nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="cb188-4155">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-4155">Value</span></span>                               | <span data-ttu-id="cb188-4156">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cb188-4157">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="cb188-4158">Il primo segnalibro viene posizionato prima del secondo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="cb188-4159">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb188-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="cb188-4160">Il primo segnalibro ha la stessa posizione del secondo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="cb188-4161">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb188-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="cb188-4162">Il primo segnalibro viene posizionato dopo il secondo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="cb188-4163">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb188-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="cb188-4164">Il primo segnalibro non ha la stessa posizione del secondo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="cb188-4165">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb188-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="cb188-4166">Il primo segnalibro non è confrontabile con il secondo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="cb188-4167">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="cb188-4168">Il messaggio CPMRestartPositionIn sposta la posizione di recupero di un cursore all'inizio del capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="cb188-4169">Come specificato nella sezione 3.1.5.2.12, il server risponderà usando lo stesso messaggio, con i risultati della richiesta contenuti nel campo \_ stato dell'intestazione CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="cb188-4170">Il formato del messaggio CPMRestartPositionIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-4171">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4171">0</span></span>

<span data-ttu-id="cb188-4172">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4172">1</span></span>

<span data-ttu-id="cb188-4173">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4173">2</span></span>

<span data-ttu-id="cb188-4174">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4174">3</span></span>

<span data-ttu-id="cb188-4175">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4175">4</span></span>

<span data-ttu-id="cb188-4176">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4176">5</span></span>

<span data-ttu-id="cb188-4177">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4177">6</span></span>

<span data-ttu-id="cb188-4178">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4178">7</span></span>

<span data-ttu-id="cb188-4179">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4179">8</span></span>

<span data-ttu-id="cb188-4180">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4180">9</span></span>

<span data-ttu-id="cb188-4181">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4181">1</span></span><br/> <span data-ttu-id="cb188-4182">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4182">0</span></span><br/>

<span data-ttu-id="cb188-4183">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4183">1</span></span>

<span data-ttu-id="cb188-4184">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4184">2</span></span>

<span data-ttu-id="cb188-4185">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4185">3</span></span>

<span data-ttu-id="cb188-4186">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4186">4</span></span>

<span data-ttu-id="cb188-4187">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4187">5</span></span>

<span data-ttu-id="cb188-4188">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4188">6</span></span>

<span data-ttu-id="cb188-4189">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4189">7</span></span>

<span data-ttu-id="cb188-4190">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4190">8</span></span>

<span data-ttu-id="cb188-4191">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4191">9</span></span>

<span data-ttu-id="cb188-4192">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4192">2</span></span><br/> <span data-ttu-id="cb188-4193">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4193">0</span></span><br/>

<span data-ttu-id="cb188-4194">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4194">1</span></span>

<span data-ttu-id="cb188-4195">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4195">2</span></span>

<span data-ttu-id="cb188-4196">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4196">3</span></span>

<span data-ttu-id="cb188-4197">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4197">4</span></span>

<span data-ttu-id="cb188-4198">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4198">5</span></span>

<span data-ttu-id="cb188-4199">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4199">6</span></span>

<span data-ttu-id="cb188-4200">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4200">7</span></span>

<span data-ttu-id="cb188-4201">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4201">8</span></span>

<span data-ttu-id="cb188-4202">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4202">9</span></span>

<span data-ttu-id="cb188-4203">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4203">3</span></span><br/> <span data-ttu-id="cb188-4204">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4204">0</span></span><br/>

<span data-ttu-id="cb188-4205">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4205">1</span></span>

<span data-ttu-id="cb188-4206">\_hCursor (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="cb188-4207">\_chapt (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="cb188-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="cb188-4208">**\_ hCursor:** valore a 32 bit che rappresenta l'handle, ottenuto da un messaggio CPMCreateQueryOut, che identifica la query per cui riavviare la posizione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="cb188-4209">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cb188-4210">**\_ chapt:** valore a 32 bit che rappresenta l'handle di un capitolo da cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="cb188-4211">Questo campo DEVE essere presente quando il messaggio viene inviato dal client e DEVE essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="cb188-4212">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="cb188-4213">Il messaggio CPMFreeCursorIn richiede il rilascio di un cursore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="cb188-4214">Il formato del messaggio CPMFreeCursorIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="cb188-4215">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4215">0</span></span>

<span data-ttu-id="cb188-4216">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4216">1</span></span>

<span data-ttu-id="cb188-4217">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4217">2</span></span>

<span data-ttu-id="cb188-4218">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4218">3</span></span>

<span data-ttu-id="cb188-4219">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4219">4</span></span>

<span data-ttu-id="cb188-4220">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4220">5</span></span>

<span data-ttu-id="cb188-4221">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4221">6</span></span>

<span data-ttu-id="cb188-4222">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4222">7</span></span>

<span data-ttu-id="cb188-4223">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4223">8</span></span>

<span data-ttu-id="cb188-4224">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4224">9</span></span>

<span data-ttu-id="cb188-4225">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4225">1</span></span><br/> <span data-ttu-id="cb188-4226">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4226">0</span></span><br/>

<span data-ttu-id="cb188-4227">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4227">1</span></span>

<span data-ttu-id="cb188-4228">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4228">2</span></span>

<span data-ttu-id="cb188-4229">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4229">3</span></span>

<span data-ttu-id="cb188-4230">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4230">4</span></span>

<span data-ttu-id="cb188-4231">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4231">5</span></span>

<span data-ttu-id="cb188-4232">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4232">6</span></span>

<span data-ttu-id="cb188-4233">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4233">7</span></span>

<span data-ttu-id="cb188-4234">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4234">8</span></span>

<span data-ttu-id="cb188-4235">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4235">9</span></span>

<span data-ttu-id="cb188-4236">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4236">2</span></span><br/> <span data-ttu-id="cb188-4237">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4237">0</span></span><br/>

<span data-ttu-id="cb188-4238">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4238">1</span></span>

<span data-ttu-id="cb188-4239">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4239">2</span></span>

<span data-ttu-id="cb188-4240">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4240">3</span></span>

<span data-ttu-id="cb188-4241">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4241">4</span></span>

<span data-ttu-id="cb188-4242">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4242">5</span></span>

<span data-ttu-id="cb188-4243">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4243">6</span></span>

<span data-ttu-id="cb188-4244">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4244">7</span></span>

<span data-ttu-id="cb188-4245">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4245">8</span></span>

<span data-ttu-id="cb188-4246">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4246">9</span></span>

<span data-ttu-id="cb188-4247">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4247">3</span></span><br/> <span data-ttu-id="cb188-4248">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4248">0</span></span><br/>

<span data-ttu-id="cb188-4249">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4249">1</span></span>

<span data-ttu-id="cb188-4250">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cb188-4250">\_hCursor</span></span>



 

<span data-ttu-id="cb188-4251">**\_ hCursor:** valore a 32 bit che rappresenta l'handle del cursore dal messaggio CPMCreateQueryOut da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="cb188-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="cb188-4252">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="cb188-4253">Il messaggio CPMFreeCursorOut risponde a un messaggio CPMFreeCursorIn con i risultati della liberatura di un cursore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="cb188-4254">Il formato del messaggio CPMFreeCursorOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="cb188-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="cb188-4255">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4255">0</span></span>

<span data-ttu-id="cb188-4256">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4256">1</span></span>

<span data-ttu-id="cb188-4257">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4257">2</span></span>

<span data-ttu-id="cb188-4258">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4258">3</span></span>

<span data-ttu-id="cb188-4259">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4259">4</span></span>

<span data-ttu-id="cb188-4260">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4260">5</span></span>

<span data-ttu-id="cb188-4261">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4261">6</span></span>

<span data-ttu-id="cb188-4262">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4262">7</span></span>

<span data-ttu-id="cb188-4263">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4263">8</span></span>

<span data-ttu-id="cb188-4264">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4264">9</span></span>

<span data-ttu-id="cb188-4265">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4265">1</span></span><br/> <span data-ttu-id="cb188-4266">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4266">0</span></span><br/>

<span data-ttu-id="cb188-4267">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4267">1</span></span>

<span data-ttu-id="cb188-4268">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4268">2</span></span>

<span data-ttu-id="cb188-4269">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4269">3</span></span>

<span data-ttu-id="cb188-4270">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4270">4</span></span>

<span data-ttu-id="cb188-4271">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4271">5</span></span>

<span data-ttu-id="cb188-4272">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4272">6</span></span>

<span data-ttu-id="cb188-4273">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4273">7</span></span>

<span data-ttu-id="cb188-4274">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4274">8</span></span>

<span data-ttu-id="cb188-4275">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4275">9</span></span>

<span data-ttu-id="cb188-4276">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4276">2</span></span><br/> <span data-ttu-id="cb188-4277">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4277">0</span></span><br/>

<span data-ttu-id="cb188-4278">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4278">1</span></span>

<span data-ttu-id="cb188-4279">2</span><span class="sxs-lookup"><span data-stu-id="cb188-4279">2</span></span>

<span data-ttu-id="cb188-4280">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4280">3</span></span>

<span data-ttu-id="cb188-4281">4</span><span class="sxs-lookup"><span data-stu-id="cb188-4281">4</span></span>

<span data-ttu-id="cb188-4282">5</span><span class="sxs-lookup"><span data-stu-id="cb188-4282">5</span></span>

<span data-ttu-id="cb188-4283">6</span><span class="sxs-lookup"><span data-stu-id="cb188-4283">6</span></span>

<span data-ttu-id="cb188-4284">7</span><span class="sxs-lookup"><span data-stu-id="cb188-4284">7</span></span>

<span data-ttu-id="cb188-4285">8</span><span class="sxs-lookup"><span data-stu-id="cb188-4285">8</span></span>

<span data-ttu-id="cb188-4286">9</span><span class="sxs-lookup"><span data-stu-id="cb188-4286">9</span></span>

<span data-ttu-id="cb188-4287">3</span><span class="sxs-lookup"><span data-stu-id="cb188-4287">3</span></span><br/> <span data-ttu-id="cb188-4288">0</span><span class="sxs-lookup"><span data-stu-id="cb188-4288">0</span></span><br/>

<span data-ttu-id="cb188-4289">1</span><span class="sxs-lookup"><span data-stu-id="cb188-4289">1</span></span>

<span data-ttu-id="cb188-4290">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="cb188-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="cb188-4291">**\_ cCursorsRemaining:** intero senza segno a 32 bit che indica il numero di cursori ancora in uso per la query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="cb188-4292">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cb188-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="cb188-4293">Il messaggio CPMDisconnect termina la connessione con il server</span><span class="sxs-lookup"><span data-stu-id="cb188-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="cb188-4294">Il messaggio NON DEVE includere un corpo. deve essere inviata solo l'intestazione del messaggio, come specificato nella sezione 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="cb188-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="cb188-4295">2.2.4 Errori</span><span class="sxs-lookup"><span data-stu-id="cb188-4295">2.2.4 Errors</span></span>

<span data-ttu-id="cb188-4296">Tutti i messaggi del protocollo del servizio di indicizzazione del contenuto DEVONO 0x00000000 se l'operazione ha esito positivo; In caso contrario, restituiscono un codice di errore diverso da zero a 32 bit che può essere un valore HRESULT o NTSTATUS (vedere la sezione 1.8).</span><span class="sxs-lookup"><span data-stu-id="cb188-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="cb188-4297">Se un buffer è troppo piccolo per adattarsi a un risultato, deve essere restituito il codice di stato STATUS \_ INSUFFICIENT RESOURCES (0xC0000009A) e l'operazione non riuscita deve essere ritentata con un buffer più \_ grande.</span><span class="sxs-lookup"><span data-stu-id="cb188-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="cb188-4298">Tutti gli altri valori di errore DEVONO essere considerati uguali.</span><span class="sxs-lookup"><span data-stu-id="cb188-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="cb188-4299">Si noti che attualmente gli spazi di numerazione HRESULT e NTSTATUS non si sovrappongono se non con valori di significato identico, ma anche se dovevano essere conflitti in futuro, non causerebbe problemi di protocollo purché il valore per STATUS \_ RISORSE \_ INSUFFICIENTI rimane univoca, poiché tutti gli altri valori di errore vengono considerati uguali.</span><span class="sxs-lookup"><span data-stu-id="cb188-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="cb188-4300">3 Dettagli del protocollo</span><span class="sxs-lookup"><span data-stu-id="cb188-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="cb188-4301">3.1 Dettagli server</span><span class="sxs-lookup"><span data-stu-id="cb188-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="cb188-4302">3.2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="cb188-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="cb188-4303">Le richieste di messaggi CISP per l'esecuzione di query in remoto nei cataloghi del servizio di indicizzazione non richiedono alcuna sequenza specifica.</span><span class="sxs-lookup"><span data-stu-id="cb188-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="cb188-4304">È tuttavia consigliabile che il livello superiore rispetti una sequenza di messaggi significativa, ad esempio per i messaggi ricevuti da questa sequenza o con dati non validi, il server risponderà con un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="cb188-4305">Alcuni messaggi dipendono anche dal livello superiore che fornisce dati validi ricevuti nei messaggi in precedenza nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="cb188-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="cb188-4306">Una sequenza di messaggi tipica per una query semplice da un client a un computer remoto è illustrata nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![sequenza di messaggi per query semplice](images/protocoldetails.jpg)

<span data-ttu-id="cb188-4308">I messaggi rappresentati nel diagramma precedente rappresentano un subset di tutti i messaggi CISP usati per l'esecuzione di query su un catalogo del servizio di indicizzazione remoto.</span><span class="sxs-lookup"><span data-stu-id="cb188-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="cb188-4309">3.1 Dettagli del server</span><span class="sxs-lookup"><span data-stu-id="cb188-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="cb188-4310">3.1.1 Modello di dati astratto</span><span class="sxs-lookup"><span data-stu-id="cb188-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="cb188-4311">La sezione seguente specifica i dati e lo stato gestiti dal server CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="cb188-4312">I dati forniti in questo caso facilitano la spiegazione del comportamento del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="cb188-4313">Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il comportamento esterno sia coerente con quello descritto in questo documento.</span><span class="sxs-lookup"><span data-stu-id="cb188-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="cb188-4314">Un servizio di indicizzazione che implementa CISP DEVE mantenere gli elementi di dati astratti seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="cb188-4315">Elenco di client connessi al server</span><span class="sxs-lookup"><span data-stu-id="cb188-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="cb188-4316">Informazioni su ogni client, tra cui:</span><span class="sxs-lookup"><span data-stu-id="cb188-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="cb188-4317">Versione del client (come indicato nel messaggio CPMConnectIn specificato nella sezione 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="cb188-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="cb188-4318">Catalogo associato al client (da un messaggio CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="cb188-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="cb188-4319">Proprietà client aggiuntive come specificato nella sezione 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="cb188-4320">Query di ricerca del client</span><span class="sxs-lookup"><span data-stu-id="cb188-4320">Client's search query</span></span>
    -   <span data-ttu-id="cb188-4321">Elenco di handle di cursore per la query e posizione nel set di risultati per ogni handle.</span><span class="sxs-lookup"><span data-stu-id="cb188-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="cb188-4322">Set corrente di associazioni</span><span class="sxs-lookup"><span data-stu-id="cb188-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="cb188-4323">Stato corrente della query che include (per ogni cursore):</span><span class="sxs-lookup"><span data-stu-id="cb188-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="cb188-4324">Numero di righe nel risultato della query</span><span class="sxs-lookup"><span data-stu-id="cb188-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="cb188-4325">Numeratore e denominatore del completamento delle query</span><span class="sxs-lookup"><span data-stu-id="cb188-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="cb188-4326">Ultimo numero di righe, segnalato dal messaggio CPMRatioFinishedOut più recente per questo cursore</span><span class="sxs-lookup"><span data-stu-id="cb188-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="cb188-4327">Se la query viene monitorata dal server per le modifiche nei risultati della query e se viene monitorata, cosa è cambiato nei risultati della query dall'ultima volta che è stata segnalata al client da CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="cb188-4328">Elenco di handle di capitoli, serviti da questa query a un client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="cb188-4329">Elenco di handle di segnalibro per ogni cursore, servito da questa query a un client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="cb188-4330">Stato corrente del servizio di indicizzazione, che può essere "non inizializzato", "in esecuzione" o "in fase di arresto".</span><span class="sxs-lookup"><span data-stu-id="cb188-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="cb188-4331">Si noti che la maggior parte del server di ora è in stato "in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="cb188-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="cb188-4332">Di seguito è riportato il diagramma della macchina a stati per il server:</span><span class="sxs-lookup"><span data-stu-id="cb188-4332">Following is the state machine diagram for the server:</span></span>

    ![diagramma della macchina a stati del server del servizio di indicizzazione](images/abstractdatamodel.jpg)

-   <span data-ttu-id="cb188-4334">Informazioni per catalogo: numero di documenti indicizzati, dimensioni dell'indice, numero di chiavi univoche e così via (vedere la sezione 2.2.3.1 per l'elenco completo), stato (che corrisponde ai valori di dwNewState nella sezione 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="cb188-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="cb188-4335">Per ogni lingua supportata, un database di variazioni delle parole come descritto nella sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="cb188-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="cb188-4336">3.1.2 Timer</span><span class="sxs-lookup"><span data-stu-id="cb188-4336">3.1.2 Timers</span></span>

<span data-ttu-id="cb188-4337">Non sono necessari timer di protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="cb188-4338">3.1.3 Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="cb188-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="cb188-4339">Al momento dell'inizializzazione, il server DEVE impostare lo stato su "non inizializzato" e avviare l'ascolto dei messaggi nel named pipe specificato nella sezione 1.9.</span><span class="sxs-lookup"><span data-stu-id="cb188-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="cb188-4340">Dopo aver eseguito qualsiasi altra inizializzazione interna, DEVE passare allo stato "in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="cb188-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="cb188-4341">3.1.4 Eventi attivati di livello più alto</span><span class="sxs-lookup"><span data-stu-id="cb188-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="cb188-4342">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="cb188-4343">3.1.5 Regole di elaborazione e sequenziazione dei messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="cb188-4344">Ogni volta che si verifica un errore durante l'elaborazione di un messaggio inviato da un client, il server DEVE segnalare un errore al client come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="cb188-4345">Interrompere l'elaborazione del messaggio inviato dal client</span><span class="sxs-lookup"><span data-stu-id="cb188-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="cb188-4346">Rispondere con l'intestazione del messaggio (solo) del messaggio inviato dal client, mantenendo intatto \_ il campo msg.</span><span class="sxs-lookup"><span data-stu-id="cb188-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="cb188-4347">Impostare il \_ campo dello stato sul valore del codice di errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="cb188-4348">Quando arriva un messaggio, il server DEVE controllare il valore del campo msg per verificare se è un tipo noto (vedere la sezione \_ 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="cb188-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="cb188-4349">Se il tipo non è noto, deve segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="cb188-4350">Il server DEVE quindi convalidare il \_ valore del campo ulChecksum se il tipo di messaggio è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="cb188-4351">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="cb188-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="cb188-4352">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="cb188-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="cb188-4353">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="cb188-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="cb188-4354">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="cb188-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="cb188-4355">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="cb188-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="cb188-4356">Per convalidare il valore del campo ulChecksum, il server DEVE controllare il valore specificato nel \_ campo \_ iClientVersion nel messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="cb188-4357">Se il campo iClientVersion non è impostato su 0x00000008 e il campo ulChecksum non è impostato su 0x00000000, il server DEVE segnalare un errore \_ \_ STATUS INVALID PARAMETER \_ \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="cb188-4358">Il server NON DEVE convalidare il campo ulChecksum per i client e imposta il campo iClientVersion su un valore minore \_ \_ di 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="cb188-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="cb188-4359">Se il valore del campo iClientVersionfield è 0x00000008 o superiore, il server DEVE convalidare che il campo ulChecksum sia stato calcolato come specificato nella sezione \_ \_ 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="cb188-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="cb188-4360">Se il \_ valore ulChecksum non è valido, il server DEVE segnalare un errore STATUS \_ INVALID PARAMETER \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="cb188-4361">Successivamente, il server controlla in quale stato si trova.</span><span class="sxs-lookup"><span data-stu-id="cb188-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="cb188-4362">Se lo stato è "non inizializzato", il server DEVE segnalare un errore CI \_ E \_ NOT \_ INITIALIZED (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="cb188-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="cb188-4363">Se lo stato è "arresto" il server DEVE segnalare un errore CI \_ E \_ SHUTDOWN (0x80041812).</span><span class="sxs-lookup"><span data-stu-id="cb188-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="cb188-4364">Dopo che un'intestazione è stata determinata come valida e il server è in stato di "esecuzione", è necessario eseguire un'ulteriore elaborazione specifica del messaggio come specificato nelle sottosezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="cb188-4365">3.1.5.1 Gestione remota del catalogo del servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="cb188-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="cb188-4366">3.1.5.1.1 Ricezione di una richiesta CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="cb188-4367">Quando il server riceve una richiesta di messaggio CPMCIStateInOut dal client, il server DEVE prima controllare se il client è in un elenco di client connessi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="cb188-4368">Se il client non è presente nell'elenco, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="cb188-4369">In caso contrario, DEVE rispondere al client con un messaggio CPMCIStateInOut, inserendo le informazioni sul catalogo associato del client, come specificato nella sezione 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="cb188-4370">3.1.5.1.2 Ricezione di una richiesta CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="cb188-4371">Quando il server riceve una richiesta di messaggio CPMSetCatStateIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4372">Verificare che il client abbia accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4372">Check that client has administrative access.</span></span> <span data-ttu-id="cb188-4373">Se il client non dispone di accesso amministrativo, il server DEVE segnalare un errore STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="cb188-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cb188-4374">Se dwNewState non è uguale a CICAT ALL OPENED, modificare lo stato del catalogo specificato nel campo CatName come specificato dal \_ \_ campo \_ \_ dwNewState.</span><span class="sxs-lookup"><span data-stu-id="cb188-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="cb188-4375">Per altri dettagli, vedere la sezione 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="cb188-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="cb188-4376">Se il server non individua un catalogo con il nome specificato nel campo CatName, il server DEVE restituire un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4377">Rispondere al client con un messaggio CPMSetCatStateOut, in cui \_ dwOldState DEVE essere impostato sullo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="cb188-4378">Se dwNewState è uguale a CICAT ALL OPENED, il server DEVE controllare lo stato di tutti i cataloghi e, se tutti sono avviati, DEVE impostare dwOldState su 0x00000001 e in caso contrario impostare \_ \_ \_ \_ \_ dwOldState su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="cb188-4379">3.1.5.1.3 Ricezione di una richiesta CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="cb188-4380">Quando il server riceve una richiesta di messaggio CPMUpdateDocumentsIn, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4381">Controllare se il client è in un elenco di client connessi (a cui è associato un catalogo).</span><span class="sxs-lookup"><span data-stu-id="cb188-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="cb188-4382">Se il client non è presente nell'elenco, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4383">Verificare che il client abbia accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4383">Check that client has administrative access.</span></span> <span data-ttu-id="cb188-4384">Se il client non dispone dell'accesso amministrativo al server, il server DEVE segnalare un errore DI ACCESSO NEGATO \_ \_ (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="cb188-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cb188-4385">Avviare il processo di indicizzazione del percorso specificato dal client, eseguendo un'analisi completa o incrementale, a seconda del valore del campo \_ flag nel messaggio CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="cb188-4386">Se il percorso non è stato indicizzato in precedenza, deve essere aggiunto alla raccolta di percorsi indicizzati e viene eseguita un'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="cb188-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="cb188-4387">Se viene specificato un valore non valido del campo flag, il server DEVE agire come se il flag fosse impostato su \_ \_ UPD \_ INIT ed eseguire un'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="cb188-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="cb188-4388">Questa operazione DEVE essere eseguita nel catalogo associato al client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="cb188-4389">Rispondere al client con l'intestazione del messaggio per CPMUpdateDocumentsIn e impostare il campo dello stato sui \_ risultati della richiesta.</span><span class="sxs-lookup"><span data-stu-id="cb188-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="cb188-4390">3.1.5.1.4 Ricezione di una richiesta CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="cb188-4391">Quando il server riceve una richiesta di messaggio CPMForceMergeIn, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4392">Controllare se il client è in un elenco di client connessi (a cui è associato un catalogo).</span><span class="sxs-lookup"><span data-stu-id="cb188-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="cb188-4393">Se il client non è presente nell'elenco, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4394">Verificare che il client abbia accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4394">Check that client has administrative access.</span></span> <span data-ttu-id="cb188-4395">Se il client non ha accesso amministrativo, il server DEVE segnalare un errore STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="cb188-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cb188-4396">Avviare qualsiasi processo di manutenzione necessario per migliorare le prestazioni delle query in un catalogo, associato al client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="cb188-4397">Rispondere al client con un'intestazione di messaggio per CPMForceMergeIn e impostare il campo di stato \_ sui risultati della richiesta.</span><span class="sxs-lookup"><span data-stu-id="cb188-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="cb188-4398">Si noti che il processo di manutenzione è asincrono e può continuare dopo che il client ha ricevuto il messaggio di risposta.</span><span class="sxs-lookup"><span data-stu-id="cb188-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="cb188-4399">Questo processo non influisce direttamente sul protocollo ,oltre al tempo di risposta.</span><span class="sxs-lookup"><span data-stu-id="cb188-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="cb188-4400">3.1.5.2 Query del servizio di indicizzazione remoto</span><span class="sxs-lookup"><span data-stu-id="cb188-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="cb188-4401">3.1.5.2.1 Ricezione di una richiesta CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="cb188-4402">Quando il server riceve una richiesta CPMConnectIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4403">Controllare se il client è presente nell'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="cb188-4404">In questo caso, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4405">Verifica se il catalogo specificato esiste e non nello stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="cb188-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="cb188-4406">Se questo non è il caso, il server DEVE segnalare un errore CI \_ E \_ NO CATALOG \_ (0x8004181D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="cb188-4407">Aggiungere il client all'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="cb188-4408">Associare il catalogo al client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="cb188-4409">Archiviare le informazioni passate nel messaggio CPMConnectIn ,ad esempio il nome del catalogo, la versione del client e così via, nello stato client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="cb188-4410">Rispondere al client con un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="cb188-4411">3.1.5.2.2 Ricezione di una richiesta CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="cb188-4412">Quando il server riceve una richiesta di messaggio CPMCreateQueryIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4413">Controllare se il client è presente nell'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="cb188-4414">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4415">Controllare se al client è già associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="cb188-4416">In questo caso, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4417">Controllare se il catalogo associato al client è nello stato che consente l'elaborazione della query (CICAT \_ READONLY o CICAT \_ WRITABLE).</span><span class="sxs-lookup"><span data-stu-id="cb188-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="cb188-4418">In caso contrario, il server DEVE segnalare un errore QUERY \_ S \_ NO QUERY \_ (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="cb188-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="cb188-4419">Analizzare il set di restrizioni, i criteri di ordinamento e i raggruppamenti specificati nella query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="cb188-4420">Se il server rileva un errore, deve segnalare un errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="cb188-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="cb188-4421">Se questo passaggio ha esito negativo per qualsiasi altro motivo, il server DEVE segnalare l'errore rilevato.</span><span class="sxs-lookup"><span data-stu-id="cb188-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="cb188-4422">Per informazioni sugli errori di query del servizio di indicizzazione, \[ vedere MSDN-QUERYERR. \]</span><span class="sxs-lookup"><span data-stu-id="cb188-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="cb188-4423">Salvare la query di ricerca nello stato per il client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="cb188-4424">Eseguire le operazioni di preparazione necessarie per rendere disponibili le righe a un client e associare la query agli handle di cursore appropriati, a seconda delle informazioni passate nel messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="cb188-4425">Aggiungere tali handle all'elenco di handle di cursore del client e inizializzare elenchi di handle di capitolo e segnalibri.</span><span class="sxs-lookup"><span data-stu-id="cb188-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="cb188-4426">Inizializzare l'elenco di handle di capitolo per ogni cursore nella query al database \_ NULL \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="cb188-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="cb188-4427">Inizializzare l'elenco di handle di segnalibro per ogni cursore nella query su un set di DBBMK \_ FIRST e DBBMK \_ LAST.</span><span class="sxs-lookup"><span data-stu-id="cb188-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="cb188-4428">Contrassegnare la query come non monitorata per le modifiche.</span><span class="sxs-lookup"><span data-stu-id="cb188-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="cb188-4429">Inizializzare il numero di righe sul numero attualmente calcolato di righe (che può essere 0 se la query non ha avviato l'esecuzione o un numero se la query è in un processo di esecuzione) e inizializzare il numeratore e il denominatore del completamento della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="cb188-4430">Rispondere al client con un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="cb188-4431">3.1.5.2.3 Ricezione di una richiesta CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="cb188-4432">Quando il server riceve una richiesta di messaggio CPMGetQueryStatusIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4433">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="cb188-4434">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4435">Controllare se l'handle del cursore si trova in un elenco di handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="cb188-4436">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4437">Preparare un messaggio CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="cb188-4438">Il server DEVE recuperare lo stato della query corrente e impostarlo nel campo \_ QStatus (vedere 2.2.3.11 per i valori possibili).</span><span class="sxs-lookup"><span data-stu-id="cb188-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="cb188-4439">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cb188-4440">Rispondere al client con il messaggio CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="cb188-4441">3.1.5.2.4 Ricezione di una richiesta CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="cb188-4442">Quando il server riceve una richiesta di messaggio CPMGetQueryStatusExIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4443">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cb188-4444">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4445">Controllare se l'handle di cursore passato è in un elenco di handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="cb188-4446">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4447">Preparare un messaggio CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="cb188-4448">Il server DEVE recuperare lo stato corrente della query e lo stato della query e impostare QStatus (vedere 2.2.3.11 per i valori \_ possibili), dwRatioFinishedDenominator e \_ dwRatioFinishedNumerator rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="cb188-4449">Deve quindi impostare il numero di righe nei risultati della query \_ su cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="cb188-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="cb188-4450">Se questo passaggio ha esito negativo per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cb188-4451">Recuperare informazioni sul catalogo del client e compilare \_ cFilteredDocuments e \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="cb188-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="cb188-4452">Se per qualsiasi motivo questo passaggio ha esito negativo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cb188-4453">Recuperare la posizione del segnalibro indicato dall'handle nel campo bmk e compilare il campo iRowBmk rimanente nel messaggio \_ \_ CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="cb188-4454">Se questo passaggio ha esito negativo per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cb188-4455">Rispondere al client con il messaggio CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="cb188-4456">3.1.5.2.5 Ricezione di una richiesta CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="cb188-4457">Quando il server riceve una richiesta di messaggio CPMRatioFinishedIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4458">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="cb188-4459">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4460">Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cb188-4461">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4462">Preparare un messaggio CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="cb188-4463">Il server DEVE recuperare lo stato della query del client e compilare i campi \_ ulNumerator, \_ ulDenominator \_ e cRows.</span><span class="sxs-lookup"><span data-stu-id="cb188-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="cb188-4464">Se per qualsiasi motivo questo passaggio ha esito negativo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cb188-4465">Se cRows è uguale all'ultimo numero segnalato di righe per la query, impostare \_ fNewRows su 0x00000000, in caso contrario impostarlo \_ su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="cb188-4466">Aggiornare l'ultimo numero segnalato di righe per questa query al valore \_ di cRows.</span><span class="sxs-lookup"><span data-stu-id="cb188-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="cb188-4467">Rispondere al client con il messaggio CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="cb188-4468">3.1.5.2.6 Ricezione di una richiesta CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="cb188-4469">Quando il server riceve una richiesta di messaggio CPMSetBindingsIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4470">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cb188-4471">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4472">Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cb188-4473">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4474">Verificare che le informazioni sulle associazioni siano valide(ad esempio, la colonna specifica almeno il valore, la lunghezza o lo stato da restituire; nessuna sovrapposizione nelle associazioni per valore, lunghezza o stato; e valore, lunghezza e stato si adattano alle dimensioni della riga specificate) e, in caso contrario, segnalare un errore \_ DB E \_ BADBINDINFO (0x80040E08).</span><span class="sxs-lookup"><span data-stu-id="cb188-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="cb188-4475">Salvare le informazioni di associazione associate alle colonne specificate nel campo aColumns.</span><span class="sxs-lookup"><span data-stu-id="cb188-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="cb188-4476">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cb188-4477">Rispondere al client con un'intestazione del messaggio (solo) con msg impostato su CPMSetBindingsIn e stato impostato sui risultati \_ \_ dell'associazione specificata.</span><span class="sxs-lookup"><span data-stu-id="cb188-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="cb188-4478">3.1.5.2.7 Ricezione di una richiesta CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="cb188-4479">Quando il server riceve una richiesta di messaggio CPMGetRowsIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4480">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="cb188-4481">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4482">Controllare se l'handle di cursore passato è in athelist degli handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="cb188-4483">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4484">Controllare se il client ha un set corrente di associazioni.</span><span class="sxs-lookup"><span data-stu-id="cb188-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="cb188-4485">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4486">Preparare un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="cb188-4487">Il server DEVE posizionare il cursore nei risultati della query come indicato dalla descrizione della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="cb188-4488">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cb188-4489">Recuperare il numero di righe che rientra in un buffer, le cui dimensioni sono indicate da cbReadBuffer, ma non più di quanto indicato da \_ \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="cb188-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="cb188-4490">Quando si recuperano righe, il server DEVE confrontare il tipo di valore della proprietà di ogni colonna selezionata con il tipo specificato nel set corrente di associazioni del client (sezione 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="cb188-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="cb188-4491">Se il tipo nell'associazione non è VARIANT VT, il server DEVE tentare di convertire il valore della proprietà della colonna \_ in tale tipo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="cb188-4492">In caso contrario, se il flag DBPROP USEEXTENDEDDBTYPES è impostato nel set di proprietà DBPROPSET QUERYEXT del client o se il valore della proprietà della colonna non è un tipo VT VECTOR, il valore della proprietà DEVE essere restituito nel tipo \_ \_ \_ normale.</span><span class="sxs-lookup"><span data-stu-id="cb188-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="cb188-4493">In caso contrario, ad esempio se il server ha un tipo VT VECTOR e il client non supporta VT VECTOR, il server DEVE tentare di convertirlo in un tipo ARRAY VT come indicato di \_ \_ \_ seguito: VT \_ I8, \_ VT UI8, VT FILETIME e gli elementi della matrice \_ \_ CLSID VT non possono essere convertiti e hanno invece esito negativo. Gli elementi di matrice \_ VT LPSTR e VT LPWSTR DEVONO essere convertiti in VT BSTR. Gli elementi di matrice di tutti gli altri tipi \_ \_ DEVONO rimanere invariati.</span><span class="sxs-lookup"><span data-stu-id="cb188-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="cb188-4494">Infine, se le colonne di riga contengono handle di capitolo o di segnalibro, il server DEVE aggiornare gli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="cb188-4495">Se per qualsiasi motivo questo passaggio ha esito negativo, il server DEVE segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cb188-4496">Archiviare il numero effettivo di righe recuperate in \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="cb188-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="cb188-4497">Copiare la descrizione della ricerca e il campo del capitolo da CPMGetRowsIn a un messaggio CPMGetRowsOut da inviare.</span><span class="sxs-lookup"><span data-stu-id="cb188-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="cb188-4498">Archiviare le righe recuperate nel campo Righe (vedere la nota sul byte di stato di seguito e la sezione 2.2.3.16 sulla struttura del campo Righe).</span><span class="sxs-lookup"><span data-stu-id="cb188-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="cb188-4499">Rispondere al client con il messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="cb188-4500">Nota sul campo byte di stato:</span><span class="sxs-lookup"><span data-stu-id="cb188-4500">Note on status byte field:</span></span>

<span data-ttu-id="cb188-4501">Se StatusUsed è impostato su 0x01 nella colonna CTableColumn del messaggio CPMSetBindingIn per la colonna, il server DEVE impostare il byte di stato (che si trova in StatusOffset dall'inizio della riga) per questa colonna su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="cb188-4502">Valore</span><span class="sxs-lookup"><span data-stu-id="cb188-4502">Value</span></span> | <span data-ttu-id="cb188-4503">Significato</span><span class="sxs-lookup"><span data-stu-id="cb188-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="cb188-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="cb188-4504">0x00</span></span>  | <span data-ttu-id="cb188-4505">StatusOK</span><span class="sxs-lookup"><span data-stu-id="cb188-4505">StatusOK</span></span>       |
| <span data-ttu-id="cb188-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="cb188-4506">0x01</span></span>  | <span data-ttu-id="cb188-4507">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="cb188-4507">StatusDeferred</span></span> |
| <span data-ttu-id="cb188-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="cb188-4508">0x02</span></span>  | <span data-ttu-id="cb188-4509">StatusNull</span><span class="sxs-lookup"><span data-stu-id="cb188-4509">StatusNull</span></span>     |



 

<span data-ttu-id="cb188-4510">Se il valore della proprietà è assente per questa riga, il server DEVE impostare il byte di stato su StatusNull.</span><span class="sxs-lookup"><span data-stu-id="cb188-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="cb188-4511">Se il valore è troppo grande per essere trasferito nel messaggio CPMGetRowsOut, il server DEVE impostare il byte di stato su StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="cb188-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="cb188-4512">In caso contrario, il server DEVE impostare il byte di stato su StatusOK.</span><span class="sxs-lookup"><span data-stu-id="cb188-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="cb188-4513">3.1.5.2.8 Ricezione di una richiesta CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="cb188-4514">Quando il server riceve una richiesta di messaggio CPMFetchValueIn da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4515">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="cb188-4516">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4517">Preparare un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="cb188-4518">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cb188-4519">Trovare il documento indicato dal campo wid e verificare se l'ID proprietà per questo documento (in seguito indicato come "valore della proprietà") indicato dalla struttura PropSpec è disponibile per \_ questo client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="cb188-4520">Se questo valore non è disponibile, il server DEVE impostare fValueExists su 0x00000000 e in caso contrario impostare \_ \_ fValueExists su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="cb188-4521">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cb188-4522">Se \_ fValueExists è uguale a 0x00000001 il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="cb188-4523">Serializzare il valore della proprietà in una struttura SERIALIZEDPROPERTYVALUE e copiare, a partire \_ dall'offset cbSoFar, al massimo byte cbChunk (ma non oltre la fine della proprietà serializzata) nel campo \_ vValue.</span><span class="sxs-lookup"><span data-stu-id="cb188-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="cb188-4524">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="cb188-4525">Impostare \_ cbValue sul numero di byte copiati nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="cb188-4526">Impostare vType sul tipo di proprietà del valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="cb188-4527">Se la lunghezza della proprietà serializzata è maggiore di \_ cbSoFar aggiunta a \_ cbValue, impostare fMoreExists su 0x00000001, in caso contrario impostarla su \_ 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="cb188-4528">Rispondere al client con il messaggio CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="cb188-4529">3.1.5.2.9 Ricezione di una richiesta CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="cb188-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="cb188-4530">Quando il server riceve un messaggio CPMGetNotify da un client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4531">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="cb188-4532">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4533">Se non sono state apportate modifiche al set di risultati della query dall'ultimo messaggio CPMSendNotifyOut per questo client o se la query non è attualmente monitorata per le modifiche nel set di risultati, il server DEVE rispondere con il messaggio CPMGetNotify e iniziare a monitorare la query per le modifiche nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="cb188-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="cb188-4534">Se in un secondo momento si verifica una modifica nel set di risultati della query, il server DEVE inviare esattamente un messaggio CPMSendNotifyOut al client e DEVE specificare la modifica nel campo \_ watchNotify.</span><span class="sxs-lookup"><span data-stu-id="cb188-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="cb188-4535">Se sono state apportate modifiche al set di risultati della query dall'ultimo messaggio CPMSendNotifyOut, il server DEVE rispondere con CPMSendNotifyOut e DEVE specificare la modifica nel campo \_ watchNotify.</span><span class="sxs-lookup"><span data-stu-id="cb188-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="cb188-4536">Si noti che, nel caso di molte modifiche ai risultati della query, DBWATCHNOTIFY ROWSCHANGED ha la priorità,ad esempio, se la query è stata eseguita di nuovo e quindi il numero di righe modificate e la query è stata eseguita di nuovo, l'evento segnalato sarà \_ DBWATCHNOTIFY \_ ROWSCHANGED.</span><span class="sxs-lookup"><span data-stu-id="cb188-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="cb188-4537">3.1.5.2.10 Ricezione di una richiesta CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="cb188-4538">Quando il server riceve una richiesta di messaggio CPMGetApproximatePositionIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4539">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cb188-4540">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4541">Controllare se l'handle del cursore, l'handle del capitolo e l'handle del segnalibro passati si trova negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="cb188-4542">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4543">Trovare una riga associata all'handle del segnalibro nei risultati della query e approssimare la posizione della riga nel set di righe, a cui fa riferimento l'handle del capitolo, e determinare il numeratore e il denominatore per la posizione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="cb188-4544">Si noti che quando l'handle del capitolo è DB \_ NULL HCHAPTER, il capitolo corrispondente è il set di righe \_ principale della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="cb188-4545">Se questo passaggio non riesce per qualsiasi motivo, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cb188-4546">Rispondere al client con un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="cb188-4547">3.1.5.2.11 Ricezione di una richiesta CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="cb188-4548">Quando il server riceve una richiesta di messaggio CPMCompareBmkIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4549">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cb188-4550">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4551">Controllare se l'handle del cursore, l'handle del capitolo e gli handle dei segnalibri passati sono presenti negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="cb188-4552">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4553">Preparare un messaggio CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="cb188-4554">Se gli handle dei segnalibri sono uguali, \_ dwComparison MUST è impostato su DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="cb188-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="cb188-4555">In caso contrario, se uno degli handle di segnalibri è DBBMK FIRST o \_ DBBMK \_ LAST, \_ dwComparison DEVE essere impostato su DBCOMPARE \_ NE.</span><span class="sxs-lookup"><span data-stu-id="cb188-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="cb188-4556">In caso contrario, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="cb188-4557">Trovare le righe a cui fa riferimento ogni handle di segnalibro nei risultati della query</span><span class="sxs-lookup"><span data-stu-id="cb188-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="cb188-4558">Se una delle righe non si trova nel capitolo indicato dall'handle del capitolo in CPMCompareBmkIn, \_ dwComparison DEVE essere impostato su DBCOMPARE \_ NOTCOMPARABLE.</span><span class="sxs-lookup"><span data-stu-id="cb188-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="cb188-4559">In caso contrario, quando entrambe le righe sono nello stesso capitolo, il server DEVE approssimare una posizione di tali righe nel set di righe a cui fa riferimento l'handle di questo capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="cb188-4560">DEVE quindi confrontare i valori di posizione e impostare dwComparison su DBCOMPARE LT se la posizione della prima riga è minore della posizione della seconda riga; in caso \_ \_ \_ contrario, dwComparison MUST deve essere impostato su DBCOMPARE \_ GT.</span><span class="sxs-lookup"><span data-stu-id="cb188-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="cb188-4561">Rispondere al client con il messaggio CPMCompareBmkOut compilato.</span><span class="sxs-lookup"><span data-stu-id="cb188-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="cb188-4562">3.1.5.2.12 Ricezione di una richiesta CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="cb188-4563">Quando il server riceve la richiesta di messaggio CPMRestartPositionIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4564">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cb188-4565">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4566">Controllare se l'handle di cursore e l'handle del capitolo passati si trova negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="cb188-4567">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4568">Spostare il cursore all'inizio del capitolo, identificato dall'handle del capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="cb188-4569">Si noti che quando l'handle del capitolo è DB \_ NULL HCHAPTER, il capitolo corrispondente \_ è il set di righe principale della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="cb188-4570">Se per qualsiasi motivo questo passaggio non riesce, il server DEVE segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cb188-4571">Rispondere al client con un messaggio CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="cb188-4572">3.1.5.2.13 Ricezione di una richiesta CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="cb188-4573">Quando il server riceve una richiesta di messaggio CPMFreeCursorIn dal client, il server DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4574">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cb188-4575">In caso contrario, il server DEVE segnalare un errore STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cb188-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cb188-4576">Controllare se l'handle di cursore passato è presente nell'elenco degli handle di cursore del client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cb188-4577">In caso contrario, il server DEVE segnalare un errore E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cb188-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cb188-4578">Rilasciare il cursore e le risorse associate (vedere la sezione 3.1.1 per l'elenco completo) per questo handle di cursore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="cb188-4579">Rimuovere il cursore dall'elenco di cursori per il client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="cb188-4580">Rispondere con un messaggio CPMFreeCursorOut, impostando il campo \_ cCursorsRemaining con il numero di cursori rimanenti.</span><span class="sxs-lookup"><span data-stu-id="cb188-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="cb188-4581">nell'elenco di questo client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4581">in this client's list.</span></span>
-   <span data-ttu-id="cb188-4582">Se non sono presenti altri cursori per questo client, il server DEVE rilasciare la query e le risorse associate (vedere la sezione 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="cb188-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="cb188-4583">3.1.5.2.14 Ricezione di una richiesta CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cb188-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="cb188-4584">Quando il server riceve una richiesta di messaggio CPMDisconnect dal client, il server DEVE rimuovere il client dall'elenco dei client connessi e rilasciare tutte le risorse associate al client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="cb188-4585">3.1.6 Eventi timer</span><span class="sxs-lookup"><span data-stu-id="cb188-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="cb188-4586">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="cb188-4587">3.1.7 Altri eventi locali</span><span class="sxs-lookup"><span data-stu-id="cb188-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="cb188-4588">Quando il server viene arrestato, deve prima passare allo stato di arresto.</span><span class="sxs-lookup"><span data-stu-id="cb188-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="cb188-4589">Deve quindi arrestare l'ascolto della pipe, eseguire qualsiasi altra attività di arresto specifica dell'implementazione e quindi passare allo stato "arrestato".</span><span class="sxs-lookup"><span data-stu-id="cb188-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="cb188-4590">3.2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="cb188-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="cb188-4591">3.2.1 Modello di dati astratto</span><span class="sxs-lookup"><span data-stu-id="cb188-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="cb188-4592">La sezione seguente specifica i dati e lo stato gestiti dal client Content Indexing Service Protocol.</span><span class="sxs-lookup"><span data-stu-id="cb188-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="cb188-4593">I dati forniti agevolano la spiegazione del comportamento del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="cb188-4594">Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il comportamento esterno sia coerente con quello descritto in questo documento.</span><span class="sxs-lookup"><span data-stu-id="cb188-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="cb188-4595">Un client ha lo stato astratto seguente:</span><span class="sxs-lookup"><span data-stu-id="cb188-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="cb188-4596">**Ultimo messaggio inviato:** copia dell'ultimo messaggio inviato al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="cb188-4597">**Valore proprietà corrente:** valore parziale di una proprietà "posticipata", che è in corso di recupero.</span><span class="sxs-lookup"><span data-stu-id="cb188-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="cb188-4598">**Byte correnti ricevuti:** numero di byte ricevuti finora per il valore della proprietà corrente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="cb188-4599">**Stato connessione named pipe:** connessione al server</span><span class="sxs-lookup"><span data-stu-id="cb188-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="cb188-4600">3.2.2 Timer</span><span class="sxs-lookup"><span data-stu-id="cb188-4600">3.2.2 Timers</span></span>

<span data-ttu-id="cb188-4601">Non sono necessari timer di protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="cb188-4602">3.2.3 Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="cb188-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="cb188-4603">Non viene eseguita alcuna azione fino a quando non viene ricevuta una richiesta di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="cb188-4604">3.2.4 Higher-Layer eventi attivati</span><span class="sxs-lookup"><span data-stu-id="cb188-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="cb188-4605">Quando una richiesta viene ricevuta da un livello superiore, il client DEVE creare una connessione named pipe al server, usando i dettagli specificati nella sezione 2.1.</span><span class="sxs-lookup"><span data-stu-id="cb188-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="cb188-4606">Se non è possibile eseguire questa operazione, la richiesta di livello superiore DEVE non essere riuscita.</span><span class="sxs-lookup"><span data-stu-id="cb188-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="cb188-4607">Ciò significa che, in caso di errore di connessione, è responsabilità del livello superiore riprovare, se necessario.</span><span class="sxs-lookup"><span data-stu-id="cb188-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="cb188-4608">Un'intestazione DEVE essere precompilata con i campi impostati come specificato nella sezione 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="cb188-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="cb188-4609">Per i messaggi specificati come che richiedono un checksum diverso da zero, il \_ valore ulChecksum DEVE essere calcolato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="cb188-4610">Il contenuto del messaggio dopo il campo ulReserved2 nell'intestazione del messaggio DEVE essere interpretato come una sequenza di interi \_ a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="cb188-4611">Il client DEVE calcolare la somma dei valori numerici specificati da questi numeri interi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="cb188-4612">Calcola l'XOR bit per bit di questo valore con 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="cb188-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="cb188-4613">Sottrae il valore specificato \_ da msg dal valore restituito dall'operatore XOR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="cb188-4614">3.2.4.1 Gestione del catalogo del servizio di indicizzazione remota</span><span class="sxs-lookup"><span data-stu-id="cb188-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="cb188-4615">Ogni messaggio viene attivato da una richiesta dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="cb188-4616">Non esiste alcuna sequenza di messaggi applicata dal client per le richieste di messaggi CISP per la gestione remota dei cataloghi, ma (ad eccezione di un messaggio CPMSetCatStateIn) il server risponderà con esito positivo solo se il client si connetteva in precedenza tramite un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="cb188-4617">3.2.4.1.1 Invio di una richiesta CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="cb188-4618">In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMCiStateInOut quando sono necessarie informazioni sui servizi di indicizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="cb188-4619">Quando viene richiesto di inviare questo messaggio, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4620">Inviare un messaggio CPMCiStateInOut come specificato nella sezione 2.2.3.1 al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="cb188-4621">Attendere di ricevere il messaggio CPMCiStateInOut dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cb188-4622">Segnalare il valore del campo dello stato della risposta e, se l'operazione ha avuto esito positivo, la struttura informativo \_ torna al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="cb188-4623">3.2.4.1.2 Invio di una richiesta CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="cb188-4624">In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMSetCatStateIn quando sono necessarie informazioni su un catalogo o su tutti i cataloghi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="cb188-4625">Per questo messaggio il livello superiore deve fornire al client del protocollo un valore per \_ dwNewState e, se necessario, il nome del catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="cb188-4626">Quando viene richiesto di inviare questo messaggio, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4627">Inviare un messaggio CPMSetCatStateIn come specificato nella versione 2.2.3.2 al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="cb188-4628">Attendere la ricezione di un messaggio CPMSetCatStateOut dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cb188-4629">Segnalare il valore del campo status della risposta e, se ha avuto esito \_ positivo, \_ dwOldState torna al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="cb188-4630">3.2.4.1.3 Invio di una richiesta CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="cb188-4631">Il livello superiore richiede in genere di inviare questo messaggio quando è necessario aggiornare i documenti nel percorso esistente o aggiungere un nuovo percorso di file all'indice.</span><span class="sxs-lookup"><span data-stu-id="cb188-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="cb188-4632">Il livello superiore è quindi quello di fornire il percorso e il tipo di un'analisi, specificata come nella sezione 2.2.3.4 in cui un aggiornamento incrementale o completo è destinato ai percorsi esistenti e la nuova inizializzazione è destinata ai nuovi percorsi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="cb188-4633">Per soddisfare la richiesta di livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4634">Inviare un messaggio CPMUpdateDocumentsIn come specificato nella sezione 2.2.3.4 al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="cb188-4635">Attendere la ricezione del messaggio CPMUpdateDocumentsIn dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cb188-4636">Segnalare il valore del \_ campo di stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="cb188-4637">3.2.4.1.4 Invio di una richiesta CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="cb188-4638">In genere, il livello superiore richiede di inviare questo messaggio quando è necessario migliorare le prestazioni delle query o fa parte della manutenzione pianificata del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="cb188-4639">Per gestire il livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4640">Inviare il messaggio CPMForceMergeIn come specificato dalla sezione 2.2.3.5 al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="cb188-4641">Attendere la ricezione di un messaggio CPMUpdateDocumentsIn dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cb188-4642">Segnalare il valore del \_ campo di stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="cb188-4643">3.2.4.2 Messaggi di query del catalogo del servizio di indicizzazione remota</span><span class="sxs-lookup"><span data-stu-id="cb188-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="cb188-4644">Ad eccezione di CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, esiste una relazione uno-a-uno tra i messaggi CISP e le richieste di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="cb188-4645">Per le due eccezioni indicate in precedenza, possono essere generati più messaggi dal client per soddisfare i requisiti di dimensione o per recuperare una proprietà completa.</span><span class="sxs-lookup"><span data-stu-id="cb188-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="cb188-4646">Il livello superiore tiene in genere traccia di tutte le informazioni specifiche della query (ad esempio gli handle di cursore aperti, i valori validi per gli handle di segnalibro e capitolo, i valori wid per i valori delle proprietà posticipate e così via) e rileva anche se il client si trova in uno stato connesso, ma questo non viene applicato in alcun modo dal client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="cb188-4647">A scopo illustrativo, la parte client del diagramma nella sezione 3 illustra questa sequenza per una semplice query del Servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="cb188-4648">3.2.4.2.1 Invio di una richiesta CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="cb188-4649">Questo messaggio è in genere la prima richiesta dal livello superiore (come se il client non fosse connesso, il server avrà esito negativo per la maggior parte dei messaggi ad eccezione di CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="cb188-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="cb188-4650">Il livello superiore fornisce al client del protocollo le informazioni necessarie per la connessione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="cb188-4651">Per gestire il livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4652">Compilare il messaggio usando le informazioni fornite dal client di livello superiore (vedere la sezione 2.2.3.6) in \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 e aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="cb188-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="cb188-4653">Impostare \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet e cExtPropSet come specificato nella versione 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="cb188-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="cb188-4654">Impostare il checksum nel \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="cb188-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="cb188-4655">Inviare il messaggio CPMConnectIn al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="cb188-4656">Attendere di ricevere un messaggio CPMConnectOut dal server, rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cb188-4657">Segnalare il valore del campo dello stato della risposta e, se l'operazione ha avuto esito \_ positivo, \_ la proprietà serverVersion al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="cb188-4658">Per scopi informativi, è previsto che i livelli superiori eseereranno in genere le azioni seguenti al completamento della connessione, ma queste non vengono applicate dal client CISP:</span><span class="sxs-lookup"><span data-stu-id="cb188-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="cb188-4659">Usare i messaggi di gestione del catalogo del servizio di indicizzazione remota per le attività amministrative</span><span class="sxs-lookup"><span data-stu-id="cb188-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="cb188-4660">Usare una richiesta CPMCreateQueryIn per creare una query di ricerca allo scopo di recuperare i risultati dal catalogo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="cb188-4661">3.2.4.2.2 Invio di una richiesta CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="cb188-4662">Il livello superiore in genere fornirà informazioni per la creazione della query dopo la connessione del client del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="cb188-4663">Il livello superiore fornisce al client un set di restrizioni, un set di colonne, regole di ordinamento e set di categorizzazione (ognuna delle quali può essere omessa), proprietà del set di righe e struttura del mapper di ID proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb188-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="cb188-4664">Quando questa richiesta viene ricevuta da un livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4665">Preparare un oggetto CPMCreateQueryOut come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="cb188-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="cb188-4666">Se è presente un set di colonne, impostare CColumnsSetPreset su 0x01 e compilare il campo ColumnsSet.</span><span class="sxs-lookup"><span data-stu-id="cb188-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="cb188-4667">Se sono presenti restrizioni, impostare CRestrictionPresent su 0x01 e compilare il campo Restrizione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="cb188-4668">Se è presente un set di ordinamento, compilare il campo SortSet.</span><span class="sxs-lookup"><span data-stu-id="cb188-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="cb188-4669">Se è presente un set di categorizzazione, impostare CSortSetPresent su 0x01 e compilare il campo CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="cb188-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="cb188-4670">Impostare il resto dei campi come specificato nella versione 2.2.3.8</span><span class="sxs-lookup"><span data-stu-id="cb188-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="cb188-4671">Calcolare \_ il campo ulCheckSum nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="cb188-4672">Inviare il messaggio CPMCreateQueryIn al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="cb188-4673">Attendere la ricezione del messaggio CPMCreateQueryOut (vedere i dettagli nella sezione 3.2.5.1.1), rimuovendo automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="cb188-4674">Segnalare il valore del campo di stato della risposta e, se ha avuto esito positivo, la matrice di handle di cursore e i valori booleani informativi (come specificato \_ nella 2.2.3.9) di nuovo al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="cb188-4675">3.2.4.2.3 Invio di una richiesta CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="cb188-4676">In genere, il livello superiore imposta le associazioni per ogni colonna da restituire nelle righe quando ha già un handle di cursore valido (dopo aver ricevuto correttamente CPMCreateQueryOut, vedere la sezione 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="cb188-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="cb188-4677">Si prevede che più alto fornirà una matrice di strutture CTableColumn, come specificato nella sezione 2.2.4.31, per il campo aColumns e un handle di cursore valido.</span><span class="sxs-lookup"><span data-stu-id="cb188-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="cb188-4678">Quando questa richiesta viene ricevuta dal livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4679">Calcolare il numero di strutture CTableColumn nella matrice aColumns e impostare il campo cColumns su questo valore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="cb188-4680">Calcolare le dimensioni totali in byte dei campi cColumns e aColumns e impostare il campo \_ cbBindingDesc su questo valore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="cb188-4681">Impostare i campi specificati nel messaggio CPMSetBindingsIn ai valori forniti dal livello superiore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="cb188-4682">Impostare il \_ campo ulChecksum sul valore calcolato come specificato nella Sezione 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="cb188-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="cb188-4683">Inviare il messaggio CPMSetBindignsIn completato al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="cb188-4684">Attendere di ricevere un messaggio CPMSetBindingsIn dal server, rimuovendo gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="cb188-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="cb188-4685">Indicare lo stato \_ dal campo dello stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="cb188-4686">Per scopi informativi, è previsto che i livelli superiori in genere richiedono a un client di inviare un messaggio CPMGetRowsIn, ma questo non viene applicato dal protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="cb188-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="cb188-4687">3.2.4.2.4 Invio di una richiesta CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="cb188-4688">Quando il livello superiore sta per ricevere informazioni sulle righe, fornirà al client del protocollo un handle di cursore e capitolo valido e una descrizione di ricerca appropriata.</span><span class="sxs-lookup"><span data-stu-id="cb188-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="cb188-4689">In genere, è previsto un livello superiore quando ha un cursore valido e/o un handle di capitolo e le associazioni sono state impostate con il messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="cb188-4690">Per accedere al set di righe in un capitolo, il livello superiore è usare l'handle di capitolo ricevuto dal server in un messaggio CPMGetRowsOut precedente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="cb188-4691">Quando questa richiesta viene ricevuta dal livello superiore, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4692">Determinare quale valore intero senza segno specificare per il \_ campo cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="cb188-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="cb188-4693">Per determinare questo valore, il client DEVE prendere il valore massimo dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="cb188-4694">Un migliaio di volte il valore del \_ campo c RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="cb188-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="cb188-4695">Valore di \_ cbRowWidth, arrotondato al multiplo di 512 byte più vicino.</span><span class="sxs-lookup"><span data-stu-id="cb188-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="cb188-4696">Prendere il valore più alto di questi due valori, fino al limite di 16.000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="cb188-4697">Nei casi in cui una singola riga è maggiore di 16.000, il server non può restituire risultati a questa query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="cb188-4698">Specificare una base client per i dati di riga di dimensioni variabili nello spazio indirizzi del client nel \_ campo ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="cb188-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="cb188-4699">*Comportamento di Windows: per un client a 32 bit che parla con un server a 32 bit o un client a 64 bit che parla con un server a 64 bit, questo valore è impostato su un indirizzo di memoria del buffer ricevente nel processo dell'applicazione. Ciò consente ai puntatori ricevuti nel campo Righe di CPMGetRowsOut di essere puntatori di memoria corretti in un processo dell'applicazione client. In caso contrario, è impostato su 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="cb188-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="cb188-4700">Calcolare le dimensioni della descrizione della ricerca e impostarla nel \_ campo cbSeek.</span><span class="sxs-lookup"><span data-stu-id="cb188-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="cb188-4701">Impostare il valore di cbReserved (che fungerebbe da offset per l'inizio delle righe) sul valore \_ cbSeek più 0x14.</span><span class="sxs-lookup"><span data-stu-id="cb188-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="cb188-4702">Inviare un messaggio CPMConnectIn come specificato nella versione 2.2.3.15 al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="cb188-4703">3.2.4.2.5 Invio di una richiesta CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="cb188-4704">Se il client riceve una risposta CPMGetRowsOut dal server con il campo Status della colonna impostato su StatusDeferred (0x01), significa che il valore della proprietà non è stato incluso nel campo Rows del messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="cb188-4705">In questo caso il livello superiore richiede in genere al client del protocollo di recuperare il valore tramite il messaggio CPMFetchValueIn e fornisce il valore PropSpec e wid per una proprietà posticipata, che il client del protocollo DEVE usare nel primo messaggio \_ CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="cb188-4706">Se si tratta del primo messaggio CPMFetchValueIn inviato dal client per richiedere la proprietà specificata, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4707">Impostare tutti i campi in un messaggio come specificato nella sezione 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="cb188-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="cb188-4708">Impostare \_ cbSoFar su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="cb188-4709">Impostare Byte correnti ricevuti su 0.</span><span class="sxs-lookup"><span data-stu-id="cb188-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="cb188-4710">Inviare il messaggio CPMFetchValueIn al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="cb188-4711">3.2.4.2.6 Invio di una richiesta CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="cb188-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="cb188-4712">Quando il livello superiore non usa più la query di ricerca, può rilasciare le risorse nel server richiedendo al client di inviare un messaggio CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="cb188-4713">Quando viene ricevuta questa richiesta, il client DEVE inviare un messaggio CPMFreeCursorIn come specificato in 2.2.3.28 al server, contenente l'handle specificato dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="cb188-4714">3.2.4.2.7 Invio di un messaggio CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cb188-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="cb188-4715">Se il livello superiore non ha più query per il servizio di indicizzazione, per liberare altre risorse del server, l'applicazione potrebbe richiedere che il client invii un messaggio CPMDisconnect al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="cb188-4716">Quando viene ricevuta questa query, il client DEVE semplicemente inviare il messaggio come richiesto.</span><span class="sxs-lookup"><span data-stu-id="cb188-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="cb188-4717">Non è disponibile alcuna risposta a questo messaggio dal server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="cb188-4718">3.2.5 Regole di elaborazione e sequenziazione dei messaggi</span><span class="sxs-lookup"><span data-stu-id="cb188-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="cb188-4719">Quando il client riceve una risposta del messaggio dal server, deve utilizzare l'ultimo messaggio inviato per determinare se il messaggio ricevuto dal server è quello previsto dal client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="cb188-4720">Tutti i messaggi con \_ campo msg diverso da quello in Ultimo messaggio di invio DEVONO essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="cb188-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="cb188-4721">3.2.5.1 Ricezione di una risposta CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="cb188-4722">Quando il client riceve una risposta al messaggio CPMCreateQueryOut dal server, il client deve restituire lo stato e, se lo stato ha esito positivo, i valori di handle del cursore tornano al \_ livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="cb188-4723">Eventuali altre azioni possono essere eseguite fino al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="cb188-4724">Poiché il livello superiore è a conoscenza della struttura della query, nel messaggio CPMCreateOueryOut verrà sempre restituito il numero corretto di handle di cursore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="cb188-4725">Gli handle di cursore vengono restituiti nell'ordine seguente: il primo handle è per il set di righe non scambiato, il secondo per il primo set di righe con capitolo (ovvero il raggruppamento dei risultati in base alla prima categoria specificata nel campo CategorizationSet del messaggio CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="cb188-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="cb188-4726">Per scopi informativi, è previsto che i livelli superiori possano eseguire le azioni seguenti, ma queste non vengono applicate dal client CISP:</span><span class="sxs-lookup"><span data-stu-id="cb188-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="cb188-4727">Usare CPMSetBindingsIn per impostare associazioni per singole colonne ed eseguire eventuali azioni successive sul percorso della query</span><span class="sxs-lookup"><span data-stu-id="cb188-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="cb188-4728">Usare CPMGetQueryStatusIn per controllare lo stato di esecuzione di una query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="cb188-4729">Usare CPMRatioFinishedIn per richiedere la percentuale di completamento della query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="cb188-4730">3.2.5.2 Ricezione di una risposta CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="cb188-4731">Quando il client riceve una risposta di messaggio CPMGetRowsOut dal server, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4732">Controllare se il \_ campo dello stato nell'intestazione indica esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="cb188-4733">Se il \_ valore di stato è STATUS BUFFER TOO SMALL \_ (0xC0000023), il client DEVE controllare lo stato Ultimo messaggio \_ \_ inviato.</span><span class="sxs-lookup"><span data-stu-id="cb188-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="cb188-4734">Se non contiene un messaggio CPMGetRowsIn, il messaggio ricevuto DEVE essere ignorato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="cb188-4735">In caso contrario, il client DEVE inviare al server un nuovo messaggio CPMGetRowsIn con tutti i campi identici a quello archiviato, ad eccezione del fatto che cbReadBuffer DEVE essere aumentato di 512 (ma non maggiore di \_ 0x4000).</span><span class="sxs-lookup"><span data-stu-id="cb188-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="cb188-4736">Se lo stato è STATUS BUFFER TOO SMALL (0xC0000023) e Last Message Sent ha già \_ \_ \_ \_ \_ cbReadBuffer uguale 0x4000 client DEVE segnalare l'errore fino al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="cb188-4737">Se il \_ valore di stato è qualsiasi altro valore di errore, il client DEVE indicare l'errore fino al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="cb188-4738">Se il valore di stato indica l'esito positivo, i risultati DEVONO essere indicati fino al livello superiore che richiede le informazioni e altre azioni sono fino \_ al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="cb188-4739">Per scopi informativi, è previsto che i livelli superiori eseecutori esecutori in genere esecutori delle azioni seguenti, ma non vengono applicati dal client content indexing service protocol:</span><span class="sxs-lookup"><span data-stu-id="cb188-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="cb188-4740">Se i valori nelle righe rappresentano gli ID documento, gli handle di capitolo o segnalibro del livello superiore vengono in genere archiviati per l'uso nelle operazioni successive che coinvolgono ID documento validi, handle di capitolo o segnalibro.</span><span class="sxs-lookup"><span data-stu-id="cb188-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="cb188-4741">Il livello superiore in genere archivia o visualizza o usa in altro modo i dati dei valori di riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="cb188-4742">Per i valori contrassegnati come livello superiore posticipato, il valore verrà recuperato usando i messaggi CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="cb188-4743">La descrizione della ricerca viene restituita anche al livello superiore e può essere riutilizzata o esaminata dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="cb188-4744">A scopo informativo, se il livello superiore ha richiesto handle per i capitoli e i segnalibri ricevuti nelle righe, è possibile eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="cb188-4745">Usare CPMGetQueryStatusExIn per controllare lo stato di esecuzione di una query, nonché informazioni aggiuntive sullo stato, ad esempio il numero di documenti filtrati, i documenti rimanenti da filtrare, il rapporto tra i documenti elaborati dalla query, il numero totale di righe nella query e la posizione del segnalibro nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="cb188-4746">Usare CPMGetNotify per richiedere che il server invii una notifica al client delle modifiche al set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="cb188-4747">Usare CPMGetApproximatePositionIn per richiedere la posizione approssimativa di un segnalibro in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="cb188-4748">Usare CPMCompareBmkIn per richiedere un confronto tra due segnalibri in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="cb188-4749">Usare CPMRestartPositionIn per il server per modificare la posizione del cursore all'inizio del set di righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="cb188-4750">3.2.5.3 Ricezione di una risposta CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="cb188-4751">Quando il client riceve una risposta di messaggio CPMGetRowsOut dal server, il client DEVE eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="cb188-4752">Controllare se il \_ campo dello stato nell'intestazione indica esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="cb188-4753">In caso di errore, inviare una notifica al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="cb188-4754">In caso contrario, continuare di seguito.</span><span class="sxs-lookup"><span data-stu-id="cb188-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="cb188-4755">Controllare fValueExist e se impostato su 0x00000000 notificare al livello \_ superiore che il valore non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="cb188-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="cb188-4756">In caso contrario, \_ aggiungere i byte cbValue da vValue al valore della proprietà corrente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="cb188-4757">Se fMoreExists è impostato su 0x00000001 incrementare i byte correnti ricevuti da cbValue e inviare un \_ \_ \_ \_ messaggio CPMFetchValueIn al server, impostando cbSoFar sul valore di Byte correnti \_ ricevuti, cbPropSpec su zero e \_ \_ cbChunk sulla dimensione del buffer desiderata dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="cb188-4758">Se fMoreExists è impostato su 0x00000000 quindi indicare il valore della proprietà da Valore proprietà \_ corrente al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="cb188-4759">3.2.5.4 Ricezione di una risposta CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="cb188-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="cb188-4760">Quando il client riceve una risposta di messaggio CPMFreeCursorOut dal server, il client DEVE restituire il valore \_ cCursorsRemaining al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="cb188-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="cb188-4761">Le informazioni seguenti vengono fornite solo a scopo informativo e non vengono applicate dal client CISP.</span><span class="sxs-lookup"><span data-stu-id="cb188-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="cb188-4762">È previsto che il livello superiore tenga traccia degli handle del cursore e non usi quelli già liberati.</span><span class="sxs-lookup"><span data-stu-id="cb188-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="cb188-4763">Quando il numero di cCursorsRemaining è uguale a 0x00000000, il livello superiore può usare la connessione per specificare un'altra query (usando un \_ messaggio CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="cb188-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="cb188-4764">3.2.6 Eventi timer</span><span class="sxs-lookup"><span data-stu-id="cb188-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="cb188-4765">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="cb188-4766">3.2.7 Altri eventi locali</span><span class="sxs-lookup"><span data-stu-id="cb188-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="cb188-4767">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="cb188-4768">4 Esempi di protocollo</span><span class="sxs-lookup"><span data-stu-id="cb188-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="cb188-4769">4.1 Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb188-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="cb188-4770">4.2 Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cb188-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="cb188-4771">4.1 Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb188-4771">4.1 Example 1</span></span>

<span data-ttu-id="cb188-4772">Nell'esempio seguente si considera uno scenario in cui l'utente JOHN nel computer A vuole ottenere le dimensioni dei file che contengono la parola "Microsoft" dal set di documenti archiviati nel server X nel catalogo SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="cb188-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="cb188-4773">Si supponga che il computer A eserciti un sistema operativo Windows XP a 32 bit e che il computer X eserciti un sistema operativo Windows Server 2003 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="cb188-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="cb188-4774">L'utente avvia un'applicazione di ricerca e immette la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cb188-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="cb188-4775">L'applicazione passa a sua volta la query di ricerca al client del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb188-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="cb188-4776">Il client del protocollo stabilisce una connessione con il server di indicizzazione X. Il client del protocollo usa named pipe \\ \\ pipe CI \_ SKADS per connettersi al server X tramite SMB.</span><span class="sxs-lookup"><span data-stu-id="cb188-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="cb188-4777">Il client del protocollo prepara quindi un messaggio CPMConnectIn con i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="cb188-4778">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4779">**\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="cb188-4780">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cb188-4781">**\_ ulChecksum** contiene il checksum, calcolato come specificato nella Sezione 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="cb188-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="cb188-4782">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cb188-4783">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4784">**\_ iClientVersion è** impostato su 0x00000008, che indica che il server deve convalidare il campo checksum.</span><span class="sxs-lookup"><span data-stu-id="cb188-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="cb188-4785">**\_ fClientIsRemote** è impostato su 0x00000001, che indica che il server è un server remoto.</span><span class="sxs-lookup"><span data-stu-id="cb188-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="cb188-4786">**\_ cbBlob1** è impostato sulla dimensione, in byte, dei campi cPropSet, PropertySet1 e PropertySet2 combinati.</span><span class="sxs-lookup"><span data-stu-id="cb188-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="cb188-4787">**\_ cbBlob2 è** impostato su 0x00000004 (ovvero nessun set di proprietà aggiuntivo).</span><span class="sxs-lookup"><span data-stu-id="cb188-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="cb188-4788">**MachineName** è impostato su A.</span><span class="sxs-lookup"><span data-stu-id="cb188-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="cb188-4789">**UserName** è impostato su JOHN.</span><span class="sxs-lookup"><span data-stu-id="cb188-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="cb188-4790">**cPropSets** è impostato su 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="cb188-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="cb188-4791">**Il campo PropertySet1** è di tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="cb188-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="cb188-4792">La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="cb188-4793">Il campo **GuidPropSet** è impostato su A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="cb188-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="cb188-4794">**Il campo cProperties** è impostato su 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="cb188-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="cb188-4795">**Un campo aProps** è una matrice di strutture CDbProp.</span><span class="sxs-lookup"><span data-stu-id="cb188-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="cb188-4796">Per **l'elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="cb188-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="cb188-4797">**PropId** è impostato su 0x00000002 (DBPROP \_ CI \_ CATALOG \_ NAME).</span><span class="sxs-lookup"><span data-stu-id="cb188-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="cb188-4798">**DBPROPOPTIONS è** impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cb188-4799">**DBPROPSTATUS è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-4800">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cb188-4801">**eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID)</span><span class="sxs-lookup"><span data-stu-id="cb188-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="cb188-4802">**IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cb188-4803">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-4804">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cb188-4805">**vType** è impostato su 0x001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="cb188-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="cb188-4806">**vValue** è impostato su "SYSTEM", il nome del catalogo desiderato.</span><span class="sxs-lookup"><span data-stu-id="cb188-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="cb188-4807">Per **l'elemento aProps \[ 1: \]**</span><span class="sxs-lookup"><span data-stu-id="cb188-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="cb188-4808">**PropId** è impostato su 0x00000007 (DBPROP \_ CI \_ QUERY \_ TYPE)</span><span class="sxs-lookup"><span data-stu-id="cb188-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="cb188-4809">**DBPROPOPTIONS è** impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cb188-4810">**DBPROPSTATUS è** impostato su0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="cb188-4811">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cb188-4812">**eKind** è impostato su 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="cb188-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cb188-4813">**GUID** è Null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cb188-4814">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-4815">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cb188-4816">**vType** è impostato su 0x0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="cb188-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="cb188-4817">**vValue** è impostato su 0x00000000 (CiNormal), ovvero si tratta di una query normale.</span><span class="sxs-lookup"><span data-stu-id="cb188-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="cb188-4818">Per **l'elemento aProps \[ 2: \]**</span><span class="sxs-lookup"><span data-stu-id="cb188-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="cb188-4819">**PropId** è impostato su 0x00000004 (DBPROP \_ CI \_ SCOPE \_ FLAGS).</span><span class="sxs-lookup"><span data-stu-id="cb188-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="cb188-4820">**DBPROPOPTIONS è** impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cb188-4821">**DBPROPSTATUS è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-4822">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cb188-4823">**eKind** è impostato su 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="cb188-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cb188-4824">**GUID** è Null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cb188-4825">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-4826">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cb188-4827">**vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="cb188-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="cb188-4828">**vValue:** 0x00000001/0x00000001 (un elemento con valore 1), ovvero le sottocartelle di ricerca</span><span class="sxs-lookup"><span data-stu-id="cb188-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="cb188-4829">Per **l'elemento aProps \[ 3: \]**</span><span class="sxs-lookup"><span data-stu-id="cb188-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="cb188-4830">**PropId:** 0x00000003 (DBPROP \_ CI \_ INCLUDE \_ SCOPES)</span><span class="sxs-lookup"><span data-stu-id="cb188-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="cb188-4831">**DBPROPOPTIONS**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="cb188-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="cb188-4832">**DBPROPSTATUS:** 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="cb188-4833">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cb188-4834">**eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID).</span><span class="sxs-lookup"><span data-stu-id="cb188-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cb188-4835">**IL GUID** è Null (tutti zeri), vale a dire che il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cb188-4836">**ulID** è impostato su 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="cb188-4837">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cb188-4838">**vType** è impostato su 0x101F (VT \_ VECTOR \| VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="cb188-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="cb188-4839">**vValue** è impostato su 0x00000001/0x00000002 / " " (un elemento con una stringa con terminazione \\ Null a 2 caratteri), ovvero l'ambito radice.</span><span class="sxs-lookup"><span data-stu-id="cb188-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="cb188-4840">Il **campo PropertySet2** è di tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="cb188-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="cb188-4841">La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="cb188-4842">**GuidPropSet** è impostato su AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="cb188-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="cb188-4843">**Il campo cProperties** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="cb188-4844">Il **campo aProps** è una matrice di strutture CDbProp.</span><span class="sxs-lookup"><span data-stu-id="cb188-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="cb188-4845">Per **l'elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="cb188-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="cb188-4846">**PropId** è impostato su 0x00000002 (DBPROP \_ MACHINE).</span><span class="sxs-lookup"><span data-stu-id="cb188-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="cb188-4847">**DBPROPOPTIONS è** impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cb188-4848">**DBPROPSTATUS è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-4849">Per **l'elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cb188-4850">**eKind** è impostato su 0x00000001 \_ \_ (DBKIND GUID PROPID),</span><span class="sxs-lookup"><span data-stu-id="cb188-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="cb188-4851">**GUID** è Null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cb188-4852">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-4853">Per **l'elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cb188-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="cb188-4854">**vType:** 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="cb188-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="cb188-4855">**vValue:** 0x04/"X" (4 byte/stringa Unicode con terminazione Null), ovvero "X" -name di un server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="cb188-4856">**Il campo cExtPropSet** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cb188-4857">**Matrice aPropertySets** inesistente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="cb188-4858">I vari campi di riempimento vengono compilati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="cb188-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="cb188-4859">Il messaggio viene inviato al server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="cb188-4860">Il server verifica che **\_ ulChecksum** sia corretto, verifica che l'utente sia autorizzato a effettuare questa richiesta e risponde con un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="cb188-4861">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4862">**\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="cb188-4863">**\_ status** è impostato su 0x0000000 che indica SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cb188-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="cb188-4864">**\_ ulChecksum** è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="cb188-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="cb188-4865">**\_ ulReserved2 è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cb188-4866">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4867">**\_ il campo serverVersion** è impostato su 0x00000007 (Windows XP a 32 bit o Windows Server 2003 a 32 bit).</span><span class="sxs-lookup"><span data-stu-id="cb188-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="cb188-4868">**\_ I** campi riservati vengono compilati con dati arbitrari.</span><span class="sxs-lookup"><span data-stu-id="cb188-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="cb188-4869">Il client prepara un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="cb188-4870">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4871">**\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="cb188-4872">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cb188-4873">**\_ ulChecksum** contiene il checksum, calcolato in base alla versione 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="cb188-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="cb188-4874">**\_ ulReserved2 è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cb188-4875">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4876">**Il** campo Dimensioni è impostato sulla dimensione del resto del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="cb188-4877">**Il campo CColumnSetPresent** è impostato su 0x01.</span><span class="sxs-lookup"><span data-stu-id="cb188-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="cb188-4878">**Il campo ColumnSet** è di tipo CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="cb188-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="cb188-4879">La struttura CColumnSet che comprende questo campo viene impostata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="cb188-4880">**\_ Il** campo count è impostato su 0x00000001 che indica che viene restituita una colonna.</span><span class="sxs-lookup"><span data-stu-id="cb188-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="cb188-4881">**La matrice indexes** 0x00000000 che indica la prima voce in \_ un oggettoPropSpec.</span><span class="sxs-lookup"><span data-stu-id="cb188-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="cb188-4882">**Il campo CRestrictionPresent** è impostato su 0x01 che indica che il **campo Restriction** è presente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="cb188-4883">**Il** campo Restriction è di tipo CRestriction ed è impostato su:</span><span class="sxs-lookup"><span data-stu-id="cb188-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="cb188-4884">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="cb188-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="cb188-4885">**\_ weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cb188-4886">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="cb188-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="cb188-4887">**\_ La** proprietà è impostata su GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC PROPID) /0x13 che rappresenta il corpo \_ del documento.</span><span class="sxs-lookup"><span data-stu-id="cb188-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="cb188-4888">**\_ Cc** è impostato su 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="cb188-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="cb188-4889">**\_ pwcsphrase** è impostato sulla stringa "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="cb188-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="cb188-4890">**\_ lcid è** impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="cb188-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="cb188-4891">**\_ ulGenerateMethod è** impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="cb188-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="cb188-4892">**CSortPresent è** impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="cb188-4893">**CCategorizationSetPresent** è impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="cb188-4894">**RowSetProperties viene** impostato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="cb188-4895">**\_ uBooleanOptions** è impostato su 0x00000001 (sequenziale).</span><span class="sxs-lookup"><span data-stu-id="cb188-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="cb188-4896">**\_ ulMaxOpenRows** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cb188-4897">**\_ ulMemoryUsage** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cb188-4898">\_**cMaxResults** è impostato su 0x00000100 (restituisce al massimo 256 righe).</span><span class="sxs-lookup"><span data-stu-id="cb188-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="cb188-4899">**\_ cCmdTimeOut** è impostato su 0x00000000 (mai timeout).</span><span class="sxs-lookup"><span data-stu-id="cb188-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="cb188-4900">**PidMapper** è impostato su:</span><span class="sxs-lookup"><span data-stu-id="cb188-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="cb188-4901">**\_ count** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="cb188-4902">**\_ aPropSpec** è impostato su GUID B725F130-47EF-101A-A5-F1-02608C9EEEBAC/0x00000001 (per PRSPEC PROPID) /0x0000000c che rappresenta la proprietà delle dimensioni \_ del file di Windows.</span><span class="sxs-lookup"><span data-stu-id="cb188-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="cb188-4903">Il server lo elabora e risponde con un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="cb188-4904">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4905">**\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="cb188-4906">**\_ status** è impostato su SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cb188-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cb188-4907">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cb188-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cb188-4908">**\_ ulReserved2 è** impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cb188-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="cb188-4909">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4910">**\_ fTrueSeqeuntial** è impostato su 0x00000000, a indicare che la query può usare un indice.</span><span class="sxs-lookup"><span data-stu-id="cb188-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="cb188-4911">**\_ fWorkIdUnique** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cb188-4912">La **matrice aCursors** contiene un solo elemento, che rappresenta un handle di cursore per questa query.</span><span class="sxs-lookup"><span data-stu-id="cb188-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="cb188-4913">Il valore dipende dallo stato del server.</span><span class="sxs-lookup"><span data-stu-id="cb188-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="cb188-4914">Si supponga che il valore restituito sia 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="cb188-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="cb188-4915">Il client esegui un messaggio di richiesta CPMSetBindingsIn per definire il formato di una riga.</span><span class="sxs-lookup"><span data-stu-id="cb188-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="cb188-4916">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4917">**\_ msg** è impostato su 0x000000D0, a indicare che si tratta di un messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="cb188-4918">**\_ status** è impostato su SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cb188-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cb188-4919">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cb188-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cb188-4920">**\_ ulReserved2 è** impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cb188-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="cb188-4921">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4922">**\_ hCursor** è impostato su 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="cb188-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="cb188-4923">**\_ cbRow è** impostato su 0x10 (sufficientemente grande da adattarsi alle colonne).</span><span class="sxs-lookup"><span data-stu-id="cb188-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="cb188-4924">**\_ cbBindingDesc** è impostato sulla dimensione dei campi **\_ cColumns** **\_ e aColumns** combinati.</span><span class="sxs-lookup"><span data-stu-id="cb188-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="cb188-4925">**\_ cColumns** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cb188-4926">**\_ La matrice aColumns** è impostata in modo da contenere una struttura CTableColumn contenente:</span><span class="sxs-lookup"><span data-stu-id="cb188-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="cb188-4927">**\_ PropSpec** è impostato su GUID b725f130-47ef-101a-a5-f1-02608c9eeebac/0x00000001 (per PRSPEC PROPID) /0x0000000c che rappresenta la proprietà delle dimensioni \_ del file di Windows.</span><span class="sxs-lookup"><span data-stu-id="cb188-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="cb188-4928">**\_ vType** è impostato su 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="cb188-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="cb188-4929">**\_ ValueUsed** è impostato su 0x01 (colonna trasferita nella riga).</span><span class="sxs-lookup"><span data-stu-id="cb188-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="cb188-4930">**\_ ValueOffset** è impostato su 0x0002 (all'inizio della riga).</span><span class="sxs-lookup"><span data-stu-id="cb188-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="cb188-4931">**\_ ValueSize è** impostato su 0x08 (dimensioni di un'interfaccia utente VT8). \_</span><span class="sxs-lookup"><span data-stu-id="cb188-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="cb188-4932">**\_ StatusUsed** è impostato su 0x01.</span><span class="sxs-lookup"><span data-stu-id="cb188-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="cb188-4933">**\_ StatusOffset** è impostato su 0x0A.</span><span class="sxs-lookup"><span data-stu-id="cb188-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="cb188-4934">**\_ LengthUsed** è impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="cb188-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="cb188-4935">Il server lo elabora e risponde con un messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="cb188-4936">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4937">**\_ msg** è impostato su 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="cb188-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="cb188-4938">**\_ status** è impostato su SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cb188-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cb188-4939">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cb188-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cb188-4940">**\_ ulReserved2** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cb188-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="cb188-4941">Il client genera un messaggio di richiesta CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="cb188-4942">Si supponga che il client sia pronto ad accettare 100 righe a questo punto e le voglia in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="cb188-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="cb188-4943">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4944">**\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cb188-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="cb188-4945">**\_ status** è impostato su 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb188-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="cb188-4946">**\_ ulChecksum** contiene il checksum, calcolato in base alla sezione 0.</span><span class="sxs-lookup"><span data-stu-id="cb188-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="cb188-4947">**\_ ulReserved2 è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cb188-4948">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4949">**\_ hCursor** è impostato su 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="cb188-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="cb188-4950">**\_ cRowsToTransfer** è impostato su 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="cb188-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="cb188-4951">**\_ cRowWidth** è impostato su 0x00000010 (da associazioni).</span><span class="sxs-lookup"><span data-stu-id="cb188-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="cb188-4952">**\_ cbSeek** è impostato su 0x14 che è la dimensione dei campi eType, chapt e \_ CRowSeekNext combinati.</span><span class="sxs-lookup"><span data-stu-id="cb188-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="cb188-4953">**\_ cbReserved è** impostato su 0x18 (0x14 \_ più cbSeek).</span><span class="sxs-lookup"><span data-stu-id="cb188-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="cb188-4954">**\_ cbReadBuffer** è impostato su 0x800 (0x64 0x10 arrotondato al multiplo \* successivo di 0x200).</span><span class="sxs-lookup"><span data-stu-id="cb188-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="cb188-4955">**\_ ulClientBase è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cb188-4956">**\_ fBwdfetch** è impostato su 0x00000000 che indica che le righe devono essere recuperate in avanti.</span><span class="sxs-lookup"><span data-stu-id="cb188-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="cb188-4957">**eType** è impostato su 0x0000001 che indica che il client desidera righe successive.</span><span class="sxs-lookup"><span data-stu-id="cb188-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="cb188-4958">**\_ chapt** è impostato su 0 (non su un risultato in capitolo).</span><span class="sxs-lookup"><span data-stu-id="cb188-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="cb188-4959">**SeekDescription** è impostato su CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="cb188-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="cb188-4960">La struttura CRowSeekNext contiene i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb188-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="cb188-4961">**CiTblChapt è** impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cb188-4962">**\_ hRegion** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cb188-4963">**\_ cSkip** è impostato su 0, a indicare che il client non vuole ignorare le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="cb188-4964">Il server lo elabora e risponde con un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="cb188-4965">Si supponga che il server ha trovato 100 documenti contenenti la parola "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="cb188-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="cb188-4966">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4967">**\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cb188-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="cb188-4968">**\_ status** è impostato su SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cb188-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cb188-4969">**\_ ulChecksum** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cb188-4970">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cb188-4971">Il corpo del messaggio viene popolato come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4972">**\_ CRowsReturned** è impostato su 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="cb188-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="cb188-4973">**eType** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cb188-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cb188-4974">**\_ chapt** è impostato su 0x00000000 (non su un risultato in capitolo).</span><span class="sxs-lookup"><span data-stu-id="cb188-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="cb188-4975">**SeekDescription** contiene una struttura CRowSeekNext, popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="cb188-4976">**CiTblChapt** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cb188-4977">**\_ hRegion** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cb188-4978">**\_ cSkip** è impostato su 0, a indicare che il client non vuole ignorare le righe.</span><span class="sxs-lookup"><span data-stu-id="cb188-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="cb188-4979">**Le** righe contengono le dimensioni dei 100 documenti che contengono la parola "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="cb188-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="cb188-4980">Poiché si tratta di dati di dimensioni fisse, è semplicemente strutturato come elenco di interi senza segno a 100 byte a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="cb188-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="cb188-4981">Il client invia un messaggio CPMDisconnect per terminare la connessione.</span><span class="sxs-lookup"><span data-stu-id="cb188-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="cb188-4982">L'intestazione del messaggio viene popolata come segue:</span><span class="sxs-lookup"><span data-stu-id="cb188-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cb188-4983">**\_ msg** è impostato su 0x000000C9, a indicare che si tratta di un messaggio CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="cb188-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="cb188-4984">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cb188-4985">**\_ ulChecksum** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="cb188-4986">Il server elabora il messaggio e rimuove tutti gli stati client.</span><span class="sxs-lookup"><span data-stu-id="cb188-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="cb188-4987">4.2 Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cb188-4987">4.2 Example 2</span></span>

<span data-ttu-id="cb188-4988">Nell'esempio precedente la query era piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="cb188-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="cb188-4989">Si consideri ora una query leggermente più complessa.</span><span class="sxs-lookup"><span data-stu-id="cb188-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="cb188-4990">Si supponga che l'utente voglia recuperare le dimensioni dei documenti che contengono entrambe le parole seguenti: "Microsoft" e "Office".</span><span class="sxs-lookup"><span data-stu-id="cb188-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="cb188-4991">Questo valore viene specificato modificando il campo Restriction contenuto nel messaggio CPMCreateQueryIn inviato nel passaggio 5 come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="cb188-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="cb188-4992">Il **campo Restriction** è di tipo CRestriction ed è impostato su:</span><span class="sxs-lookup"><span data-stu-id="cb188-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="cb188-4993">**\_ ulType** è impostato su 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="cb188-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="cb188-4994">**\_ weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="cb188-4995">Il resto del campo contiene una struttura CNodeRestriction:</span><span class="sxs-lookup"><span data-stu-id="cb188-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="cb188-4996">**\_ cNode** è impostato su 0x00000002, a indicare che sono presenti due nodi nella matrice paNode.</span><span class="sxs-lookup"><span data-stu-id="cb188-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="cb188-4997">Il **\_ campo paNode** è una matrice di due strutture CRestriction.</span><span class="sxs-lookup"><span data-stu-id="cb188-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="cb188-4998">**\_ paNode \[ \] 0** contiene:</span><span class="sxs-lookup"><span data-stu-id="cb188-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="cb188-4999">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="cb188-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="cb188-5000">**\_ weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-5001">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="cb188-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="cb188-5002">**\_ La** proprietà è impostata su GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (per \_ PRSPEC PROPID) / 0x13.</span><span class="sxs-lookup"><span data-stu-id="cb188-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="cb188-5003">**\_ Cc** è impostato su 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="cb188-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="cb188-5004">**\_ pwcsphrase** è impostato sulla stringa "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="cb188-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="cb188-5005">**\_ lcid** è impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="cb188-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="cb188-5006">**\_ ulGenerateMethod è** impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="cb188-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="cb188-5007">**\_ paNode \[ \] 1** contiene:</span><span class="sxs-lookup"><span data-stu-id="cb188-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="cb188-5008">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="cb188-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="cb188-5009">**\_ weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cb188-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cb188-5010">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="cb188-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="cb188-5011">**\_ La** proprietà è impostata su GUID b725f130-47ef-101a-a5f1-02608c9eeebac/0x00000001 (per PRSPEC \_ PROPID) /0x13.</span><span class="sxs-lookup"><span data-stu-id="cb188-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="cb188-5012">**\_ Cc** è impostato su 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="cb188-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="cb188-5013">**\_ pwcsphrase** è impostato sulla stringa "Office".</span><span class="sxs-lookup"><span data-stu-id="cb188-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="cb188-5014">**\_ lcid è** impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="cb188-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="cb188-5015">**\_ ulGenerateMethod è** impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="cb188-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="cb188-5016">5 Sicurezza</span><span class="sxs-lookup"><span data-stu-id="cb188-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="cb188-5017">5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione</span><span class="sxs-lookup"><span data-stu-id="cb188-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="cb188-5018">Implementazioni di indicizzazione che indicizzano il contenuto protetto devono considerare l'uso del contesto utente fornito da SMB MS-SMB per tagliare i risultati della ricerca e restituire solo quelli accessibili \[ \] al chiamante.</span><span class="sxs-lookup"><span data-stu-id="cb188-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="cb188-5019">5.2 Indice dei parametri di sicurezza</span><span class="sxs-lookup"><span data-stu-id="cb188-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="cb188-5020">Parametro di sicurezza</span><span class="sxs-lookup"><span data-stu-id="cb188-5020">Security Parameter</span></span>  | <span data-ttu-id="cb188-5021">Sezione</span><span class="sxs-lookup"><span data-stu-id="cb188-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="cb188-5022">Livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="cb188-5022">Impersonation level</span></span> | <span data-ttu-id="cb188-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="cb188-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="cb188-5024">6 Indice del comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="cb188-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="cb188-5025">Comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="cb188-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="cb188-5026">Sezione</span><span class="sxs-lookup"><span data-stu-id="cb188-5026">Section</span></span>   | <span data-ttu-id="cb188-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cb188-5027">Windows 2000</span></span> | <span data-ttu-id="cb188-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb188-5028">Windows XP</span></span> | <span data-ttu-id="cb188-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb188-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="cb188-5030">Questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb188-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="cb188-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="cb188-5031">1.3.2</span></span>     | <span data-ttu-id="cb188-5032">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5032">X</span></span>            | <span data-ttu-id="cb188-5033">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5033">X</span></span>          | <span data-ttu-id="cb188-5034">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5034">X</span></span>                   |
| <span data-ttu-id="cb188-5035">Le applicazioni interagiscono in genere con un wrapper OLE DB interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="cb188-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="cb188-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="cb188-5036">1.4</span></span>       | <span data-ttu-id="cb188-5037">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5037">X</span></span>            | <span data-ttu-id="cb188-5038">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5038">X</span></span>          | <span data-ttu-id="cb188-5039">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5039">X</span></span>                   |
| <span data-ttu-id="cb188-5040">Valori NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="cb188-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="cb188-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="cb188-5041">1.8</span></span>       | <span data-ttu-id="cb188-5042">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5042">X</span></span>            | <span data-ttu-id="cb188-5043">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5043">X</span></span>          | <span data-ttu-id="cb188-5044">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5044">X</span></span>                   |
| <span data-ttu-id="cb188-5045">Il client imposta il \_ campo dello stato in ogni intestazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cb188-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="cb188-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="cb188-5046">2.2.2</span></span>     | <span data-ttu-id="cb188-5047">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5047">X</span></span>            | <span data-ttu-id="cb188-5048">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5048">X</span></span>          | <span data-ttu-id="cb188-5049">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5049">X</span></span>                   |
| <span data-ttu-id="cb188-5050">Il valore di cPendingScans è in genere zero</span><span class="sxs-lookup"><span data-stu-id="cb188-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="cb188-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="cb188-5051">2.2.3.1</span></span>   | <span data-ttu-id="cb188-5052">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5052">X</span></span>            | <span data-ttu-id="cb188-5053">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5053">X</span></span>          | <span data-ttu-id="cb188-5054">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5054">X</span></span>                   |
| <span data-ttu-id="cb188-5055">Valore iClientVersion</span><span class="sxs-lookup"><span data-stu-id="cb188-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="cb188-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="cb188-5056">2.2.3.6</span></span>   | <span data-ttu-id="cb188-5057">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5057">X</span></span>            | <span data-ttu-id="cb188-5058">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5058">X</span></span>          | <span data-ttu-id="cb188-5059">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5059">X</span></span>                   |
| <span data-ttu-id="cb188-5060">\_Valore cbChunk</span><span class="sxs-lookup"><span data-stu-id="cb188-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="cb188-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="cb188-5061">2.2.3.19</span></span>  | <span data-ttu-id="cb188-5062">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5062">X</span></span>            | <span data-ttu-id="cb188-5063">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5063">X</span></span>          | <span data-ttu-id="cb188-5064">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5064">X</span></span>                   |
| <span data-ttu-id="cb188-5065">Indirizzi di memoria a 32 bit e a 64 bit</span><span class="sxs-lookup"><span data-stu-id="cb188-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="cb188-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="cb188-5066">3.2.4.2.4</span></span> | <span data-ttu-id="cb188-5067">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5067">X</span></span>            | <span data-ttu-id="cb188-5068">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5068">X</span></span>          | <span data-ttu-id="cb188-5069">X</span><span class="sxs-lookup"><span data-stu-id="cb188-5069">X</span></span>                   |



 

 

 





