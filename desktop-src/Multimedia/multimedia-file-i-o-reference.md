---
title: Riferimento I/O file multimediale
description: Riferimento I/O file multimediale
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows Multimedia, riferimento I/O file
- Multimedia, riferimento I/O file
- input multimediale, riferimento I/O file
- I/O file multimediale, informazioni di riferimento
- I/O di file, riferimento
- input e output (I/O), riferimento
- I/O (input e output), riferimento
- informazioni di riferimento per l'I/O del file multimediale, informazioni
- riferimento I/O file multimediale, informazioni
- riferimento I/O file, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724818"
---
# <a name="multimedia-file-io-reference"></a>Riferimento I/O file multimediale

Questa sezione descrive le funzioni, le macro, i messaggi e le strutture associati all'input e all'output del file multimediale. Questi elementi vengono raggruppati come indicato di seguito.

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

## <a name="riff-io"></a>I/O RIFF

-   [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a>Procedure di I/O personalizzate

-   [**IOProc**](/previous-versions//dd757098(v=vs.85))
-   [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [**chiusura di MMIOM \_**](mmiom-close.md)
-   [**MMIOM \_ aperto**](mmiom-open.md)
-   [**MMIOM di \_ lettura**](mmiom-read.md)
-   [**ridenominazione MMIOM \_**](mmiom-rename.md)
-   [**MMIOM \_ Seek**](mmiom-seek.md)
-   [**\_scrittura MMIOM**](mmiom-write.md)
-   [**\_WRITEFLUSH MMIOM**](mmiom-writeflush.md)
-   [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[I/O file multimediale](multimedia-file-i-o.md)
</dt> </dl>

 

 