---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Utilizzi dell'oggetto PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103969005"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="a5e5b-104">Utilizzi dell'oggetto PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="a5e5b-104">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="a5e5b-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-105">This topic is not current.</span></span> <span data-ttu-id="a5e5b-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a5e5b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a5e5b-107">Il PrintCapabilities è progettato per rappresentare gli attributi di dispositivo configurabili come costrutti di funzionalità o di opzione o costrutti di parametro.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-107">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="a5e5b-108">Queste informazioni definiscono lo spazio di configurazione del dispositivo e possono essere usate da un client dell'interfaccia utente per costruire un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-108">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="a5e5b-109">Le parole chiave dello schema di stampa definiscono un set di istanze di funzionalità standard, le istanze delle opzioni per le istanze della funzionalità standard e le istanze ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-109">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="a5e5b-110">I costrutti di funzione, opzione o parametro nell'elemento PrintCapabilities sono destinati a ospitare istanze di proprietà o ScoredProperty che descrivono un dispositivo e che sono supportate dal sottosistema spooler.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-110">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="a5e5b-111">Queste istanze di proprietà e ScoredProperty sono di interesse generale per i client del dispositivo e contengono le informazioni fornite dalle funzioni DevCaps Win32.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-111">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="a5e5b-112">Le parole chiave Print Schema definiscono un set di proprietà standard e istanze ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-112">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="a5e5b-113">È opportuno sottolineare che il documento PrintCapabilities è destinato a rappresentare solo dati a valore singolo, ovvero dati che non dipendono da una particolare configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-113">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="a5e5b-114">Il documento PrintCapabilities fornisce solo uno snapshot dei dati dipendenti dalla configurazione.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-114">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5e5b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5e5b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5e5b-116">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a5e5b-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



