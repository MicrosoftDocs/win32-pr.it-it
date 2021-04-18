---
title: Funzioni XAudio2
description: Questa sezione contiene informazioni sulle funzioni fornite dall'API Microsoft XAudio2.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd8bcfdb00565d6f8bbc31ae0ee6a24f106dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314420"
---
# <a name="xaudio2-functions"></a>Funzioni XAudio2

Questa sezione contiene informazioni sulle funzioni fornite dall'API Microsoft XAudio2.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                       | Descrizione                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Crea un'istanza dell'effetto [XAPOFX](xapofx-overview.md) richiesto.<br/>                                                                                                                                                         |
| [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Crea un'istanza dell'interfaccia [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) per l'elaborazione HRTF (Head-Related Transfer Function).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Funzione inline che converte i parametri I3DL2 (Interactive 3D audio rendering Guidelines Level 2,0) in parametri XAudio2 nativi.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Calcola le impostazioni DSP rispetto ai parametri 3D.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Imposta tutte le costanti audio 3D globali.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Funzione inline che converte un valore del rapporto di ampiezza in un valore di decibel.<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Crea un nuovo oggetto **XAudio2** e restituisce un puntatore alla relativa interfaccia [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Crea un nuovo oggetto di elaborazione audio di riverbero (APO) e restituisce un puntatore a tale oggetto.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Crea un nuovo oggetto di elaborazione audio del contatore del volume (APO) e ne restituisce un puntatore.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Funzione inline che esegue la conversione dalle frequenze di taglio del filtro espresse in Hertz ai coefficienti di filtro utilizzati con il membro **Frequency** della struttura dei [**\_ \_ parametri del filtro XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Funzione inline che esegue la conversione dalle frequenze di taglio del filtro espresse in Hertz ai valori di frequenza radianti utilizzati nel membro **Frequency** della struttura dei [**\_ \_ parametri del filtro XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Funzione inline che converte un valore di decibel in un valore di proporzioni di ampiezza.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Funzione inline che converte un valore frequency ratio in un valore semitono.<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Funzione inline che esegue la conversione dalle frequenze radianti usate [**nei \_ \_ parametri di filtro XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) a frequenze assolute in Hertz.<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Funzione inline che converte un valore semitono in un valore frequency ratio.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[XAudio2: riferimento a:P rogramming](programming-reference.md)
</dt> </dl>

 

 




