---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilità degli utenti del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320953"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="47b3f-104">Responsabilità degli utenti del documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="47b3f-104">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="47b3f-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="47b3f-105">This topic is not current.</span></span> <span data-ttu-id="47b3f-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="47b3f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="47b3f-107">Gli utenti dei documenti PrintCapabilities hanno determinati obblighi che devono sostenere per poter usare un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="47b3f-107">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="47b3f-108">I requisiti seguenti si applicano ai client di un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="47b3f-108">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="47b3f-109">Non devono rifiutare o non riuscire a elaborare elementi PrintCapabilities sintatticamente validi; ovvero qualsiasi documento PrintCapabilities conforme allo schema PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="47b3f-109">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="47b3f-110">Devono essere in grado di aggirare la presenza imprevista o l'assenza di contenuto definito privatamente.</span><span class="sxs-lookup"><span data-stu-id="47b3f-110">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="47b3f-111">Questo include contenuto definito privatamente che viene visualizzato all'interno di istanze di elementi di stampa definiti dallo schema.</span><span class="sxs-lookup"><span data-stu-id="47b3f-111">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="47b3f-112">Devono essere in grado di aggirare il contenuto facoltativo dello schema di stampa che è assente.</span><span class="sxs-lookup"><span data-stu-id="47b3f-112">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="47b3f-113">Devono essere consapevoli del momento in cui richiedere un nuovo documento.</span><span class="sxs-lookup"><span data-stu-id="47b3f-113">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="47b3f-114">I valori delle istanze di proprietà sono dipendenti dalla configurazione, quindi dipendenti dallo snapshot.</span><span class="sxs-lookup"><span data-stu-id="47b3f-114">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="47b3f-115">Quando si accede a un'istanza di proprietà, è necessario aggiornare lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="47b3f-115">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="47b3f-116">Le istanze di feature, Option e ScoredProperty che devono essere copiate in un oggetto PrintTicket sono statiche per definizione.</span><span class="sxs-lookup"><span data-stu-id="47b3f-116">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="47b3f-117">Ovvero non sono (e non devono essere) dipendenti dalla configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47b3f-117">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="47b3f-118">Se si accede a tutte le istanze di questi tipi, non è necessario ottenere un nuovo documento PrintCapabilities quando viene modificata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="47b3f-118">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="47b3f-119">I consumer di PrintCapabilities che sono client dell'interfaccia utente devono essere in grado di utilizzare le informazioni in un documento PrintCapabilities per costruire un'interfaccia utente e costruire un oggetto PrintTicket valido dalle selezioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="47b3f-119">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="47b3f-120">Ciò include la conoscenza delle istanze di ParameterInit che è necessario specificare e la convalida delle istanze specificate.</span><span class="sxs-lookup"><span data-stu-id="47b3f-120">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47b3f-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47b3f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47b3f-122">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="47b3f-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



