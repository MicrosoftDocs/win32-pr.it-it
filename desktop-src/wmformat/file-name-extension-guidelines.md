---
title: Linee guida per l'estensione del nome file
description: Linee guida per l'estensione del nome file
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media Format SDK, estensioni di file
- Advanced Systems Format (ASF), estensioni di file
- ASF (Advanced Systems Format), estensioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ccd8c3b1b4ba27aa7360296fc336625cb0f51c4374bb77c06d349cb70a987c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704004"
---
# <a name="file-name-extension-guidelines"></a>Linee guida per l'estensione del nome file

Un'estensione di file fornisce a un fornitore di software indipendente informazioni sui requisiti di rendering di un'applicazione che usa tale estensione specifica.

L'estensione di file che è necessario usare per un file creato da un'applicazione basata su Windows Media Format SDK è determinata dal tipo di contenuto nel file. Usare la logica seguente per determinare l'estensione di file che è necessario usare.

Se il file contiene flussi codificati con codec di terze parti o dati non compressi non supportati (inclusi dati arbitrari), il file deve usare l'estensione asf.

Se il file non contiene flussi non supportati e contiene uno o più flussi video non compressi o codificati con qualsiasi codec video Windows Media, il file deve usare l'estensione wmv. Questi file possono includere anche flussi audio PCM, flussi Windows audio codificati con qualsiasi codec audio multimediale, flussi di script e flussi Web.

Se il file non contiene flussi non supportati e nessun flusso video supportato e contiene uno o più flussi audio non compressi PCM o codificati con qualsiasi codec audio Windows Media, il file deve usare l'estensione wma. Questi file possono contenere anche flussi di script e flussi Web.

Se il file contiene solo flussi che non sono né audio né video, deve usare l'estensione asf.

I tipi di video non compressi supportati includono RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU e YVU9.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Project Considerazioni**](project-considerations.md)
</dt> </dl>

 

 




