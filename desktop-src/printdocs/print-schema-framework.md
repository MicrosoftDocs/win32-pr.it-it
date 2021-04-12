---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Print Schema Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234546"
---
# <a name="print-schema-framework"></a><span data-ttu-id="f97a8-104">Print Schema Framework</span><span class="sxs-lookup"><span data-stu-id="f97a8-104">Print Schema Framework</span></span>

<span data-ttu-id="f97a8-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f97a8-105">This topic is not current.</span></span> <span data-ttu-id="f97a8-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f97a8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f97a8-107">In questa sezione vengono fornite informazioni più dettagliate sul significato e sull'utilizzo dei tipi di elemento dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="f97a8-107">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="f97a8-108">L'obiettivo principale della versione iniziale di Print Schema Framework consiste nel rappresentare le configurazioni e le funzionalità degli attributi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f97a8-108">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="f97a8-109">A livello generale, questo Framework offre due stili diversi per descrivere un attributo del dispositivo: come costrutto di funzionalità/opzione o come costrutto di parametro.</span><span class="sxs-lookup"><span data-stu-id="f97a8-109">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="f97a8-110">Se un attributo del dispositivo ha un numero ridotto di valori o stati disponibili, l'attributo deve essere caratterizzato da una funzionalità con i valori consentiti o gli stati definiti elementi option.</span><span class="sxs-lookup"><span data-stu-id="f97a8-110">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="f97a8-111">Viceversa, se un attributo del dispositivo ha un numero elevato di valori o stati disponibili e il set di tutti i valori possibili è facilmente definito senza ricorrere all'enumerazione esplicita, l'attributo del dispositivo deve essere caratterizzato da un parametro.</span><span class="sxs-lookup"><span data-stu-id="f97a8-111">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="f97a8-112">(Un parametro viene definito tramite un elemento ParameterDef e un'istanza di parametro viene inizializzata tramite un elemento ParameterInit). Gli elementi Property vengono utilizzati all'interno di costrutti di funzionalità, opzioni e parametri per offrire un livello di differenziazione più preciso.</span><span class="sxs-lookup"><span data-stu-id="f97a8-112">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f97a8-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f97a8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f97a8-114">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="f97a8-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



