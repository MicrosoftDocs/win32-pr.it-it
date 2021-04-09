---
title: Configurazione compressore e decompressore
description: Configurazione compressore e decompressore
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Gestione compressione video (VCM), configurazione di compressatori
- VCM (Gestione compressione video), configurazione dei commediatori
- Messaggio ICM_CONFIGURE
- ICQueryConfigure (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955396"
---
# <a name="compressor-and-decompressor-configuration"></a><span data-ttu-id="7e722-107">Configurazione compressore e decompressore</span><span class="sxs-lookup"><span data-stu-id="7e722-107">Compressor and Decompressor Configuration</span></span>

<span data-ttu-id="7e722-108">L'applicazione può configurare il compressore o il decompressore automaticamente oppure può consentire all'utente di configurarli.</span><span class="sxs-lookup"><span data-stu-id="7e722-108">Your application can configure the compressor or decompressor automatically, or it can allow the user to configure them.</span></span> <span data-ttu-id="7e722-109">Se è pratico, consentire all'utente di configurare il compressore o il decompressore; in questo modo si evita di considerare tutte le opzioni per il compressore o il decompressore.</span><span class="sxs-lookup"><span data-stu-id="7e722-109">If it is practical, allow the user to configure the compressor or decompressor; this frees you from considering all the options for the compressor or decompressor.</span></span>

<span data-ttu-id="7e722-110">L'utente può configurare il compressore o il decompressore usando una finestra di dialogo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7e722-110">The user can configure the compressor or decompressor by using a configuration dialog box.</span></span> <span data-ttu-id="7e722-111">È possibile inviare il messaggio di [**\_ configurazione ICM**](icm-configure.md) a VCM (oppure usare la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ) per determinare se un compressore o un decompressore può visualizzare una finestra di dialogo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7e722-111">You can send the [**ICM\_CONFIGURE**](icm-configure.md) message to VCM (or use the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro) to determine if a compressor or decompressor can display a configuration dialog box.</span></span> <span data-ttu-id="7e722-112">In tal caso, inviare il \_ messaggio di configurazione ICM (oppure usare la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ) per visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="7e722-112">If so, send the ICM\_CONFIGURE message (or use the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro) to display it.</span></span>

<span data-ttu-id="7e722-113">L'applicazione può inviare i messaggi di stato [**MCI \_ GetState**](icm-getstate.md) e [**ICM \_**](icm-setstate.md) (oppure usare le macro [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)e [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) per ottenere e impostare lo stato di un compressore o un decompressore.</span><span class="sxs-lookup"><span data-stu-id="7e722-113">Your application can send the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages (or use the [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate), and [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macros) to get and set the status for a compressor or decompressor.</span></span> <span data-ttu-id="7e722-114">Se l'applicazione crea o modifica lo stato, deve ottenere il layout dei dati del compressore o del decompressore prima di ripristinarne lo stato.</span><span class="sxs-lookup"><span data-stu-id="7e722-114">If your application creates or modifies the status, it must obtain the layout of the compressor or decompressor data before restoring its status.</span></span> <span data-ttu-id="7e722-115">In alternativa, se l'applicazione ottiene lo stato da un compressore o da un decompressore e lo usa per ripristinare lo stato in una sessione successiva, deve assicurarsi che ripristini solo le informazioni sullo stato ottenute dal compressore o dal decompressore attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="7e722-115">Alternatively, if your application obtains the status from a compressor or decompressor and uses it to restore the status in a subsequent session, it must ensure that it restores only status information obtained from the compressor or decompressor it is currently using.</span></span>

 

 




