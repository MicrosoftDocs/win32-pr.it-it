---
description: Questo argomento descrive come cercare durante la riproduzione usando MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Come eseguire la ricerca durante la riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47e035ff8cc3764a9080698e8596660ce61907319bda70ac019b4cba1f8c27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974420"
---
# <a name="how-to-seek-during-playback"></a>Come eseguire la ricerca durante la riproduzione

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

Questo argomento descrive come cercare durante la riproduzione usando MFPlay.

**Da cercare durante la riproduzione**

1.  Inizializzare **un oggetto PROPVARIANT** per contenere il tempo di ricerca in unità da 100 nanosecondi, come **tipo LARGE \_ INTEGER** (**VT \_ I8).**
2.  Chiamare [**IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition). Specificare **MFP \_ POSITIONTYPE \_ 100NS** per il primo parametro e passare **PROPVARIANT** per il secondo parametro.

## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



