---
title: Creazione di una finestra di dialogo per la selezione di formati limitati
description: Creazione di una finestra di dialogo per la selezione di formati limitati
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Gestione compressione audio (ACM), creazione di finestre di dialogo
- ACM (Gestione compressione audio), creazione di finestre di dialogo
- Esempi di ACM, creazione di finestre di dialogo
- creazione di finestre di dialogo
- acmFormatChoose (funzione)
- Gestione compressione audio (ACM), selezione di formati limitati
- ACM (Gestione compressione audio), selezione di formati limitati
- Esempi di ACM, selezione di formati limitati
- selezione di formati limitati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044847"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a><span data-ttu-id="3949e-112">Creazione di una finestra di dialogo per la selezione di formati limitati</span><span class="sxs-lookup"><span data-stu-id="3949e-112">Producing a Dialog Box for Selecting Restricted Formats</span></span>

<span data-ttu-id="3949e-113">Potrebbe essere necessario utilizzare la finestra di dialogo creata dalla funzione [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , ma limitare o controllare i formati nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="3949e-113">You might want to use the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, but limit or control the formats in the dialog box.</span></span> <span data-ttu-id="3949e-114">A tale scopo, è possibile utilizzare il \_ flag ACMFORMATCHOOSE STYLEF \_ ENABLEHOOK per associare la routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="3949e-114">You can do this by using the ACMFORMATCHOOSE\_STYLEF\_ENABLEHOOK flag to hook the dialog procedure.</span></span> <span data-ttu-id="3949e-115">L'applicazione può quindi filtrare i formati rispondendo al messaggio [**mm \_ ACM \_ FORMATCHOOSE**](mm-acm-formatchoose.md) nella procedura del messaggio per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="3949e-115">The application can then filter the formats by responding to the [**MM\_ACM\_FORMATCHOOSE**](mm-acm-formatchoose.md) message in the message procedure for the dialog box.</span></span>

 

 




