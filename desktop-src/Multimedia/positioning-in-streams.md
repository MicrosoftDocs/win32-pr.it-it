---
title: Posizionamento in Flussi
description: Posizionamento in Flussi
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- Funzione AVIStreamStart
- Funzione AVIStreamFindSample
- Funzione AVIStreamSampleToTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0528fea9ea10e28a418d253bd1abe6c599a952fe95a8c8f6c86807abe0e41159
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805861"
---
# <a name="positioning-in-streams"></a>Posizionamento in Flussi

AVIFile offre diversi modi per individuare e passare a una posizione in un flusso di dati. Le funzioni e le macro in questa sezione consentono all'applicazione di trovare la posizione iniziale, la lunghezza e i fotogrammi chiave (contenenti un'immagine completa nell'esempio) all'interno di un flusso. Le funzioni e le macro associano anche il tempo alle posizioni in un flusso calcolando il tempo trascorso necessario per riprodurre un flusso dall'inizio a qualsiasi punto di un flusso.

## <a name="finding-the-starting-position"></a>Ricerca della posizione iniziale

È possibile recuperare il numero di esempio del primo fotogramma in un flusso video usando la [**funzione AVIStreamStart.**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) I fotogrammi di un film potrebbero iniziare dall'esempio 0 o 1, a seconda della preferenza dell'autore. È anche possibile ottenere queste informazioni usando la [**funzione AVIStreamInfo.**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) Questa funzione archivia il numero di esempio nel **membro dwStart** della [**struttura AVISTREAMINFO.**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) È possibile recuperare l'ora di inizio del primo esempio di un flusso usando la macro [**AVIStreamStartTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)

È possibile recuperare la lunghezza del flusso usando la [**funzione AVIStreamLength.**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) Questa funzione restituisce il numero di esempi nel flusso. È anche possibile ottenere queste informazioni usando la **funzione AVIStreamInfo.** Questa funzione archivia la lunghezza del flusso nel **membro dwLength** della **struttura AVISTREAMINFO.** Per recuperare la lunghezza di un flusso in millisecondi, usare la macro [**AVIStreamLengthTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)

In un flusso video, ogni esempio corrisponde in genere a un fotogramma di video. Potrebbero tuttavia essere presenti esempi per cui non sono presenti dati video. Se si chiama la [**funzione AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) specificando una di queste posizioni, viene restituita una lunghezza dei dati pari a 0 byte. È possibile trovare esempi che contengono dati usando la [**funzione AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) e specificando il flag FIND \_ ANY.

In un flusso audio, ogni campione corrisponde a un blocco di dati di dati audio. Ad esempio, se i dati audio hanno un formato ADPCM (Adaptive Differential Pulse Code Modulation) a 22 kHz, ogni campione per **AVIStreamLength** corrisponde a un blocco di 256 byte di dati audio compressi. Questo blocco di dati audio contiene circa 500 campioni audio quando non sono compressi. Le funzioni e le macro di AVIFile, tuttavia, trattano ogni blocco di 256 byte come un singolo esempio.

> [!Note]  
> Posizioni valide all'interno di un intervallo di flussi dall'inizio alla fine del flusso, ovvero la somma del punto iniziale del flusso e della relativa lunghezza. La posizione rappresentata dalla somma della posizione iniziale e della lunghezza corrisponde a un'ora dopo il rendering degli ultimi dati. non contiene dati. È possibile recuperare il numero di esempio che rappresenta la fine del flusso usando la macro [**AVIStreamEnd.**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) È possibile recuperare il valore temporale in millisecondi che rappresenta la fine del flusso usando la macro [**AVIStreamEndTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

 

## <a name="finding-sample-and-key-frames"></a>Ricerca di fotogrammi chiave e di esempio

