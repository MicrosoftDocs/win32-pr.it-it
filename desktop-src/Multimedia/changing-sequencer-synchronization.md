---
title: Modifica della sincronizzazione del sequencer
description: Modifica della sincronizzazione del sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "106320055"
---
# <a name="changing-sequencer-synchronization"></a><span data-ttu-id="4ee26-104">Modifica della sincronizzazione del sequencer</span><span class="sxs-lookup"><span data-stu-id="4ee26-104">Changing Sequencer Synchronization</span></span>

> [!NOTE]
> <span data-ttu-id="4ee26-105">Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.</span><span class="sxs-lookup"><span data-stu-id="4ee26-105">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="4ee26-106">All'interno di questo documento sono presenti riferimenti alla parola "slave".</span><span class="sxs-lookup"><span data-stu-id="4ee26-106">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="4ee26-107">La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.</span><span class="sxs-lookup"><span data-stu-id="4ee26-107">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="4ee26-108">Questo testo viene usato in quanto è attualmente il wording utilizzato all'interno del software.</span><span class="sxs-lookup"><span data-stu-id="4ee26-108">This wording is used as it is currently the wording used within the software.</span></span> <span data-ttu-id="4ee26-109">Per coerenza, questo documento contiene questa parola.</span><span class="sxs-lookup"><span data-stu-id="4ee26-109">For consistency, this document contains this word.</span></span> <span data-ttu-id="4ee26-110">Quando questa parola viene rimossa dal software, il documento verrà corretto per essere allineato.</span><span class="sxs-lookup"><span data-stu-id="4ee26-110">When this word is removed from the software, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="4ee26-111">Per modificare la modalità di sincronizzazione di un dispositivo Sequencer, utilizzare il messaggio di comando [**\_ set MCI**](mci-set.md) con \_ i \_ \_ \_ \_ \_ flag slave set master e MCI Seq set</span><span class="sxs-lookup"><span data-stu-id="4ee26-111">To change the synchronization mode of a sequencer device, use the [**MCI\_SET**](mci-set.md) command message with the MCI\_SEQ\_SET\_MASTER and MCI\_SEQ\_SET\_SLAVE flags.</span></span> <span data-ttu-id="4ee26-112">Per specificare le modalità di sincronizzazione master e subordinata, vengono usati due membri della struttura [**parametri di MCI \_ \_ set \_**](mci-seq-set-parms.md) , **dwMaster** e **dwSlave**.</span><span class="sxs-lookup"><span data-stu-id="4ee26-112">Two members in the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, **dwMaster** and **dwSlave**, are used to specify the master and subordinate synchronization modes.</span></span>

<span data-ttu-id="4ee26-113">La modalità di sincronizzazione master controlla le informazioni di sincronizzazione inviate dal sequencer a una porta di output.</span><span class="sxs-lookup"><span data-stu-id="4ee26-113">The master synchronization mode controls synchronization information sent by the sequencer to an output port.</span></span> <span data-ttu-id="4ee26-114">Di seguito sono riportate le costanti per il membro **dwMaster** e le modalità di sincronizzazione master corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="4ee26-114">Following are the constants for the **dwMaster** member and their corresponding master synchronization modes.</span></span>



| <span data-ttu-id="4ee26-115">Costante</span><span class="sxs-lookup"><span data-stu-id="4ee26-115">Constant</span></span>        | <span data-ttu-id="4ee26-116">Modalità di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="4ee26-116">Synchronization mode</span></span>                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee26-117">\_MIDI seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="4ee26-117">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="4ee26-118">Sincronizzazione MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ee26-118">MIDI Synchronization.</span></span> <span data-ttu-id="4ee26-119">Inviare le informazioni di temporizzazione alla porta di output usando i messaggi di clock temporizzati MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ee26-119">Send timing information to output port using MIDI timing clock messages.</span></span>   |
| <span data-ttu-id="4ee26-120">sequenza di MCI \_ seq \_</span><span class="sxs-lookup"><span data-stu-id="4ee26-120">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="4ee26-121">Sincronizzazione SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4ee26-121">SMPTE Synchronization.</span></span> <span data-ttu-id="4ee26-122">Inviare le informazioni di temporizzazione alla porta di output usando i messaggi MIDI del trimestre.</span><span class="sxs-lookup"><span data-stu-id="4ee26-122">Send timing information to output port using MIDI quarter-frame messages.</span></span> |
| <span data-ttu-id="4ee26-123">\_nessuno Seq seq \_</span><span class="sxs-lookup"><span data-stu-id="4ee26-123">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="4ee26-124">Nessuna sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4ee26-124">No Synchronization.</span></span> <span data-ttu-id="4ee26-125">Non inviare informazioni sull'intervallo.</span><span class="sxs-lookup"><span data-stu-id="4ee26-125">Send no timing information.</span></span>                                                  |



 

