---
title: Canonizzazione XML
description: La canonizzazione XML risolve il problema della conversione di un set di nodi XML in byte in modo tale che le modifiche banali apportate al codice XML, ad esempio la modifica dell'ordine degli attributi in un elemento, non modifichino il formato di byte risultante.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Servizi Web per la canonizzazione XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873129"
---
# <a name="xml-canonicalization"></a><span data-ttu-id="49d78-106">Canonizzazione XML</span><span class="sxs-lookup"><span data-stu-id="49d78-106">XML Canonicalization</span></span>

<span data-ttu-id="49d78-107">La canonizzazione XML risolve il problema della conversione di un set di nodi XML in byte in modo tale che le modifiche banali apportate al codice XML, ad esempio la modifica dell'ordine degli attributi in un elemento, non modifichino il formato di byte risultante.</span><span class="sxs-lookup"><span data-stu-id="49d78-107">XML canonicalization solves the problem of converting a set of XML nodes into bytes in such a way that trivial changes to the XML (such as changing the order of attributes in an element) do not change the resulting byte form.</span></span> <span data-ttu-id="49d78-108">I byte ottenuti dalla canonizzazione vengono comunemente utilizzati per generare una firma crittografica sul contenuto XML.</span><span class="sxs-lookup"><span data-stu-id="49d78-108">The bytes obtained from canonicalization are commonly used to generate a cryptographic signature over XML content.</span></span>


<span data-ttu-id="49d78-109">Gli algoritmi di canonizzazione XML di uso comune standardizzano gli aspetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="49d78-109">The commonly used XML canonicalization algorithms standardize the following aspects:</span></span>

-   <span data-ttu-id="49d78-110">Codifica di caratteri (UTF-8 senza preambolo)</span><span class="sxs-lookup"><span data-stu-id="49d78-110">Character encoding (UTF-8 without preamble)</span></span>
-   <span data-ttu-id="49d78-111">Avanzamento riga e altri formati carattere</span><span class="sxs-lookup"><span data-stu-id="49d78-111">Linefeed and other character forms</span></span>
-   <span data-ttu-id="49d78-112">Ordine degli attributi in un elemento</span><span class="sxs-lookup"><span data-stu-id="49d78-112">Attribute order in an element</span></span>
-   <span data-ttu-id="49d78-113">Form elemento vuoto</span><span class="sxs-lookup"><span data-stu-id="49d78-113">Empty element form</span></span>
-   <span data-ttu-id="49d78-114">Rendering delle dichiarazioni dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49d78-114">Rendering namespace declarations</span></span>

<span data-ttu-id="49d78-115">Le API [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) e [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) forniscono la funzionalità di canonizzazione XML durante la lettura di un documento.</span><span class="sxs-lookup"><span data-stu-id="49d78-115">The APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) and [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) provide the XML canonicalization functionality while reading a document.</span></span>

<span data-ttu-id="49d78-116">Le API [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) e [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) forniscono la funzionalità di canonizzazione XML durante la scrittura di un documento.</span><span class="sxs-lookup"><span data-stu-id="49d78-116">The APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) and [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) provide the XML canonicalization functionality while writing a document.</span></span>

<span data-ttu-id="49d78-117">Con la canonizzazione vengono usate le enumerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="49d78-117">The following enumerations are used with canonicalization:</span></span>

-   [<span data-ttu-id="49d78-118">**\_algoritmo di \_ canonizzazione WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="49d78-118">**WS\_XML\_CANONICALIZATION\_ALGORITHM**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [<span data-ttu-id="49d78-119">**\_ID della \_ proprietà di canonizzazione di WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49d78-119">**WS\_XML\_CANONICALIZATION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

<span data-ttu-id="49d78-120">Con la canonizzazione vengono usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="49d78-120">The following functions are used with canonicalization:</span></span>

-   [<span data-ttu-id="49d78-121">**WsEndReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="49d78-121">**WsEndReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [<span data-ttu-id="49d78-122">**WsEndWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="49d78-122">**WsEndWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [<span data-ttu-id="49d78-123">**WsStartReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="49d78-123">**WsStartReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [<span data-ttu-id="49d78-124">**WsStartWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="49d78-124">**WsStartWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

<span data-ttu-id="49d78-125">Con la canonizzazione vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="49d78-125">The following structures are used with canonicalization:</span></span>

-   [<span data-ttu-id="49d78-126">**\_prefissi \_ inclusivi di canonizzazione WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49d78-126">**WS\_XML\_CANONICALIZATION\_INCLUSIVE\_PREFIXES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [<span data-ttu-id="49d78-127">**\_proprietà di \_ canonizzazione WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="49d78-127">**WS\_XML\_CANONICALIZATION\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




