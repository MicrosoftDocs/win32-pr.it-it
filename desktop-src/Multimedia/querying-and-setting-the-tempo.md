---
title: Esecuzione di query e impostazione del tempo
description: Esecuzione di query e impostazione del tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- MIDI (Musical Instrument Digital Interface), tempo
- MIDI (Musical Instrument Digital Interface), tempo
- Sequencer MIDI MCI, tempo
- Comando MCI_STATUS
- tempo sequenza
- tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714578"
---
# <a name="querying-and-setting-the-tempo"></a><span data-ttu-id="42ee9-109">Esecuzione di query e impostazione del tempo</span><span class="sxs-lookup"><span data-stu-id="42ee9-109">Querying and Setting the Tempo</span></span>

<span data-ttu-id="42ee9-110">Per recuperare il tempo di una sequenza, utilizzare il comando [**MCI \_ status**](mci-status.md) e impostare il membro **dwItem** della struttura [**\_ \_ parametri stato MCI**](mci-status-parms.md) su MCI \_ seq \_ status \_ tempo.</span><span class="sxs-lookup"><span data-stu-id="42ee9-110">To retrieve the tempo of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_TEMPO.</span></span> <span data-ttu-id="42ee9-111">Se il comando di **\_ stato MCI** ha esito positivo, il membro **dwReturn** della struttura **\_ \_ parametri stato MCI** contiene il tempo corrente.</span><span class="sxs-lookup"><span data-stu-id="42ee9-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure contains the current tempo.</span></span>

<span data-ttu-id="42ee9-112">Per modificare il tempo, utilizzare il comando [**MCI \_ set**](mci-set.md) con la struttura [**MCI \_ seq \_ set \_ parametri**](mci-seq-set-parms.md) , specificando \_ il \_ flag set tempo per MCI Seq set \_ tempo e impostando il membro **dwTempo** della struttura sul tempo desiderato.</span><span class="sxs-lookup"><span data-stu-id="42ee9-112">To change tempo, use the [**MCI\_SET**](mci-set.md) command with the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, specifying the MCI\_SEQ\_SET\_TEMPO flag and setting the **dwTempo** member of the structure to the desired tempo.</span></span>

<span data-ttu-id="42ee9-113">Il modo in cui viene rappresentato il tempo dipende dal tipo di divisione della sequenza.</span><span class="sxs-lookup"><span data-stu-id="42ee9-113">The way tempo is represented depends on the division type of the sequence.</span></span> <span data-ttu-id="42ee9-114">Se il tipo di divisione è PPQN, il tempo viene rappresentato in battute al minuto.</span><span class="sxs-lookup"><span data-stu-id="42ee9-114">If the division type is PPQN, the tempo is represented in beats per minute.</span></span> <span data-ttu-id="42ee9-115">Se il tipo di divisione è uno dei tipi di divisione SMPTE, il tempo viene rappresentato in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="42ee9-115">If the division type is one of the SMPTE division types, the tempo is represented in frames per second.</span></span> <span data-ttu-id="42ee9-116">Per informazioni sulla determinazione del tipo di divisione di una sequenza, vedere [recupero del tipo di divisione Sequence](retrieving-the-sequence-division-type.md).</span><span class="sxs-lookup"><span data-stu-id="42ee9-116">For information about determining the division type of a sequence, see [Retrieving the Sequence Division Type](retrieving-the-sequence-division-type.md).</span></span>

 

 




