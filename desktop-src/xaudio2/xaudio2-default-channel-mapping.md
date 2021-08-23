---
description: Un client XAudio2 ha il controllo completo del mapping dai canali di una voce ai canali di ogni voce di destinazione.
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: Mapping dei canali predefinito XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42bb2f67709586532a19d86a916d3b7852652e76f9b6ce1ae115f1fc670e37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025949"
---
# <a name="xaudio2-default-channel-mapping"></a>Mapping dei canali predefinito XAudio2

Un client XAudio2 ha il controllo completo del mapping dai canali di una voce ai canali di ogni voce di destinazioneIt controlla il mapping tramite l'uso del metodo [**IXAudio2Voice::SetOutputMatrix.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) In alcune circostanze, tuttavia, XAudio2 semplifica questa attività configurando automaticamente una matrice di invio predefinita. A tale scopo, usa la maschera di canale, se presente, associata ai canali audio di una voce. Una maschera di canale è una combinazione di maschere di bit SPEAKER xxx, come definito \_ in X3DAudio.h e altrove. XAudio2 richiede che le maschere di canale siano 0 o che sia impostato lo stesso numero di bit del numero di canali.

La tabella seguente illustra i requisiti e le impostazioni predefinite della maschera del canale per i formati supportati da XAudio2. 

| Formato | Requisito della maschera di canale             | Maschera predefinita                        | Membro della struttura corrispondente                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | Il file potrebbe contenere una maschera di canale    | Channel mask è 0 o assente        | WAVEFORMATEXTENSIBLE.dwChannelMask o none (WAVEFORMATEX) |
| Adpcm  | Il file non contiene una maschera di canale | Viene sempre usata la maschera di canale predefinita | Nessuno (ADPCMWAVEFORMAT)                                    |



 

Per le voci submix e mastering e per le voci di origine senza channel mask o channel mask 0, XAudio2 presuppone le posizioni predefinite del parlante in base alla tabella seguente. 

| Canali  | Posizioni implicite dei canali                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | Esegue sempre il mapping a FrontLeft e FrontRight su larga scala in entrambi gli altoparlanti (caso speciale per suoni mono)                 |
| 2         | FrontLeft, FrontRight (configurazione stereo di base)                                                                    |
| 3         | FrontLeft, FrontRight, LowFrequency (configurazione 2.1)                                                               |
| 4         | FrontLeft, FrontRight, BackLeft, BackRight (quadrafono)                                                             |
| 5         | FrontLeft, FrontRight, FrontCenter, SideLeft, SideRight (configurazione 5.0)                                           |
| 6         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight (configurazione 5.1) (vedere le osservazioni seguenti) |
| 7         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight, BackCenter (configurazione 6.1)                 |
| 8         | FrontLeft, FrontRight, FrontCenter, LowFrequency, BackLeft, BackRight, SideLeft, SideRight (configurazione 7.1)        |
| 9 o più | Nessuna posizione implicita (mapping uno-a-uno)                                                                            |



 

Se una determinata coppia di voci nel grafico audio non ha posizioni del parlante associate alla voce di origine o di destinazione (una voce ha più di otto canali), nessuna voce può essere riprodotta finché la voce di origine non ha una matrice di invio impostata in modo esplicito usando il metodo [**IXAudio2Voice::SetOutputMatrix.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) La chiamata [**al metodo IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) per entrambe le voci avrà esito negativo fino a quando non si esegue questa operazione.

Se la voce di origine e la voce di destinazione hanno un numero diverso di posizioni degli altoparlanti e [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) non è stato chiamato sulla voce di origine, XAudio2 invia ogni canale di origine all'altoparlante di destinazione (o ai parlanti) di destinazione più vicino disponibile, in proporzione alla loro vicinanza all'altoparlante previsto. Esistono due casi speciali in cui il comportamento predefinito è diverso.

1.  Se l'audio di origine è mono e viene posizionato in POSIZIONE FRONT CENTER VOCE o non ha una posizione definita, viene sempre inviato a SPEAKER FRONT LEFT e SPEAKER FRONT RIGHT se sono presenti nell'audio di \_ \_ \_ \_ \_ \_ output. Se non esistono, torna al caso normale.
2.  Se l'origine e la destinazione sono entrambe a 6 canali e sono posizionate in una delle configurazioni standard degli altoparlanti 5.1 (Left+Right+Center+Sub+BackL+BackR o Left+Right+Center+Sub+SideL+SideR), i canali vengono mappati uno a uno. In altre parole, SideLeft/Right e BackLeft/Right vengono trattati in modo equivalente. Ciò è dovuto al fatto che si è verificata confusione cronologica in queste configurazioni. Pertanto, l'intento presupposto è sempre quello di eseguire il mapping uno a uno.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci](voices.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[**GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
