---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Supporto di Delta PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321037"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="031bb-104">Supporto di Delta PrintTicket</span><span class="sxs-lookup"><span data-stu-id="031bb-104">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="031bb-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="031bb-105">This topic is not current.</span></span> <span data-ttu-id="031bb-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="031bb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="031bb-107">L'interfaccia del provider PrintTicket dispone di metodi che possono essere utilizzati per apportare modifiche incrementali a un oggetto PrintTicket esistente.</span><span class="sxs-lookup"><span data-stu-id="031bb-107">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="031bb-108">Le modifiche del PrintTicket incrementale possono essere specificate in un oggetto PrintTicket parziale noto come Delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="031bb-108">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="031bb-109">Un oggetto PrintTicket modificato viene creato unendo un Delta PrintTicket con un oggetto PrintTicket esistente.</span><span class="sxs-lookup"><span data-stu-id="031bb-109">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="031bb-110">Per ulteriori informazioni sui metodi che coinvolgono i Delta PrintTicket, vedere il documento di interfaccia del provider PrintTicket imminente.</span><span class="sxs-lookup"><span data-stu-id="031bb-110">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="031bb-111">Quando viene elaborato un Delta PrintTicket, è necessario eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="031bb-111">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="031bb-112">Identificare le istanze di feature o ParameterInit comuni sia al PrintTicket esistente (il PrintTicket di destinazione) sia al Delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="031bb-112">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="031bb-113">Per ogni funzionalità comune sia per l'oggetto PrintTicket di destinazione che per il Delta PrintTicket, sostituire la funzionalità nel PrintTicket di destinazione con la caratteristica corrispondente nel Delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="031bb-113">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="031bb-114">Per ogni ParameterInit comune sia al PrintTicket di destinazione sia al Delta PrintTicket, sostituire ParameterInit nel PrintTicket di destinazione con il ParameterInit corrispondente nel Delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="031bb-114">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="031bb-115">Copiare tutte le istanze ParameterInit e della funzionalità rimanenti nel Delta PrintTicket nel PrintTicket di destinazione.</span><span class="sxs-lookup"><span data-stu-id="031bb-115">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="031bb-116">Se l'algoritmo di risoluzione dei conflitti consente di specificare le priorità nel PrintTicket stesso, è possibile scegliere di elevare le priorità della funzionalità e delle istanze di ParameterInit denominate nel Delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="031bb-116">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="031bb-117">Eseguire la convalida PrintTicket come descritto nell' [elenco di controllo di convalida PrintTicket](printticket-validation-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="031bb-117">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="031bb-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="031bb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="031bb-119">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="031bb-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



