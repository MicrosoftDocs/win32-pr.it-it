---
description: Questi articoli forniscono informazioni più dettagliate sul significato e sull'utilizzo dei tipi di elemento dello schema di stampa.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Framework dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407164"
---
# <a name="print-schema-framework"></a><span data-ttu-id="9ce8f-103">Framework dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9ce8f-103">Print Schema Framework</span></span>

<span data-ttu-id="9ce8f-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="9ce8f-104">This topic is not current.</span></span> <span data-ttu-id="9ce8f-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9ce8f-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9ce8f-106">In questa sezione vengono fornite informazioni più dettagliate sul significato e sull'utilizzo dei tipi di elemento dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="9ce8f-106">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="9ce8f-107">L'obiettivo principale della versione iniziale di Print Schema Framework è rappresentare le configurazioni e le funzionalità degli attributi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ce8f-107">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="9ce8f-108">A livello elevato, questo framework offre due stili diversi per descrivere un attributo del dispositivo: come costrutto Feature/Option o come costrutto di parametro.</span><span class="sxs-lookup"><span data-stu-id="9ce8f-108">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="9ce8f-109">Se un attributo dispositivo ha un numero ridotto di valori o stati disponibili, l'attributo deve essere caratterizzato come feature con i valori o gli stati consentiti definiti elementi Option.</span><span class="sxs-lookup"><span data-stu-id="9ce8f-109">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="9ce8f-110">Viceversa, se un attributo del dispositivo ha un numero elevato di valori o stati disponibili e il set di tutti i valori possibili è facilmente definito senza ricorrere all'enumerazione esplicita, l'attributo dispositivo deve essere caratterizzato come parametro.</span><span class="sxs-lookup"><span data-stu-id="9ce8f-110">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="9ce8f-111">Un parametro viene definito tramite un elemento ParameterDef e un'istanza del parametro viene inizializzata tramite un elemento ParameterInit. Gli elementi proprietà vengono usati all'interno di costrutti feature/option e parametri per fornire un livello di differenziazione più fine.</span><span class="sxs-lookup"><span data-stu-id="9ce8f-111">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ce8f-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ce8f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ce8f-113">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9ce8f-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



