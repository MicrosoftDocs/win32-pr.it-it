---
title: Documento come snapshot delle proprietà
description: Esaminare il documento PrintCapabilities come snapshot delle proprietà. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118646"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="77a0b-105">Documento PrintCapabilities come snapshot delle proprietà</span><span class="sxs-lookup"><span data-stu-id="77a0b-105">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="77a0b-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="77a0b-106">This topic is not current.</span></span> <span data-ttu-id="77a0b-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="77a0b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="77a0b-108">Il dispositivo descritto da PrintCapabilities può avere proprietà che dipendono dallo stato o dalla configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77a0b-108">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="77a0b-109">Mentre PrintCapabilities rappresenta l'intero spazio di configurazione di un dispositivo, il provider PrintCapabilities produce un'istanza dipendente dalla configurazione di PrintCapabilities denominata documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="77a0b-109">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="77a0b-110">Questo documento PrintCapabilities dipendente dalla configurazione evita di gravare sullo schema PrintCapabilities con la complessità della rappresentazione di dati multivalore.</span><span class="sxs-lookup"><span data-stu-id="77a0b-110">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="77a0b-111">Ancora più importante, per liberare un consumer del documento PrintCapabilities dall'onere di estrarre il valore appropriato da una rappresentazione dei dati multivalore, tutte le istanze Property e ScoredProperty in un documento PrintCapabilities devono essere a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="77a0b-111">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="77a0b-112">In altre parole, ogni istanza Property e ScoredProperty in un documento PrintCapabilities deve avere un valore fisso, relativo alla configurazione di input.</span><span class="sxs-lookup"><span data-stu-id="77a0b-112">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="77a0b-113">Ogni documento PrintCapabilities può essere pensato come uno snapshot delle proprietà del dispositivo quando il dispositivo si trova in uno stato specifico.</span><span class="sxs-lookup"><span data-stu-id="77a0b-113">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="77a0b-114">Di conseguenza, prima di poter costruire un documento PrintCapabilities, è necessario specificare la configurazione da usare.</span><span class="sxs-lookup"><span data-stu-id="77a0b-114">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77a0b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77a0b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77a0b-116">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="77a0b-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



