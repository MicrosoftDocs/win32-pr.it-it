---
description: La certificazione incrociata consente alle entità in un'infrastruttura a chiave pubblica (PKI) di considerare attendibili le entità in un'altra PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificazione incrociata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232664"
---
# <a name="cross-certification"></a><span data-ttu-id="89b19-103">Certificazione incrociata</span><span class="sxs-lookup"><span data-stu-id="89b19-103">Cross Certification</span></span>

<span data-ttu-id="89b19-104">La certificazione incrociata consente alle entità in un'infrastruttura a chiave pubblica (PKI) di considerare attendibili le entità in un'altra PKI.</span><span class="sxs-lookup"><span data-stu-id="89b19-104">Cross certification enables entities in one public key infrastructure (PKI) to trust entities in another PKI.</span></span> <span data-ttu-id="89b19-105">Questa relazione di trust reciproco è in genere supportata da un contratto di certificazione incrociata tra le autorità di certificazione (CAs) in ogni infrastruttura PKI.</span><span class="sxs-lookup"><span data-stu-id="89b19-105">This mutual trust relationship is typically supported by a cross-certification agreement between the certification authorities (CAs) in each PKI.</span></span> <span data-ttu-id="89b19-106">Il contratto stabilisce le responsabilità e la responsabilità di ogni parte.</span><span class="sxs-lookup"><span data-stu-id="89b19-106">The agreement establishes the responsibilities and liability of each party.</span></span>

<span data-ttu-id="89b19-107">Una relazione di trust reciproca tra due ca richiede che ogni CA rilascia un certificato all'altro per stabilire la relazione in entrambe le direzioni.</span><span class="sxs-lookup"><span data-stu-id="89b19-107">A mutual trust relationship between two CAs requires that each CA issue a certificate to the other to establish the relationship in both directions.</span></span> <span data-ttu-id="89b19-108">Il percorso di attendibilità non è gerarchico (nessuna delle CA di governance è subordinata all'altra) Sebbene il PKI separato possa essere costituito da gerarchie di certificati.</span><span class="sxs-lookup"><span data-stu-id="89b19-108">The path of trust is not hierarchal (neither of the governing CAs is subordinate to the other) although the separate PKIs may be certificate hierarchies.</span></span> <span data-ttu-id="89b19-109">Dopo che due CA hanno stabilito e specificato le condizioni di attendibilità e i certificati emessi tra loro, le entità all'interno del PKI separato possono interagire in base ai criteri specificati nei certificati.</span><span class="sxs-lookup"><span data-stu-id="89b19-109">After two CAs have established and specified the terms of trust and issued certificates to each other, entities within the separate PKIs can interact subject to the policies specified in the certificates.</span></span>

![diagramma di certificazione incrociata](images/cross-certification.png)

## <a name="related-topics"></a><span data-ttu-id="89b19-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89b19-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89b19-112">Modelli di attendibilità</span><span class="sxs-lookup"><span data-stu-id="89b19-112">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



