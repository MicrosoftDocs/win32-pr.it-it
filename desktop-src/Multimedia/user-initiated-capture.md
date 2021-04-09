---
title: Acquisizione di User-Initiated
description: Acquisizione di User-Initiated
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856625"
---
# <a name="user-initiated-capture"></a><span data-ttu-id="decac-105">Acquisizione di User-Initiated</span><span class="sxs-lookup"><span data-stu-id="decac-105">User-Initiated Capture</span></span>

<span data-ttu-id="decac-106">È possibile recuperare il valore corrente del flag di acquisizione avviato dall'utente usando il messaggio di [**\_ installazione della \_ sequenza di recupero della \_ sequenza \_ di WM Cap**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="decac-106">You can retrieve the current value of the user-initiated capture flag by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="decac-107">Il valore del flag viene archiviato nel membro **fMakeUserHitOKToCapture** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="decac-107">The value of the flag is stored in the **fMakeUserHitOKToCapture** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="decac-108">È possibile fornire all'utente un controllo preciso su quando avviare una sessione di acquisizione impostando questo membro su **true**.</span><span class="sxs-lookup"><span data-stu-id="decac-108">You can provide the user with precise control over when to start a capture session by setting this member to **TRUE**.</span></span> <span data-ttu-id="decac-109">AVICap Visualizza una finestra di dialogo dopo l'allocazione di tutti i buffer video e audio per una sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="decac-109">AVICap displays a dialog box after allocating all video and audio buffers for a capture session.</span></span> <span data-ttu-id="decac-110">Ciò consente all'utente di eliminare i ritardi di acquisizione a causa dell'inizializzazione del software.</span><span class="sxs-lookup"><span data-stu-id="decac-110">This lets the user eliminate capture delays because of software initialization.</span></span> <span data-ttu-id="decac-111">Se l'applicazione usa un numero ridotto di buffer video, questa finestra di dialogo è probabilmente non necessaria.</span><span class="sxs-lookup"><span data-stu-id="decac-111">If your application uses a small number of video buffers, this dialog box is probably unnecessary.</span></span> <span data-ttu-id="decac-112">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="decac-112">The default value is **FALSE**.</span></span>

 

 




