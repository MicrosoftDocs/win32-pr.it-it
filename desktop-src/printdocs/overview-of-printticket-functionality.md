---
description: Questa panoramica della funzionalità PrintTicket descrive il formato per esprimere le informazioni di configurazione del dispositivo e l'uso di un PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Panoramica della funzionalità PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408544"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="bc52b-103">Panoramica della funzionalità PrintTicket</span><span class="sxs-lookup"><span data-stu-id="bc52b-103">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="bc52b-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="bc52b-104">This topic is not current.</span></span> <span data-ttu-id="bc52b-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bc52b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bc52b-106">PrintTicket usa un formato basato su XML per esprimere le informazioni di configurazione del dispositivo usando i costrutti di funzionalità/opzione e di parametro di Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="bc52b-106">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="bc52b-107">Sono inclusi tutti i tipi di elemento standard, nonché le funzionalità di estendibilità del framework dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="bc52b-107">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="bc52b-108">Si presuppone che un PrintTicket sia una descrizione autonoma della modalità di elaborazione di una singola pagina.</span><span class="sxs-lookup"><span data-stu-id="bc52b-108">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="bc52b-109">I passaggi necessari per estrarre e costruire un PrintTicket di questo tipo da un particolare formato di documento non sono trattati qui.</span><span class="sxs-lookup"><span data-stu-id="bc52b-109">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="bc52b-110">Un PrintTicket può essere usato per ottenere un documento PrintCapabilities che descrive le caratteristiche del dispositivo per una particolare configurazione.</span><span class="sxs-lookup"><span data-stu-id="bc52b-110">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="bc52b-111">In alternativa, è possibile inviare PrintTicket con un set di istruzioni per il rendering per produrre una pagina di output sottoposta a rendering ed elaborata in base alla configurazione specificata in PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="bc52b-111">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc52b-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc52b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc52b-113">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="bc52b-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



