---
title: Modelli di conformità dei dispositivi video
description: Modelli di conformità dei dispositivi video
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- Windows Media Format SDK, modelli di conformità dei dispositivi
- Advanced Systems Format (ASF), modelli di conformità dei dispositivi
- ASF (Advanced Systems Format),modelli di conformità dei dispositivi
- Windows Media Format SDK, modelli di conformità dei dispositivi video
- Advanced Systems Format (ASF), modelli di conformità dei dispositivi video
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi video
- Windows Codec Media Video 9, modelli di conformità dei dispositivi video
- codec, codec Windows Media Video 9
- modelli di conformità dei dispositivi, video
- modelli di conformità dei dispositivi video
- modelli, modelli di conformità dei dispositivi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df63d40152e814f879498f0f99e386c9b21ef1e32746cf0c405aa46ab9d2fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584841"
---
# <a name="video-device-conformance-templates"></a>Modelli di conformità dei dispositivi video

Le tabelle seguenti elencano i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Video 9.

## <a name="simple-profile-low-level"></a>Profilo semplice, livello basso



| Parametro                                | Valore                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Stringa del modello                          | "SP@LL"                                                                               |
| Dispositivi appropriati                      | Telefoni wireless (soluzione SmartPhone Windows-Powered Microsoft e dispositivi simili) |
| Risoluzione massima                       | 176 x 144                                                                             |
| Frequenza fotogrammi massima                       | 15 fps                                                                                |
| Velocità in bit massima                         | 96 Kbps                                                                               |
| Dimensioni massime del buffer (in unità a 16384 bit) | 20 (circa 3,4 secondi alla velocità in bit massima)                                            |
| Codifica interlacciata                      | No                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Profilo semplice, livello medio



| Parametro                                | Valore                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Stringa del modello                          | "SP@ML"                                                                              |
| Dispositivi appropriati                      | Computer portatili e assistenti ai dati personaliSitteri wireless di fascia alta<br/> |
| Risoluzione massima                       | 352 x 288                                                                            |
| Frequenza fotogrammi massima                       | 15 fps @ 352 x 28824 fps @ 320 x 240<br/>                                      |
| Velocità in bit massima                         | 384 Kbps                                                                             |
| Dimensioni massime del buffer (in unità a 16384 bit) | 77 (circa 3,3 secondi alla velocità in bit massima)                                           |
| Codifica interlacciata                      | No                                                                                   |



 

## <a name="generic-simple-profile"></a>Profilo semplice generico

A un flusso conforme alle limitazioni algoritmiche del profilo semplice, ma che non rientra in una delle specifiche di livello, verrà assegnato "SP" come stringa del modello di conformità del dispositivo.

## <a name="main-profile-low-level"></a>Profilo principale, livello basso



| Parametro                                | Valore                                       |
|------------------------------------------|---------------------------------------------|
| Stringa del modello                          | "MP@LL"                                     |
| Dispositivi appropriati                      | Set-top box                               |
| Risoluzione massima                       | 352 x 288                                   |
| Frequenza fotogrammi massima                       | 30 fps                                      |
| Velocità in bit massima                         | 2 Mbps                                      |
| Dimensioni massime del buffer (in unità a 16384 bit) | 306 (circa 2,5 secondi alla velocità in bit massima) |
| Codifica interlacciata                      | No                                          |



 

## <a name="main-profile-medium-level"></a>Profilo principale, livello medio



| Parametro                                | Valore                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Stringa del modello                          | "MP@ML"                                                                                                                |
| Dispositivi appropriati                      | Set-top boxSlower computers using DirectX Video Acceleration<br/> Windows Lettori DVD abilitati per i supporti<br/> |
| Risoluzione massima                       | 720 x 576                                                                                                              |
| Frequenza fotogrammi massima                       | 30 fps @ 720 x 48025 fps @ 720 x 576<br/>                                                                        |
| Velocità in bit massima                         | 10 Mbps                                                                                                                |
| Dimensioni massime del buffer (in unità a 16384 bit) | 611 (circa 1 secondo alla velocità in bit massima)                                                                               |
| Codifica interlacciata                      | Sì                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Profilo principale, livello alto



| Parametro                                | Valore                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stringa del modello                          | "MP@HL"                                                                                                                                                               |
| Dispositivi appropriati                      | Computer che usano lettori DVD AccelerationHigh-Definition Windows DirectX Video abilitati per supporti<br/> Digital cinema<br/> streaming ad alta definizione<br/> |
| Risoluzione massima                       | 1920 x 1080                                                                                                                                                           |
| Frequenza fotogrammi massima                       | 30 fps @ 1920 x 108060 fps @ 1280 x 720<br/>                                                                                                                    |
| Velocità in bit massima                         | 20 Mbps                                                                                                                                                               |
| Dimensioni massime del buffer (in unità a 16384 bit) | 2442 (circa 2,66 secondi alla velocità in bit massima)                                                                                                                         |
| Codifica interlacciata                      | Sì                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Profilo principale generico

A un flusso conforme alle limitazioni algoritmiche del profilo principale, ma che non rientra in una delle specifiche di livello, verrà assegnato "MP" come stringa del modello di conformità del dispositivo.

## <a name="complex-profile"></a>Profilo complesso



| Parametro       | Valore                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Stringa del modello | "CP"                                                                                                                                   |
| Commenti         | Il profilo complesso non presenta limitazioni esplicite. Viene usato per abilitare tutti gli algoritmi di codec, in genere a scopo dimostrativo. |



 

Le tabelle seguenti elencano i parametri dei modelli di conformità dei dispositivi per il codec Windows Media Video 9 Image.

## <a name="video-image-level-1"></a>Livello 1 dell'immagine video



| Parametro                                | Valore                                       |
|------------------------------------------|---------------------------------------------|
| Stringa del modello                          | "I1"                                        |
| Risoluzione massima                       | 352 x 288                                   |
| Frequenza fotogrammi massima                       | 30 fps                                      |
| Velocità in bit massima                         | 192 Kbps                                    |
| Dimensioni massime del buffer (in unità a 16384 bit) | 39 (circa 3,26 secondi alla velocità in bit massima) |
| Codifica interlacciata                      | No                                          |



 

## <a name="video-image-level-2"></a>Livello 2 dell'immagine video



| Parametro                                | Valore                                       |
|------------------------------------------|---------------------------------------------|
| Stringa del modello                          | "I2"                                        |
| Risoluzione massima                       | 1024 x 768                                  |
| Frequenza fotogrammi massima                       | 30 fps                                      |
| Velocità in bit massima                         | 384 Kbps                                    |
| Dimensioni massime del buffer (in unità a 16384 bit) | 77 (circa 3,26 secondi alla velocità in bit massima) |
| Codifica interlacciata                      | No                                          |



 

## <a name="generic-video-image"></a>Immagine video generica

A un flusso di immagini video che non rientra in una delle specifiche di livello verrà assegnato "I" come stringa del modello di conformità del dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modelli di conformità dei dispositivi audio**](audio-device-conformance-templates.md)
</dt> <dt>

[**Parametri del modello di conformità del dispositivo**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinazioni consigliate di modelli di conformità dei dispositivi**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