<span data-ttu-id="4ee26-126">La modalità di sincronizzazione subordinata controlla il punto in cui Sequencer ottiene le informazioni sull'intervallo per riprodurre un file MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ee26-126">The subordinate synchronization mode controls where the sequencer gets its timing information to play a MIDI file.</span></span> <span data-ttu-id="4ee26-127">Di seguito sono riportate le costanti per il membro **dwSlave** e le corrispondenti modalità di sincronizzazione subordinata.</span><span class="sxs-lookup"><span data-stu-id="4ee26-127">Following are the constants for the **dwSlave** member and their corresponding subordinate synchronization modes.</span></span>



| <span data-ttu-id="4ee26-128">Costante</span><span class="sxs-lookup"><span data-stu-id="4ee26-128">Constant</span></span>        | <span data-ttu-id="4ee26-129">Modalità di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="4ee26-129">Synchronization mode</span></span>                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee26-130">\_file SEQ di MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ee26-130">MCI\_SEQ\_FILE</span></span>  | <span data-ttu-id="4ee26-131">Sincronizzazione file.</span><span class="sxs-lookup"><span data-stu-id="4ee26-131">File Synchronization.</span></span> <span data-ttu-id="4ee26-132">Ottenere informazioni sulla tempistica dal file MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ee26-132">Get timing information from MIDI file.</span></span>                                                                                       |
| <span data-ttu-id="4ee26-133">\_MIDI seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="4ee26-133">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="4ee26-134">Sincronizzazione MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ee26-134">MIDI Synchronization.</span></span> <span data-ttu-id="4ee26-135">Ottenere informazioni sulla tempistica dalla porta di input usando i messaggi di clock temporizzati MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ee26-135">Get timing information from input port using MIDI timing clock messages.</span></span>                                                     |
| <span data-ttu-id="4ee26-136">sequenza di MCI \_ seq \_</span><span class="sxs-lookup"><span data-stu-id="4ee26-136">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="4ee26-137">Sincronizzazione SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4ee26-137">SMPTE Synchronization.</span></span> <span data-ttu-id="4ee26-138">Ottenere informazioni sulla tempistica dalla porta di input usando i messaggi MIDI del trimestre.</span><span class="sxs-lookup"><span data-stu-id="4ee26-138">Get timing information from input port using MIDI quarter-frame messages.</span></span>                                                   |
| <span data-ttu-id="4ee26-139">\_nessuno Seq seq \_</span><span class="sxs-lookup"><span data-stu-id="4ee26-139">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="4ee26-140">Nessuna sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4ee26-140">No Synchronization.</span></span> <span data-ttu-id="4ee26-141">Ottenere informazioni sui tempi solo dai comandi MCI e ignorare le informazioni di temporizzazione, ad esempio le modifiche del tempo, presenti nel file MIDI.</span><span class="sxs-lookup"><span data-stu-id="4ee26-141">Get timing information from MCI commands only and ignore timing information (such as tempo changes) that are in the MIDI file.</span></span> |



 

> [!Note]  
> <span data-ttu-id="4ee26-142">Attualmente, per la sincronizzazione principale, MCI MIDI Sequencer supporta solo la modalità Nessuna sincronizzazione (MCI \_ seq \_ None).</span><span class="sxs-lookup"><span data-stu-id="4ee26-142">Currently, for master synchronization, the MCI MIDI sequencer supports only the No Synchronization mode (MCI\_SEQ\_NONE).</span></span> <span data-ttu-id="4ee26-143">Per la sincronizzazione subordinata, supporta solo la modalità di sincronizzazione file ( \_ \_ file SEQ di MCI) e la modalità Nessuna sincronizzazione (MCI \_ seq \_ None).</span><span class="sxs-lookup"><span data-stu-id="4ee26-143">For subordinate synchronization, it supports only the File Synchronization mode (MCI\_SEQ\_FILE) and the No Synchronization mode (MCI\_SEQ\_NONE).</span></span>

 

 

 




