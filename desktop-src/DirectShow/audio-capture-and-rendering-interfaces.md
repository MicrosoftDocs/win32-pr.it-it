---
description: Interfacce di acquisizione e rendering audio
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfacce di acquisizione e rendering audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ffdf586ec8566abddadcb0b7109680664963a63071472a3ac7aa895981e643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824251"
---
# <a name="audio-capture-and-rendering-interfaces"></a>Interfacce di acquisizione e rendering audio

Queste interfacce supportano l'acquisizione e il rendering audio in DirectShow



| Interfaccia                                              | Descrizione                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Accedere agli input analogici nella scheda audio del sistema e regolare le caratteristiche, ad esempio mono o stereo, livello di mix, livello di panoramica, volume, acuti e bassi. |
| [**IAMAudioRendererStats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Ottenere informazioni statistiche sulle prestazioni relative al renderering audio.                                                                                          |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Controllare la modalità di allocazione dei buffer da parte del filtro di acquisizione audio.                                                                                                   |
| [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Controllare la tolleranza di un renderer audio quando corrisponde alle frequenze con un altro clock.                                                                      |
| [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Consente a un'applicazione di specificare quale finestra ha lo stato attivo per il controllo della riproduzione audio DirectSound.                                                      |
| [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Mantenere una risorsa del dispositivo audio prima che sia necessaria.                                                                                                        |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Eseguire una query e impostare il formato di output del filtro di acquisizione.                                                                                                         |
| [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Impostare il volume e il bilanciamento dell'output audio.                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce](interfaces.md)
</dt> </dl>

 

 



