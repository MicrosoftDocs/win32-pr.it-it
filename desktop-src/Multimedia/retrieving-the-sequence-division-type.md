---
title: Recupero del tipo di divisione sequenza
description: Recupero del tipo di divisione sequenza
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- MIDI (Musical Instrument Digital Interface), tipo divisione sequenza
- MIDI (Musical Instrument Digital Interface), tipo divisione sequenza
- MCI MIDI sequencer, tipo di divisione
- Comando MCI_STATUS
- tipo divisione sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955420"
---
# <a name="retrieving-the-sequence-division-type"></a><span data-ttu-id="10c7e-108">Recupero del tipo di divisione sequenza</span><span class="sxs-lookup"><span data-stu-id="10c7e-108">Retrieving the Sequence Division Type</span></span>

<span data-ttu-id="10c7e-109">Il *tipo di divisione* di una sequenza MIDI determina la quantità di tempo tra gli eventi MIDI nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="10c7e-109">The *division type* of a MIDI sequence determines the amount of time between MIDI events in the sequence.</span></span> <span data-ttu-id="10c7e-110">Per determinare il tipo di divisione di una sequenza, utilizzare il comando [**MCI \_ status**](mci-status.md) e impostare il membro **dwItem** della [**struttura \_ \_ parametri stato MCI**](mci-status-parms.md) su MCI \_ seq \_ status \_ DIVTYPE.</span><span class="sxs-lookup"><span data-stu-id="10c7e-110">To determine the division type of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_DIVTYPE .</span></span>

<span data-ttu-id="10c7e-111">Se il comando di **\_ stato MCI** ha esito positivo, il membro **dwReturn** della struttura **\_ \_ parametri stato MCI** conterrà uno dei valori seguenti per indicare il tipo di divisione.</span><span class="sxs-lookup"><span data-stu-id="10c7e-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure will contain one of the following values to indicate the division type.</span></span>



| <span data-ttu-id="10c7e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="10c7e-112">Value</span></span>                        | <span data-ttu-id="10c7e-113">Tipo divisione</span><span class="sxs-lookup"><span data-stu-id="10c7e-113">Division type</span></span>                     |
|------------------------------|-----------------------------------|
| <span data-ttu-id="10c7e-114">PPQN per MCI \_ seq \_ div \_</span><span class="sxs-lookup"><span data-stu-id="10c7e-114">MCI\_SEQ\_DIV\_PPQN</span></span>          | <span data-ttu-id="10c7e-115">PPQN (note parti per trimestre)</span><span class="sxs-lookup"><span data-stu-id="10c7e-115">PPQN (parts-per-quarter note)</span></span>     |
| <span data-ttu-id="10c7e-116">MCI \_ seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="10c7e-116">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>     | <span data-ttu-id="10c7e-117">SMPTE, 24 fps (fotogrammi al secondo)</span><span class="sxs-lookup"><span data-stu-id="10c7e-117">SMPTE, 24 fps (frames per second)</span></span> |
| <span data-ttu-id="10c7e-118">MCI \_ seq \_ div \_ \_ 25</span><span class="sxs-lookup"><span data-stu-id="10c7e-118">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>     | <span data-ttu-id="10c7e-119">SMPTE, 25 fps</span><span class="sxs-lookup"><span data-stu-id="10c7e-119">SMPTE, 25 fps</span></span>                     |
| <span data-ttu-id="10c7e-120">MCI \_ seq \_ div \_ \_ 30</span><span class="sxs-lookup"><span data-stu-id="10c7e-120">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>     | <span data-ttu-id="10c7e-121">SMPTE, 30 fps</span><span class="sxs-lookup"><span data-stu-id="10c7e-121">SMPTE, 30 fps</span></span>                     |
| <span data-ttu-id="10c7e-122">MCI \_ seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="10c7e-122">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span> | <span data-ttu-id="10c7e-123">SMPTE, 30 fps drop frame</span><span class="sxs-lookup"><span data-stu-id="10c7e-123">SMPTE, 30 fps drop frame</span></span>          |



 

<span data-ttu-id="10c7e-124">È necessario essere a conoscenza del tipo di divisione di una sequenza per modificare o eseguire una query sul tempo.</span><span class="sxs-lookup"><span data-stu-id="10c7e-124">You must know the division type of a sequence to change or query its tempo.</span></span> <span data-ttu-id="10c7e-125">Non è possibile modificare il tipo di divisione di una sequenza usando MCI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="10c7e-125">You cannot change the division type of a sequence by using the MCI sequencer.</span></span>

 

 




