---
title: Protocollo di servizi di indicizzazione del contenuto
description: Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c22bbda912333368e50d3e4a8ace2cd98856ea
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724226"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="8992a-103">Protocollo di servizi di indicizzazione del contenuto</span><span class="sxs-lookup"><span data-stu-id="8992a-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="8992a-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8992a-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8992a-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="8992a-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="8992a-106">Specifica del protocollo, versione 0,12</span><span class="sxs-lookup"><span data-stu-id="8992a-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="8992a-107">1 Introduzione</span><span class="sxs-lookup"><span data-stu-id="8992a-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="8992a-108">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="8992a-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="8992a-109">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="8992a-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="8992a-110">Panoramica sul protocollo 1,3 (sinossia)</span><span class="sxs-lookup"><span data-stu-id="8992a-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="8992a-111">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="8992a-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="8992a-112">1,5 prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="8992a-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="8992a-113">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="8992a-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="8992a-114">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="8992a-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="8992a-115">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="8992a-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="8992a-116">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="8992a-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="8992a-117">2 Messaggi</span><span class="sxs-lookup"><span data-stu-id="8992a-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="8992a-118">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="8992a-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="8992a-119">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="8992a-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="8992a-120">3 Dettagli del protocollo</span><span class="sxs-lookup"><span data-stu-id="8992a-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="8992a-121">3,1 Dettagli server</span><span class="sxs-lookup"><span data-stu-id="8992a-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="8992a-122">3,2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="8992a-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="8992a-123">4 Esempi di protocollo</span><span class="sxs-lookup"><span data-stu-id="8992a-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="8992a-124">4,1 esempio 1</span><span class="sxs-lookup"><span data-stu-id="8992a-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="8992a-125">4,2 esempio 2</span><span class="sxs-lookup"><span data-stu-id="8992a-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="8992a-126">5 Sicurezza</span><span class="sxs-lookup"><span data-stu-id="8992a-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="8992a-127">5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione</span><span class="sxs-lookup"><span data-stu-id="8992a-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="8992a-128">5.2 Indice dei parametri di sicurezza</span><span class="sxs-lookup"><span data-stu-id="8992a-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="8992a-129">6 Indice del comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="8992a-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="8992a-130">Questo documento è una specifica del protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="8992a-131">La documentazione di WSPP (Workgroup Server Protocol Program) è destinata all'utilizzo in combinazione con la documentazione degli standard pubblici, la programmazione di rete e i concetti relativi ai sistemi distribuiti del gruppo di lavoro e presuppone che il lettore abbia familiarità con il materiale menzionato in questo caso o abbia accesso immediato.</span><span class="sxs-lookup"><span data-stu-id="8992a-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="8992a-132">Una specifica del protocollo WSPP non richiede l'uso di strumenti di programmazione Microsoft o ambienti di programmazione per consentire a una licenza di sviluppare un'implementazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="8992a-133">Le licenze che hanno accesso agli strumenti e agli ambienti di programmazione Microsoft sono gratuite per sfruttarle.</span><span class="sxs-lookup"><span data-stu-id="8992a-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="8992a-134">1 Introduzione</span><span class="sxs-lookup"><span data-stu-id="8992a-134">1 Introduction</span></span>

-   [<span data-ttu-id="8992a-135">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="8992a-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="8992a-136">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="8992a-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="8992a-137">Panoramica sul protocollo 1,3 (sinossia)</span><span class="sxs-lookup"><span data-stu-id="8992a-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="8992a-138">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="8992a-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="8992a-139">1,5 prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="8992a-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="8992a-140">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="8992a-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="8992a-141">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="8992a-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="8992a-142">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="8992a-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="8992a-143">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="8992a-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="8992a-144">1.1 Glossario</span><span class="sxs-lookup"><span data-stu-id="8992a-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="8992a-145">I termini seguenti sono definiti nella sezione Glossario di \[ ms-sys \] :</span><span class="sxs-lookup"><span data-stu-id="8992a-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="8992a-146">GUID</span><span class="sxs-lookup"><span data-stu-id="8992a-146">GUID</span></span>
> -   <span data-ttu-id="8992a-147">Little Endian</span><span class="sxs-lookup"><span data-stu-id="8992a-147">Little Endian</span></span>
> -   <span data-ttu-id="8992a-148">Named pipe</span><span class="sxs-lookup"><span data-stu-id="8992a-148">Named Pipe</span></span>
> -   <span data-ttu-id="8992a-149">Percorso</span><span class="sxs-lookup"><span data-stu-id="8992a-149">Path</span></span>

 

<span data-ttu-id="8992a-150">**Binding**: richiesta di inclusione di una determinata **colonna** in un **set di righe** restituito.</span><span class="sxs-lookup"><span data-stu-id="8992a-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="8992a-151">L' **associazione** specifica una proprietà da includere nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="8992a-152">**Segnalibro**: marcatore che identifica in modo univoco una riga all'interno di un set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="8992a-153">**Catalog**: unità di livello superiore dell'organizzazione nel servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="8992a-154">Rappresenta un set di documenti indicizzati su cui è possibile eseguire query utilizzando il protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="8992a-155">**Category**: raggruppamento gerarchico di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="8992a-156">Ad esempio, il risultato di una query contenente le colonne autore e titolo può essere categorizzato in base all'autore.</span><span class="sxs-lookup"><span data-stu-id="8992a-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="8992a-157">Ogni gruppo di righe contenente lo stesso valore per autore costituisce una categoria.</span><span class="sxs-lookup"><span data-stu-id="8992a-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="8992a-158">**Capitolo** : un intervallo di **righe** all'interno di un set di **righe** .</span><span class="sxs-lookup"><span data-stu-id="8992a-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="8992a-159">**Column**: contenitore per un singolo tipo di informazioni in una **riga** .</span><span class="sxs-lookup"><span data-stu-id="8992a-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="8992a-160">Le colonne eseguono il mapping ai nomi di proprietà e specificano quali proprietà vengono usate per gli elementi della **struttura ad albero** dei **comandi** della query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="8992a-161">**Albero dei comandi**: una combinazione di **restrizioni** , **categorie** e **ordinamenti specificati per** la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="8992a-162">**Cursor**: entità utilizzata come meccanismo per lavorare con una **riga** o un piccolo blocco di **righe** alla volta in un set di dati restituito in un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="8992a-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="8992a-163">Un **cursore** viene posizionato in corrispondenza di una singola **riga** all'interno del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="8992a-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="8992a-164">Dopo aver posizionato il **cursore** su una riga, è possibile eseguire le operazioni su tale **riga** o su un blocco di **righe** a partire da quella posizione.</span><span class="sxs-lookup"><span data-stu-id="8992a-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="8992a-165">**Handle**: token che può essere utilizzato per identificare e accedere a **cursori** , **capitoli** e **segnalibri** .</span><span class="sxs-lookup"><span data-stu-id="8992a-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="8992a-166">**Index**: struttura permanente che contiene il contenuto di testo estratto dai file da un **servizio di indicizzazione** .</span><span class="sxs-lookup"><span data-stu-id="8992a-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="8992a-167">Include l'elenco di parole, che vengono archiviate insieme al nome file, alla posizione e alle **impostazioni locali** .</span><span class="sxs-lookup"><span data-stu-id="8992a-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="8992a-168">**Indicizzazione**: processo di estrazione di testo e proprietà da file e archiviazione dei valori estratti negli **indici** (per il testo) e nella **cache delle proprietà** (per le proprietà).</span><span class="sxs-lookup"><span data-stu-id="8992a-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="8992a-169">**Servizio di indicizzazione**: un servizio che crea **cataloghi** indicizzati per il contenuto e le proprietà dei file System.</span><span class="sxs-lookup"><span data-stu-id="8992a-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="8992a-170">Le applicazioni possono eseguire ricerche nei cataloghi per ottenere informazioni dai file nella file system indicizzata.</span><span class="sxs-lookup"><span data-stu-id="8992a-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="8992a-171">**Impostazioni locali**: un identificatore, come specificato nell' \[ appendice MS-GPSI \] , che specifica le preferenze relative alla lingua.</span><span class="sxs-lookup"><span data-stu-id="8992a-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="8992a-172">Queste preferenze indicano il modo in cui le date e le ore devono essere formattate, gli elementi devono essere ordinati alfabeticamente, le stringhe devono essere confrontate e così via.</span><span class="sxs-lookup"><span data-stu-id="8992a-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="8992a-173">**Query in linguaggio naturale**: una query costruita usando il linguaggio umano invece della sintassi di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="8992a-174">**Parole non significative**: una parola che viene ignorata dal servizio di indicizzazione quando è presente nelle **restrizioni** specificate per la query di ricerca perché presenta un valore discriminatorio minimo.</span><span class="sxs-lookup"><span data-stu-id="8992a-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="8992a-175">Gli esempi in inglese includono "a", "and" e "The".</span><span class="sxs-lookup"><span data-stu-id="8992a-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="8992a-176">**Cache delle proprietà**: una cache delle proprietà dei file estratte da un **servizio di indicizzazione** .</span><span class="sxs-lookup"><span data-stu-id="8992a-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="8992a-177">**Indicizzazione delle proprietà**: processo di creazione di un **Indice** di proprietà del **tipo di valore** di un documento, tra cui autore, oggetto, tipo, conteggio delle parole, conteggio delle pagine stampate e qualsiasi altra proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="8992a-178">**Restrizione**: set di condizioni che un file deve soddisfare per essere incluso nei risultati della ricerca restituiti dal **servizio di indicizzazione** in risposta a una query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="8992a-179">Una **restrizione** restringe l'attenzione di una query di ricerca, limitando i file che il **servizio di indicizzazione** include nei risultati della ricerca solo a quelli che soddisfano le condizioni.</span><span class="sxs-lookup"><span data-stu-id="8992a-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="8992a-180">**Row**: raccolta di **colonne** contenente i valori delle proprietà che descrivono un singolo file del set di file che corrisponde alle **restrizioni** specificate nella query di ricerca inviata al **servizio di indicizzazione** .</span><span class="sxs-lookup"><span data-stu-id="8992a-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="8992a-181">**Rowset**: set di **righe** restituito nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="8992a-182">**Ordinamento**: set di regole in una query di ricerca che definiscono l'ordinamento delle righe nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="8992a-183">Ogni regola è costituita da una proprietà (nome, dimensioni e così via) e da una direzione per l'ordinamento (crescente o decrescente).</span><span class="sxs-lookup"><span data-stu-id="8992a-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="8992a-184">Più regole vengono applicate in sequenza</span><span class="sxs-lookup"><span data-stu-id="8992a-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="8992a-185">**Proprietà di tipo text**: proprietà che descrive il contenuto di un documento e ha solo testo non formattato associato al nome.</span><span class="sxs-lookup"><span data-stu-id="8992a-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="8992a-186">**Proprietà di tipo valore**: proprietà che descrive un singolo attributo di un intero documento.</span><span class="sxs-lookup"><span data-stu-id="8992a-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="8992a-187">Una proprietà di tipo valore ha un ID del tipo di dati e un valore di tale tipo di dati associato al nome.</span><span class="sxs-lookup"><span data-stu-id="8992a-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="8992a-188">**Radice virtuale**: un percorso alternativo a una cartella.</span><span class="sxs-lookup"><span data-stu-id="8992a-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="8992a-189">Una cartella fisica può avere zero o più radici virtuali.</span><span class="sxs-lookup"><span data-stu-id="8992a-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="8992a-190">I percorsi che iniziano con una radice virtuale sono denominati percorsi virtuali.</span><span class="sxs-lookup"><span data-stu-id="8992a-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="8992a-191">Ad esempio,/server/vanityroot potrebbe essere una radice virtuale di C: \\ \\ folder1 Web IIS \\ .</span><span class="sxs-lookup"><span data-stu-id="8992a-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="8992a-192">Il file C: \\ IIS \\ web \\ folder1 \\default.htm avrà quindi un percorso virtuale/Server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="8992a-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="8992a-193">**May, should, Most, should not, must not**: questi termini (in tutti i limiti) vengono usati come descritto in \[ RFC2119 \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="8992a-194">Tutte le istruzioni di comportamento facoltativo usano MAY, SHOULD, o SHOULD NOT.</span><span class="sxs-lookup"><span data-stu-id="8992a-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="8992a-195">1.2 Riferimenti</span><span class="sxs-lookup"><span data-stu-id="8992a-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="8992a-196">1.2.1 Riferimenti normativi</span><span class="sxs-lookup"><span data-stu-id="8992a-196">1.2.1 Normative References</span></span>

<span data-ttu-id="8992a-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "standard for Binary Floating-Point aritmetico", IEEE 754-1985, ottobre 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="8992a-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="8992a-198">\[MS-DCOM \] Microsoft Corporation, "distributed Component Object Model Remote Protocols", giugno 2006.</span><span class="sxs-lookup"><span data-stu-id="8992a-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="8992a-199">\[MS-GPSI \] Microsoft Corporation, "criteri di gruppo Installazione software Extension", 2006 giugno.</span><span class="sxs-lookup"><span data-stu-id="8992a-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="8992a-200">\[MS-SMB \] Microsoft Corporation, protocollo "Microsoft Server Message Block (SMB) ed estensioni", 2006 maggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="8992a-201">\[MS-SYS \] Microsoft Corporation, "System Overview V4", luglio 2006.</span><span class="sxs-lookup"><span data-stu-id="8992a-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="8992a-202">\[Salton \] Salton, G., "elaborazione automatica del testo: analisi della trasformazione e recupero di informazioni per computer", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="8992a-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="8992a-203">\[UNICODE \] il Consorzio Unicode, "lo standard Unicode, versione 2,0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="8992a-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="8992a-204">1.2.2 Riferimenti informativi</span><span class="sxs-lookup"><span data-stu-id="8992a-204">1.2.2 Informative References</span></span>

<span data-ttu-id="8992a-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="8992a-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="8992a-206">\[MSDN-QUERYERR \] Microsoft Corporation, valori Query-Execution, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="8992a-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="8992a-207">Panoramica sul protocollo 1,3 (sinossia)</span><span class="sxs-lookup"><span data-stu-id="8992a-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="8992a-208">Un **servizio di indicizzazione** del contenuto consente di organizzare in modo efficiente le funzionalità estratte di una raccolta di documenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="8992a-209">Il protocollo CISP (Content Indexing Service) consente a un client di comunicare con un server che ospita un servizio di indicizzazione per eseguire query e consentire a un amministratore di gestire il server di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="8992a-210">Quando si elaborano i file, un servizio di indicizzazione analizza un set di documenti e ne riorganizza il contenuto in modo che le **Proprietà** di tali documenti possano essere restituite in modo efficiente in risposta alle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="8992a-211">Una raccolta di documenti su cui è possibile eseguire query è costituita da un **Catalogo** .</span><span class="sxs-lookup"><span data-stu-id="8992a-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="8992a-212">Un catalogo può contenere un **Indice** (per riferimento rapido al testo) e una **cache delle proprietà** (per il recupero rapido dei valori delle proprietà).</span><span class="sxs-lookup"><span data-stu-id="8992a-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="8992a-213">Concettualmente, un catalogo è costituito da una "tabella" logica di proprietà con il testo o il valore e le impostazioni locali corrispondenti archiviate nelle **colonne** della tabella.</span><span class="sxs-lookup"><span data-stu-id="8992a-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="8992a-214">Ogni "riga" della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni "colonna" della tabella corrisponde a una proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="8992a-215">Le attività specifiche eseguite da CISP vengono raggruppate in due aree funzionali:</span><span class="sxs-lookup"><span data-stu-id="8992a-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="8992a-216">Amministrazione remota dei cataloghi di servizi di indicizzazione,</span><span class="sxs-lookup"><span data-stu-id="8992a-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="8992a-217">Esecuzione di query remote sui cataloghi dei servizi di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="8992a-218">1.3.1 attività di amministrazione remota</span><span class="sxs-lookup"><span data-stu-id="8992a-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="8992a-219">CISP Abilita le seguenti attività di gestione del catalogo dei servizi di indicizzazione da un client:</span><span class="sxs-lookup"><span data-stu-id="8992a-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="8992a-220">Eseguire una query sullo stato corrente di un catalogo di servizi di indicizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="8992a-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="8992a-221">Aggiornare lo stato di un catalogo di servizi di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="8992a-222">Avviare il processo di indicizzazione per un determinato set di file.</span><span class="sxs-lookup"><span data-stu-id="8992a-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="8992a-223">Avviare l'ottimizzazione di un indice per migliorare le prestazioni di esecuzione delle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="8992a-224">Tutte le attività di amministrazione remota seguono un semplice modello di richiesta/risposta.</span><span class="sxs-lookup"><span data-stu-id="8992a-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="8992a-225">Non viene mantenuto alcuno stato sul client per nessuna chiamata di amministrazione e le chiamate amministrative possono essere eseguite in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="8992a-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="8992a-226">1.3.2 query remote</span><span class="sxs-lookup"><span data-stu-id="8992a-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="8992a-227">CISP consente ai client di eseguire query di ricerca su un server remoto che ospita un servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="8992a-228">L'invio di una query di ricerca è un processo in più passaggi avviato dal client.</span><span class="sxs-lookup"><span data-stu-id="8992a-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="8992a-229">Attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="8992a-230">Il client richiede una connessione a un server che ospita un servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="8992a-231">Il client invia i parametri per la query di ricerca, che includono:</span><span class="sxs-lookup"><span data-stu-id="8992a-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="8992a-232">**Limitazioni** per specificare quali documenti devono essere inclusi e/o esclusi dai risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="8992a-233">Ordine in cui devono essere restituiti i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="8992a-234">Colonne da restituire nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="8992a-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="8992a-235">Numero massimo di **righe** che devono essere restituite per la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="8992a-236">Tempo massimo per l'esecuzione delle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="8992a-237">Una volta che il server ha riconosciuto la richiesta di avvio della query da parte del client, il client può richiedere informazioni sullo stato della query, ma non si tratta di un passaggio obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8992a-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="8992a-238">Il client specifica quindi le proprietà che il server deve includere nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="8992a-239">Il client richiede un set di risultati dal server e il server risponde inviando al client i valori della proprietà per i file inclusi nei risultati per la query di ricerca del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="8992a-240">Se il valore di una proprietà è troppo grande per essere inserito in un singolo buffer di risposta, il server non invierà la proprietà, ma lo stato della proprietà verrà impostato su rinviato.</span><span class="sxs-lookup"><span data-stu-id="8992a-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="8992a-241">Il client richiede quindi il valore della proprietà separatamente usando una serie di richieste per i blocchi successivi del valore, quindi riprende la richiesta di altri valori.</span><span class="sxs-lookup"><span data-stu-id="8992a-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="8992a-242">Una volta terminata la query di ricerca e non sono più necessari risultati aggiuntivi, il client contatta il server per rilasciare la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="8992a-243">Una volta che il server ha rilasciato la query, il client può inviare una richiesta di disconnessione dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="8992a-244">La connessione viene quindi chiusa.</span><span class="sxs-lookup"><span data-stu-id="8992a-244">The connection is then closed.</span></span> <span data-ttu-id="8992a-245">In alternativa, il client può eseguire un'altra query e ripetere la sequenza dal passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="8992a-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="8992a-246">Comportamento di Windows: questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8992a-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="8992a-247">1.4 Relazione con altri protocolli</span><span class="sxs-lookup"><span data-stu-id="8992a-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="8992a-248">Il CISP si basa sul protocollo SMB \[ MS-SMB \] per il trasporto dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="8992a-249">Nessun altro protocollo dipende direttamente dal protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="8992a-250">*Comportamento di Windows: le applicazioni in genere interagiscono con un wrapper di interfaccia OLE DB \[ MSDN-OLEDB \] (ad esempio, un client di protocollo) e non direttamente con il protocollo.*</span><span class="sxs-lookup"><span data-stu-id="8992a-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="8992a-251">1,5 prerequisiti e precondizioni</span><span class="sxs-lookup"><span data-stu-id="8992a-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="8992a-252">Si presuppone che il client abbia ottenuto il nome del server e un nome di catalogo prima che questo protocollo venga richiamato.</span><span class="sxs-lookup"><span data-stu-id="8992a-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="8992a-253">Il modo in cui un client esegue questa operazione esula dall'ambito di questa specifica.</span><span class="sxs-lookup"><span data-stu-id="8992a-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="8992a-254">Si presuppone inoltre che il client e il server dispongano di un'associazione di sicurezza utilizzabile con named pipe \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="8992a-255">1.6 Dichiarazione di applicabilità</span><span class="sxs-lookup"><span data-stu-id="8992a-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="8992a-256">CISP è progettato per l'esecuzione di query e la gestione di cataloghi in un server remoto da un client.</span><span class="sxs-lookup"><span data-stu-id="8992a-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="8992a-257">CISP è deprecato in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8992a-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="8992a-258">1.7 Controllo delle versioni e negoziazione dalla capacità</span><span class="sxs-lookup"><span data-stu-id="8992a-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="8992a-259">Questo protocollo non dispone di meccanismi di negoziazione delle versioni o di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8992a-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="8992a-260">1.8 Campi estendibili dal fornitore</span><span class="sxs-lookup"><span data-stu-id="8992a-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="8992a-261">Questo protocollo utilizza HRESULT che sono estendibili dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="8992a-262">I fornitori possono scegliere i propri valori per questo campo, purché il bit C (0x20000000) sia impostato come specificato nella sezione 4.1.1 di \[ ms-sys \] , a indicare che si tratta di un codice cliente.</span><span class="sxs-lookup"><span data-stu-id="8992a-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="8992a-263">Questo protocollo usa anche valori NTSTATUS tratti dallo spazio dei numeri NTSTATUS definito in \[ ms-sys \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="8992a-264">I fornitori devono riutilizzare questi valori con il significato indicato.</span><span class="sxs-lookup"><span data-stu-id="8992a-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="8992a-265">La scelta di qualsiasi altro valore può comportare il rischio di un conflitto in futuro.</span><span class="sxs-lookup"><span data-stu-id="8992a-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="8992a-266">*Comportamento di Windows: Windows utilizza solo i valori specificati nella sezione 4.1.3 di \[ ms-sys \] .*</span><span class="sxs-lookup"><span data-stu-id="8992a-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="8992a-267">ID proprietà 1.8.1</span><span class="sxs-lookup"><span data-stu-id="8992a-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="8992a-268">Le proprietà sono rappresentate da ID noti come ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="8992a-269">Ogni proprietà deve avere un identificatore univoco globale.</span><span class="sxs-lookup"><span data-stu-id="8992a-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="8992a-270">Questo identificatore è costituito da un **GUID** che rappresenta una raccolta di proprietà denominate set di proprietà più una stringa o un integer a 32 bit per identificare la proprietà all'interno del set.</span><span class="sxs-lookup"><span data-stu-id="8992a-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="8992a-271">Se viene usato il formato integer di ID, i valori 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE vengono considerati non validi.</span><span class="sxs-lookup"><span data-stu-id="8992a-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="8992a-272">I fornitori possono garantire che le proprie proprietà siano definite in modo univoco inserendole in un set di proprietà definito dal rispettivo GUID.</span><span class="sxs-lookup"><span data-stu-id="8992a-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="8992a-273">1.9 Assegnazioni degli standard</span><span class="sxs-lookup"><span data-stu-id="8992a-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="8992a-274">Questo protocollo non prevede assegnazioni di standard, ma solo le assegnazioni private effettuate da Microsoft utilizzando le procedure di allocazione specificate in altri protocolli.</span><span class="sxs-lookup"><span data-stu-id="8992a-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="8992a-275">Questo protocollo è stato allocato da Microsoft named pipe come specificato in \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="8992a-276">L'assegnazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-276">The assignment is:</span></span>



| <span data-ttu-id="8992a-277">Parametro</span><span class="sxs-lookup"><span data-stu-id="8992a-277">Parameter</span></span> | <span data-ttu-id="8992a-278">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-278">Value</span></span>             | <span data-ttu-id="8992a-279">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8992a-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="8992a-280">Nome pipe</span><span class="sxs-lookup"><span data-stu-id="8992a-280">Pipe name</span></span> | <span data-ttu-id="8992a-281">\\\\SKADS ci \_ pipe</span><span class="sxs-lookup"><span data-stu-id="8992a-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="8992a-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="8992a-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="8992a-283">2 Messaggi</span><span class="sxs-lookup"><span data-stu-id="8992a-283">2 Messages</span></span>

-   [<span data-ttu-id="8992a-284">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="8992a-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="8992a-285">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="8992a-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="8992a-286">2.1 Trasporto</span><span class="sxs-lookup"><span data-stu-id="8992a-286">2.1 Transport</span></span>

<span data-ttu-id="8992a-287">Tutti i messaggi devono essere trasportati utilizzando un named pipe, come specificato in \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="8992a-288">Viene utilizzato il seguente nome pipe:</span><span class="sxs-lookup"><span data-stu-id="8992a-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="8992a-289">\\\\SKADS ci \_ pipe</span><span class="sxs-lookup"><span data-stu-id="8992a-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="8992a-290">Questo protocollo usa il protocollo di named pipe SMB sottostante per recuperare l'identità del chiamante che ha effettuato la connessione come specificato nella sezione 2.2.8 di \[ MS-SMB \] . il client deve impostare l'identificazione di sicurezza \_ come ImpersonationLevel nella richiesta per aprire il named pipe.</span><span class="sxs-lookup"><span data-stu-id="8992a-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="8992a-291">2.2 Sintassi dei messaggi</span><span class="sxs-lookup"><span data-stu-id="8992a-291">2.2 Message Syntax</span></span>

<span data-ttu-id="8992a-292">Diverse strutture e messaggi nelle sezioni seguenti si riferiscono agli handle del capitolo o dei segnalibri.</span><span class="sxs-lookup"><span data-stu-id="8992a-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="8992a-293">Un handle è una struttura opaca lunga a 32 bit che identifica in modo univoco un capitolo o un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="8992a-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="8992a-294">In genere, le applicazioni client ricevono valori di handle tramite chiamate al metodo; Tuttavia, esistono diversi valori noti che non devono essere ottenuti da un server, il cui significato è specificato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="8992a-295">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-295">Value</span></span>                         | <span data-ttu-id="8992a-296">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-297">DB \_ null \_ hChapter 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="8992a-298">Handle del capitolo per il set di righe non sottocapito, che contiene tutti i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="8992a-299">DBBMK \_ primo 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="8992a-300">Handle di segnalibro per un segnalibro che identifica la prima riga nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="8992a-301">DBBMK \_ ultimo 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="8992a-302">Handle di segnalibro per un segnalibro che identifica l'ultima riga nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="8992a-303">2.2.1 strutture</span><span class="sxs-lookup"><span data-stu-id="8992a-303">2.2.1 Structures</span></span>

<span data-ttu-id="8992a-304">In questa sezione vengono illustrate in dettaglio le strutture di dati definite e utilizzate da CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="8992a-305">Tutti gli Integer a 2, 4 e 8 byte con segno e senza segno nelle seguenti strutture devono essere trasferiti nell'ordine dei byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="8992a-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="8992a-306">Nella tabella seguente sono riepilogate le strutture di dati definite in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="8992a-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="8992a-307">Struttura</span><span class="sxs-lookup"><span data-stu-id="8992a-307">Structure</span></span>                    | <span data-ttu-id="8992a-308">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8992a-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="8992a-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="8992a-310">Contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata in una struttura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="8992a-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="8992a-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="8992a-312">Contiene una matrice multidimensionale.</span><span class="sxs-lookup"><span data-stu-id="8992a-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="8992a-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="8992a-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="8992a-314">Rappresenta i limiti per una dimensione di una matrice specificata in una struttura SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="8992a-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="8992a-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="8992a-315">CFullPropSpec</span></span>                | <span data-ttu-id="8992a-316">Contiene una specifica della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="8992a-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-317">CContentRestriction</span></span>          | <span data-ttu-id="8992a-318">Contiene una stringa di cui trovare una corrispondenza per un valore di proprietà nella cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="8992a-319">CKey</span><span class="sxs-lookup"><span data-stu-id="8992a-319">CKey</span></span>                         | <span data-ttu-id="8992a-320">Contiene un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="8992a-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="8992a-322">Contiene un valore della proprietà da confrontare con un'operazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="8992a-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="8992a-324">Contiene una corrispondenza di query in linguaggio naturale per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="8992a-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-325">CNodeRestriction</span></span>             | <span data-ttu-id="8992a-326">Contiene una matrice di nodi della struttura ad albero dei comandi che specificano le restrizioni per una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="8992a-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-327">COccRestriction</span></span>              | <span data-ttu-id="8992a-328">Contiene la posizione di una parola in una frase.</span><span class="sxs-lookup"><span data-stu-id="8992a-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="8992a-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-329">CPropertyRestriction</span></span>         | <span data-ttu-id="8992a-330">Contiene un valore della proprietà da confrontare con un'operazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="8992a-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-331">CRangeRestriction</span></span>            | <span data-ttu-id="8992a-332">Contiene una restrizione per un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="8992a-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="8992a-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-333">CScopeRestriction</span></span>            | <span data-ttu-id="8992a-334">Contiene una restrizione sui file in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="8992a-335">CSort</span><span class="sxs-lookup"><span data-stu-id="8992a-335">CSort</span></span>                        | <span data-ttu-id="8992a-336">Identifica una colonna da ordinare.</span><span class="sxs-lookup"><span data-stu-id="8992a-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="8992a-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-337">CSynRestriction</span></span>              | <span data-ttu-id="8992a-338">Contiene una parola o i sinonimi per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="8992a-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-339">CVectorRestriction</span></span>           | <span data-ttu-id="8992a-340">Contiene un'operazione ponderata o su un nodo della struttura ad albero del comando.</span><span class="sxs-lookup"><span data-stu-id="8992a-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="8992a-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-341">CWordRestriction</span></span>             | <span data-ttu-id="8992a-342">Contiene una parola per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="8992a-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-343">CRestriction</span></span>                 | <span data-ttu-id="8992a-344">Contiene un nodo di un albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="8992a-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="8992a-345">CColumnSet</span></span>                   | <span data-ttu-id="8992a-346">Indica il numero di colonne da restituire.</span><span class="sxs-lookup"><span data-stu-id="8992a-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="8992a-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="8992a-347">CCategorizationSet</span></span>           | <span data-ttu-id="8992a-348">Contiene informazioni sul raggruppamento di un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="8992a-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="8992a-349">CCategorizationSpec</span></span>          | <span data-ttu-id="8992a-350">Contiene una definizione di categorie in cui verranno categorizzati i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="8992a-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="8992a-351">CDbColId</span></span>                     | <span data-ttu-id="8992a-352">Contiene una colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="8992a-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="8992a-353">CDbProp</span></span>                      | <span data-ttu-id="8992a-354">Contiene una proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="8992a-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="8992a-355">CDbPropSet</span></span>                   | <span data-ttu-id="8992a-356">Contiene un set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="8992a-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="8992a-357">CPidMapper</span></span>                   | <span data-ttu-id="8992a-358">Contiene una matrice di ID di proprietà che specificano le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="8992a-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="8992a-359">CRowSeekAt</span></span>                   | <span data-ttu-id="8992a-360">Contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="8992a-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="8992a-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="8992a-362">Identifica il punto in corrispondenza del quale iniziare il recupero per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="8992a-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="8992a-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="8992a-364">Identifica i segnalibri da cui recuperare le righe per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="8992a-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="8992a-365">CRowSeekNext</span></span>                 | <span data-ttu-id="8992a-366">Contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="8992a-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="8992a-367">CRowsetProperties</span></span>            | <span data-ttu-id="8992a-368">Contiene le informazioni di configurazione per una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="8992a-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="8992a-369">CSortSet</span></span>                     | <span data-ttu-id="8992a-370">Contiene l'ordinamento di una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="8992a-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="8992a-371">CTableColumn</span></span>                 | <span data-ttu-id="8992a-372">Contiene una colonna per il messaggio CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="8992a-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="8992a-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="8992a-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="8992a-374">Contiene un valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="8992a-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="8992a-375">CBaseStorageVariant 2.2.1.1</span><span class="sxs-lookup"><span data-stu-id="8992a-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="8992a-376">La struttura CBaseStorageVariant contiene il valore su cui eseguire un'operazione di corrispondenza per una proprietà specificata nella struttura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="8992a-377">0</span><span class="sxs-lookup"><span data-stu-id="8992a-377">0</span></span>

<span data-ttu-id="8992a-378">1</span><span class="sxs-lookup"><span data-stu-id="8992a-378">1</span></span>

<span data-ttu-id="8992a-379">2</span><span class="sxs-lookup"><span data-stu-id="8992a-379">2</span></span>

<span data-ttu-id="8992a-380">3</span><span class="sxs-lookup"><span data-stu-id="8992a-380">3</span></span>

<span data-ttu-id="8992a-381">4</span><span class="sxs-lookup"><span data-stu-id="8992a-381">4</span></span>

<span data-ttu-id="8992a-382">5</span><span class="sxs-lookup"><span data-stu-id="8992a-382">5</span></span>

<span data-ttu-id="8992a-383">6</span><span class="sxs-lookup"><span data-stu-id="8992a-383">6</span></span>

<span data-ttu-id="8992a-384">7</span><span class="sxs-lookup"><span data-stu-id="8992a-384">7</span></span>

<span data-ttu-id="8992a-385">8</span><span class="sxs-lookup"><span data-stu-id="8992a-385">8</span></span>

<span data-ttu-id="8992a-386">9</span><span class="sxs-lookup"><span data-stu-id="8992a-386">9</span></span>

<span data-ttu-id="8992a-387">1</span><span class="sxs-lookup"><span data-stu-id="8992a-387">1</span></span><br/> <span data-ttu-id="8992a-388">0</span><span class="sxs-lookup"><span data-stu-id="8992a-388">0</span></span><br/>

<span data-ttu-id="8992a-389">1</span><span class="sxs-lookup"><span data-stu-id="8992a-389">1</span></span>

<span data-ttu-id="8992a-390">2</span><span class="sxs-lookup"><span data-stu-id="8992a-390">2</span></span>

<span data-ttu-id="8992a-391">3</span><span class="sxs-lookup"><span data-stu-id="8992a-391">3</span></span>

<span data-ttu-id="8992a-392">4</span><span class="sxs-lookup"><span data-stu-id="8992a-392">4</span></span>

<span data-ttu-id="8992a-393">5</span><span class="sxs-lookup"><span data-stu-id="8992a-393">5</span></span>

<span data-ttu-id="8992a-394">6</span><span class="sxs-lookup"><span data-stu-id="8992a-394">6</span></span>

<span data-ttu-id="8992a-395">7</span><span class="sxs-lookup"><span data-stu-id="8992a-395">7</span></span>

<span data-ttu-id="8992a-396">8</span><span class="sxs-lookup"><span data-stu-id="8992a-396">8</span></span>

<span data-ttu-id="8992a-397">9</span><span class="sxs-lookup"><span data-stu-id="8992a-397">9</span></span>

<span data-ttu-id="8992a-398">2</span><span class="sxs-lookup"><span data-stu-id="8992a-398">2</span></span><br/> <span data-ttu-id="8992a-399">0</span><span class="sxs-lookup"><span data-stu-id="8992a-399">0</span></span><br/>

<span data-ttu-id="8992a-400">1</span><span class="sxs-lookup"><span data-stu-id="8992a-400">1</span></span>

<span data-ttu-id="8992a-401">2</span><span class="sxs-lookup"><span data-stu-id="8992a-401">2</span></span>

<span data-ttu-id="8992a-402">3</span><span class="sxs-lookup"><span data-stu-id="8992a-402">3</span></span>

<span data-ttu-id="8992a-403">4</span><span class="sxs-lookup"><span data-stu-id="8992a-403">4</span></span>

<span data-ttu-id="8992a-404">5</span><span class="sxs-lookup"><span data-stu-id="8992a-404">5</span></span>

<span data-ttu-id="8992a-405">6</span><span class="sxs-lookup"><span data-stu-id="8992a-405">6</span></span>

<span data-ttu-id="8992a-406">7</span><span class="sxs-lookup"><span data-stu-id="8992a-406">7</span></span>

<span data-ttu-id="8992a-407">8</span><span class="sxs-lookup"><span data-stu-id="8992a-407">8</span></span>

<span data-ttu-id="8992a-408">9</span><span class="sxs-lookup"><span data-stu-id="8992a-408">9</span></span>

<span data-ttu-id="8992a-409">3</span><span class="sxs-lookup"><span data-stu-id="8992a-409">3</span></span><br/> <span data-ttu-id="8992a-410">0</span><span class="sxs-lookup"><span data-stu-id="8992a-410">0</span></span><br/>

<span data-ttu-id="8992a-411">1</span><span class="sxs-lookup"><span data-stu-id="8992a-411">1</span></span>

<span data-ttu-id="8992a-412">vType</span><span class="sxs-lookup"><span data-stu-id="8992a-412">vType</span></span>

<span data-ttu-id="8992a-413">vData1</span><span class="sxs-lookup"><span data-stu-id="8992a-413">vData1</span></span>

<span data-ttu-id="8992a-414">vData2</span><span class="sxs-lookup"><span data-stu-id="8992a-414">vData2</span></span>

<span data-ttu-id="8992a-415">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-415">vValue (variable)</span></span>



 

<span data-ttu-id="8992a-416">**vType**: indicatore di tipo, che indica il tipo di vValue.</span><span class="sxs-lookup"><span data-stu-id="8992a-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="8992a-417">DEVE essere uno dei valori di VARENUM specificati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8992a-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="8992a-418">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-418">Value</span></span>                 | <span data-ttu-id="8992a-419">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-420">VT \_ vuoto (0x0000)</span><span class="sxs-lookup"><span data-stu-id="8992a-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="8992a-421">vValue non è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="8992a-422">VT \_ null (0x0001)</span><span class="sxs-lookup"><span data-stu-id="8992a-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="8992a-423">vValue non è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="8992a-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="8992a-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="8992a-425">Intero con segno a 1 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="8992a-426">VT \_ Ui1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="8992a-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="8992a-427">Intero senza segno a 1 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="8992a-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="8992a-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="8992a-429">Intero con segno a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="8992a-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="8992a-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="8992a-431">Intero senza segno a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="8992a-432">VT \_ bool (0x000B)</span><span class="sxs-lookup"><span data-stu-id="8992a-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="8992a-433">Valore booleano; intero a 2 byte contenente 0x0000 (FALSE) o 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="8992a-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="8992a-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="8992a-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="8992a-435">Intero con segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="8992a-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="8992a-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="8992a-437">Intero senza segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="8992a-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="8992a-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="8992a-439">Numero a virgola mobile IEEE a 32 bit, come definito in \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="8992a-440">VT \_ int (0x0016)</span><span class="sxs-lookup"><span data-stu-id="8992a-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="8992a-441">Intero con segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="8992a-442">VT \_ uint (0x0017)</span><span class="sxs-lookup"><span data-stu-id="8992a-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="8992a-443">Intero senza segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="8992a-444">\_Errore VT (0x000a)</span><span class="sxs-lookup"><span data-stu-id="8992a-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="8992a-445">Unsigned Integer a 4 byte contenente un HRESULT, come specificato in \[ ms-sys \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="8992a-446">VT \_ i8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="8992a-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="8992a-447">Intero con segno a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="8992a-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="8992a-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="8992a-449">Intero senza segno a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="8992a-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="8992a-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="8992a-451">Numero a virgola mobile IEEE a 64 bit come definito in \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="8992a-452">\_CY VT (0x0006)</span><span class="sxs-lookup"><span data-stu-id="8992a-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="8992a-453">Intero di complemento a due byte a 8 byte (ridimensionato di 10.000).</span><span class="sxs-lookup"><span data-stu-id="8992a-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="8992a-454">\_Data VT (0x0007)</span><span class="sxs-lookup"><span data-stu-id="8992a-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="8992a-455">Numero a virgola mobile a 64 bit che rappresenta il numero di giorni a partire da 00:00:00 il 31 dicembre 1899 (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="8992a-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="8992a-456">FILETIME VT \_ (0x0040)</span><span class="sxs-lookup"><span data-stu-id="8992a-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="8992a-457">Intero a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 00:00:00 il 1 ° gennaio 1601 (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="8992a-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="8992a-458">\_Decimale VT (0x000E)</span><span class="sxs-lookup"><span data-stu-id="8992a-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="8992a-459">Struttura decimale come specificato nella sezione 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="8992a-460">\_CLSID VT (0x0048)</span><span class="sxs-lookup"><span data-stu-id="8992a-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="8992a-461">Valore binario a 16 byte contenente un GUID.</span><span class="sxs-lookup"><span data-stu-id="8992a-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="8992a-462">\_BLOB VT (0x0041)</span><span class="sxs-lookup"><span data-stu-id="8992a-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="8992a-463">Un numero Unsigned Integer di byte di 4 byte nel BLOB, seguito da tale numero di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="8992a-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="8992a-464">\_BSTR VT (0x0008)</span><span class="sxs-lookup"><span data-stu-id="8992a-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="8992a-465">Un numero Unsigned Integer di byte di 4 byte nella stringa, seguito da una stringa, come specificato di seguito in vValue.</span><span class="sxs-lookup"><span data-stu-id="8992a-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="8992a-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="8992a-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="8992a-467">Stringa ANSI con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="8992a-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="8992a-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="8992a-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="8992a-469">Stringa Unicode Unicode con terminazione null \[ \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="8992a-470">\_Variante VT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="8992a-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="8992a-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="8992a-471">CBaseStorageVariant.</span></span> <span data-ttu-id="8992a-472">DEVE essere combinato con un modificatore di tipo di \_ matrice VT o \_ vettore VT.</span><span class="sxs-lookup"><span data-stu-id="8992a-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="8992a-473">Nella tabella seguente vengono specificati i modificatori di tipo per vType.</span><span class="sxs-lookup"><span data-stu-id="8992a-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="8992a-474">I modificatori di tipo possono essere ORed binari con vType per modificare il significato di vValue per indicare che si tratta di uno dei due tipi di matrice possibili.</span><span class="sxs-lookup"><span data-stu-id="8992a-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="8992a-475">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-475">Value</span></span>               | <span data-ttu-id="8992a-476">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-477">\_Vettore VT (0x1000)</span><span class="sxs-lookup"><span data-stu-id="8992a-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="8992a-478">Se l'indicatore di tipo è combinato con \_ un vettore VT usando un operatore OR, vValue è una matrice conteggiata di valori del tipo indicato.</span><span class="sxs-lookup"><span data-stu-id="8992a-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="8992a-479">Per informazioni dettagliate, vedere la sezione 2.2.1.1.1.2.</span><span class="sxs-lookup"><span data-stu-id="8992a-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="8992a-480">Questo modificatore di tipo non deve essere combinato con i tipi seguenti: VT \_ int, VT \_ uint, VT \_ Decimal, VT \_ BLOB, VT \_ BLOB \_ Object.</span><span class="sxs-lookup"><span data-stu-id="8992a-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="8992a-481">\_Array VT (0x2000)</span><span class="sxs-lookup"><span data-stu-id="8992a-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="8992a-482">Se l'indicatore di tipo è combinato con \_ una matrice VT da un operatore OR, il valore è un SAFEARRAY (come specificato nella sezione 2.2.1.1.1.3) che contiene i valori del tipo indicato.</span><span class="sxs-lookup"><span data-stu-id="8992a-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="8992a-483">Questo modificatore di tipo non deve essere combinato con i tipi seguenti: VT \_ i8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ Object, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="8992a-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="8992a-484">**vData1**: quando vType è un \_ numero decimale VT, il valore di questo campo viene specificato come campo di scala nella sezione 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="8992a-485">Per tutti gli altri vTypes, il valore deve essere impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="8992a-486">**vData2**: quando vType è un \_ numero decimale VT, il valore di questo campo viene specificato come campo di segno nella sezione 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="8992a-487">Per tutti gli altri vTypes, il valore deve essere impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="8992a-488">**vValue**: valore per l'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8992a-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="8992a-489">La sintassi deve essere come indicato nel campo vType.</span><span class="sxs-lookup"><span data-stu-id="8992a-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="8992a-490">Nella tabella seguente sono riepilogate le dimensioni per il campo vValue, a seconda del campo vType per i tipi di dati a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="8992a-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="8992a-491">La dimensione è in byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-491">The size is in bytes.</span></span>



| <span data-ttu-id="8992a-492">vType</span><span class="sxs-lookup"><span data-stu-id="8992a-492">vType</span></span>                                                   | <span data-ttu-id="8992a-493">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8992a-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="8992a-494">VT \_ i1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="8992a-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="8992a-495">1</span><span class="sxs-lookup"><span data-stu-id="8992a-495">1</span></span>    |
| <span data-ttu-id="8992a-496">VT \_ I2, VT \_ UI2, VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="8992a-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="8992a-497">2</span><span class="sxs-lookup"><span data-stu-id="8992a-497">2</span></span>    |
| <span data-ttu-id="8992a-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, VT \_ Error</span><span class="sxs-lookup"><span data-stu-id="8992a-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="8992a-499">4</span><span class="sxs-lookup"><span data-stu-id="8992a-499">4</span></span>    |
| <span data-ttu-id="8992a-500">VT \_ i8, VT \_ UI8, VT \_ R8, VT \_ CY, \_ Data VT, \_ FILETIME VT</span><span class="sxs-lookup"><span data-stu-id="8992a-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="8992a-501">8</span><span class="sxs-lookup"><span data-stu-id="8992a-501">8</span></span>    |
| <span data-ttu-id="8992a-502">\_decimale VT, \_ CLSID VT</span><span class="sxs-lookup"><span data-stu-id="8992a-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="8992a-503">16</span><span class="sxs-lookup"><span data-stu-id="8992a-503">16</span></span>   |



 

<span data-ttu-id="8992a-504">Se vType è impostato su VT \_ BLOB, VT \_ BSTR o VT \_ LPSTR, la struttura di vValue viene specificata nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="8992a-505">0</span><span class="sxs-lookup"><span data-stu-id="8992a-505">0</span></span>

<span data-ttu-id="8992a-506">1</span><span class="sxs-lookup"><span data-stu-id="8992a-506">1</span></span>

<span data-ttu-id="8992a-507">2</span><span class="sxs-lookup"><span data-stu-id="8992a-507">2</span></span>

<span data-ttu-id="8992a-508">3</span><span class="sxs-lookup"><span data-stu-id="8992a-508">3</span></span>

<span data-ttu-id="8992a-509">4</span><span class="sxs-lookup"><span data-stu-id="8992a-509">4</span></span>

<span data-ttu-id="8992a-510">5</span><span class="sxs-lookup"><span data-stu-id="8992a-510">5</span></span>

<span data-ttu-id="8992a-511">6</span><span class="sxs-lookup"><span data-stu-id="8992a-511">6</span></span>

<span data-ttu-id="8992a-512">7</span><span class="sxs-lookup"><span data-stu-id="8992a-512">7</span></span>

<span data-ttu-id="8992a-513">8</span><span class="sxs-lookup"><span data-stu-id="8992a-513">8</span></span>

<span data-ttu-id="8992a-514">9</span><span class="sxs-lookup"><span data-stu-id="8992a-514">9</span></span>

<span data-ttu-id="8992a-515">1</span><span class="sxs-lookup"><span data-stu-id="8992a-515">1</span></span><br/> <span data-ttu-id="8992a-516">0</span><span class="sxs-lookup"><span data-stu-id="8992a-516">0</span></span><br/>

<span data-ttu-id="8992a-517">1</span><span class="sxs-lookup"><span data-stu-id="8992a-517">1</span></span>

<span data-ttu-id="8992a-518">2</span><span class="sxs-lookup"><span data-stu-id="8992a-518">2</span></span>

<span data-ttu-id="8992a-519">3</span><span class="sxs-lookup"><span data-stu-id="8992a-519">3</span></span>

<span data-ttu-id="8992a-520">4</span><span class="sxs-lookup"><span data-stu-id="8992a-520">4</span></span>

<span data-ttu-id="8992a-521">5</span><span class="sxs-lookup"><span data-stu-id="8992a-521">5</span></span>

<span data-ttu-id="8992a-522">6</span><span class="sxs-lookup"><span data-stu-id="8992a-522">6</span></span>

<span data-ttu-id="8992a-523">7</span><span class="sxs-lookup"><span data-stu-id="8992a-523">7</span></span>

<span data-ttu-id="8992a-524">8</span><span class="sxs-lookup"><span data-stu-id="8992a-524">8</span></span>

<span data-ttu-id="8992a-525">9</span><span class="sxs-lookup"><span data-stu-id="8992a-525">9</span></span>

<span data-ttu-id="8992a-526">2</span><span class="sxs-lookup"><span data-stu-id="8992a-526">2</span></span><br/> <span data-ttu-id="8992a-527">0</span><span class="sxs-lookup"><span data-stu-id="8992a-527">0</span></span><br/>

<span data-ttu-id="8992a-528">1</span><span class="sxs-lookup"><span data-stu-id="8992a-528">1</span></span>

<span data-ttu-id="8992a-529">2</span><span class="sxs-lookup"><span data-stu-id="8992a-529">2</span></span>

<span data-ttu-id="8992a-530">3</span><span class="sxs-lookup"><span data-stu-id="8992a-530">3</span></span>

<span data-ttu-id="8992a-531">4</span><span class="sxs-lookup"><span data-stu-id="8992a-531">4</span></span>

<span data-ttu-id="8992a-532">5</span><span class="sxs-lookup"><span data-stu-id="8992a-532">5</span></span>

<span data-ttu-id="8992a-533">6</span><span class="sxs-lookup"><span data-stu-id="8992a-533">6</span></span>

<span data-ttu-id="8992a-534">7</span><span class="sxs-lookup"><span data-stu-id="8992a-534">7</span></span>

<span data-ttu-id="8992a-535">8</span><span class="sxs-lookup"><span data-stu-id="8992a-535">8</span></span>

<span data-ttu-id="8992a-536">9</span><span class="sxs-lookup"><span data-stu-id="8992a-536">9</span></span>

<span data-ttu-id="8992a-537">3</span><span class="sxs-lookup"><span data-stu-id="8992a-537">3</span></span><br/> <span data-ttu-id="8992a-538">0</span><span class="sxs-lookup"><span data-stu-id="8992a-538">0</span></span><br/>

<span data-ttu-id="8992a-539">1</span><span class="sxs-lookup"><span data-stu-id="8992a-539">1</span></span>

<span data-ttu-id="8992a-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="8992a-540">cbSize</span></span>

<span data-ttu-id="8992a-541">blobData (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="8992a-542">**cbSize**: intero senza segno a 32 bit, che indica le dimensioni in byte del campo BlobData.</span><span class="sxs-lookup"><span data-stu-id="8992a-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="8992a-543">Se vType è impostato su VT \_ BSTR o VT \_ LPSTR, cbSize deve essere impostato su 0x00000000 quando la stringa rappresentata è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="8992a-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="8992a-544">**blobData**: deve essere di lunghezza cbSize in byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="8992a-545">Per vType impostato su VT \_ BLOB, questo campo è dati BLOB binari opachi.</span><span class="sxs-lookup"><span data-stu-id="8992a-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="8992a-546">Per vType impostato su VT \_ BSTR, questo campo è un set di caratteri in un set di caratteri selezionato OEM.</span><span class="sxs-lookup"><span data-stu-id="8992a-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="8992a-547">Il client e il server devono essere configurati in modo che dispongano di set di caratteri interoperativi (fuori banda del protocollo).</span><span class="sxs-lookup"><span data-stu-id="8992a-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="8992a-548">Non è necessario che sia con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="8992a-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="8992a-549">Per vType impostato su VT \_ LPSTR questo campo è una stringa di caratteri con terminazione null in un set di caratteri selezionato OEM.</span><span class="sxs-lookup"><span data-stu-id="8992a-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="8992a-550">Il client e il server devono essere configurati in modo che dispongano di set di caratteri interoperativi (fuori banda del protocollo).</span><span class="sxs-lookup"><span data-stu-id="8992a-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="8992a-551">Se vType è impostato su VT \_ LPWSTR, la struttura di vValue viene specificata nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="8992a-552">0</span><span class="sxs-lookup"><span data-stu-id="8992a-552">0</span></span>

<span data-ttu-id="8992a-553">1</span><span class="sxs-lookup"><span data-stu-id="8992a-553">1</span></span>

<span data-ttu-id="8992a-554">2</span><span class="sxs-lookup"><span data-stu-id="8992a-554">2</span></span>

<span data-ttu-id="8992a-555">3</span><span class="sxs-lookup"><span data-stu-id="8992a-555">3</span></span>

<span data-ttu-id="8992a-556">4</span><span class="sxs-lookup"><span data-stu-id="8992a-556">4</span></span>

<span data-ttu-id="8992a-557">5</span><span class="sxs-lookup"><span data-stu-id="8992a-557">5</span></span>

<span data-ttu-id="8992a-558">6</span><span class="sxs-lookup"><span data-stu-id="8992a-558">6</span></span>

<span data-ttu-id="8992a-559">7</span><span class="sxs-lookup"><span data-stu-id="8992a-559">7</span></span>

<span data-ttu-id="8992a-560">8</span><span class="sxs-lookup"><span data-stu-id="8992a-560">8</span></span>

<span data-ttu-id="8992a-561">9</span><span class="sxs-lookup"><span data-stu-id="8992a-561">9</span></span>

<span data-ttu-id="8992a-562">1</span><span class="sxs-lookup"><span data-stu-id="8992a-562">1</span></span><br/> <span data-ttu-id="8992a-563">0</span><span class="sxs-lookup"><span data-stu-id="8992a-563">0</span></span><br/>

<span data-ttu-id="8992a-564">1</span><span class="sxs-lookup"><span data-stu-id="8992a-564">1</span></span>

<span data-ttu-id="8992a-565">2</span><span class="sxs-lookup"><span data-stu-id="8992a-565">2</span></span>

<span data-ttu-id="8992a-566">3</span><span class="sxs-lookup"><span data-stu-id="8992a-566">3</span></span>

<span data-ttu-id="8992a-567">4</span><span class="sxs-lookup"><span data-stu-id="8992a-567">4</span></span>

<span data-ttu-id="8992a-568">5</span><span class="sxs-lookup"><span data-stu-id="8992a-568">5</span></span>

<span data-ttu-id="8992a-569">6</span><span class="sxs-lookup"><span data-stu-id="8992a-569">6</span></span>

<span data-ttu-id="8992a-570">7</span><span class="sxs-lookup"><span data-stu-id="8992a-570">7</span></span>

<span data-ttu-id="8992a-571">8</span><span class="sxs-lookup"><span data-stu-id="8992a-571">8</span></span>

<span data-ttu-id="8992a-572">9</span><span class="sxs-lookup"><span data-stu-id="8992a-572">9</span></span>

<span data-ttu-id="8992a-573">2</span><span class="sxs-lookup"><span data-stu-id="8992a-573">2</span></span><br/> <span data-ttu-id="8992a-574">0</span><span class="sxs-lookup"><span data-stu-id="8992a-574">0</span></span><br/>

<span data-ttu-id="8992a-575">1</span><span class="sxs-lookup"><span data-stu-id="8992a-575">1</span></span>

<span data-ttu-id="8992a-576">2</span><span class="sxs-lookup"><span data-stu-id="8992a-576">2</span></span>

<span data-ttu-id="8992a-577">3</span><span class="sxs-lookup"><span data-stu-id="8992a-577">3</span></span>

<span data-ttu-id="8992a-578">4</span><span class="sxs-lookup"><span data-stu-id="8992a-578">4</span></span>

<span data-ttu-id="8992a-579">5</span><span class="sxs-lookup"><span data-stu-id="8992a-579">5</span></span>

<span data-ttu-id="8992a-580">6</span><span class="sxs-lookup"><span data-stu-id="8992a-580">6</span></span>

<span data-ttu-id="8992a-581">7</span><span class="sxs-lookup"><span data-stu-id="8992a-581">7</span></span>

<span data-ttu-id="8992a-582">8</span><span class="sxs-lookup"><span data-stu-id="8992a-582">8</span></span>

<span data-ttu-id="8992a-583">9</span><span class="sxs-lookup"><span data-stu-id="8992a-583">9</span></span>

<span data-ttu-id="8992a-584">3</span><span class="sxs-lookup"><span data-stu-id="8992a-584">3</span></span><br/> <span data-ttu-id="8992a-585">0</span><span class="sxs-lookup"><span data-stu-id="8992a-585">0</span></span><br/>

<span data-ttu-id="8992a-586">1</span><span class="sxs-lookup"><span data-stu-id="8992a-586">1</span></span>

<span data-ttu-id="8992a-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="8992a-587">ccLen</span></span>

<span data-ttu-id="8992a-588">String (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-588">string (variable, optional)</span></span>



 

<span data-ttu-id="8992a-589">**ccLen**: intero senza segno a 32 bit, che indica le dimensioni del campo stringa nei caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="8992a-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="8992a-590">DEVE essere impostato su 0x00000000 per una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="8992a-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="8992a-591">**stringa**: stringa Unicode con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="8992a-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="8992a-592">Strutture CBaseStorageVariant di 2.2.1.1.1</span><span class="sxs-lookup"><span data-stu-id="8992a-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="8992a-593">Nella struttura CBaseStorageVariant vengono utilizzate le strutture seguenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="8992a-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="8992a-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="8992a-595">DECIMAL viene usato per rappresentare un valore numerico esatto con una precisione fissa e una scala fissa.</span><span class="sxs-lookup"><span data-stu-id="8992a-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="8992a-596">Quando vType è impostato su VT \_ Decimal (0x0000E), i campi vData1 e vData2 di CBASESTORAGEVARIANT devono essere interpretati nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="8992a-597">**vData1**: numero di cifre a destra della virgola decimale.</span><span class="sxs-lookup"><span data-stu-id="8992a-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="8992a-598">DEVE essere compreso tra 0 e 28.</span><span class="sxs-lookup"><span data-stu-id="8992a-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="8992a-599">**vData2**: il segno del valore numerico.</span><span class="sxs-lookup"><span data-stu-id="8992a-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="8992a-600">Impostare su 0x00 se positivo, 0x80 se negativo.</span><span class="sxs-lookup"><span data-stu-id="8992a-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="8992a-601">Il formato del Campo vValue è:</span><span class="sxs-lookup"><span data-stu-id="8992a-601">The format of the vValue field is:</span></span>



<span data-ttu-id="8992a-602">0</span><span class="sxs-lookup"><span data-stu-id="8992a-602">0</span></span>

<span data-ttu-id="8992a-603">1</span><span class="sxs-lookup"><span data-stu-id="8992a-603">1</span></span>

<span data-ttu-id="8992a-604">2</span><span class="sxs-lookup"><span data-stu-id="8992a-604">2</span></span>

<span data-ttu-id="8992a-605">3</span><span class="sxs-lookup"><span data-stu-id="8992a-605">3</span></span>

<span data-ttu-id="8992a-606">4</span><span class="sxs-lookup"><span data-stu-id="8992a-606">4</span></span>

<span data-ttu-id="8992a-607">5</span><span class="sxs-lookup"><span data-stu-id="8992a-607">5</span></span>

<span data-ttu-id="8992a-608">6</span><span class="sxs-lookup"><span data-stu-id="8992a-608">6</span></span>

<span data-ttu-id="8992a-609">7</span><span class="sxs-lookup"><span data-stu-id="8992a-609">7</span></span>

<span data-ttu-id="8992a-610">8</span><span class="sxs-lookup"><span data-stu-id="8992a-610">8</span></span>

<span data-ttu-id="8992a-611">9</span><span class="sxs-lookup"><span data-stu-id="8992a-611">9</span></span>

<span data-ttu-id="8992a-612">1</span><span class="sxs-lookup"><span data-stu-id="8992a-612">1</span></span><br/> <span data-ttu-id="8992a-613">0</span><span class="sxs-lookup"><span data-stu-id="8992a-613">0</span></span><br/>

<span data-ttu-id="8992a-614">1</span><span class="sxs-lookup"><span data-stu-id="8992a-614">1</span></span>

<span data-ttu-id="8992a-615">2</span><span class="sxs-lookup"><span data-stu-id="8992a-615">2</span></span>

<span data-ttu-id="8992a-616">3</span><span class="sxs-lookup"><span data-stu-id="8992a-616">3</span></span>

<span data-ttu-id="8992a-617">4</span><span class="sxs-lookup"><span data-stu-id="8992a-617">4</span></span>

<span data-ttu-id="8992a-618">5</span><span class="sxs-lookup"><span data-stu-id="8992a-618">5</span></span>

<span data-ttu-id="8992a-619">6</span><span class="sxs-lookup"><span data-stu-id="8992a-619">6</span></span>

<span data-ttu-id="8992a-620">7</span><span class="sxs-lookup"><span data-stu-id="8992a-620">7</span></span>

<span data-ttu-id="8992a-621">8</span><span class="sxs-lookup"><span data-stu-id="8992a-621">8</span></span>

<span data-ttu-id="8992a-622">9</span><span class="sxs-lookup"><span data-stu-id="8992a-622">9</span></span>

<span data-ttu-id="8992a-623">2</span><span class="sxs-lookup"><span data-stu-id="8992a-623">2</span></span><br/> <span data-ttu-id="8992a-624">0</span><span class="sxs-lookup"><span data-stu-id="8992a-624">0</span></span><br/>

<span data-ttu-id="8992a-625">1</span><span class="sxs-lookup"><span data-stu-id="8992a-625">1</span></span>

<span data-ttu-id="8992a-626">2</span><span class="sxs-lookup"><span data-stu-id="8992a-626">2</span></span>

<span data-ttu-id="8992a-627">3</span><span class="sxs-lookup"><span data-stu-id="8992a-627">3</span></span>

<span data-ttu-id="8992a-628">4</span><span class="sxs-lookup"><span data-stu-id="8992a-628">4</span></span>

<span data-ttu-id="8992a-629">5</span><span class="sxs-lookup"><span data-stu-id="8992a-629">5</span></span>

<span data-ttu-id="8992a-630">6</span><span class="sxs-lookup"><span data-stu-id="8992a-630">6</span></span>

<span data-ttu-id="8992a-631">7</span><span class="sxs-lookup"><span data-stu-id="8992a-631">7</span></span>

<span data-ttu-id="8992a-632">8</span><span class="sxs-lookup"><span data-stu-id="8992a-632">8</span></span>

<span data-ttu-id="8992a-633">9</span><span class="sxs-lookup"><span data-stu-id="8992a-633">9</span></span>

<span data-ttu-id="8992a-634">3</span><span class="sxs-lookup"><span data-stu-id="8992a-634">3</span></span><br/> <span data-ttu-id="8992a-635">0</span><span class="sxs-lookup"><span data-stu-id="8992a-635">0</span></span><br/>

<span data-ttu-id="8992a-636">1</span><span class="sxs-lookup"><span data-stu-id="8992a-636">1</span></span>

<span data-ttu-id="8992a-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="8992a-637">Hi32</span></span>

<span data-ttu-id="8992a-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="8992a-638">Lo32</span></span>

<span data-ttu-id="8992a-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="8992a-639">Mid32</span></span>



 

<span data-ttu-id="8992a-640">**Hi32**: i 32 bit più alti dell'integer a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="8992a-641">**Lo32**: 32 bit più bassi dell'integer a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="8992a-642">**Mid32**: bit 32 intermedi dell'integer a 96 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="8992a-643">vettore 2.2.1.1.1.2 VT \_</span><span class="sxs-lookup"><span data-stu-id="8992a-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="8992a-644">Il \_ vettore VT viene usato per passare matrici unidimensionali.</span><span class="sxs-lookup"><span data-stu-id="8992a-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="8992a-645">0</span><span class="sxs-lookup"><span data-stu-id="8992a-645">0</span></span>

<span data-ttu-id="8992a-646">1</span><span class="sxs-lookup"><span data-stu-id="8992a-646">1</span></span>

<span data-ttu-id="8992a-647">2</span><span class="sxs-lookup"><span data-stu-id="8992a-647">2</span></span>

<span data-ttu-id="8992a-648">3</span><span class="sxs-lookup"><span data-stu-id="8992a-648">3</span></span>

<span data-ttu-id="8992a-649">4</span><span class="sxs-lookup"><span data-stu-id="8992a-649">4</span></span>

<span data-ttu-id="8992a-650">5</span><span class="sxs-lookup"><span data-stu-id="8992a-650">5</span></span>

<span data-ttu-id="8992a-651">6</span><span class="sxs-lookup"><span data-stu-id="8992a-651">6</span></span>

<span data-ttu-id="8992a-652">7</span><span class="sxs-lookup"><span data-stu-id="8992a-652">7</span></span>

<span data-ttu-id="8992a-653">8</span><span class="sxs-lookup"><span data-stu-id="8992a-653">8</span></span>

<span data-ttu-id="8992a-654">9</span><span class="sxs-lookup"><span data-stu-id="8992a-654">9</span></span>

<span data-ttu-id="8992a-655">1</span><span class="sxs-lookup"><span data-stu-id="8992a-655">1</span></span><br/> <span data-ttu-id="8992a-656">0</span><span class="sxs-lookup"><span data-stu-id="8992a-656">0</span></span><br/>

<span data-ttu-id="8992a-657">1</span><span class="sxs-lookup"><span data-stu-id="8992a-657">1</span></span>

<span data-ttu-id="8992a-658">2</span><span class="sxs-lookup"><span data-stu-id="8992a-658">2</span></span>

<span data-ttu-id="8992a-659">3</span><span class="sxs-lookup"><span data-stu-id="8992a-659">3</span></span>

<span data-ttu-id="8992a-660">4</span><span class="sxs-lookup"><span data-stu-id="8992a-660">4</span></span>

<span data-ttu-id="8992a-661">5</span><span class="sxs-lookup"><span data-stu-id="8992a-661">5</span></span>

<span data-ttu-id="8992a-662">6</span><span class="sxs-lookup"><span data-stu-id="8992a-662">6</span></span>

<span data-ttu-id="8992a-663">7</span><span class="sxs-lookup"><span data-stu-id="8992a-663">7</span></span>

<span data-ttu-id="8992a-664">8</span><span class="sxs-lookup"><span data-stu-id="8992a-664">8</span></span>

<span data-ttu-id="8992a-665">9</span><span class="sxs-lookup"><span data-stu-id="8992a-665">9</span></span>

<span data-ttu-id="8992a-666">2</span><span class="sxs-lookup"><span data-stu-id="8992a-666">2</span></span><br/> <span data-ttu-id="8992a-667">0</span><span class="sxs-lookup"><span data-stu-id="8992a-667">0</span></span><br/>

<span data-ttu-id="8992a-668">1</span><span class="sxs-lookup"><span data-stu-id="8992a-668">1</span></span>

<span data-ttu-id="8992a-669">2</span><span class="sxs-lookup"><span data-stu-id="8992a-669">2</span></span>

<span data-ttu-id="8992a-670">3</span><span class="sxs-lookup"><span data-stu-id="8992a-670">3</span></span>

<span data-ttu-id="8992a-671">4</span><span class="sxs-lookup"><span data-stu-id="8992a-671">4</span></span>

<span data-ttu-id="8992a-672">5</span><span class="sxs-lookup"><span data-stu-id="8992a-672">5</span></span>

<span data-ttu-id="8992a-673">6</span><span class="sxs-lookup"><span data-stu-id="8992a-673">6</span></span>

<span data-ttu-id="8992a-674">7</span><span class="sxs-lookup"><span data-stu-id="8992a-674">7</span></span>

<span data-ttu-id="8992a-675">8</span><span class="sxs-lookup"><span data-stu-id="8992a-675">8</span></span>

<span data-ttu-id="8992a-676">9</span><span class="sxs-lookup"><span data-stu-id="8992a-676">9</span></span>

<span data-ttu-id="8992a-677">3</span><span class="sxs-lookup"><span data-stu-id="8992a-677">3</span></span><br/> <span data-ttu-id="8992a-678">0</span><span class="sxs-lookup"><span data-stu-id="8992a-678">0</span></span><br/>

<span data-ttu-id="8992a-679">1</span><span class="sxs-lookup"><span data-stu-id="8992a-679">1</span></span>

<span data-ttu-id="8992a-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="8992a-680">vVectorElements</span></span>

<span data-ttu-id="8992a-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="8992a-681">vVectorData</span></span>



 

<span data-ttu-id="8992a-682">**vVectorElements**: intero senza segno a 32 bit, che indica il numero di elementi nel campo vVectorData.</span><span class="sxs-lookup"><span data-stu-id="8992a-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="8992a-683">**vVectorData**: matrice di elementi il cui tipo è indicato da vType con il bit 0x1000 cancellato.</span><span class="sxs-lookup"><span data-stu-id="8992a-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="8992a-684">Le dimensioni di un singolo elemento a lunghezza fissa possono essere ottenute dalla tabella con tipo di dati a lunghezza fissa, come specificato nella sezione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="8992a-685">La lunghezza di questo campo, in byte, può essere calcolata moltiplicando vVectorElements per la dimensione del singolo elemento.</span><span class="sxs-lookup"><span data-stu-id="8992a-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="8992a-686">Per i tipi di dati a lunghezza variabile vVectorData contiene una sequenza di tipi semplici con marshalling consecutivo in cui il tipo è indicato da vType con il bit 0x1000 cancellato.</span><span class="sxs-lookup"><span data-stu-id="8992a-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="8992a-687">Questo include un caso speciale indicato da vType VT \_ array \| VT \_ Variant (ad esempio, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="8992a-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="8992a-688">Gli elementi nel campo vVectorData devono essere separati da un byte di riempimento compreso tra 0 e 3 in modo che ogni elemento inizi in corrispondenza di un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la matrice.</span><span class="sxs-lookup"><span data-stu-id="8992a-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="8992a-689">Se sono presenti byte di riempimento, il valore che contengono è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="8992a-690">Il contenuto dei byte di riempimento deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-691">Per una vType impostata su VT \_ array \| VT \_ Variant, il tipo per gli elementi in questa sequenza è CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="8992a-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="8992a-692">SAFEARRAY 2.2.1.1.1.3</span><span class="sxs-lookup"><span data-stu-id="8992a-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="8992a-693">SAFEARRAY viene utilizzato per passare matrici multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="8992a-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="8992a-694">La struttura contiene informazioni sulle dimensioni della matrice, oltre ai dati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="8992a-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="8992a-695">0</span><span class="sxs-lookup"><span data-stu-id="8992a-695">0</span></span>

<span data-ttu-id="8992a-696">1</span><span class="sxs-lookup"><span data-stu-id="8992a-696">1</span></span>

<span data-ttu-id="8992a-697">2</span><span class="sxs-lookup"><span data-stu-id="8992a-697">2</span></span>

<span data-ttu-id="8992a-698">3</span><span class="sxs-lookup"><span data-stu-id="8992a-698">3</span></span>

<span data-ttu-id="8992a-699">4</span><span class="sxs-lookup"><span data-stu-id="8992a-699">4</span></span>

<span data-ttu-id="8992a-700">5</span><span class="sxs-lookup"><span data-stu-id="8992a-700">5</span></span>

<span data-ttu-id="8992a-701">6</span><span class="sxs-lookup"><span data-stu-id="8992a-701">6</span></span>

<span data-ttu-id="8992a-702">7</span><span class="sxs-lookup"><span data-stu-id="8992a-702">7</span></span>

<span data-ttu-id="8992a-703">8</span><span class="sxs-lookup"><span data-stu-id="8992a-703">8</span></span>

<span data-ttu-id="8992a-704">9</span><span class="sxs-lookup"><span data-stu-id="8992a-704">9</span></span>

<span data-ttu-id="8992a-705">1</span><span class="sxs-lookup"><span data-stu-id="8992a-705">1</span></span><br/> <span data-ttu-id="8992a-706">0</span><span class="sxs-lookup"><span data-stu-id="8992a-706">0</span></span><br/>

<span data-ttu-id="8992a-707">1</span><span class="sxs-lookup"><span data-stu-id="8992a-707">1</span></span>

<span data-ttu-id="8992a-708">2</span><span class="sxs-lookup"><span data-stu-id="8992a-708">2</span></span>

<span data-ttu-id="8992a-709">3</span><span class="sxs-lookup"><span data-stu-id="8992a-709">3</span></span>

<span data-ttu-id="8992a-710">4</span><span class="sxs-lookup"><span data-stu-id="8992a-710">4</span></span>

<span data-ttu-id="8992a-711">5</span><span class="sxs-lookup"><span data-stu-id="8992a-711">5</span></span>

<span data-ttu-id="8992a-712">6</span><span class="sxs-lookup"><span data-stu-id="8992a-712">6</span></span>

<span data-ttu-id="8992a-713">7</span><span class="sxs-lookup"><span data-stu-id="8992a-713">7</span></span>

<span data-ttu-id="8992a-714">8</span><span class="sxs-lookup"><span data-stu-id="8992a-714">8</span></span>

<span data-ttu-id="8992a-715">9</span><span class="sxs-lookup"><span data-stu-id="8992a-715">9</span></span>

<span data-ttu-id="8992a-716">2</span><span class="sxs-lookup"><span data-stu-id="8992a-716">2</span></span><br/> <span data-ttu-id="8992a-717">0</span><span class="sxs-lookup"><span data-stu-id="8992a-717">0</span></span><br/>

<span data-ttu-id="8992a-718">1</span><span class="sxs-lookup"><span data-stu-id="8992a-718">1</span></span>

<span data-ttu-id="8992a-719">2</span><span class="sxs-lookup"><span data-stu-id="8992a-719">2</span></span>

<span data-ttu-id="8992a-720">3</span><span class="sxs-lookup"><span data-stu-id="8992a-720">3</span></span>

<span data-ttu-id="8992a-721">4</span><span class="sxs-lookup"><span data-stu-id="8992a-721">4</span></span>

<span data-ttu-id="8992a-722">5</span><span class="sxs-lookup"><span data-stu-id="8992a-722">5</span></span>

<span data-ttu-id="8992a-723">6</span><span class="sxs-lookup"><span data-stu-id="8992a-723">6</span></span>

<span data-ttu-id="8992a-724">7</span><span class="sxs-lookup"><span data-stu-id="8992a-724">7</span></span>

<span data-ttu-id="8992a-725">8</span><span class="sxs-lookup"><span data-stu-id="8992a-725">8</span></span>

<span data-ttu-id="8992a-726">9</span><span class="sxs-lookup"><span data-stu-id="8992a-726">9</span></span>

<span data-ttu-id="8992a-727">3</span><span class="sxs-lookup"><span data-stu-id="8992a-727">3</span></span><br/> <span data-ttu-id="8992a-728">0</span><span class="sxs-lookup"><span data-stu-id="8992a-728">0</span></span><br/>

<span data-ttu-id="8992a-729">1</span><span class="sxs-lookup"><span data-stu-id="8992a-729">1</span></span>

<span data-ttu-id="8992a-730">cDims</span><span class="sxs-lookup"><span data-stu-id="8992a-730">cDims</span></span>

<span data-ttu-id="8992a-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="8992a-731">fFeatures</span></span>

<span data-ttu-id="8992a-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="8992a-732">cbElements</span></span>

<span data-ttu-id="8992a-733">Rgsabound (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-733">Rgsabound (variable)</span></span>

<span data-ttu-id="8992a-734">vData (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-734">vData (variable)</span></span>



 

<span data-ttu-id="8992a-735">**cDims**: intero senza segno a 16 bit, che indica il numero di dimensioni della matrice multidimensionale.</span><span class="sxs-lookup"><span data-stu-id="8992a-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="8992a-736">**fFeatures**: bit A 16 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="8992a-737">I valori rappresentano le funzionalità, definite dalle applicazioni di livello superiore, e devono essere ignorate.</span><span class="sxs-lookup"><span data-stu-id="8992a-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="8992a-738">**cbElements**: un Unsigned Integer a 32 bit che specifica la dimensione di ogni elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="8992a-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="8992a-739">**Rgsabound**: matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4, per dimensione in SafeArray.</span><span class="sxs-lookup"><span data-stu-id="8992a-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="8992a-740">Questa matrice contiene prima la dimensione più a sinistra e la dimensione più a destra.</span><span class="sxs-lookup"><span data-stu-id="8992a-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="8992a-741">**vdata**: vettore di elementi di cui è stato eseguito il marshalling di un determinato tipo, indicato da vType dell'oggetto che lo contiene CBaseStorageVariant, con il bit 0x2000 cancellato.</span><span class="sxs-lookup"><span data-stu-id="8992a-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="8992a-742">viene eseguito il marshalling di vData in modo analogo al \_ vettore VT, come specificato nella sezione 2.2.1.1.1.2, con la differenza che il numero di elementi non è archiviato davanti al vettore.</span><span class="sxs-lookup"><span data-stu-id="8992a-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="8992a-743">Invece il numero di elementi viene calcolato moltiplicando il valore cElements con tutti i limiti di matrice sicuri specificati nel campo rgsabound.</span><span class="sxs-lookup"><span data-stu-id="8992a-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="8992a-744">Gli elementi vengono archiviati in un vettore in ordine di dimensioni, scorrendo a partire dalla dimensione più a destra.</span><span class="sxs-lookup"><span data-stu-id="8992a-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="8992a-745">Il diagramma seguente rappresenta visivamente una matrice bidimensionale di esempio.</span><span class="sxs-lookup"><span data-stu-id="8992a-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="8992a-746">La prima dimensione ha cElements uguale a 4 (rappresentato orizzontalmente) e lLbound è uguale a 0, mentre la seconda dimensione ha cElements uguale a 2 (rappresentata verticalmente) e lLbound uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="8992a-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="8992a-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-747">0x00000001</span></span> | <span data-ttu-id="8992a-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-748">0x00000002</span></span> | <span data-ttu-id="8992a-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="8992a-749">0x00000003</span></span> | <span data-ttu-id="8992a-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8992a-750">0x00000005</span></span> |
| <span data-ttu-id="8992a-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="8992a-751">0x00000007</span></span> | <span data-ttu-id="8992a-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8992a-752">0x00000011</span></span> | <span data-ttu-id="8992a-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8992a-753">0x00000013</span></span> | <span data-ttu-id="8992a-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="8992a-754">0x00000017</span></span> |



 

<span data-ttu-id="8992a-755">Utilizzando il diagramma precedente, vData conterrà la sequenza seguente: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (per prima cosa scorrendo la dimensione più a destra e quindi incrementando la dimensione successiva).</span><span class="sxs-lookup"><span data-stu-id="8992a-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="8992a-756">Il rgsabound precedente (che registra cElements e LBound) sarà: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="8992a-757">SAFEARRAYBOUND 2.2.1.1.1.4</span><span class="sxs-lookup"><span data-stu-id="8992a-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="8992a-758">La struttura SAFEARRAYBOUND rappresenta i limiti di una dimensione di SAFEARRAY o SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="8992a-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="8992a-759">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="8992a-759">Its format is:</span></span>



<span data-ttu-id="8992a-760">0</span><span class="sxs-lookup"><span data-stu-id="8992a-760">0</span></span>

<span data-ttu-id="8992a-761">1</span><span class="sxs-lookup"><span data-stu-id="8992a-761">1</span></span>

<span data-ttu-id="8992a-762">2</span><span class="sxs-lookup"><span data-stu-id="8992a-762">2</span></span>

<span data-ttu-id="8992a-763">3</span><span class="sxs-lookup"><span data-stu-id="8992a-763">3</span></span>

<span data-ttu-id="8992a-764">4</span><span class="sxs-lookup"><span data-stu-id="8992a-764">4</span></span>

<span data-ttu-id="8992a-765">5</span><span class="sxs-lookup"><span data-stu-id="8992a-765">5</span></span>

<span data-ttu-id="8992a-766">6</span><span class="sxs-lookup"><span data-stu-id="8992a-766">6</span></span>

<span data-ttu-id="8992a-767">7</span><span class="sxs-lookup"><span data-stu-id="8992a-767">7</span></span>

<span data-ttu-id="8992a-768">8</span><span class="sxs-lookup"><span data-stu-id="8992a-768">8</span></span>

<span data-ttu-id="8992a-769">9</span><span class="sxs-lookup"><span data-stu-id="8992a-769">9</span></span>

<span data-ttu-id="8992a-770">1</span><span class="sxs-lookup"><span data-stu-id="8992a-770">1</span></span><br/> <span data-ttu-id="8992a-771">0</span><span class="sxs-lookup"><span data-stu-id="8992a-771">0</span></span><br/>

<span data-ttu-id="8992a-772">1</span><span class="sxs-lookup"><span data-stu-id="8992a-772">1</span></span>

<span data-ttu-id="8992a-773">2</span><span class="sxs-lookup"><span data-stu-id="8992a-773">2</span></span>

<span data-ttu-id="8992a-774">3</span><span class="sxs-lookup"><span data-stu-id="8992a-774">3</span></span>

<span data-ttu-id="8992a-775">4</span><span class="sxs-lookup"><span data-stu-id="8992a-775">4</span></span>

<span data-ttu-id="8992a-776">5</span><span class="sxs-lookup"><span data-stu-id="8992a-776">5</span></span>

<span data-ttu-id="8992a-777">6</span><span class="sxs-lookup"><span data-stu-id="8992a-777">6</span></span>

<span data-ttu-id="8992a-778">7</span><span class="sxs-lookup"><span data-stu-id="8992a-778">7</span></span>

<span data-ttu-id="8992a-779">8</span><span class="sxs-lookup"><span data-stu-id="8992a-779">8</span></span>

<span data-ttu-id="8992a-780">9</span><span class="sxs-lookup"><span data-stu-id="8992a-780">9</span></span>

<span data-ttu-id="8992a-781">2</span><span class="sxs-lookup"><span data-stu-id="8992a-781">2</span></span><br/> <span data-ttu-id="8992a-782">0</span><span class="sxs-lookup"><span data-stu-id="8992a-782">0</span></span><br/>

<span data-ttu-id="8992a-783">1</span><span class="sxs-lookup"><span data-stu-id="8992a-783">1</span></span>

<span data-ttu-id="8992a-784">2</span><span class="sxs-lookup"><span data-stu-id="8992a-784">2</span></span>

<span data-ttu-id="8992a-785">3</span><span class="sxs-lookup"><span data-stu-id="8992a-785">3</span></span>

<span data-ttu-id="8992a-786">4</span><span class="sxs-lookup"><span data-stu-id="8992a-786">4</span></span>

<span data-ttu-id="8992a-787">5</span><span class="sxs-lookup"><span data-stu-id="8992a-787">5</span></span>

<span data-ttu-id="8992a-788">6</span><span class="sxs-lookup"><span data-stu-id="8992a-788">6</span></span>

<span data-ttu-id="8992a-789">7</span><span class="sxs-lookup"><span data-stu-id="8992a-789">7</span></span>

<span data-ttu-id="8992a-790">8</span><span class="sxs-lookup"><span data-stu-id="8992a-790">8</span></span>

<span data-ttu-id="8992a-791">9</span><span class="sxs-lookup"><span data-stu-id="8992a-791">9</span></span>

<span data-ttu-id="8992a-792">3</span><span class="sxs-lookup"><span data-stu-id="8992a-792">3</span></span><br/> <span data-ttu-id="8992a-793">0</span><span class="sxs-lookup"><span data-stu-id="8992a-793">0</span></span><br/>

<span data-ttu-id="8992a-794">1</span><span class="sxs-lookup"><span data-stu-id="8992a-794">1</span></span>

<span data-ttu-id="8992a-795">cElements</span><span class="sxs-lookup"><span data-stu-id="8992a-795">cElements</span></span>

<span data-ttu-id="8992a-796">lLbound</span><span class="sxs-lookup"><span data-stu-id="8992a-796">lLbound</span></span>



 

<span data-ttu-id="8992a-797">**cElements**: Unsigned Integer a 32 bit, che specifica il numero di elementi nella dimensione.</span><span class="sxs-lookup"><span data-stu-id="8992a-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="8992a-798">**lLbound**: Unsigned Integer A 32 bit, che specifica il limite inferiore della dimensione.</span><span class="sxs-lookup"><span data-stu-id="8992a-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="8992a-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="8992a-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="8992a-800">SAFEARRAY2 viene utilizzato per passare matrici multidimensionali in SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="8992a-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="8992a-801">La struttura contiene informazioni sui limiti e sui dati.</span><span class="sxs-lookup"><span data-stu-id="8992a-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="8992a-802">0</span><span class="sxs-lookup"><span data-stu-id="8992a-802">0</span></span>

<span data-ttu-id="8992a-803">1</span><span class="sxs-lookup"><span data-stu-id="8992a-803">1</span></span>

<span data-ttu-id="8992a-804">2</span><span class="sxs-lookup"><span data-stu-id="8992a-804">2</span></span>

<span data-ttu-id="8992a-805">3</span><span class="sxs-lookup"><span data-stu-id="8992a-805">3</span></span>

<span data-ttu-id="8992a-806">4</span><span class="sxs-lookup"><span data-stu-id="8992a-806">4</span></span>

<span data-ttu-id="8992a-807">5</span><span class="sxs-lookup"><span data-stu-id="8992a-807">5</span></span>

<span data-ttu-id="8992a-808">6</span><span class="sxs-lookup"><span data-stu-id="8992a-808">6</span></span>

<span data-ttu-id="8992a-809">7</span><span class="sxs-lookup"><span data-stu-id="8992a-809">7</span></span>

<span data-ttu-id="8992a-810">8</span><span class="sxs-lookup"><span data-stu-id="8992a-810">8</span></span>

<span data-ttu-id="8992a-811">9</span><span class="sxs-lookup"><span data-stu-id="8992a-811">9</span></span>

<span data-ttu-id="8992a-812">1</span><span class="sxs-lookup"><span data-stu-id="8992a-812">1</span></span><br/> <span data-ttu-id="8992a-813">0</span><span class="sxs-lookup"><span data-stu-id="8992a-813">0</span></span><br/>

<span data-ttu-id="8992a-814">1</span><span class="sxs-lookup"><span data-stu-id="8992a-814">1</span></span>

<span data-ttu-id="8992a-815">2</span><span class="sxs-lookup"><span data-stu-id="8992a-815">2</span></span>

<span data-ttu-id="8992a-816">3</span><span class="sxs-lookup"><span data-stu-id="8992a-816">3</span></span>

<span data-ttu-id="8992a-817">4</span><span class="sxs-lookup"><span data-stu-id="8992a-817">4</span></span>

<span data-ttu-id="8992a-818">5</span><span class="sxs-lookup"><span data-stu-id="8992a-818">5</span></span>

<span data-ttu-id="8992a-819">6</span><span class="sxs-lookup"><span data-stu-id="8992a-819">6</span></span>

<span data-ttu-id="8992a-820">7</span><span class="sxs-lookup"><span data-stu-id="8992a-820">7</span></span>

<span data-ttu-id="8992a-821">8</span><span class="sxs-lookup"><span data-stu-id="8992a-821">8</span></span>

<span data-ttu-id="8992a-822">9</span><span class="sxs-lookup"><span data-stu-id="8992a-822">9</span></span>

<span data-ttu-id="8992a-823">2</span><span class="sxs-lookup"><span data-stu-id="8992a-823">2</span></span><br/> <span data-ttu-id="8992a-824">0</span><span class="sxs-lookup"><span data-stu-id="8992a-824">0</span></span><br/>

<span data-ttu-id="8992a-825">1</span><span class="sxs-lookup"><span data-stu-id="8992a-825">1</span></span>

<span data-ttu-id="8992a-826">2</span><span class="sxs-lookup"><span data-stu-id="8992a-826">2</span></span>

<span data-ttu-id="8992a-827">3</span><span class="sxs-lookup"><span data-stu-id="8992a-827">3</span></span>

<span data-ttu-id="8992a-828">4</span><span class="sxs-lookup"><span data-stu-id="8992a-828">4</span></span>

<span data-ttu-id="8992a-829">5</span><span class="sxs-lookup"><span data-stu-id="8992a-829">5</span></span>

<span data-ttu-id="8992a-830">6</span><span class="sxs-lookup"><span data-stu-id="8992a-830">6</span></span>

<span data-ttu-id="8992a-831">7</span><span class="sxs-lookup"><span data-stu-id="8992a-831">7</span></span>

<span data-ttu-id="8992a-832">8</span><span class="sxs-lookup"><span data-stu-id="8992a-832">8</span></span>

<span data-ttu-id="8992a-833">9</span><span class="sxs-lookup"><span data-stu-id="8992a-833">9</span></span>

<span data-ttu-id="8992a-834">3</span><span class="sxs-lookup"><span data-stu-id="8992a-834">3</span></span><br/> <span data-ttu-id="8992a-835">0</span><span class="sxs-lookup"><span data-stu-id="8992a-835">0</span></span><br/>

<span data-ttu-id="8992a-836">1</span><span class="sxs-lookup"><span data-stu-id="8992a-836">1</span></span>

<span data-ttu-id="8992a-837">cDims</span><span class="sxs-lookup"><span data-stu-id="8992a-837">cDims</span></span>

<span data-ttu-id="8992a-838">Rgsabound (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-838">Rgsabound (variable)</span></span>

<span data-ttu-id="8992a-839">vData (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-839">vData (variable)</span></span>



 

<span data-ttu-id="8992a-840">**cDims**: intero senza segno a 32 bit, che indica il numero di dimensioni di SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="8992a-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="8992a-841">**Rgsabound**: matrice che contiene una struttura SAFEARRAYBOUND, come specificato nella sezione 2.2.1.1.1.4 per dimensione in SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="8992a-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="8992a-842">Questa matrice contiene prima la dimensione più a sinistra e la dimensione più a destra.</span><span class="sxs-lookup"><span data-stu-id="8992a-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="8992a-843">**vdata**: vettore di elementi di cui è stato eseguito il marshalling di un determinato tipo, indicato da dwType dell'oggetto che lo contiene SERIALIZEDPROPERTYVALUE, con bit 0x2000 cancellato.</span><span class="sxs-lookup"><span data-stu-id="8992a-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="8992a-844">Il formato di vData è uguale a quello specificato per il campo vData di SAFEARRAY nella sezione 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="8992a-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="8992a-845">CFullPropSpec 2.2.1.2</span><span class="sxs-lookup"><span data-stu-id="8992a-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="8992a-846">La struttura CFullPropSpec contiene un GUID del set di proprietà e un identificatore di proprietà per identificare in modo univoco la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="8992a-847">0</span><span class="sxs-lookup"><span data-stu-id="8992a-847">0</span></span>

<span data-ttu-id="8992a-848">1</span><span class="sxs-lookup"><span data-stu-id="8992a-848">1</span></span>

<span data-ttu-id="8992a-849">2</span><span class="sxs-lookup"><span data-stu-id="8992a-849">2</span></span>

<span data-ttu-id="8992a-850">3</span><span class="sxs-lookup"><span data-stu-id="8992a-850">3</span></span>

<span data-ttu-id="8992a-851">4</span><span class="sxs-lookup"><span data-stu-id="8992a-851">4</span></span>

<span data-ttu-id="8992a-852">5</span><span class="sxs-lookup"><span data-stu-id="8992a-852">5</span></span>

<span data-ttu-id="8992a-853">6</span><span class="sxs-lookup"><span data-stu-id="8992a-853">6</span></span>

<span data-ttu-id="8992a-854">7</span><span class="sxs-lookup"><span data-stu-id="8992a-854">7</span></span>

<span data-ttu-id="8992a-855">8</span><span class="sxs-lookup"><span data-stu-id="8992a-855">8</span></span>

<span data-ttu-id="8992a-856">9</span><span class="sxs-lookup"><span data-stu-id="8992a-856">9</span></span>

<span data-ttu-id="8992a-857">1</span><span class="sxs-lookup"><span data-stu-id="8992a-857">1</span></span><br/> <span data-ttu-id="8992a-858">0</span><span class="sxs-lookup"><span data-stu-id="8992a-858">0</span></span><br/>

<span data-ttu-id="8992a-859">1</span><span class="sxs-lookup"><span data-stu-id="8992a-859">1</span></span>

<span data-ttu-id="8992a-860">2</span><span class="sxs-lookup"><span data-stu-id="8992a-860">2</span></span>

<span data-ttu-id="8992a-861">3</span><span class="sxs-lookup"><span data-stu-id="8992a-861">3</span></span>

<span data-ttu-id="8992a-862">4</span><span class="sxs-lookup"><span data-stu-id="8992a-862">4</span></span>

<span data-ttu-id="8992a-863">5</span><span class="sxs-lookup"><span data-stu-id="8992a-863">5</span></span>

<span data-ttu-id="8992a-864">6</span><span class="sxs-lookup"><span data-stu-id="8992a-864">6</span></span>

<span data-ttu-id="8992a-865">7</span><span class="sxs-lookup"><span data-stu-id="8992a-865">7</span></span>

<span data-ttu-id="8992a-866">8</span><span class="sxs-lookup"><span data-stu-id="8992a-866">8</span></span>

<span data-ttu-id="8992a-867">9</span><span class="sxs-lookup"><span data-stu-id="8992a-867">9</span></span>

<span data-ttu-id="8992a-868">2</span><span class="sxs-lookup"><span data-stu-id="8992a-868">2</span></span><br/> <span data-ttu-id="8992a-869">0</span><span class="sxs-lookup"><span data-stu-id="8992a-869">0</span></span><br/>

<span data-ttu-id="8992a-870">1</span><span class="sxs-lookup"><span data-stu-id="8992a-870">1</span></span>

<span data-ttu-id="8992a-871">2</span><span class="sxs-lookup"><span data-stu-id="8992a-871">2</span></span>

<span data-ttu-id="8992a-872">3</span><span class="sxs-lookup"><span data-stu-id="8992a-872">3</span></span>

<span data-ttu-id="8992a-873">4</span><span class="sxs-lookup"><span data-stu-id="8992a-873">4</span></span>

<span data-ttu-id="8992a-874">5</span><span class="sxs-lookup"><span data-stu-id="8992a-874">5</span></span>

<span data-ttu-id="8992a-875">6</span><span class="sxs-lookup"><span data-stu-id="8992a-875">6</span></span>

<span data-ttu-id="8992a-876">7</span><span class="sxs-lookup"><span data-stu-id="8992a-876">7</span></span>

<span data-ttu-id="8992a-877">8</span><span class="sxs-lookup"><span data-stu-id="8992a-877">8</span></span>

<span data-ttu-id="8992a-878">9</span><span class="sxs-lookup"><span data-stu-id="8992a-878">9</span></span>

<span data-ttu-id="8992a-879">3</span><span class="sxs-lookup"><span data-stu-id="8992a-879">3</span></span><br/> <span data-ttu-id="8992a-880">0</span><span class="sxs-lookup"><span data-stu-id="8992a-880">0</span></span><br/>

<span data-ttu-id="8992a-881">1</span><span class="sxs-lookup"><span data-stu-id="8992a-881">1</span></span>

<span data-ttu-id="8992a-882">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="8992a-882">\_guidPropSet</span></span>

<span data-ttu-id="8992a-883">...</span><span class="sxs-lookup"><span data-stu-id="8992a-883">...</span></span>

<span data-ttu-id="8992a-884">...</span><span class="sxs-lookup"><span data-stu-id="8992a-884">...</span></span>

<span data-ttu-id="8992a-885">...</span><span class="sxs-lookup"><span data-stu-id="8992a-885">...</span></span>

<span data-ttu-id="8992a-886">ulKind</span><span class="sxs-lookup"><span data-stu-id="8992a-886">ulKind</span></span>

<span data-ttu-id="8992a-887">PrSpec</span><span class="sxs-lookup"><span data-stu-id="8992a-887">PrSpec</span></span>

<span data-ttu-id="8992a-888">Nome proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-888">Property name (variable)</span></span>



 

<span data-ttu-id="8992a-889">**\_ GUIDPROPSET**: GUID del set di proprietà a cui appartiene la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="8992a-890">**ulKind**: Unsigned Integer A 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8992a-891">Uno dei valori seguenti, che indica il contenuto di PrSpec.</span><span class="sxs-lookup"><span data-stu-id="8992a-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="8992a-892">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-892">Value</span></span>                                            | <span data-ttu-id="8992a-893">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-894">\_LPWSTR PRSPEC</span><span class="sxs-lookup"><span data-stu-id="8992a-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="8992a-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-895">0x00000000</span></span><br/> | <span data-ttu-id="8992a-896">Il campo PrSpec specifica il numero di caratteri non NULL nel campo del nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="8992a-897">\_propid PRSPEC</span><span class="sxs-lookup"><span data-stu-id="8992a-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="8992a-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-898">0x00000001</span></span><br/>  | <span data-ttu-id="8992a-899">Il campo PrSpec specifica l'ID della proprietà (PROPID).</span><span class="sxs-lookup"><span data-stu-id="8992a-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="8992a-900">**PrSpec**: un Unsigned Integer a 32 bit con un significato come indicato dal Campo ulKind.</span><span class="sxs-lookup"><span data-stu-id="8992a-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="8992a-901">**Nome proprietà**: se ulKind è impostato su PRSPEC \_ propid, questo campo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="8992a-902">Se ulKind è impostato su PRSPEC \_ LPWSTR, questo campo deve contenere una matrice senza distinzione tra maiuscole e minuscole di PRSPEC caratteri Unicode non null, che contiene il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="8992a-903">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="8992a-904">La struttura CContentRestriction contiene una stringa di cui trovare una corrispondenza per una proprietà nella cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="8992a-905">0</span><span class="sxs-lookup"><span data-stu-id="8992a-905">0</span></span>

<span data-ttu-id="8992a-906">1</span><span class="sxs-lookup"><span data-stu-id="8992a-906">1</span></span>

<span data-ttu-id="8992a-907">2</span><span class="sxs-lookup"><span data-stu-id="8992a-907">2</span></span>

<span data-ttu-id="8992a-908">3</span><span class="sxs-lookup"><span data-stu-id="8992a-908">3</span></span>

<span data-ttu-id="8992a-909">4</span><span class="sxs-lookup"><span data-stu-id="8992a-909">4</span></span>

<span data-ttu-id="8992a-910">5</span><span class="sxs-lookup"><span data-stu-id="8992a-910">5</span></span>

<span data-ttu-id="8992a-911">6</span><span class="sxs-lookup"><span data-stu-id="8992a-911">6</span></span>

<span data-ttu-id="8992a-912">7</span><span class="sxs-lookup"><span data-stu-id="8992a-912">7</span></span>

<span data-ttu-id="8992a-913">8</span><span class="sxs-lookup"><span data-stu-id="8992a-913">8</span></span>

<span data-ttu-id="8992a-914">9</span><span class="sxs-lookup"><span data-stu-id="8992a-914">9</span></span>

<span data-ttu-id="8992a-915">1</span><span class="sxs-lookup"><span data-stu-id="8992a-915">1</span></span><br/> <span data-ttu-id="8992a-916">0</span><span class="sxs-lookup"><span data-stu-id="8992a-916">0</span></span><br/>

<span data-ttu-id="8992a-917">1</span><span class="sxs-lookup"><span data-stu-id="8992a-917">1</span></span>

<span data-ttu-id="8992a-918">2</span><span class="sxs-lookup"><span data-stu-id="8992a-918">2</span></span>

<span data-ttu-id="8992a-919">3</span><span class="sxs-lookup"><span data-stu-id="8992a-919">3</span></span>

<span data-ttu-id="8992a-920">4</span><span class="sxs-lookup"><span data-stu-id="8992a-920">4</span></span>

<span data-ttu-id="8992a-921">5</span><span class="sxs-lookup"><span data-stu-id="8992a-921">5</span></span>

<span data-ttu-id="8992a-922">6</span><span class="sxs-lookup"><span data-stu-id="8992a-922">6</span></span>

<span data-ttu-id="8992a-923">7</span><span class="sxs-lookup"><span data-stu-id="8992a-923">7</span></span>

<span data-ttu-id="8992a-924">8</span><span class="sxs-lookup"><span data-stu-id="8992a-924">8</span></span>

<span data-ttu-id="8992a-925">9</span><span class="sxs-lookup"><span data-stu-id="8992a-925">9</span></span>

<span data-ttu-id="8992a-926">2</span><span class="sxs-lookup"><span data-stu-id="8992a-926">2</span></span><br/> <span data-ttu-id="8992a-927">0</span><span class="sxs-lookup"><span data-stu-id="8992a-927">0</span></span><br/>

<span data-ttu-id="8992a-928">1</span><span class="sxs-lookup"><span data-stu-id="8992a-928">1</span></span>

<span data-ttu-id="8992a-929">2</span><span class="sxs-lookup"><span data-stu-id="8992a-929">2</span></span>

<span data-ttu-id="8992a-930">3</span><span class="sxs-lookup"><span data-stu-id="8992a-930">3</span></span>

<span data-ttu-id="8992a-931">4</span><span class="sxs-lookup"><span data-stu-id="8992a-931">4</span></span>

<span data-ttu-id="8992a-932">5</span><span class="sxs-lookup"><span data-stu-id="8992a-932">5</span></span>

<span data-ttu-id="8992a-933">6</span><span class="sxs-lookup"><span data-stu-id="8992a-933">6</span></span>

<span data-ttu-id="8992a-934">7</span><span class="sxs-lookup"><span data-stu-id="8992a-934">7</span></span>

<span data-ttu-id="8992a-935">8</span><span class="sxs-lookup"><span data-stu-id="8992a-935">8</span></span>

<span data-ttu-id="8992a-936">9</span><span class="sxs-lookup"><span data-stu-id="8992a-936">9</span></span>

<span data-ttu-id="8992a-937">3</span><span class="sxs-lookup"><span data-stu-id="8992a-937">3</span></span><br/> <span data-ttu-id="8992a-938">0</span><span class="sxs-lookup"><span data-stu-id="8992a-938">0</span></span><br/>

<span data-ttu-id="8992a-939">1</span><span class="sxs-lookup"><span data-stu-id="8992a-939">1</span></span>

<span data-ttu-id="8992a-940">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-940">\_Property (variable)</span></span>

<span data-ttu-id="8992a-941">...</span><span class="sxs-lookup"><span data-stu-id="8992a-941">...</span></span>

<span data-ttu-id="8992a-942">Padding1 (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-942">Padding1 (variable)</span></span>

<span data-ttu-id="8992a-943">Cc</span><span class="sxs-lookup"><span data-stu-id="8992a-943">Cc</span></span>

<span data-ttu-id="8992a-944">\_pwcsPhrase (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="8992a-945">...</span><span class="sxs-lookup"><span data-stu-id="8992a-945">...</span></span>

<span data-ttu-id="8992a-946">Padding2 (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-946">Padding2 (variable)</span></span>

<span data-ttu-id="8992a-947">lcid</span><span class="sxs-lookup"><span data-stu-id="8992a-947">lcid</span></span>

<span data-ttu-id="8992a-948">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="8992a-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="8992a-949">**\_ Property**: struttura CFullPropSpec, come specificato nella sezione 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="8992a-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="8992a-950">Questo campo indica la proprietà su cui eseguire un'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8992a-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="8992a-951">**Padding1**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8992a-952">La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura.</span><span class="sxs-lookup"><span data-stu-id="8992a-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8992a-953">Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8992a-954">Il contenuto di questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-955">**CC**: Unsigned Integer a 32 bit, che specifica il numero di caratteri nel \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="8992a-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="8992a-956">**\_ pwcsPhrase**: stringa Unicode senza terminazione null che rappresenta la parola o la frase da confrontare per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="8992a-957">Questo campo non deve essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="8992a-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="8992a-958">Il campo CC contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="8992a-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="8992a-959">**Padding2**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8992a-960">La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura.</span><span class="sxs-lookup"><span data-stu-id="8992a-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8992a-961">Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8992a-962">Il contenuto di questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-963">**LCID**: Unsigned Integer a 32 bit, che indica le impostazioni locali di \_ pwcsPhrase, come specificato in \[ MS-GPSI \] appendice a.</span><span class="sxs-lookup"><span data-stu-id="8992a-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="8992a-964">**\_ ulGenerateMethod**: Unsigned Integer a 32 bit, che specifica il metodo da usare per la generazione di moduli Word alternativi</span><span class="sxs-lookup"><span data-stu-id="8992a-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="8992a-965">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-965">Value</span></span>                                                       | <span data-ttu-id="8992a-966">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-967">GENERA il \_ metodo \_ esatto</span><span class="sxs-lookup"><span data-stu-id="8992a-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="8992a-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-968">0x00000000</span></span><br/>    | <span data-ttu-id="8992a-969">Corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="8992a-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8992a-970">\_prefisso del metodo generate \_</span><span class="sxs-lookup"><span data-stu-id="8992a-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="8992a-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-971">0x00000001</span></span> <br/>  | <span data-ttu-id="8992a-972">Corrispondenza prefisso.</span><span class="sxs-lookup"><span data-stu-id="8992a-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8992a-973">GENERA il \_ metodo \_ flettere</span><span class="sxs-lookup"><span data-stu-id="8992a-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="8992a-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-974">0x00000002</span></span><br/> | <span data-ttu-id="8992a-975">Corrisponde a flessioni di una parola.</span><span class="sxs-lookup"><span data-stu-id="8992a-975">Matches inflections of a word.</span></span> <span data-ttu-id="8992a-976">Una flessione di una parola è una variante della parola radice nella stessa parte del discorso che è stata modificata in base alle regole linguistiche di una determinata lingua.</span><span class="sxs-lookup"><span data-stu-id="8992a-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="8992a-977">Ad esempio, le flessioni del verbo "swim" in inglese includono "swim", "swims", "swimming" e "nuotate".</span><span class="sxs-lookup"><span data-stu-id="8992a-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="8992a-978">CKey 2.2.1.4</span><span class="sxs-lookup"><span data-stu-id="8992a-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="8992a-979">La struttura CKey contiene un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="8992a-980">0</span><span class="sxs-lookup"><span data-stu-id="8992a-980">0</span></span>

<span data-ttu-id="8992a-981">1</span><span class="sxs-lookup"><span data-stu-id="8992a-981">1</span></span>

<span data-ttu-id="8992a-982">2</span><span class="sxs-lookup"><span data-stu-id="8992a-982">2</span></span>

<span data-ttu-id="8992a-983">3</span><span class="sxs-lookup"><span data-stu-id="8992a-983">3</span></span>

<span data-ttu-id="8992a-984">4</span><span class="sxs-lookup"><span data-stu-id="8992a-984">4</span></span>

<span data-ttu-id="8992a-985">5</span><span class="sxs-lookup"><span data-stu-id="8992a-985">5</span></span>

<span data-ttu-id="8992a-986">6</span><span class="sxs-lookup"><span data-stu-id="8992a-986">6</span></span>

<span data-ttu-id="8992a-987">7</span><span class="sxs-lookup"><span data-stu-id="8992a-987">7</span></span>

<span data-ttu-id="8992a-988">8</span><span class="sxs-lookup"><span data-stu-id="8992a-988">8</span></span>

<span data-ttu-id="8992a-989">9</span><span class="sxs-lookup"><span data-stu-id="8992a-989">9</span></span>

<span data-ttu-id="8992a-990">1</span><span class="sxs-lookup"><span data-stu-id="8992a-990">1</span></span><br/> <span data-ttu-id="8992a-991">0</span><span class="sxs-lookup"><span data-stu-id="8992a-991">0</span></span><br/>

<span data-ttu-id="8992a-992">1</span><span class="sxs-lookup"><span data-stu-id="8992a-992">1</span></span>

<span data-ttu-id="8992a-993">2</span><span class="sxs-lookup"><span data-stu-id="8992a-993">2</span></span>

<span data-ttu-id="8992a-994">3</span><span class="sxs-lookup"><span data-stu-id="8992a-994">3</span></span>

<span data-ttu-id="8992a-995">4</span><span class="sxs-lookup"><span data-stu-id="8992a-995">4</span></span>

<span data-ttu-id="8992a-996">5</span><span class="sxs-lookup"><span data-stu-id="8992a-996">5</span></span>

<span data-ttu-id="8992a-997">6</span><span class="sxs-lookup"><span data-stu-id="8992a-997">6</span></span>

<span data-ttu-id="8992a-998">7</span><span class="sxs-lookup"><span data-stu-id="8992a-998">7</span></span>

<span data-ttu-id="8992a-999">8</span><span class="sxs-lookup"><span data-stu-id="8992a-999">8</span></span>

<span data-ttu-id="8992a-1000">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1000">9</span></span>

<span data-ttu-id="8992a-1001">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1001">2</span></span><br/> <span data-ttu-id="8992a-1002">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1002">0</span></span><br/>

<span data-ttu-id="8992a-1003">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1003">1</span></span>

<span data-ttu-id="8992a-1004">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1004">2</span></span>

<span data-ttu-id="8992a-1005">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1005">3</span></span>

<span data-ttu-id="8992a-1006">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1006">4</span></span>

<span data-ttu-id="8992a-1007">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1007">5</span></span>

<span data-ttu-id="8992a-1008">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1008">6</span></span>

<span data-ttu-id="8992a-1009">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1009">7</span></span>

<span data-ttu-id="8992a-1010">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1010">8</span></span>

<span data-ttu-id="8992a-1011">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1011">9</span></span>

<span data-ttu-id="8992a-1012">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1012">3</span></span><br/> <span data-ttu-id="8992a-1013">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1013">0</span></span><br/>

<span data-ttu-id="8992a-1014">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1014">1</span></span>

<span data-ttu-id="8992a-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="8992a-1015">PROPID</span></span>

<span data-ttu-id="8992a-1016">CB</span><span class="sxs-lookup"><span data-stu-id="8992a-1016">Cb</span></span>

<span data-ttu-id="8992a-1017">BUF (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1017">buf (variable)</span></span>



 

<span data-ttu-id="8992a-1018">**Propid**: Unsigned Integer a 32 bit, che rappresenta l'ID della proprietà, come illustrato nella sezione 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="8992a-1019">I valori noti sono:</span><span class="sxs-lookup"><span data-stu-id="8992a-1019">Well-known values are:</span></span>



| <span data-ttu-id="8992a-1020">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1020">Value</span></span>      | <span data-ttu-id="8992a-1021">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="8992a-1022">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="8992a-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="8992a-1023">Rappresenta un ID di proprietà non valido e non deve essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8992a-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="8992a-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="8992a-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="8992a-1025">Rappresenta un ID di proprietà non valido e non deve essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8992a-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="8992a-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-1026">0x00000000</span></span> | <span data-ttu-id="8992a-1027">Rappresenta qualsiasi ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="8992a-1028">**CB**: Unsigned Integer a 32 bit contenente la lunghezza di BUF, in byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="8992a-1029">**BUF**: sequenza di byte che rappresenta il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="8992a-1030">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="8992a-1031">La struttura CInternalPropertyRestriction contiene un valore della proprietà da confrontare con un'operazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="8992a-1032">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1032">0</span></span>

<span data-ttu-id="8992a-1033">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1033">1</span></span>

<span data-ttu-id="8992a-1034">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1034">2</span></span>

<span data-ttu-id="8992a-1035">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1035">3</span></span>

<span data-ttu-id="8992a-1036">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1036">4</span></span>

<span data-ttu-id="8992a-1037">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1037">5</span></span>

<span data-ttu-id="8992a-1038">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1038">6</span></span>

<span data-ttu-id="8992a-1039">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1039">7</span></span>

<span data-ttu-id="8992a-1040">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1040">8</span></span>

<span data-ttu-id="8992a-1041">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1041">9</span></span>

<span data-ttu-id="8992a-1042">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1042">1</span></span><br/> <span data-ttu-id="8992a-1043">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1043">0</span></span><br/>

<span data-ttu-id="8992a-1044">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1044">1</span></span>

<span data-ttu-id="8992a-1045">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1045">2</span></span>

<span data-ttu-id="8992a-1046">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1046">3</span></span>

<span data-ttu-id="8992a-1047">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1047">4</span></span>

<span data-ttu-id="8992a-1048">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1048">5</span></span>

<span data-ttu-id="8992a-1049">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1049">6</span></span>

<span data-ttu-id="8992a-1050">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1050">7</span></span>

<span data-ttu-id="8992a-1051">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1051">8</span></span>

<span data-ttu-id="8992a-1052">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1052">9</span></span>

<span data-ttu-id="8992a-1053">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1053">2</span></span><br/> <span data-ttu-id="8992a-1054">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1054">0</span></span><br/>

<span data-ttu-id="8992a-1055">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1055">1</span></span>

<span data-ttu-id="8992a-1056">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1056">2</span></span>

<span data-ttu-id="8992a-1057">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1057">3</span></span>

<span data-ttu-id="8992a-1058">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1058">4</span></span>

<span data-ttu-id="8992a-1059">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1059">5</span></span>

<span data-ttu-id="8992a-1060">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1060">6</span></span>

<span data-ttu-id="8992a-1061">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1061">7</span></span>

<span data-ttu-id="8992a-1062">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1062">8</span></span>

<span data-ttu-id="8992a-1063">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1063">9</span></span>

<span data-ttu-id="8992a-1064">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1064">3</span></span><br/> <span data-ttu-id="8992a-1065">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1065">0</span></span><br/>

<span data-ttu-id="8992a-1066">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1066">1</span></span>

<span data-ttu-id="8992a-1067">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="8992a-1067">\_relop</span></span>

<span data-ttu-id="8992a-1068">\_pid</span><span class="sxs-lookup"><span data-stu-id="8992a-1068">\_pid</span></span>

<span data-ttu-id="8992a-1069">\_prval (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1069">\_prval (variable)</span></span>

<span data-ttu-id="8992a-1070">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="8992a-1070">restrictionPresent</span></span>

<span data-ttu-id="8992a-1071">nextRestriction (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="8992a-1072">**\_ RelOp**: intero a 32 bit che specifica la relazione da eseguire sulla proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="8992a-1073">DEVE essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="8992a-1074">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1074">Value</span></span>                 | <span data-ttu-id="8992a-1075">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1076">0x00000000 PRLT</span><span class="sxs-lookup"><span data-stu-id="8992a-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="8992a-1077">Confronto di minore di.</span><span class="sxs-lookup"><span data-stu-id="8992a-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="8992a-1078">0x00000001 PRLE</span><span class="sxs-lookup"><span data-stu-id="8992a-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="8992a-1079">Confronto di minore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="8992a-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="8992a-1080">0x00000002 PRGT</span><span class="sxs-lookup"><span data-stu-id="8992a-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="8992a-1081">Confronto maggiore di.</span><span class="sxs-lookup"><span data-stu-id="8992a-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="8992a-1082">0x00000003 PRGE</span><span class="sxs-lookup"><span data-stu-id="8992a-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="8992a-1083">Confronto maggiore di o uguale a.</span><span class="sxs-lookup"><span data-stu-id="8992a-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="8992a-1084">0x00000004 PREQ</span><span class="sxs-lookup"><span data-stu-id="8992a-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="8992a-1085">Confronto di uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="8992a-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="8992a-1086">0x00000005 PRNE</span><span class="sxs-lookup"><span data-stu-id="8992a-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="8992a-1087">Confronto non uguale.</span><span class="sxs-lookup"><span data-stu-id="8992a-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="8992a-1088">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="8992a-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="8992a-1089">Confronto di espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="8992a-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="8992a-1090">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8992a-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="8992a-1091">Operatore AND bit per bit che restituisce l'operando destro.</span><span class="sxs-lookup"><span data-stu-id="8992a-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="8992a-1092">0x00000008 PRSomeBits</span><span class="sxs-lookup"><span data-stu-id="8992a-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="8992a-1093">Operatore AND bit per bit che restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8992a-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="8992a-1094">0x00000100 PRAll</span><span class="sxs-lookup"><span data-stu-id="8992a-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="8992a-1095">L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="8992a-1096">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="8992a-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="8992a-1097">L'operazione deve essere eseguita su una colonna di un set di righe e è true se l'operazione è true per qualsiasi riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="8992a-1098">**\_ pid**: Unsigned Integer a 32 bit, che rappresenta l'ID della proprietà (vedere propid nella sezione 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="8992a-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="8992a-1099">**\_ Prval**: CBaseStorageVariant che contiene il valore da correlare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="8992a-1100">**restrictionPresent**: valore di byte che indica se il campo nextRestriction è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="8992a-1101">DEVE essere impostato su 0x00 o 0x01.</span><span class="sxs-lookup"><span data-stu-id="8992a-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="8992a-1102">Se impostato su 0x01, restrictionPresent indica che è presente il campo nextRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="8992a-1103">Se impostato su 0x00, restrictionPresent indica che il campo nextRestriction non è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="8992a-1104">**nextRestriction**: struttura CRestriction, come specificato nella sezione 2.2.1.16, che specifica un'ulteriore restrizione.</span><span class="sxs-lookup"><span data-stu-id="8992a-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="8992a-1105">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="8992a-1106">La struttura CNatLanguageRestriction contiene una corrispondenza di **query in linguaggio naturale** per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="8992a-1107">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1107">0</span></span>

<span data-ttu-id="8992a-1108">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1108">1</span></span>

<span data-ttu-id="8992a-1109">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1109">2</span></span>

<span data-ttu-id="8992a-1110">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1110">3</span></span>

<span data-ttu-id="8992a-1111">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1111">4</span></span>

<span data-ttu-id="8992a-1112">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1112">5</span></span>

<span data-ttu-id="8992a-1113">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1113">6</span></span>

<span data-ttu-id="8992a-1114">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1114">7</span></span>

<span data-ttu-id="8992a-1115">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1115">8</span></span>

<span data-ttu-id="8992a-1116">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1116">9</span></span>

<span data-ttu-id="8992a-1117">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1117">1</span></span><br/> <span data-ttu-id="8992a-1118">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1118">0</span></span><br/>

<span data-ttu-id="8992a-1119">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1119">1</span></span>

<span data-ttu-id="8992a-1120">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1120">2</span></span>

<span data-ttu-id="8992a-1121">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1121">3</span></span>

<span data-ttu-id="8992a-1122">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1122">4</span></span>

<span data-ttu-id="8992a-1123">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1123">5</span></span>

<span data-ttu-id="8992a-1124">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1124">6</span></span>

<span data-ttu-id="8992a-1125">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1125">7</span></span>

<span data-ttu-id="8992a-1126">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1126">8</span></span>

<span data-ttu-id="8992a-1127">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1127">9</span></span>

<span data-ttu-id="8992a-1128">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1128">2</span></span><br/> <span data-ttu-id="8992a-1129">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1129">0</span></span><br/>

<span data-ttu-id="8992a-1130">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1130">1</span></span>

<span data-ttu-id="8992a-1131">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1131">2</span></span>

<span data-ttu-id="8992a-1132">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1132">3</span></span>

<span data-ttu-id="8992a-1133">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1133">4</span></span>

<span data-ttu-id="8992a-1134">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1134">5</span></span>

<span data-ttu-id="8992a-1135">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1135">6</span></span>

<span data-ttu-id="8992a-1136">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1136">7</span></span>

<span data-ttu-id="8992a-1137">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1137">8</span></span>

<span data-ttu-id="8992a-1138">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1138">9</span></span>

<span data-ttu-id="8992a-1139">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1139">3</span></span><br/> <span data-ttu-id="8992a-1140">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1140">0</span></span><br/>

<span data-ttu-id="8992a-1141">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1141">1</span></span>

<span data-ttu-id="8992a-1142">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1142">\_Property (variable)</span></span>

<span data-ttu-id="8992a-1143">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1143">...</span></span>

<span data-ttu-id="8992a-1144">\_riempimento di \_ CC (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="8992a-1145">Cc</span><span class="sxs-lookup"><span data-stu-id="8992a-1145">Cc</span></span>

<span data-ttu-id="8992a-1146">\_pwcsPhrase (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="8992a-1147">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1147">...</span></span>

<span data-ttu-id="8992a-1148">\_riempimento \_ LCID (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="8992a-1149">LCID</span><span class="sxs-lookup"><span data-stu-id="8992a-1149">Lcid</span></span>



 

<span data-ttu-id="8992a-1150">**\_ Property**: struttura CFullPropSpec, come specificato nella sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="8992a-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="8992a-1151">Questo campo indica la proprietà sulla quale eseguire l'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8992a-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="8992a-1152">**\_ riempimento \_ CC**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8992a-1153">La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura.</span><span class="sxs-lookup"><span data-stu-id="8992a-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8992a-1154">Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8992a-1155">Il contenuto di questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-1156">**CC**: A 32 bit unsigned integer.</span><span class="sxs-lookup"><span data-stu-id="8992a-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8992a-1157">Numero di caratteri nel \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="8992a-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="8992a-1158">**\_ pwcsPhrase**: stringa Unicode senza terminazione null che rappresenta la parola o la frase da confrontare per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="8992a-1159">NON deve essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="8992a-1159">MUST NOT be empty.</span></span> <span data-ttu-id="8992a-1160">Il campo CC contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="8992a-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="8992a-1161">**\_ riempimento \_ LCID**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8992a-1162">La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura.</span><span class="sxs-lookup"><span data-stu-id="8992a-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8992a-1163">Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8992a-1164">Il contenuto di questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-1165">**LCID**: Unsigned Integer a 32 bit che indica le impostazioni locali di \_ pwcsPhrase, come specificato in \[ MS-GPSI \] appendice a.</span><span class="sxs-lookup"><span data-stu-id="8992a-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="8992a-1166">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="8992a-1167">La struttura CNodeRestriction contiene una matrice di nodi della **struttura ad albero dei comandi** che specificano le restrizioni per la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="8992a-1168">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1168">0</span></span>

<span data-ttu-id="8992a-1169">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1169">1</span></span>

<span data-ttu-id="8992a-1170">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1170">2</span></span>

<span data-ttu-id="8992a-1171">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1171">3</span></span>

<span data-ttu-id="8992a-1172">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1172">4</span></span>

<span data-ttu-id="8992a-1173">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1173">5</span></span>

<span data-ttu-id="8992a-1174">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1174">6</span></span>

<span data-ttu-id="8992a-1175">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1175">7</span></span>

<span data-ttu-id="8992a-1176">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1176">8</span></span>

<span data-ttu-id="8992a-1177">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1177">9</span></span>

<span data-ttu-id="8992a-1178">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1178">1</span></span><br/> <span data-ttu-id="8992a-1179">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1179">0</span></span><br/>

<span data-ttu-id="8992a-1180">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1180">1</span></span>

<span data-ttu-id="8992a-1181">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1181">2</span></span>

<span data-ttu-id="8992a-1182">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1182">3</span></span>

<span data-ttu-id="8992a-1183">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1183">4</span></span>

<span data-ttu-id="8992a-1184">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1184">5</span></span>

<span data-ttu-id="8992a-1185">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1185">6</span></span>

<span data-ttu-id="8992a-1186">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1186">7</span></span>

<span data-ttu-id="8992a-1187">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1187">8</span></span>

<span data-ttu-id="8992a-1188">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1188">9</span></span>

<span data-ttu-id="8992a-1189">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1189">2</span></span><br/> <span data-ttu-id="8992a-1190">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1190">0</span></span><br/>

<span data-ttu-id="8992a-1191">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1191">1</span></span>

<span data-ttu-id="8992a-1192">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1192">2</span></span>

<span data-ttu-id="8992a-1193">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1193">3</span></span>

<span data-ttu-id="8992a-1194">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1194">4</span></span>

<span data-ttu-id="8992a-1195">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1195">5</span></span>

<span data-ttu-id="8992a-1196">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1196">6</span></span>

<span data-ttu-id="8992a-1197">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1197">7</span></span>

<span data-ttu-id="8992a-1198">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1198">8</span></span>

<span data-ttu-id="8992a-1199">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1199">9</span></span>

<span data-ttu-id="8992a-1200">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1200">3</span></span><br/> <span data-ttu-id="8992a-1201">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1201">0</span></span><br/>

<span data-ttu-id="8992a-1202">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1202">1</span></span>

<span data-ttu-id="8992a-1203">\_cNode</span><span class="sxs-lookup"><span data-stu-id="8992a-1203">\_cNode</span></span>

<span data-ttu-id="8992a-1204">\_paNode (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="8992a-1205">**\_ CNode**: un Unsigned Integer a 32 bit che specifica il numero di strutture CRestriction contenute nel \_ campo paNode.</span><span class="sxs-lookup"><span data-stu-id="8992a-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="8992a-1206">**\_ paNode**: matrice di strutture CRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="8992a-1207">Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura inizi in corrispondenza di un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la matrice.</span><span class="sxs-lookup"><span data-stu-id="8992a-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="8992a-1208">Se sono presenti byte di riempimento, il valore che contengono è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="8992a-1209">Il contenuto dei byte di riempimento deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="8992a-1210">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="8992a-1211">La struttura COccRestriction contiene la posizione di una parola in una frase.</span><span class="sxs-lookup"><span data-stu-id="8992a-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="8992a-1212">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1212">0</span></span>

<span data-ttu-id="8992a-1213">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1213">1</span></span>

<span data-ttu-id="8992a-1214">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1214">2</span></span>

<span data-ttu-id="8992a-1215">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1215">3</span></span>

<span data-ttu-id="8992a-1216">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1216">4</span></span>

<span data-ttu-id="8992a-1217">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1217">5</span></span>

<span data-ttu-id="8992a-1218">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1218">6</span></span>

<span data-ttu-id="8992a-1219">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1219">7</span></span>

<span data-ttu-id="8992a-1220">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1220">8</span></span>

<span data-ttu-id="8992a-1221">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1221">9</span></span>

<span data-ttu-id="8992a-1222">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1222">1</span></span><br/> <span data-ttu-id="8992a-1223">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1223">0</span></span><br/>

<span data-ttu-id="8992a-1224">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1224">1</span></span>

<span data-ttu-id="8992a-1225">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1225">2</span></span>

<span data-ttu-id="8992a-1226">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1226">3</span></span>

<span data-ttu-id="8992a-1227">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1227">4</span></span>

<span data-ttu-id="8992a-1228">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1228">5</span></span>

<span data-ttu-id="8992a-1229">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1229">6</span></span>

<span data-ttu-id="8992a-1230">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1230">7</span></span>

<span data-ttu-id="8992a-1231">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1231">8</span></span>

<span data-ttu-id="8992a-1232">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1232">9</span></span>

<span data-ttu-id="8992a-1233">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1233">2</span></span><br/> <span data-ttu-id="8992a-1234">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1234">0</span></span><br/>

<span data-ttu-id="8992a-1235">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1235">1</span></span>

<span data-ttu-id="8992a-1236">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1236">2</span></span>

<span data-ttu-id="8992a-1237">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1237">3</span></span>

<span data-ttu-id="8992a-1238">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1238">4</span></span>

<span data-ttu-id="8992a-1239">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1239">5</span></span>

<span data-ttu-id="8992a-1240">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1240">6</span></span>

<span data-ttu-id="8992a-1241">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1241">7</span></span>

<span data-ttu-id="8992a-1242">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1242">8</span></span>

<span data-ttu-id="8992a-1243">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1243">9</span></span>

<span data-ttu-id="8992a-1244">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1244">3</span></span><br/> <span data-ttu-id="8992a-1245">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1245">0</span></span><br/>

<span data-ttu-id="8992a-1246">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1246">1</span></span>

<span data-ttu-id="8992a-1247">\_ETag</span><span class="sxs-lookup"><span data-stu-id="8992a-1247">\_occ</span></span>

<span data-ttu-id="8992a-1248">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="8992a-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="8992a-1249">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="8992a-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="8992a-1250">**\_ OCC**: un Unsigned Integer a 32 bit che specifica l'offset della parola in una stringa di query, in unità di parole.</span><span class="sxs-lookup"><span data-stu-id="8992a-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="8992a-1251">Una parola, come usato in questa specifica, è un'unità di linguaggio in tutte le impostazioni locali che portano il significato.</span><span class="sxs-lookup"><span data-stu-id="8992a-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="8992a-1252">**\_ cPrevNoiseWords**: un Unsigned Integer a 32 bit contenente il numero di **parole non significative** che si verificano tra la parola e la parola precedente nella frase.</span><span class="sxs-lookup"><span data-stu-id="8992a-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="8992a-1253">**\_ cNextNoiseWords**: un Unsigned Integer a 32 bit contenente il numero di parole non significative che si verificano tra la parola e la parola successiva nella frase.</span><span class="sxs-lookup"><span data-stu-id="8992a-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="8992a-1254">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="8992a-1255">La struttura CPropertyRestriction contiene un valore della proprietà da confrontare con un'operazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="8992a-1256">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1256">0</span></span>

<span data-ttu-id="8992a-1257">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1257">1</span></span>

<span data-ttu-id="8992a-1258">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1258">2</span></span>

<span data-ttu-id="8992a-1259">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1259">3</span></span>

<span data-ttu-id="8992a-1260">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1260">4</span></span>

<span data-ttu-id="8992a-1261">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1261">5</span></span>

<span data-ttu-id="8992a-1262">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1262">6</span></span>

<span data-ttu-id="8992a-1263">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1263">7</span></span>

<span data-ttu-id="8992a-1264">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1264">8</span></span>

<span data-ttu-id="8992a-1265">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1265">9</span></span>

<span data-ttu-id="8992a-1266">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1266">1</span></span><br/> <span data-ttu-id="8992a-1267">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1267">0</span></span><br/>

<span data-ttu-id="8992a-1268">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1268">1</span></span>

<span data-ttu-id="8992a-1269">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1269">2</span></span>

<span data-ttu-id="8992a-1270">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1270">3</span></span>

<span data-ttu-id="8992a-1271">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1271">4</span></span>

<span data-ttu-id="8992a-1272">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1272">5</span></span>

<span data-ttu-id="8992a-1273">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1273">6</span></span>

<span data-ttu-id="8992a-1274">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1274">7</span></span>

<span data-ttu-id="8992a-1275">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1275">8</span></span>

<span data-ttu-id="8992a-1276">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1276">9</span></span>

<span data-ttu-id="8992a-1277">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1277">2</span></span><br/> <span data-ttu-id="8992a-1278">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1278">0</span></span><br/>

<span data-ttu-id="8992a-1279">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1279">1</span></span>

<span data-ttu-id="8992a-1280">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1280">2</span></span>

<span data-ttu-id="8992a-1281">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1281">3</span></span>

<span data-ttu-id="8992a-1282">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1282">4</span></span>

<span data-ttu-id="8992a-1283">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1283">5</span></span>

<span data-ttu-id="8992a-1284">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1284">6</span></span>

<span data-ttu-id="8992a-1285">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1285">7</span></span>

<span data-ttu-id="8992a-1286">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1286">8</span></span>

<span data-ttu-id="8992a-1287">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1287">9</span></span>

<span data-ttu-id="8992a-1288">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1288">3</span></span><br/> <span data-ttu-id="8992a-1289">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1289">0</span></span><br/>

<span data-ttu-id="8992a-1290">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1290">1</span></span>

<span data-ttu-id="8992a-1291">\_RelOp</span><span class="sxs-lookup"><span data-stu-id="8992a-1291">\_relop</span></span>

<span data-ttu-id="8992a-1292">\_Proprietà (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1292">\_Property (variable)</span></span>

<span data-ttu-id="8992a-1293">\_prval (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="8992a-1294">**\_ RelOp**: una Unsigned Integer a 32 bit che specifica la relazione da eseguire sulla proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="8992a-1295">DEVE essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="8992a-1296">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1296">Value</span></span>                 | <span data-ttu-id="8992a-1297">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1298">0x00000000 PRLT</span><span class="sxs-lookup"><span data-stu-id="8992a-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="8992a-1299">Confronto di minore di.</span><span class="sxs-lookup"><span data-stu-id="8992a-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="8992a-1300">0x00000001 PRLE</span><span class="sxs-lookup"><span data-stu-id="8992a-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="8992a-1301">Confronto di minore o uguale a.</span><span class="sxs-lookup"><span data-stu-id="8992a-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="8992a-1302">0x00000002 PRGT</span><span class="sxs-lookup"><span data-stu-id="8992a-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="8992a-1303">Confronto maggiore di.</span><span class="sxs-lookup"><span data-stu-id="8992a-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="8992a-1304">0x00000003 PRGE</span><span class="sxs-lookup"><span data-stu-id="8992a-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="8992a-1305">Confronto maggiore di o uguale a.</span><span class="sxs-lookup"><span data-stu-id="8992a-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="8992a-1306">0x00000004 PREQ</span><span class="sxs-lookup"><span data-stu-id="8992a-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="8992a-1307">Confronto di uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="8992a-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="8992a-1308">0x00000005 PRNE</span><span class="sxs-lookup"><span data-stu-id="8992a-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="8992a-1309">Confronto non uguale.</span><span class="sxs-lookup"><span data-stu-id="8992a-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="8992a-1310">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="8992a-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="8992a-1311">Confronto di espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="8992a-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="8992a-1312">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8992a-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="8992a-1313">Operatore AND bit per bit che restituisce l'operando destro.</span><span class="sxs-lookup"><span data-stu-id="8992a-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="8992a-1314">0x00000008 PRSomeBits</span><span class="sxs-lookup"><span data-stu-id="8992a-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="8992a-1315">Operatore AND bit per bit che restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8992a-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="8992a-1316">0x00000100 PRAll</span><span class="sxs-lookup"><span data-stu-id="8992a-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="8992a-1317">L'operazione deve essere eseguita su una colonna di un set di righe ed è true solo se l'operazione è true per tutte le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="8992a-1318">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="8992a-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="8992a-1319">L'operazione deve essere eseguita su una colonna di un set di righe e è true se l'operazione è true per qualsiasi riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="8992a-1320">**\_ Property**: una struttura CFullPropSpec, come specificato nella sezione 2.2.1.2, che indica la proprietà su cui eseguire un'operazione di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8992a-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="8992a-1321">**\_ prval**: struttura CBaseStorageVariant, come specificato nella sezione 2.2.1.1, che contiene il valore da correlare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="8992a-1322">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="8992a-1323">La struttura CRangeRestriction contiene una restrizione su un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="8992a-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="8992a-1324">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1324">0</span></span>

<span data-ttu-id="8992a-1325">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1325">1</span></span>

<span data-ttu-id="8992a-1326">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1326">2</span></span>

<span data-ttu-id="8992a-1327">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1327">3</span></span>

<span data-ttu-id="8992a-1328">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1328">4</span></span>

<span data-ttu-id="8992a-1329">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1329">5</span></span>

<span data-ttu-id="8992a-1330">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1330">6</span></span>

<span data-ttu-id="8992a-1331">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1331">7</span></span>

<span data-ttu-id="8992a-1332">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1332">8</span></span>

<span data-ttu-id="8992a-1333">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1333">9</span></span>

<span data-ttu-id="8992a-1334">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1334">1</span></span><br/> <span data-ttu-id="8992a-1335">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1335">0</span></span><br/>

<span data-ttu-id="8992a-1336">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1336">1</span></span>

<span data-ttu-id="8992a-1337">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1337">2</span></span>

<span data-ttu-id="8992a-1338">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1338">3</span></span>

<span data-ttu-id="8992a-1339">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1339">4</span></span>

<span data-ttu-id="8992a-1340">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1340">5</span></span>

<span data-ttu-id="8992a-1341">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1341">6</span></span>

<span data-ttu-id="8992a-1342">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1342">7</span></span>

<span data-ttu-id="8992a-1343">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1343">8</span></span>

<span data-ttu-id="8992a-1344">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1344">9</span></span>

<span data-ttu-id="8992a-1345">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1345">2</span></span><br/> <span data-ttu-id="8992a-1346">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1346">0</span></span><br/>

<span data-ttu-id="8992a-1347">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1347">1</span></span>

<span data-ttu-id="8992a-1348">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1348">2</span></span>

<span data-ttu-id="8992a-1349">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1349">3</span></span>

<span data-ttu-id="8992a-1350">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1350">4</span></span>

<span data-ttu-id="8992a-1351">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1351">5</span></span>

<span data-ttu-id="8992a-1352">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1352">6</span></span>

<span data-ttu-id="8992a-1353">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1353">7</span></span>

<span data-ttu-id="8992a-1354">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1354">8</span></span>

<span data-ttu-id="8992a-1355">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1355">9</span></span>

<span data-ttu-id="8992a-1356">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1356">3</span></span><br/> <span data-ttu-id="8992a-1357">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1357">0</span></span><br/>

<span data-ttu-id="8992a-1358">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1358">1</span></span>

<span data-ttu-id="8992a-1359">\_Avvio della pagina (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="8992a-1360">\_keyEnd (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="8992a-1361">**\_ Start di avvio**: una struttura CKey, come specificato nella sezione 2.2.1.4, che contiene l'inizio dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="8992a-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="8992a-1362">**\_ keyEnd**: struttura CKey che contiene la fine dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="8992a-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="8992a-1363">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="8992a-1364">La struttura CScopeRestriction contiene una restrizione sui file da cercare</span><span class="sxs-lookup"><span data-stu-id="8992a-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="8992a-1365">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1365">0</span></span>

<span data-ttu-id="8992a-1366">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1366">1</span></span>

<span data-ttu-id="8992a-1367">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1367">2</span></span>

<span data-ttu-id="8992a-1368">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1368">3</span></span>

<span data-ttu-id="8992a-1369">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1369">4</span></span>

<span data-ttu-id="8992a-1370">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1370">5</span></span>

<span data-ttu-id="8992a-1371">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1371">6</span></span>

<span data-ttu-id="8992a-1372">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1372">7</span></span>

<span data-ttu-id="8992a-1373">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1373">8</span></span>

<span data-ttu-id="8992a-1374">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1374">9</span></span>

<span data-ttu-id="8992a-1375">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1375">1</span></span><br/> <span data-ttu-id="8992a-1376">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1376">0</span></span><br/>

<span data-ttu-id="8992a-1377">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1377">1</span></span>

<span data-ttu-id="8992a-1378">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1378">2</span></span>

<span data-ttu-id="8992a-1379">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1379">3</span></span>

<span data-ttu-id="8992a-1380">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1380">4</span></span>

<span data-ttu-id="8992a-1381">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1381">5</span></span>

<span data-ttu-id="8992a-1382">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1382">6</span></span>

<span data-ttu-id="8992a-1383">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1383">7</span></span>

<span data-ttu-id="8992a-1384">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1384">8</span></span>

<span data-ttu-id="8992a-1385">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1385">9</span></span>

<span data-ttu-id="8992a-1386">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1386">2</span></span><br/> <span data-ttu-id="8992a-1387">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1387">0</span></span><br/>

<span data-ttu-id="8992a-1388">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1388">1</span></span>

<span data-ttu-id="8992a-1389">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1389">2</span></span>

<span data-ttu-id="8992a-1390">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1390">3</span></span>

<span data-ttu-id="8992a-1391">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1391">4</span></span>

<span data-ttu-id="8992a-1392">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1392">5</span></span>

<span data-ttu-id="8992a-1393">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1393">6</span></span>

<span data-ttu-id="8992a-1394">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1394">7</span></span>

<span data-ttu-id="8992a-1395">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1395">8</span></span>

<span data-ttu-id="8992a-1396">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1396">9</span></span>

<span data-ttu-id="8992a-1397">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1397">3</span></span><br/> <span data-ttu-id="8992a-1398">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1398">0</span></span><br/>

<span data-ttu-id="8992a-1399">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1399">1</span></span>

<span data-ttu-id="8992a-1400">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="8992a-1400">CcLowerPath</span></span>

<span data-ttu-id="8992a-1401">\_lowerPath (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="8992a-1402">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1402">...</span></span>

<span data-ttu-id="8992a-1403">\_spaziatura interna (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1403">\_padding ( variable)</span></span>

<span data-ttu-id="8992a-1404">\_lunghezza</span><span class="sxs-lookup"><span data-stu-id="8992a-1404">\_length</span></span>

<span data-ttu-id="8992a-1405">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="8992a-1405">\_fRecursive</span></span>

<span data-ttu-id="8992a-1406">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="8992a-1406">\_fVirtual</span></span>



 

<span data-ttu-id="8992a-1407">**CcLowerPath**: Unsigned Integer a 32 bit contenente il numero di caratteri Unicode nel \_ campo lowerPath.</span><span class="sxs-lookup"><span data-stu-id="8992a-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="8992a-1408">**\_ lowerPath**: stringa Unicode senza terminazione null che rappresenta il **percorso** in cui la query deve essere limitata.</span><span class="sxs-lookup"><span data-stu-id="8992a-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="8992a-1409">Il campo CcLowerPath contiene la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="8992a-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="8992a-1410">**\_ spaziatura interna**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8992a-1411">La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura.</span><span class="sxs-lookup"><span data-stu-id="8992a-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8992a-1412">Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8992a-1413">Il contenuto di questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-1414">**\_ length**: Unsigned Integer a 32 bit contenente la lunghezza di \_ LowerPath, in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="8992a-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="8992a-1415">DEVE corrispondere al valore di CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="8992a-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="8992a-1416">**\_ fRecursive**: Unsigned Integer A 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8992a-1417">DEVE essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="8992a-1418">Se impostato su 0x00000001, il server deve esaminare in modo ricorsivo tutte le sottodirectory del percorso.</span><span class="sxs-lookup"><span data-stu-id="8992a-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="8992a-1419">Se impostato su 0x00000000, il server non deve esaminare le sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="8992a-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="8992a-1420">**\_ fVirtual**: Unsigned Integer A 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8992a-1421">DEVE essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="8992a-1422">Se è impostato su 0x00000001, \_ lowerPath è un percorso virtuale, ovvero il Uniform Resource Locator (URL) associato a una directory fisica nel file System) per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="8992a-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="8992a-1423">Se impostato su 0x00000000, \_ lowerPath è un percorso file System.</span><span class="sxs-lookup"><span data-stu-id="8992a-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="8992a-1424">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="8992a-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="8992a-1425">La struttura CSort identifica una colonna da ordinare.</span><span class="sxs-lookup"><span data-stu-id="8992a-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="8992a-1426">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1426">0</span></span>

<span data-ttu-id="8992a-1427">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1427">1</span></span>

<span data-ttu-id="8992a-1428">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1428">2</span></span>

<span data-ttu-id="8992a-1429">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1429">3</span></span>

<span data-ttu-id="8992a-1430">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1430">4</span></span>

<span data-ttu-id="8992a-1431">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1431">5</span></span>

<span data-ttu-id="8992a-1432">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1432">6</span></span>

<span data-ttu-id="8992a-1433">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1433">7</span></span>

<span data-ttu-id="8992a-1434">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1434">8</span></span>

<span data-ttu-id="8992a-1435">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1435">9</span></span>

<span data-ttu-id="8992a-1436">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1436">1</span></span><br/> <span data-ttu-id="8992a-1437">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1437">0</span></span><br/>

<span data-ttu-id="8992a-1438">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1438">1</span></span>

<span data-ttu-id="8992a-1439">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1439">2</span></span>

<span data-ttu-id="8992a-1440">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1440">3</span></span>

<span data-ttu-id="8992a-1441">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1441">4</span></span>

<span data-ttu-id="8992a-1442">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1442">5</span></span>

<span data-ttu-id="8992a-1443">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1443">6</span></span>

<span data-ttu-id="8992a-1444">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1444">7</span></span>

<span data-ttu-id="8992a-1445">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1445">8</span></span>

<span data-ttu-id="8992a-1446">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1446">9</span></span>

<span data-ttu-id="8992a-1447">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1447">2</span></span><br/> <span data-ttu-id="8992a-1448">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1448">0</span></span><br/>

<span data-ttu-id="8992a-1449">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1449">1</span></span>

<span data-ttu-id="8992a-1450">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1450">2</span></span>

<span data-ttu-id="8992a-1451">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1451">3</span></span>

<span data-ttu-id="8992a-1452">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1452">4</span></span>

<span data-ttu-id="8992a-1453">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1453">5</span></span>

<span data-ttu-id="8992a-1454">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1454">6</span></span>

<span data-ttu-id="8992a-1455">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1455">7</span></span>

<span data-ttu-id="8992a-1456">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1456">8</span></span>

<span data-ttu-id="8992a-1457">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1457">9</span></span>

<span data-ttu-id="8992a-1458">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1458">3</span></span><br/> <span data-ttu-id="8992a-1459">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1459">0</span></span><br/>

<span data-ttu-id="8992a-1460">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1460">1</span></span>

<span data-ttu-id="8992a-1461">pidColumn</span><span class="sxs-lookup"><span data-stu-id="8992a-1461">pidColumn</span></span>

<span data-ttu-id="8992a-1462">dwOrder</span><span class="sxs-lookup"><span data-stu-id="8992a-1462">dwOrder</span></span>

<span data-ttu-id="8992a-1463">locale</span><span class="sxs-lookup"><span data-stu-id="8992a-1463">locale</span></span>



 

<span data-ttu-id="8992a-1464">**pidColumn**: Unsigned Integer A 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8992a-1465">Numero della colonna in base alla quale eseguire l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="8992a-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="8992a-1466">**dworder**: Unsigned Integer A 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8992a-1467">DEVE essere uno dei valori seguenti, che specifica la modalità di ordinamento in base alla colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="8992a-1468">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1468">Value</span></span>                        | <span data-ttu-id="8992a-1469">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1470">QUERY \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="8992a-1471">Le righe devono essere ordinate in ordine crescente in base ai valori nella colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="8992a-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="8992a-1472">QUERY \_ discendente 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="8992a-1473">Le righe devono essere ordinate in ordine decrescente in base ai valori nella colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="8992a-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="8992a-1474">**impostazioni locali**: un Unsigned Integer a 32 bit che indica le impostazioni locali, come specificato nell' \[ appendice MS-GPSI \] , della colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="8992a-1475">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="8992a-1476">La struttura CSynRestriction contiene una parola o i relativi sinonimi per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="8992a-1477">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1477">0</span></span>

<span data-ttu-id="8992a-1478">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1478">1</span></span>

<span data-ttu-id="8992a-1479">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1479">2</span></span>

<span data-ttu-id="8992a-1480">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1480">3</span></span>

<span data-ttu-id="8992a-1481">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1481">4</span></span>

<span data-ttu-id="8992a-1482">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1482">5</span></span>

<span data-ttu-id="8992a-1483">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1483">6</span></span>

<span data-ttu-id="8992a-1484">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1484">7</span></span>

<span data-ttu-id="8992a-1485">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1485">8</span></span>

<span data-ttu-id="8992a-1486">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1486">9</span></span>

<span data-ttu-id="8992a-1487">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1487">1</span></span><br/> <span data-ttu-id="8992a-1488">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1488">0</span></span><br/>

<span data-ttu-id="8992a-1489">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1489">1</span></span>

<span data-ttu-id="8992a-1490">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1490">2</span></span>

<span data-ttu-id="8992a-1491">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1491">3</span></span>

<span data-ttu-id="8992a-1492">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1492">4</span></span>

<span data-ttu-id="8992a-1493">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1493">5</span></span>

<span data-ttu-id="8992a-1494">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1494">6</span></span>

<span data-ttu-id="8992a-1495">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1495">7</span></span>

<span data-ttu-id="8992a-1496">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1496">8</span></span>

<span data-ttu-id="8992a-1497">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1497">9</span></span>

<span data-ttu-id="8992a-1498">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1498">2</span></span><br/> <span data-ttu-id="8992a-1499">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1499">0</span></span><br/>

<span data-ttu-id="8992a-1500">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1500">1</span></span>

<span data-ttu-id="8992a-1501">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1501">2</span></span>

<span data-ttu-id="8992a-1502">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1502">3</span></span>

<span data-ttu-id="8992a-1503">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1503">4</span></span>

<span data-ttu-id="8992a-1504">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1504">5</span></span>

<span data-ttu-id="8992a-1505">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1505">6</span></span>

<span data-ttu-id="8992a-1506">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1506">7</span></span>

<span data-ttu-id="8992a-1507">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1507">8</span></span>

<span data-ttu-id="8992a-1508">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1508">9</span></span>

<span data-ttu-id="8992a-1509">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1509">3</span></span><br/> <span data-ttu-id="8992a-1510">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1510">0</span></span><br/>

<span data-ttu-id="8992a-1511">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1511">1</span></span>

<span data-ttu-id="8992a-1512">Restrizione</span><span class="sxs-lookup"><span data-stu-id="8992a-1512">Restriction</span></span>

<span data-ttu-id="8992a-1513">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1513">...</span></span>

<span data-ttu-id="8992a-1514">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1514">...</span></span>

<span data-ttu-id="8992a-1515">cKey</span><span class="sxs-lookup"><span data-stu-id="8992a-1515">cKey</span></span>

<span data-ttu-id="8992a-1516">\_Matrice di matrici (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="8992a-1517">\_isRange</span><span class="sxs-lookup"><span data-stu-id="8992a-1517">\_isRange</span></span>



 

<span data-ttu-id="8992a-1518">**Restrizione**: struttura COccRestriction che specifica la posizione della parola.</span><span class="sxs-lookup"><span data-stu-id="8992a-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="8992a-1519">**CKEY**: un Unsigned Integer a 32 bit che specifica il numero di elementi nella \_ matrice di matrici di matrici.</span><span class="sxs-lookup"><span data-stu-id="8992a-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="8992a-1520">**\_ dataArray**: matrice di strutture CKey che specifica una parola e i relativi sinonimi.</span><span class="sxs-lookup"><span data-stu-id="8992a-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="8992a-1521">IsMatch **\_ : se** è impostato su 0x01, le chiavi sono prefissi per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8992a-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="8992a-1522">Se impostato su 0x00, le chiavi corrispondono ai valori esatti corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="8992a-1523">\_l'intervallo di valori non deve essere impostato su nessun altro valore.</span><span class="sxs-lookup"><span data-stu-id="8992a-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="8992a-1524">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="8992a-1525">La struttura CVectorRestriction contiene un'operazione ponderata o su un nodo della struttura ad albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="8992a-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="8992a-1526">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1526">0</span></span>

<span data-ttu-id="8992a-1527">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1527">1</span></span>

<span data-ttu-id="8992a-1528">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1528">2</span></span>

<span data-ttu-id="8992a-1529">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1529">3</span></span>

<span data-ttu-id="8992a-1530">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1530">4</span></span>

<span data-ttu-id="8992a-1531">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1531">5</span></span>

<span data-ttu-id="8992a-1532">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1532">6</span></span>

<span data-ttu-id="8992a-1533">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1533">7</span></span>

<span data-ttu-id="8992a-1534">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1534">8</span></span>

<span data-ttu-id="8992a-1535">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1535">9</span></span>

<span data-ttu-id="8992a-1536">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1536">1</span></span><br/> <span data-ttu-id="8992a-1537">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1537">0</span></span><br/>

<span data-ttu-id="8992a-1538">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1538">1</span></span>

<span data-ttu-id="8992a-1539">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1539">2</span></span>

<span data-ttu-id="8992a-1540">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1540">3</span></span>

<span data-ttu-id="8992a-1541">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1541">4</span></span>

<span data-ttu-id="8992a-1542">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1542">5</span></span>

<span data-ttu-id="8992a-1543">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1543">6</span></span>

<span data-ttu-id="8992a-1544">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1544">7</span></span>

<span data-ttu-id="8992a-1545">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1545">8</span></span>

<span data-ttu-id="8992a-1546">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1546">9</span></span>

<span data-ttu-id="8992a-1547">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1547">2</span></span><br/> <span data-ttu-id="8992a-1548">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1548">0</span></span><br/>

<span data-ttu-id="8992a-1549">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1549">1</span></span>

<span data-ttu-id="8992a-1550">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1550">2</span></span>

<span data-ttu-id="8992a-1551">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1551">3</span></span>

<span data-ttu-id="8992a-1552">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1552">4</span></span>

<span data-ttu-id="8992a-1553">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1553">5</span></span>

<span data-ttu-id="8992a-1554">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1554">6</span></span>

<span data-ttu-id="8992a-1555">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1555">7</span></span>

<span data-ttu-id="8992a-1556">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1556">8</span></span>

<span data-ttu-id="8992a-1557">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1557">9</span></span>

<span data-ttu-id="8992a-1558">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1558">3</span></span><br/> <span data-ttu-id="8992a-1559">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1559">0</span></span><br/>

<span data-ttu-id="8992a-1560">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1560">1</span></span>

<span data-ttu-id="8992a-1561">\_Pres (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1561">\_pres (variable)</span></span>

<span data-ttu-id="8992a-1562">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1562">...</span></span>

<span data-ttu-id="8992a-1563">\_spaziatura interna (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1563">\_padding (variable)</span></span>

<span data-ttu-id="8992a-1564">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="8992a-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="8992a-1565">**\_ pres**: albero dei comandi CNodeRestriction su cui deve essere eseguita un'operazione di classificazione o.</span><span class="sxs-lookup"><span data-stu-id="8992a-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="8992a-1566">**\_ spaziatura interna**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8992a-1567">La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura.</span><span class="sxs-lookup"><span data-stu-id="8992a-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8992a-1568">Se questo campo è presente, ad esempio length diverso da zero, il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8992a-1569">Il contenuto di questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-1570">**\_ ulRankMethod**: un Unsigned Integer a 32 bit che specifica un algoritmo di classificazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="8992a-1571">DEVE essere impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="8992a-1572">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1572">Value</span></span>                            | <span data-ttu-id="8992a-1573">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="8992a-1574">\_Dimensioni \_ minime vettore 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="8992a-1575">Usare l'algoritmo minimo \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="8992a-1576">\_ \_ Numero massimo di 0x00000001 di rango vettoriale</span><span class="sxs-lookup"><span data-stu-id="8992a-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="8992a-1577">Usare l'algoritmo Max \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="8992a-1578">\_ \_ 0x00000002 Inner Rank vettore</span><span class="sxs-lookup"><span data-stu-id="8992a-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="8992a-1579">Usare l'algoritmo prodotto interno \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="8992a-1580">VECTOR \_ Rank \_ dadi 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8992a-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="8992a-1581">Usare l'algoritmo del coefficiente dadi \[ \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="8992a-1582">VECTOR \_ Rank \_ JACCARD 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8992a-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="8992a-1583">Usare l'algoritmo coefficiente Jaccard di \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="8992a-1584">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="8992a-1585">La struttura CWordRestriction contiene una parola per una frase di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="8992a-1586">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1586">0</span></span>

<span data-ttu-id="8992a-1587">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1587">1</span></span>

<span data-ttu-id="8992a-1588">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1588">2</span></span>

<span data-ttu-id="8992a-1589">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1589">3</span></span>

<span data-ttu-id="8992a-1590">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1590">4</span></span>

<span data-ttu-id="8992a-1591">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1591">5</span></span>

<span data-ttu-id="8992a-1592">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1592">6</span></span>

<span data-ttu-id="8992a-1593">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1593">7</span></span>

<span data-ttu-id="8992a-1594">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1594">8</span></span>

<span data-ttu-id="8992a-1595">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1595">9</span></span>

<span data-ttu-id="8992a-1596">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1596">1</span></span><br/> <span data-ttu-id="8992a-1597">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1597">0</span></span><br/>

<span data-ttu-id="8992a-1598">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1598">1</span></span>

<span data-ttu-id="8992a-1599">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1599">2</span></span>

<span data-ttu-id="8992a-1600">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1600">3</span></span>

<span data-ttu-id="8992a-1601">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1601">4</span></span>

<span data-ttu-id="8992a-1602">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1602">5</span></span>

<span data-ttu-id="8992a-1603">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1603">6</span></span>

<span data-ttu-id="8992a-1604">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1604">7</span></span>

<span data-ttu-id="8992a-1605">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1605">8</span></span>

<span data-ttu-id="8992a-1606">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1606">9</span></span>

<span data-ttu-id="8992a-1607">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1607">2</span></span><br/> <span data-ttu-id="8992a-1608">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1608">0</span></span><br/>

<span data-ttu-id="8992a-1609">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1609">1</span></span>

<span data-ttu-id="8992a-1610">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1610">2</span></span>

<span data-ttu-id="8992a-1611">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1611">3</span></span>

<span data-ttu-id="8992a-1612">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1612">4</span></span>

<span data-ttu-id="8992a-1613">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1613">5</span></span>

<span data-ttu-id="8992a-1614">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1614">6</span></span>

<span data-ttu-id="8992a-1615">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1615">7</span></span>

<span data-ttu-id="8992a-1616">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1616">8</span></span>

<span data-ttu-id="8992a-1617">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1617">9</span></span>

<span data-ttu-id="8992a-1618">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1618">3</span></span><br/> <span data-ttu-id="8992a-1619">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1619">0</span></span><br/>

<span data-ttu-id="8992a-1620">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1620">1</span></span>

<span data-ttu-id="8992a-1621">restrizione</span><span class="sxs-lookup"><span data-stu-id="8992a-1621">restriction</span></span>

<span data-ttu-id="8992a-1622">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1622">...</span></span>

<span data-ttu-id="8992a-1623">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1623">...</span></span>

<span data-ttu-id="8992a-1624">\_chiave (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1624">\_key (variable)</span></span>

<span data-ttu-id="8992a-1625">\_isRange</span><span class="sxs-lookup"><span data-stu-id="8992a-1625">\_isRange</span></span>



 

<span data-ttu-id="8992a-1626">**restrizione**: struttura COccRestriction che specifica la posizione della parola.</span><span class="sxs-lookup"><span data-stu-id="8992a-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="8992a-1627">**\_ Key**: struttura CKey che specifica una parola.</span><span class="sxs-lookup"><span data-stu-id="8992a-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="8992a-1628">IsMatch **\_ : se** è impostato su 0x01, la chiave corrisponde a un prefisso.</span><span class="sxs-lookup"><span data-stu-id="8992a-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="8992a-1629">Se impostato su 0x00, la chiave è un valore esatto per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="8992a-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="8992a-1630">\_l'intervallo di valori non deve essere impostato su un altro valore.</span><span class="sxs-lookup"><span data-stu-id="8992a-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="8992a-1631">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="8992a-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="8992a-1632">La struttura CRestriction contiene un nodo di un albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="8992a-1633">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1633">0</span></span>

<span data-ttu-id="8992a-1634">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1634">1</span></span>

<span data-ttu-id="8992a-1635">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1635">2</span></span>

<span data-ttu-id="8992a-1636">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1636">3</span></span>

<span data-ttu-id="8992a-1637">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1637">4</span></span>

<span data-ttu-id="8992a-1638">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1638">5</span></span>

<span data-ttu-id="8992a-1639">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1639">6</span></span>

<span data-ttu-id="8992a-1640">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1640">7</span></span>

<span data-ttu-id="8992a-1641">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1641">8</span></span>

<span data-ttu-id="8992a-1642">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1642">9</span></span>

<span data-ttu-id="8992a-1643">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1643">1</span></span><br/> <span data-ttu-id="8992a-1644">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1644">0</span></span><br/>

<span data-ttu-id="8992a-1645">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1645">1</span></span>

<span data-ttu-id="8992a-1646">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1646">2</span></span>

<span data-ttu-id="8992a-1647">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1647">3</span></span>

<span data-ttu-id="8992a-1648">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1648">4</span></span>

<span data-ttu-id="8992a-1649">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1649">5</span></span>

<span data-ttu-id="8992a-1650">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1650">6</span></span>

<span data-ttu-id="8992a-1651">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1651">7</span></span>

<span data-ttu-id="8992a-1652">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1652">8</span></span>

<span data-ttu-id="8992a-1653">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1653">9</span></span>

<span data-ttu-id="8992a-1654">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1654">2</span></span><br/> <span data-ttu-id="8992a-1655">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1655">0</span></span><br/>

<span data-ttu-id="8992a-1656">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1656">1</span></span>

<span data-ttu-id="8992a-1657">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1657">2</span></span>

<span data-ttu-id="8992a-1658">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1658">3</span></span>

<span data-ttu-id="8992a-1659">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1659">4</span></span>

<span data-ttu-id="8992a-1660">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1660">5</span></span>

<span data-ttu-id="8992a-1661">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1661">6</span></span>

<span data-ttu-id="8992a-1662">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1662">7</span></span>

<span data-ttu-id="8992a-1663">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1663">8</span></span>

<span data-ttu-id="8992a-1664">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1664">9</span></span>

<span data-ttu-id="8992a-1665">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1665">3</span></span><br/> <span data-ttu-id="8992a-1666">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1666">0</span></span><br/>

<span data-ttu-id="8992a-1667">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1667">1</span></span>

<span data-ttu-id="8992a-1668">\_ulType</span><span class="sxs-lookup"><span data-stu-id="8992a-1668">\_ulType</span></span>

<span data-ttu-id="8992a-1669">Peso</span><span class="sxs-lookup"><span data-stu-id="8992a-1669">Weight</span></span>

<span data-ttu-id="8992a-1670">Restrizione</span><span class="sxs-lookup"><span data-stu-id="8992a-1670">Restriction</span></span>



 

<span data-ttu-id="8992a-1671">**\_ ulType**: Unsigned Integer a 32 bit che indica il tipo di restrizione utilizzato per il nodo della struttura ad albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="8992a-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="8992a-1672">DEVE essere impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="8992a-1673">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1673">Value</span></span>                    | <span data-ttu-id="8992a-1674">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1675">0x00000000 RTNone</span><span class="sxs-lookup"><span data-stu-id="8992a-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="8992a-1676">Il nodo rappresenta una parola non significativa in una query vettoriale.</span><span class="sxs-lookup"><span data-stu-id="8992a-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="8992a-1677">0x00000001 RTAnd</span><span class="sxs-lookup"><span data-stu-id="8992a-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="8992a-1678">Il nodo contiene un CNodeRestriction su cui eseguire un'operazione AND logica.</span><span class="sxs-lookup"><span data-stu-id="8992a-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="8992a-1679">0x00000002 RTOr</span><span class="sxs-lookup"><span data-stu-id="8992a-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="8992a-1680">Il nodo contiene un CNodeRestriction su cui deve essere eseguita un'operazione OR logica.</span><span class="sxs-lookup"><span data-stu-id="8992a-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="8992a-1681">0x00000003 RTNot</span><span class="sxs-lookup"><span data-stu-id="8992a-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="8992a-1682">Il nodo contiene un CRestriction su cui deve essere eseguita un'operazione NOT.</span><span class="sxs-lookup"><span data-stu-id="8992a-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="8992a-1683">0x00000004 RTContent</span><span class="sxs-lookup"><span data-stu-id="8992a-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="8992a-1684">Il nodo contiene un CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="8992a-1685">0x00000005 RTProperty</span><span class="sxs-lookup"><span data-stu-id="8992a-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="8992a-1686">Il nodo contiene un CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="8992a-1687">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="8992a-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="8992a-1688">Il nodo contiene un CNodeRestriction su cui deve essere eseguita una classificazione di prossimità.</span><span class="sxs-lookup"><span data-stu-id="8992a-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="8992a-1689">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8992a-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="8992a-1690">Il nodo contiene un CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="8992a-1691">0x00000008 RTNatLanguage</span><span class="sxs-lookup"><span data-stu-id="8992a-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="8992a-1692">Il nodo contiene un CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="8992a-1693">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="8992a-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="8992a-1694">Il nodo contiene un CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="8992a-1695">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="8992a-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="8992a-1696">Il nodo contiene un CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="8992a-1697">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="8992a-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="8992a-1698">Il nodo contiene un CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="8992a-1699">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="8992a-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="8992a-1700">Il nodo contiene un CNodeRestriction su cui deve essere eseguita una frase corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8992a-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="8992a-1701">0xFFFFFFFE RTSynonym</span><span class="sxs-lookup"><span data-stu-id="8992a-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="8992a-1702">Il nodo contiene un CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="8992a-1703">RTWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="8992a-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="8992a-1704">Il nodo contiene un CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="8992a-1705">**Weight**: Unsigned Integer A 32 bit che rappresenta il peso del nodo.</span><span class="sxs-lookup"><span data-stu-id="8992a-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="8992a-1706">Weight indica l'importanza del nodo rispetto ad altri nodi nell'albero dei comandi di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="8992a-1707">I valori di peso più elevati sono più importanti.</span><span class="sxs-lookup"><span data-stu-id="8992a-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="8992a-1708">**Restrizione**: tipo di restrizione per il nodo della struttura ad albero dei comandi.</span><span class="sxs-lookup"><span data-stu-id="8992a-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="8992a-1709">La sintassi deve essere indicata dal \_ campo ulType.</span><span class="sxs-lookup"><span data-stu-id="8992a-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="8992a-1710">CColumnSet 2.2.1.17</span><span class="sxs-lookup"><span data-stu-id="8992a-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="8992a-1711">La struttura CColumnSet specifica i numeri di colonna da restituire.</span><span class="sxs-lookup"><span data-stu-id="8992a-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="8992a-1712">Questa struttura viene sempre utilizzata in riferimento a una struttura CPidMapper specifica (Section 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="8992a-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="8992a-1713">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1713">0</span></span>

<span data-ttu-id="8992a-1714">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1714">1</span></span>

<span data-ttu-id="8992a-1715">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1715">2</span></span>

<span data-ttu-id="8992a-1716">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1716">3</span></span>

<span data-ttu-id="8992a-1717">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1717">4</span></span>

<span data-ttu-id="8992a-1718">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1718">5</span></span>

<span data-ttu-id="8992a-1719">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1719">6</span></span>

<span data-ttu-id="8992a-1720">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1720">7</span></span>

<span data-ttu-id="8992a-1721">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1721">8</span></span>

<span data-ttu-id="8992a-1722">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1722">9</span></span>

<span data-ttu-id="8992a-1723">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1723">1</span></span><br/> <span data-ttu-id="8992a-1724">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1724">0</span></span><br/>

<span data-ttu-id="8992a-1725">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1725">1</span></span>

<span data-ttu-id="8992a-1726">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1726">2</span></span>

<span data-ttu-id="8992a-1727">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1727">3</span></span>

<span data-ttu-id="8992a-1728">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1728">4</span></span>

<span data-ttu-id="8992a-1729">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1729">5</span></span>

<span data-ttu-id="8992a-1730">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1730">6</span></span>

<span data-ttu-id="8992a-1731">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1731">7</span></span>

<span data-ttu-id="8992a-1732">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1732">8</span></span>

<span data-ttu-id="8992a-1733">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1733">9</span></span>

<span data-ttu-id="8992a-1734">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1734">2</span></span><br/> <span data-ttu-id="8992a-1735">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1735">0</span></span><br/>

<span data-ttu-id="8992a-1736">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1736">1</span></span>

<span data-ttu-id="8992a-1737">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1737">2</span></span>

<span data-ttu-id="8992a-1738">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1738">3</span></span>

<span data-ttu-id="8992a-1739">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1739">4</span></span>

<span data-ttu-id="8992a-1740">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1740">5</span></span>

<span data-ttu-id="8992a-1741">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1741">6</span></span>

<span data-ttu-id="8992a-1742">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1742">7</span></span>

<span data-ttu-id="8992a-1743">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1743">8</span></span>

<span data-ttu-id="8992a-1744">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1744">9</span></span>

<span data-ttu-id="8992a-1745">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1745">3</span></span><br/> <span data-ttu-id="8992a-1746">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1746">0</span></span><br/>

<span data-ttu-id="8992a-1747">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1747">1</span></span>

<span data-ttu-id="8992a-1748">count</span><span class="sxs-lookup"><span data-stu-id="8992a-1748">count</span></span>

<span data-ttu-id="8992a-1749">indici (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1749">indexes (variable)</span></span>



 

<span data-ttu-id="8992a-1750">**count**: un Unsigned Integer a 32 bit che specifica il numero di elementi nella matrice di indici.</span><span class="sxs-lookup"><span data-stu-id="8992a-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="8992a-1751">**indici**: matrice di interi senza segno a 4 byte che rappresenta gli indici in base zero nella matrice aPropSpec nella struttura CPidMapper corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8992a-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="8992a-1752">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="8992a-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="8992a-1753">La struttura CCategorizationSet contiene informazioni sul raggruppamento di un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="8992a-1754">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1754">0</span></span>

<span data-ttu-id="8992a-1755">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1755">1</span></span>

<span data-ttu-id="8992a-1756">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1756">2</span></span>

<span data-ttu-id="8992a-1757">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1757">3</span></span>

<span data-ttu-id="8992a-1758">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1758">4</span></span>

<span data-ttu-id="8992a-1759">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1759">5</span></span>

<span data-ttu-id="8992a-1760">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1760">6</span></span>

<span data-ttu-id="8992a-1761">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1761">7</span></span>

<span data-ttu-id="8992a-1762">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1762">8</span></span>

<span data-ttu-id="8992a-1763">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1763">9</span></span>

<span data-ttu-id="8992a-1764">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1764">1</span></span><br/> <span data-ttu-id="8992a-1765">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1765">0</span></span><br/>

<span data-ttu-id="8992a-1766">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1766">1</span></span>

<span data-ttu-id="8992a-1767">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1767">2</span></span>

<span data-ttu-id="8992a-1768">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1768">3</span></span>

<span data-ttu-id="8992a-1769">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1769">4</span></span>

<span data-ttu-id="8992a-1770">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1770">5</span></span>

<span data-ttu-id="8992a-1771">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1771">6</span></span>

<span data-ttu-id="8992a-1772">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1772">7</span></span>

<span data-ttu-id="8992a-1773">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1773">8</span></span>

<span data-ttu-id="8992a-1774">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1774">9</span></span>

<span data-ttu-id="8992a-1775">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1775">2</span></span><br/> <span data-ttu-id="8992a-1776">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1776">0</span></span><br/>

<span data-ttu-id="8992a-1777">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1777">1</span></span>

<span data-ttu-id="8992a-1778">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1778">2</span></span>

<span data-ttu-id="8992a-1779">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1779">3</span></span>

<span data-ttu-id="8992a-1780">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1780">4</span></span>

<span data-ttu-id="8992a-1781">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1781">5</span></span>

<span data-ttu-id="8992a-1782">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1782">6</span></span>

<span data-ttu-id="8992a-1783">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1783">7</span></span>

<span data-ttu-id="8992a-1784">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1784">8</span></span>

<span data-ttu-id="8992a-1785">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1785">9</span></span>

<span data-ttu-id="8992a-1786">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1786">3</span></span><br/> <span data-ttu-id="8992a-1787">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1787">0</span></span><br/>

<span data-ttu-id="8992a-1788">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1788">1</span></span>

<span data-ttu-id="8992a-1789">count</span><span class="sxs-lookup"><span data-stu-id="8992a-1789">count</span></span>

<span data-ttu-id="8992a-1790">Categorie (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1790">categories (variable)</span></span>



 

<span data-ttu-id="8992a-1791">**count**: Unsigned Integer a 32 bit contenente il numero di elementi nella matrice di categorie.</span><span class="sxs-lookup"><span data-stu-id="8992a-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="8992a-1792">**categorie**: matrice di strutture CCategorizationSpec che specificano il raggruppamento della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="8992a-1793">CCategorizationSpec 2.2.1.19</span><span class="sxs-lookup"><span data-stu-id="8992a-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="8992a-1794">La struttura CCategorizationSpec contiene un raggruppamento per un set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="8992a-1795">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1795">0</span></span>

<span data-ttu-id="8992a-1796">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1796">1</span></span>

<span data-ttu-id="8992a-1797">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1797">2</span></span>

<span data-ttu-id="8992a-1798">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1798">3</span></span>

<span data-ttu-id="8992a-1799">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1799">4</span></span>

<span data-ttu-id="8992a-1800">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1800">5</span></span>

<span data-ttu-id="8992a-1801">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1801">6</span></span>

<span data-ttu-id="8992a-1802">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1802">7</span></span>

<span data-ttu-id="8992a-1803">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1803">8</span></span>

<span data-ttu-id="8992a-1804">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1804">9</span></span>

<span data-ttu-id="8992a-1805">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1805">1</span></span><br/> <span data-ttu-id="8992a-1806">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1806">0</span></span><br/>

<span data-ttu-id="8992a-1807">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1807">1</span></span>

<span data-ttu-id="8992a-1808">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1808">2</span></span>

<span data-ttu-id="8992a-1809">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1809">3</span></span>

<span data-ttu-id="8992a-1810">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1810">4</span></span>

<span data-ttu-id="8992a-1811">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1811">5</span></span>

<span data-ttu-id="8992a-1812">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1812">6</span></span>

<span data-ttu-id="8992a-1813">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1813">7</span></span>

<span data-ttu-id="8992a-1814">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1814">8</span></span>

<span data-ttu-id="8992a-1815">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1815">9</span></span>

<span data-ttu-id="8992a-1816">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1816">2</span></span><br/> <span data-ttu-id="8992a-1817">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1817">0</span></span><br/>

<span data-ttu-id="8992a-1818">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1818">1</span></span>

<span data-ttu-id="8992a-1819">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1819">2</span></span>

<span data-ttu-id="8992a-1820">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1820">3</span></span>

<span data-ttu-id="8992a-1821">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1821">4</span></span>

<span data-ttu-id="8992a-1822">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1822">5</span></span>

<span data-ttu-id="8992a-1823">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1823">6</span></span>

<span data-ttu-id="8992a-1824">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1824">7</span></span>

<span data-ttu-id="8992a-1825">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1825">8</span></span>

<span data-ttu-id="8992a-1826">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1826">9</span></span>

<span data-ttu-id="8992a-1827">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1827">3</span></span><br/> <span data-ttu-id="8992a-1828">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1828">0</span></span><br/>

<span data-ttu-id="8992a-1829">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1829">1</span></span>

<span data-ttu-id="8992a-1830">\_csColumns (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="8992a-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="8992a-1831">\_ulCategType</span></span>



 

<span data-ttu-id="8992a-1832">**\_ csColumns**: struttura CColumnSet che indica le colonne in base alle quali raggruppare la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="8992a-1833">**\_ ulCategType**: Unsigned Integer A 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8992a-1834">DEVE essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="8992a-1835">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="8992a-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="8992a-1836">La struttura CDbColId contiene una colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="8992a-1837">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1837">0</span></span>

<span data-ttu-id="8992a-1838">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1838">1</span></span>

<span data-ttu-id="8992a-1839">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1839">2</span></span>

<span data-ttu-id="8992a-1840">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1840">3</span></span>

<span data-ttu-id="8992a-1841">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1841">4</span></span>

<span data-ttu-id="8992a-1842">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1842">5</span></span>

<span data-ttu-id="8992a-1843">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1843">6</span></span>

<span data-ttu-id="8992a-1844">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1844">7</span></span>

<span data-ttu-id="8992a-1845">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1845">8</span></span>

<span data-ttu-id="8992a-1846">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1846">9</span></span>

<span data-ttu-id="8992a-1847">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1847">1</span></span><br/> <span data-ttu-id="8992a-1848">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1848">0</span></span><br/>

<span data-ttu-id="8992a-1849">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1849">1</span></span>

<span data-ttu-id="8992a-1850">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1850">2</span></span>

<span data-ttu-id="8992a-1851">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1851">3</span></span>

<span data-ttu-id="8992a-1852">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1852">4</span></span>

<span data-ttu-id="8992a-1853">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1853">5</span></span>

<span data-ttu-id="8992a-1854">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1854">6</span></span>

<span data-ttu-id="8992a-1855">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1855">7</span></span>

<span data-ttu-id="8992a-1856">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1856">8</span></span>

<span data-ttu-id="8992a-1857">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1857">9</span></span>

<span data-ttu-id="8992a-1858">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1858">2</span></span><br/> <span data-ttu-id="8992a-1859">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1859">0</span></span><br/>

<span data-ttu-id="8992a-1860">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1860">1</span></span>

<span data-ttu-id="8992a-1861">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1861">2</span></span>

<span data-ttu-id="8992a-1862">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1862">3</span></span>

<span data-ttu-id="8992a-1863">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1863">4</span></span>

<span data-ttu-id="8992a-1864">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1864">5</span></span>

<span data-ttu-id="8992a-1865">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1865">6</span></span>

<span data-ttu-id="8992a-1866">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1866">7</span></span>

<span data-ttu-id="8992a-1867">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1867">8</span></span>

<span data-ttu-id="8992a-1868">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1868">9</span></span>

<span data-ttu-id="8992a-1869">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1869">3</span></span><br/> <span data-ttu-id="8992a-1870">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1870">0</span></span><br/>

<span data-ttu-id="8992a-1871">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1871">1</span></span>

<span data-ttu-id="8992a-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="8992a-1872">eKind</span></span>

<span data-ttu-id="8992a-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="8992a-1873">GUID</span></span>

<span data-ttu-id="8992a-1874">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1874">...</span></span>

<span data-ttu-id="8992a-1875">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1875">...</span></span>

<span data-ttu-id="8992a-1876">...</span><span class="sxs-lookup"><span data-stu-id="8992a-1876">...</span></span>

<span data-ttu-id="8992a-1877">ulId</span><span class="sxs-lookup"><span data-stu-id="8992a-1877">ulId</span></span>

<span data-ttu-id="8992a-1878">vString (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1878">vString (variable)</span></span>



 

<span data-ttu-id="8992a-1879">**eKind**: deve essere impostato su uno dei valori riportati di seguito che indica il contenuto di GUID e vValue.</span><span class="sxs-lookup"><span data-stu-id="8992a-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="8992a-1880">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1880">Value</span></span>                            | <span data-ttu-id="8992a-1881">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1882">\_Nome GUID dbkind \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="8992a-1883">vString contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="8992a-1884">\_GUID dbkind \_ propid 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="8992a-1885">ulId contiene un intero a 4 byte che indica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="8992a-1886">DBKIND \_ PGUID \_ nome 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8992a-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="8992a-1887">vString contiene un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1887">vString contains a property name.</span></span> <span data-ttu-id="8992a-1888">Questo valore deve essere considerato uguale al \_ nome GUID di dbkind \_ .</span><span class="sxs-lookup"><span data-stu-id="8992a-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="8992a-1889">DBKIND \_ PGUID \_ propid 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8992a-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="8992a-1890">ulId contiene un intero a 4 byte che indica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="8992a-1891">Questo valore deve corrispondere al \_ GUID dbkind \_ propid.</span><span class="sxs-lookup"><span data-stu-id="8992a-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="8992a-1892">**GUID**: GUID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="8992a-1893">**ulId**: se EKIND è dbkind \_ GUID \_ propid o dbkind PGUID propid \_ \_ , questo campo contiene un Unsigned Integer, specificando l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="8992a-1894">Se eKind è DBKIND \_ GUID \_ Name o dbkind \_ PGUID \_ Name, questo campo contiene un Unsigned Integer specificando il numero di caratteri Unicode contenuti nel campo VString.</span><span class="sxs-lookup"><span data-stu-id="8992a-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="8992a-1895">**VString**: stringa Unicode senza terminazione null che rappresenta il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="8992a-1896">È necessario ometterlo, a meno che il campo eKind non sia impostato su DBKIND \_ GUID \_ Name o dbkind \_ PGUID \_ .</span><span class="sxs-lookup"><span data-stu-id="8992a-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="8992a-1897">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="8992a-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="8992a-1898">La struttura CDbProp contiene una proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="8992a-1899">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1899">0</span></span>

<span data-ttu-id="8992a-1900">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1900">1</span></span>

<span data-ttu-id="8992a-1901">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1901">2</span></span>

<span data-ttu-id="8992a-1902">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1902">3</span></span>

<span data-ttu-id="8992a-1903">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1903">4</span></span>

<span data-ttu-id="8992a-1904">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1904">5</span></span>

<span data-ttu-id="8992a-1905">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1905">6</span></span>

<span data-ttu-id="8992a-1906">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1906">7</span></span>

<span data-ttu-id="8992a-1907">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1907">8</span></span>

<span data-ttu-id="8992a-1908">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1908">9</span></span>

<span data-ttu-id="8992a-1909">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1909">1</span></span><br/> <span data-ttu-id="8992a-1910">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1910">0</span></span><br/>

<span data-ttu-id="8992a-1911">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1911">1</span></span>

<span data-ttu-id="8992a-1912">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1912">2</span></span>

<span data-ttu-id="8992a-1913">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1913">3</span></span>

<span data-ttu-id="8992a-1914">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1914">4</span></span>

<span data-ttu-id="8992a-1915">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1915">5</span></span>

<span data-ttu-id="8992a-1916">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1916">6</span></span>

<span data-ttu-id="8992a-1917">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1917">7</span></span>

<span data-ttu-id="8992a-1918">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1918">8</span></span>

<span data-ttu-id="8992a-1919">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1919">9</span></span>

<span data-ttu-id="8992a-1920">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1920">2</span></span><br/> <span data-ttu-id="8992a-1921">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1921">0</span></span><br/>

<span data-ttu-id="8992a-1922">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1922">1</span></span>

<span data-ttu-id="8992a-1923">2</span><span class="sxs-lookup"><span data-stu-id="8992a-1923">2</span></span>

<span data-ttu-id="8992a-1924">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1924">3</span></span>

<span data-ttu-id="8992a-1925">4</span><span class="sxs-lookup"><span data-stu-id="8992a-1925">4</span></span>

<span data-ttu-id="8992a-1926">5</span><span class="sxs-lookup"><span data-stu-id="8992a-1926">5</span></span>

<span data-ttu-id="8992a-1927">6</span><span class="sxs-lookup"><span data-stu-id="8992a-1927">6</span></span>

<span data-ttu-id="8992a-1928">7</span><span class="sxs-lookup"><span data-stu-id="8992a-1928">7</span></span>

<span data-ttu-id="8992a-1929">8</span><span class="sxs-lookup"><span data-stu-id="8992a-1929">8</span></span>

<span data-ttu-id="8992a-1930">9</span><span class="sxs-lookup"><span data-stu-id="8992a-1930">9</span></span>

<span data-ttu-id="8992a-1931">3</span><span class="sxs-lookup"><span data-stu-id="8992a-1931">3</span></span><br/> <span data-ttu-id="8992a-1932">0</span><span class="sxs-lookup"><span data-stu-id="8992a-1932">0</span></span><br/>

<span data-ttu-id="8992a-1933">1</span><span class="sxs-lookup"><span data-stu-id="8992a-1933">1</span></span>

<span data-ttu-id="8992a-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="8992a-1934">DBPROPID</span></span>

<span data-ttu-id="8992a-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="8992a-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="8992a-1936">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="8992a-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="8992a-1937">colid (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1937">colid (variable)</span></span>

<span data-ttu-id="8992a-1938">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-1938">vValue (variable)</span></span>



 

<span data-ttu-id="8992a-1939">**DBPROPID**: Unsigned Integer A 32 bit, che indica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="8992a-1940">**DBPROPOPTIONS** : deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="8992a-1941">**DBPROPSTATUS**: deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="8992a-1942">**colid**: struttura CDbColId, come specificato nella sezione 2.2.1.20, che indica la colonna a cui viene applicata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="8992a-1943">**vValue**: CBaseStorageVariant che contiene il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="8992a-1944">Proprietà di 2.2.1.21.1</span><span class="sxs-lookup"><span data-stu-id="8992a-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="8992a-1945">In questa sezione vengono illustrate in dettaglio le proprietà utilizzate da CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="8992a-1946">Queste proprietà sono raggruppate in tre set di proprietà, ident 2.2.1.21.1 in Unified nel campo guidPropertySet della struttura CDbPropSet (Section 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="8992a-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="8992a-1947">La tabella seguente elenca le proprietà che fanno parte del set di \_ proprietà DBPROPSET FSCIFRMWRK \_ ext.</span><span class="sxs-lookup"><span data-stu-id="8992a-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="8992a-1948">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1948">Value</span></span>                                  | <span data-ttu-id="8992a-1949">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1950">DBPROP \_ \_ nome catalogo ci \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="8992a-1951">Specifica il nome del catalogo o dei cataloghi su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="8992a-1952">Il valore deve essere un VT \_ LPWSTR o un \_ vettore \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="8992a-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="8992a-1953">DBPROP \_ ci \_ include \_ ambiti 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8992a-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="8992a-1954">Specifica uno o più percorsi da includere nella query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="8992a-1955">Il valore deve essere un \_ LPWSTR VT o un \_ LPWSTR VT Vector VT \| \_ .</span><span class="sxs-lookup"><span data-stu-id="8992a-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="8992a-1956">DBPROP \_ \_ flag di ambito ci \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8992a-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="8992a-1957">Specifica il modo in cui devono essere gestiti i percorsi specificati dalla \_ \_ proprietà degli ambiti di inclusione DBPROP ci \_ .</span><span class="sxs-lookup"><span data-stu-id="8992a-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="8992a-1958">Il valore deve essere un VT \_ I4 o un \_ vettore \| VT \_ i4.</span><span class="sxs-lookup"><span data-stu-id="8992a-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="8992a-1959">\_Tipo di \_ query ci DBPROP \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8992a-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="8992a-1960">Specifica il tipo di query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1960">Specifies the type of query.</span></span> <span data-ttu-id="8992a-1961">CDbColId deve essere impostato su DB \_ NULLID.</span><span class="sxs-lookup"><span data-stu-id="8992a-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="8992a-1962">La tabella seguente elenca i flag per la \_ proprietà dei \_ flag di ambito ci DBPROP \_ :</span><span class="sxs-lookup"><span data-stu-id="8992a-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="8992a-1963">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1963">Value</span></span>                     | <span data-ttu-id="8992a-1964">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1965">Eseguire QUERY \_ 0x01 approfondite</span><span class="sxs-lookup"><span data-stu-id="8992a-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="8992a-1966">Se impostato, indica che i file nella directory scope e in tutte le sottodirectory sono inclusi nei risultati.</span><span class="sxs-lookup"><span data-stu-id="8992a-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="8992a-1967">Se è chiaro, nei risultati vengono inclusi solo i file nella directory dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="8992a-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="8992a-1968">NON devono essere combinati con una QUERY \_ approfondita.</span><span class="sxs-lookup"><span data-stu-id="8992a-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="8992a-1969">QUERY \_ \_ percorso virtuale 0x02</span><span class="sxs-lookup"><span data-stu-id="8992a-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="8992a-1970">Se impostato, indica che l'ambito è un percorso virtuale.</span><span class="sxs-lookup"><span data-stu-id="8992a-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="8992a-1971">Se chiaro, indica che l'ambito è una directory fisica.</span><span class="sxs-lookup"><span data-stu-id="8992a-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="8992a-1972">Nella tabella seguente sono elencati i tipi di query per \_ la \_ Proprietà tipo di query ci DBPROP \_ :</span><span class="sxs-lookup"><span data-stu-id="8992a-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="8992a-1973">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1973">Value</span></span>                     | <span data-ttu-id="8992a-1974">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1975">0x00000000 CiNormal</span><span class="sxs-lookup"><span data-stu-id="8992a-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="8992a-1976">Query normale.</span><span class="sxs-lookup"><span data-stu-id="8992a-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="8992a-1977">0x00000001 CiVirtualRoots</span><span class="sxs-lookup"><span data-stu-id="8992a-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="8992a-1978">La query richiede un elenco delle radici virtuali del catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="8992a-1979">Questo valore richiede privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="8992a-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="8992a-1980">0x00000003 CiProperties</span><span class="sxs-lookup"><span data-stu-id="8992a-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="8992a-1981">La query richiede un elenco di tutte le proprietà supportate dal servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="8992a-1982">0x00000004 CiAdminOp</span><span class="sxs-lookup"><span data-stu-id="8992a-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="8992a-1983">La query è un'operazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="8992a-1983">The query is an administrative operation.</span></span> <span data-ttu-id="8992a-1984">Questo valore richiede privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="8992a-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="8992a-1985">La tabella seguente elenca le proprietà che fanno parte del set di \_ Proprietà QUERYEXT di DBPROPSET.</span><span class="sxs-lookup"><span data-stu-id="8992a-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="8992a-1986">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-1986">Value</span></span>                                      | <span data-ttu-id="8992a-1987">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-1988">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="8992a-1989">Specifica il modo in cui il servizio di indicizzazione è in grado di gestire query lente.</span><span class="sxs-lookup"><span data-stu-id="8992a-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="8992a-1990">Il valore deve essere un \_ bool VT.</span><span class="sxs-lookup"><span data-stu-id="8992a-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="8992a-1991">Se TRUE, il server è autorizzato a eseguire l'errore di queste query.</span><span class="sxs-lookup"><span data-stu-id="8992a-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="8992a-1992">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8992a-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="8992a-1993">Indica se il servizio di indicizzazione deve eseguire la rimozione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="8992a-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="8992a-1994">Se TRUE, il server deve prendere in considerazione l'esecuzione del taglio dei risultati in modo da ottimizzare il tempo di risposta per il client.</span><span class="sxs-lookup"><span data-stu-id="8992a-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="8992a-1995">Il valore deve essere un \_ bool VT.</span><span class="sxs-lookup"><span data-stu-id="8992a-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="8992a-1996">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8992a-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="8992a-1997">Indica se il client supporta i \_ tipi di dati vettoriali VT.</span><span class="sxs-lookup"><span data-stu-id="8992a-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="8992a-1998">Se TRUE, il client supporta il \_ vettore VT; se è false, il server deve convertire i \_ tipi di dati vettoriali VT in tipi di \_ dati matrice VT.</span><span class="sxs-lookup"><span data-stu-id="8992a-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="8992a-1999">Il valore deve essere un \_ bool VT.</span><span class="sxs-lookup"><span data-stu-id="8992a-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="8992a-2000">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8992a-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="8992a-2001">Indica le corrispondenze di riga da restituire.</span><span class="sxs-lookup"><span data-stu-id="8992a-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="8992a-2002">Se TRUE, il server deve restituire il primo set di righe corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="8992a-2003">Se FALSE, verranno restituite le righe corrispondenti migliori.</span><span class="sxs-lookup"><span data-stu-id="8992a-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="8992a-2004">Il valore deve essere un \_ bool VT.</span><span class="sxs-lookup"><span data-stu-id="8992a-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="8992a-2005">La tabella seguente elenca le proprietà che fanno parte del set di \_ proprietà DBPROPSET CIFRMWRKCORE \_ ext.</span><span class="sxs-lookup"><span data-stu-id="8992a-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="8992a-2006">Valore/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="8992a-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="8992a-2007">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-2008">\_0x00000002 del computer DBPROP</span><span class="sxs-lookup"><span data-stu-id="8992a-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="8992a-2009">Specifica i nomi dei computer in cui deve essere elaborata una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="8992a-2010">Il valore deve essere VT \_ BSTR o VT \_ Array VT \| \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="8992a-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="8992a-2011">\_ \_ 0x00000003 CLSID client DBPROP</span><span class="sxs-lookup"><span data-stu-id="8992a-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="8992a-2012">Specifica una costante di connessione per il servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="8992a-2013">Il valore deve essere un \_ CLSID VT contenente 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="8992a-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="8992a-2014">CDbPropSet 2.2.1.22</span><span class="sxs-lookup"><span data-stu-id="8992a-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="8992a-2015">La struttura CDbPropSet contiene un set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="8992a-2016">Si noti che il primo campo è a dimensione fissa, ma potrebbe non essere allineato a un offset che corrisponde a un multiplo di 4 byte dall'inizio del messaggio che contiene la struttura.</span><span class="sxs-lookup"><span data-stu-id="8992a-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="8992a-2017">Tuttavia, il campo cProperties è allineato come tale, quindi il formato viene illustrato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="8992a-2018">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2018">0</span></span>

<span data-ttu-id="8992a-2019">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2019">1</span></span>

<span data-ttu-id="8992a-2020">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2020">2</span></span>

<span data-ttu-id="8992a-2021">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2021">3</span></span>

<span data-ttu-id="8992a-2022">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2022">4</span></span>

<span data-ttu-id="8992a-2023">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2023">5</span></span>

<span data-ttu-id="8992a-2024">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2024">6</span></span>

<span data-ttu-id="8992a-2025">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2025">7</span></span>

<span data-ttu-id="8992a-2026">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2026">8</span></span>

<span data-ttu-id="8992a-2027">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2027">9</span></span>

<span data-ttu-id="8992a-2028">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2028">1</span></span><br/> <span data-ttu-id="8992a-2029">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2029">0</span></span><br/>

<span data-ttu-id="8992a-2030">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2030">1</span></span>

<span data-ttu-id="8992a-2031">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2031">2</span></span>

<span data-ttu-id="8992a-2032">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2032">3</span></span>

<span data-ttu-id="8992a-2033">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2033">4</span></span>

<span data-ttu-id="8992a-2034">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2034">5</span></span>

<span data-ttu-id="8992a-2035">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2035">6</span></span>

<span data-ttu-id="8992a-2036">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2036">7</span></span>

<span data-ttu-id="8992a-2037">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2037">8</span></span>

<span data-ttu-id="8992a-2038">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2038">9</span></span>

<span data-ttu-id="8992a-2039">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2039">2</span></span><br/> <span data-ttu-id="8992a-2040">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2040">0</span></span><br/>

<span data-ttu-id="8992a-2041">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2041">1</span></span>

<span data-ttu-id="8992a-2042">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2042">2</span></span>

<span data-ttu-id="8992a-2043">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2043">3</span></span>

<span data-ttu-id="8992a-2044">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2044">4</span></span>

<span data-ttu-id="8992a-2045">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2045">5</span></span>

<span data-ttu-id="8992a-2046">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2046">6</span></span>

<span data-ttu-id="8992a-2047">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2047">7</span></span>

<span data-ttu-id="8992a-2048">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2048">8</span></span>

<span data-ttu-id="8992a-2049">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2049">9</span></span>

<span data-ttu-id="8992a-2050">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2050">3</span></span><br/> <span data-ttu-id="8992a-2051">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2051">0</span></span><br/>

<span data-ttu-id="8992a-2052">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2052">1</span></span>

<span data-ttu-id="8992a-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="8992a-2053">guidPropertySet</span></span>

<span data-ttu-id="8992a-2054">...</span><span class="sxs-lookup"><span data-stu-id="8992a-2054">...</span></span>

<span data-ttu-id="8992a-2055">...</span><span class="sxs-lookup"><span data-stu-id="8992a-2055">...</span></span>

<span data-ttu-id="8992a-2056">...</span><span class="sxs-lookup"><span data-stu-id="8992a-2056">...</span></span>

<span data-ttu-id="8992a-2057">...</span><span class="sxs-lookup"><span data-stu-id="8992a-2057">...</span></span>

<span data-ttu-id="8992a-2058">\_spaziatura interna (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-2058">\_padding (variable)</span></span>

<span data-ttu-id="8992a-2059">cProperties</span><span class="sxs-lookup"><span data-stu-id="8992a-2059">cProperties</span></span>

<span data-ttu-id="8992a-2060">aProps (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-2060">aProps (variable)</span></span>



 

<span data-ttu-id="8992a-2061">**guidPropertySet**: GUID che identifica il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="8992a-2062">DEVE essere impostato sul form binario corrispondente a uno dei valori seguenti (visualizzato nel formato di rappresentazione di stringa), che identifica il set di proprietà delle proprietà contenute nel campo aProps.</span><span class="sxs-lookup"><span data-stu-id="8992a-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="8992a-2063">Valore/GUID</span><span class="sxs-lookup"><span data-stu-id="8992a-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="8992a-2064">Nome</span><span class="sxs-lookup"><span data-stu-id="8992a-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="8992a-2065">DBPROPSET \_ FSCIFRMWRK \_ ext</span><span class="sxs-lookup"><span data-stu-id="8992a-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="8992a-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="8992a-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="8992a-2067">Set di proprietà del Framework dell'indice di contenuto del file System</span><span class="sxs-lookup"><span data-stu-id="8992a-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="8992a-2068">\_QUERYEXT DBPROPSET</span><span class="sxs-lookup"><span data-stu-id="8992a-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="8992a-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="8992a-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="8992a-2070">Set di proprietà dell'estensione di query</span><span class="sxs-lookup"><span data-stu-id="8992a-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="8992a-2071">DBPROPSET \_ CIFRMWRKCORE \_ ext</span><span class="sxs-lookup"><span data-stu-id="8992a-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="8992a-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="8992a-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="8992a-2073">Set di proprietà di base dell'indice di contenuto</span><span class="sxs-lookup"><span data-stu-id="8992a-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="8992a-2074">**\_ spaziatura interna**: questo campo deve avere una lunghezza compresa tra 0 e 3 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8992a-2075">La lunghezza di questo campo deve essere tale che il campo seguente inizia con un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la struttura.</span><span class="sxs-lookup"><span data-stu-id="8992a-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8992a-2076">Se questo campo è presente (ovvero, lunghezza diversa da zero), il valore in esso contenuto è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8992a-2077">Il contenuto di questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-2078">**cProperties**: Unsigned Integer a 32 bit contenente il numero di elementi nella matrice aProps.</span><span class="sxs-lookup"><span data-stu-id="8992a-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="8992a-2079">**aProps**: matrice di strutture CDbProp, come specificato nella sezione 0, che contiene le proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="8992a-2080">Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura inizi in corrispondenza di un offset costituito da un multiplo di 4 byte a partire dall'inizio del messaggio che contiene la matrice.</span><span class="sxs-lookup"><span data-stu-id="8992a-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="8992a-2081">Se sono presenti byte di riempimento, il valore che contengono è arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="8992a-2082">Il contenuto dei byte di riempimento deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="8992a-2083">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="8992a-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="8992a-2084">La struttura CPidMapper contiene una matrice di ID di proprietà che specificano le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="8992a-2085">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2085">0</span></span>

<span data-ttu-id="8992a-2086">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2086">1</span></span>

<span data-ttu-id="8992a-2087">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2087">2</span></span>

<span data-ttu-id="8992a-2088">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2088">3</span></span>

<span data-ttu-id="8992a-2089">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2089">4</span></span>

<span data-ttu-id="8992a-2090">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2090">5</span></span>

<span data-ttu-id="8992a-2091">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2091">6</span></span>

<span data-ttu-id="8992a-2092">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2092">7</span></span>

<span data-ttu-id="8992a-2093">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2093">8</span></span>

<span data-ttu-id="8992a-2094">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2094">9</span></span>

<span data-ttu-id="8992a-2095">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2095">1</span></span><br/> <span data-ttu-id="8992a-2096">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2096">0</span></span><br/>

<span data-ttu-id="8992a-2097">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2097">1</span></span>

<span data-ttu-id="8992a-2098">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2098">2</span></span>

<span data-ttu-id="8992a-2099">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2099">3</span></span>

<span data-ttu-id="8992a-2100">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2100">4</span></span>

<span data-ttu-id="8992a-2101">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2101">5</span></span>

<span data-ttu-id="8992a-2102">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2102">6</span></span>

<span data-ttu-id="8992a-2103">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2103">7</span></span>

<span data-ttu-id="8992a-2104">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2104">8</span></span>

<span data-ttu-id="8992a-2105">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2105">9</span></span>

<span data-ttu-id="8992a-2106">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2106">2</span></span><br/> <span data-ttu-id="8992a-2107">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2107">0</span></span><br/>

<span data-ttu-id="8992a-2108">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2108">1</span></span>

<span data-ttu-id="8992a-2109">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2109">2</span></span>

<span data-ttu-id="8992a-2110">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2110">3</span></span>

<span data-ttu-id="8992a-2111">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2111">4</span></span>

<span data-ttu-id="8992a-2112">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2112">5</span></span>

<span data-ttu-id="8992a-2113">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2113">6</span></span>

<span data-ttu-id="8992a-2114">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2114">7</span></span>

<span data-ttu-id="8992a-2115">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2115">8</span></span>

<span data-ttu-id="8992a-2116">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2116">9</span></span>

<span data-ttu-id="8992a-2117">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2117">3</span></span><br/> <span data-ttu-id="8992a-2118">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2118">0</span></span><br/>

<span data-ttu-id="8992a-2119">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2119">1</span></span>

<span data-ttu-id="8992a-2120">count</span><span class="sxs-lookup"><span data-stu-id="8992a-2120">count</span></span>

<span data-ttu-id="8992a-2121">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="8992a-2121">aPropSpec</span></span>

<span data-ttu-id="8992a-2122">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-2122">... (variable)</span></span>



 

<span data-ttu-id="8992a-2123">**count**: Unsigned Integer a 32 bit contenente il numero di elementi nella matrice aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="8992a-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="8992a-2124">**aPropSpec**: matrice di strutture CFullPropSpec che indica le proprietà da restituire.</span><span class="sxs-lookup"><span data-stu-id="8992a-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="8992a-2125">Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura disponga di un allineamento a 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="8992a-2126">Tali byte di riempimento possono essere qualsiasi valore arbitrario e devono essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="8992a-2127">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="8992a-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="8992a-2128">La struttura CRowSeekAt contiene l'offset in corrispondenza del quale recuperare le righe in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="8992a-2129">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2129">0</span></span>

<span data-ttu-id="8992a-2130">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2130">1</span></span>

<span data-ttu-id="8992a-2131">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2131">2</span></span>

<span data-ttu-id="8992a-2132">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2132">3</span></span>

<span data-ttu-id="8992a-2133">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2133">4</span></span>

<span data-ttu-id="8992a-2134">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2134">5</span></span>

<span data-ttu-id="8992a-2135">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2135">6</span></span>

<span data-ttu-id="8992a-2136">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2136">7</span></span>

<span data-ttu-id="8992a-2137">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2137">8</span></span>

<span data-ttu-id="8992a-2138">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2138">9</span></span>

<span data-ttu-id="8992a-2139">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2139">1</span></span><br/> <span data-ttu-id="8992a-2140">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2140">0</span></span><br/>

<span data-ttu-id="8992a-2141">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2141">1</span></span>

<span data-ttu-id="8992a-2142">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2142">2</span></span>

<span data-ttu-id="8992a-2143">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2143">3</span></span>

<span data-ttu-id="8992a-2144">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2144">4</span></span>

<span data-ttu-id="8992a-2145">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2145">5</span></span>

<span data-ttu-id="8992a-2146">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2146">6</span></span>

<span data-ttu-id="8992a-2147">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2147">7</span></span>

<span data-ttu-id="8992a-2148">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2148">8</span></span>

<span data-ttu-id="8992a-2149">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2149">9</span></span>

<span data-ttu-id="8992a-2150">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2150">2</span></span><br/> <span data-ttu-id="8992a-2151">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2151">0</span></span><br/>

<span data-ttu-id="8992a-2152">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2152">1</span></span>

<span data-ttu-id="8992a-2153">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2153">2</span></span>

<span data-ttu-id="8992a-2154">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2154">3</span></span>

<span data-ttu-id="8992a-2155">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2155">4</span></span>

<span data-ttu-id="8992a-2156">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2156">5</span></span>

<span data-ttu-id="8992a-2157">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2157">6</span></span>

<span data-ttu-id="8992a-2158">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2158">7</span></span>

<span data-ttu-id="8992a-2159">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2159">8</span></span>

<span data-ttu-id="8992a-2160">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2160">9</span></span>

<span data-ttu-id="8992a-2161">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2161">3</span></span><br/> <span data-ttu-id="8992a-2162">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2162">0</span></span><br/>

<span data-ttu-id="8992a-2163">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2163">1</span></span>

<span data-ttu-id="8992a-2164">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="8992a-2164">\_hRegion</span></span>

<span data-ttu-id="8992a-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="8992a-2165">\_cskip</span></span>

<span data-ttu-id="8992a-2166">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="8992a-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="8992a-2167">**\_ hRegion**: deve essere impostato su 0x00000000 e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="8992a-2168">**\_ cskip**: Unsigned Integer a 32 bit contenente il numero di righe da ignorare nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="8992a-2169">**\_ bmkOffset**: valore a 32 bit che rappresenta l'handle del **segnalibro** che indica la posizione iniziale dalla quale ignorare il numero di righe specificato in \_ cskip, prima di iniziare il recupero.</span><span class="sxs-lookup"><span data-stu-id="8992a-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="8992a-2170">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="8992a-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="8992a-2171">La struttura CRowSeekAtRatio identifica il punto in corrispondenza del quale iniziare il recupero per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="8992a-2172">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2172">0</span></span>

<span data-ttu-id="8992a-2173">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2173">1</span></span>

<span data-ttu-id="8992a-2174">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2174">2</span></span>

<span data-ttu-id="8992a-2175">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2175">3</span></span>

<span data-ttu-id="8992a-2176">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2176">4</span></span>

<span data-ttu-id="8992a-2177">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2177">5</span></span>

<span data-ttu-id="8992a-2178">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2178">6</span></span>

<span data-ttu-id="8992a-2179">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2179">7</span></span>

<span data-ttu-id="8992a-2180">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2180">8</span></span>

<span data-ttu-id="8992a-2181">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2181">9</span></span>

<span data-ttu-id="8992a-2182">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2182">1</span></span><br/> <span data-ttu-id="8992a-2183">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2183">0</span></span><br/>

<span data-ttu-id="8992a-2184">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2184">1</span></span>

<span data-ttu-id="8992a-2185">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2185">2</span></span>

<span data-ttu-id="8992a-2186">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2186">3</span></span>

<span data-ttu-id="8992a-2187">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2187">4</span></span>

<span data-ttu-id="8992a-2188">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2188">5</span></span>

<span data-ttu-id="8992a-2189">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2189">6</span></span>

<span data-ttu-id="8992a-2190">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2190">7</span></span>

<span data-ttu-id="8992a-2191">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2191">8</span></span>

<span data-ttu-id="8992a-2192">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2192">9</span></span>

<span data-ttu-id="8992a-2193">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2193">2</span></span><br/> <span data-ttu-id="8992a-2194">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2194">0</span></span><br/>

<span data-ttu-id="8992a-2195">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2195">1</span></span>

<span data-ttu-id="8992a-2196">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2196">2</span></span>

<span data-ttu-id="8992a-2197">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2197">3</span></span>

<span data-ttu-id="8992a-2198">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2198">4</span></span>

<span data-ttu-id="8992a-2199">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2199">5</span></span>

<span data-ttu-id="8992a-2200">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2200">6</span></span>

<span data-ttu-id="8992a-2201">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2201">7</span></span>

<span data-ttu-id="8992a-2202">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2202">8</span></span>

<span data-ttu-id="8992a-2203">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2203">9</span></span>

<span data-ttu-id="8992a-2204">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2204">3</span></span><br/> <span data-ttu-id="8992a-2205">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2205">0</span></span><br/>

<span data-ttu-id="8992a-2206">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2206">1</span></span>

<span data-ttu-id="8992a-2207">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="8992a-2207">CiTblChapt</span></span>

<span data-ttu-id="8992a-2208">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="8992a-2208">\_hRegion</span></span>

<span data-ttu-id="8992a-2209">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="8992a-2209">\_ulNumerator</span></span>

<span data-ttu-id="8992a-2210">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="8992a-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="8992a-2211">**CiTblChapt**: Unsigned Integer a 32 bit che indica il capitolo del set di righe da cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="8992a-2212">**\_ hRegion**: deve essere impostato su 0x00000000 e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="8992a-2213">**\_ ulNumerator**: intero senza segno a 32 bit che rappresenta il numeratore del rapporto di righe nel capitolo da cui iniziare il recupero.</span><span class="sxs-lookup"><span data-stu-id="8992a-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="8992a-2214">**\_ ulDenominator**: intero senza segno a 32 bit che rappresenta il denominatore del rapporto di righe nel capitolo da cui iniziare il recupero.</span><span class="sxs-lookup"><span data-stu-id="8992a-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="8992a-2215">DEVE essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="8992a-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="8992a-2216">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="8992a-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="8992a-2217">La struttura CRowSeekByBookmark identifica i segnalibri da cui iniziare il recupero delle righe per un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="8992a-2218">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2218">0</span></span>

<span data-ttu-id="8992a-2219">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2219">1</span></span>

<span data-ttu-id="8992a-2220">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2220">2</span></span>

<span data-ttu-id="8992a-2221">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2221">3</span></span>

<span data-ttu-id="8992a-2222">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2222">4</span></span>

<span data-ttu-id="8992a-2223">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2223">5</span></span>

<span data-ttu-id="8992a-2224">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2224">6</span></span>

<span data-ttu-id="8992a-2225">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2225">7</span></span>

<span data-ttu-id="8992a-2226">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2226">8</span></span>

<span data-ttu-id="8992a-2227">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2227">9</span></span>

<span data-ttu-id="8992a-2228">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2228">1</span></span><br/> <span data-ttu-id="8992a-2229">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2229">0</span></span><br/>

<span data-ttu-id="8992a-2230">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2230">1</span></span>

<span data-ttu-id="8992a-2231">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2231">2</span></span>

<span data-ttu-id="8992a-2232">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2232">3</span></span>

<span data-ttu-id="8992a-2233">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2233">4</span></span>

<span data-ttu-id="8992a-2234">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2234">5</span></span>

<span data-ttu-id="8992a-2235">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2235">6</span></span>

<span data-ttu-id="8992a-2236">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2236">7</span></span>

<span data-ttu-id="8992a-2237">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2237">8</span></span>

<span data-ttu-id="8992a-2238">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2238">9</span></span>

<span data-ttu-id="8992a-2239">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2239">2</span></span><br/> <span data-ttu-id="8992a-2240">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2240">0</span></span><br/>

<span data-ttu-id="8992a-2241">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2241">1</span></span>

<span data-ttu-id="8992a-2242">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2242">2</span></span>

<span data-ttu-id="8992a-2243">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2243">3</span></span>

<span data-ttu-id="8992a-2244">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2244">4</span></span>

<span data-ttu-id="8992a-2245">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2245">5</span></span>

<span data-ttu-id="8992a-2246">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2246">6</span></span>

<span data-ttu-id="8992a-2247">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2247">7</span></span>

<span data-ttu-id="8992a-2248">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2248">8</span></span>

<span data-ttu-id="8992a-2249">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2249">9</span></span>

<span data-ttu-id="8992a-2250">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2250">3</span></span><br/> <span data-ttu-id="8992a-2251">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2251">0</span></span><br/>

<span data-ttu-id="8992a-2252">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2252">1</span></span>

<span data-ttu-id="8992a-2253">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="8992a-2253">\_hRegion</span></span>

<span data-ttu-id="8992a-2254">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="8992a-2254">\_cBookmarks</span></span>

<span data-ttu-id="8992a-2255">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="8992a-2255">\_maxRet</span></span>

<span data-ttu-id="8992a-2256">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="8992a-2256">\_cValidRet</span></span>

<span data-ttu-id="8992a-2257">\_aBookmarks (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="8992a-2258">\_ascRet (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="8992a-2259">**\_ hRegion**: deve essere impostato su 0x00000000 e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="8992a-2260">**\_ cBookmarks**: intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice aBookmarks.</span><span class="sxs-lookup"><span data-stu-id="8992a-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="8992a-2261">**\_ maxRet**: intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice ascRet.</span><span class="sxs-lookup"><span data-stu-id="8992a-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="8992a-2262">**\_ cValidRet**: intero senza segno a 32 bit che rappresenta il numero di elementi nella \_ matrice ascRet che sono validi.</span><span class="sxs-lookup"><span data-stu-id="8992a-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="8992a-2263">Nella matrice sono stati definiti elementi validi, mentre gli elementi non validi sono indefiniti.</span><span class="sxs-lookup"><span data-stu-id="8992a-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="8992a-2264">**\_ aBookmarks**: matrice di handle di segnalibro, rappresentati da 4 byte, ottenuti da un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="8992a-2265">**\_ ascRet**: matrice di valori HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8992a-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="8992a-2266">Quando CRowSeekByBookMark viene inviato come parte della richiesta CPMGetRowsIn, il numero di voci nella matrice deve essere uguale a \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="8992a-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="8992a-2267">Quando vengono inviati dal client, i valori devono essere impostati su zero e il server deve ignorare il contenuto della matrice.</span><span class="sxs-lookup"><span data-stu-id="8992a-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="8992a-2268">Quando viene inviato dal server (come parte del messaggio CPMGetRowsOut), i valori nella matrice indicano lo stato dei risultati per ogni recupero di riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="8992a-2269">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="8992a-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="8992a-2270">La struttura CRowSeekNext contiene il numero di righe da ignorare in un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="8992a-2271">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2271">0</span></span>

<span data-ttu-id="8992a-2272">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2272">1</span></span>

<span data-ttu-id="8992a-2273">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2273">2</span></span>

<span data-ttu-id="8992a-2274">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2274">3</span></span>

<span data-ttu-id="8992a-2275">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2275">4</span></span>

<span data-ttu-id="8992a-2276">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2276">5</span></span>

<span data-ttu-id="8992a-2277">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2277">6</span></span>

<span data-ttu-id="8992a-2278">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2278">7</span></span>

<span data-ttu-id="8992a-2279">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2279">8</span></span>

<span data-ttu-id="8992a-2280">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2280">9</span></span>

<span data-ttu-id="8992a-2281">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2281">1</span></span><br/> <span data-ttu-id="8992a-2282">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2282">0</span></span><br/>

<span data-ttu-id="8992a-2283">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2283">1</span></span>

<span data-ttu-id="8992a-2284">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2284">2</span></span>

<span data-ttu-id="8992a-2285">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2285">3</span></span>

<span data-ttu-id="8992a-2286">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2286">4</span></span>

<span data-ttu-id="8992a-2287">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2287">5</span></span>

<span data-ttu-id="8992a-2288">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2288">6</span></span>

<span data-ttu-id="8992a-2289">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2289">7</span></span>

<span data-ttu-id="8992a-2290">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2290">8</span></span>

<span data-ttu-id="8992a-2291">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2291">9</span></span>

<span data-ttu-id="8992a-2292">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2292">2</span></span><br/> <span data-ttu-id="8992a-2293">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2293">0</span></span><br/>

<span data-ttu-id="8992a-2294">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2294">1</span></span>

<span data-ttu-id="8992a-2295">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2295">2</span></span>

<span data-ttu-id="8992a-2296">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2296">3</span></span>

<span data-ttu-id="8992a-2297">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2297">4</span></span>

<span data-ttu-id="8992a-2298">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2298">5</span></span>

<span data-ttu-id="8992a-2299">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2299">6</span></span>

<span data-ttu-id="8992a-2300">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2300">7</span></span>

<span data-ttu-id="8992a-2301">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2301">8</span></span>

<span data-ttu-id="8992a-2302">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2302">9</span></span>

<span data-ttu-id="8992a-2303">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2303">3</span></span><br/> <span data-ttu-id="8992a-2304">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2304">0</span></span><br/>

<span data-ttu-id="8992a-2305">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2305">1</span></span>

<span data-ttu-id="8992a-2306">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="8992a-2306">CiTblChapt</span></span>

<span data-ttu-id="8992a-2307">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="8992a-2307">\_hRegion</span></span>

<span data-ttu-id="8992a-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="8992a-2308">\_cskip</span></span>



 

<span data-ttu-id="8992a-2309">**CiTblChapt**: intero senza segno a 32 bit che specifica il capitolo del set di righe da cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="8992a-2310">**\_ hRegion**: deve essere impostato su 0x00000000 e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="8992a-2311">**\_ cskip**: intero senza segno a 32 bit che rappresenta il numero di righe da ignorare nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="8992a-2312">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="8992a-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="8992a-2313">La struttura CRowsetProperties contiene le informazioni di configurazione per una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="8992a-2314">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2314">0</span></span>

<span data-ttu-id="8992a-2315">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2315">1</span></span>

<span data-ttu-id="8992a-2316">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2316">2</span></span>

<span data-ttu-id="8992a-2317">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2317">3</span></span>

<span data-ttu-id="8992a-2318">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2318">4</span></span>

<span data-ttu-id="8992a-2319">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2319">5</span></span>

<span data-ttu-id="8992a-2320">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2320">6</span></span>

<span data-ttu-id="8992a-2321">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2321">7</span></span>

<span data-ttu-id="8992a-2322">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2322">8</span></span>

<span data-ttu-id="8992a-2323">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2323">9</span></span>

<span data-ttu-id="8992a-2324">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2324">1</span></span><br/> <span data-ttu-id="8992a-2325">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2325">0</span></span><br/>

<span data-ttu-id="8992a-2326">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2326">1</span></span>

<span data-ttu-id="8992a-2327">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2327">2</span></span>

<span data-ttu-id="8992a-2328">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2328">3</span></span>

<span data-ttu-id="8992a-2329">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2329">4</span></span>

<span data-ttu-id="8992a-2330">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2330">5</span></span>

<span data-ttu-id="8992a-2331">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2331">6</span></span>

<span data-ttu-id="8992a-2332">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2332">7</span></span>

<span data-ttu-id="8992a-2333">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2333">8</span></span>

<span data-ttu-id="8992a-2334">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2334">9</span></span>

<span data-ttu-id="8992a-2335">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2335">2</span></span><br/> <span data-ttu-id="8992a-2336">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2336">0</span></span><br/>

<span data-ttu-id="8992a-2337">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2337">1</span></span>

<span data-ttu-id="8992a-2338">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2338">2</span></span>

<span data-ttu-id="8992a-2339">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2339">3</span></span>

<span data-ttu-id="8992a-2340">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2340">4</span></span>

<span data-ttu-id="8992a-2341">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2341">5</span></span>

<span data-ttu-id="8992a-2342">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2342">6</span></span>

<span data-ttu-id="8992a-2343">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2343">7</span></span>

<span data-ttu-id="8992a-2344">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2344">8</span></span>

<span data-ttu-id="8992a-2345">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2345">9</span></span>

<span data-ttu-id="8992a-2346">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2346">3</span></span><br/> <span data-ttu-id="8992a-2347">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2347">0</span></span><br/>

<span data-ttu-id="8992a-2348">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2348">1</span></span>

<span data-ttu-id="8992a-2349">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="8992a-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="8992a-2350">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="8992a-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="8992a-2351">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="8992a-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="8992a-2352">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="8992a-2352">\_cMaxResults</span></span>

<span data-ttu-id="8992a-2353">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="8992a-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="8992a-2354">**\_ uBooleanOptions**: i 3 bit meno significativi di questo campo devono contenere uno dei tre valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="8992a-2355">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-2355">Value</span></span>                  | <span data-ttu-id="8992a-2356">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8992a-2357">0x00000001 eSequential</span><span class="sxs-lookup"><span data-stu-id="8992a-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="8992a-2358">Il cursore può essere spostato solo in un altro passaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="8992a-2359">0x00000003 eLocatable</span><span class="sxs-lookup"><span data-stu-id="8992a-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="8992a-2360">È possibile spostare il cursore in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="8992a-2361">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8992a-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="8992a-2362">È possibile spostare il cursore in qualsiasi posizione e recuperarlo in qualsiasi direzione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="8992a-2363">I bit rimanenti possono essere cancellati o essere impostati in modo logico o combinato tra i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="8992a-2364">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-2364">Value</span></span>                     | <span data-ttu-id="8992a-2365">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-2366">0x00000008 eAsynchronous</span><span class="sxs-lookup"><span data-stu-id="8992a-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="8992a-2367">Il client non attende il completamento dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="8992a-2368">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="8992a-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="8992a-2369">Restituisce le prime righe rilevate, non le corrispondenze migliori.</span><span class="sxs-lookup"><span data-stu-id="8992a-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="8992a-2370">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="8992a-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="8992a-2371">Il server non deve eliminare righe finché il client non viene eseguito con una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="8992a-2372">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="8992a-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="8992a-2373">Il set di righe supporta i capitoli.</span><span class="sxs-lookup"><span data-stu-id="8992a-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="8992a-2374">0x00001000 eUseCI</span><span class="sxs-lookup"><span data-stu-id="8992a-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="8992a-2375">Rispondere solo alla query dall'indice, non al file system.</span><span class="sxs-lookup"><span data-stu-id="8992a-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="8992a-2376">0x00002000 eDeferTrimming</span><span class="sxs-lookup"><span data-stu-id="8992a-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="8992a-2377">Il servizio di indicizzazione consiste nel considerare l'ottimizzazione del tempo di risposta al client quando si esegue la rimozione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="8992a-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="8992a-2378">**\_ ulMaxOpenRows**: intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="8992a-2379">Deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="8992a-2380">Non usato e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="8992a-2381">**\_ ulMemoryUsage**: intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="8992a-2382">Deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="8992a-2383">Non usato e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="8992a-2384">**\_ cMaxResults**: un Unsigned Integer a 32 bit che specifica il numero massimo di righe da restituire per la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="8992a-2385">**\_ cCmdTimeout**: Unsigned Integer a 32 bit, che specifica il numero di secondi di timeout di una query e di interruzione automatica, dal momento che la query inizia l'esecuzione nel server.</span><span class="sxs-lookup"><span data-stu-id="8992a-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="8992a-2386">Il valore 0x00000000 indica che non è previsto il timeout della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="8992a-2387">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="8992a-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="8992a-2388">La struttura CRowVariant contiene la parte a dimensione fissa di un tipo di dati a lunghezza variabile archiviato nel messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="8992a-2389">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2389">0</span></span>

<span data-ttu-id="8992a-2390">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2390">1</span></span>

<span data-ttu-id="8992a-2391">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2391">2</span></span>

<span data-ttu-id="8992a-2392">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2392">3</span></span>

<span data-ttu-id="8992a-2393">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2393">4</span></span>

<span data-ttu-id="8992a-2394">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2394">5</span></span>

<span data-ttu-id="8992a-2395">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2395">6</span></span>

<span data-ttu-id="8992a-2396">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2396">7</span></span>

<span data-ttu-id="8992a-2397">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2397">8</span></span>

<span data-ttu-id="8992a-2398">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2398">9</span></span>

<span data-ttu-id="8992a-2399">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2399">1</span></span><br/> <span data-ttu-id="8992a-2400">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2400">0</span></span><br/>

<span data-ttu-id="8992a-2401">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2401">1</span></span>

<span data-ttu-id="8992a-2402">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2402">2</span></span>

<span data-ttu-id="8992a-2403">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2403">3</span></span>

<span data-ttu-id="8992a-2404">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2404">4</span></span>

<span data-ttu-id="8992a-2405">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2405">5</span></span>

<span data-ttu-id="8992a-2406">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2406">6</span></span>

<span data-ttu-id="8992a-2407">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2407">7</span></span>

<span data-ttu-id="8992a-2408">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2408">8</span></span>

<span data-ttu-id="8992a-2409">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2409">9</span></span>

<span data-ttu-id="8992a-2410">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2410">2</span></span><br/> <span data-ttu-id="8992a-2411">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2411">0</span></span><br/>

<span data-ttu-id="8992a-2412">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2412">1</span></span>

<span data-ttu-id="8992a-2413">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2413">2</span></span>

<span data-ttu-id="8992a-2414">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2414">3</span></span>

<span data-ttu-id="8992a-2415">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2415">4</span></span>

<span data-ttu-id="8992a-2416">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2416">5</span></span>

<span data-ttu-id="8992a-2417">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2417">6</span></span>

<span data-ttu-id="8992a-2418">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2418">7</span></span>

<span data-ttu-id="8992a-2419">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2419">8</span></span>

<span data-ttu-id="8992a-2420">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2420">9</span></span>

<span data-ttu-id="8992a-2421">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2421">3</span></span><br/> <span data-ttu-id="8992a-2422">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2422">0</span></span><br/>

<span data-ttu-id="8992a-2423">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2423">1</span></span>

<span data-ttu-id="8992a-2424">vType</span><span class="sxs-lookup"><span data-stu-id="8992a-2424">vType</span></span>

<span data-ttu-id="8992a-2425">Reserved1</span><span class="sxs-lookup"><span data-stu-id="8992a-2425">reserved1</span></span>

<span data-ttu-id="8992a-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="8992a-2426">reserved2</span></span>

<span data-ttu-id="8992a-2427">Offset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2427">Offset (optional)</span></span>



 

<span data-ttu-id="8992a-2428">**vType**: indicatore di tipo, che indica il tipo di vValue.</span><span class="sxs-lookup"><span data-stu-id="8992a-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="8992a-2429">DEVE essere uno dei valori VARENUM specificati nella sezione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="8992a-2430">**Reserved1**: non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="8992a-2431">Il valore può essere impostato su qualsiasi valore arbitrario ed è necessario ignorarlo alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="8992a-2432">**Reserved2**: non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="8992a-2433">Il valore può essere impostato su qualsiasi valore arbitrario ed è necessario ignorarlo alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="8992a-2434">**Offset**: offset ai dati a lunghezza variabile (ad esempio, una stringa).</span><span class="sxs-lookup"><span data-stu-id="8992a-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="8992a-2435">DEVE essere un valore a 32 bit (lungo 4 byte) se vengono usati offset a 32 bit (in base alle regole nella sezione 2.2.3.16) o un valore di 64 byte (lungo 8 byte) se vengono usati offset a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="8992a-2436">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="8992a-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="8992a-2437">La struttura CSortSet contiene l'ordinamento della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="8992a-2438">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2438">0</span></span>

<span data-ttu-id="8992a-2439">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2439">1</span></span>

<span data-ttu-id="8992a-2440">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2440">2</span></span>

<span data-ttu-id="8992a-2441">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2441">3</span></span>

<span data-ttu-id="8992a-2442">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2442">4</span></span>

<span data-ttu-id="8992a-2443">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2443">5</span></span>

<span data-ttu-id="8992a-2444">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2444">6</span></span>

<span data-ttu-id="8992a-2445">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2445">7</span></span>

<span data-ttu-id="8992a-2446">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2446">8</span></span>

<span data-ttu-id="8992a-2447">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2447">9</span></span>

<span data-ttu-id="8992a-2448">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2448">1</span></span><br/> <span data-ttu-id="8992a-2449">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2449">0</span></span><br/>

<span data-ttu-id="8992a-2450">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2450">1</span></span>

<span data-ttu-id="8992a-2451">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2451">2</span></span>

<span data-ttu-id="8992a-2452">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2452">3</span></span>

<span data-ttu-id="8992a-2453">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2453">4</span></span>

<span data-ttu-id="8992a-2454">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2454">5</span></span>

<span data-ttu-id="8992a-2455">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2455">6</span></span>

<span data-ttu-id="8992a-2456">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2456">7</span></span>

<span data-ttu-id="8992a-2457">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2457">8</span></span>

<span data-ttu-id="8992a-2458">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2458">9</span></span>

<span data-ttu-id="8992a-2459">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2459">2</span></span><br/> <span data-ttu-id="8992a-2460">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2460">0</span></span><br/>

<span data-ttu-id="8992a-2461">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2461">1</span></span>

<span data-ttu-id="8992a-2462">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2462">2</span></span>

<span data-ttu-id="8992a-2463">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2463">3</span></span>

<span data-ttu-id="8992a-2464">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2464">4</span></span>

<span data-ttu-id="8992a-2465">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2465">5</span></span>

<span data-ttu-id="8992a-2466">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2466">6</span></span>

<span data-ttu-id="8992a-2467">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2467">7</span></span>

<span data-ttu-id="8992a-2468">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2468">8</span></span>

<span data-ttu-id="8992a-2469">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2469">9</span></span>

<span data-ttu-id="8992a-2470">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2470">3</span></span><br/> <span data-ttu-id="8992a-2471">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2471">0</span></span><br/>

<span data-ttu-id="8992a-2472">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2472">1</span></span>

<span data-ttu-id="8992a-2473">Conteggio</span><span class="sxs-lookup"><span data-stu-id="8992a-2473">Count</span></span>

<span data-ttu-id="8992a-2474">sortArray (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="8992a-2475">**count**: un Unsigned Integer a 32 bit che specifica il numero di elementi in SortArray.</span><span class="sxs-lookup"><span data-stu-id="8992a-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="8992a-2476">**SortArray**: matrice di strutture CSort che descrive l'ordine in cui ordinare i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="8992a-2477">Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura disponga di un allineamento a 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="8992a-2478">Tali byte di riempimento possono essere qualsiasi valore arbitrario e devono essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="8992a-2479">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="8992a-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="8992a-2480">La struttura CTableColumn contiene una colonna di un messaggio CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="8992a-2481">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2481">0</span></span>

<span data-ttu-id="8992a-2482">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2482">1</span></span>

<span data-ttu-id="8992a-2483">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2483">2</span></span>

<span data-ttu-id="8992a-2484">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2484">3</span></span>

<span data-ttu-id="8992a-2485">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2485">4</span></span>

<span data-ttu-id="8992a-2486">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2486">5</span></span>

<span data-ttu-id="8992a-2487">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2487">6</span></span>

<span data-ttu-id="8992a-2488">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2488">7</span></span>

<span data-ttu-id="8992a-2489">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2489">8</span></span>

<span data-ttu-id="8992a-2490">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2490">9</span></span>

<span data-ttu-id="8992a-2491">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2491">1</span></span><br/> <span data-ttu-id="8992a-2492">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2492">0</span></span><br/>

<span data-ttu-id="8992a-2493">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2493">1</span></span>

<span data-ttu-id="8992a-2494">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2494">2</span></span>

<span data-ttu-id="8992a-2495">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2495">3</span></span>

<span data-ttu-id="8992a-2496">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2496">4</span></span>

<span data-ttu-id="8992a-2497">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2497">5</span></span>

<span data-ttu-id="8992a-2498">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2498">6</span></span>

<span data-ttu-id="8992a-2499">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2499">7</span></span>

<span data-ttu-id="8992a-2500">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2500">8</span></span>

<span data-ttu-id="8992a-2501">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2501">9</span></span>

<span data-ttu-id="8992a-2502">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2502">2</span></span><br/> <span data-ttu-id="8992a-2503">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2503">0</span></span><br/>

<span data-ttu-id="8992a-2504">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2504">1</span></span>

<span data-ttu-id="8992a-2505">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2505">2</span></span>

<span data-ttu-id="8992a-2506">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2506">3</span></span>

<span data-ttu-id="8992a-2507">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2507">4</span></span>

<span data-ttu-id="8992a-2508">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2508">5</span></span>

<span data-ttu-id="8992a-2509">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2509">6</span></span>

<span data-ttu-id="8992a-2510">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2510">7</span></span>

<span data-ttu-id="8992a-2511">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2511">8</span></span>

<span data-ttu-id="8992a-2512">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2512">9</span></span>

<span data-ttu-id="8992a-2513">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2513">3</span></span><br/> <span data-ttu-id="8992a-2514">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2514">0</span></span><br/>

<span data-ttu-id="8992a-2515">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2515">1</span></span>

<span data-ttu-id="8992a-2516">Campo PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="8992a-2516">PropSpec</span></span>

<span data-ttu-id="8992a-2517">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-2517">...(variable)</span></span>

<span data-ttu-id="8992a-2518">vType</span><span class="sxs-lookup"><span data-stu-id="8992a-2518">vType</span></span>

<span data-ttu-id="8992a-2519">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="8992a-2519">ValueUsed</span></span>

<span data-ttu-id="8992a-2520">\_padding1 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="8992a-2521">ValueOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="8992a-2522">ValueSize (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2522">ValueSize (optional)</span></span>

<span data-ttu-id="8992a-2523">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="8992a-2523">StatusUsed</span></span>

<span data-ttu-id="8992a-2524">\_padding2 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="8992a-2525">StatusOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="8992a-2526">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="8992a-2526">LengthUsed</span></span>

<span data-ttu-id="8992a-2527">\_padding3 (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="8992a-2528">LengthOffset (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="8992a-2529">**Campo PROPSPEC**: struttura CFullPropSpec come specificato nella sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="8992a-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="8992a-2530">**vType**: specifica il tipo di valore di dati contenuto nella colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="8992a-2531">Vedere il campo vType nella sezione 2.2.1.1 per l'elenco dei valori per questo campo.</span><span class="sxs-lookup"><span data-stu-id="8992a-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="8992a-2532">**ValueUsed**: campo a un byte che deve essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="8992a-2533">Se impostato su 0x01, la colonna viene trasferita all'interno della riga a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="8992a-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="8992a-2534">Se impostato su 0x00, il valore della colonna viene trasferito nella sezione a lunghezza variabile alla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="8992a-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="8992a-2535">**\_ padding1**: campo a un byte che deve essere inserito prima di ValueOffset se, senza di esso, ValueOffset non inizierà con un offset pari dall'inizio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="8992a-2536">Il valore di questo byte è arbitrario e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="8992a-2537">Se ValueUsed è impostato su 0x00, questo campo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8992a-2538">**ValueOffset**: intero senza segno a 2 byte che specifica l'offset del valore della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="8992a-2539">Se ValueUsed è impostato su 0x00, questo campo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8992a-2540">**ValueSize**: intero senza segno a 2 byte che specifica le dimensioni in byte del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="8992a-2541">Se ValueUsed è impostato su 0x00, questo campo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8992a-2542">**StatusUsed**: campo a un byte che deve essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="8992a-2543">Se impostato su 0x01, lo stato della colonna viene trasferito all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="8992a-2544">Se 0x00, lo stato della colonna non viene trasferito all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="8992a-2545">**\_ padding2**: campo a un byte che deve essere inserito prima di StatusOffset se, senza di esso, il campo StatusOffset non inizia con un offset pari dall'inizio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="8992a-2546">Il valore di questo byte è arbitrario e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="8992a-2547">Se StatusUsed è impostato su 0x00, questo campo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8992a-2548">**StatusOffset**: intero senza segno a 2 byte che specifica l'offset dello stato della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="8992a-2549">Se StatusUsed è impostato su 0x00, questo campo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8992a-2550">**LengthUsed**: campo a un byte che deve essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="8992a-2551">Se impostato su 0x01, la lunghezza della colonna viene trasferita all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="8992a-2552">Se 0x00, la lunghezza della colonna non deve essere trasferita all'interno della riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="8992a-2553">**\_ padding3**: campo a un byte che deve essere inserito prima di LengthOffset se, senza di esso, LengthOffset non inizierà con un offset pari dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="8992a-2554">Il valore di questo byte è arbitrario e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="8992a-2555">Se LengthUsed è impostato su 0x00, questo campo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8992a-2556">**LengthOffset**: intero senza segno a 2 byte che specifica l'offset della lunghezza della colonna nella riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="8992a-2557">Se LengthUsed è impostato su 0x00, questo campo non deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="8992a-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="8992a-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="8992a-2559">La struttura SERIALIZEDPROPERTYVALUE contiene un valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="8992a-2560">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2560">0</span></span>

<span data-ttu-id="8992a-2561">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2561">1</span></span>

<span data-ttu-id="8992a-2562">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2562">2</span></span>

<span data-ttu-id="8992a-2563">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2563">3</span></span>

<span data-ttu-id="8992a-2564">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2564">4</span></span>

<span data-ttu-id="8992a-2565">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2565">5</span></span>

<span data-ttu-id="8992a-2566">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2566">6</span></span>

<span data-ttu-id="8992a-2567">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2567">7</span></span>

<span data-ttu-id="8992a-2568">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2568">8</span></span>

<span data-ttu-id="8992a-2569">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2569">9</span></span>

<span data-ttu-id="8992a-2570">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2570">1</span></span><br/> <span data-ttu-id="8992a-2571">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2571">0</span></span><br/>

<span data-ttu-id="8992a-2572">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2572">1</span></span>

<span data-ttu-id="8992a-2573">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2573">2</span></span>

<span data-ttu-id="8992a-2574">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2574">3</span></span>

<span data-ttu-id="8992a-2575">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2575">4</span></span>

<span data-ttu-id="8992a-2576">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2576">5</span></span>

<span data-ttu-id="8992a-2577">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2577">6</span></span>

<span data-ttu-id="8992a-2578">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2578">7</span></span>

<span data-ttu-id="8992a-2579">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2579">8</span></span>

<span data-ttu-id="8992a-2580">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2580">9</span></span>

<span data-ttu-id="8992a-2581">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2581">2</span></span><br/> <span data-ttu-id="8992a-2582">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2582">0</span></span><br/>

<span data-ttu-id="8992a-2583">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2583">1</span></span>

<span data-ttu-id="8992a-2584">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2584">2</span></span>

<span data-ttu-id="8992a-2585">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2585">3</span></span>

<span data-ttu-id="8992a-2586">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2586">4</span></span>

<span data-ttu-id="8992a-2587">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2587">5</span></span>

<span data-ttu-id="8992a-2588">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2588">6</span></span>

<span data-ttu-id="8992a-2589">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2589">7</span></span>

<span data-ttu-id="8992a-2590">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2590">8</span></span>

<span data-ttu-id="8992a-2591">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2591">9</span></span>

<span data-ttu-id="8992a-2592">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2592">3</span></span><br/> <span data-ttu-id="8992a-2593">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2593">0</span></span><br/>

<span data-ttu-id="8992a-2594">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2594">1</span></span>

<span data-ttu-id="8992a-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="8992a-2595">dwType</span></span>

<span data-ttu-id="8992a-2596">RGB (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-2596">rgb (variable)</span></span>



 

<span data-ttu-id="8992a-2597">**dwType**: uno dei tipi Variant, definito nella sezione 2.2.1.1, che può essere combinato con modificatori di tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="8992a-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="8992a-2598">Per tutti i tipi Variant, ad eccezione di quelli combinati con \_ la matrice VT, SERIALIZEDPROPERTYVALUE ha lo stesso layout di CBaseStorageVariant, come specificato nella sezione 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="8992a-2599">Se il tipo Variant è combinato con il \_ modificatore di tipo matrice VT, viene usato SAFEARRAY2, specificato nella sezione 2.2.1.2.1.1, anziché SAFEARRAY nel campo vValue di CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="8992a-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="8992a-2600">**RGB**: valore serializzato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="8992a-2601">Vedere i dettagli della serializzazione per vValue in 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="8992a-2602">2.2.2 intestazioni di messaggio</span><span class="sxs-lookup"><span data-stu-id="8992a-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="8992a-2603">Tutti i messaggi del protocollo del servizio di indicizzazione del contenuto hanno un'intestazione di 16 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="8992a-2604">Di seguito è riportato un diagramma che mostra il formato dell'intestazione del messaggio protocollo del servizio di indicizzazione contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="8992a-2605">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2605">0</span></span>

<span data-ttu-id="8992a-2606">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2606">1</span></span>

<span data-ttu-id="8992a-2607">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2607">2</span></span>

<span data-ttu-id="8992a-2608">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2608">3</span></span>

<span data-ttu-id="8992a-2609">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2609">4</span></span>

<span data-ttu-id="8992a-2610">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2610">5</span></span>

<span data-ttu-id="8992a-2611">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2611">6</span></span>

<span data-ttu-id="8992a-2612">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2612">7</span></span>

<span data-ttu-id="8992a-2613">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2613">8</span></span>

<span data-ttu-id="8992a-2614">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2614">9</span></span>

<span data-ttu-id="8992a-2615">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2615">1</span></span><br/> <span data-ttu-id="8992a-2616">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2616">0</span></span><br/>

<span data-ttu-id="8992a-2617">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2617">1</span></span>

<span data-ttu-id="8992a-2618">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2618">2</span></span>

<span data-ttu-id="8992a-2619">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2619">3</span></span>

<span data-ttu-id="8992a-2620">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2620">4</span></span>

<span data-ttu-id="8992a-2621">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2621">5</span></span>

<span data-ttu-id="8992a-2622">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2622">6</span></span>

<span data-ttu-id="8992a-2623">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2623">7</span></span>

<span data-ttu-id="8992a-2624">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2624">8</span></span>

<span data-ttu-id="8992a-2625">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2625">9</span></span>

<span data-ttu-id="8992a-2626">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2626">2</span></span><br/> <span data-ttu-id="8992a-2627">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2627">0</span></span><br/>

<span data-ttu-id="8992a-2628">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2628">1</span></span>

<span data-ttu-id="8992a-2629">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2629">2</span></span>

<span data-ttu-id="8992a-2630">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2630">3</span></span>

<span data-ttu-id="8992a-2631">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2631">4</span></span>

<span data-ttu-id="8992a-2632">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2632">5</span></span>

<span data-ttu-id="8992a-2633">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2633">6</span></span>

<span data-ttu-id="8992a-2634">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2634">7</span></span>

<span data-ttu-id="8992a-2635">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2635">8</span></span>

<span data-ttu-id="8992a-2636">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2636">9</span></span>

<span data-ttu-id="8992a-2637">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2637">3</span></span><br/> <span data-ttu-id="8992a-2638">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2638">0</span></span><br/>

<span data-ttu-id="8992a-2639">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2639">1</span></span>

<span data-ttu-id="8992a-2640">\_messaggio</span><span class="sxs-lookup"><span data-stu-id="8992a-2640">\_msg</span></span>

<span data-ttu-id="8992a-2641">\_stato</span><span class="sxs-lookup"><span data-stu-id="8992a-2641">\_status</span></span>

<span data-ttu-id="8992a-2642">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="8992a-2642">\_ulChecksum</span></span>

<span data-ttu-id="8992a-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="8992a-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="8992a-2644">\_**msg**: intero A 32 bit che identifica il tipo di messaggio dopo l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="8992a-2645">Nella tabella seguente sono elencati i messaggi del protocollo del servizio di indicizzazione del contenuto e i valori integer specificati per ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="8992a-2646">Come illustrato nella tabella, alcuni valori identificano 2 messaggi nella tabella.</span><span class="sxs-lookup"><span data-stu-id="8992a-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="8992a-2647">In tali istanze il messaggio che segue l'intestazione può essere identificato dalla direzione del flusso di messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="8992a-2648">Se la direzione è da client a server, viene indicato il messaggio con "in" aggiunto al nome del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="8992a-2649">Se la direzione è da server a client, viene indicato il messaggio con "out" aggiunto al nome del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="8992a-2650">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-2650">Value</span></span>      | <span data-ttu-id="8992a-2651">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="8992a-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="8992a-2652">0x000000C8</span></span> | <span data-ttu-id="8992a-2653">CPMConnectIn o CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="8992a-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="8992a-2654">0x000000C9</span></span> | <span data-ttu-id="8992a-2655">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="8992a-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="8992a-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="8992a-2656">0x000000CA</span></span> | <span data-ttu-id="8992a-2657">CPMCreateQueryIn o CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="8992a-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="8992a-2658">0x000000CB</span></span> | <span data-ttu-id="8992a-2659">CPMFreeCursorIn o CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="8992a-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="8992a-2660">0x000000CC</span></span> | <span data-ttu-id="8992a-2661">CPMGetRowsIn o CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="8992a-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="8992a-2662">0x000000CD</span></span> | <span data-ttu-id="8992a-2663">CPMRatioFinishedIn o CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="8992a-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="8992a-2664">0x000000CE</span></span> | <span data-ttu-id="8992a-2665">CPMCompareBmkIn o CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="8992a-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="8992a-2666">0x000000CF</span></span> | <span data-ttu-id="8992a-2667">CPMGetApproximatePositionIn o CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="8992a-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="8992a-2668">0x000000D0</span></span> | <span data-ttu-id="8992a-2669">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="8992a-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="8992a-2670">0x000000D1</span></span> | <span data-ttu-id="8992a-2671">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="8992a-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="8992a-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="8992a-2672">0x000000D2</span></span> | <span data-ttu-id="8992a-2673">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="8992a-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="8992a-2674">0x000000D7</span></span> | <span data-ttu-id="8992a-2675">CPMGetQueryStatusIn o CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="8992a-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="8992a-2676">0x000000D9</span></span> | <span data-ttu-id="8992a-2677">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="8992a-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="8992a-2678">0x000000E1</span></span> | <span data-ttu-id="8992a-2679">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="8992a-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="8992a-2680">0x000000E4</span></span> | <span data-ttu-id="8992a-2681">CPMFetchValueIn o CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="8992a-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="8992a-2682">0x000000E6</span></span> | <span data-ttu-id="8992a-2683">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="8992a-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="8992a-2684">0x000000E7</span></span> | <span data-ttu-id="8992a-2685">CPMGetQueryStatusExIn o PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="8992a-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="8992a-2686">0x000000E8</span></span> | <span data-ttu-id="8992a-2687">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="8992a-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="8992a-2688">0x000000E9</span></span> | <span data-ttu-id="8992a-2689">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="8992a-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="8992a-2690">0x000000EC</span></span> | <span data-ttu-id="8992a-2691">CPMSetCatStateIn o CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="8992a-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="8992a-2692">\_**stato**: HRESULT \[ ms-sys \] , che indica lo stato dell'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="8992a-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="8992a-2693">*Comportamento di Windows: il client imposta sempre il \_ campo stato su 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="8992a-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="8992a-2694">**\_ ulChecksum**: \_ ulChecksum deve essere calcolato come specificato nella sezione 3.2.4 per i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="8992a-2695">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="8992a-2696">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="8992a-2697">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="8992a-2698">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="8992a-2699">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="8992a-2700">Per tutti gli altri messaggi, \_ ULCHECKSUM deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="8992a-2701">Un client deve ignorare il \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="8992a-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="8992a-2702">**\_ ulReserved2**: deve essere impostato su 0 e ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="8992a-2703">2.2.3 messaggi</span><span class="sxs-lookup"><span data-stu-id="8992a-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="8992a-2704">CPMCiStateInOut 2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="8992a-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="8992a-2705">Il messaggio CPMCiStateInOut contiene informazioni sullo stato del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="8992a-2706">Il formato del messaggio CPMCiStateInOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-2707">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2707">0</span></span>

<span data-ttu-id="8992a-2708">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2708">1</span></span>

<span data-ttu-id="8992a-2709">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2709">2</span></span>

<span data-ttu-id="8992a-2710">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2710">3</span></span>

<span data-ttu-id="8992a-2711">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2711">4</span></span>

<span data-ttu-id="8992a-2712">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2712">5</span></span>

<span data-ttu-id="8992a-2713">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2713">6</span></span>

<span data-ttu-id="8992a-2714">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2714">7</span></span>

<span data-ttu-id="8992a-2715">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2715">8</span></span>

<span data-ttu-id="8992a-2716">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2716">9</span></span>

<span data-ttu-id="8992a-2717">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2717">1</span></span><br/> <span data-ttu-id="8992a-2718">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2718">0</span></span><br/>

<span data-ttu-id="8992a-2719">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2719">1</span></span>

<span data-ttu-id="8992a-2720">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2720">2</span></span>

<span data-ttu-id="8992a-2721">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2721">3</span></span>

<span data-ttu-id="8992a-2722">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2722">4</span></span>

<span data-ttu-id="8992a-2723">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2723">5</span></span>

<span data-ttu-id="8992a-2724">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2724">6</span></span>

<span data-ttu-id="8992a-2725">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2725">7</span></span>

<span data-ttu-id="8992a-2726">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2726">8</span></span>

<span data-ttu-id="8992a-2727">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2727">9</span></span>

<span data-ttu-id="8992a-2728">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2728">2</span></span><br/> <span data-ttu-id="8992a-2729">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2729">0</span></span><br/>

<span data-ttu-id="8992a-2730">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2730">1</span></span>

<span data-ttu-id="8992a-2731">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2731">2</span></span>

<span data-ttu-id="8992a-2732">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2732">3</span></span>

<span data-ttu-id="8992a-2733">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2733">4</span></span>

<span data-ttu-id="8992a-2734">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2734">5</span></span>

<span data-ttu-id="8992a-2735">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2735">6</span></span>

<span data-ttu-id="8992a-2736">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2736">7</span></span>

<span data-ttu-id="8992a-2737">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2737">8</span></span>

<span data-ttu-id="8992a-2738">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2738">9</span></span>

<span data-ttu-id="8992a-2739">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2739">3</span></span><br/> <span data-ttu-id="8992a-2740">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2740">0</span></span><br/>

<span data-ttu-id="8992a-2741">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2741">1</span></span>

<span data-ttu-id="8992a-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="8992a-2742">cbStruct</span></span>

<span data-ttu-id="8992a-2743">cWordList</span><span class="sxs-lookup"><span data-stu-id="8992a-2743">cWordList</span></span>

<span data-ttu-id="8992a-2744">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="8992a-2744">cPersistentIndex</span></span>

<span data-ttu-id="8992a-2745">cQueries</span><span class="sxs-lookup"><span data-stu-id="8992a-2745">cQueries</span></span>

<span data-ttu-id="8992a-2746">cDocuments</span><span class="sxs-lookup"><span data-stu-id="8992a-2746">cDocuments</span></span>

<span data-ttu-id="8992a-2747">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="8992a-2747">cFreshTest</span></span>

<span data-ttu-id="8992a-2748">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="8992a-2748">dwMergeProgress</span></span>

<span data-ttu-id="8992a-2749">Area</span><span class="sxs-lookup"><span data-stu-id="8992a-2749">eState</span></span>

<span data-ttu-id="8992a-2750">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="8992a-2750">cFilteredDocuments</span></span>

<span data-ttu-id="8992a-2751">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="8992a-2751">cTotalDocuments</span></span>

<span data-ttu-id="8992a-2752">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="8992a-2752">cPendingScans</span></span>

<span data-ttu-id="8992a-2753">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="8992a-2753">dwIndexSize</span></span>

<span data-ttu-id="8992a-2754">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="8992a-2754">cUniqueKeys</span></span>

<span data-ttu-id="8992a-2755">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="8992a-2755">cSecQDocuments</span></span>

<span data-ttu-id="8992a-2756">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="8992a-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="8992a-2757">**cbStruct**: Unsigned Integer A 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8992a-2758">Dimensioni in byte di questo messaggio (esclusa l'intestazione comune).</span><span class="sxs-lookup"><span data-stu-id="8992a-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="8992a-2759">DEVE essere impostato su 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="8992a-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="8992a-2760">**cWordList**: Unsigned Integer A 32 bit che indica il numero di indici iniziali creati per i documenti indicizzati di recente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="8992a-2761">**cPersistentIndex**: Unsigned Integer A 32 bit che indica il numero di indici permanenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="8992a-2762">**cQueries**: un Unsigned Integer a 32 bit che indica una serie di query attivamente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="8992a-2763">**CDocuments**: Unsigned Integer a 32 bit che indica il numero totale di documenti in attesa di essere indicizzati.</span><span class="sxs-lookup"><span data-stu-id="8992a-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="8992a-2764">**cFreshTest**: un Unsigned Integer a 32 bit che indica il numero di documenti univoci con informazioni negli indici che non sono completamente ottimizzati per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8992a-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="8992a-2765">**dwMergeProgress**: intero senza segno a 32 bit che specifica la percentuale di completamento dell'ottimizzazione completa corrente degli indici, se è attualmente in corso l'ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="8992a-2766">DEVE essere minore o uguale a 100.</span><span class="sxs-lookup"><span data-stu-id="8992a-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="8992a-2767">**estate**: stato dell'indicizzazione del contenuto fornito da una o più costanti di \_ stato ci \_ \* , definite nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8992a-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="8992a-2768">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-2768">Value</span></span>                                         | <span data-ttu-id="8992a-2769">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-2770">\_ \_ 0x00000001 Unione Shadow dello stato ci \_</span><span class="sxs-lookup"><span data-stu-id="8992a-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="8992a-2771">Il servizio di indicizzazione è in corso di ottimizzazione di alcuni indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8992a-2772">\_ \_ Unione 0x00000002 Master stati ci \_</span><span class="sxs-lookup"><span data-stu-id="8992a-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="8992a-2773">Il servizio di indicizzazione è nel processo di ottimizzazione completa per tutti gli indici.</span><span class="sxs-lookup"><span data-stu-id="8992a-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8992a-2774">\_Analisi del contenuto dello stato ci \_ \_ \_ obbligatoria 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8992a-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="8992a-2775">Alcuni documenti nell'indice sono stati modificati e il servizio di indicizzazione deve determinare quali sono stati aggiunti, modificati o eliminati.</span><span class="sxs-lookup"><span data-stu-id="8992a-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8992a-2776">\_Stati \_ Uniti che annealing \_ merge 0x00000008</span><span class="sxs-lookup"><span data-stu-id="8992a-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="8992a-2777">Il servizio di indicizzazione è in corso di ottimizzazione degli indici per ridurre l'utilizzo della memoria e migliorare le prestazioni delle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="8992a-2778">Questo processo è più completo rispetto a quello identificato dal valore di \_ merge Shadow dello stato ci \_ \_ , ma non è completo come specificato dal \_ valore di unione master dello stato ci \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8992a-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="8992a-2779">Queste ottimizzazioni sono specifiche dell'implementazione perché dipendono dal modo in cui i dati vengono archiviati internamente; le ottimizzazioni non influiscono sul protocollo in alcun modo diverso dal tempo di risposta.</span><span class="sxs-lookup"><span data-stu-id="8992a-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="8992a-2780">\_0x00000010 di analisi dello stato ci \_</span><span class="sxs-lookup"><span data-stu-id="8992a-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="8992a-2781">Il servizio di indicizzazione sta esaminando una directory o un set di directory per verificare se i file sono stati aggiunti, eliminati o aggiornati dall'ultima volta che la directory è stata indicizzata.</span><span class="sxs-lookup"><span data-stu-id="8992a-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8992a-2782">\_Ripristino dello stato ci \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="8992a-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="8992a-2783">Il servizio è stato avviato dall'ultimo stato salvato ed è in corso di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8992a-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8992a-2784">Stato CI- \_ \_ memoria insufficiente \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="8992a-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="8992a-2785">La maggior parte della memoria virtuale del server è in uso.</span><span class="sxs-lookup"><span data-stu-id="8992a-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8992a-2786">I/o \_ elevato stato ci \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="8992a-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="8992a-2787">Il livello di attività di I/O (input/output) sul server è relativamente elevato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8992a-2788">\_ \_ Unione principale stato \_ ci \_ sospeso 0x00000200</span><span class="sxs-lookup"><span data-stu-id="8992a-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="8992a-2789">Il processo di ottimizzazione completa per tutti gli indici in corso è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="8992a-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="8992a-2790">Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8992a-2791">Stato CI di \_ \_ sola lettura \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="8992a-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="8992a-2792">La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="8992a-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="8992a-2793">Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8992a-2794">\_0x00000800 di \_ alimentazione della batteria a stati ci \_</span><span class="sxs-lookup"><span data-stu-id="8992a-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="8992a-2795">La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa per conservare la durata della batteria, ma comunque risponde alle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="8992a-2796">Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8992a-2797">\_Utente stato \_ ci \_ attivo 0x00001000</span><span class="sxs-lookup"><span data-stu-id="8992a-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="8992a-2798">La parte del servizio di indicizzazione che preleva nuovi documenti da indicizzare è stata sospesa a causa di un'attività elevata da parte dell'utente (tastiera o mouse) ma risponde comunque alle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="8992a-2799">Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="8992a-2800">\_Stato ci \_ iniziale 0x00002000</span><span class="sxs-lookup"><span data-stu-id="8992a-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="8992a-2801">Il servizio è in fase di avvio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2801">The service is starting.</span></span> <span data-ttu-id="8992a-2802">È possibile eseguire le query, ma l'analisi e la notifica non sono ancora state abilitate.</span><span class="sxs-lookup"><span data-stu-id="8992a-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="8992a-2803">Questa operazione viene fornita solo a scopo informativo e non influisce su CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="8992a-2804">Stato CI che \_ \_ legge \_ USNS 0x00004000</span><span class="sxs-lookup"><span data-stu-id="8992a-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="8992a-2805">Il servizio non ha letto il log mantenuto dal file system per tenere traccia delle modifiche apportate ai file o alle directory in un volume, pertanto l'indice potrebbe non essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="8992a-2806">**cFilteredDocuments**: Unsigned Integer A 32 bit che indica il numero di documenti indicizzati dall'inizio dell'indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="8992a-2807">**cTotalDocuments**: Unsigned Integer a 32 bit che indica il numero totale di documenti presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="8992a-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="8992a-2808">**cPendingScans**: Unsigned Integer A 32 bit che indica il numero di operazioni di indicizzazione di alto livello in sospeso.</span><span class="sxs-lookup"><span data-stu-id="8992a-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="8992a-2809">Il significato di questo valore è specifico del provider, ma sono previsti numeri maggiori per indicare che l'indicizzazione rimane maggiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="8992a-2810">*Comportamento di Windows*: questo valore è in genere zero, tranne che subito dopo l'avvio dell'indicizzazione o dopo l'overflow di una coda di notifica.</span><span class="sxs-lookup"><span data-stu-id="8992a-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="8992a-2811">**dwIndexSize**: un Unsigned Integer a 32 bit che indica le dimensioni, in megabyte, dell'indice (esclusa la cache delle proprietà).</span><span class="sxs-lookup"><span data-stu-id="8992a-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="8992a-2812">**cUniqueKeys**: Unsigned Integer a 32 bit che indica il numero approssimativo di chiavi univoche nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="8992a-2813">**cSecQDocuments**: un Unsigned Integer a 32 bit che indica il numero di documenti che il servizio di indicizzazione tenterà di eseguire di nuovo l'indicizzazione a causa di un errore durante il tentativo di indicizzazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="8992a-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="8992a-2814">**dwPropCacheSize**: un Unsigned Integer a 32 bit che indica le dimensioni, in megabyte, della cache delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="8992a-2815">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="8992a-2816">Il messaggio CPMSetCatStateIn imposta lo stato di un catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="8992a-2817">Il formato del messaggio CPMSetCatStateIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-2818">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2818">0</span></span>

<span data-ttu-id="8992a-2819">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2819">1</span></span>

<span data-ttu-id="8992a-2820">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2820">2</span></span>

<span data-ttu-id="8992a-2821">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2821">3</span></span>

<span data-ttu-id="8992a-2822">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2822">4</span></span>

<span data-ttu-id="8992a-2823">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2823">5</span></span>

<span data-ttu-id="8992a-2824">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2824">6</span></span>

<span data-ttu-id="8992a-2825">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2825">7</span></span>

<span data-ttu-id="8992a-2826">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2826">8</span></span>

<span data-ttu-id="8992a-2827">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2827">9</span></span>

<span data-ttu-id="8992a-2828">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2828">1</span></span><br/> <span data-ttu-id="8992a-2829">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2829">0</span></span><br/>

<span data-ttu-id="8992a-2830">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2830">1</span></span>

<span data-ttu-id="8992a-2831">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2831">2</span></span>

<span data-ttu-id="8992a-2832">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2832">3</span></span>

<span data-ttu-id="8992a-2833">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2833">4</span></span>

<span data-ttu-id="8992a-2834">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2834">5</span></span>

<span data-ttu-id="8992a-2835">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2835">6</span></span>

<span data-ttu-id="8992a-2836">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2836">7</span></span>

<span data-ttu-id="8992a-2837">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2837">8</span></span>

<span data-ttu-id="8992a-2838">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2838">9</span></span>

<span data-ttu-id="8992a-2839">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2839">2</span></span><br/> <span data-ttu-id="8992a-2840">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2840">0</span></span><br/>

<span data-ttu-id="8992a-2841">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2841">1</span></span>

<span data-ttu-id="8992a-2842">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2842">2</span></span>

<span data-ttu-id="8992a-2843">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2843">3</span></span>

<span data-ttu-id="8992a-2844">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2844">4</span></span>

<span data-ttu-id="8992a-2845">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2845">5</span></span>

<span data-ttu-id="8992a-2846">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2846">6</span></span>

<span data-ttu-id="8992a-2847">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2847">7</span></span>

<span data-ttu-id="8992a-2848">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2848">8</span></span>

<span data-ttu-id="8992a-2849">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2849">9</span></span>

<span data-ttu-id="8992a-2850">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2850">3</span></span><br/> <span data-ttu-id="8992a-2851">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2851">0</span></span><br/>

<span data-ttu-id="8992a-2852">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2852">1</span></span>

<span data-ttu-id="8992a-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="8992a-2853">\_partID</span></span>

<span data-ttu-id="8992a-2854">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="8992a-2854">\_dwNewState</span></span>

<span data-ttu-id="8992a-2855">\_CatName (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="8992a-2856">**\_ partID**: deve essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="8992a-2857">**\_ dwNewState**: deve essere impostato su uno dei valori seguenti, che indica il nuovo stato del catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="8992a-2858">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-2858">Value</span></span>                         | <span data-ttu-id="8992a-2859">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-2860">CICAT \_ arrestato 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="8992a-2861">Il catalogo è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2861">The catalog is stopped.</span></span> <span data-ttu-id="8992a-2862">Questo stato indica che non è necessario indicizzare nuovi file e che non devono essere elaborate query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="8992a-2863">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="8992a-2864">Il catalogo è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8992a-2864">The catalog is read-only.</span></span> <span data-ttu-id="8992a-2865">Non è necessario indicizzare nuovi file.</span><span class="sxs-lookup"><span data-stu-id="8992a-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="8992a-2866">\_0x00000004 scrivibile CICAT</span><span class="sxs-lookup"><span data-stu-id="8992a-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="8992a-2867">Il catalogo è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="8992a-2867">The catalog is writable.</span></span> <span data-ttu-id="8992a-2868">I nuovi file possono essere indicizzati e le query di ricerca devono essere elaborate.</span><span class="sxs-lookup"><span data-stu-id="8992a-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="8992a-2869">CICAT \_ senza \_ 0x00000008 di query</span><span class="sxs-lookup"><span data-stu-id="8992a-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="8992a-2870">Il catalogo non è disponibile per le query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="8992a-2871">CICAT \_ ottenere \_ lo stato 0x00000010</span><span class="sxs-lookup"><span data-stu-id="8992a-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="8992a-2872">Lo stato del catalogo non deve essere modificato, ma solo recuperato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="8992a-2873">CICAT \_ tutti \_ 0x00000020 aperti</span><span class="sxs-lookup"><span data-stu-id="8992a-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="8992a-2874">Un controllo per verificare se tutti i cataloghi sono stati avviati.</span><span class="sxs-lookup"><span data-stu-id="8992a-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="8992a-2875">In tal caso, il \_ campo dwOldState inviato nella risposta CPMSetCatStateOut a questo messaggio verrà segnalato come diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8992a-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="8992a-2876">**\_ CatName**: nome del catalogo per cui viene modificato lo stato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="8992a-2877">Il nome deve essere una stringa Unicode con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="8992a-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="8992a-2878">Se \_ dwNewState è impostato su CICAT \_ tutti aperti, questo campo deve essere omesso \_ .</span><span class="sxs-lookup"><span data-stu-id="8992a-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="8992a-2879">CPMSetCatStateOut 2.2.3.3</span><span class="sxs-lookup"><span data-stu-id="8992a-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="8992a-2880">Il messaggio CPMSetCatStateOut è una risposta a un messaggio CPMSetCatStateIn con lo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="8992a-2881">Il formato del messaggio CPMSetCatStateOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-2882">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2882">0</span></span>

<span data-ttu-id="8992a-2883">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2883">1</span></span>

<span data-ttu-id="8992a-2884">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2884">2</span></span>

<span data-ttu-id="8992a-2885">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2885">3</span></span>

<span data-ttu-id="8992a-2886">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2886">4</span></span>

<span data-ttu-id="8992a-2887">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2887">5</span></span>

<span data-ttu-id="8992a-2888">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2888">6</span></span>

<span data-ttu-id="8992a-2889">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2889">7</span></span>

<span data-ttu-id="8992a-2890">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2890">8</span></span>

<span data-ttu-id="8992a-2891">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2891">9</span></span>

<span data-ttu-id="8992a-2892">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2892">1</span></span><br/> <span data-ttu-id="8992a-2893">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2893">0</span></span><br/>

<span data-ttu-id="8992a-2894">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2894">1</span></span>

<span data-ttu-id="8992a-2895">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2895">2</span></span>

<span data-ttu-id="8992a-2896">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2896">3</span></span>

<span data-ttu-id="8992a-2897">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2897">4</span></span>

<span data-ttu-id="8992a-2898">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2898">5</span></span>

<span data-ttu-id="8992a-2899">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2899">6</span></span>

<span data-ttu-id="8992a-2900">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2900">7</span></span>

<span data-ttu-id="8992a-2901">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2901">8</span></span>

<span data-ttu-id="8992a-2902">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2902">9</span></span>

<span data-ttu-id="8992a-2903">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2903">2</span></span><br/> <span data-ttu-id="8992a-2904">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2904">0</span></span><br/>

<span data-ttu-id="8992a-2905">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2905">1</span></span>

<span data-ttu-id="8992a-2906">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2906">2</span></span>

<span data-ttu-id="8992a-2907">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2907">3</span></span>

<span data-ttu-id="8992a-2908">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2908">4</span></span>

<span data-ttu-id="8992a-2909">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2909">5</span></span>

<span data-ttu-id="8992a-2910">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2910">6</span></span>

<span data-ttu-id="8992a-2911">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2911">7</span></span>

<span data-ttu-id="8992a-2912">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2912">8</span></span>

<span data-ttu-id="8992a-2913">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2913">9</span></span>

<span data-ttu-id="8992a-2914">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2914">3</span></span><br/> <span data-ttu-id="8992a-2915">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2915">0</span></span><br/>

<span data-ttu-id="8992a-2916">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2916">1</span></span>

<span data-ttu-id="8992a-2917">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="8992a-2917">\_dwOldState</span></span>



 

<span data-ttu-id="8992a-2918">**\_ dwOldState**: uno dei valori seguenti, che indica lo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="8992a-2919">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-2919">Value</span></span>                       | <span data-ttu-id="8992a-2920">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="8992a-2921">CICAT \_ arrestato 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="8992a-2922">Il catalogo è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="8992a-2923">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="8992a-2924">Il catalogo è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8992a-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="8992a-2925">\_0x00000004 scrivibile CICAT</span><span class="sxs-lookup"><span data-stu-id="8992a-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="8992a-2926">Il catalogo è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="8992a-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="8992a-2927">CICAT \_ senza \_ 0x00000008 di query</span><span class="sxs-lookup"><span data-stu-id="8992a-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="8992a-2928">Il catalogo non è disponibile per le query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="8992a-2929">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="8992a-2930">Il messaggio CPMUpdateDocumentsIn indica al server di indicizzare il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="8992a-2931">Il server risponderà con l'intestazione del messaggio del messaggio CPMUpdateDocumentsOut, con i risultati della richiesta contenuti nel \_ campo stato dell'intestazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="8992a-2932">Il formato del messaggio CPMUpdateDocumentsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-2933">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2933">0</span></span>

<span data-ttu-id="8992a-2934">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2934">1</span></span>

<span data-ttu-id="8992a-2935">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2935">2</span></span>

<span data-ttu-id="8992a-2936">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2936">3</span></span>

<span data-ttu-id="8992a-2937">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2937">4</span></span>

<span data-ttu-id="8992a-2938">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2938">5</span></span>

<span data-ttu-id="8992a-2939">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2939">6</span></span>

<span data-ttu-id="8992a-2940">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2940">7</span></span>

<span data-ttu-id="8992a-2941">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2941">8</span></span>

<span data-ttu-id="8992a-2942">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2942">9</span></span>

<span data-ttu-id="8992a-2943">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2943">1</span></span><br/> <span data-ttu-id="8992a-2944">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2944">0</span></span><br/>

<span data-ttu-id="8992a-2945">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2945">1</span></span>

<span data-ttu-id="8992a-2946">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2946">2</span></span>

<span data-ttu-id="8992a-2947">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2947">3</span></span>

<span data-ttu-id="8992a-2948">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2948">4</span></span>

<span data-ttu-id="8992a-2949">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2949">5</span></span>

<span data-ttu-id="8992a-2950">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2950">6</span></span>

<span data-ttu-id="8992a-2951">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2951">7</span></span>

<span data-ttu-id="8992a-2952">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2952">8</span></span>

<span data-ttu-id="8992a-2953">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2953">9</span></span>

<span data-ttu-id="8992a-2954">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2954">2</span></span><br/> <span data-ttu-id="8992a-2955">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2955">0</span></span><br/>

<span data-ttu-id="8992a-2956">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2956">1</span></span>

<span data-ttu-id="8992a-2957">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2957">2</span></span>

<span data-ttu-id="8992a-2958">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2958">3</span></span>

<span data-ttu-id="8992a-2959">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2959">4</span></span>

<span data-ttu-id="8992a-2960">5</span><span class="sxs-lookup"><span data-stu-id="8992a-2960">5</span></span>

<span data-ttu-id="8992a-2961">6</span><span class="sxs-lookup"><span data-stu-id="8992a-2961">6</span></span>

<span data-ttu-id="8992a-2962">7</span><span class="sxs-lookup"><span data-stu-id="8992a-2962">7</span></span>

<span data-ttu-id="8992a-2963">8</span><span class="sxs-lookup"><span data-stu-id="8992a-2963">8</span></span>

<span data-ttu-id="8992a-2964">9</span><span class="sxs-lookup"><span data-stu-id="8992a-2964">9</span></span>

<span data-ttu-id="8992a-2965">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2965">3</span></span><br/> <span data-ttu-id="8992a-2966">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2966">0</span></span><br/>

<span data-ttu-id="8992a-2967">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2967">1</span></span>

<span data-ttu-id="8992a-2968">\_flag (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2968">\_flag (optional)</span></span>

<span data-ttu-id="8992a-2969">\_fRootPath (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="8992a-2970">RootPath (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="8992a-2971">**\_ flag**: tipo di aggiornamento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8992a-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="8992a-2972">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8992a-2973">Questo campo deve essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="8992a-2974">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-2974">Value</span></span>                  | <span data-ttu-id="8992a-2975">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="8992a-2976">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="8992a-2977">È necessario eseguire un aggiornamento incrementale.</span><span class="sxs-lookup"><span data-stu-id="8992a-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="8992a-2978">\_0x00000001 completo UPD</span><span class="sxs-lookup"><span data-stu-id="8992a-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="8992a-2979">È necessario eseguire un aggiornamento completo.</span><span class="sxs-lookup"><span data-stu-id="8992a-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="8992a-2980">UPD \_ init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="8992a-2981">È necessario eseguire una nuova inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="8992a-2982">**\_ fRootPath**: valore booleano che indica se il campo RootPath specifica un percorso in cui eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8992a-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="8992a-2983">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8992a-2984">Questo campo deve essere impostato su 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="8992a-2985">Se impostato su 0x00000001, un percorso in cui eseguire l'aggiornamento è incluso in RootPath.</span><span class="sxs-lookup"><span data-stu-id="8992a-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="8992a-2986">Se impostato su 0x00000000, l'aggiornamento deve essere eseguito su tutti i percorsi indicizzati.</span><span class="sxs-lookup"><span data-stu-id="8992a-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="8992a-2987">**RootPath**: nome del percorso da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="8992a-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="8992a-2988">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8992a-2989">Il nome deve essere una stringa Unicode con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="8992a-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="8992a-2990">Questo campo deve essere omesso se \_ fRootPath è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="8992a-2991">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="8992a-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="8992a-2992">Il messaggio CPMForceMergeIn richiede a un server di eseguire qualsiasi manutenzione necessaria per migliorare le prestazioni di esecuzione delle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="8992a-2993">Il server risponderà con l'intestazione del messaggio del messaggio CPMForceMergeIn, con i risultati della richiesta contenuti nel \_ campo stato.</span><span class="sxs-lookup"><span data-stu-id="8992a-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="8992a-2994">Il formato del messaggio CPMForceMergeIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-2995">0</span><span class="sxs-lookup"><span data-stu-id="8992a-2995">0</span></span>

<span data-ttu-id="8992a-2996">1</span><span class="sxs-lookup"><span data-stu-id="8992a-2996">1</span></span>

<span data-ttu-id="8992a-2997">2</span><span class="sxs-lookup"><span data-stu-id="8992a-2997">2</span></span>

<span data-ttu-id="8992a-2998">3</span><span class="sxs-lookup"><span data-stu-id="8992a-2998">3</span></span>

<span data-ttu-id="8992a-2999">4</span><span class="sxs-lookup"><span data-stu-id="8992a-2999">4</span></span>

<span data-ttu-id="8992a-3000">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3000">5</span></span>

<span data-ttu-id="8992a-3001">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3001">6</span></span>

<span data-ttu-id="8992a-3002">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3002">7</span></span>

<span data-ttu-id="8992a-3003">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3003">8</span></span>

<span data-ttu-id="8992a-3004">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3004">9</span></span>

<span data-ttu-id="8992a-3005">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3005">1</span></span><br/> <span data-ttu-id="8992a-3006">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3006">0</span></span><br/>

<span data-ttu-id="8992a-3007">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3007">1</span></span>

<span data-ttu-id="8992a-3008">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3008">2</span></span>

<span data-ttu-id="8992a-3009">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3009">3</span></span>

<span data-ttu-id="8992a-3010">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3010">4</span></span>

<span data-ttu-id="8992a-3011">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3011">5</span></span>

<span data-ttu-id="8992a-3012">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3012">6</span></span>

<span data-ttu-id="8992a-3013">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3013">7</span></span>

<span data-ttu-id="8992a-3014">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3014">8</span></span>

<span data-ttu-id="8992a-3015">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3015">9</span></span>

<span data-ttu-id="8992a-3016">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3016">2</span></span><br/> <span data-ttu-id="8992a-3017">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3017">0</span></span><br/>

<span data-ttu-id="8992a-3018">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3018">1</span></span>

<span data-ttu-id="8992a-3019">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3019">2</span></span>

<span data-ttu-id="8992a-3020">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3020">3</span></span>

<span data-ttu-id="8992a-3021">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3021">4</span></span>

<span data-ttu-id="8992a-3022">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3022">5</span></span>

<span data-ttu-id="8992a-3023">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3023">6</span></span>

<span data-ttu-id="8992a-3024">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3024">7</span></span>

<span data-ttu-id="8992a-3025">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3025">8</span></span>

<span data-ttu-id="8992a-3026">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3026">9</span></span>

<span data-ttu-id="8992a-3027">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3027">3</span></span><br/> <span data-ttu-id="8992a-3028">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3028">0</span></span><br/>

<span data-ttu-id="8992a-3029">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3029">1</span></span>

<span data-ttu-id="8992a-3030">\_partId (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="8992a-3031">**\_ partID**: questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8992a-3032">Quando questo campo è presente, deve essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="8992a-3033">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="8992a-3034">Il messaggio CPMConnectIn inizia una sessione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="8992a-3035">Il formato del messaggio CPMConnectIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3036">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3036">0</span></span>

<span data-ttu-id="8992a-3037">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3037">1</span></span>

<span data-ttu-id="8992a-3038">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3038">2</span></span>

<span data-ttu-id="8992a-3039">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3039">3</span></span>

<span data-ttu-id="8992a-3040">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3040">4</span></span>

<span data-ttu-id="8992a-3041">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3041">5</span></span>

<span data-ttu-id="8992a-3042">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3042">6</span></span>

<span data-ttu-id="8992a-3043">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3043">7</span></span>

<span data-ttu-id="8992a-3044">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3044">8</span></span>

<span data-ttu-id="8992a-3045">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3045">9</span></span>

<span data-ttu-id="8992a-3046">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3046">1</span></span><br/> <span data-ttu-id="8992a-3047">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3047">0</span></span><br/>

<span data-ttu-id="8992a-3048">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3048">1</span></span>

<span data-ttu-id="8992a-3049">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3049">2</span></span>

<span data-ttu-id="8992a-3050">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3050">3</span></span>

<span data-ttu-id="8992a-3051">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3051">4</span></span>

<span data-ttu-id="8992a-3052">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3052">5</span></span>

<span data-ttu-id="8992a-3053">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3053">6</span></span>

<span data-ttu-id="8992a-3054">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3054">7</span></span>

<span data-ttu-id="8992a-3055">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3055">8</span></span>

<span data-ttu-id="8992a-3056">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3056">9</span></span>

<span data-ttu-id="8992a-3057">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3057">2</span></span><br/> <span data-ttu-id="8992a-3058">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3058">0</span></span><br/>

<span data-ttu-id="8992a-3059">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3059">1</span></span>

<span data-ttu-id="8992a-3060">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3060">2</span></span>

<span data-ttu-id="8992a-3061">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3061">3</span></span>

<span data-ttu-id="8992a-3062">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3062">4</span></span>

<span data-ttu-id="8992a-3063">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3063">5</span></span>

<span data-ttu-id="8992a-3064">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3064">6</span></span>

<span data-ttu-id="8992a-3065">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3065">7</span></span>

<span data-ttu-id="8992a-3066">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3066">8</span></span>

<span data-ttu-id="8992a-3067">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3067">9</span></span>

<span data-ttu-id="8992a-3068">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3068">3</span></span><br/> <span data-ttu-id="8992a-3069">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3069">0</span></span><br/>

<span data-ttu-id="8992a-3070">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3070">1</span></span>

<span data-ttu-id="8992a-3071">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="8992a-3071">\_iClientVersion</span></span>

<span data-ttu-id="8992a-3072">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="8992a-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="8992a-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="8992a-3073">\_cbBlob1</span></span>

<span data-ttu-id="8992a-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="8992a-3074">\_cbBlob2</span></span>

<span data-ttu-id="8992a-3075">\_imbottitura</span><span class="sxs-lookup"><span data-stu-id="8992a-3075">\_padding</span></span>

<span data-ttu-id="8992a-3076">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3076">...</span></span>

<span data-ttu-id="8992a-3077">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3077">...</span></span>

<span data-ttu-id="8992a-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="8992a-3078">MachineName</span></span>

<span data-ttu-id="8992a-3079">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-3079">... (variable)</span></span>

<span data-ttu-id="8992a-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="8992a-3080">UserName</span></span>

<span data-ttu-id="8992a-3081">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-3081">... (variable)</span></span>

<span data-ttu-id="8992a-3082">\_paddingcPropSets (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="8992a-3083">cPropSets</span><span class="sxs-lookup"><span data-stu-id="8992a-3083">cPropSets</span></span>

<span data-ttu-id="8992a-3084">PropertySet1 (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="8992a-3085">PropertySet2 (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="8992a-3086">\_paddingExtPropset (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="8992a-3087">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="8992a-3087">cExtPropSet</span></span>

<span data-ttu-id="8992a-3088">aPropertySets (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="8992a-3089">**\_ iClientVersion**: intero a 32 bit che indica se il server deve convalidare il valore di checksum specificato nel \_ campo ulChecksum delle intestazioni del messaggio per i messaggi inviati dal client.</span><span class="sxs-lookup"><span data-stu-id="8992a-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="8992a-3090">Se il \_ campo iClientVersion è impostato su 0x00000008 o su un valore superiore, il server deve convalidare il \_ valore del campo ulChecksum per i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="8992a-3091">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="8992a-3092">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="8992a-3093">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="8992a-3094">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="8992a-3095">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="8992a-3096">Per informazioni dettagliate sul modo in cui il server convalida il valore specificato dal client nel campo ulChecksum per i messaggi sopra elencati, vedere la sezione 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="8992a-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="8992a-3097">Se il valore è maggiore di 0x00000008, si presuppone che il client sia in grado di gestire gli offset a 64 bit nei messaggi CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="8992a-3098">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="8992a-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="8992a-3099">*Comportamento di Windows: nei client Windows, iClientVersion è impostato come segue*:</span><span class="sxs-lookup"><span data-stu-id="8992a-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="8992a-3100">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-3100">Value</span></span>      | <span data-ttu-id="8992a-3101">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="8992a-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8992a-3102">0x00000005</span></span> | <span data-ttu-id="8992a-3103">Il sistema operativo client è Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8992a-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="8992a-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8992a-3104">0x00000008</span></span> | <span data-ttu-id="8992a-3105">Il sistema operativo client è Windows XP a 32 bit o Windows Server 2003 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="8992a-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="8992a-3106">0x00010008</span></span> | <span data-ttu-id="8992a-3107">Il sistema operativo client è Windows XP a 64 bit o Windows Server 2003 a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="8992a-3108">\_**fClientIsRemote**: valore booleano che indica se il client è in esecuzione in un computer diverso da quello del server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="8992a-3109">DEVE essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="8992a-3110">\_**cbBlob1**: un Unsigned Integer a 32 bit che indica le dimensioni in byte dei campi CPropSet, PropertySet1 e PropertySet2, combinati.</span><span class="sxs-lookup"><span data-stu-id="8992a-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="8992a-3111">\_**cbBlob2**: un Unsigned Integer a 32 bit che indica le dimensioni in byte dei campi CExPropSet e aPropertySet, combinati.</span><span class="sxs-lookup"><span data-stu-id="8992a-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="8992a-3112">\_**spaziatura interna**: 12 byte di riempimento che possono contenere valori arbitrari e devono essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="8992a-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="8992a-3113">**MachineName**: nome del computer del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="8992a-3114">La stringa del nome deve essere una matrice con terminazione null di meno di 512 caratteri Unicode, incluso il terminatore NULL.</span><span class="sxs-lookup"><span data-stu-id="8992a-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="8992a-3115">**Username**: stringa che rappresenta il nome utente della persona che esegue l'applicazione che ha richiamato questo protocollo.</span><span class="sxs-lookup"><span data-stu-id="8992a-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="8992a-3116">La stringa del nome deve essere una matrice con terminazione null con un numero di caratteri Unicode inferiore a 512, se concatenata a MachineName.</span><span class="sxs-lookup"><span data-stu-id="8992a-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="8992a-3117">**\_ paddingcPropSets**: questo campo deve avere una lunghezza compresa tra 0 e 7 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="8992a-3118">Il numero di byte deve essere il numero necessario per fare in modo che l'offset di byte del campo cPropSets dall'inizio del messaggio che contiene la struttura sia un multiplo di 8.</span><span class="sxs-lookup"><span data-stu-id="8992a-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="8992a-3119">Il valore dei byte può essere qualsiasi valore arbitrario e deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-3120">**cPropSets**: Unsigned Integer A 32 bit che indica il numero di strutture CDbPropSet che seguono questo campo.</span><span class="sxs-lookup"><span data-stu-id="8992a-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="8992a-3121">Questo valore deve essere impostato su 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="8992a-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="8992a-3122">**PropertySet1**: struttura CDbPropSet con guidPropertySet che contiene DBPROPSET \_ FSCIFRMWRK \_ ext (vedere la sezione 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="8992a-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="8992a-3123">**PropertySet2**: struttura CDbPropSet con guidPropertySet che contiene DBPROPSET \_ CIFRMWRKCORE \_ ext (vedere la sezione 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="8992a-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="8992a-3124">\_**PaddingExtPropset**: questo campo deve avere una lunghezza compresa tra 0 e 7 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="8992a-3125">Il numero di byte deve essere il numero necessario per fare in modo che l'offset di byte del campo cExtPropSets dall'inizio del messaggio che contiene la struttura sia un multiplo di 8.</span><span class="sxs-lookup"><span data-stu-id="8992a-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="8992a-3126">Il valore dei byte può essere qualsiasi valore arbitrario e deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-3127">**cExtPropSet**: Unsigned Integer A 32 bit che indica il numero di strutture CDbPropSet che seguono questo campo.</span><span class="sxs-lookup"><span data-stu-id="8992a-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="8992a-3128">**aPropertySets**: matrice di strutture CDbPropSet che specifica altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="8992a-3129">Il numero di elementi nella matrice deve essere uguale a cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="8992a-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="8992a-3130">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="8992a-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="8992a-3131">Il messaggio CPMConnectOut contiene una risposta a un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="8992a-3132">Il formato del messaggio CPMConnectOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-3133">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3133">0</span></span>

<span data-ttu-id="8992a-3134">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3134">1</span></span>

<span data-ttu-id="8992a-3135">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3135">2</span></span>

<span data-ttu-id="8992a-3136">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3136">3</span></span>

<span data-ttu-id="8992a-3137">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3137">4</span></span>

<span data-ttu-id="8992a-3138">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3138">5</span></span>

<span data-ttu-id="8992a-3139">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3139">6</span></span>

<span data-ttu-id="8992a-3140">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3140">7</span></span>

<span data-ttu-id="8992a-3141">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3141">8</span></span>

<span data-ttu-id="8992a-3142">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3142">9</span></span>

<span data-ttu-id="8992a-3143">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3143">1</span></span><br/> <span data-ttu-id="8992a-3144">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3144">0</span></span><br/>

<span data-ttu-id="8992a-3145">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3145">1</span></span>

<span data-ttu-id="8992a-3146">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3146">2</span></span>

<span data-ttu-id="8992a-3147">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3147">3</span></span>

<span data-ttu-id="8992a-3148">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3148">4</span></span>

<span data-ttu-id="8992a-3149">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3149">5</span></span>

<span data-ttu-id="8992a-3150">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3150">6</span></span>

<span data-ttu-id="8992a-3151">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3151">7</span></span>

<span data-ttu-id="8992a-3152">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3152">8</span></span>

<span data-ttu-id="8992a-3153">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3153">9</span></span>

<span data-ttu-id="8992a-3154">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3154">2</span></span><br/> <span data-ttu-id="8992a-3155">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3155">0</span></span><br/>

<span data-ttu-id="8992a-3156">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3156">1</span></span>

<span data-ttu-id="8992a-3157">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3157">2</span></span>

<span data-ttu-id="8992a-3158">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3158">3</span></span>

<span data-ttu-id="8992a-3159">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3159">4</span></span>

<span data-ttu-id="8992a-3160">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3160">5</span></span>

<span data-ttu-id="8992a-3161">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3161">6</span></span>

<span data-ttu-id="8992a-3162">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3162">7</span></span>

<span data-ttu-id="8992a-3163">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3163">8</span></span>

<span data-ttu-id="8992a-3164">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3164">9</span></span>

<span data-ttu-id="8992a-3165">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3165">3</span></span><br/> <span data-ttu-id="8992a-3166">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3166">0</span></span><br/>

<span data-ttu-id="8992a-3167">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3167">1</span></span>

<span data-ttu-id="8992a-3168">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="8992a-3168">\_serverVersion</span></span>

<span data-ttu-id="8992a-3169">\_riservato (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="8992a-3170">**\_ ServerVersion**:</span><span class="sxs-lookup"><span data-stu-id="8992a-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="8992a-3171">Intero A 32 bit che indica se il server può supportare gli offset a 64 bit *.*</span><span class="sxs-lookup"><span data-stu-id="8992a-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="8992a-3172">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="8992a-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="8992a-3173">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-3173">Value</span></span>      | <span data-ttu-id="8992a-3174">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="8992a-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="8992a-3175">0x00000007</span></span> | <span data-ttu-id="8992a-3176">Il server è in grado di inviare solo offset a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="8992a-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="8992a-3177">0x00010007</span></span> | <span data-ttu-id="8992a-3178">Il server può inviare offset 32 o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="8992a-3179">**\_ riservato**: riservato.</span><span class="sxs-lookup"><span data-stu-id="8992a-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="8992a-3180">Il server può inviare un numero arbitrario di valori arbitrari e il client deve ignorare questi valori, se presenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="8992a-3181">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="8992a-3182">Il messaggio CPMCreateQueryIn crea una nuova query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="8992a-3183">Il formato del messaggio CPMCreateQueryIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3184">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3184">0</span></span>

<span data-ttu-id="8992a-3185">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3185">1</span></span>

<span data-ttu-id="8992a-3186">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3186">2</span></span>

<span data-ttu-id="8992a-3187">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3187">3</span></span>

<span data-ttu-id="8992a-3188">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3188">4</span></span>

<span data-ttu-id="8992a-3189">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3189">5</span></span>

<span data-ttu-id="8992a-3190">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3190">6</span></span>

<span data-ttu-id="8992a-3191">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3191">7</span></span>

<span data-ttu-id="8992a-3192">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3192">8</span></span>

<span data-ttu-id="8992a-3193">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3193">9</span></span>

<span data-ttu-id="8992a-3194">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3194">1</span></span><br/> <span data-ttu-id="8992a-3195">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3195">0</span></span><br/>

<span data-ttu-id="8992a-3196">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3196">1</span></span>

<span data-ttu-id="8992a-3197">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3197">2</span></span>

<span data-ttu-id="8992a-3198">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3198">3</span></span>

<span data-ttu-id="8992a-3199">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3199">4</span></span>

<span data-ttu-id="8992a-3200">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3200">5</span></span>

<span data-ttu-id="8992a-3201">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3201">6</span></span>

<span data-ttu-id="8992a-3202">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3202">7</span></span>

<span data-ttu-id="8992a-3203">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3203">8</span></span>

<span data-ttu-id="8992a-3204">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3204">9</span></span>

<span data-ttu-id="8992a-3205">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3205">2</span></span><br/> <span data-ttu-id="8992a-3206">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3206">0</span></span><br/>

<span data-ttu-id="8992a-3207">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3207">1</span></span>

<span data-ttu-id="8992a-3208">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3208">2</span></span>

<span data-ttu-id="8992a-3209">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3209">3</span></span>

<span data-ttu-id="8992a-3210">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3210">4</span></span>

<span data-ttu-id="8992a-3211">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3211">5</span></span>

<span data-ttu-id="8992a-3212">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3212">6</span></span>

<span data-ttu-id="8992a-3213">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3213">7</span></span>

<span data-ttu-id="8992a-3214">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3214">8</span></span>

<span data-ttu-id="8992a-3215">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3215">9</span></span>

<span data-ttu-id="8992a-3216">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3216">3</span></span><br/> <span data-ttu-id="8992a-3217">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3217">0</span></span><br/>

<span data-ttu-id="8992a-3218">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3218">1</span></span>

<span data-ttu-id="8992a-3219">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8992a-3219">Size</span></span>

<span data-ttu-id="8992a-3220">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="8992a-3220">CColumnSetPresent</span></span>

<span data-ttu-id="8992a-3221">ColumnStore (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="8992a-3222">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-3222">... (variable)</span></span>

<span data-ttu-id="8992a-3223">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="8992a-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="8992a-3224">Restrizione (facoltativa)</span><span class="sxs-lookup"><span data-stu-id="8992a-3224">Restriction (optional)</span></span>

<span data-ttu-id="8992a-3225">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-3225">... (variable)</span></span>

<span data-ttu-id="8992a-3226">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="8992a-3226">CSortSetPresent</span></span>

<span data-ttu-id="8992a-3227">Sortt (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3227">SortSet (optional)</span></span>

<span data-ttu-id="8992a-3228">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-3228">... (variable)</span></span>

<span data-ttu-id="8992a-3229">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="8992a-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="8992a-3230">CategorizationSet (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="8992a-3231">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-3231">... (variable)</span></span>

<span data-ttu-id="8992a-3232">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="8992a-3232">RowSetProperties</span></span>

<span data-ttu-id="8992a-3233">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3233">...</span></span>

<span data-ttu-id="8992a-3234">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3234">...</span></span>

<span data-ttu-id="8992a-3235">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3235">...</span></span>

<span data-ttu-id="8992a-3236">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3236">...</span></span>

<span data-ttu-id="8992a-3237">PidMapper (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="8992a-3238">**Size**: Unsigned Integer a 32 bit che indica il numero di byte dall'inizio di questo campo alla fine del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="8992a-3239">**CColumnSetPresent**: campo byte che indica se il campo di un oggetto columnstore è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="8992a-3240">Questo campo deve essere impostato su 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="8992a-3241">Se impostato su 0x01, il campo CColumnSet deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="8992a-3242">Se impostato su 0x00, deve essere assente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="8992a-3243">**Columnstore**: struttura CColumnSet contenente i numeri di colonna in cui devono essere restituite le proprietà di CPidMapper.</span><span class="sxs-lookup"><span data-stu-id="8992a-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="8992a-3244">**CRestrictionPresent**: campo di byte che indica se il campo di restrizione è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="8992a-3245">Se è impostato su un valore diverso da zero, il campo di restrizione deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="8992a-3246">Se impostato su 0x00, la restrizione deve essere assente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="8992a-3247">**Restrizione**: struttura CRestriction contenente l'albero dei comandi della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="8992a-3248">**CSortSetPresent**: campo di byte che indica se il campo di ordinamento è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="8992a-3249">Se è impostato su un valore diverso da zero, il campo del set di ordinamenti deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="8992a-3250">Se impostato su 0x00, il set di ordinamenti deve essere assente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="8992a-3251">**Sortt**: struttura CSortSet che indica l'ordinamento della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="8992a-3252">**CCategorizationSetPresent**: campo byte che indica se il campo CCategorizationSet è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="8992a-3253">Se è impostato su un valore diverso da zero, è necessario che il campo CCategorizationSet sia presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="8992a-3254">Se impostato su 0x00, CCategorizationSet deve essere assente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="8992a-3255">**CCategorizationSet**: struttura CCategorizationSet che contiene i gruppi per la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="8992a-3256">**RowSetProperties**: struttura CRowsetProperties che fornisce le informazioni di configurazione per la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="8992a-3257">**PidMapper**: struttura CPidMapper che contiene le proprietà da restituire in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="8992a-3258">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="8992a-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="8992a-3259">Il messaggio CPMCreateQueryOut contiene una risposta a un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="8992a-3260">Il formato del messaggio CPMCreateQueryOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-3261">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3261">0</span></span>

<span data-ttu-id="8992a-3262">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3262">1</span></span>

<span data-ttu-id="8992a-3263">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3263">2</span></span>

<span data-ttu-id="8992a-3264">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3264">3</span></span>

<span data-ttu-id="8992a-3265">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3265">4</span></span>

<span data-ttu-id="8992a-3266">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3266">5</span></span>

<span data-ttu-id="8992a-3267">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3267">6</span></span>

<span data-ttu-id="8992a-3268">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3268">7</span></span>

<span data-ttu-id="8992a-3269">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3269">8</span></span>

<span data-ttu-id="8992a-3270">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3270">9</span></span>

<span data-ttu-id="8992a-3271">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3271">1</span></span><br/> <span data-ttu-id="8992a-3272">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3272">0</span></span><br/>

<span data-ttu-id="8992a-3273">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3273">1</span></span>

<span data-ttu-id="8992a-3274">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3274">2</span></span>

<span data-ttu-id="8992a-3275">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3275">3</span></span>

<span data-ttu-id="8992a-3276">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3276">4</span></span>

<span data-ttu-id="8992a-3277">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3277">5</span></span>

<span data-ttu-id="8992a-3278">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3278">6</span></span>

<span data-ttu-id="8992a-3279">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3279">7</span></span>

<span data-ttu-id="8992a-3280">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3280">8</span></span>

<span data-ttu-id="8992a-3281">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3281">9</span></span>

<span data-ttu-id="8992a-3282">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3282">2</span></span><br/> <span data-ttu-id="8992a-3283">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3283">0</span></span><br/>

<span data-ttu-id="8992a-3284">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3284">1</span></span>

<span data-ttu-id="8992a-3285">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3285">2</span></span>

<span data-ttu-id="8992a-3286">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3286">3</span></span>

<span data-ttu-id="8992a-3287">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3287">4</span></span>

<span data-ttu-id="8992a-3288">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3288">5</span></span>

<span data-ttu-id="8992a-3289">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3289">6</span></span>

<span data-ttu-id="8992a-3290">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3290">7</span></span>

<span data-ttu-id="8992a-3291">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3291">8</span></span>

<span data-ttu-id="8992a-3292">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3292">9</span></span>

<span data-ttu-id="8992a-3293">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3293">3</span></span><br/> <span data-ttu-id="8992a-3294">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3294">0</span></span><br/>

<span data-ttu-id="8992a-3295">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3295">1</span></span>

<span data-ttu-id="8992a-3296">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="8992a-3296">\_fTrueSequential</span></span>

<span data-ttu-id="8992a-3297">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="8992a-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="8992a-3298">aCursors</span><span class="sxs-lookup"><span data-stu-id="8992a-3298">aCursors</span></span>



 

<span data-ttu-id="8992a-3299">**\_ fTrueSequential**: valore booleano informativo che indica se la query può fornire risultati più velocemente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="8992a-3300">Quando è impostato su 0x00000001 per la query fornita in CPMCreateQueryIn, il server può utilizzare l'indice in modo che i risultati della query vengano recapitati più velocemente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="8992a-3301">Quando è impostato su 0x00000000, si verificherà una latenza maggiore nel recapito dei risultati della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="8992a-3302">Non deve essere impostato su un altro valore.</span><span class="sxs-lookup"><span data-stu-id="8992a-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="8992a-3303">**\_ fWorkIdUnique**: valore booleano che indica se gli identificatori di documento a cui puntano i cursori sono univoci per tutti i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="8992a-3304">Se impostato su 0x00000001, gli identificatori sono univoci.</span><span class="sxs-lookup"><span data-stu-id="8992a-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="8992a-3305">Se impostata su 0x00000000, sono univoche solo in tutto il set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="8992a-3306">**aCursors**: matrice di interi senza segno a 32 bit che rappresenta gli handle per i cursori, con il numero di elementi uguale al numero di categorie nel campo CategorizationSet del messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="8992a-3307">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="8992a-3308">Il messaggio CPMGetQueryStatusIn richiede lo stato di una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="8992a-3309">Il formato del messaggio CPMGetQueryStatusIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3310">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3310">0</span></span>

<span data-ttu-id="8992a-3311">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3311">1</span></span>

<span data-ttu-id="8992a-3312">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3312">2</span></span>

<span data-ttu-id="8992a-3313">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3313">3</span></span>

<span data-ttu-id="8992a-3314">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3314">4</span></span>

<span data-ttu-id="8992a-3315">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3315">5</span></span>

<span data-ttu-id="8992a-3316">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3316">6</span></span>

<span data-ttu-id="8992a-3317">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3317">7</span></span>

<span data-ttu-id="8992a-3318">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3318">8</span></span>

<span data-ttu-id="8992a-3319">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3319">9</span></span>

<span data-ttu-id="8992a-3320">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3320">1</span></span><br/> <span data-ttu-id="8992a-3321">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3321">0</span></span><br/>

<span data-ttu-id="8992a-3322">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3322">1</span></span>

<span data-ttu-id="8992a-3323">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3323">2</span></span>

<span data-ttu-id="8992a-3324">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3324">3</span></span>

<span data-ttu-id="8992a-3325">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3325">4</span></span>

<span data-ttu-id="8992a-3326">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3326">5</span></span>

<span data-ttu-id="8992a-3327">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3327">6</span></span>

<span data-ttu-id="8992a-3328">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3328">7</span></span>

<span data-ttu-id="8992a-3329">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3329">8</span></span>

<span data-ttu-id="8992a-3330">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3330">9</span></span>

<span data-ttu-id="8992a-3331">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3331">2</span></span><br/> <span data-ttu-id="8992a-3332">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3332">0</span></span><br/>

<span data-ttu-id="8992a-3333">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3333">1</span></span>

<span data-ttu-id="8992a-3334">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3334">2</span></span>

<span data-ttu-id="8992a-3335">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3335">3</span></span>

<span data-ttu-id="8992a-3336">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3336">4</span></span>

<span data-ttu-id="8992a-3337">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3337">5</span></span>

<span data-ttu-id="8992a-3338">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3338">6</span></span>

<span data-ttu-id="8992a-3339">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3339">7</span></span>

<span data-ttu-id="8992a-3340">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3340">8</span></span>

<span data-ttu-id="8992a-3341">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3341">9</span></span>

<span data-ttu-id="8992a-3342">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3342">3</span></span><br/> <span data-ttu-id="8992a-3343">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3343">0</span></span><br/>

<span data-ttu-id="8992a-3344">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3344">1</span></span>

<span data-ttu-id="8992a-3345">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8992a-3345">\_hCursor</span></span>



 

<span data-ttu-id="8992a-3346">**\_ hCursor**: un Unsigned Integer a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per la quale recuperare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="8992a-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="8992a-3347">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="8992a-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="8992a-3348">Il messaggio CPMGetQueryStatusOut risponde a un messaggio CPMGetQueryStatusIn con lo stato della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="8992a-3349">Il formato del messaggio CPMGetQueryStatusOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-3350">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3350">0</span></span>

<span data-ttu-id="8992a-3351">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3351">1</span></span>

<span data-ttu-id="8992a-3352">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3352">2</span></span>

<span data-ttu-id="8992a-3353">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3353">3</span></span>

<span data-ttu-id="8992a-3354">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3354">4</span></span>

<span data-ttu-id="8992a-3355">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3355">5</span></span>

<span data-ttu-id="8992a-3356">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3356">6</span></span>

<span data-ttu-id="8992a-3357">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3357">7</span></span>

<span data-ttu-id="8992a-3358">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3358">8</span></span>

<span data-ttu-id="8992a-3359">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3359">9</span></span>

<span data-ttu-id="8992a-3360">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3360">1</span></span><br/> <span data-ttu-id="8992a-3361">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3361">0</span></span><br/>

<span data-ttu-id="8992a-3362">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3362">1</span></span>

<span data-ttu-id="8992a-3363">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3363">2</span></span>

<span data-ttu-id="8992a-3364">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3364">3</span></span>

<span data-ttu-id="8992a-3365">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3365">4</span></span>

<span data-ttu-id="8992a-3366">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3366">5</span></span>

<span data-ttu-id="8992a-3367">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3367">6</span></span>

<span data-ttu-id="8992a-3368">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3368">7</span></span>

<span data-ttu-id="8992a-3369">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3369">8</span></span>

<span data-ttu-id="8992a-3370">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3370">9</span></span>

<span data-ttu-id="8992a-3371">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3371">2</span></span><br/> <span data-ttu-id="8992a-3372">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3372">0</span></span><br/>

<span data-ttu-id="8992a-3373">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3373">1</span></span>

<span data-ttu-id="8992a-3374">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3374">2</span></span>

<span data-ttu-id="8992a-3375">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3375">3</span></span>

<span data-ttu-id="8992a-3376">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3376">4</span></span>

<span data-ttu-id="8992a-3377">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3377">5</span></span>

<span data-ttu-id="8992a-3378">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3378">6</span></span>

<span data-ttu-id="8992a-3379">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3379">7</span></span>

<span data-ttu-id="8992a-3380">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3380">8</span></span>

<span data-ttu-id="8992a-3381">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3381">9</span></span>

<span data-ttu-id="8992a-3382">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3382">3</span></span><br/> <span data-ttu-id="8992a-3383">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3383">0</span></span><br/>

<span data-ttu-id="8992a-3384">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3384">1</span></span>

<span data-ttu-id="8992a-3385">\_Stato</span><span class="sxs-lookup"><span data-stu-id="8992a-3385">\_Status</span></span>



 

<span data-ttu-id="8992a-3386">**\_ Stato**: maschera di maschera dei valori definiti nelle tabelle seguenti, che descrive la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="8992a-3387">La tabella seguente elenca \_ \* i valori stat ottenuti eseguendo un'operazione and bit per bit sullo \_ stato con 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="8992a-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="8992a-3388">Il risultato deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="8992a-3389">Costante</span><span class="sxs-lookup"><span data-stu-id="8992a-3389">Constant</span></span>                 | <span data-ttu-id="8992a-3390">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-3391">STAT \_ occupato 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="8992a-3392">La query asincrona è ancora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8992a-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="8992a-3393">\_Errore stat 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="8992a-3394">La query è in stato di errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="8992a-3395">STAT \_ completato 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="8992a-3396">La query è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8992a-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="8992a-3397">STAT \_ Refresh 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8992a-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="8992a-3398">La query è stata completata, ma gli aggiornamenti hanno come risultato un calcolo aggiuntivo delle query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="8992a-3399">Nella tabella seguente sono elencati i bit STAT aggiuntivi \_ \* che è possibile impostare in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="8992a-3400">Costante</span><span class="sxs-lookup"><span data-stu-id="8992a-3400">Constant</span></span>                                    | <span data-ttu-id="8992a-3401">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8992a-3402">\_Parole non significative \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="8992a-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="8992a-3403">Parole non significative sostituite da caratteri jolly nella query sul contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="8992a-3404">\_Contenuto stat \_ non \_ \_ aggiornato 0x00000020</span><span class="sxs-lookup"><span data-stu-id="8992a-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="8992a-3405">I risultati della query potrebbero non essere corretti perché la query ha richiesto file modificati ma non indicizzati.</span><span class="sxs-lookup"><span data-stu-id="8992a-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="8992a-3406">\_0x00000040 di aggiornamento stat \_ incompleto</span><span class="sxs-lookup"><span data-stu-id="8992a-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="8992a-3407">I risultati della query potrebbero non essere corretti perché la query ha richiesto la modifica e la reindicizzazione dei file il cui contenuto non è incluso.</span><span class="sxs-lookup"><span data-stu-id="8992a-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="8992a-3408">\_Query sul contenuto stat \_ \_ incompleta 0x00000080</span><span class="sxs-lookup"><span data-stu-id="8992a-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="8992a-3409">La query sul contenuto è troppo complessa per completare l'enumerazione o obbligatoria anziché utilizzare l'indice di contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="8992a-3410">\_Limite di tempo stat \_ \_ superato 0x00000100</span><span class="sxs-lookup"><span data-stu-id="8992a-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="8992a-3411">I risultati della query potrebbero non essere corretti perché il tempo di esecuzione della query ha raggiunto il tempo massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="8992a-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="8992a-3412">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="8992a-3413">Il messaggio CPMGetQueryStatusExIn richiede lo stato di una query e informazioni aggiuntive, ad esempio il numero di documenti indicizzati, il numero di documenti rimanenti da indicizzare e così via.</span><span class="sxs-lookup"><span data-stu-id="8992a-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="8992a-3414">Il formato del messaggio CPMGetQueryStatusExIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3415">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3415">0</span></span>

<span data-ttu-id="8992a-3416">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3416">1</span></span>

<span data-ttu-id="8992a-3417">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3417">2</span></span>

<span data-ttu-id="8992a-3418">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3418">3</span></span>

<span data-ttu-id="8992a-3419">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3419">4</span></span>

<span data-ttu-id="8992a-3420">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3420">5</span></span>

<span data-ttu-id="8992a-3421">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3421">6</span></span>

<span data-ttu-id="8992a-3422">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3422">7</span></span>

<span data-ttu-id="8992a-3423">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3423">8</span></span>

<span data-ttu-id="8992a-3424">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3424">9</span></span>

<span data-ttu-id="8992a-3425">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3425">1</span></span><br/> <span data-ttu-id="8992a-3426">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3426">0</span></span><br/>

<span data-ttu-id="8992a-3427">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3427">1</span></span>

<span data-ttu-id="8992a-3428">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3428">2</span></span>

<span data-ttu-id="8992a-3429">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3429">3</span></span>

<span data-ttu-id="8992a-3430">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3430">4</span></span>

<span data-ttu-id="8992a-3431">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3431">5</span></span>

<span data-ttu-id="8992a-3432">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3432">6</span></span>

<span data-ttu-id="8992a-3433">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3433">7</span></span>

<span data-ttu-id="8992a-3434">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3434">8</span></span>

<span data-ttu-id="8992a-3435">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3435">9</span></span>

<span data-ttu-id="8992a-3436">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3436">2</span></span><br/> <span data-ttu-id="8992a-3437">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3437">0</span></span><br/>

<span data-ttu-id="8992a-3438">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3438">1</span></span>

<span data-ttu-id="8992a-3439">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3439">2</span></span>

<span data-ttu-id="8992a-3440">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3440">3</span></span>

<span data-ttu-id="8992a-3441">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3441">4</span></span>

<span data-ttu-id="8992a-3442">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3442">5</span></span>

<span data-ttu-id="8992a-3443">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3443">6</span></span>

<span data-ttu-id="8992a-3444">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3444">7</span></span>

<span data-ttu-id="8992a-3445">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3445">8</span></span>

<span data-ttu-id="8992a-3446">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3446">9</span></span>

<span data-ttu-id="8992a-3447">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3447">3</span></span><br/> <span data-ttu-id="8992a-3448">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3448">0</span></span><br/>

<span data-ttu-id="8992a-3449">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3449">1</span></span>

<span data-ttu-id="8992a-3450">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8992a-3450">\_hCursor</span></span>

<span data-ttu-id="8992a-3451">\_BMK</span><span class="sxs-lookup"><span data-stu-id="8992a-3451">\_bmk</span></span>



 

<span data-ttu-id="8992a-3452">**\_ hCursor**: valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per la quale recuperare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="8992a-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="8992a-3453">**\_ BMK**: valore a 32 bit che indica l'handle di un segnalibro la cui posizione deve essere recuperata.</span><span class="sxs-lookup"><span data-stu-id="8992a-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="8992a-3454">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="8992a-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="8992a-3455">Il messaggio CPMGetQueryStatusExOut risponde a un messaggio CPMGetQueryStatusExIn con lo stato della query e altre informazioni sullo stato, come illustrato nel diagramma riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8992a-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="8992a-3456">Il formato del messaggio CPMGetQueryStatusExOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-3457">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3457">0</span></span>

<span data-ttu-id="8992a-3458">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3458">1</span></span>

<span data-ttu-id="8992a-3459">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3459">2</span></span>

<span data-ttu-id="8992a-3460">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3460">3</span></span>

<span data-ttu-id="8992a-3461">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3461">4</span></span>

<span data-ttu-id="8992a-3462">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3462">5</span></span>

<span data-ttu-id="8992a-3463">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3463">6</span></span>

<span data-ttu-id="8992a-3464">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3464">7</span></span>

<span data-ttu-id="8992a-3465">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3465">8</span></span>

<span data-ttu-id="8992a-3466">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3466">9</span></span>

<span data-ttu-id="8992a-3467">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3467">1</span></span><br/> <span data-ttu-id="8992a-3468">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3468">0</span></span><br/>

<span data-ttu-id="8992a-3469">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3469">1</span></span>

<span data-ttu-id="8992a-3470">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3470">2</span></span>

<span data-ttu-id="8992a-3471">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3471">3</span></span>

<span data-ttu-id="8992a-3472">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3472">4</span></span>

<span data-ttu-id="8992a-3473">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3473">5</span></span>

<span data-ttu-id="8992a-3474">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3474">6</span></span>

<span data-ttu-id="8992a-3475">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3475">7</span></span>

<span data-ttu-id="8992a-3476">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3476">8</span></span>

<span data-ttu-id="8992a-3477">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3477">9</span></span>

<span data-ttu-id="8992a-3478">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3478">2</span></span><br/> <span data-ttu-id="8992a-3479">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3479">0</span></span><br/>

<span data-ttu-id="8992a-3480">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3480">1</span></span>

<span data-ttu-id="8992a-3481">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3481">2</span></span>

<span data-ttu-id="8992a-3482">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3482">3</span></span>

<span data-ttu-id="8992a-3483">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3483">4</span></span>

<span data-ttu-id="8992a-3484">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3484">5</span></span>

<span data-ttu-id="8992a-3485">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3485">6</span></span>

<span data-ttu-id="8992a-3486">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3486">7</span></span>

<span data-ttu-id="8992a-3487">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3487">8</span></span>

<span data-ttu-id="8992a-3488">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3488">9</span></span>

<span data-ttu-id="8992a-3489">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3489">3</span></span><br/> <span data-ttu-id="8992a-3490">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3490">0</span></span><br/>

<span data-ttu-id="8992a-3491">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3491">1</span></span>

<span data-ttu-id="8992a-3492">\_Stato</span><span class="sxs-lookup"><span data-stu-id="8992a-3492">\_Status</span></span>

<span data-ttu-id="8992a-3493">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="8992a-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="8992a-3494">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="8992a-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="8992a-3495">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="8992a-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="8992a-3496">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="8992a-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="8992a-3497">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="8992a-3497">\_iRowBmk</span></span>

<span data-ttu-id="8992a-3498">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="8992a-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="8992a-3499">**\_ Stato**: una delle stat \_ \* valori specificati nella sezione 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="8992a-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="8992a-3500">**\_ cFilteredDocuments**: Unsigned Integer A 32 bit che indica il numero di documenti indicizzati</span><span class="sxs-lookup"><span data-stu-id="8992a-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="8992a-3501">**\_ cDocumentsToFilter**: Unsigned Integer a 32 bit che indica il numero di documenti rimanenti da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="8992a-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="8992a-3502">**\_ dwRatioFinishedDenominator**: un Unsigned Integer a 32 bit che indica il denominatore del rapporto dei documenti completati dall'elaborazione della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="8992a-3503">**\_ dwRatioFinishedNumerator**: un Unsigned Integer a 32 bit che indica il numeratore del rapporto dei documenti completati dall'elaborazione della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="8992a-3504">**\_ iRowBmk**: Unsigned Integer a 32 bit che indica la posizione approssimativa del segnalibro nel set di righe in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="8992a-3505">**\_ cRowsTotal**: un Unsigned Integer a 32 bit che specifica il numero totale di righe nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="8992a-3506">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="8992a-3507">Il messaggio CPMSetBindingsIn richiede l'associazione di colonne a un set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="8992a-3508">Il server risponderà al messaggio di richiesta CPMSetBindingsIn usando la sezione di intestazione del messaggio CPMBindingsIn con i risultati della richiesta contenuta nel \_ campo stato.</span><span class="sxs-lookup"><span data-stu-id="8992a-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="8992a-3509">Il formato del messaggio CPMSetBindingsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3510">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3510">0</span></span>

<span data-ttu-id="8992a-3511">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3511">1</span></span>

<span data-ttu-id="8992a-3512">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3512">2</span></span>

<span data-ttu-id="8992a-3513">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3513">3</span></span>

<span data-ttu-id="8992a-3514">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3514">4</span></span>

<span data-ttu-id="8992a-3515">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3515">5</span></span>

<span data-ttu-id="8992a-3516">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3516">6</span></span>

<span data-ttu-id="8992a-3517">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3517">7</span></span>

<span data-ttu-id="8992a-3518">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3518">8</span></span>

<span data-ttu-id="8992a-3519">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3519">9</span></span>

<span data-ttu-id="8992a-3520">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3520">1</span></span><br/> <span data-ttu-id="8992a-3521">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3521">0</span></span><br/>

<span data-ttu-id="8992a-3522">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3522">1</span></span>

<span data-ttu-id="8992a-3523">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3523">2</span></span>

<span data-ttu-id="8992a-3524">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3524">3</span></span>

<span data-ttu-id="8992a-3525">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3525">4</span></span>

<span data-ttu-id="8992a-3526">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3526">5</span></span>

<span data-ttu-id="8992a-3527">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3527">6</span></span>

<span data-ttu-id="8992a-3528">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3528">7</span></span>

<span data-ttu-id="8992a-3529">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3529">8</span></span>

<span data-ttu-id="8992a-3530">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3530">9</span></span>

<span data-ttu-id="8992a-3531">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3531">2</span></span><br/> <span data-ttu-id="8992a-3532">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3532">0</span></span><br/>

<span data-ttu-id="8992a-3533">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3533">1</span></span>

<span data-ttu-id="8992a-3534">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3534">2</span></span>

<span data-ttu-id="8992a-3535">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3535">3</span></span>

<span data-ttu-id="8992a-3536">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3536">4</span></span>

<span data-ttu-id="8992a-3537">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3537">5</span></span>

<span data-ttu-id="8992a-3538">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3538">6</span></span>

<span data-ttu-id="8992a-3539">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3539">7</span></span>

<span data-ttu-id="8992a-3540">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3540">8</span></span>

<span data-ttu-id="8992a-3541">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3541">9</span></span>

<span data-ttu-id="8992a-3542">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3542">3</span></span><br/> <span data-ttu-id="8992a-3543">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3543">0</span></span><br/>

<span data-ttu-id="8992a-3544">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3544">1</span></span>

<span data-ttu-id="8992a-3545">\_hCursor (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="8992a-3546">\_cbRow (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="8992a-3547">\_cbBindingDesc (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="8992a-3548">\_fittizio (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3548">\_dummy (optional)</span></span>

<span data-ttu-id="8992a-3549">cColumns (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3549">cColumns (optional)</span></span>

<span data-ttu-id="8992a-3550">aColumns (variabile, facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="8992a-3551">**\_ hCursor**: valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la riga per cui impostare le associazioni.</span><span class="sxs-lookup"><span data-stu-id="8992a-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="8992a-3552">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8992a-3553">**\_ cbRow**: un Unsigned Integer a 32 bit che indica le dimensioni, in byte, di una riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="8992a-3554">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8992a-3555">**\_ cbBindingDesc**: Unsigned Integer a 32 bit che indica la lunghezza, in byte, dei campi che seguono il \_ campo fittizio.</span><span class="sxs-lookup"><span data-stu-id="8992a-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="8992a-3556">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8992a-3557">**\_ fittizio**: questo campo non è usato e deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8992a-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="8992a-3558">Può essere impostata su qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="8992a-3559">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8992a-3560">**CColumns**: Unsigned Integer a 32 bit che indica il numero di elementi nella matrice aColumns.</span><span class="sxs-lookup"><span data-stu-id="8992a-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="8992a-3561">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8992a-3562">**aColumns**: matrice di strutture CTableColumn che descrive le colonne di una riga nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="8992a-3563">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8992a-3564">Le strutture nella matrice devono essere separate da un byte di riempimento compreso tra 0 e 3 in modo che ogni struttura disponga di un allineamento a 4 byte dall'inizio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="8992a-3565">Tali byte di riempimento possono essere qualsiasi valore arbitrario e devono essere ignorati alla ricezione.</span><span class="sxs-lookup"><span data-stu-id="8992a-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="8992a-3566">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="8992a-3567">Il messaggio CPMGetRowsIn richiede righe da una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="8992a-3568">Il formato del messaggio CPMGetRowsIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3569">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3569">0</span></span>

<span data-ttu-id="8992a-3570">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3570">1</span></span>

<span data-ttu-id="8992a-3571">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3571">2</span></span>

<span data-ttu-id="8992a-3572">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3572">3</span></span>

<span data-ttu-id="8992a-3573">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3573">4</span></span>

<span data-ttu-id="8992a-3574">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3574">5</span></span>

<span data-ttu-id="8992a-3575">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3575">6</span></span>

<span data-ttu-id="8992a-3576">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3576">7</span></span>

<span data-ttu-id="8992a-3577">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3577">8</span></span>

<span data-ttu-id="8992a-3578">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3578">9</span></span>

<span data-ttu-id="8992a-3579">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3579">1</span></span><br/> <span data-ttu-id="8992a-3580">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3580">0</span></span><br/>

<span data-ttu-id="8992a-3581">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3581">1</span></span>

<span data-ttu-id="8992a-3582">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3582">2</span></span>

<span data-ttu-id="8992a-3583">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3583">3</span></span>

<span data-ttu-id="8992a-3584">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3584">4</span></span>

<span data-ttu-id="8992a-3585">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3585">5</span></span>

<span data-ttu-id="8992a-3586">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3586">6</span></span>

<span data-ttu-id="8992a-3587">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3587">7</span></span>

<span data-ttu-id="8992a-3588">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3588">8</span></span>

<span data-ttu-id="8992a-3589">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3589">9</span></span>

<span data-ttu-id="8992a-3590">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3590">2</span></span><br/> <span data-ttu-id="8992a-3591">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3591">0</span></span><br/>

<span data-ttu-id="8992a-3592">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3592">1</span></span>

<span data-ttu-id="8992a-3593">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3593">2</span></span>

<span data-ttu-id="8992a-3594">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3594">3</span></span>

<span data-ttu-id="8992a-3595">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3595">4</span></span>

<span data-ttu-id="8992a-3596">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3596">5</span></span>

<span data-ttu-id="8992a-3597">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3597">6</span></span>

<span data-ttu-id="8992a-3598">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3598">7</span></span>

<span data-ttu-id="8992a-3599">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3599">8</span></span>

<span data-ttu-id="8992a-3600">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3600">9</span></span>

<span data-ttu-id="8992a-3601">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3601">3</span></span><br/> <span data-ttu-id="8992a-3602">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3602">0</span></span><br/>

<span data-ttu-id="8992a-3603">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3603">1</span></span>

<span data-ttu-id="8992a-3604">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8992a-3604">\_hCursor</span></span>

<span data-ttu-id="8992a-3605">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="8992a-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="8992a-3606">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="8992a-3606">\_cbRowWidth</span></span>

<span data-ttu-id="8992a-3607">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="8992a-3607">\_cbSeek</span></span>

<span data-ttu-id="8992a-3608">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="8992a-3608">\_cbReserved</span></span>

<span data-ttu-id="8992a-3609">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="8992a-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="8992a-3610">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="8992a-3610">\_ulClientBase</span></span>

<span data-ttu-id="8992a-3611">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="8992a-3611">\_fBwdFetch</span></span>

<span data-ttu-id="8992a-3612">eType</span><span class="sxs-lookup"><span data-stu-id="8992a-3612">eType</span></span>

<span data-ttu-id="8992a-3613">\_Cap</span><span class="sxs-lookup"><span data-stu-id="8992a-3613">\_chapt</span></span>

<span data-ttu-id="8992a-3614">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="8992a-3614">SeekDescription</span></span>

<span data-ttu-id="8992a-3615">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3615">...</span></span>

<span data-ttu-id="8992a-3616">... variabile</span><span class="sxs-lookup"><span data-stu-id="8992a-3616">... (variable)</span></span>



 

<span data-ttu-id="8992a-3617">**\_ hCursor**: valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut che identifica la query per la quale recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="8992a-3618">**\_ cRowsToTransfer**: Unsigned Integer a 32 bit che indica il numero massimo di righe che il client desidera ricevere in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="8992a-3619">**\_ cbRowWidth**: Unsigned Integer a 32 bit che indica la lunghezza di una riga, in byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="8992a-3620">**\_ cbSeek**: Unsigned Integer A 32 bit che indica la dimensione del messaggio che inizia con etype.</span><span class="sxs-lookup"><span data-stu-id="8992a-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="8992a-3621">**\_ cbReserved**: un Unsigned Integer a 32 bit che indica le dimensioni, in byte, di un messaggio CPMGetRowsOut (senza i campi Rows e SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="8992a-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="8992a-3622">Questo valore in questo campo viene aggiunto al valore del \_ campo cbSeek e quindi deve essere utilizzato per calcolare il campo offset di righe nel messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="8992a-3623">**\_ cbReadBuffer**: un Unsigned Integer a 32 bit che deve essere impostato sul valore massimo di \_ cbRowWidth o 1000 volte il valore di \_ cRowsToTransfer, arrotondato per eccesso al più vicino 512 byte multiplo.</span><span class="sxs-lookup"><span data-stu-id="8992a-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="8992a-3624">Il valore non deve superare 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="8992a-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="8992a-3625">**\_ ulClientBase**: Unsigned Integer a 32 bit che indica il valore di base da utilizzare per i calcoli dei puntatori nel buffer di riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="8992a-3626">Se vengono usati offset a 64 bit, il campo Reserved2 dell'intestazione del messaggio viene usato come 32 bit superiore e \_ ulClientBase come 32 bit inferiori di un valore a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="8992a-3627">Per informazioni dettagliate, vedere la sezione 2.2.3.16.</span><span class="sxs-lookup"><span data-stu-id="8992a-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="8992a-3628">**\_ fBwdFetch**: Unsigned Integer a 32 bit che indica l'ordine in cui recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="8992a-3629">Se impostato su 0x00000001, le righe devono essere recuperate in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="8992a-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="8992a-3630">Se impostato su 0x00000000, le righe devono essere recuperate in ordine di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="8992a-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="8992a-3631">NON deve essere impostato su nessun altro valore.</span><span class="sxs-lookup"><span data-stu-id="8992a-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="8992a-3632">**etype**: Unsigned Integer a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8992a-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="8992a-3633">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-3633">Value</span></span>                         | <span data-ttu-id="8992a-3634">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="8992a-3635">0x00000001 eRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="8992a-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="8992a-3636">SeekDescription contiene una struttura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="8992a-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="8992a-3637">0x00000002 eRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="8992a-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="8992a-3638">SeekDescription contiene una struttura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="8992a-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="8992a-3639">0x00000003 eRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="8992a-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="8992a-3640">SeekDescription contiene una struttura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="8992a-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="8992a-3641">0x00000004 eRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="8992a-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="8992a-3642">SeekDescription contiene una struttura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="8992a-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="8992a-3643">**\_ Chapt**: valore a 32 bit che rappresenta l'handle del capitolo del set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="8992a-3644">**SeekDescription**: questo campo deve contenere una struttura del tipo indicato dal valore di etype.</span><span class="sxs-lookup"><span data-stu-id="8992a-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="8992a-3645">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="8992a-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="8992a-3646">Il messaggio CPMGetRowsOut risponde a un messaggio CPMGetRowsIn con le righe di una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="8992a-3647">I server devono formattare gli offset in tipi di dati a lunghezza variabile nel campo righe come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="8992a-3648">Il client ha indicato che si tratta di un sistema a 32 bit (0x00000008 o less nel campo iClientVersion di CPMConnectIn): gli offset sono Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="8992a-3649">Il client indica che si tratta di un sistema a 64 bit ( \_ iClientVersion > 0x00000008 in CPMConnectIn) e che il server ha indicato che si tratta di un sistema a 32 bit ( \_ ServerVersion impostato su 0X00000007 in CPMConnectOut): gli offset sono integer a 32 bit</span><span class="sxs-lookup"><span data-stu-id="8992a-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="8992a-3650">Il client indica che si tratta di un sistema a 64 bit ( \_ iClientVersion > 0x00000008 in CPMConnectIn) e che il server ha indicato che si tratta di un sistema a 64 bit ( \_ ServerVersion impostato su 0X00010007 in CPMConnectOut): gli offset sono integer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="8992a-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="8992a-3651">Il formato del messaggio CPMGetRowsOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-3652">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3652">0</span></span>

<span data-ttu-id="8992a-3653">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3653">1</span></span>

<span data-ttu-id="8992a-3654">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3654">2</span></span>

<span data-ttu-id="8992a-3655">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3655">3</span></span>

<span data-ttu-id="8992a-3656">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3656">4</span></span>

<span data-ttu-id="8992a-3657">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3657">5</span></span>

<span data-ttu-id="8992a-3658">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3658">6</span></span>

<span data-ttu-id="8992a-3659">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3659">7</span></span>

<span data-ttu-id="8992a-3660">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3660">8</span></span>

<span data-ttu-id="8992a-3661">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3661">9</span></span>

<span data-ttu-id="8992a-3662">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3662">1</span></span><br/> <span data-ttu-id="8992a-3663">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3663">0</span></span><br/>

<span data-ttu-id="8992a-3664">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3664">1</span></span>

<span data-ttu-id="8992a-3665">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3665">2</span></span>

<span data-ttu-id="8992a-3666">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3666">3</span></span>

<span data-ttu-id="8992a-3667">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3667">4</span></span>

<span data-ttu-id="8992a-3668">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3668">5</span></span>

<span data-ttu-id="8992a-3669">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3669">6</span></span>

<span data-ttu-id="8992a-3670">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3670">7</span></span>

<span data-ttu-id="8992a-3671">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3671">8</span></span>

<span data-ttu-id="8992a-3672">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3672">9</span></span>

<span data-ttu-id="8992a-3673">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3673">2</span></span><br/> <span data-ttu-id="8992a-3674">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3674">0</span></span><br/>

<span data-ttu-id="8992a-3675">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3675">1</span></span>

<span data-ttu-id="8992a-3676">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3676">2</span></span>

<span data-ttu-id="8992a-3677">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3677">3</span></span>

<span data-ttu-id="8992a-3678">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3678">4</span></span>

<span data-ttu-id="8992a-3679">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3679">5</span></span>

<span data-ttu-id="8992a-3680">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3680">6</span></span>

<span data-ttu-id="8992a-3681">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3681">7</span></span>

<span data-ttu-id="8992a-3682">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3682">8</span></span>

<span data-ttu-id="8992a-3683">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3683">9</span></span>

<span data-ttu-id="8992a-3684">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3684">3</span></span><br/> <span data-ttu-id="8992a-3685">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3685">0</span></span><br/>

<span data-ttu-id="8992a-3686">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3686">1</span></span>

<span data-ttu-id="8992a-3687">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="8992a-3687">\_cRowsReturned</span></span>

<span data-ttu-id="8992a-3688">eType</span><span class="sxs-lookup"><span data-stu-id="8992a-3688">eType</span></span>

<span data-ttu-id="8992a-3689">\_Cap</span><span class="sxs-lookup"><span data-stu-id="8992a-3689">\_chapt</span></span>

<span data-ttu-id="8992a-3690">SeekDescription (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="8992a-3691">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3691">...</span></span>

<span data-ttu-id="8992a-3692">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3692">...</span></span>

<span data-ttu-id="8992a-3693">paddingRows (facoltativo, variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="8992a-3694">Righe</span><span class="sxs-lookup"><span data-stu-id="8992a-3694">Rows</span></span>



 

<span data-ttu-id="8992a-3695">**\_ cRowsReturned**: Unsigned Integer a 32 bit che indica il numero di righe restituite nelle righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="8992a-3696">**etype**: Unsigned Integer a 32 bit contenente uno dei valori seguenti per indicare il tipo di operazione rowseek da eseguire</span><span class="sxs-lookup"><span data-stu-id="8992a-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="8992a-3697">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-3697">Value</span></span>                         | <span data-ttu-id="8992a-3698">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="8992a-3699">0x00000000 eRowsSeekNone</span><span class="sxs-lookup"><span data-stu-id="8992a-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="8992a-3700">Nessun SeekDescription, ignora il campo SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="8992a-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="8992a-3701">0x00000001 eRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="8992a-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="8992a-3702">SeekDescription contiene una struttura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="8992a-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="8992a-3703">0x00000002 eRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="8992a-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="8992a-3704">SeekDescription contiene una struttura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="8992a-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="8992a-3705">0x00000003 eRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="8992a-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="8992a-3706">SeekDescription contiene una struttura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="8992a-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="8992a-3707">0x00000004 eRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="8992a-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="8992a-3708">SeekDescription contiene una struttura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="8992a-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="8992a-3709">**\_ Chapt**: valore a 32 bit che rappresenta l'handle del capitolo del set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="8992a-3710">**SeekDescription**: questo campo deve contenere una struttura del tipo indicato dal campo etype.</span><span class="sxs-lookup"><span data-stu-id="8992a-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="8992a-3711">**paddingRows**: questo campo deve avere una lunghezza sufficiente (da 0 a \_ cbReserved-1 byte) per riempire il campo righe in \_ offset cbReserved dall'inizio di un messaggio, dove \_ cbReserved è il valore nel messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="8992a-3712">I byte di riempimento utilizzati in questo campo possono essere qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="8992a-3713">Questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8992a-3714">**Rows**: i dati delle righe sono formattati come previsto dalle informazioni sulle colonne nel messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="8992a-3715">Le righe devono essere archiviate in ordine di avanzamento (ad esempio, la riga 1 prima della riga 2).</span><span class="sxs-lookup"><span data-stu-id="8992a-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="8992a-3716">Le colonne a dimensione fissa devono essere archiviate in corrispondenza degli offset specificati dal messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="8992a-3717">Le colonne di dimensioni variabili, ad esempio le stringhe, devono essere archiviate come segue:</span><span class="sxs-lookup"><span data-stu-id="8992a-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="8992a-3718">I dati della variabile (ad esempio, la stringa) vengono archiviati in ordine decrescente verso la fine del buffer, ad esempio la raccolta di tutti i dati delle variabili per la riga 1 si trova alla fine, riga 2 successiva più vicina e così via.</span><span class="sxs-lookup"><span data-stu-id="8992a-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="8992a-3719">L'area a dimensione fissa (all'inizio del buffer di riga) deve contenere un CRowVariant per ogni colonna, archiviato in corrispondenza dell'offset specificato nel messaggio CPMSetBindingsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="8992a-3720">vType deve contenere il tipo di dati (ad esempio, VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="8992a-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="8992a-3721">Se, come determinato dalle regole all'inizio della sezione in questa sezione vengono utilizzati offset 32 bit, il campo offset in CRowVariant deve contenere un valore a 32 bit che rappresenta l'offset dei dati della variabile dall'inizio del messaggio CPMGetRowsOut, più il valore di \_ ulClientBase specificato nel messaggio CPMGetRowsIn più recente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="8992a-3722">Se vengono utilizzati offset a 64 bit, il campo offset in CRowVariant deve contenere un valore a 64 bit che rappresenta l'offset dall'inizio del messaggio CPMGetRowsOut, aggiunto a un valore a 64 bit composto utilizzando \_ ulClientBase come minimo 32 bit e \_ ulReserved2 come bit 32.</span><span class="sxs-lookup"><span data-stu-id="8992a-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="8992a-3723">Se, ad esempio, il messaggio CPMSetBindingsIn ha specificato due colonne (VT \_ I4) e title (VT \_ LPWSTR) e \_ ulClientBase da CPMGetRowsIn è 0x10000, verranno visualizzate due righe, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8992a-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="8992a-3724">La sezione contrassegnata in grigio è la parte a lunghezza fissa del buffer.</span><span class="sxs-lookup"><span data-stu-id="8992a-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![esempio di messaggio cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="8992a-3726">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="8992a-3727">Il messaggio CPMRatioFinishedIn richiede la percentuale di completamento di una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="8992a-3728">Il formato del messaggio CPMRatioFinishedIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3729">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3729">0</span></span>

<span data-ttu-id="8992a-3730">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3730">1</span></span>

<span data-ttu-id="8992a-3731">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3731">2</span></span>

<span data-ttu-id="8992a-3732">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3732">3</span></span>

<span data-ttu-id="8992a-3733">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3733">4</span></span>

<span data-ttu-id="8992a-3734">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3734">5</span></span>

<span data-ttu-id="8992a-3735">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3735">6</span></span>

<span data-ttu-id="8992a-3736">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3736">7</span></span>

<span data-ttu-id="8992a-3737">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3737">8</span></span>

<span data-ttu-id="8992a-3738">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3738">9</span></span>

<span data-ttu-id="8992a-3739">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3739">1</span></span><br/> <span data-ttu-id="8992a-3740">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3740">0</span></span><br/>

<span data-ttu-id="8992a-3741">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3741">1</span></span>

<span data-ttu-id="8992a-3742">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3742">2</span></span>

<span data-ttu-id="8992a-3743">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3743">3</span></span>

<span data-ttu-id="8992a-3744">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3744">4</span></span>

<span data-ttu-id="8992a-3745">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3745">5</span></span>

<span data-ttu-id="8992a-3746">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3746">6</span></span>

<span data-ttu-id="8992a-3747">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3747">7</span></span>

<span data-ttu-id="8992a-3748">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3748">8</span></span>

<span data-ttu-id="8992a-3749">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3749">9</span></span>

<span data-ttu-id="8992a-3750">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3750">2</span></span><br/> <span data-ttu-id="8992a-3751">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3751">0</span></span><br/>

<span data-ttu-id="8992a-3752">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3752">1</span></span>

<span data-ttu-id="8992a-3753">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3753">2</span></span>

<span data-ttu-id="8992a-3754">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3754">3</span></span>

<span data-ttu-id="8992a-3755">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3755">4</span></span>

<span data-ttu-id="8992a-3756">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3756">5</span></span>

<span data-ttu-id="8992a-3757">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3757">6</span></span>

<span data-ttu-id="8992a-3758">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3758">7</span></span>

<span data-ttu-id="8992a-3759">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3759">8</span></span>

<span data-ttu-id="8992a-3760">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3760">9</span></span>

<span data-ttu-id="8992a-3761">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3761">3</span></span><br/> <span data-ttu-id="8992a-3762">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3762">0</span></span><br/>

<span data-ttu-id="8992a-3763">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3763">1</span></span>

<span data-ttu-id="8992a-3764">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8992a-3764">\_hCursor</span></span>

<span data-ttu-id="8992a-3765">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="8992a-3765">\_fQuick</span></span>



 

<span data-ttu-id="8992a-3766">**\_ hCursor**: handle del messaggio CPMCreateQueryOut che identifica la query per la quale richiedere informazioni di completamento.</span><span class="sxs-lookup"><span data-stu-id="8992a-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="8992a-3767">**\_ fQuick**: deve essere impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="8992a-3768">Non usato e deve essere ignorato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="8992a-3769">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="8992a-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="8992a-3770">Il messaggio CPMRatioFinishedOut risponde a un messaggio CPMRatioFinishedIn con il rapporto di completamento di una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="8992a-3771">Il formato del messaggio CPMRatioFinishedOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-3772">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3772">0</span></span>

<span data-ttu-id="8992a-3773">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3773">1</span></span>

<span data-ttu-id="8992a-3774">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3774">2</span></span>

<span data-ttu-id="8992a-3775">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3775">3</span></span>

<span data-ttu-id="8992a-3776">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3776">4</span></span>

<span data-ttu-id="8992a-3777">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3777">5</span></span>

<span data-ttu-id="8992a-3778">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3778">6</span></span>

<span data-ttu-id="8992a-3779">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3779">7</span></span>

<span data-ttu-id="8992a-3780">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3780">8</span></span>

<span data-ttu-id="8992a-3781">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3781">9</span></span>

<span data-ttu-id="8992a-3782">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3782">1</span></span><br/> <span data-ttu-id="8992a-3783">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3783">0</span></span><br/>

<span data-ttu-id="8992a-3784">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3784">1</span></span>

<span data-ttu-id="8992a-3785">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3785">2</span></span>

<span data-ttu-id="8992a-3786">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3786">3</span></span>

<span data-ttu-id="8992a-3787">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3787">4</span></span>

<span data-ttu-id="8992a-3788">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3788">5</span></span>

<span data-ttu-id="8992a-3789">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3789">6</span></span>

<span data-ttu-id="8992a-3790">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3790">7</span></span>

<span data-ttu-id="8992a-3791">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3791">8</span></span>

<span data-ttu-id="8992a-3792">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3792">9</span></span>

<span data-ttu-id="8992a-3793">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3793">2</span></span><br/> <span data-ttu-id="8992a-3794">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3794">0</span></span><br/>

<span data-ttu-id="8992a-3795">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3795">1</span></span>

<span data-ttu-id="8992a-3796">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3796">2</span></span>

<span data-ttu-id="8992a-3797">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3797">3</span></span>

<span data-ttu-id="8992a-3798">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3798">4</span></span>

<span data-ttu-id="8992a-3799">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3799">5</span></span>

<span data-ttu-id="8992a-3800">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3800">6</span></span>

<span data-ttu-id="8992a-3801">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3801">7</span></span>

<span data-ttu-id="8992a-3802">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3802">8</span></span>

<span data-ttu-id="8992a-3803">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3803">9</span></span>

<span data-ttu-id="8992a-3804">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3804">3</span></span><br/> <span data-ttu-id="8992a-3805">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3805">0</span></span><br/>

<span data-ttu-id="8992a-3806">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3806">1</span></span>

<span data-ttu-id="8992a-3807">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="8992a-3807">\_ ulNumerator</span></span>

<span data-ttu-id="8992a-3808">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="8992a-3808">\_ulDenominator</span></span>

<span data-ttu-id="8992a-3809">\_Corvi</span><span class="sxs-lookup"><span data-stu-id="8992a-3809">\_cRows</span></span>

<span data-ttu-id="8992a-3810">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="8992a-3810">\_fNewRows</span></span>



 

<span data-ttu-id="8992a-3811">**\_ ulNumerator**: Unsigned Integer a 32 bit che indica il numeratore del rapporto di completamento in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="8992a-3812">**\_ ulDenominator**: un Unsigned Integer a 32 bit che indica il denominatore del rapporto di completamento in termini di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="8992a-3813">DEVE essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="8992a-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="8992a-3814">**\_ Crows**: Unsigned Integer a 32 bit che indica il numero totale di righe per la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="8992a-3815">**\_ fNewRows**: valore booleano che indica se sono disponibili nuove righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="8992a-3816">Il valore 0x00000001 indica che nel set di righe sono disponibili nuove righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="8992a-3817">Il valore 0x00000000 indica che il set di righe non contiene nuove righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="8992a-3818">Questo campo non deve essere impostato su nessun altro valore.</span><span class="sxs-lookup"><span data-stu-id="8992a-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="8992a-3819">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="8992a-3820">Il messaggio CPMFetchValueIn richiede un valore della proprietà troppo grande per essere restituito in un set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="8992a-3821">Come specificato nella sezione 3.2.4.2.5, questo messaggio viene inviato ripetutamente per recuperare tutti i byte della proprietà, aggiornando \_ cbSoFar per ogni, finché il \_ campo fMoreExists del messaggio CPMFetchValueOut non è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="8992a-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="8992a-3822">Il formato del messaggio CPMFetchValueIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3823">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3823">0</span></span>

<span data-ttu-id="8992a-3824">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3824">1</span></span>

<span data-ttu-id="8992a-3825">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3825">2</span></span>

<span data-ttu-id="8992a-3826">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3826">3</span></span>

<span data-ttu-id="8992a-3827">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3827">4</span></span>

<span data-ttu-id="8992a-3828">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3828">5</span></span>

<span data-ttu-id="8992a-3829">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3829">6</span></span>

<span data-ttu-id="8992a-3830">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3830">7</span></span>

<span data-ttu-id="8992a-3831">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3831">8</span></span>

<span data-ttu-id="8992a-3832">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3832">9</span></span>

<span data-ttu-id="8992a-3833">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3833">1</span></span><br/> <span data-ttu-id="8992a-3834">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3834">0</span></span><br/>

<span data-ttu-id="8992a-3835">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3835">1</span></span>

<span data-ttu-id="8992a-3836">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3836">2</span></span>

<span data-ttu-id="8992a-3837">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3837">3</span></span>

<span data-ttu-id="8992a-3838">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3838">4</span></span>

<span data-ttu-id="8992a-3839">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3839">5</span></span>

<span data-ttu-id="8992a-3840">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3840">6</span></span>

<span data-ttu-id="8992a-3841">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3841">7</span></span>

<span data-ttu-id="8992a-3842">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3842">8</span></span>

<span data-ttu-id="8992a-3843">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3843">9</span></span>

<span data-ttu-id="8992a-3844">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3844">2</span></span><br/> <span data-ttu-id="8992a-3845">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3845">0</span></span><br/>

<span data-ttu-id="8992a-3846">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3846">1</span></span>

<span data-ttu-id="8992a-3847">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3847">2</span></span>

<span data-ttu-id="8992a-3848">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3848">3</span></span>

<span data-ttu-id="8992a-3849">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3849">4</span></span>

<span data-ttu-id="8992a-3850">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3850">5</span></span>

<span data-ttu-id="8992a-3851">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3851">6</span></span>

<span data-ttu-id="8992a-3852">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3852">7</span></span>

<span data-ttu-id="8992a-3853">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3853">8</span></span>

<span data-ttu-id="8992a-3854">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3854">9</span></span>

<span data-ttu-id="8992a-3855">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3855">3</span></span><br/> <span data-ttu-id="8992a-3856">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3856">0</span></span><br/>

<span data-ttu-id="8992a-3857">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3857">1</span></span>

<span data-ttu-id="8992a-3858">\_wid</span><span class="sxs-lookup"><span data-stu-id="8992a-3858">\_wid</span></span>

<span data-ttu-id="8992a-3859">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="8992a-3859">\_cbSoFar</span></span>

<span data-ttu-id="8992a-3860">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="8992a-3860">\_cbPropSpec</span></span>

<span data-ttu-id="8992a-3861">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="8992a-3861">\_cbChunk</span></span>

<span data-ttu-id="8992a-3862">Campo PROPSPEC (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3862">PropSpec (variable)</span></span>

<span data-ttu-id="8992a-3863">...</span><span class="sxs-lookup"><span data-stu-id="8992a-3863">...</span></span>

<span data-ttu-id="8992a-3864">\_spaziatura interna (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="8992a-3865">**\_ wid**: un Unsigned Integer a 32 bit che rappresenta l'ID documento che identifica il documento per cui deve essere recuperata una proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-3865">**\_wid**: A 32-bit unsigned integer representing the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="8992a-3866">**\_ cbSoFar**: Unsigned Integer a 32 bit contenente il numero di byte trasferiti in precedenza per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="8992a-3867">DEVE essere impostato su 0x00000000 nel primo messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="8992a-3868">**\_ cbPropSpec**: Unsigned Integer a 32 bit contenente le dimensioni del campo Campo PROPSPEC, in byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="8992a-3869">**\_ cbChunk**: un Unsigned Integer a 32 bit contenente il numero massimo di byte che il mittente può accettare in un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="8992a-3870">*Comportamento di Windows: questo campo è impostato su 0x00004000 per tutte le versioni di Windows.*</span><span class="sxs-lookup"><span data-stu-id="8992a-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="8992a-3871">**Campo PROPSPEC**: struttura CFullPropSpec che specifica la proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8992a-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="8992a-3872">**\_ spaziatura interna**: questo campo deve essere della lunghezza necessaria (da 0 a 3 byte) per riempire il messaggio a un multiplo di 4 byte di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="8992a-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="8992a-3873">Il valore dei byte di riempimento può essere qualsiasi valore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="8992a-3874">Questo campo deve essere ignorato dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="8992a-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="8992a-3875">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="8992a-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="8992a-3876">Il messaggio CPMFetchValueOut risponde a un messaggio CPMFetchValueIn con un valore della proprietà di una query precedente.</span><span class="sxs-lookup"><span data-stu-id="8992a-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="8992a-3877">Come specificato nella sezione 3.1.5.2.8, questo messaggio viene inviato dopo ogni messaggio CPMFetchValueIn fino a quando non vengono trasferiti tutti i byte della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="8992a-3878">Il formato del messaggio CPMFetchValueOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-3879">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3879">0</span></span>

<span data-ttu-id="8992a-3880">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3880">1</span></span>

<span data-ttu-id="8992a-3881">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3881">2</span></span>

<span data-ttu-id="8992a-3882">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3882">3</span></span>

<span data-ttu-id="8992a-3883">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3883">4</span></span>

<span data-ttu-id="8992a-3884">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3884">5</span></span>

<span data-ttu-id="8992a-3885">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3885">6</span></span>

<span data-ttu-id="8992a-3886">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3886">7</span></span>

<span data-ttu-id="8992a-3887">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3887">8</span></span>

<span data-ttu-id="8992a-3888">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3888">9</span></span>

<span data-ttu-id="8992a-3889">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3889">1</span></span><br/> <span data-ttu-id="8992a-3890">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3890">0</span></span><br/>

<span data-ttu-id="8992a-3891">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3891">1</span></span>

<span data-ttu-id="8992a-3892">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3892">2</span></span>

<span data-ttu-id="8992a-3893">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3893">3</span></span>

<span data-ttu-id="8992a-3894">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3894">4</span></span>

<span data-ttu-id="8992a-3895">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3895">5</span></span>

<span data-ttu-id="8992a-3896">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3896">6</span></span>

<span data-ttu-id="8992a-3897">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3897">7</span></span>

<span data-ttu-id="8992a-3898">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3898">8</span></span>

<span data-ttu-id="8992a-3899">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3899">9</span></span>

<span data-ttu-id="8992a-3900">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3900">2</span></span><br/> <span data-ttu-id="8992a-3901">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3901">0</span></span><br/>

<span data-ttu-id="8992a-3902">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3902">1</span></span>

<span data-ttu-id="8992a-3903">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3903">2</span></span>

<span data-ttu-id="8992a-3904">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3904">3</span></span>

<span data-ttu-id="8992a-3905">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3905">4</span></span>

<span data-ttu-id="8992a-3906">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3906">5</span></span>

<span data-ttu-id="8992a-3907">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3907">6</span></span>

<span data-ttu-id="8992a-3908">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3908">7</span></span>

<span data-ttu-id="8992a-3909">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3909">8</span></span>

<span data-ttu-id="8992a-3910">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3910">9</span></span>

<span data-ttu-id="8992a-3911">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3911">3</span></span><br/> <span data-ttu-id="8992a-3912">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3912">0</span></span><br/>

<span data-ttu-id="8992a-3913">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3913">1</span></span>

<span data-ttu-id="8992a-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="8992a-3914">\_cbValue</span></span>

<span data-ttu-id="8992a-3915">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="8992a-3915">\_fMoreExists</span></span>

<span data-ttu-id="8992a-3916">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="8992a-3916">\_fValueExists</span></span>

<span data-ttu-id="8992a-3917">vType</span><span class="sxs-lookup"><span data-stu-id="8992a-3917">vType</span></span>

<span data-ttu-id="8992a-3918">vValue (variabile)</span><span class="sxs-lookup"><span data-stu-id="8992a-3918">vValue (variable)</span></span>



 

<span data-ttu-id="8992a-3919">**\_ cbValue**: Unsigned Integer a 32 bit contenente le dimensioni totali, in byte in vValue.</span><span class="sxs-lookup"><span data-stu-id="8992a-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="8992a-3920">**\_ fMoreExists**: valore booleano che indica se sono presenti altri messaggi CPMFetchValueOut disponibili.</span><span class="sxs-lookup"><span data-stu-id="8992a-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="8992a-3921">Se impostato su 0x00000001, sono presenti altri messaggi CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="8992a-3922">Se impostato su 0x00000000, non sono disponibili altri messaggi di CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="8992a-3923">**\_ fValueExists**: valore booleano che indica se è presente un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="8992a-3924">Se impostato su 0x00000001, esiste un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="8992a-3925">Se impostato su 0x00000000, non esiste un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="8992a-3926">**vType**: valore dell'enumerazione VarEnum. per informazioni dettagliate, vedere la sezione 2.2.1.1, che descrive il tipo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="8992a-3927">**vValue**: parte di una matrice di byte contenente una struttura SERIALIZEDPROPERTYVALUE come specificato nella sezione 2.2.1.32, in cui l'offset dell'inizio della parte è il valore di \_ cbSoFar in CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="8992a-3928">La lunghezza della parte, indicata dal \_ campo cbValue, deve essere uguale al valore di \_ CbChunk in CPMFetchValueIn se \_ fMoreExists è impostata su 0x00000001 e deve essere minore o uguale al valore di \_ cbChunk in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8992a-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="8992a-3929">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="8992a-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="8992a-3930">Il messaggio CPMGetNotify richiede che il client desideri ricevere una notifica delle modifiche apportate al set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="8992a-3931">Il messaggio non deve includere un corpo; è necessario inviare solo l'intestazione del messaggio, come specificato nella sezione 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="8992a-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="8992a-3932">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="8992a-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="8992a-3933">Il messaggio CPMSendNotifyOut invia una notifica al client di una modifica ai risultati di una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="8992a-3934">Questo messaggio viene inviato solo quando si verifica una modifica.</span><span class="sxs-lookup"><span data-stu-id="8992a-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="8992a-3935">Il formato del messaggio CPMSendNotifyOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-3936">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3936">0</span></span>

<span data-ttu-id="8992a-3937">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3937">1</span></span>

<span data-ttu-id="8992a-3938">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3938">2</span></span>

<span data-ttu-id="8992a-3939">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3939">3</span></span>

<span data-ttu-id="8992a-3940">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3940">4</span></span>

<span data-ttu-id="8992a-3941">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3941">5</span></span>

<span data-ttu-id="8992a-3942">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3942">6</span></span>

<span data-ttu-id="8992a-3943">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3943">7</span></span>

<span data-ttu-id="8992a-3944">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3944">8</span></span>

<span data-ttu-id="8992a-3945">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3945">9</span></span>

<span data-ttu-id="8992a-3946">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3946">1</span></span><br/> <span data-ttu-id="8992a-3947">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3947">0</span></span><br/>

<span data-ttu-id="8992a-3948">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3948">1</span></span>

<span data-ttu-id="8992a-3949">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3949">2</span></span>

<span data-ttu-id="8992a-3950">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3950">3</span></span>

<span data-ttu-id="8992a-3951">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3951">4</span></span>

<span data-ttu-id="8992a-3952">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3952">5</span></span>

<span data-ttu-id="8992a-3953">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3953">6</span></span>

<span data-ttu-id="8992a-3954">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3954">7</span></span>

<span data-ttu-id="8992a-3955">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3955">8</span></span>

<span data-ttu-id="8992a-3956">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3956">9</span></span>

<span data-ttu-id="8992a-3957">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3957">2</span></span><br/> <span data-ttu-id="8992a-3958">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3958">0</span></span><br/>

<span data-ttu-id="8992a-3959">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3959">1</span></span>

<span data-ttu-id="8992a-3960">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3960">2</span></span>

<span data-ttu-id="8992a-3961">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3961">3</span></span>

<span data-ttu-id="8992a-3962">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3962">4</span></span>

<span data-ttu-id="8992a-3963">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3963">5</span></span>

<span data-ttu-id="8992a-3964">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3964">6</span></span>

<span data-ttu-id="8992a-3965">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3965">7</span></span>

<span data-ttu-id="8992a-3966">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3966">8</span></span>

<span data-ttu-id="8992a-3967">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3967">9</span></span>

<span data-ttu-id="8992a-3968">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3968">3</span></span><br/> <span data-ttu-id="8992a-3969">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3969">0</span></span><br/>

<span data-ttu-id="8992a-3970">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3970">1</span></span>

<span data-ttu-id="8992a-3971">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="8992a-3971">\_watchNotify</span></span>



 

<span data-ttu-id="8992a-3972">**\_ watchNotify**: modifica apportata alla query.</span><span class="sxs-lookup"><span data-stu-id="8992a-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="8992a-3973">DEVE essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="8992a-3974">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-3974">Value</span></span>                                     | <span data-ttu-id="8992a-3975">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="8992a-3976">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8992a-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="8992a-3977">Il numero di righe nel set di righe della query è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="8992a-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="8992a-3978">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="8992a-3979">La query è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8992a-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="8992a-3980">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8992a-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="8992a-3981">La query è stata eseguita di nuovo.</span><span class="sxs-lookup"><span data-stu-id="8992a-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="8992a-3982">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="8992a-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="8992a-3983">Il messaggio CPMGetApproximatePositionIn richiede la posizione approssimativa di un segnalibro in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="8992a-3984">Il formato del messaggio CPMGetApproximatePositionIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-3985">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3985">0</span></span>

<span data-ttu-id="8992a-3986">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3986">1</span></span>

<span data-ttu-id="8992a-3987">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3987">2</span></span>

<span data-ttu-id="8992a-3988">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3988">3</span></span>

<span data-ttu-id="8992a-3989">4</span><span class="sxs-lookup"><span data-stu-id="8992a-3989">4</span></span>

<span data-ttu-id="8992a-3990">5</span><span class="sxs-lookup"><span data-stu-id="8992a-3990">5</span></span>

<span data-ttu-id="8992a-3991">6</span><span class="sxs-lookup"><span data-stu-id="8992a-3991">6</span></span>

<span data-ttu-id="8992a-3992">7</span><span class="sxs-lookup"><span data-stu-id="8992a-3992">7</span></span>

<span data-ttu-id="8992a-3993">8</span><span class="sxs-lookup"><span data-stu-id="8992a-3993">8</span></span>

<span data-ttu-id="8992a-3994">9</span><span class="sxs-lookup"><span data-stu-id="8992a-3994">9</span></span>

<span data-ttu-id="8992a-3995">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3995">1</span></span><br/> <span data-ttu-id="8992a-3996">0</span><span class="sxs-lookup"><span data-stu-id="8992a-3996">0</span></span><br/>

<span data-ttu-id="8992a-3997">1</span><span class="sxs-lookup"><span data-stu-id="8992a-3997">1</span></span>

<span data-ttu-id="8992a-3998">2</span><span class="sxs-lookup"><span data-stu-id="8992a-3998">2</span></span>

<span data-ttu-id="8992a-3999">3</span><span class="sxs-lookup"><span data-stu-id="8992a-3999">3</span></span>

<span data-ttu-id="8992a-4000">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4000">4</span></span>

<span data-ttu-id="8992a-4001">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4001">5</span></span>

<span data-ttu-id="8992a-4002">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4002">6</span></span>

<span data-ttu-id="8992a-4003">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4003">7</span></span>

<span data-ttu-id="8992a-4004">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4004">8</span></span>

<span data-ttu-id="8992a-4005">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4005">9</span></span>

<span data-ttu-id="8992a-4006">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4006">2</span></span><br/> <span data-ttu-id="8992a-4007">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4007">0</span></span><br/>

<span data-ttu-id="8992a-4008">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4008">1</span></span>

<span data-ttu-id="8992a-4009">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4009">2</span></span>

<span data-ttu-id="8992a-4010">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4010">3</span></span>

<span data-ttu-id="8992a-4011">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4011">4</span></span>

<span data-ttu-id="8992a-4012">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4012">5</span></span>

<span data-ttu-id="8992a-4013">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4013">6</span></span>

<span data-ttu-id="8992a-4014">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4014">7</span></span>

<span data-ttu-id="8992a-4015">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4015">8</span></span>

<span data-ttu-id="8992a-4016">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4016">9</span></span>

<span data-ttu-id="8992a-4017">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4017">3</span></span><br/> <span data-ttu-id="8992a-4018">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4018">0</span></span><br/>

<span data-ttu-id="8992a-4019">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4019">1</span></span>

<span data-ttu-id="8992a-4020">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8992a-4020">\_hCursor</span></span>

<span data-ttu-id="8992a-4021">\_Cap</span><span class="sxs-lookup"><span data-stu-id="8992a-4021">\_chapt</span></span>

<span data-ttu-id="8992a-4022">\_BMK</span><span class="sxs-lookup"><span data-stu-id="8992a-4022">\_bmk</span></span>



 

<span data-ttu-id="8992a-4023">**\_ hCursor**: valore a 32 bit che rappresenta il cursore di query ottenuto da CPMCreateQueryOut per il set di righe che contiene il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="8992a-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="8992a-4024">**\_ Chapt**: valore a 32 bit che rappresenta l'handle per il capitolo contenente il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="8992a-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="8992a-4025">**\_ BMK**: valore a 32 bit che rappresenta l'handle per il segnalibro per il quale recuperare la posizione approssimativa.</span><span class="sxs-lookup"><span data-stu-id="8992a-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="8992a-4026">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="8992a-4027">Il messaggio CPMGetApproximatePositionOut risponde a un messaggio CPMGetApproximatePositionIn che descrive la posizione approssimativa del segnalibro nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="8992a-4028">Il formato del messaggio CPMGetApproximatePositionOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-4029">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4029">0</span></span>

<span data-ttu-id="8992a-4030">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4030">1</span></span>

<span data-ttu-id="8992a-4031">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4031">2</span></span>

<span data-ttu-id="8992a-4032">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4032">3</span></span>

<span data-ttu-id="8992a-4033">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4033">4</span></span>

<span data-ttu-id="8992a-4034">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4034">5</span></span>

<span data-ttu-id="8992a-4035">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4035">6</span></span>

<span data-ttu-id="8992a-4036">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4036">7</span></span>

<span data-ttu-id="8992a-4037">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4037">8</span></span>

<span data-ttu-id="8992a-4038">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4038">9</span></span>

<span data-ttu-id="8992a-4039">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4039">1</span></span><br/> <span data-ttu-id="8992a-4040">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4040">0</span></span><br/>

<span data-ttu-id="8992a-4041">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4041">1</span></span>

<span data-ttu-id="8992a-4042">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4042">2</span></span>

<span data-ttu-id="8992a-4043">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4043">3</span></span>

<span data-ttu-id="8992a-4044">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4044">4</span></span>

<span data-ttu-id="8992a-4045">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4045">5</span></span>

<span data-ttu-id="8992a-4046">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4046">6</span></span>

<span data-ttu-id="8992a-4047">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4047">7</span></span>

<span data-ttu-id="8992a-4048">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4048">8</span></span>

<span data-ttu-id="8992a-4049">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4049">9</span></span>

<span data-ttu-id="8992a-4050">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4050">2</span></span><br/> <span data-ttu-id="8992a-4051">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4051">0</span></span><br/>

<span data-ttu-id="8992a-4052">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4052">1</span></span>

<span data-ttu-id="8992a-4053">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4053">2</span></span>

<span data-ttu-id="8992a-4054">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4054">3</span></span>

<span data-ttu-id="8992a-4055">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4055">4</span></span>

<span data-ttu-id="8992a-4056">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4056">5</span></span>

<span data-ttu-id="8992a-4057">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4057">6</span></span>

<span data-ttu-id="8992a-4058">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4058">7</span></span>

<span data-ttu-id="8992a-4059">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4059">8</span></span>

<span data-ttu-id="8992a-4060">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4060">9</span></span>

<span data-ttu-id="8992a-4061">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4061">3</span></span><br/> <span data-ttu-id="8992a-4062">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4062">0</span></span><br/>

<span data-ttu-id="8992a-4063">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4063">1</span></span>

<span data-ttu-id="8992a-4064">\_numerator</span><span class="sxs-lookup"><span data-stu-id="8992a-4064">\_numerator</span></span>

<span data-ttu-id="8992a-4065">\_denominator</span><span class="sxs-lookup"><span data-stu-id="8992a-4065">\_denominator</span></span>



 

<span data-ttu-id="8992a-4066">**\_ numerator**: un Unsigned Integer a 32 bit contenente il numero di riga del segnalibro nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="8992a-4067">Se non sono presenti righe, questo campo deve essere impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="8992a-4068">**\_ denominatore**: Unsigned Integer a 32 bit contenente il numero di righe nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="8992a-4069">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="8992a-4070">Il messaggio CPMCompareBmkIn richiede un confronto tra due segnalibri in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="8992a-4071">Il formato del messaggio CPMCompareBmkIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-4072">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4072">0</span></span>

<span data-ttu-id="8992a-4073">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4073">1</span></span>

<span data-ttu-id="8992a-4074">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4074">2</span></span>

<span data-ttu-id="8992a-4075">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4075">3</span></span>

<span data-ttu-id="8992a-4076">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4076">4</span></span>

<span data-ttu-id="8992a-4077">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4077">5</span></span>

<span data-ttu-id="8992a-4078">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4078">6</span></span>

<span data-ttu-id="8992a-4079">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4079">7</span></span>

<span data-ttu-id="8992a-4080">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4080">8</span></span>

<span data-ttu-id="8992a-4081">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4081">9</span></span>

<span data-ttu-id="8992a-4082">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4082">1</span></span><br/> <span data-ttu-id="8992a-4083">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4083">0</span></span><br/>

<span data-ttu-id="8992a-4084">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4084">1</span></span>

<span data-ttu-id="8992a-4085">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4085">2</span></span>

<span data-ttu-id="8992a-4086">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4086">3</span></span>

<span data-ttu-id="8992a-4087">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4087">4</span></span>

<span data-ttu-id="8992a-4088">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4088">5</span></span>

<span data-ttu-id="8992a-4089">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4089">6</span></span>

<span data-ttu-id="8992a-4090">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4090">7</span></span>

<span data-ttu-id="8992a-4091">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4091">8</span></span>

<span data-ttu-id="8992a-4092">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4092">9</span></span>

<span data-ttu-id="8992a-4093">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4093">2</span></span><br/> <span data-ttu-id="8992a-4094">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4094">0</span></span><br/>

<span data-ttu-id="8992a-4095">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4095">1</span></span>

<span data-ttu-id="8992a-4096">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4096">2</span></span>

<span data-ttu-id="8992a-4097">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4097">3</span></span>

<span data-ttu-id="8992a-4098">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4098">4</span></span>

<span data-ttu-id="8992a-4099">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4099">5</span></span>

<span data-ttu-id="8992a-4100">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4100">6</span></span>

<span data-ttu-id="8992a-4101">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4101">7</span></span>

<span data-ttu-id="8992a-4102">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4102">8</span></span>

<span data-ttu-id="8992a-4103">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4103">9</span></span>

<span data-ttu-id="8992a-4104">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4104">3</span></span><br/> <span data-ttu-id="8992a-4105">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4105">0</span></span><br/>

<span data-ttu-id="8992a-4106">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4106">1</span></span>

<span data-ttu-id="8992a-4107">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8992a-4107">\_hCursor</span></span>

<span data-ttu-id="8992a-4108">\_Cap</span><span class="sxs-lookup"><span data-stu-id="8992a-4108">\_chapt</span></span>

<span data-ttu-id="8992a-4109">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="8992a-4109">\_bmkFirst</span></span>

<span data-ttu-id="8992a-4110">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="8992a-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="8992a-4111">\_**hCursor**: valore a 32 bit che rappresenta l'handle del messaggio CPMCreateQueryOut per il set di righe contenente i segnalibri.</span><span class="sxs-lookup"><span data-stu-id="8992a-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="8992a-4112">\_**Chapt**: valore a 32 bit che rappresenta l'handle del capitolo contenente i segnalibri da confrontare.</span><span class="sxs-lookup"><span data-stu-id="8992a-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="8992a-4113">\_**bmkFirst**: valore a 32 bit che rappresenta l'handle del primo segnalibro da confrontare.</span><span class="sxs-lookup"><span data-stu-id="8992a-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="8992a-4114">\_**bmkSecond**: valore a 32 bit che rappresenta l'handle per il secondo segnalibro da confrontare.</span><span class="sxs-lookup"><span data-stu-id="8992a-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="8992a-4115">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="8992a-4116">Il messaggio CPMCompareBmkOut risponde a un messaggio CPMCompareBmkIn con il confronto dei due segnalibri nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="8992a-4117">Il formato del messaggio CPMCompareBmkOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-4118">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4118">0</span></span>

<span data-ttu-id="8992a-4119">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4119">1</span></span>

<span data-ttu-id="8992a-4120">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4120">2</span></span>

<span data-ttu-id="8992a-4121">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4121">3</span></span>

<span data-ttu-id="8992a-4122">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4122">4</span></span>

<span data-ttu-id="8992a-4123">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4123">5</span></span>

<span data-ttu-id="8992a-4124">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4124">6</span></span>

<span data-ttu-id="8992a-4125">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4125">7</span></span>

<span data-ttu-id="8992a-4126">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4126">8</span></span>

<span data-ttu-id="8992a-4127">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4127">9</span></span>

<span data-ttu-id="8992a-4128">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4128">1</span></span><br/> <span data-ttu-id="8992a-4129">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4129">0</span></span><br/>

<span data-ttu-id="8992a-4130">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4130">1</span></span>

<span data-ttu-id="8992a-4131">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4131">2</span></span>

<span data-ttu-id="8992a-4132">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4132">3</span></span>

<span data-ttu-id="8992a-4133">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4133">4</span></span>

<span data-ttu-id="8992a-4134">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4134">5</span></span>

<span data-ttu-id="8992a-4135">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4135">6</span></span>

<span data-ttu-id="8992a-4136">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4136">7</span></span>

<span data-ttu-id="8992a-4137">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4137">8</span></span>

<span data-ttu-id="8992a-4138">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4138">9</span></span>

<span data-ttu-id="8992a-4139">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4139">2</span></span><br/> <span data-ttu-id="8992a-4140">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4140">0</span></span><br/>

<span data-ttu-id="8992a-4141">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4141">1</span></span>

<span data-ttu-id="8992a-4142">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4142">2</span></span>

<span data-ttu-id="8992a-4143">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4143">3</span></span>

<span data-ttu-id="8992a-4144">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4144">4</span></span>

<span data-ttu-id="8992a-4145">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4145">5</span></span>

<span data-ttu-id="8992a-4146">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4146">6</span></span>

<span data-ttu-id="8992a-4147">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4147">7</span></span>

<span data-ttu-id="8992a-4148">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4148">8</span></span>

<span data-ttu-id="8992a-4149">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4149">9</span></span>

<span data-ttu-id="8992a-4150">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4150">3</span></span><br/> <span data-ttu-id="8992a-4151">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4151">0</span></span><br/>

<span data-ttu-id="8992a-4152">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4152">1</span></span>

<span data-ttu-id="8992a-4153">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="8992a-4153">\_dwComparison</span></span>



 

<span data-ttu-id="8992a-4154">\_**dwComparison**: uno dei valori seguenti, che indica le posizioni relative dei due segnalibri nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="8992a-4155">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-4155">Value</span></span>                               | <span data-ttu-id="8992a-4156">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8992a-4157">DBCOMPARE \_ lt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="8992a-4158">Il primo segnalibro viene posizionato prima del secondo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="8992a-4159">\_0x00000001 DBCOMPARE EQ</span><span class="sxs-lookup"><span data-stu-id="8992a-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="8992a-4160">Il primo segnalibro ha la stessa posizione del secondo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="8992a-4161">DBCOMPARE \_ gt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8992a-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="8992a-4162">Il primo segnalibro viene posizionato dopo il secondo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="8992a-4163">DBCOMPARE \_ ne 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8992a-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="8992a-4164">Il primo segnalibro non ha la stessa posizione del secondo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="8992a-4165">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8992a-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="8992a-4166">Il primo segnalibro non è confrontabile con il secondo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="8992a-4167">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="8992a-4168">Il messaggio CPMRestartPositionIn sposta la posizione di recupero di un cursore all'inizio del capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="8992a-4169">Come specificato nella sezione 3.1.5.2.12, il server risponderà usando lo stesso messaggio, con i risultati della richiesta contenuti nel \_ campo status dell'intestazione CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="8992a-4170">Il formato del messaggio CPMRestartPositionIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-4171">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4171">0</span></span>

<span data-ttu-id="8992a-4172">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4172">1</span></span>

<span data-ttu-id="8992a-4173">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4173">2</span></span>

<span data-ttu-id="8992a-4174">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4174">3</span></span>

<span data-ttu-id="8992a-4175">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4175">4</span></span>

<span data-ttu-id="8992a-4176">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4176">5</span></span>

<span data-ttu-id="8992a-4177">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4177">6</span></span>

<span data-ttu-id="8992a-4178">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4178">7</span></span>

<span data-ttu-id="8992a-4179">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4179">8</span></span>

<span data-ttu-id="8992a-4180">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4180">9</span></span>

<span data-ttu-id="8992a-4181">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4181">1</span></span><br/> <span data-ttu-id="8992a-4182">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4182">0</span></span><br/>

<span data-ttu-id="8992a-4183">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4183">1</span></span>

<span data-ttu-id="8992a-4184">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4184">2</span></span>

<span data-ttu-id="8992a-4185">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4185">3</span></span>

<span data-ttu-id="8992a-4186">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4186">4</span></span>

<span data-ttu-id="8992a-4187">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4187">5</span></span>

<span data-ttu-id="8992a-4188">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4188">6</span></span>

<span data-ttu-id="8992a-4189">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4189">7</span></span>

<span data-ttu-id="8992a-4190">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4190">8</span></span>

<span data-ttu-id="8992a-4191">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4191">9</span></span>

<span data-ttu-id="8992a-4192">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4192">2</span></span><br/> <span data-ttu-id="8992a-4193">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4193">0</span></span><br/>

<span data-ttu-id="8992a-4194">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4194">1</span></span>

<span data-ttu-id="8992a-4195">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4195">2</span></span>

<span data-ttu-id="8992a-4196">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4196">3</span></span>

<span data-ttu-id="8992a-4197">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4197">4</span></span>

<span data-ttu-id="8992a-4198">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4198">5</span></span>

<span data-ttu-id="8992a-4199">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4199">6</span></span>

<span data-ttu-id="8992a-4200">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4200">7</span></span>

<span data-ttu-id="8992a-4201">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4201">8</span></span>

<span data-ttu-id="8992a-4202">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4202">9</span></span>

<span data-ttu-id="8992a-4203">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4203">3</span></span><br/> <span data-ttu-id="8992a-4204">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4204">0</span></span><br/>

<span data-ttu-id="8992a-4205">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4205">1</span></span>

<span data-ttu-id="8992a-4206">\_hCursor (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="8992a-4207">\_Chapt (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="8992a-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="8992a-4208">**\_ hCursor**: valore a 32 bit che rappresenta l'handle, ottenuto da un messaggio CPMCreateQueryOut che identifica la query per la quale riavviare la posizione.</span><span class="sxs-lookup"><span data-stu-id="8992a-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="8992a-4209">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8992a-4210">**\_ Chapt**: valore a 32 bit che rappresenta l'handle di un capitolo dal quale recuperare le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="8992a-4211">Questo campo deve essere presente quando il messaggio viene inviato dal client e deve essere assente quando il messaggio viene inviato dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="8992a-4212">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="8992a-4213">Il messaggio CPMFreeCursorIn richiede il rilascio di un cursore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="8992a-4214">Il formato del messaggio CPMFreeCursorIn che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="8992a-4215">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4215">0</span></span>

<span data-ttu-id="8992a-4216">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4216">1</span></span>

<span data-ttu-id="8992a-4217">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4217">2</span></span>

<span data-ttu-id="8992a-4218">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4218">3</span></span>

<span data-ttu-id="8992a-4219">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4219">4</span></span>

<span data-ttu-id="8992a-4220">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4220">5</span></span>

<span data-ttu-id="8992a-4221">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4221">6</span></span>

<span data-ttu-id="8992a-4222">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4222">7</span></span>

<span data-ttu-id="8992a-4223">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4223">8</span></span>

<span data-ttu-id="8992a-4224">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4224">9</span></span>

<span data-ttu-id="8992a-4225">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4225">1</span></span><br/> <span data-ttu-id="8992a-4226">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4226">0</span></span><br/>

<span data-ttu-id="8992a-4227">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4227">1</span></span>

<span data-ttu-id="8992a-4228">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4228">2</span></span>

<span data-ttu-id="8992a-4229">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4229">3</span></span>

<span data-ttu-id="8992a-4230">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4230">4</span></span>

<span data-ttu-id="8992a-4231">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4231">5</span></span>

<span data-ttu-id="8992a-4232">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4232">6</span></span>

<span data-ttu-id="8992a-4233">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4233">7</span></span>

<span data-ttu-id="8992a-4234">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4234">8</span></span>

<span data-ttu-id="8992a-4235">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4235">9</span></span>

<span data-ttu-id="8992a-4236">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4236">2</span></span><br/> <span data-ttu-id="8992a-4237">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4237">0</span></span><br/>

<span data-ttu-id="8992a-4238">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4238">1</span></span>

<span data-ttu-id="8992a-4239">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4239">2</span></span>

<span data-ttu-id="8992a-4240">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4240">3</span></span>

<span data-ttu-id="8992a-4241">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4241">4</span></span>

<span data-ttu-id="8992a-4242">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4242">5</span></span>

<span data-ttu-id="8992a-4243">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4243">6</span></span>

<span data-ttu-id="8992a-4244">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4244">7</span></span>

<span data-ttu-id="8992a-4245">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4245">8</span></span>

<span data-ttu-id="8992a-4246">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4246">9</span></span>

<span data-ttu-id="8992a-4247">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4247">3</span></span><br/> <span data-ttu-id="8992a-4248">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4248">0</span></span><br/>

<span data-ttu-id="8992a-4249">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4249">1</span></span>

<span data-ttu-id="8992a-4250">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8992a-4250">\_hCursor</span></span>



 

<span data-ttu-id="8992a-4251">**\_ hCursor**: valore a 32 bit che rappresenta l'handle del cursore dal messaggio CPMCreateQueryOut da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="8992a-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="8992a-4252">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="8992a-4253">Il messaggio CPMFreeCursorOut risponde a un messaggio CPMFreeCursorIn con i risultati della liberazione di un cursore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="8992a-4254">Il formato del messaggio CPMFreeCursorOut che segue l'intestazione è:</span><span class="sxs-lookup"><span data-stu-id="8992a-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="8992a-4255">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4255">0</span></span>

<span data-ttu-id="8992a-4256">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4256">1</span></span>

<span data-ttu-id="8992a-4257">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4257">2</span></span>

<span data-ttu-id="8992a-4258">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4258">3</span></span>

<span data-ttu-id="8992a-4259">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4259">4</span></span>

<span data-ttu-id="8992a-4260">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4260">5</span></span>

<span data-ttu-id="8992a-4261">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4261">6</span></span>

<span data-ttu-id="8992a-4262">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4262">7</span></span>

<span data-ttu-id="8992a-4263">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4263">8</span></span>

<span data-ttu-id="8992a-4264">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4264">9</span></span>

<span data-ttu-id="8992a-4265">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4265">1</span></span><br/> <span data-ttu-id="8992a-4266">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4266">0</span></span><br/>

<span data-ttu-id="8992a-4267">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4267">1</span></span>

<span data-ttu-id="8992a-4268">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4268">2</span></span>

<span data-ttu-id="8992a-4269">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4269">3</span></span>

<span data-ttu-id="8992a-4270">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4270">4</span></span>

<span data-ttu-id="8992a-4271">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4271">5</span></span>

<span data-ttu-id="8992a-4272">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4272">6</span></span>

<span data-ttu-id="8992a-4273">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4273">7</span></span>

<span data-ttu-id="8992a-4274">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4274">8</span></span>

<span data-ttu-id="8992a-4275">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4275">9</span></span>

<span data-ttu-id="8992a-4276">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4276">2</span></span><br/> <span data-ttu-id="8992a-4277">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4277">0</span></span><br/>

<span data-ttu-id="8992a-4278">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4278">1</span></span>

<span data-ttu-id="8992a-4279">2</span><span class="sxs-lookup"><span data-stu-id="8992a-4279">2</span></span>

<span data-ttu-id="8992a-4280">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4280">3</span></span>

<span data-ttu-id="8992a-4281">4</span><span class="sxs-lookup"><span data-stu-id="8992a-4281">4</span></span>

<span data-ttu-id="8992a-4282">5</span><span class="sxs-lookup"><span data-stu-id="8992a-4282">5</span></span>

<span data-ttu-id="8992a-4283">6</span><span class="sxs-lookup"><span data-stu-id="8992a-4283">6</span></span>

<span data-ttu-id="8992a-4284">7</span><span class="sxs-lookup"><span data-stu-id="8992a-4284">7</span></span>

<span data-ttu-id="8992a-4285">8</span><span class="sxs-lookup"><span data-stu-id="8992a-4285">8</span></span>

<span data-ttu-id="8992a-4286">9</span><span class="sxs-lookup"><span data-stu-id="8992a-4286">9</span></span>

<span data-ttu-id="8992a-4287">3</span><span class="sxs-lookup"><span data-stu-id="8992a-4287">3</span></span><br/> <span data-ttu-id="8992a-4288">0</span><span class="sxs-lookup"><span data-stu-id="8992a-4288">0</span></span><br/>

<span data-ttu-id="8992a-4289">1</span><span class="sxs-lookup"><span data-stu-id="8992a-4289">1</span></span>

<span data-ttu-id="8992a-4290">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="8992a-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="8992a-4291">**\_ cCursorsRemaining**: Unsigned Integer a 32 bit che indica il numero di cursori ancora in uso per la query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="8992a-4292">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="8992a-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="8992a-4293">Il messaggio CPMDisconnect termina la connessione con il server</span><span class="sxs-lookup"><span data-stu-id="8992a-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="8992a-4294">Il messaggio non deve includere un corpo; è necessario inviare solo l'intestazione del messaggio, come specificato nella sezione 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="8992a-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="8992a-4295">2.2.4 errori</span><span class="sxs-lookup"><span data-stu-id="8992a-4295">2.2.4 Errors</span></span>

<span data-ttu-id="8992a-4296">Tutti i messaggi del protocollo del servizio di indicizzazione del contenuto devono restituire 0x00000000 in caso di successo; in caso contrario, restituiscono un codice di errore diverso da zero a 32 bit che può essere un valore HRESULT o un valore NTSTATUS (vedere la sezione 1,8).</span><span class="sxs-lookup"><span data-stu-id="8992a-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="8992a-4297">Se un buffer è troppo piccolo per adattarsi a un risultato, è \_ necessario che venga restituito un codice di stato risorse insufficienti \_ (0XC0000009A) e che l'operazione non riuscita venga ritentata con un buffer più grande.</span><span class="sxs-lookup"><span data-stu-id="8992a-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="8992a-4298">Tutti gli altri valori di errore devono essere considerati uguali.</span><span class="sxs-lookup"><span data-stu-id="8992a-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="8992a-4299">Si noti che attualmente gli spazi di numerazione HRESULT e NTSTATUS non si sovrappongono, tranne che con valori di significato identico, ma anche se sono in conflitto in futuro, non si verificheranno problemi di protocollo purché il valore per lo stato \_ Le \_ risorse insufficienti rimangono univoche, in quanto tutti gli altri valori di errore vengono considerati uguali.</span><span class="sxs-lookup"><span data-stu-id="8992a-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="8992a-4300">3 Dettagli del protocollo</span><span class="sxs-lookup"><span data-stu-id="8992a-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="8992a-4301">3,1 Dettagli server</span><span class="sxs-lookup"><span data-stu-id="8992a-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="8992a-4302">3,2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="8992a-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="8992a-4303">Le richieste di messaggi CISP per l'esecuzione di query remote sui cataloghi dei servizi di indicizzazione non richiedono una sequenza specifica.</span><span class="sxs-lookup"><span data-stu-id="8992a-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="8992a-4304">È consigliabile che il livello più alto rispetti una sequenza di messaggi significativa, tuttavia, come per i messaggi ricevuti da questa sequenza o con dati non validi, il server risponderà con un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="8992a-4305">Alcuni messaggi dipendono anche dal livello superiore che fornisce dati validi ricevuti nei messaggi precedenti nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="8992a-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="8992a-4306">Nel diagramma seguente viene illustrata una tipica sequenza di messaggi per una query semplice da un client a un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="8992a-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![sequenza di messaggi per query semplice](images/protocoldetails.jpg)

<span data-ttu-id="8992a-4308">I messaggi rappresentati nel diagramma precedente rappresentano un subset di tutti i messaggi CISP usati per eseguire query su un catalogo di servizi di indicizzazione remota.</span><span class="sxs-lookup"><span data-stu-id="8992a-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="8992a-4309">3,1 Dettagli server</span><span class="sxs-lookup"><span data-stu-id="8992a-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="8992a-4310">3.1.1 Modello di dati astratto</span><span class="sxs-lookup"><span data-stu-id="8992a-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="8992a-4311">Nella sezione seguente vengono specificati i dati e lo stato gestiti dal server CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="8992a-4312">I dati forniti sono per semplificare la spiegazione del comportamento del protocollo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="8992a-4313">Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il loro comportamento esterno sia coerente con quello descritto in questo documento.</span><span class="sxs-lookup"><span data-stu-id="8992a-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="8992a-4314">Un servizio di indicizzazione che implementa CISP deve mantenere gli elementi dati astratti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="8992a-4315">Elenco dei client connessi al server</span><span class="sxs-lookup"><span data-stu-id="8992a-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="8992a-4316">Informazioni su ogni client, che include:</span><span class="sxs-lookup"><span data-stu-id="8992a-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="8992a-4317">Versione del client (come indicato nel messaggio CPMConnectIn specificato nella sezione 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="8992a-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="8992a-4318">Catalogo associato al client (tramite un messaggio CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="8992a-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="8992a-4319">Proprietà client aggiuntive come specificato nella sezione 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="8992a-4320">Query di ricerca del client</span><span class="sxs-lookup"><span data-stu-id="8992a-4320">Client's search query</span></span>
    -   <span data-ttu-id="8992a-4321">Elenco di handle del cursore per la query e la posizione nel set di risultati per ogni handle.</span><span class="sxs-lookup"><span data-stu-id="8992a-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="8992a-4322">Set corrente di associazioni</span><span class="sxs-lookup"><span data-stu-id="8992a-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="8992a-4323">Stato corrente della query che include (per ogni cursore):</span><span class="sxs-lookup"><span data-stu-id="8992a-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="8992a-4324">Numero di righe nel risultato della query</span><span class="sxs-lookup"><span data-stu-id="8992a-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="8992a-4325">Numeratore e denominatore del completamento delle query</span><span class="sxs-lookup"><span data-stu-id="8992a-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="8992a-4326">Ultimo numero di righe, segnalato dal messaggio CPMRatioFinishedOut più recente per questo cursore</span><span class="sxs-lookup"><span data-stu-id="8992a-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="8992a-4327">Indica se la query viene monitorata dal server per le modifiche nei risultati della query e se viene monitorata, cosa è cambiato nei risultati della query dall'ultima segnalazione al client da parte di CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="8992a-4328">Elenco di handle dei capitoli, serviti da questa query a un client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="8992a-4329">Elenco di handle di segnalibro per ogni cursore, servito da questa query a un client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="8992a-4330">Stato corrente del servizio di indicizzazione, che può essere "non inizializzato", "in esecuzione" o "arresto".</span><span class="sxs-lookup"><span data-stu-id="8992a-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="8992a-4331">Si noti che la maggior parte del tempo del server si trova nello stato "in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="8992a-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="8992a-4332">Di seguito è riportato il diagramma della macchina a stati per il server:</span><span class="sxs-lookup"><span data-stu-id="8992a-4332">Following is the state machine diagram for the server:</span></span>

    ![diagramma della macchina a Stati del server del servizio di indicizzazione](images/abstractdatamodel.jpg)

-   <span data-ttu-id="8992a-4334">Informazioni per catalogo: numero di documenti indicizzati, dimensioni dell'indice, numero di chiavi univoche e così via (vedere la sezione 2.2.3.1 per l'elenco completo), stato (che corrisponde ai valori di dwNewState nella sezione 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="8992a-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="8992a-4335">Per ogni lingua supportata, un database di varianti di parole, come illustrato nella sezione 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="8992a-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="8992a-4336">3.1.2 Timer</span><span class="sxs-lookup"><span data-stu-id="8992a-4336">3.1.2 Timers</span></span>

<span data-ttu-id="8992a-4337">Non sono richiesti timer del protocollo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="8992a-4338">3.1.3 Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="8992a-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="8992a-4339">Al momento dell'inizializzazione, il server deve impostare lo stato su "non inizializzato" e iniziare l'ascolto dei messaggi nell'named pipe specificato nella sezione 1,9.</span><span class="sxs-lookup"><span data-stu-id="8992a-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="8992a-4340">Dopo l'esecuzione di qualsiasi altra inizializzazione interna, deve passare allo stato "Running".</span><span class="sxs-lookup"><span data-stu-id="8992a-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="8992a-4341">3.1.4 Eventi attivati di livello più alto</span><span class="sxs-lookup"><span data-stu-id="8992a-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="8992a-4342">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="8992a-4343">Regole di sequenziazione e elaborazione dei messaggi 3.1.5</span><span class="sxs-lookup"><span data-stu-id="8992a-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="8992a-4344">Ogni volta che si verifica un errore durante l'elaborazione di un messaggio inviato da un client, il server deve segnalare un errore al client nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="8992a-4345">Interrompi elaborazione del messaggio inviato dal client</span><span class="sxs-lookup"><span data-stu-id="8992a-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="8992a-4346">Rispondere con l'intestazione del messaggio (solo) del messaggio inviato dal client, mantenendo \_ intatto il campo msg.</span><span class="sxs-lookup"><span data-stu-id="8992a-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="8992a-4347">Impostare il \_ campo stato sul valore del codice di errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="8992a-4348">Quando arriva un messaggio, il server deve controllare il \_ valore del campo msg per verificare se è un tipo noto (vedere la sezione 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="8992a-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="8992a-4349">Se il tipo non è noto, deve segnalare un errore di \_ parametro di stato non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="8992a-4350">Il server deve quindi convalidare il \_ valore del campo ulChecksum se il tipo di messaggio è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="8992a-4351">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="8992a-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="8992a-4352">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="8992a-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="8992a-4353">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="8992a-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="8992a-4354">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="8992a-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="8992a-4355">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="8992a-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="8992a-4356">Per convalidare il \_ valore del campo ulChecksum, il server deve controllare il valore specificato dal client nel \_ campo iClientVersion del messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="8992a-4357">Se il \_ campo iClientVersion non è impostato su 0x00000008 e il \_ campo ulChecksum non è impostato su 0x00000000, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="8992a-4358">Il server non deve convalidare il \_ campo ulChecksum per i client impostando il \_ campo iClientVersion su un valore minore di 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="8992a-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="8992a-4359">Se il \_ valore del campo iClientVersionfield è 0x00000008 o superiore, il server deve verificare che il \_ campo ulChecksum sia stato calcolato come specificato nella sezione 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="8992a-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="8992a-4360">Se il \_ valore ulChecksum non è valido, è necessario che il server segnali un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="8992a-4361">Successivamente, il server verifica lo stato in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="8992a-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="8992a-4362">Se lo stato è "non inizializzato", il server deve segnalare \_ un \_ errore ci E non \_ inizializzato (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="8992a-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="8992a-4363">Se lo stato è "chiusura in corso", il server deve segnalare un \_ errore ci E \_ Shutdown (0x80041812).</span><span class="sxs-lookup"><span data-stu-id="8992a-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="8992a-4364">Quando un'intestazione è stata determinata come valida e lo stato del server è "in esecuzione", è necessario eseguire un'ulteriore elaborazione specifica del messaggio come specificato nelle sottosezioni riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="8992a-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="8992a-4365">Gestione del catalogo di servizi di indicizzazione remota di 3.1.5.1</span><span class="sxs-lookup"><span data-stu-id="8992a-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="8992a-4366">3.1.5.1.1 che riceve una richiesta CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="8992a-4367">Quando il server riceve una richiesta di messaggio CPMCIStateInOut dal client, il server deve prima verificare se il client si trova in un elenco di client connessi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="8992a-4368">Se il client non è presente nell'elenco, il server deve segnalare un \_ errore di parametro di stato non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="8992a-4369">In caso contrario, deve rispondere al client con un messaggio CPMCIStateInOut, inserendolo con informazioni sul catalogo associato del client come specificato nella sezione 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="8992a-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="8992a-4370">3.1.5.1.2 che riceve una richiesta CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="8992a-4371">Quando il server riceve una richiesta di messaggio CPMSetCatStateIn dal client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4372">Verificare che il client disponga dell'accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4372">Check that client has administrative access.</span></span> <span data-ttu-id="8992a-4373">Se il client non dispone di accesso amministrativo, il server deve segnalare un errore di stato \_ accesso \_ negato (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="8992a-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="8992a-4374">Se \_ dwNewState è diverso da CICAT \_ tutti \_ aperti, modificare lo stato del catalogo specificato nel campo CatName come specificato dal \_ campo dwNewState.</span><span class="sxs-lookup"><span data-stu-id="8992a-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="8992a-4375">Per ulteriori informazioni, vedere la sezione 2.2.3.2.</span><span class="sxs-lookup"><span data-stu-id="8992a-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="8992a-4376">Se il server non individua un catalogo con il nome specificato nel campo CatName, il server deve restituire un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4377">Rispondere al client con un messaggio CPMSetCatStateOut, in cui \_ DWOLDSTATE deve essere impostato sullo stato precedente del catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="8992a-4378">Se \_ dwNewState è uguale a CICAT \_ tutti \_ aperti, il server deve controllare lo stato di tutti i cataloghi e, se tutti gli elementi vengono avviati \_ , deve impostare dwOldState su 0x00000001 e in caso contrario impostare \_ dwOldState su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="8992a-4379">3.1.5.1.3 che riceve una richiesta CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="8992a-4380">Quando il server riceve una richiesta di messaggio CPMUpdateDocumentsIn, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4381">Controllare se il client si trova in un elenco di client connessi (a cui è associato un catalogo).</span><span class="sxs-lookup"><span data-stu-id="8992a-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="8992a-4382">Se il client non è presente nell'elenco, il server deve segnalare un \_ errore di parametro di stato non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4383">Verificare che il client disponga dell'accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4383">Check that client has administrative access.</span></span> <span data-ttu-id="8992a-4384">Se il client non dispone di accesso amministrativo al server, il server deve segnalare un errore di stato \_ accesso \_ negato (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="8992a-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="8992a-4385">Avviare il processo di indicizzazione del percorso specificato dal client, eseguendo un'analisi completa o incrementale, a seconda del valore del \_ campo del flag nel messaggio CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="8992a-4386">Se il percorso non è stato indicizzato in precedenza, deve essere aggiunto alla raccolta di percorsi indicizzati ed è stata eseguita un'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="8992a-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="8992a-4387">Se viene specificato un valore non valido \_ per il campo del flag, il server deve agire come se \_ flag fosse stato impostato su UPD \_ init ed eseguire un'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="8992a-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="8992a-4388">Questa operazione deve essere eseguita nel catalogo associato al client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="8992a-4389">Rispondere al client con l'intestazione del messaggio per il CPMUpdateDocumentsIn e impostare il \_ campo stato sui risultati della richiesta.</span><span class="sxs-lookup"><span data-stu-id="8992a-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="8992a-4390">3.1.5.1.4 che riceve una richiesta CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="8992a-4391">Quando il server riceve una richiesta di messaggio CPMForceMergeIn, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4392">Controllare se il client si trova in un elenco di client connessi (a cui è associato un catalogo).</span><span class="sxs-lookup"><span data-stu-id="8992a-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="8992a-4393">Se il client non è presente nell'elenco, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4394">Verificare che il client disponga dell'accesso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4394">Check that client has administrative access.</span></span> <span data-ttu-id="8992a-4395">Se il client non dispone di accesso amministrativo, il server deve segnalare un errore di stato \_ accesso \_ negato (0xc0000022).</span><span class="sxs-lookup"><span data-stu-id="8992a-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="8992a-4396">Avviare qualsiasi processo di manutenzione necessario per migliorare le prestazioni di esecuzione delle query in un catalogo, associato al client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="8992a-4397">Rispondere al client con un'intestazione del messaggio per il CPMForceMergeIn e impostare il \_ campo stato sui risultati della richiesta.</span><span class="sxs-lookup"><span data-stu-id="8992a-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="8992a-4398">Si noti che il processo di manutenzione è asincrono e può continuare dopo la ricezione del messaggio di risposta da parte del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="8992a-4399">Questo processo non influisca direttamente sul protocollo in alcun modo, ad eccezione del tempo di risposta.</span><span class="sxs-lookup"><span data-stu-id="8992a-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="8992a-4400">Esecuzione di query sul servizio di indicizzazione remota 3.1.5.2</span><span class="sxs-lookup"><span data-stu-id="8992a-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="8992a-4401">3.1.5.2.1 che riceve una richiesta CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="8992a-4402">Quando il server riceve una richiesta CPMConnectIn da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4403">Controllare se il client è nell'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="8992a-4404">In tal caso, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4405">Verifica se il catalogo specificato esiste e non è nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="8992a-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="8992a-4406">In caso contrario, il server deve essere un \_ \_ errore di 0X8004181D (ci E \_ No Catalog) del report.</span><span class="sxs-lookup"><span data-stu-id="8992a-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="8992a-4407">Aggiungere il client all'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="8992a-4408">Associare il catalogo al client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="8992a-4409">Archiviare le informazioni passate nel messaggio CPMConnectIn, ad esempio il nome del catalogo, la versione del client e così via, nello stato del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="8992a-4410">Rispondere al client con un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="8992a-4411">3.1.5.2.2 che riceve una richiesta CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="8992a-4412">Quando il server riceve una richiesta di messaggio CPMCreateQueryIn da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4413">Controllare se il client è nell'elenco dei client connessi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="8992a-4414">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4415">Controllare se il client dispone già di una query associata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="8992a-4416">In tal caso, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4417">Controllare se il catalogo associato al client si trova nello stato che consente l'elaborazione della query (CICAT \_ ReadOnly o CICAT \_ scrivibile).</span><span class="sxs-lookup"><span data-stu-id="8992a-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="8992a-4418">In caso contrario, il server deve segnalare un errore di query \_ S \_ senza \_ query (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="8992a-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="8992a-4419">Analizza il set di restrizioni, gli ordinamenti e i raggruppamenti specificati nella query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="8992a-4420">Se il server rileva un errore, deve segnalare un errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="8992a-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="8992a-4421">Se questo passaggio ha esito negativo per qualsiasi altro motivo, il server deve segnalare l'errore rilevato.</span><span class="sxs-lookup"><span data-stu-id="8992a-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="8992a-4422">Per informazioni sugli errori di query del servizio di indicizzazione, vedere \[ MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="8992a-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="8992a-4423">Salvare la query di ricerca nello stato del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="8992a-4424">Apportare le preparazioni necessarie per gestire le righe a un client e associare la query ai cursori appropriati (a seconda delle informazioni passate nel messaggio CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="8992a-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="8992a-4425">Aggiungere gli handle all'elenco di handle del cursore del client e inizializzare gli elenchi di punti di manipolazione e segnalibri del capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="8992a-4426">Inizializza l'elenco di handle del capitolo per ogni cursore in questa query su DB \_ null \_ hChapter</span><span class="sxs-lookup"><span data-stu-id="8992a-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="8992a-4427">Inizializza l'elenco di handle di segnalibro per ogni cursore in questa query su un set di DBBMK \_ First e DBBMK \_ Last.</span><span class="sxs-lookup"><span data-stu-id="8992a-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="8992a-4428">Contrassegnare la query come non monitorata per le modifiche.</span><span class="sxs-lookup"><span data-stu-id="8992a-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="8992a-4429">Inizializza il numero di righe sul numero di righe attualmente calcolato, che può essere 0 se la query non è stata avviata o un numero se la query è in un processo di esecuzione, e inizializza il numeratore e il denominatore del completamento della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="8992a-4430">Rispondere al client con un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="8992a-4431">3.1.5.2.3 che riceve una richiesta CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="8992a-4432">Quando il server riceve una richiesta di messaggio CPMGetQueryStatusIn da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4433">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="8992a-4434">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4435">Controllare se l'handle del cursore si trova in un elenco di handle del cursore del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="8992a-4436">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4437">Preparare un messaggio CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="8992a-4438">Il server deve recuperare lo stato corrente della query e impostarlo nel \_ campo QStatus. per i valori possibili, vedere 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="8992a-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="8992a-4439">Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8992a-4440">Rispondere al client con il messaggio CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="8992a-4441">3.1.5.2.4 che riceve una richiesta CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="8992a-4442">Quando il server riceve una richiesta di messaggio CPMGetQueryStatusExIn da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4443">Controllare se il client dispone di una query associata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8992a-4444">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4445">Controllare se l'handle del cursore passato si trova in un elenco di handle del cursore del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="8992a-4446">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4447">Preparare un messaggio CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="8992a-4448">Il server deve recuperare lo stato della query corrente e lo stato di avanzamento della query e impostare QStatus (vedere 2.2.3.11 per i valori possibili), \_ rispettivamente dwRatioFinishedDenominator e \_ dwRatioFinishedNumerator.</span><span class="sxs-lookup"><span data-stu-id="8992a-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="8992a-4449">DEVE quindi impostare il numero di righe nei risultati della query su \_ cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="8992a-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="8992a-4450">Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8992a-4451">Recuperare informazioni sul catalogo del client e compilare \_ cFilteredDocuments e \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="8992a-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="8992a-4452">Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8992a-4453">Recuperare la posizione del segnalibro indicato dall'handle nel \_ campo BMK e riempire il campo iRowBmk rimanente \_ nel messaggio CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="8992a-4454">Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8992a-4455">Rispondere al client con il messaggio CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="8992a-4456">3.1.5.2.5 che riceve una richiesta CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="8992a-4457">Quando il server riceve una richiesta di messaggio CPMRatioFinishedIn da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4458">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="8992a-4459">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4460">Controllare se l'handle del cursore passato è nell'elenco degli handle del cursore del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="8992a-4461">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4462">Preparare un messaggio CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="8992a-4463">Il server deve recuperare lo stato della query del client e compilare i \_ campi ulNumerator, \_ ulDenominator e \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="8992a-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="8992a-4464">Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8992a-4465">Se \_ Crow è uguale all'ultimo numero di righe segnalato per la query, impostare \_ fNewRows su 0x00000000. in caso contrario, impostarlo su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="8992a-4466">Aggiornare l'ultimo numero di righe segnalato per la query al valore di \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="8992a-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="8992a-4467">Rispondere al client con il messaggio CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="8992a-4468">3.1.5.2.6 che riceve una richiesta CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="8992a-4469">Quando il server riceve una richiesta di messaggio CPMSetBindingsIn da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4470">Controllare se il client dispone di una query associata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8992a-4471">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4472">Controllare se l'handle del cursore passato è nell'elenco degli handle del cursore del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="8992a-4473">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4474">Verificare che le informazioni sulle associazioni siano valide (ad esempio, la colonna almeno specifica il valore, la lunghezza o lo stato da restituire; nessuna sovrapposizione nei binding per valore, lunghezza o stato; e valore, lunghezza e stato rientrano nelle dimensioni della riga specificate) e se non segnala un \_ errore DB e \_ BADBINDINFO (0x80040E08).</span><span class="sxs-lookup"><span data-stu-id="8992a-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="8992a-4475">Salvare le informazioni di binding associate alle colonne specificate nel campo aColumns.</span><span class="sxs-lookup"><span data-stu-id="8992a-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="8992a-4476">Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8992a-4477">Rispondere al client con un'intestazione del messaggio (solo) con \_ msg impostato su CPMSetBindingsIn e \_ lo stato impostato sui risultati dell'associazione specificata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="8992a-4478">3.1.5.2.7 che riceve una richiesta CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="8992a-4479">Quando il server riceve una richiesta di messaggio CPMGetRowsIn da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4480">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="8992a-4481">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4482">Controllare se l'handle del cursore passato è in athelist degli handle del cursore del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="8992a-4483">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4484">Controllare se il client dispone di un set di associazioni corrente.</span><span class="sxs-lookup"><span data-stu-id="8992a-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="8992a-4485">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4486">Preparare un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="8992a-4487">Il server deve posizionare il cursore nei risultati della query come indicato dalla descrizione della ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="8992a-4488">Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8992a-4489">Recuperare il numero di righe che corrisponde a un buffer, le cui dimensioni sono indicate da \_ cbReadBuffer, ma non più di quelle indicate da \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="8992a-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="8992a-4490">Durante il recupero delle righe, il server deve confrontare il tipo di valore della proprietà di ogni colonna selezionata con il tipo specificato nel set di associazioni corrente del client (sezione 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="8992a-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="8992a-4491">Se il tipo nell'associazione non è una \_ variante VT, il server deve tentare di convertire il valore della proprietà della colonna in quel tipo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="8992a-4492">In caso contrario, se il \_ flag DBPROP USEEXTENDEDDBTYPES è impostato nel set di \_ proprietà DBPROPSET QUERYEXT del client o se il valore della proprietà della colonna non è un tipo di vettore VT \_ , il valore della proprietà deve essere restituito nel tipo normale.</span><span class="sxs-lookup"><span data-stu-id="8992a-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="8992a-4493">Se nessuno di questi casi (ad esempio, il server ha un \_ tipo di vettore VT e il client non supporta il \_ vettore VT), il server deve tentare di convertirlo in un tipo di matrice VT \_ come segue: VT \_ i8, VT \_ UI8, VT \_ FILETIME e \_ gli elementi della matrice CLSID VT non possono essere convertiti e non hanno esito negativo; \_ \_ Gli elementi della matrice VT LPSTR e VT LPWSTR devono essere convertiti in un \_ BSTR di tipo VT; gli elementi di matrice di tutti gli altri tipi devono rimanere invariati.</span><span class="sxs-lookup"><span data-stu-id="8992a-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="8992a-4494">Infine, se le colonne di riga contengono handle di capitolo o di segnalibri, il server deve aggiornare gli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="8992a-4495">Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8992a-4496">Archiviare il numero effettivo di righe recuperate in \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="8992a-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="8992a-4497">Copiare la descrizione della ricerca e il campo del capitolo da CPMGetRowsIn a un messaggio CPMGetRowsOut da inviare.</span><span class="sxs-lookup"><span data-stu-id="8992a-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="8992a-4498">Archiviare le righe recuperate nel campo Rows (vedere la nota sul byte di stato sotto e la sezione 2.2.3.16 sulla struttura del campo Rows).</span><span class="sxs-lookup"><span data-stu-id="8992a-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="8992a-4499">Rispondere al client con il messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="8992a-4500">Nota sul campo byte di stato:</span><span class="sxs-lookup"><span data-stu-id="8992a-4500">Note on status byte field:</span></span>

<span data-ttu-id="8992a-4501">Se StatusUsed è impostato su 0x01 in CTableColumn del messaggio CPMSetBindingIn per la colonna, il server deve impostare il byte di stato (che si trova in StatusOffset dall'inizio della riga) per la colonna su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="8992a-4502">Valore</span><span class="sxs-lookup"><span data-stu-id="8992a-4502">Value</span></span> | <span data-ttu-id="8992a-4503">Significato</span><span class="sxs-lookup"><span data-stu-id="8992a-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="8992a-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="8992a-4504">0x00</span></span>  | <span data-ttu-id="8992a-4505">StatusOK</span><span class="sxs-lookup"><span data-stu-id="8992a-4505">StatusOK</span></span>       |
| <span data-ttu-id="8992a-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="8992a-4506">0x01</span></span>  | <span data-ttu-id="8992a-4507">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="8992a-4507">StatusDeferred</span></span> |
| <span data-ttu-id="8992a-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="8992a-4508">0x02</span></span>  | <span data-ttu-id="8992a-4509">StatusNull</span><span class="sxs-lookup"><span data-stu-id="8992a-4509">StatusNull</span></span>     |



 

<span data-ttu-id="8992a-4510">Se per questa riga il valore della proprietà è assente, il server deve impostare il byte di stato su StatusNull.</span><span class="sxs-lookup"><span data-stu-id="8992a-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="8992a-4511">Se il valore è troppo grande per essere trasferito nel messaggio CPMGetRowsOut, il server deve impostare il byte di stato su StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="8992a-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="8992a-4512">In caso contrario, il server deve impostare il byte di stato su StatusOK.</span><span class="sxs-lookup"><span data-stu-id="8992a-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="8992a-4513">3.1.5.2.8 che riceve una richiesta CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="8992a-4514">Quando il server riceve una richiesta di messaggio CPMFetchValueIn da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4515">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="8992a-4516">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4517">Preparare un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="8992a-4518">Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8992a-4519">Trovare il documento indicato dal \_ campo wid e verificare se l'ID di proprietà del documento (in seguito definito "valore della proprietà") indicato dalla struttura Campo PROPSPEC è disponibile per questo client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="8992a-4520">Se questo valore non è disponibile, il server deve impostare \_ fValueExists su 0x00000000 e in caso contrario impostare \_ fValueExists su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="8992a-4521">Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8992a-4522">Se \_ fValueExists è uguale a 0x00000001, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="8992a-4523">Serializzare il valore della proprietà in una struttura SERIALIZEDPROPERTYVALUE e copiare, a partire dall' \_ offset cbSoFar, al massimo \_ cbChunk byte, ma non oltre la fine della proprietà serializzata, nel campo vValue.</span><span class="sxs-lookup"><span data-stu-id="8992a-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="8992a-4524">Se questo passaggio ha esito negativo per qualsiasi motivo, il server deve segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="8992a-4525">Impostare \_ cbValue sul numero di byte copiati nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="8992a-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="8992a-4526">Impostare vType sul tipo di proprietà del valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="8992a-4527">Se la lunghezza della proprietà serializzata è maggiore di \_ cbSoFar aggiunta a \_ cbValue, impostare \_ fMoreExists su 0x00000001. in caso contrario, impostarla su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="8992a-4528">Rispondere al client con il messaggio CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="8992a-4529">3.1.5.2.9 che riceve una richiesta CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="8992a-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="8992a-4530">Quando il server riceve un messaggio CPMGetNotify da un client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4531">Controllare se al client è associata una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="8992a-4532">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4533">Se non sono state apportate modifiche al set di risultati della query dopo l'ultimo messaggio CPMSendNotifyOut per questo client o se la query non è attualmente monitorata per le modifiche nel set di risultati, il server deve rispondere con un messaggio CPMGetNotify e iniziare a monitorare la query per le modifiche nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="8992a-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="8992a-4534">Se in un secondo momento viene apportata una modifica al set di risultati della query, il server deve inviare esattamente un messaggio CPMSendNotifyOut al client e deve specificare la modifica nel \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="8992a-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="8992a-4535">Se sono state apportate modifiche al set di risultati della query dall'ultimo messaggio CPMSendNotifyOut, il server deve rispondere con CPMSendNotifyOut e deve specificare la modifica nel \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="8992a-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="8992a-4536">Si noti che, nel caso di molte modifiche ai risultati della query, DBWATCHNOTIFY \_ ROWSCHANGED ha priorità (ad esempio, se la query è stata eseguita, rieseguita e quindi il numero di righe è stato modificato e la query è stata eseguita di nuovo, l'evento segnalato sarebbe DBWATCHNOTIFY \_ ROWSCHANGED).</span><span class="sxs-lookup"><span data-stu-id="8992a-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="8992a-4537">3.1.5.2.10 che riceve una richiesta CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="8992a-4538">Quando il server riceve una richiesta di messaggio CPMGetApproximatePositionIn dal client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4539">Controllare se il client dispone di una query associata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8992a-4540">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4541">Verificare che l'handle del cursore, l'handle del capitolo e l'handle di segnalibro passati si trovino negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="8992a-4542">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4543">Trovare una riga associata all'handle dei segnalibri nei risultati della query e approssimare la posizione della riga nel set di righe, a cui fa riferimento l'handle del capitolo e determinare il numeratore e il denominatore per la posizione.</span><span class="sxs-lookup"><span data-stu-id="8992a-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="8992a-4544">Si noti che quando l'handle del capitolo è DB \_ null \_ hChapter, il capitolo corrispondente è il set di righe principale della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="8992a-4545">Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8992a-4546">Rispondere al client con un messaggio CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="8992a-4547">3.1.5.2.11 che riceve una richiesta CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="8992a-4548">Quando il server riceve una richiesta di messaggio CPMCompareBmkIn dal client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4549">Controllare se il client dispone di una query associata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8992a-4550">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4551">Verificare che l'handle del cursore, l'handle del capitolo e gli handle dei segnalibri passati si trovino negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="8992a-4552">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4553">Preparare un messaggio CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="8992a-4554">Se gli handle di segnalibro sono uguali, \_ DWCOMPARISON deve essere impostato su DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="8992a-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="8992a-4555">In caso contrario, se uno dei segnalibri gestisce è DBBMK \_ First o DBBMK \_ Last, \_ dwComparison deve essere impostato su DBCOMPARE \_ ne.</span><span class="sxs-lookup"><span data-stu-id="8992a-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="8992a-4556">In caso contrario, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="8992a-4557">Trova le righe a cui fa riferimento ogni handle di segnalibro nei risultati della query</span><span class="sxs-lookup"><span data-stu-id="8992a-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="8992a-4558">Se una delle righe non è presente nel capitolo indicato dall'handle del capitolo in CPMCompareBmkIn, \_ DWCOMPARISON deve essere impostato su DBCOMPARE \_ NOTCOMPARABLE.</span><span class="sxs-lookup"><span data-stu-id="8992a-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="8992a-4559">In caso contrario, quando entrambe le righe si trovano nello stesso capitolo, il server deve approssimare una posizione di tali righe nel set di righe a cui fa riferimento l'handle di questo capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="8992a-4560">DEVE quindi confrontare i valori di posizione e impostare \_ dwComparison su DBCOMPARE \_ lt se la posizione della prima riga è minore della posizione della seconda riga; in caso contrario, \_ dwComparison deve essere impostato su DBCOMPARE \_ gt.</span><span class="sxs-lookup"><span data-stu-id="8992a-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="8992a-4561">Rispondere al client con un messaggio CPMCompareBmkOut compilato.</span><span class="sxs-lookup"><span data-stu-id="8992a-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="8992a-4562">3.1.5.2.12 che riceve una richiesta CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="8992a-4563">Quando il server riceve la richiesta del messaggio CPMRestartPositionIn dal client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4564">Controllare se il client dispone di una query associata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8992a-4565">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4566">Controllare se l'handle del cursore e l'handle del capitolo sono stati passati negli elenchi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="8992a-4567">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4568">Spostare il cursore all'inizio del capitolo, identificato dall'handle del capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="8992a-4569">Si noti che quando l'handle del capitolo è DB \_ null \_ hChapter, il capitolo corrispondente è il set di righe principale della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="8992a-4570">Se questo passaggio ha esito negativo per qualsiasi motivo, è necessario che il server segnali un errore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8992a-4571">Rispondere al client con un messaggio CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="8992a-4572">3.1.5.2.13 che riceve una richiesta CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="8992a-4573">Quando il server riceve una richiesta di messaggio CPMFreeCursorIn dal client, il server deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4574">Controllare se il client dispone di una query associata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8992a-4575">In caso contrario, il server deve segnalare un errore di parametro di stato \_ non valido \_ (0xc000000d).</span><span class="sxs-lookup"><span data-stu-id="8992a-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8992a-4576">Controllare se l'handle del cursore passato è nell'elenco degli handle del cursore del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="8992a-4577">In caso contrario, il server deve segnalare un errore di E \_ (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8992a-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8992a-4578">Rilasciare il cursore e le risorse associate (vedere la sezione 3.1.1 per l'elenco completo) per questo handle del cursore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="8992a-4579">Rimuovere il cursore dall'elenco dei cursori per il client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="8992a-4580">Rispondere con un messaggio CPMFreeCursorOut, impostando il \_ campo cCursorsRemaining con il numero di cursori rimanenti.</span><span class="sxs-lookup"><span data-stu-id="8992a-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="8992a-4581">nell'elenco di questo client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4581">in this client's list.</span></span>
-   <span data-ttu-id="8992a-4582">Se non sono presenti altri cursori per questo client, il server deve rilasciare la query e le risorse associate (vedere la sezione 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="8992a-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="8992a-4583">3.1.5.2.14 che riceve una richiesta CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="8992a-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="8992a-4584">Quando il server riceve una richiesta di messaggio CPMDisconnect dal client, il server deve rimuovere il client dall'elenco dei client connessi e rilasciare tutte le risorse associate al client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="8992a-4585">Eventi del timer 3.1.6</span><span class="sxs-lookup"><span data-stu-id="8992a-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="8992a-4586">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="8992a-4587">3.1.7 altri eventi locali</span><span class="sxs-lookup"><span data-stu-id="8992a-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="8992a-4588">Quando il server viene arrestato, è necessario innanzitutto eseguire la transizione allo stato "chiusura in corso".</span><span class="sxs-lookup"><span data-stu-id="8992a-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="8992a-4589">DEVE quindi interrompere l'ascolto della pipe, eseguire altre attività di arresto specifiche dell'implementazione e quindi passare allo stato "arrestato".</span><span class="sxs-lookup"><span data-stu-id="8992a-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="8992a-4590">3,2 Dettagli client</span><span class="sxs-lookup"><span data-stu-id="8992a-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="8992a-4591">3.2.1 modello di dati astratto</span><span class="sxs-lookup"><span data-stu-id="8992a-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="8992a-4592">La sezione seguente specifica i dati e lo stato gestiti dal client del protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="8992a-4593">I dati forniti consentono di semplificare la spiegazione del comportamento del protocollo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="8992a-4594">Questa sezione non impone che le implementazioni siano conformi a questo modello, purché il loro comportamento esterno sia coerente con quello descritto in questo documento.</span><span class="sxs-lookup"><span data-stu-id="8992a-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="8992a-4595">Un client ha lo stato astratto seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="8992a-4596">**Ultimo messaggio inviato**: copia dell'ultimo messaggio inviato al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="8992a-4597">**Valore della proprietà corrente**: valore parziale di una proprietà "rinviata", che è in fase di recupero.</span><span class="sxs-lookup"><span data-stu-id="8992a-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="8992a-4598">**Byte correnti ricevuti**: finora il numero di byte ricevuti per il valore corrente della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="8992a-4599">**Stato connessione named pipe**: una connessione al server</span><span class="sxs-lookup"><span data-stu-id="8992a-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="8992a-4600">3.2.2 timer</span><span class="sxs-lookup"><span data-stu-id="8992a-4600">3.2.2 Timers</span></span>

<span data-ttu-id="8992a-4601">Non sono richiesti timer del protocollo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="8992a-4602">3.2.3 inizializzazione</span><span class="sxs-lookup"><span data-stu-id="8992a-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="8992a-4603">Non viene eseguita alcuna azione fino a quando non viene ricevuta una richiesta di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="8992a-4604">3.2.4 Higher-Layer eventi attivati</span><span class="sxs-lookup"><span data-stu-id="8992a-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="8992a-4605">Quando una richiesta viene ricevuta da un livello superiore, il client deve creare una connessione named pipe al server, usando i dettagli specificati nella sezione 2,1.</span><span class="sxs-lookup"><span data-stu-id="8992a-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="8992a-4606">Se non è possibile eseguire questa operazione, la richiesta di livello superiore deve essere non riuscita.</span><span class="sxs-lookup"><span data-stu-id="8992a-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="8992a-4607">Ovvero, in caso di errore di connessione, è responsabilità del livello superiore ritentare, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="8992a-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="8992a-4608">Un'intestazione deve essere pre-sospesa con i campi impostati come specificato nella sezione 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="8992a-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="8992a-4609">Per i messaggi specificati in modo da richiedere un checksum diverso da zero, il \_ valore di ULCHECKSUM deve essere calcolato come segue:</span><span class="sxs-lookup"><span data-stu-id="8992a-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="8992a-4610">Il contenuto del messaggio dopo il \_ campo ulReserved2 nell'intestazione del messaggio deve essere interpretato come una sequenza di interi a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="8992a-4611">Il client deve calcolare la somma dei valori numerici forniti da questi numeri interi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="8992a-4612">Calcola l'XOR bit per bit di questo valore con 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="8992a-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="8992a-4613">Sottrae il valore specificato da \_ msg dal valore risultante dall'operazione XOR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="8992a-4614">Gestione del catalogo di servizi di indicizzazione remota di 3.2.4.1</span><span class="sxs-lookup"><span data-stu-id="8992a-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="8992a-4615">Ogni messaggio viene attivato da una richiesta dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="8992a-4616">Non esiste alcuna sequenza di messaggi applicata dal client per le richieste di messaggi CISP per la gestione remota dei cataloghi, ma (ad eccezione di un messaggio CPMSetCatStateIn) il server risponderà con esito positivo solo se il client si è connesso in precedenza tramite un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="8992a-4617">3.2.4.1.1 invio di una richiesta CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="8992a-4618">In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMCiStateInOut quando richiede informazioni sull'indicizzazione dei servizi nel server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="8992a-4619">Quando viene richiesto di inviare questo messaggio, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4620">Inviare un messaggio CPMCiStateInOut come specificato nella sezione 2.2.3.1 al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="8992a-4621">Attendere la ricezione del messaggio CPMCiStateInOut dal server, ignorando automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8992a-4622">Segnalare il valore del \_ campo status della risposta e, in caso di esito positivo, la struttura informativa torna al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="8992a-4623">3.2.4.1.2 invio di una richiesta CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="8992a-4624">In genere, il livello superiore chiede al client del protocollo di inviare un messaggio CPMSetCatStateIn quando richiede informazioni su un catalogo o su tutto il catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="8992a-4625">Per questo messaggio, il livello superiore deve fornire al client del protocollo un valore per \_ dwNewState e, se necessario, il nome del catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="8992a-4626">Quando viene richiesto di inviare questo messaggio, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4627">Inviare un messaggio CPMSetCatStateIn come specificato in 2.2.3.2 al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="8992a-4628">Attendere la ricezione di un messaggio CPMSetCatStateOut dal server, ignorando automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8992a-4629">Segnalare il valore del \_ campo status della risposta e, in caso di esito positivo, \_ dwOldState di nuovo al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="8992a-4630">3.2.4.1.3 invio di una richiesta CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="8992a-4631">Il livello superiore richiede in genere di inviare questo messaggio quando è necessario aggiornare i documenti in un percorso esistente o aggiungere un nuovo percorso di file all'indice.</span><span class="sxs-lookup"><span data-stu-id="8992a-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="8992a-4632">Quindi, il livello superiore consiste nel fornire il percorso e il tipo di un'analisi, specificata come nella sezione 2.2.3.4, in cui un aggiornamento incrementale o completo è destinato ai percorsi esistenti e la nuova inizializzazione è destinata a nuovi percorsi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="8992a-4633">Per soddisfare la richiesta di livello superiore, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4634">Inviare un messaggio CPMUpdateDocumentsIn come specificato nella sezione 2.2.3.4 al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="8992a-4635">Attendere la ricezione del messaggio CPMUpdateDocumentsIn dal server, ignorando automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8992a-4636">Segnalare il valore del \_ campo stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="8992a-4637">3.2.4.1.4 invio di una richiesta CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="8992a-4638">In genere, il livello superiore richiede di inviare questo messaggio quando è necessario migliorare le prestazioni di esecuzione delle query oppure fa parte della manutenzione pianificata del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="8992a-4639">Per gestire il livello superiore, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4640">Inviare il messaggio CPMForceMergeIn come specificato dalla sezione 2.2.3.5 al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="8992a-4641">Attendere la ricezione di un messaggio CPMUpdateDocumentsIn dal server, ignorando automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8992a-4642">Segnalare il valore del \_ campo stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="8992a-4643">Messaggi di query del catalogo di servizi di indicizzazione remota 3.2.4.2</span><span class="sxs-lookup"><span data-stu-id="8992a-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="8992a-4644">Ad eccezione di CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, esiste una relazione uno-a-uno tra i messaggi di CISP e le richieste di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="8992a-4645">Per le due eccezioni indicate in precedenza, possono essere presenti più messaggi generati dal client per soddisfare i requisiti di dimensione o per recuperare una proprietà completa.</span><span class="sxs-lookup"><span data-stu-id="8992a-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="8992a-4646">Il livello superiore tiene in genere traccia di tutte le informazioni specifiche della query (ad esempio, gli handle del cursore aperti, i valori validi per gli handle di segnalibro e di capitolo, i valori wid per i valori delle proprietà posticipate e così via) e tiene traccia anche se il client si trova in uno stato connesso, ma ciò non viene applicato in alcun modo dal client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="8992a-4647">A scopo illustrativo, la parte client del diagramma nella sezione 3 illustra questa sequenza per una semplice query del servizio di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="8992a-4648">3.2.4.2.1 invio di una richiesta CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="8992a-4649">Questo messaggio è in genere la prima richiesta del livello superiore (come se il client non fosse connesso, il server avrà esito negativo nella maggior parte dei messaggi ad eccezione di CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="8992a-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="8992a-4650">Il livello superiore fornisce al client del protocollo le informazioni necessarie per la connessione.</span><span class="sxs-lookup"><span data-stu-id="8992a-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="8992a-4651">Per gestire il livello superiore, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4652">Compilare il messaggio, usando le informazioni fornite dal client di livello superiore (vedere la sezione 2.2.3.6) in \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 e aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="8992a-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="8992a-4653">Impostare \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet e cExtPropSet come specificato in 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="8992a-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="8992a-4654">Impostare il checksum nel \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="8992a-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="8992a-4655">Inviare il messaggio CPMConnectIn al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="8992a-4656">Attendere la ricezione di un messaggio CPMConnectOut dal server, ignorando automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8992a-4657">Segnalare il valore del \_ campo status della risposta e, in caso di esito positivo, \_ ServerVersion di nuovo al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="8992a-4658">A scopo informativo, si prevede che i livelli più elevati eseguano in genere le azioni seguenti al completamento della connessione, ma non vengono applicati dal client CISP:</span><span class="sxs-lookup"><span data-stu-id="8992a-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="8992a-4659">Usare i messaggi di gestione del catalogo di servizi di indicizzazione remota per le attività amministrative</span><span class="sxs-lookup"><span data-stu-id="8992a-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="8992a-4660">Usare una richiesta CPMCreateQueryIn per creare una query di ricerca con lo scopo di recuperare i risultati dal catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="8992a-4661">3.2.4.2.2 invio di una richiesta CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="8992a-4662">Il livello superiore fornirà in genere informazioni per la creazione della query dopo la connessione del client del protocollo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="8992a-4663">Il livello superiore fornisce al client un set di restrizioni, un set di colonne, le regole di ordinamento e il set di categorizzazione (ognuno di essi può essere omesso), le proprietà del set di righe e la struttura di mapping degli ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="8992a-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="8992a-4664">Quando questa richiesta viene ricevuta da un livello superiore, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4665">Preparare un CPMCreateQueryOut come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8992a-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="8992a-4666">Se è presente un set di colonne, impostare CColumnsSetPreset su 0x01 e compilare il campo ColumnsSet.</span><span class="sxs-lookup"><span data-stu-id="8992a-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="8992a-4667">Se sono presenti restrizioni, impostare CRestrictionPresent su 0x01 e compilare il campo restrizione.</span><span class="sxs-lookup"><span data-stu-id="8992a-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="8992a-4668">Se è presente un set di ordinamento, compilare il campo Fascicola.</span><span class="sxs-lookup"><span data-stu-id="8992a-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="8992a-4669">Se è presente un set di categorizzazione, impostare CSortSetPresent su 0x01 e compilare il campo CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="8992a-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="8992a-4670">Imposta il resto dei campi come specificato in 2.2.3.8</span><span class="sxs-lookup"><span data-stu-id="8992a-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="8992a-4671">Calcolare \_ il campo ulCheckSum nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="8992a-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="8992a-4672">Inviare il messaggio CPMCreateQueryIn al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="8992a-4673">Attendere la ricezione del messaggio CPMCreateQueryOut (vedere i dettagli nella sezione 3.2.5.1.1), ignorando automaticamente tutti gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="8992a-4674">Segnalare il valore del \_ campo status della risposta e, in caso di esito positivo, la matrice di handle del cursore e i valori booleani informativi, come specificato in 2.2.3.9, al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="8992a-4675">3.2.4.2.3 invio di una richiesta CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="8992a-4676">In genere, il livello superiore imposta le associazioni per ogni colonna da restituire nelle righe quando dispone già di un handle di cursore valido (dopo la ricezione corretta di CPMCreateQueryOut, vedere la sezione 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="8992a-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="8992a-4677">Maggiore è il previsto che fornisca una matrice di strutture CTableColumn, come specificato nella sezione 2.2.4.31, per il campo aColumns e un handle di cursore valido.</span><span class="sxs-lookup"><span data-stu-id="8992a-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="8992a-4678">Quando questa richiesta viene ricevuta dal livello superiore, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4679">Calcolare il numero di strutture CTableColumn nella matrice aColumns e impostare il campo cColumns su questo valore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="8992a-4680">Calcolare la dimensione totale in byte dei campi cColumns e aColumns e impostare il \_ campo cbBindingDesc su questo valore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="8992a-4681">Impostare i campi specificati nel messaggio CPMSetBindingsIn sui valori forniti dal livello dell'applicazione superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="8992a-4682">Impostare il \_ campo ulChecksum sul valore calcolato come specificato nella sezione 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="8992a-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="8992a-4683">Inviare il messaggio CPMSetBindignsIn completato al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="8992a-4684">Attendere la ricezione di un messaggio CPMSetBindingsIn dal server, ignorando gli altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="8992a-4685">Indicare lo stato dal \_ campo stato della risposta al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="8992a-4686">A scopo informativo, è previsto che i livelli più elevati in genere chiedano a un client di inviare un messaggio CPMGetRowsIn, ma questo non viene applicato dal protocollo del servizio di indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8992a-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="8992a-4687">3.2.4.2.4 invio di una richiesta CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="8992a-4688">Quando il livello superiore sta per ricevere le informazioni sulle righe, fornirà il client del protocollo con handle di cursore e capitolo validi e fornirà la descrizione di ricerca appropriata.</span><span class="sxs-lookup"><span data-stu-id="8992a-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="8992a-4689">In genere, è previsto un livello superiore quando dispone di un handle di cursore e/o di un capitolo valido e i binding sono stati impostati con un messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="8992a-4690">Per accedere al set di righe in un capitolo, il livello superiore prevede l'uso dell'handle del capitolo ricevuto dal server in un messaggio CPMGetRowsOut precedente.</span><span class="sxs-lookup"><span data-stu-id="8992a-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="8992a-4691">Quando questa richiesta viene ricevuta dal livello superiore, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4692">Determinare il valore Unsigned Integer da specificare per il \_ campo cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="8992a-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="8992a-4693">Per determinare questo valore, il client deve assumere il valore massimo da quanto segue:</span><span class="sxs-lookup"><span data-stu-id="8992a-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="8992a-4694">1000 volte il valore del campo c \_ RowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="8992a-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="8992a-4695">Valore di \_ cbRowWidth, arrotondato per eccesso al più vicino 512 byte più vicino.</span><span class="sxs-lookup"><span data-stu-id="8992a-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="8992a-4696">Prendere il valore superiore di questi due valori, fino al limite di 16K.</span><span class="sxs-lookup"><span data-stu-id="8992a-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="8992a-4697">Nei casi in cui una singola riga è maggiore di 16K, il server non può restituire risultati a questa query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="8992a-4698">Specificare una base client per i dati di riga a dimensione variabile nello spazio degli indirizzi del client nel \_ campo ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="8992a-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="8992a-4699">*Comportamento di Windows: per un client a 32 bit che comunica con un server a 32 bit o un client a 64 bit che comunica con un server a 64 bit, questo valore è impostato su un indirizzo di memoria del buffer di ricezione nel processo dell'applicazione. In questo modo, i puntatori, ricevuti nel campo Rows di CPMGetRowsOut, sono corretti per i puntatori di memoria in un processo dell'applicazione client. In caso contrario, viene impostato su 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="8992a-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="8992a-4700">Calcolare la dimensione della descrizione della ricerca e impostarla nel \_ campo cbSeek.</span><span class="sxs-lookup"><span data-stu-id="8992a-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="8992a-4701">Impostare il valore di cbReserved (che fungerebbe da offset per l'avvio delle righe) al valore di \_ cbSeek più 0x14.</span><span class="sxs-lookup"><span data-stu-id="8992a-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="8992a-4702">Inviare un messaggio CPMConnectIn come specificato in 2.2.3.15 al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="8992a-4703">3.2.4.2.5 invio di una richiesta CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="8992a-4704">Se il client riceve una risposta CPMGetRowsOut dal server con il campo di stato della colonna impostato su StatusDeferred (0x01), significa che il valore della proprietà non è stato incluso nel campo Rows del messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="8992a-4705">In questo caso, il livello superiore richiede in genere al client del protocollo di recuperare il valore per mezzo del messaggio CPMFetchValueIn e fornisce il \_ valore Campo PROPSPEC e wid per una proprietà posticipata, che il client del protocollo deve usare nel primo messaggio CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="8992a-4706">Se questo è il primo messaggio CPMFetchValueIn inviato dal client per richiedere la proprietà specificata, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4707">Impostare tutti i campi in un messaggio come specificato nella sezione 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="8992a-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="8992a-4708">Impostare \_ cbSoFar su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="8992a-4709">Imposta i byte correnti ricevuti su 0.</span><span class="sxs-lookup"><span data-stu-id="8992a-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="8992a-4710">Inviare il messaggio CPMFetchValueIn al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="8992a-4711">3.2.4.2.6 invio di una richiesta CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="8992a-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="8992a-4712">Quando il livello superiore non utilizza più la query di ricerca, può rilasciare le risorse sul server chiedendo al client di inviare un messaggio CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="8992a-4713">Quando viene ricevuta questa richiesta, il client deve inviare un messaggio CPMFreeCursorIn come specificato in 2.2.3.28 al server, contenente l'handle specificato dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="8992a-4714">3.2.4.2.7 invio di un messaggio CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="8992a-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="8992a-4715">Se il livello superiore non ha altre query per il servizio di indicizzazione, per liberare più risorse server, l'applicazione può richiedere che il client invii un messaggio CPMDisconnect al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="8992a-4716">Quando la query viene ricevuta, il client deve semplicemente inviare il messaggio come richiesto.</span><span class="sxs-lookup"><span data-stu-id="8992a-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="8992a-4717">Non esiste alcuna risposta a questo messaggio dal server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="8992a-4718">Regole di sequenziazione e elaborazione dei messaggi 3.2.5</span><span class="sxs-lookup"><span data-stu-id="8992a-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="8992a-4719">Quando il client riceve una risposta del messaggio dal server, il client deve utilizzare l'ultimo messaggio inviato per determinare se il messaggio ricevuto dal server è quello previsto dal client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="8992a-4720">Tutti i messaggi con \_ un campo msg diverso da quello nell'ultimo messaggio di invio devono essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="8992a-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="8992a-4721">3.2.5.1 ricezione di una risposta CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="8992a-4722">Quando il client riceve una risposta del messaggio CPMCreateQueryOut dal server, il client deve restituire \_ lo stato e (se lo stato ha esito positivo) i valori di handle del cursore al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="8992a-4723">Tutte le altre azioni sono al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="8992a-4724">Poiché il livello superiore è in grado di riconoscere la struttura della query, il numero di handle di cursore da restituire nel messaggio CPMCreateOueryOut sarà sempre corretto.</span><span class="sxs-lookup"><span data-stu-id="8992a-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="8992a-4725">Gli handle del cursore vengono restituiti nell'ordine seguente: il primo handle viene utilizzato per il set di righe non sottoscritto, il secondo al primo set di righe con capitoli, ovvero il raggruppamento dei risultati in base alla prima categoria specificata nel campo CategorizationSet del messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="8992a-4726">A scopo informativo, si prevede che i livelli più elevati possano eseguire le azioni seguenti, ma non vengono applicati dal client CISP:</span><span class="sxs-lookup"><span data-stu-id="8992a-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="8992a-4727">Usare CPMSetBindingsIn per impostare le associazioni per le singole colonne ed eseguire eventuali azioni successive sul percorso della query</span><span class="sxs-lookup"><span data-stu-id="8992a-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="8992a-4728">Usare CPMGetQueryStatusIn per controllare lo stato di esecuzione di una query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="8992a-4729">Usare CPMRatioFinishedIn per richiedere la percentuale di completamento della query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="8992a-4730">3.2.5.2 ricezione di una risposta CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="8992a-4731">Quando il client riceve una risposta del messaggio CPMGetRowsOut dal server, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4732">Controllare che il \_ campo stato nell'intestazione indichi esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="8992a-4733">Se il \_ valore dello stato è un buffer di stato \_ \_ troppo \_ piccolo (0xC0000023), il client deve controllare lo stato dell'ultimo messaggio inviato.</span><span class="sxs-lookup"><span data-stu-id="8992a-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="8992a-4734">Se non contiene un messaggio CPMGetRowsIn, il messaggio ricevuto deve essere ignorato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8992a-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="8992a-4735">In caso contrario, il client deve inviare al server un nuovo messaggio CPMGetRowsIn con tutti i campi identici a quello archiviato, ad eccezione del fatto che \_ CBREADBUFFER deve essere aumentato di 512 (ma non maggiore di 0x4000).</span><span class="sxs-lookup"><span data-stu-id="8992a-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="8992a-4736">Se \_ lo stato è \_ \_ un buffer di stato troppo \_ piccolo (0XC0000023) e l'ultimo messaggio inviato ha già \_ CBREADBUFFER uguale a 0x4000 client deve segnalare l'errore fino al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="8992a-4737">Se il \_ valore di stato è qualsiasi altro valore di errore, il client deve indicare l'errore fino al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="8992a-4738">Se il \_ valore di stato indica esito positivo, i risultati devono essere indicati fino al livello superiore che richiede le informazioni e altre azioni sono al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="8992a-4739">A scopo informativo, si prevede che i livelli superiori eseguano in genere le azioni seguenti, ma non vengono applicati dal client del protocollo del servizio di indicizzazione del contenuto:</span><span class="sxs-lookup"><span data-stu-id="8992a-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="8992a-4740">Se i valori nelle righe rappresentano gli ID del documento, il capitolo o il segnalibro gestisce il livello superiore in genere li archivia per l'utilizzo in operazioni successive che coinvolgono ID documento o handle di segnalibro validi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="8992a-4741">Il livello superiore in genere archivia o Visualizza o utilizza in altro modo i dati dei valori di riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="8992a-4742">Per i valori che sono stati contrassegnati come livello superiore posticipato, recupereranno il valore usando i messaggi CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="8992a-4743">La descrizione della ricerca viene restituita anche a livello superiore e può essere riutilizzata o esaminata dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="8992a-4744">A scopo informativo, se il livello superiore ha richiesto handle ai capitoli e ai segnalibri ricevuti nelle righe, è possibile eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="8992a-4745">Utilizzare CPMGetQueryStatusExIn, per verificare lo stato di esecuzione di una query, nonché informazioni aggiuntive sullo stato, ad esempio il numero di documenti filtrati, i documenti rimanenti da filtrare, il rapporto tra documenti elaborati dalla query, il numero totale di righe nella query e la posizione del segnalibro nel set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="8992a-4746">Utilizzare CPMGetNotify per richiedere che il server invii notifiche al client delle modifiche dei set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="8992a-4747">Usare CPMGetApproximatePositionIn per richiedere la posizione approssimativa di un segnalibro in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="8992a-4748">Usare CPMCompareBmkIn per richiedere un confronto tra due segnalibri in un capitolo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="8992a-4749">Utilizzare CPMRestartPositionIn nel server per modificare la posizione del cursore all'inizio del set di righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="8992a-4750">3.2.5.3 ricezione di una risposta CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="8992a-4751">Quando il client riceve una risposta del messaggio CPMGetRowsOut dal server, il client deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="8992a-4752">Controllare che il \_ campo stato nell'intestazione indichi esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="8992a-4753">In caso di errore, notificare il livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="8992a-4754">In caso contrario, continuare.</span><span class="sxs-lookup"><span data-stu-id="8992a-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="8992a-4755">Controllare \_ fValueExist e, se impostato su 0x00000000, notificare al livello superiore che il valore non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="8992a-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="8992a-4756">In caso contrario \_ , aggiungere cbValue byte da vValue al valore della proprietà corrente.</span><span class="sxs-lookup"><span data-stu-id="8992a-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="8992a-4757">Se \_ \_ fMoreExists è impostato su 0x00000001, incrementare i \_ byte correnti ricevuti da \_ cbValue e inviare un messaggio CPMFetchValueIn al server, impostando \_ CbSoFar sul valore dei byte correnti ricevuti, \_ cbPropSpec su zero e \_ cbChunk sulle dimensioni del buffer desiderate dal livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="8992a-4758">Se \_ fMoreExists è impostato su 0x00000000, indicare il valore della proprietà dal valore della proprietà corrente al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="8992a-4759">3.2.5.4 ricezione di una risposta CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="8992a-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="8992a-4760">Quando il client riceve una risposta corretta del messaggio CPMFreeCursorOut dal server, il client deve restituire il \_ valore cCursorsRemaining al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8992a-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="8992a-4761">Le informazioni seguenti vengono fornite solo a scopo informativo e non vengono applicate dal client CISP.</span><span class="sxs-lookup"><span data-stu-id="8992a-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="8992a-4762">Si prevede che il livello superiore tenga traccia degli handle del cursore e non di quelli che sono già stati liberati.</span><span class="sxs-lookup"><span data-stu-id="8992a-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="8992a-4763">Quando il numero di \_ cCursorsRemaining è uguale a 0x00000000, il livello superiore può usare la connessione per specificare un'altra query (usando un messaggio CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="8992a-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="8992a-4764">Eventi del timer 3.2.6 nelle</span><span class="sxs-lookup"><span data-stu-id="8992a-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="8992a-4765">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="8992a-4766">3.2.7 altri eventi locali</span><span class="sxs-lookup"><span data-stu-id="8992a-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="8992a-4767">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="8992a-4768">4 Esempi di protocollo</span><span class="sxs-lookup"><span data-stu-id="8992a-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="8992a-4769">4,1 esempio 1</span><span class="sxs-lookup"><span data-stu-id="8992a-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="8992a-4770">4,2 esempio 2</span><span class="sxs-lookup"><span data-stu-id="8992a-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="8992a-4771">4,1 esempio 1</span><span class="sxs-lookup"><span data-stu-id="8992a-4771">4.1 Example 1</span></span>

<span data-ttu-id="8992a-4772">Nell'esempio seguente viene considerato uno scenario in cui l'utente JOHN sul computer A desidera ottenere le dimensioni dei file che contengono la parola "Microsoft" dal set di documenti archiviati in server X nel sistema di catalogo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="8992a-4773">Supponiamo che il computer A esegua un sistema operativo Windows XP a 32 bit e che il computer X esegua un sistema operativo Windows Server 2003 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8992a-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="8992a-4774">L'utente avvia un'applicazione di ricerca e immette la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8992a-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="8992a-4775">A sua volta, l'applicazione passa la query di ricerca al client del protocollo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="8992a-4776">Il client del protocollo stabilisce una connessione con il server di indicizzazione X. Il client del protocollo usa il named pipe \\ pipe \\ ci \_ SKADS per connettersi al server X tramite SMB.</span><span class="sxs-lookup"><span data-stu-id="8992a-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="8992a-4777">Il client del protocollo prepara quindi un messaggio CPMConnectIn con i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="8992a-4778">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4779">**\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="8992a-4780">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8992a-4781">**\_ ulChecksum** contiene il checksum, calcolato come specificato nella sezione 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="8992a-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="8992a-4782">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8992a-4783">Il corpo del messaggio viene popolato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4784">**\_ iClientVersion** è impostato su 0x00000008, che indica che il server deve convalidare il campo di checksum.</span><span class="sxs-lookup"><span data-stu-id="8992a-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="8992a-4785">**\_ fClientIsRemote** è impostato su 0x00000001, che indica che il server è un server remoto.</span><span class="sxs-lookup"><span data-stu-id="8992a-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="8992a-4786">**\_ cbBlob1** è impostato sulle dimensioni, in byte, dei campi cPropSet, PropertySet1 e PropertySet2 combinati.</span><span class="sxs-lookup"><span data-stu-id="8992a-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="8992a-4787">**\_ cbBlob2** è impostato su 0x00000004 (ovvero senza set di proprietà aggiuntivi).</span><span class="sxs-lookup"><span data-stu-id="8992a-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="8992a-4788">**MachineName** è impostato su.</span><span class="sxs-lookup"><span data-stu-id="8992a-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="8992a-4789">**Username** è impostato su John.</span><span class="sxs-lookup"><span data-stu-id="8992a-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="8992a-4790">**cPropSets** è impostato su 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="8992a-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="8992a-4791">Il campo **PropertySet1** è di tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="8992a-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="8992a-4792">La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="8992a-4793">Il campo **GuidPropSet** è impostato su A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="8992a-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="8992a-4794">il campo **cProperties** è impostato su 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="8992a-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="8992a-4795">il campo **aProps** è una matrice di strutture CDbProp.</span><span class="sxs-lookup"><span data-stu-id="8992a-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="8992a-4796">Per l' **elemento \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="8992a-4797">**PropId** è impostato su 0x00000002 ( \_ nome del \_ catalogo ci DBPROP \_ ).</span><span class="sxs-lookup"><span data-stu-id="8992a-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="8992a-4798">**DBPROPOPTIONS** è impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="8992a-4799">**DBPROPSTATUS** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-4800">Per l'elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8992a-4801">**eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid)</span><span class="sxs-lookup"><span data-stu-id="8992a-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="8992a-4802">Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8992a-4803">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-4804">Per l'elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="8992a-4805">**vType** è impostato su 0X001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="8992a-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="8992a-4806">**vValue** è impostato su "System", il nome del catalogo desiderato.</span><span class="sxs-lookup"><span data-stu-id="8992a-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="8992a-4807">Per l' **elemento \[ aProps \] 1** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="8992a-4808">**PropId** è impostato su 0x00000007 ( \_ tipo di \_ query ci DBPROP \_ )</span><span class="sxs-lookup"><span data-stu-id="8992a-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="8992a-4809">**DBPROPOPTIONS** è impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="8992a-4810">**DBPROPSTATUS** è impostato su to0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="8992a-4811">Per l'elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8992a-4812">**eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="8992a-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="8992a-4813">Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8992a-4814">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-4815">Per l'elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="8992a-4816">**vType** è impostato su 0X0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="8992a-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="8992a-4817">**vValue** è impostato su 0x00000000 (CiNormal), ovvero una query normale.</span><span class="sxs-lookup"><span data-stu-id="8992a-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="8992a-4818">Per l' **elemento \[ aProps \] 2** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="8992a-4819">**PropId** è impostato su 0x00000004 ( \_ flag di \_ ambito ci DBPROP \_ ).</span><span class="sxs-lookup"><span data-stu-id="8992a-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="8992a-4820">**DBPROPOPTIONS** è impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="8992a-4821">**DBPROPSTATUS** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-4822">Per l'elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8992a-4823">**eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="8992a-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="8992a-4824">Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8992a-4825">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-4826">Per l'elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="8992a-4827">**vType**: 0X1003 (VT \_ vector \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="8992a-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="8992a-4828">**vValue**: 0x00000001/0x00000001 (un elemento con valore 1), che indica le sottocartelle di ricerca</span><span class="sxs-lookup"><span data-stu-id="8992a-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="8992a-4829">Per l' **elemento \[ aProps \] 3** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="8992a-4830">**PropId**: 0X00000003 (DBPROP \_ ci \_ include \_ ambiti)</span><span class="sxs-lookup"><span data-stu-id="8992a-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="8992a-4831">**DBPROPOPTIONS**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="8992a-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="8992a-4832">**DBPROPSTATUS**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="8992a-4833">Per l'elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8992a-4834">**eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid).</span><span class="sxs-lookup"><span data-stu-id="8992a-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="8992a-4835">Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8992a-4836">**ulID** è impostato su 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="8992a-4837">Per l'elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="8992a-4838">**vType** è impostato su 0X101F (VT \_ vector \| VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="8992a-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="8992a-4839">**vValue** è impostato su 0x00000001/0x00000002/" \\ " (un elemento con una stringa a terminazione null di 2 caratteri), ovvero l'ambito radice.</span><span class="sxs-lookup"><span data-stu-id="8992a-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="8992a-4840">Il campo **PropertySet2** è di tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="8992a-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="8992a-4841">La struttura CDbPropSet che comprende il campo PropertySet1 viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="8992a-4842">**GuidPropSet** è impostato su AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="8992a-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="8992a-4843">il campo **cProperties** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="8992a-4844">Il campo **aProps** è una matrice di strutture CDbProp.</span><span class="sxs-lookup"><span data-stu-id="8992a-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="8992a-4845">Per l' **elemento \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="8992a-4846">**PropId** è impostato su 0x00000002 ( \_ computer DBPROP).</span><span class="sxs-lookup"><span data-stu-id="8992a-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="8992a-4847">**DBPROPOPTIONS** è impostato su 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="8992a-4848">**DBPROPSTATUS** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-4849">Per l'elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8992a-4850">**eKind** è impostato su 0x00000001 (dbkind \_ GUID \_ propid),</span><span class="sxs-lookup"><span data-stu-id="8992a-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="8992a-4851">Il **GUID** è null (tutti zeri), ovvero il valore si applica alla query, non solo a una singola colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8992a-4852">**ulID** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-4853">Per l'elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8992a-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="8992a-4854">**vType**: 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="8992a-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="8992a-4855">**vValue**: 0x04/"x" (4 byte/stringa Unicode con terminazione null), che significa "x"-nome di un server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="8992a-4856">il campo **cExtPropSet** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8992a-4857">matrice **aPropertySets** inesistente.</span><span class="sxs-lookup"><span data-stu-id="8992a-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="8992a-4858">I vari campi di riempimento vengono compilati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="8992a-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="8992a-4859">Il messaggio viene inviato al server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="8992a-4860">Il server verifica che il **\_ ulChecksum** sia corretto, verifica che l'utente sia autorizzato a eseguire la richiesta e risponde con un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="8992a-4861">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4862">**\_ msg** è impostato su 0x000000C8, a indicare che si tratta di un messaggio CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="8992a-4863">**\_ status** è impostato su 0x0000000 per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="8992a-4864">**\_ ulChecksum** è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="8992a-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="8992a-4865">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8992a-4866">Il corpo del messaggio viene popolato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4867">il campo **\_ ServerVersion** è impostato su 0X00000007 (Windows XP 32 o Windows Server 2003 a 32 bit).</span><span class="sxs-lookup"><span data-stu-id="8992a-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="8992a-4868">i campi **\_ riservati** sono riempiti con dati arbitrari.</span><span class="sxs-lookup"><span data-stu-id="8992a-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="8992a-4869">Il client prepara un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="8992a-4870">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4871">**\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="8992a-4872">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8992a-4873">**\_ ulChecksum** contiene il checksum, calcolato in base a 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="8992a-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="8992a-4874">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8992a-4875">Il corpo del messaggio viene popolato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4876">Il campo **dimensioni** è impostato sulla dimensione del resto del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="8992a-4877">Il campo **CColumnSetPresent** è impostato su 0x01.</span><span class="sxs-lookup"><span data-stu-id="8992a-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="8992a-4878">Il campo **columnstore** è di tipo CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="8992a-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="8992a-4879">La struttura CColumnSet che comprende questo campo è impostata nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="8992a-4880">il campo **\_ count** è impostato su 0x00000001 per indicare che viene restituita una colonna.</span><span class="sxs-lookup"><span data-stu-id="8992a-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="8992a-4881">la matrice **indexes** è 0x00000000 che indica la prima voce in \_ aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="8992a-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="8992a-4882">Il campo **CRestrictionPresent** è impostato su 0x01, che indica che il campo di **restrizione** è presente.</span><span class="sxs-lookup"><span data-stu-id="8992a-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="8992a-4883">Il campo di **restrizione** è di tipo CRestriction ed è impostato su:</span><span class="sxs-lookup"><span data-stu-id="8992a-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="8992a-4884">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="8992a-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="8992a-4885">**\_ Weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8992a-4886">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="8992a-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="8992a-4887">La **\_ Proprietà** è impostata su GUID B725F130-47ef-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC \_ propid)/0x13 che rappresenta il corpo del documento.</span><span class="sxs-lookup"><span data-stu-id="8992a-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="8992a-4888">**\_ CC** è impostata su 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="8992a-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="8992a-4889">**\_ pwcsphrase** è impostato sulla stringa "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8992a-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="8992a-4890">**\_ LCID** è impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="8992a-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="8992a-4891">**\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="8992a-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="8992a-4892">**CSortPresent** è impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="8992a-4893">**CCategorizationSetPresent** è impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="8992a-4894">**RowSetProperties** viene impostato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="8992a-4895">**\_ uBooleanOptions** è impostato su 0x00000001 (sequenziale).</span><span class="sxs-lookup"><span data-stu-id="8992a-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="8992a-4896">**\_ ulMaxOpenRows** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8992a-4897">**\_ ulMemoryUsage** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8992a-4898">\_**cMaxResults** è impostato su 0x00000100 (restituisce al massimo 256 righe).</span><span class="sxs-lookup"><span data-stu-id="8992a-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="8992a-4899">**\_ cCmdTimeOut** è impostato su 0x00000000 (Never timeout).</span><span class="sxs-lookup"><span data-stu-id="8992a-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="8992a-4900">**PidMapper** è impostato su:</span><span class="sxs-lookup"><span data-stu-id="8992a-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="8992a-4901">**\_ count** è impostata su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="8992a-4902">**\_ aPropSpec** è impostato su GUID B725F130-47ef-101A-a5-F1-02608C9EEBAC/0x00000001 (per PRSPEC \_ propid)/0x0000000c che rappresenta la proprietà dimensioni file di Windows.</span><span class="sxs-lookup"><span data-stu-id="8992a-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="8992a-4903">Il server lo elabora e risponde con un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="8992a-4904">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4905">**\_ msg** è impostato su 0x000000CA, a indicare che si tratta di un messaggio CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="8992a-4906">**\_ lo stato** è impostato su esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="8992a-4907">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8992a-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="8992a-4908">**\_ ulReserved2** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8992a-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="8992a-4909">Il corpo del messaggio viene popolato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4910">**\_ fTrueSeqeuntial** è impostato su 0x00000000, a indicare che la query può utilizzare un indice.</span><span class="sxs-lookup"><span data-stu-id="8992a-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="8992a-4911">**\_ fWorkIdUnique** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="8992a-4912">La matrice **aCursors** contiene un solo elemento, che rappresenta un handle del cursore per questa query.</span><span class="sxs-lookup"><span data-stu-id="8992a-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="8992a-4913">Il valore dipende dallo stato del server.</span><span class="sxs-lookup"><span data-stu-id="8992a-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="8992a-4914">Si supponga che il valore restituito sia 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="8992a-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="8992a-4915">Il client invia un messaggio di richiesta CPMSetBindingsIn per definire il formato di una riga.</span><span class="sxs-lookup"><span data-stu-id="8992a-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="8992a-4916">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4917">**\_ msg** è impostato su 0x000000D0, a indicare che si tratta di un messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="8992a-4918">**\_ lo stato** è impostato su esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="8992a-4919">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8992a-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="8992a-4920">**\_ ulReserved2** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8992a-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="8992a-4921">Il corpo del messaggio viene popolato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4922">**\_ hCursor** è impostato su 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="8992a-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="8992a-4923">**\_ cbRow** è impostato su 0x10 (abbastanza grande da contenere le colonne).</span><span class="sxs-lookup"><span data-stu-id="8992a-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="8992a-4924">**\_ cbBindingDesc** è impostato sulle dimensioni dei campi **\_ CColumns** e **\_ aColumns** combinati.</span><span class="sxs-lookup"><span data-stu-id="8992a-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="8992a-4925">**\_ CColumns** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="8992a-4926">la matrice **\_ aColumns** è impostata in modo da contenere una struttura CTableColumn contenente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="8992a-4927">**\_ Campo PROPSPEC** è impostato su GUID b725f130-47ef-101A-a5-F1-02608c9eebac/0x00000001 (per PRSPEC \_ propid)/0x0000000c che rappresenta la proprietà dimensioni file di Windows.</span><span class="sxs-lookup"><span data-stu-id="8992a-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="8992a-4928">**\_ vType** è impostato su 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="8992a-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="8992a-4929">**\_ ValueUsed** è impostato su 0x01 (colonna trasferita nella riga).</span><span class="sxs-lookup"><span data-stu-id="8992a-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="8992a-4930">**\_ ValueOffset** è impostato su 0x0002 (all'inizio della riga).</span><span class="sxs-lookup"><span data-stu-id="8992a-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="8992a-4931">**\_ ValueSize** è impostato su 0x08 (size of a VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="8992a-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="8992a-4932">**\_ StatusUsed** è impostato su 0x01.</span><span class="sxs-lookup"><span data-stu-id="8992a-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="8992a-4933">**\_ StatusOffset** è impostato su 0x0A.</span><span class="sxs-lookup"><span data-stu-id="8992a-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="8992a-4934">**\_ LengthUsed** è impostato su 0x00.</span><span class="sxs-lookup"><span data-stu-id="8992a-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="8992a-4935">Il server lo elabora e risponde con un messaggio CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="8992a-4936">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4937">**\_ msg** è impostato su 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="8992a-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="8992a-4938">**\_ lo stato** è impostato su esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="8992a-4939">**\_ ulChecksum** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8992a-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="8992a-4940">**\_ ulReserved2** è impostato su 0x00000000 (o qualsiasi altro valore arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8992a-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="8992a-4941">Il client invia un messaggio di richiesta CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="8992a-4942">Si supponga che il client sia pronto ad accettare 100 righe in questo momento e le desideri in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="8992a-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="8992a-4943">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4944">**\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8992a-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="8992a-4945">**\_ lo stato** è impostato su 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8992a-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="8992a-4946">**\_ ulChecksum** contiene il checksum calcolato in base alla sezione 0.</span><span class="sxs-lookup"><span data-stu-id="8992a-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="8992a-4947">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8992a-4948">Il corpo del messaggio viene popolato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4949">**\_ hCursor** è impostato su 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="8992a-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="8992a-4950">**\_ cRowsToTransfer** è impostato su 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="8992a-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="8992a-4951">**\_ cRowWidth** è impostato su 0x00000010 (dalle associazioni).</span><span class="sxs-lookup"><span data-stu-id="8992a-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="8992a-4952">**\_ cbSeek** è impostato su 0x14, ovvero le dimensioni dei campi etype, \_ Chapt e CRowSeekNext combinati.</span><span class="sxs-lookup"><span data-stu-id="8992a-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="8992a-4953">**\_ cbReserved** è impostato su 0x18 (0x14 più \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="8992a-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="8992a-4954">**\_ cbReadBuffer** è impostato su 0x800 (0x64 \* 0x10 arrotondato al multiplo successivo di 0x200).</span><span class="sxs-lookup"><span data-stu-id="8992a-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="8992a-4955">**\_ ulClientBase** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8992a-4956">**\_ fBwdfetch** è impostato su 0x00000000 per indicare che le righe devono essere recuperate in ordine di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="8992a-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="8992a-4957">**etype** è impostato su 0x0000001 che indica che il client desidera le righe successive.</span><span class="sxs-lookup"><span data-stu-id="8992a-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="8992a-4958">**\_ Chapt** è impostato su 0 (non è un risultato con capitoli).</span><span class="sxs-lookup"><span data-stu-id="8992a-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="8992a-4959">**SeekDescription** è impostato su CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="8992a-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="8992a-4960">La struttura CRowSeekNext contiene i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8992a-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="8992a-4961">**CiTblChapt** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8992a-4962">**\_ hRegion** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8992a-4963">**\_ cSkip** è impostato su 0 per indicare che il client non desidera ignorare le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="8992a-4964">Il server lo elabora e risponde con un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="8992a-4965">Si supponga che nel server siano stati trovati 100 documenti contenenti la parola "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8992a-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="8992a-4966">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4967">**\_ msg** è impostato su 0x000000CC, a indicare che si tratta di un messaggio CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8992a-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="8992a-4968">**\_ lo stato** è impostato su esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8992a-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="8992a-4969">**\_ ulChecksum** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8992a-4970">**\_ ulReserved2** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8992a-4971">Il corpo del messaggio viene popolato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8992a-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4972">**\_ CRowsReturned** è impostato su 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="8992a-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="8992a-4973">**etype** è impostato su 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8992a-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="8992a-4974">**\_ Chapt** è impostato su 0x00000000 (non è un risultato con capitoli).</span><span class="sxs-lookup"><span data-stu-id="8992a-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="8992a-4975">**SeekDescription** contiene una struttura CRowSeekNext, popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="8992a-4976">**CiTblChapt** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8992a-4977">**\_ hRegion** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8992a-4978">**\_ cSkip** è impostato su 0 per indicare che il client non desidera ignorare le righe.</span><span class="sxs-lookup"><span data-stu-id="8992a-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="8992a-4979">**Rows** contiene la dimensione dei documenti 100 che contengono la parola "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8992a-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="8992a-4980">Poiché si tratta di dati a dimensione fissa, viene semplicemente strutturato come un elenco di interi senza segno a 100, a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="8992a-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="8992a-4981">Il client invia un messaggio CPMDisconnect per terminare la connessione.</span><span class="sxs-lookup"><span data-stu-id="8992a-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="8992a-4982">L'intestazione del messaggio viene popolata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8992a-4983">**\_ msg** è impostato su 0x000000C9, a indicare che si tratta di un messaggio CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="8992a-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="8992a-4984">**\_ status** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8992a-4985">**\_ ulChecksum** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="8992a-4986">Il server elabora il messaggio e rimuove tutto lo stato del client.</span><span class="sxs-lookup"><span data-stu-id="8992a-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="8992a-4987">4,2 esempio 2</span><span class="sxs-lookup"><span data-stu-id="8992a-4987">4.2 Example 2</span></span>

<span data-ttu-id="8992a-4988">Nell'esempio precedente la query era piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="8992a-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="8992a-4989">Si prenda ora in considerazione una query leggermente più complessa.</span><span class="sxs-lookup"><span data-stu-id="8992a-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="8992a-4990">Si supponga che l'utente desideri recuperare le dimensioni dei documenti che contengono entrambe le parole seguenti: "Microsoft" e "Office".</span><span class="sxs-lookup"><span data-stu-id="8992a-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="8992a-4991">Questa impostazione viene specificata modificando il campo di restrizione contenuto nel messaggio CPMCreateQueryIn inviato nel passaggio 5, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8992a-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="8992a-4992">Il campo di **restrizione** è di tipo CRestriction ed è impostato su:</span><span class="sxs-lookup"><span data-stu-id="8992a-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="8992a-4993">**\_ ulType** è impostato su 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="8992a-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="8992a-4994">**\_ Weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="8992a-4995">Il resto del campo contiene una struttura CNodeRestriction:</span><span class="sxs-lookup"><span data-stu-id="8992a-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="8992a-4996">**\_ CNode** è impostato su 0x00000002, a indicare che nella matrice paNode sono presenti due nodi.</span><span class="sxs-lookup"><span data-stu-id="8992a-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="8992a-4997">Il campo **\_ paNode** è una matrice di due strutture CRestriction.</span><span class="sxs-lookup"><span data-stu-id="8992a-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="8992a-4998">**\_ paNode \[ 0 \]** contiene:</span><span class="sxs-lookup"><span data-stu-id="8992a-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="8992a-4999">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="8992a-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="8992a-5000">**\_ Weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-5001">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="8992a-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="8992a-5002">La **\_ Proprietà** è impostata su GUID b725f130-47ef-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC \_ propid)/0x13.</span><span class="sxs-lookup"><span data-stu-id="8992a-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="8992a-5003">**\_ CC** è impostata su 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="8992a-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="8992a-5004">**\_ pwcsphrase** è impostato sulla stringa "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8992a-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="8992a-5005">**\_ LCID** è impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="8992a-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="8992a-5006">**\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="8992a-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="8992a-5007">**\_ paNode \[ 1 \]** contiene:</span><span class="sxs-lookup"><span data-stu-id="8992a-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="8992a-5008">**\_ ulType** è impostato su 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="8992a-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="8992a-5009">**\_ Weight** è impostato su 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8992a-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8992a-5010">Il resto del campo contiene una struttura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="8992a-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="8992a-5011">La **\_ Proprietà** è impostata su GUID b725f130-47ef-101A-A5F1-02608c9eebac/0x00000001 (per PRSPEC \_ propid)/0x13.</span><span class="sxs-lookup"><span data-stu-id="8992a-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="8992a-5012">**\_ CC** è impostata su 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="8992a-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="8992a-5013">**\_ pwcsphrase** è impostato sulla stringa "Office".</span><span class="sxs-lookup"><span data-stu-id="8992a-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="8992a-5014">**\_ LCID** è impostato su 0x409 (per l'inglese).</span><span class="sxs-lookup"><span data-stu-id="8992a-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="8992a-5015">**\_ ulGenerateMethod** è impostato su 0x00000000 (corrispondenza esatta).</span><span class="sxs-lookup"><span data-stu-id="8992a-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="8992a-5016">5 Sicurezza</span><span class="sxs-lookup"><span data-stu-id="8992a-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="8992a-5017">5.1 Considerazioni sulla sicurezza per i responsabili dell'implementazione</span><span class="sxs-lookup"><span data-stu-id="8992a-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="8992a-5018">Le implementazioni di indicizzazione che indicizzano il contenuto protetto devono considerare l'utilizzo del contesto utente fornito da SMB \[ MS-SMB \] per tagliare i risultati della ricerca e restituire solo quelli accessibili al chiamante.</span><span class="sxs-lookup"><span data-stu-id="8992a-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="8992a-5019">5.2 Indice dei parametri di sicurezza</span><span class="sxs-lookup"><span data-stu-id="8992a-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="8992a-5020">Parametro di sicurezza</span><span class="sxs-lookup"><span data-stu-id="8992a-5020">Security Parameter</span></span>  | <span data-ttu-id="8992a-5021">Sezione</span><span class="sxs-lookup"><span data-stu-id="8992a-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="8992a-5022">Livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="8992a-5022">Impersonation level</span></span> | <span data-ttu-id="8992a-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="8992a-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="8992a-5024">6 Indice del comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="8992a-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="8992a-5025">Comportamento specifico della versione</span><span class="sxs-lookup"><span data-stu-id="8992a-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="8992a-5026">Sezione</span><span class="sxs-lookup"><span data-stu-id="8992a-5026">Section</span></span>   | <span data-ttu-id="8992a-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8992a-5027">Windows 2000</span></span> | <span data-ttu-id="8992a-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8992a-5028">Windows XP</span></span> | <span data-ttu-id="8992a-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8992a-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="8992a-5030">Questo protocollo viene implementato in Windows 2000, Windows XP, Windows Server 2003 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8992a-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="8992a-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="8992a-5031">1.3.2</span></span>     | <span data-ttu-id="8992a-5032">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5032">X</span></span>            | <span data-ttu-id="8992a-5033">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5033">X</span></span>          | <span data-ttu-id="8992a-5034">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5034">X</span></span>                   |
| <span data-ttu-id="8992a-5035">Le applicazioni in genere interagiscono con un wrapper di interfaccia OLE DB</span><span class="sxs-lookup"><span data-stu-id="8992a-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="8992a-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="8992a-5036">1.4</span></span>       | <span data-ttu-id="8992a-5037">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5037">X</span></span>            | <span data-ttu-id="8992a-5038">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5038">X</span></span>          | <span data-ttu-id="8992a-5039">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5039">X</span></span>                   |
| <span data-ttu-id="8992a-5040">Valori NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="8992a-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="8992a-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="8992a-5041">1.8</span></span>       | <span data-ttu-id="8992a-5042">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5042">X</span></span>            | <span data-ttu-id="8992a-5043">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5043">X</span></span>          | <span data-ttu-id="8992a-5044">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5044">X</span></span>                   |
| <span data-ttu-id="8992a-5045">Il client imposta il \_ campo stato in ogni intestazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8992a-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="8992a-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="8992a-5046">2.2.2</span></span>     | <span data-ttu-id="8992a-5047">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5047">X</span></span>            | <span data-ttu-id="8992a-5048">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5048">X</span></span>          | <span data-ttu-id="8992a-5049">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5049">X</span></span>                   |
| <span data-ttu-id="8992a-5050">il valore cPendingScans è in genere zero</span><span class="sxs-lookup"><span data-stu-id="8992a-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="8992a-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="8992a-5051">2.2.3.1</span></span>   | <span data-ttu-id="8992a-5052">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5052">X</span></span>            | <span data-ttu-id="8992a-5053">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5053">X</span></span>          | <span data-ttu-id="8992a-5054">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5054">X</span></span>                   |
| <span data-ttu-id="8992a-5055">valore iClientVersion</span><span class="sxs-lookup"><span data-stu-id="8992a-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="8992a-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="8992a-5056">2.2.3.6</span></span>   | <span data-ttu-id="8992a-5057">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5057">X</span></span>            | <span data-ttu-id="8992a-5058">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5058">X</span></span>          | <span data-ttu-id="8992a-5059">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5059">X</span></span>                   |
| <span data-ttu-id="8992a-5060">\_valore cbChunk</span><span class="sxs-lookup"><span data-stu-id="8992a-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="8992a-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="8992a-5061">2.2.3.19</span></span>  | <span data-ttu-id="8992a-5062">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5062">X</span></span>            | <span data-ttu-id="8992a-5063">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5063">X</span></span>          | <span data-ttu-id="8992a-5064">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5064">X</span></span>                   |
| <span data-ttu-id="8992a-5065">indirizzi di memoria a 32 bit e a 64 bit</span><span class="sxs-lookup"><span data-stu-id="8992a-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="8992a-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="8992a-5066">3.2.4.2.4</span></span> | <span data-ttu-id="8992a-5067">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5067">X</span></span>            | <span data-ttu-id="8992a-5068">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5068">X</span></span>          | <span data-ttu-id="8992a-5069">X</span><span class="sxs-lookup"><span data-stu-id="8992a-5069">X</span></span>                   |



 

 

 





