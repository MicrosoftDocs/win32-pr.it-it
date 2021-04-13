---
title: Documento come snapshot delle proprietà
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401840"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="84b09-104">Documento PrintCapabilities come snapshot delle proprietà</span><span class="sxs-lookup"><span data-stu-id="84b09-104">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="84b09-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="84b09-105">This topic is not current.</span></span> <span data-ttu-id="84b09-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="84b09-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="84b09-107">Il dispositivo descritto dall'oggetto PrintCapabilities potrebbe avere proprietà che dipendono dallo stato o dalla configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84b09-107">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="84b09-108">Mentre l'oggetto PrintCapabilities rappresenta lo spazio di configurazione completo di un dispositivo, il provider PrintCapabilities produce un'istanza dipendente dalla configurazione della classe PrintCapabilities denominata documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="84b09-108">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="84b09-109">Questo documento PrintCapabilities dipendente dalla configurazione evita di sovraccaricare lo schema PrintCapabilities con la complessità della rappresentazione dei dati multivalore.</span><span class="sxs-lookup"><span data-stu-id="84b09-109">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="84b09-110">Ancora più importante, per alleviare un consumer del documento PrintCapabilities dal carico di estrarre il valore appropriato da una rappresentazione dati multivalore, tutte le istanze Property e ScoredProperty in un documento PrintCapabilities devono essere a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="84b09-110">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="84b09-111">In altre parole, ogni proprietà e istanza di ScoredProperty in un documento PrintCapabilities deve avere un valore fisso rispetto alla configurazione di input.</span><span class="sxs-lookup"><span data-stu-id="84b09-111">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="84b09-112">Ogni documento PrintCapabilities può essere considerato come uno snapshot delle proprietà del dispositivo quando il dispositivo si trova in un determinato stato.</span><span class="sxs-lookup"><span data-stu-id="84b09-112">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="84b09-113">Di conseguenza, prima di poter costruire un documento PrintCapabilities, è necessario fornire la configurazione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="84b09-113">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84b09-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84b09-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84b09-115">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="84b09-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



