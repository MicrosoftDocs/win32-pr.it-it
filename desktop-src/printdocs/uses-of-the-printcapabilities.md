---
description: Informazioni sugli usi di PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usi di PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119426"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="44f0c-105">Usi di PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="44f0c-105">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="44f0c-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="44f0c-106">This topic is not current.</span></span> <span data-ttu-id="44f0c-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="44f0c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="44f0c-108">PrintCapabilities è progettato per rappresentare gli attributi del dispositivo configurabili come costrutti Feature/Option o costrutti di parametro.</span><span class="sxs-lookup"><span data-stu-id="44f0c-108">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="44f0c-109">Queste informazioni definiscono lo spazio di configurazione del dispositivo e possono essere usate da un client dell'interfaccia utente per costruire un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="44f0c-109">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="44f0c-110">Le parole chiave dello schema di stampa definiscono un set di istanze di funzionalità standard, istanze option per le istanze feature standard e istanze ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="44f0c-110">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="44f0c-111">I costrutti di funzionalità/opzione o parametro in PrintCapabilities sono destinati a contenere istanze Property o ScoredProperty che descrivono un dispositivo e che sono supportate dal sottosistema spooler.</span><span class="sxs-lookup"><span data-stu-id="44f0c-111">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="44f0c-112">Queste istanze Property e ScoredProperty sono di interesse generale per i client del dispositivo e contengono le informazioni fornite dalle funzioni Win32 DevCaps.</span><span class="sxs-lookup"><span data-stu-id="44f0c-112">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="44f0c-113">Le parole chiave dello schema di stampa definiscono un set di istanze standard di Property e ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="44f0c-113">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="44f0c-114">È importante sottolineare che il documento PrintCapabilities è destinato a rappresentare solo dati a valore singolo: dati che non dipendono da una particolare configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44f0c-114">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="44f0c-115">Il documento PrintCapabilities fornisce solo uno snapshot dei dati dipendenti dalla configurazione.</span><span class="sxs-lookup"><span data-stu-id="44f0c-115">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44f0c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44f0c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44f0c-117">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="44f0c-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



