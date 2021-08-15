---
title: Formato audio
description: Formato audio
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- WM_CAP_GET_AUDIOFORMAT messaggio
- Macro capGetAudioFormat
- Macro capGetAudioFormatSize
- WM_CAP_SET_AUDIOFORMAT messaggio
- Macro capSetAudioFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5891e8c244487895c51d68dd92fc4935f8981a36cf67d81437ff45f58950527b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375700"
---
# <a name="audio-format"></a>Formato audio

È possibile recuperare il formato di acquisizione corrente per i dati audio o le dimensioni della struttura del formato audio inviando il messaggio [**WM \_ CAP GET \_ \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) (o le macro [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) e [**capGetAudioFormatSize)**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) a una finestra di acquisizione. Il formato di acquisizione audio predefinito è mono, PCM a 8 bit e 11 kHz (pulse code modulation). Quando si recupera il formato usando WM \_ CAP \_ GET \_ AUDIOFORMAT, usare sempre la [**struttura WAVEFORMATEX.**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)

È possibile impostare il formato di acquisizione per i dati audio inviando il messaggio [**WM \_ CAP SET \_ \_ AUDIOFORMAT**](wm-cap-set-audioformat.md) (o la macro [**capSetAudioFormat)**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) a una finestra di acquisizione. Quando si imposta il formato audio, è possibile passare un puntatore a una struttura [**WAVEFORMAT,**](/windows/win32/api/mmreg/ns-mmreg-waveformat) **WAVEFORMATEX** o [**PCMWAVEFORMAT,**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) a seconda del formato audio specificato.

 

 