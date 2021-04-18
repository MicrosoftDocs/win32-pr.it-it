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
# <a name="capture-filename"></a>Nome file di acquisizione

AVICap, per impostazione predefinita, instrada i dati del flusso audio e video da una finestra di acquisizione a un file denominato CAPTURE.AVI nella directory radice dell'unità corrente. È possibile specificare un nome di file alternativo inviando il messaggio del [**file di acquisizione del \_ \_ set di file \_ \_ \_ di WM**](wm-cap-file-set-capture-file.md) (o la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) a una finestra di acquisizione. Questo messaggio specifica il nome del file; non crea, alloca o apre il file. È possibile recuperare il nome file di acquisizione corrente inviando il messaggio [**WM \_ Cap file \_ \_ get \_ Capture \_ file**](wm-cap-file-get-capture-file.md) (o la macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) a una finestra di acquisizione.

 

 




