---
title: Acquisisci nome file
description: Acquisisci nome file
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE messaggio
- Macro capFileSetCaptureFile
- WM_CAP_FILE_GET_CAPTURE_FILE messaggio
- Macro capFileGetCaptureFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e48ecd727accccb868d0f78c68a833ac6ec6655bada23db8a56f2a9aeaffd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941596"
---
# <a name="capture-filename"></a>Acquisisci nome file

Per impostazione predefinita, AVICap instrada i dati del flusso audio e video da una finestra di acquisizione a un file denominato CAPTURE.AVI nella directory radice dell'unità corrente. È possibile specificare un nome file alternativo inviando il messaggio [**WM CAP FILE SET CAPTURE \_ \_ \_ \_ \_ FILE**](wm-cap-file-set-capture-file.md) (o la macro [**capFileSetCaptureFile)**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) a una finestra di acquisizione. Questo messaggio specifica il nome file. non crea, alloca o apre il file. È possibile recuperare il nome file di acquisizione corrente inviando il messaggio [**WM CAP FILE GET CAPTURE \_ \_ \_ \_ \_ FILE**](wm-cap-file-get-capture-file.md) (o la macro [**capFileGetCaptureFile)**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) a una finestra di acquisizione.

 

 




