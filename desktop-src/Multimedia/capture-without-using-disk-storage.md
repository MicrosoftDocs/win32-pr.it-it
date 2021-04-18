---
title: Acquisisci senza usare archiviazione su disco
description: Acquisisci senza usare archiviazione su disco
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Messaggio WM_CAP_SEQUENCE_NOFILE
- capCaptureSequenceNoFile (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298011"
---
# <a name="capture-without-using-disk-storage"></a><span data-ttu-id="33be0-105">Acquisisci senza usare archiviazione su disco</span><span class="sxs-lookup"><span data-stu-id="33be0-105">Capture Without Using Disk Storage</span></span>

<span data-ttu-id="33be0-106">È possibile utilizzare i servizi di acquisizione senza scrivere i dati in un file su disco utilizzando il messaggio di [**sequenza di WM \_ Cap \_ Sequence \_ nofile**](wm-cap-sequence-nofile.md) (o la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ).</span><span class="sxs-lookup"><span data-stu-id="33be0-106">You can use capture services without writing the data to a disk file by using the [**WM\_CAP\_SEQUENCE\_NOFILE**](wm-cap-sequence-nofile.md) message (or the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro).</span></span> <span data-ttu-id="33be0-107">Questo messaggio è utile solo in combinazione con le funzioni di callback che consentono all'applicazione di usare direttamente i dati video e audio.</span><span class="sxs-lookup"><span data-stu-id="33be0-107">This message is useful only in conjunction with callback functions that allow your application to use the video and audio data directly.</span></span> <span data-ttu-id="33be0-108">Ad esempio, le applicazioni di videoconferenza potrebbero utilizzare questo messaggio per ottenere i frame video di streaming.</span><span class="sxs-lookup"><span data-stu-id="33be0-108">For example, videoconferencing applications might use this message to obtain streaming video frames.</span></span> <span data-ttu-id="33be0-109">Le funzioni di callback trasferiscono le immagini acquisite al computer remoto.</span><span class="sxs-lookup"><span data-stu-id="33be0-109">The callback functions would transfer the captured images to the remote computer.</span></span>

 

 




