---
title: Linee guida sull'estensione del nome file
description: Linee guida sull'estensione del nome file
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media Format SDK, estensioni di file
- ASF (Advanced Systems Format), estensioni di file
- ASF (Advanced Systems Format), estensioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955424"
---
# <a name="file-name-extension-guidelines"></a>Linee guida sull'estensione del nome file

Un'estensione di file fornisce un fornitore di software indipendente con informazioni sui requisiti di rendering di un'applicazione che utilizza l'estensione specifica.

L'estensione del nome di file che è necessario usare per un file creato da un'applicazione basata su Windows Media Format SDK è determinata dal tipo di contenuto del file. Usare la logica seguente per determinare l'estensione del nome di file che è necessario usare.

Se il file contiene flussi codificati con codec di terze parti o dati non compressi non supportati (inclusi dati arbitrari), il file deve utilizzare l'estensione ASF.

Se il file non contiene flussi non supportati e contiene uno o più flussi video non compressi o codificati con qualsiasi codec video Windows Media, il file deve usare l'estensione. wmv. Questi file possono includere anche flussi audio PCM, flussi audio codificati con qualsiasi codec audio Windows Media, flussi di script e flussi Web.

Se il file non contiene flussi non supportati e nessun flusso video supportato e contiene uno o più flussi audio decompressi PCM o codificati con qualsiasi codec audio Windows Media, il file deve utilizzare l'estensione WMA. Questi file possono contenere anche flussi di script e flussi Web.

Se il file contiene solo flussi che non sono audio né video, è necessario usare l'estensione ASF.

I tipi di video non compressi supportati includono RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU e YVU9.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Considerazioni sui progetti**](project-considerations.md)
</dt> </dl>

 

 




