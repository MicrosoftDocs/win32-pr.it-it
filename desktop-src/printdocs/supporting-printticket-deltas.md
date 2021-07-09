---
description: Informazioni sul supporto dei delta PrintTicket. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Supporto dei delta di PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548780"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="6e8e6-105">Supporto dei delta di PrintTicket</span><span class="sxs-lookup"><span data-stu-id="6e8e6-105">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="6e8e6-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-106">This topic is not current.</span></span> <span data-ttu-id="6e8e6-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6e8e6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6e8e6-108">L'interfaccia del provider PrintTicket include metodi che possono essere usati per apportare modifiche incrementali a un oggetto PrintTicket esistente.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-108">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="6e8e6-109">Le modifiche incrementali di PrintTicket possono essere specificate in un oggetto PrintTicket parziale noto come delta di PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-109">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="6e8e6-110">Un oggetto PrintTicket modificato viene creato unendo un delta PrintTicket con un oggetto PrintTicket esistente.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-110">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="6e8e6-111">Per altre informazioni sui metodi che coinvolgono i delta di PrintTicket, vedere il documento dell'interfaccia del provider PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-111">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="6e8e6-112">Quando viene elaborato un delta PrintTicket, è necessario eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-112">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="6e8e6-113">Identificare le istanze Feature o ParameterInit comuni sia all'oggetto PrintTicket esistente (PrintTicket di destinazione) che al delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-113">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="6e8e6-114">Per ogni funzionalità comune sia al valore PrintTicket di destinazione che al delta PrintTicket, sostituire la funzionalità nell'oggetto PrintTicket di destinazione con la funzionalità corrispondente nel delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-114">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="6e8e6-115">Per ogni ParameterInit comune sia al valore PrintTicket di destinazione che al delta PrintTicket, sostituire ParameterInit nell'oggetto PrintTicket di destinazione con il parametro ParameterInit corrispondente nel delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-115">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="6e8e6-116">Copiare tutte le istanze Feature e ParameterInit rimanenti nel delta PrintTicket nell'oggetto PrintTicket di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-116">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="6e8e6-117">Se l'algoritmo di risoluzione dei conflitti consente di definire priorità in PrintTicket stesso, è possibile scegliere di elevare le priorità delle istanze Feature e ParameterInit denominate nel delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-117">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="6e8e6-118">Eseguire la convalida di PrintTicket come descritto in [Elenco di controllo per la convalida di PrintTicket](printticket-validation-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="6e8e6-118">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e8e6-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e8e6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e8e6-120">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6e8e6-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



