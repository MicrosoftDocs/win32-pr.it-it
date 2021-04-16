---
description: Un client XAudio2 ha il controllo completo del mapping tra i canali di una voce e i canali di ciascuna voce di destinazione.
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: Mapping del canale predefinito XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d77371223ccef02d6f0831a7aea182326f8477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485860"
---
# <a name="xaudio2-default-channel-mapping"></a>Mapping del canale predefinito XAudio2

Un client XAudio2 dispone del controllo completo del mapping tra i canali di una voce e i canali di ogni voicesIt di destinazione controlla il mapping tramite l'utilizzo del metodo [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) . In alcune circostanze, tuttavia, XAudio2 semplifica questa attività impostando automaticamente una matrice di trasmissione predefinita. A tale scopo, viene utilizzato il canale Mask, se presente, associato ai canali audio di una voce. Una maschera di canale è una combinazione di \_ maschere di bit xxx come definito in X3DAudio. h e altrove. XAudio2 richiede che le maschere del canale siano 0 o che lo stesso numero di bit sia impostato come numero di canali.

Nella tabella seguente vengono illustrati i requisiti e le impostazioni predefinite della maschera di canale per i formati supportati da XAudio2. 

| Formato | Requisito Channel mask             | Maschera predefinita                        | Membro della struttura corrispondente                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | Il file potrebbe contenere una maschera di canale    | La maschera del canale è 0 o assente        | WAVEFORMATEXTENSIBLE. dwChannelMask o None (WAVEFORMATEX) |
| ADPCM  | Il file non contiene una maschera di canale | Viene sempre utilizzata la maschera di canale predefinita | Nessuno (ADPCMWAVEFORMAT)                                    |



 

Per le voci submix e mastering e per le voci di origine senza una maschera di canale o una maschera di canale pari a 0, XAudio2 presuppone le posizioni predefinite del relatore in base alla tabella seguente. 

| Canali  | Posizioni del canale implicite                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | Viene sempre eseguito il mapping a FrontLeft e FrontRight su scala completa in entrambi gli altoparlanti (caso speciale per i suoni mono)                 |
| 2         | FrontLeft, FrontRight (configurazione stereo di base)                                                                    |
| 3         | FrontLeft, FrontRight, LowFrequency (configurazione 2,1)                                                               |
| 4         | FrontLeft, FrontRight, backLeft, backright (quadrifonica)                                                             |
| 5         | FrontLeft, FrontRight, FrontCenter, SideLeft, SideRight (configurazione 5,0)                                           |
| 6         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight (configurazione 5,1) (vedere le osservazioni seguenti) |
| 7         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight, backcenter (6,1 Configuration)                 |
| 8         | FrontLeft, FrontRight, FrontCenter, LowFrequency, backLeft, backright, SideLeft, SideRight (configurazione 7,1)        |
| 9 o più | Nessuna posizione implicita (mapping uno a uno)                                                                            |



 

Se una coppia vocale specificata nel grafico audio non dispone di posizioni dell'altoparlante associate alla voce di origine o di destinazione (una voce ha più di otto canali), nessuna voce è giocabile finché la voce di origine non dispone di una matrice di trasmissione impostata in modo esplicito tramite il metodo [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) . La chiamata al metodo [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) per entrambe le voci avrà esito negativo fino a quando non si esegue questa operazione.

Se la voce di origine e la voce di destinazione hanno un numero diverso di posizioni del relatore e [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) non è stato chiamato sulla voce di origine, XAudio2 invia ogni canale di origine al relatore di destinazione più vicino (o agli altoparlanti) disponibili, proporzionalmente alla distanza di relatore desiderata. Esistono due casi speciali in cui il comportamento predefinito è diverso.

1.  Se l'audio di origine è mono ed è posizionato in corrispondenza del centro del altoparlante \_ \_ o non ha una posizione definita, viene sempre inviato all'altoparlante \_ anteriore \_ sinistro e all'altoparlante \_ anteriore \_ destro, se esistono nell'audio di output. Se non esistono, viene eseguito il fallback al normale caso.
2.  Se l'origine e la destinazione sono entrambi a 6 canali e sono posizionati in corrispondenza di una delle configurazioni standard di 5,1 Speaker (Left + Right + Center + Sub + Backal + Backr o Left + Right + Center + Sub + SideL + Sider), i canali vengono mappati attraverso uno a uno. In altre parole, SideLeft/Right e backLeft/right vengono considerati equivalenti. Questo è dovuto al fatto che si è verificata una confusione storica per queste configurazioni. Pertanto, lo scopo presunto è sempre di eseguire il mapping uno-a-uno.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci](voices.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[**GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
