---
title: Modelli di conformità del dispositivo video
description: Modelli di conformità del dispositivo video
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- Windows Media Format SDK, modelli di conformità del dispositivo
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
- Windows Media Format SDK, modelli di conformità dei dispositivi video
- Modelli di conformità dei dispositivi avanzati, ASF (Advanced Systems Format)
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi video
- Windows Media Video 9 codec, modelli di conformità dei dispositivi video
- codec, Windows Media Video 9 codec
- modelli di conformità del dispositivo, video
- modelli di conformità del dispositivo video
- modelli, modelli di conformità dei dispositivi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6735d029bc2339296fa2a0af8a48ace3303ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856921"
---
# <a name="video-device-conformance-templates"></a>Modelli di conformità del dispositivo video

Le tabelle seguenti elencano i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Video 9.

## <a name="simple-profile-low-level"></a>Profilo semplice, basso livello



| Parametro                                | Valore                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Stringa modello                          | "SP@LL"                                                                               |
| Dispositivi appropriati                      | Telefoni cellulari (soluzione per SmartPhone Microsoft Windows-Powered e dispositivi simili) |
| Risoluzione massima                       | 176 x 144                                                                             |
| Frequenza massima frame                       | 15 fps                                                                                |
| Velocità in bit massima                         | 96 kbps                                                                               |
| Dimensioni massime del buffer (in unità a 16384 bit) | 20 (circa 3,4 secondi alla velocità in bit massima)                                            |
| Codifica interlacciata                      | No                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Profilo semplice, livello medio



| Parametro                                | Valore                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Stringa modello                          | "SP@ML"                                                                              |
| Dispositivi appropriati                      | Computer palmari e personal data assistantsHigh-terminali wireless finali<br/> |
| Risoluzione massima                       | 352 x 288                                                                            |
| Frequenza massima frame                       | 15 fps @ 352 x 28824 fps @ 320 x 240<br/>                                      |
| Velocità in bit massima                         | 384 kbps                                                                             |
| Dimensioni massime del buffer (in unità a 16384 bit) | 77 (circa 3,3 secondi alla velocità in bit massima)                                           |
| Codifica interlacciata                      | No                                                                                   |



 

## <a name="generic-simple-profile"></a>Profilo semplice generico

Un flusso che è conforme alle limitazioni algoritmiche del profilo semplice, ma non rientra in una delle specifiche di livello, verrà assegnato "SP" come stringa del modello di conformità del dispositivo.

## <a name="main-profile-low-level"></a>Profilo principale, livello basso



| Parametro                                | Valore                                       |
|------------------------------------------|---------------------------------------------|
| Stringa modello                          | "MP@LL"                                     |
| Dispositivi appropriati                      | Set-top box                               |
| Risoluzione massima                       | 352 x 288                                   |
| Frequenza massima frame                       | 30 fps                                      |
| Velocità in bit massima                         | 2 Mbps                                      |
| Dimensioni massime del buffer (in unità a 16384 bit) | 306 (circa 2,5 secondi alla velocità in bit massima) |
| Codifica interlacciata                      | No                                          |



 

## <a name="main-profile-medium-level"></a>Profilo principale, livello medio



| Parametro                                | Valore                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Stringa modello                          | "MP@ML"                                                                                                                |
| Dispositivi appropriati                      | Set-top boxesSlower computers using DirectX Video Acceleration<br/> Lettori DVD abilitati per Windows Media<br/> |
| Risoluzione massima                       | 720 x 576                                                                                                              |
| Frequenza massima frame                       | 30 fps a 720 x 48025 fps @ 720 x 576<br/>                                                                        |
| Velocità in bit massima                         | 10 Mbps                                                                                                                |
| Dimensioni massime del buffer (in unità a 16384 bit) | 611 (circa 1 secondo alla velocità in bit massima)                                                                               |
| Codifica interlacciata                      | Sì                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Profilo principale, livello superiore



| Parametro                                | Valore                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stringa modello                          | "MP@HL"                                                                                                                                                               |
| Dispositivi appropriati                      | Computer che utilizzano video DirectX AccelerationHigh-Definition lettori DVD abilitati per Windows Media<br/> Cinema digitale<br/> streaming ad alta definizione<br/> |
| Risoluzione massima                       | 1920 x 1080                                                                                                                                                           |
| Frequenza massima frame                       | 30 fps a 1920 x 108060 fps @ 1280 x 720<br/>                                                                                                                    |
| Velocità in bit massima                         | 20 Mbps                                                                                                                                                               |
| Dimensioni massime del buffer (in unità a 16384 bit) | 2442 (circa 2,66 secondi alla velocità in bit massima)                                                                                                                         |
| Codifica interlacciata                      | Sì                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Profilo principale generico

Un flusso che è conforme alle limitazioni algoritmiche del profilo principale, ma non rientra in una delle specifiche di livello, verrà assegnato "MP" come stringa del modello di conformità del dispositivo.

## <a name="complex-profile"></a>Profilo complesso



| Parametro       | Valore                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Stringa modello | CP                                                                                                                                   |
| Commenti         | Il profilo complesso non presenta limitazioni esplicite. Viene usato per abilitare tutti gli algoritmi di codec, in genere a scopo dimostrativo. |



 

Le tabelle seguenti elencano i parametri dei modelli di conformità del dispositivo per il codec di immagine Windows Media Video 9.

## <a name="video-image-level-1"></a>Livello immagine video 1



| Parametro                                | Valore                                       |
|------------------------------------------|---------------------------------------------|
| Stringa modello                          | I1                                        |
| Risoluzione massima                       | 352 x 288                                   |
| Frequenza massima frame                       | 30 fps                                      |
| Velocità in bit massima                         | 192 Kbps                                    |
| Dimensioni massime del buffer (in unità a 16384 bit) | 39 (circa 3,26 secondi alla velocità in bit massima) |
| Codifica interlacciata                      | No                                          |



 

## <a name="video-image-level-2"></a>Livello immagine video 2



| Parametro                                | Valore                                       |
|------------------------------------------|---------------------------------------------|
| Stringa modello                          | I2                                        |
| Risoluzione massima                       | 1024 x 768                                  |
| Frequenza massima frame                       | 30 fps                                      |
| Velocità in bit massima                         | 384 kbps                                    |
| Dimensioni massime del buffer (in unità a 16384 bit) | 77 (circa 3,26 secondi alla velocità in bit massima) |
| Codifica interlacciata                      | No                                          |



 

## <a name="generic-video-image"></a>Immagine video generica

Un flusso di immagini video che non rientra in una delle specifiche di livello verrà assegnato "I" come stringa del modello di conformità del dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modelli di conformità del dispositivo audio**](audio-device-conformance-templates.md)
</dt> <dt>

[**Parametri del modello di conformità del dispositivo**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinazioni consigliate per il modello di conformità dei dispositivi**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