È possibile cercare diversi tipi di esempi in un flusso usando la [**funzione AVIStreamFindSample.**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) Questa funzione cerca in avanti o indietro in un flusso un esempio del tipo appropriato, a partire dal numero di esempio specificato. È possibile cercare diversi tipi di esempi in un flusso specificando un flag nella sequenza di chiamata **AVIStreamFindSample.** Specificare il flag FIND \_ ANY per individuare gli esempi non erppi o per ignorare gli esempi che non dispongono di dati. Specificare il flag FIND KEY per cercare fotogrammi chiave che contengono i dati per eseguire il rendering di un'immagine completa senza dover \_ fare riferimento ai fotogrammi precedenti. Specificare il flag FIND \_ FORMAT per cercare le modifiche al formato. **AVIStreamFindSample** viene usato principalmente con flussi video.

Diverse macro che usano funzioni AVIFile integrano le funzionalità di ricerca del flusso. Nell'elenco seguente viene fornita una breve descrizione di ogni macro. Le macro che ricercano una posizione o un tipo di dati specifico richiedono che nel flusso sia specificata una posizione iniziale.



| Macro                                                                | Descrizione                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Indica se un campione in un flusso specificato è un fotogramma chiave.                                                            |
| [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Individua il fotogramma chiave in corrispondenza o prima di una posizione specificata in un flusso.                                                     |
| [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Determina l'ora corrispondente all'inizio del fotogramma chiave più vicina (in corrispondenza o precedente) a un'ora specificata in un flusso. |
| [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Individua l'esempio non empty più vicino in corrispondenza o che precede una posizione specificata in un flusso.                                       |
| [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Determina l'ora corrispondente all'inizio di un campione più vicino a un'ora specificata in un flusso.             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Individua il fotogramma chiave successivo dopo una posizione specificata in un flusso.                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Restituisce l'ora del fotogramma chiave successivo in un flusso, a partire da un determinato momento.                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Individua l'esempio successivo non empty da una posizione specificata in un flusso.                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Restituisce l'ora in cui un esempio viene modificato nell'esempio successivo nel flusso.                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Individua il fotogramma chiave che precede una posizione specificata in un flusso.                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Restituisce l'ora del fotogramma chiave precedente nel flusso, a partire da un determinato momento.                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Individua l'esempio non empty che precede una posizione specificata in un flusso.                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Determina l'ora in cui l'esempio precedente sostituisce il relativo predecessore nel flusso.                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Restituisce l'esempio in un flusso che si verifica contemporaneamente a un campione che si verifica in un secondo flusso.                     |



 

## <a name="switching-between-samples-and-time"></a>Passaggio tra esempi e ora

È possibile determinare il tempo trascorso dall'inizio di un flusso a un esempio usando la [**funzione AVIStreamSampleToTime.**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) Questa funzione converte il numero di esempio in un valore di ora espresso in millisecondi. Per un fotogramma video (che si estende per diversi millisecondi), questo valore rappresenta l'ora in cui l'esempio inizia a essere riprodotto dall'inizio della riproduzione e presuppone che il clip video sia riprodotto alla velocità normale. Per un campione audio (che ha diversi campioni in millisecondi), il valore temporale corrisponde al momento in cui inizia la riproduzione del campione e presuppone che il flusso audio sia riprodotto alla velocità normale.

Al contrario, è possibile trovare il numero di esempio associato a un valore di ora usando la [**funzione AVIStreamTimeToSample.**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) Questa funzione converte il valore del millisecondo in un numero di campione e presuppone che il clip video sia riprodotto alla velocità normale.

Poiché **AVIStreamSampleToTime** restituisce l'ora in cui inizia la riproduzione di un frame, la relazione tra **AVIStreamSampleToTime** e **AVIStreamTimeToSample** non è realmente inversa. Determinano la posizione in un file in modo più accurato rispetto a quanto determinano l'ora. Ad esempio, due campioni audio consecutivi possono essere riprodotti entrambi nello stesso millisecondo. **L'uso di AVIStreamSampleToTime** per convertire i numeri di esempio comporterebbe valori temporici identici. Se si converte il valore di ora in un numero di esempio usando **AVIStreamTimeToSample,** viene fatto riferimento a un singolo esempio.

 

 




