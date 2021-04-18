---
description: Questo argomento descrive come eseguire ricerche durante la riproduzione usando MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Modalità di ricerca durante la riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308760"
---
# <a name="how-to-seek-during-playback"></a>Modalità di ricerca durante la riproduzione

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

Questo argomento descrive come eseguire ricerche durante la riproduzione usando MFPlay.

**Per eseguire la ricerca durante la riproduzione**

1.  Inizializzare un **PROPVARIANT** per conservare il tempo di ricerca in unità 100-nanosecondi, come tipo **\_ Integer grande** (**VT \_ i8**).
2.  Chiamare [**IMFPMediaPlayer:: seposition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition). Specificare **MFP \_ POSITIONTYPE \_ 100 ns** per il primo parametro e passare **PROPVARIANT** per il secondo parametro.

## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



