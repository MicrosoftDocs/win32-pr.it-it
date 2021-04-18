---
description: Interfacce di acquisizione e rendering audio
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfacce di acquisizione e rendering audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304255"
---
# <a name="audio-capture-and-rendering-interfaces"></a>Interfacce di acquisizione e rendering audio

Queste interfacce supportano l'acquisizione e il rendering audio in DirectShow



| Interfaccia                                              | Descrizione                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Accedere agli input analoghi sulla scheda audio del sistema e modificare le caratteristiche, ad esempio mono o stereo, livello di combinazione, livello pan, sonorità, acute e bassi. |
| [**IAMAudioRendererStats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Ottenere informazioni statistiche sulle prestazioni relative al renderer audio.                                                                                          |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Controllare il modo in cui il filtro di acquisizione audio alloca i buffer.                                                                                                   |
| [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Controllare la tolleranza di un renderer audio quando corrisponde a frequenze con un altro Clock.                                                                      |
| [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Consente a un'applicazione di specificare quale finestra ha lo stato attivo per il controllo della riproduzione di audio DirectSound.                                                      |
| [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Mantenere una risorsa del dispositivo audio prima che sia necessaria.                                                                                                        |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Eseguire una query e impostare il formato di output del filtro di acquisizione.                                                                                                         |
| [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Imposta volume e bilancia di output audio.                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce](interfaces.md)
</dt> </dl>

 

 



