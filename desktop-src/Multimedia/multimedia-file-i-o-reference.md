---
title: Informazioni di riferimento su I/O file multimediali
description: Informazioni di riferimento su I/O file multimediali
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows multimediali, informazioni di riferimento su I/O file
- multimediali, informazioni di riferimento su I/O di file
- input multimediale, informazioni di riferimento su I/O di file
- I/O di file multimediali, informazioni di riferimento
- I/O file, informazioni di riferimento
- input e output (I/O),informazioni di riferimento
- I/O (input e output),informazioni di riferimento
- informazioni di riferimento sull'I/O di file multimediali, informazioni
- informazioni di riferimento sull'I/O dei file multimediali, informazioni
- file I/O reference,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d61b06c16b12a9276adc0d858a3170dae2f7d636cc63a9ac6cc032a65c978c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136902"
---
# <a name="multimedia-file-io-reference"></a>Informazioni di riferimento su I/O file multimediali

In questa sezione vengono descritte le funzioni, le macro, i messaggi e le strutture associate all'input e all'output di file multimediali. Questi elementi sono raggruppati nel modo seguente.

## <a name="basic-io"></a>I/O di base

-   [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a>I/O memorizzato nel buffer

-   [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))
-   [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a>RIFF I/O

-   [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a>Procedure di I/O personalizzate

-   [**IOProc**](/previous-versions//dd757098(v=vs.85))
-   [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [**MMIOM \_ CLOSE**](mmiom-close.md)
-   [**MMIOM \_ OPEN**](mmiom-open.md)
-   [**MMIOM \_ READ**](mmiom-read.md)
-   [**MMIOM \_ RENAME**](mmiom-rename.md)
-   [**MMIOM \_ SEEK**](mmiom-seek.md)
-   [**MMIOM \_ WRITE**](mmiom-write.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)
-   [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[I/O file multimediali](multimedia-file-i-o.md)
</dt> </dl>

 

 