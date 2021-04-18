---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: Cenni preliminari sull'oggetto PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ac6de8276c275fab05b728054b6f9a4e50e9bd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321076"
---
# <a name="overview-of-the-printcapabilities"></a><span data-ttu-id="eed3a-104">Cenni preliminari sull'oggetto PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="eed3a-104">Overview of the PrintCapabilities</span></span>

<span data-ttu-id="eed3a-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="eed3a-105">This topic is not current.</span></span> <span data-ttu-id="eed3a-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eed3a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eed3a-107">L'oggetto PrintCapabilities descrive le configurazioni o gli stati disponibili in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eed3a-107">The PrintCapabilities describe the configurations or states available on a device.</span></span> <span data-ttu-id="eed3a-108">Un dispositivo descritto da PrintCapabilities può spesso essere inserito in una serie di configurazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="eed3a-108">A device that is described by PrintCapabilities can often be placed in a number of different configurations.</span></span> <span data-ttu-id="eed3a-109">Nel caso di un dispositivo di stampa, gli attributi di stampa tipici includono la stampa duplex, la risoluzione e le dimensioni dei supporti.</span><span class="sxs-lookup"><span data-stu-id="eed3a-109">In the case of a printing device, typical printing attributes include duplex printing, resolution, and media size.</span></span> <span data-ttu-id="eed3a-110">Se il dispositivo supporta questi attributi, fanno parte della configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eed3a-110">If the device supports these attributes, they are part of the configuration for that device.</span></span> <span data-ttu-id="eed3a-111">L'utente seleziona una configurazione specifica assegnando un valore specifico a ognuno degli attributi disponibili. ad esempio, Duplex: unilaterale, risoluzione: 600 dpi e MediaSize: Legal.</span><span class="sxs-lookup"><span data-stu-id="eed3a-111">The user selects a particular configuration by assigning a specific value to each of the available attributes; for example, Duplex: OneSided, Resolution: 600 dpi, and MediaSize: Legal.</span></span>

<span data-ttu-id="eed3a-112">Gli elementi PrintCapabilities sono basati sul Framework dello schema di stampa, che definisce gli elementi che possono essere utilizzati nell'elemento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="eed3a-112">The PrintCapabilities are built on the Print Schema Framework, which defines the elements that can be used in the PrintCapabilities.</span></span> <span data-ttu-id="eed3a-113">Le parole chiave dello schema di stampa definiscono le gerarchie degli elementi comunemente utilizzate, o parole chiave, allo scopo di promuovere la portabilità delle informazioni e lo scopo tra i singoli client.</span><span class="sxs-lookup"><span data-stu-id="eed3a-113">The Print Schema Keywords define commonly-used element hierarchies, or keywords, for the purpose of promoting portability of the information and intent between individual clients.</span></span> <span data-ttu-id="eed3a-114">Tuttavia, le parole chiave dello schema di stampa consentono anche le estensioni private, in modo che PrintCapabilities possa essere personalizzato per soddisfare esigenze specifiche.</span><span class="sxs-lookup"><span data-stu-id="eed3a-114">However, the Print Schema Keywords also allow private extensions so that PrintCapabilities can be tailored to meet specific needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eed3a-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eed3a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eed3a-116">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="eed3a-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



