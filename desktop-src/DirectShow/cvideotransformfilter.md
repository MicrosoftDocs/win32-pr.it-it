---
description: La classe CVideoTransformFilter è progettata principalmente come classe di base per i filtri di decompressione AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Classe CVideoTransformFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103877042"
---
# <a name="cvideotransformfilter-class"></a>Classe CVideoTransformFilter

![gerarchia di classi cvideotransformfilter](images/vtsip01.png)

La `CVideoTransformFilter` classe è progettata principalmente come classe di base per i filtri di decompressione AVI. Questa classe aggiunge il supporto per il controllo qualità alla classe [**CTransformFilter**](ctransformfilter.md) . Il metodo di **ricezione** del filtro può decidere di eliminare i frame, in base ai messaggi di qualità del renderer e alle misurazioni delle prestazioni che il filtro raccoglie durante il flusso.

Se il filtro rilascia un frame, continua a rilasciare i frame fino a raggiungere il fotogramma chiave successivo. Per i flussi MPEG, il filtro non distingue tra B frame e P frame.



| Variabili membro protette                                                      | Descrizione                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**\_bQualityChanged m**](cvideotransformfilter-m-bqualitychanged.md)           | Indica se il filtro ha eliminato i frame.                                               |
| [**\_bSkipping m**](cvideotransformfilter-m-bskipping.md)                       | Indica se il filtro sta attualmente eliminando i frame.                                     |
| [**\_itrAvgDecode m**](cvideotransformfilter-m-itravgdecode.md)                 | Durata media del tempo impiegato per decodificare un frame.                                         |
| [**\_itrLate m**](cvideotransformfilter-m-itrlate.md)                           | Indica la fine dell'arrivo degli esempi nel renderer.                                   |
| [**\_nFramesSinceKeyFrame m**](cvideotransformfilter-m-nframessincekeyframe.md) | Numero di frame ricevuti dal filtro dall'ultimo fotogramma chiave.                    |
| [**\_nKeyFramePeriod m**](cvideotransformfilter-m-nkeyframeperiod.md)           | Intervallo osservato più grande tra fotogrammi chiave.                                              |
| [**\_nWaitForKey m**](cvideotransformfilter-m-nwaitforkey.md)                   | Numero massimo corrente di fotogrammi Delta da eliminare.                                            |
| [**\_tDecodeStart m**](cvideotransformfilter-m-tdecodestart.md)                 | Tempo impiegato per decodificare l'esempio più recente.                                  |
| Metodi protetti                                                               | Descrizione                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | Utilizzato per segnalare un errore di streaming.                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | Notifica al filtro che è richiesta una modifica di qualità.                                        |
| [**Ricevere**](cvideotransformfilter-receive.md)                                | Riceve un esempio multimediale, lo elabora e recapita un esempio di output al filtro downstream. |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | Determina se il filtro deve eliminare un campione specificato.                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | Chiamato quando il filtro passa allo stato sospeso.                                           |
| Metodi pubblici                                                                  | Descrizione                                                                                    |
| [**CVideoTransformFilter**](cvideotransformfilter-cvideotransformfilter.md)    | Metodo del costruttore.                                                                            |
| [**EndFlush**](cvideotransformfilter-endflush.md)                              | Termina un'operazione di svuotamento.                                                                        |



 

 

 



