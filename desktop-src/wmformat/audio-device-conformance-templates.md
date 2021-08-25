---
title: Modelli di conformità dei dispositivi audio
description: Modelli di conformità dei dispositivi audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media Format SDK, modelli di conformità dei dispositivi
- Advanced Systems Format (ASF), modelli di conformità dei dispositivi
- ASF (Advanced Systems Format),modelli di conformità dei dispositivi
- Windows Media Format SDK, modelli di conformità dei dispositivi audio
- Advanced Systems Format (ASF), modelli di conformità dei dispositivi audio
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi audio
- Windows Codec Audio multimediale 9, modelli di conformità dei dispositivi audio
- codec, codec Windows Media Audio 9
- modelli di conformità dei dispositivi, video
- modelli di conformità dei dispositivi audio
- modelli, modelli di conformità dei dispositivi audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b66c3c414ef2132120cb0824e1e48847310396cf8002d95be13d7f841a0ff6db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840251"
---
# <a name="audio-device-conformance-templates"></a>Modelli di conformità dei dispositivi audio

Nella tabella seguente sono elencati i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 o versione successiva.



| Stringa del modello | Intervallo di velocità in bit     | Note                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "L1"            | 64 Kbps 160 Kbps | Questo modello è destinato ai dispositivi vincolati solo audio.                                                                                                                                                                        |
| "L2"            | <= 160 Kbps     | Questo modello corrisponde alla classe 4 nel kit Windows porting dell'audio multimediale, che supporta l'intera Windows decodificatore audio multimediale.                                                                                   |
| "L3"            | <= 384 Kbps     | Questo modello corrisponde alla classe 4 nel Windows di porting audio multimediale, che supporta l'intera Windows decodificatore audio multimediale. L'intervallo di velocità in bit è l'unica differenza tra questo modello e L2.<br/> |
| "L"             | Tutte le velocità in bit      | Questo modello è solo per l'uso con i personal computer e viene in genere usato per presentare tutte le funzionalità del codec.                                                                                                           |



 

La tabella seguente elenca i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 Voice.



| Stringa del modello | Intervallo di velocità in bit | Note                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| "S1"            | <= 20 Kbps  | Questo modello è destinato solo ai dispositivi con complessità molto bassa. Questo modello è solo voce.<br/>                    |
| "S2"            | <= 20 Kbps  | Questo è il modello consigliato per la maggior parte delle applicazioni. Questo modello supporta combinazioni di voce e musica.<br/> |



 

Nella tabella seguente sono elencati i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 Professional o versione successiva.



| Stringa del modello | Proprietà                                                                                   | Note                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "M1"            | Velocità in bit <= 384 KbpsSampling rate <= 48 kHz<br/> Canali <= 5.1<br/>   | Questo modello è consigliato per i film standard con audio surround.                                                                                                                                                                           |
| "M2"            | Velocità in bit <= 768 KbpsSampling rate <= 96 kHz<br/> Canali <= 5.1<br/>   | Questo modello è consigliato per i film ad alta definizione con audio surround.                                                                                                                                                                    |
| "M3"            | Velocità in bit <= 1.500 KbpsSampling rate <= 96 kHz<br/> Canali <= 7.1<br/> | Questo modello è consigliato per i film ad alta definizione con audio surround a 8 canali, ad esempio il contenuto codificato per la presentazione nelle sale.                                                                                                    |
| "M"             | Tutte le frequenze di bitTutte le frequenze di campionamento<br/> Tutti i canali<br/>                           | Questo modello è solo per l'uso con i personal computer e viene in genere usato per presentare tutte le funzionalità del codec. Questa è anche la designazione del modello per tutto l'audio codificato con il codec Windows Media Audio 9 Lossless.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Parametri del modello di conformità del dispositivo**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinazioni consigliate di modelli di conformità dei dispositivi**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Modelli di conformità dei dispositivi video**](video-device-conformance-templates.md)
</dt> </dl>

 

 





