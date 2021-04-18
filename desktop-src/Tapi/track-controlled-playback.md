---
description: I passaggi seguenti vengono eseguiti per la riproduzione controllata dal rilevamento.
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Riproduzione Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc657f0d301097edd280c358a34daafa83ef356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313252"
---
# <a name="track-controlled-playback"></a><span data-ttu-id="96a45-103">Riproduzione Track-Controlled</span><span class="sxs-lookup"><span data-stu-id="96a45-103">Track-Controlled Playback</span></span>

<span data-ttu-id="96a45-104">Per eseguire la riproduzione con controllo della traccia, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="96a45-104">To perform track-controlled playback, do the following:</span></span>

-   <span data-ttu-id="96a45-105">Selezionare i terminali di rilevamento sui flussi.</span><span class="sxs-lookup"><span data-stu-id="96a45-105">Select the Track Terminals onto streams.</span></span>
-   <span data-ttu-id="96a45-106">Creare il terminale per la riproduzione di file.</span><span class="sxs-lookup"><span data-stu-id="96a45-106">Create the File Playback Terminal.</span></span>
-   <span data-ttu-id="96a45-107">Impostare le proprietà: nome file e tipo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="96a45-107">Set properties—file name and type of storage.</span></span>
-   <span data-ttu-id="96a45-108">Utilizzando un metodo nel terminale di riproduzione file, enumerare i terminali di tracking dei file.</span><span class="sxs-lookup"><span data-stu-id="96a45-108">Using a method on the File Playback Terminal, enumerate File Track Terminals.</span></span>
-   <span data-ttu-id="96a45-109">Enumera i flussi nella chiamata TAPI.</span><span class="sxs-lookup"><span data-stu-id="96a45-109">Enumerate streams on the TAPI call.</span></span>
-   <span data-ttu-id="96a45-110">Selezionare il terminale di tracking del file nel flusso.</span><span class="sxs-lookup"><span data-stu-id="96a45-110">Select the File Track Terminal on the stream.</span></span>
-   <span data-ttu-id="96a45-111">Chiamare il metodo [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sul terminale riproduzione file per avviare la riproduzione dei dati registrati nei flussi TAPI.</span><span class="sxs-lookup"><span data-stu-id="96a45-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of recorded data to the TAPI streams.</span></span>

 

 



