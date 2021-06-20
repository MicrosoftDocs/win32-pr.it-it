---
description: I consumer di documenti PrintCapabilities hanno determinati obblighi che devono rispettare prima di poter usare un documento PrintCapabilities.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilità dei consumer del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec123509515de32b88c7352dcf0fc2c2b54504ff
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404944"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="b0cdb-103">Responsabilità dei consumer del documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="b0cdb-103">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="b0cdb-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-104">This topic is not current.</span></span> <span data-ttu-id="b0cdb-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b0cdb-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b0cdb-106">I consumer di documenti PrintCapabilities hanno determinati obblighi che devono rispettare prima di poter usare un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-106">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="b0cdb-107">I requisiti seguenti si applicano ai client di un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-107">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="b0cdb-108">Non devono rifiutare o non riuscire a elaborare printCapabilities sintatticamente validi; in altre informazioni, qualsiasi documento PrintCapabilities conforme allo schema PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-108">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="b0cdb-109">Devono essere in grado di risolvere la presenza imprevista o l'assenza di contenuto definito privatamente.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-109">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="b0cdb-110">È incluso il contenuto definito privatamente che viene visualizzato all'interno di istanze di elementi definiti dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-110">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="b0cdb-111">Devono essere in grado di aggirare il contenuto facoltativo dello schema di stampa assente.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-111">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="b0cdb-112">Devono sapere quando richiedere un nuovo documento.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-112">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="b0cdb-113">I valori delle istanze property sono dipendenti dalla configurazione (di conseguenza, dipendenti da snapshot).</span><span class="sxs-lookup"><span data-stu-id="b0cdb-113">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="b0cdb-114">È necessario aggiornare lo snapshot quando si accede a un'istanza property.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-114">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="b0cdb-115">Le istanze Feature, Option e ScoredProperty che devono essere copiate in printTicket sono statiche per definizione.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-115">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="b0cdb-116">Ciò significa che non dipendono (e non devono essere) dalla configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-116">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="b0cdb-117">Se si accede a istanze di questi tipi, non è necessario ottenere un nuovo documento PrintCapabilities quando la configurazione viene modificata.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-117">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="b0cdb-118">I consumer di PrintCapabilities che sono client dell'interfaccia utente devono essere in grado di usare le informazioni in un documento PrintCapabilities per costruire un'interfaccia utente e costruire un PrintTicket valido dalle selezioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-118">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="b0cdb-119">Ciò include la conoscenza delle istanze ParameterInit da specificare e la convalida delle istanze specificate.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-119">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0cdb-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0cdb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0cdb-121">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b0cdb-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



