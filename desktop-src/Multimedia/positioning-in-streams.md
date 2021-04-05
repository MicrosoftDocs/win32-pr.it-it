---
title: Posizionamento nei flussi
description: Posizionamento nei flussi
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- AVIStreamStart (funzione)
- AVIStreamFindSample (funzione)
- AVIStreamSampleToTime (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252aa938d32c323da9fcf7ae106d11db0ff2fb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709865"
---
# <a name="positioning-in-streams"></a>Posizionamento nei flussi

In AVIFile sono disponibili diversi modi per individuare e spostare in una posizione in un flusso di dati. Le funzioni e le macro in questa sezione consentono all'applicazione di individuare la posizione iniziale, la lunghezza e i fotogrammi chiave (contenenti un'immagine completa nell'esempio) all'interno di un flusso. Le funzioni e le macro inoltre associano l'ora alle posizioni in un flusso calcolando il tempo trascorso necessario per riprodurre un flusso dall'inizio a qualsiasi punto in un flusso.

## <a name="finding-the-starting-position"></a>Individuazione della posizione iniziale

È possibile recuperare il numero di esempio del primo frame in un flusso video usando la funzione [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) . I frame di un film possono iniziare in corrispondenza dell'esempio 0 o 1, a seconda delle preferenze dell'autore. È possibile ottenere queste informazioni anche tramite la funzione [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) . Questa funzione archivia il numero di esempio nel membro **dwStart** della struttura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) . È possibile recuperare l'ora di inizio del primo esempio di un flusso usando la macro [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime) .

È possibile recuperare la lunghezza del flusso tramite la funzione [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) . Questa funzione restituisce il numero di campioni nel flusso. È possibile ottenere queste informazioni anche tramite la funzione **AVIStreamInfo** . Questa funzione Archivia la lunghezza del flusso nel membro **dwLength** della struttura **AVISTREAMINFO** . Per recuperare la lunghezza di un flusso in millisecondi, usare la macro [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime) .

In un flusso video, ogni campione corrisponde in genere a un frame di video. Potrebbero, tuttavia, essere presenti esempi per i quali non sono presenti dati video. Se si chiama la funzione [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) specificando una di queste posizioni, viene restituita una lunghezza di dati di 0 byte. È possibile trovare esempi che contengono dati tramite la funzione [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) e specificando il \_ flag find any.

In un flusso audio ogni campione corrisponde a un blocco di dati audio. Se, ad esempio, i dati audio hanno un formato di modulazione del codice Pulse differenziale di 22 kHz, ogni esempio per **AVIStreamLength** corrisponde a un blocco di 256 byte di dati audio compressi. Questo blocco di dati audio contiene circa 500 di campioni audio quando non compressi. Le funzioni e le macro di AVIFile, tuttavia, trattano ogni blocco di 256 byte come singolo campione.

> [!Note]  
> Posizioni valide all'interno di un intervallo di flusso dall'inizio alla fine del flusso, ovvero la somma del punto iniziale del flusso e della relativa lunghezza. La posizione rappresentata dalla somma della posizione iniziale e della lunghezza corrisponde a un periodo di tempo dopo il rendering degli ultimi dati. non contiene dati. È possibile recuperare il numero di esempio che rappresenta la fine del flusso usando la macro [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) . È possibile recuperare il valore di tempo in millisecondi che rappresenta la fine del flusso usando la macro [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime) .

 

## <a name="finding-sample-and-key-frames"></a>Ricerca di fotogrammi chiave e di esempio

È possibile cercare tipi diversi di esempi in un flusso tramite la funzione [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) . Questa funzione esegue la ricerca all'indietro o in avanti tramite un flusso per un campione del tipo appropriato, a partire dal numero di esempio specificato. È possibile cercare tipi diversi di esempi in un flusso specificando un flag nella sequenza chiamante **AVIStreamFindSample** . Specificare il \_ flag find any per individuare gli esempi non vuoti o ignorare gli esempi privi di dati. Specificare il \_ flag trova chiave per cercare i fotogrammi chiave che contengono i dati per eseguire il rendering di un'immagine completa senza dover fare riferimento ai frame precedenti. Specificare il \_ flag trova formato per cercare le modifiche nel formato. **AVIStreamFindSample** viene usato principalmente con i flussi video.

Diverse macro che usano funzioni AVIFile integrano le funzionalità di ricerca di flussi. Nell'elenco seguente viene fornita una breve descrizione di ogni macro. Le macro che cercano una posizione o un tipo di dati specifico richiedono una posizione iniziale da specificare nel flusso.



| Macro                                                                | Descrizione                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Indica se un campione in un flusso specificato è un fotogramma chiave.                                                            |
| [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Individua il fotogramma chiave in corrispondenza o prima di una posizione specificata in un flusso.                                                     |
| [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Determina l'ora corrispondente all'inizio del fotogramma chiave più vicino (alla o precedente) un'ora specificata in un flusso. |
| [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Individua il campione non vuoto più vicino in corrispondenza o prima di una posizione specificata in un flusso.                                       |
| [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Determina l'ora corrispondente all'inizio di un campione che è più vicino a un tempo specificato in un flusso.             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Individua il fotogramma chiave successivo dopo una posizione specificata in un flusso.                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Restituisce l'ora del fotogramma chiave successivo in un flusso, a partire da un determinato momento.                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Individua il successivo campione non vuoto da una posizione specificata in un flusso.                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Restituisce l'ora in cui un esempio viene modificato nell'esempio successivo nel flusso.                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Individua il fotogramma chiave che precede una posizione specificata in un flusso.                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Restituisce l'ora del fotogramma chiave precedente nel flusso, a partire da un determinato momento.                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Individua l'esempio non vuoto che precede una posizione specificata in un flusso.                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Determina l'ora in cui l'esempio precedente sostituisce il relativo predecessore nel flusso.                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Restituisce l'esempio in un flusso che si verifica contemporaneamente a un esempio che si verifica in un secondo flusso.                     |



 

## <a name="switching-between-samples-and-time"></a>Spostamento tra campioni e tempo

È possibile determinare il tempo trascorso dall'inizio di un flusso a un esempio utilizzando la funzione [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) . Questa funzione converte il numero di campione in un valore di ora espresso in millisecondi. Per un fotogramma video (che si estende su diversi millisecondi), questo valore rappresenta l'ora in cui inizia la riproduzione del campione dall'inizio della riproduzione e presuppone che il clip video riproduca la velocità normale. Per un esempio audio (che include diversi esempi in un millisecondo), il valore Time corrisponde all'ora in cui inizia la riproduzione dell'esempio e presuppone che il flusso audio riproduca la velocità normale.

Viceversa, è possibile trovare il numero di esempio associato a un valore di ora tramite la funzione [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) . Questa funzione converte il valore in millisecondi in un numero di campione e presuppone che il clip video riproduca la velocità normale.

Poiché **AVIStreamSampleToTime** restituisce l'ora in cui inizia a riprodurre un frame, la relazione tra **AVIStreamSampleToTime** e **AVIStreamTimeToSample** non è realmente inversa. Determinano la posizione in un file più acurately di quanto determinino il tempo. Ad esempio, due esempi audio consecutivi possono essere riprodotti nello stesso millisecondo. Se si usa **AVIStreamSampleToTime** per convertire i numeri di esempio, si verificheranno valori temporali identici. Se si converte il valore dell'ora di nuovo in un numero di campione usando **AVIStreamTimeToSample**, viene fatto riferimento a un singolo campione.

 

 




