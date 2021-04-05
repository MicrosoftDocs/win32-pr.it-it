---
description: Questo argomento fornisce una procedura per eseguire la registrazione controllata da tracking dei flussi audio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Record Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882333"
---
# <a name="track-controlled-record"></a><span data-ttu-id="91acd-103">Record Track-Controlled</span><span class="sxs-lookup"><span data-stu-id="91acd-103">Track-Controlled Record</span></span>

<span data-ttu-id="91acd-104">Questo argomento fornisce una procedura per eseguire la registrazione controllata da tracking dei flussi audio.</span><span class="sxs-lookup"><span data-stu-id="91acd-104">This topic provides a procedure for performing track-controlled recording of audio streams.</span></span>

<span data-ttu-id="91acd-105">**Per eseguire la registrazione controllata dal rilevamento dei flussi audio**</span><span class="sxs-lookup"><span data-stu-id="91acd-105">**To perform track-controlled recording of audio streams**</span></span>

1.  <span data-ttu-id="91acd-106">Selezionare file rileva terminali nei flussi.</span><span class="sxs-lookup"><span data-stu-id="91acd-106">Select File Track Terminals onto streams.</span></span>
2.  <span data-ttu-id="91acd-107">Creare il terminale del record di file.</span><span class="sxs-lookup"><span data-stu-id="91acd-107">Create the File Record Terminal.</span></span>
3.  <span data-ttu-id="91acd-108">Impostare il nome del file.</span><span class="sxs-lookup"><span data-stu-id="91acd-108">Set the file name.</span></span>
4.  <span data-ttu-id="91acd-109">Enumera i flussi nella chiamata TAPI.</span><span class="sxs-lookup"><span data-stu-id="91acd-109">Enumerate streams on the TAPI call.</span></span> <span data-ttu-id="91acd-110">Per questi passaggi, vedere la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="91acd-110">For these steps, see the following procedure.</span></span>
5.  <span data-ttu-id="91acd-111">Chiamare il metodo [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sul terminale del record di file per avviare la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="91acd-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Record Terminal to start stream recording.</span></span>

<span data-ttu-id="91acd-112">**Per enumerare i flussi nella chiamata TAPI**</span><span class="sxs-lookup"><span data-stu-id="91acd-112">**To enumerate streams on the TAPI call**</span></span>

1.  <span data-ttu-id="91acd-113">Creare una traccia dello stesso tipo di audio e della stessa direzione del flusso.</span><span class="sxs-lookup"><span data-stu-id="91acd-113">Create a track of the same audio type and direction as the stream.</span></span>
2.  <span data-ttu-id="91acd-114">Impostare le proprietà della traccia per il formato audio.</span><span class="sxs-lookup"><span data-stu-id="91acd-114">Set the track properties for audio format.</span></span> <span data-ttu-id="91acd-115">Se non è impostato, il formato sarà uguale al formato dei flussi.</span><span class="sxs-lookup"><span data-stu-id="91acd-115">If not set, the format will be the same as the streams format.</span></span>
3.  <span data-ttu-id="91acd-116">Selezionare la traccia nel flusso.</span><span class="sxs-lookup"><span data-stu-id="91acd-116">Select the track on the stream.</span></span>

<span data-ttu-id="91acd-117">Se si seleziona una traccia in più flussi, questo implica la combinazione di flussi.</span><span class="sxs-lookup"><span data-stu-id="91acd-117">If one track is selected on multiple streams, this implies mixing streams.</span></span>

 

 



