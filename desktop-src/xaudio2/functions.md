---
title: Funzioni XAudio2
description: Questa sezione contiene informazioni sulle funzioni fornite dall'API Microsoft XAudio2.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b950ce33f55a4b834f3ee7a068f613e144c2e30633c67e887b8a24789140a618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109651"
---
# <a name="xaudio2-functions"></a>Funzioni XAudio2

Questa sezione contiene informazioni sulle funzioni fornite dall'API Microsoft XAudio2.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                       | Descrizione                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Crea un'istanza [dell'effetto XAPOFX](xapofx-overview.md) richiesto.<br/>                                                                                                                                                         |
| [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Crea un'istanza [**dell'interfaccia IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) per l'elaborazione hrTF (Head-Related Transfer Function).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Funzione inline che converte i parametri I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) in parametri XAudio2 nativi.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Calcola le impostazioni DSP rispetto ai parametri 3D.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Imposta tutte le costanti audio 3D globali.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Funzione inline che converte un valore del rapporto di ampiezza in un valore decibel.<br/>                                                                                                                                                         |
| [**XAudio2Crea**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Crea un nuovo **oggetto XAudio2** e restituisce un puntatore alla relativa [**interfaccia IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Crea un nuovo oggetto di elaborazione audio riverbero (APO) e restituisce un puntatore a esso.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Crea un nuovo oggetto di elaborazione audio del contatore del volume (APO) e restituisce un puntatore a esso.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Funzione inline che esegue la conversione dalle frequenze di taglio del filtro espresse in hertz ai coefficienti di filtro usati con il membro **Frequency** della [**struttura XAUDIO2 \_ FILTER \_ PARAMETERS.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)<br/>   |
| [**XAudio2CutoffFrequencyToRadian**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Funzione inline che esegue la conversione dalle frequenze di taglio del filtro espresse in hertz ai valori di frequenza radianti usati nel membro **Frequency** della [**struttura XAUDIO2 \_ FILTER \_ PARAMETERS.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Funzione inline che converte un valore decibel in un valore di rapporto di ampiezza.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Funzione inline che converte un valore di rapporto di frequenza in un valore semitone.<br/>                                                                                                                                                         |
| [**XAudio2RadianToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Funzione inline che converte dalle frequenze radianti usate in [**XAUDIO2 \_ FILTER \_ PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) alle frequenze assolute in hertz.<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Funzione inline che converte un valore semitone in un valore di rapporto di frequenza.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su XAudio2::P rogramming](programming-reference.md)
</dt> </dl>

 

 




