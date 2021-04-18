---
title: Nome file di acquisizione
description: Nome file di acquisizione
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- Messaggio WM_CAP_FILE_SET_CAPTURE_FILE
- capFileSetCaptureFile (macro)
- Messaggio WM_CAP_FILE_GET_CAPTURE_FILE
- capFileGetCaptureFile (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298241"
---
# <a name="capture-filename"></a><span data-ttu-id="11abf-107">Nome file di acquisizione</span><span class="sxs-lookup"><span data-stu-id="11abf-107">Capture Filename</span></span>

<span data-ttu-id="11abf-108">AVICap, per impostazione predefinita, instrada i dati del flusso audio e video da una finestra di acquisizione a un file denominato CAPTURE.AVI nella directory radice dell'unità corrente.</span><span class="sxs-lookup"><span data-stu-id="11abf-108">AVICap, by default, routes video and audio stream data from a capture window to a file named CAPTURE.AVI in the root directory of the current drive.</span></span> <span data-ttu-id="11abf-109">È possibile specificare un nome di file alternativo inviando il messaggio del [**file di acquisizione del \_ \_ set di file \_ \_ \_ di WM**](wm-cap-file-set-capture-file.md) (o la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="11abf-109">You can specify an alternate filename by sending the [**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**](wm-cap-file-set-capture-file.md) message (or the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro) to a capture window.</span></span> <span data-ttu-id="11abf-110">Questo messaggio specifica il nome del file; non crea, alloca o apre il file.</span><span class="sxs-lookup"><span data-stu-id="11abf-110">This message specifies the filename; it does not create, allocate, or open the file.</span></span> <span data-ttu-id="11abf-111">È possibile recuperare il nome file di acquisizione corrente inviando il messaggio [**WM \_ Cap file \_ \_ get \_ Capture \_ file**](wm-cap-file-get-capture-file.md) (o la macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="11abf-111">You can retrieve the current capture filename by sending the [**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**](wm-cap-file-get-capture-file.md) message (or the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro) to a capture window.</span></span>

 

 




