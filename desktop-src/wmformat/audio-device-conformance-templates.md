---
title: Modelli di conformità del dispositivo audio
description: Modelli di conformità del dispositivo audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media Format SDK, modelli di conformità del dispositivo
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
- Windows Media Format SDK, modelli di conformità del dispositivo audio
- Modelli di conformità dei sistemi avanzati (ASF), modelli di conformità dei dispositivi audio
- ASF (formato avanzato dei sistemi), modelli di conformità del dispositivo audio
- Windows Media Audio 9 codec, modelli di conformità del dispositivo audio
- codec, Windows Media Audio 9 codec
- modelli di conformità del dispositivo, video
- modelli di conformità del dispositivo audio
- modelli, modelli di conformità dei dispositivi audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329895"
---
# <a name="audio-device-conformance-templates"></a>Modelli di conformità del dispositivo audio

La tabella seguente elenca i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 o versioni successive.



| Stringa modello | Intervallo di velocità in bit     | Note                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L1            | 64 Kbps 160 Kbps | Questo modello è destinato a dispositivi solo audio vincolati.                                                                                                                                                                        |
| L2            | <= 160 Kbps     | Questo modello corrisponde alla classe 4 nel Windows Media Audio Porting Kit, che supporta l'intera implementazione del decodificatore Windows Media Audio.                                                                                   |
| L3            | <= 384 kbps     | Questo modello corrisponde alla classe 4 nel Windows Media Audio Porting Kit, che supporta l'intera implementazione del decodificatore Windows Media Audio. L'intervallo della velocità in bit è l'unica differenza tra questo modello e L2.<br/> |
| L             | Tutte le velocità in bit      | Questo modello è da usare solo con personal computer e viene in genere usato per presentare le funzionalità complete del codec.                                                                                                           |



 

La tabella seguente elenca i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 Voice.



| Stringa modello | Intervallo di velocità in bit | Note                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| S1            | <= 20 kbps  | Questo modello è destinato solo ai dispositivi con complessità molto bassa. Questo modello è solo sintesi vocale.<br/>                    |
| S2            | <= 20 kbps  | Si tratta del modello consigliato per la maggior parte delle applicazioni. Questo modello supporta combinazioni di riconoscimento vocale e musica.<br/> |



 

La tabella seguente elenca i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 Professional o versioni successive.



| Stringa modello | Proprietà                                                                                   | Note                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M1            | Velocità in bit <= 384 velocità KbpsSampling <= 48 kHz<br/> Canali <= 5,1<br/>   | Questo modello è consigliato per i film standard con audio surround.                                                                                                                                                                           |
| M2            | Velocità in bit <= 768 velocità KbpsSampling <= 96 kHz<br/> Canali <= 5,1<br/>   | Questo modello è consigliato per i filmati ad alta definizione con audio surround.                                                                                                                                                                    |
| M3            | Velocità in bit <= 1.500 velocità KbpsSampling <= 96 kHz<br/> Canali <= 7,1<br/> | Questo modello è consigliato per i filmati ad alta definizione con audio surround a 8 canali, ad esempio il contenuto codificato per la presentazione nei teatri.                                                                                                    |
| "M"             | Tutte le frequenze di campionamento ratesAll bit<br/> Tutti i canali<br/>                           | Questo modello è da usare solo con personal computer e viene in genere usato per presentare le funzionalità complete del codec. Si tratta anche della designazione del modello per tutti gli audio codificati con il codec Windows Media Audio 9 Lossless.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Parametri del modello di conformità del dispositivo**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinazioni consigliate per il modello di conformità dei dispositivi**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Modelli di conformità del dispositivo video**](video-device-conformance-templates.md)
</dt> </dl>

 

 





