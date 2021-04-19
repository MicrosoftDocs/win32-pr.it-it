---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Panoramica della funzionalità PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a70945fcc18e08615a9674a90a023f4ee12a76e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321078"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="7a3be-104">Panoramica della funzionalità PrintTicket</span><span class="sxs-lookup"><span data-stu-id="7a3be-104">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="7a3be-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7a3be-105">This topic is not current.</span></span> <span data-ttu-id="7a3be-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7a3be-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a3be-107">L'oggetto PrintTicket utilizza un formato basato su XML per esprimere le informazioni di configurazione del dispositivo utilizzando i costrutti di funzionalità, opzioni e parametri del Framework dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="7a3be-107">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="7a3be-108">Sono inclusi tutti i tipi di elemento standard e le funzionalità di estendibilità di Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="7a3be-108">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="7a3be-109">Si presuppone che un PrintTicket sia una descrizione autonoma della modalità di elaborazione di una singola pagina.</span><span class="sxs-lookup"><span data-stu-id="7a3be-109">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="7a3be-110">I passaggi necessari per estrarre e costruire tale PrintTicket da un particolare formato di documento non sono trattati in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="7a3be-110">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="7a3be-111">Un oggetto PrintTicket può essere utilizzato per ottenere un documento PrintCapabilities che descrive le caratteristiche del dispositivo per una particolare configurazione.</span><span class="sxs-lookup"><span data-stu-id="7a3be-111">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="7a3be-112">In alternativa, è possibile inviare l'oggetto PrintTicket con un set di istruzioni di rendering per produrre una pagina di output sottoposta a rendering ed elaborata in base alla configurazione specificata nell'oggetto PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="7a3be-112">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a3be-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a3be-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a3be-114">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7a3be-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



