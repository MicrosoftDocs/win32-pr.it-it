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
ms.openlocfilehash: a1e1a1b717aeb2814b469fc34a9e038052abb6720dde0ed75982f27716978de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907007"
---
# <a name="cvideotransformfilter-class"></a>Classe CVideoTransformFilter

![Gerarchia di classi cvideotransformfilter](images/vtsip01.png)

La `CVideoTransformFilter` classe è progettata principalmente come classe di base per i filtri di decompressione AVI. Questa classe aggiunge il supporto per il controllo qualità alla [**classe CTransformFilter.**](ctransformfilter.md) Il metodo **Receive** del filtro può decidere di eliminare i frame in base ai messaggi di qualità del renderer e alle misurazioni delle prestazioni raccolte dal filtro durante lo streaming.

Se il filtro elimina un frame, continua a rilasciare i fotogrammi fino a raggiungere il fotogramma chiave successivo. Per i flussi MPEG, il filtro non distingue tra i frame B e I frame P.



| Variabili membro protette                                                      | Descrizione                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ bQualityChanged**](cvideotransformfilter-m-bqualitychanged.md)           | Indica se il filtro ha eliminato frame.                                               |
| [**m \_ bSkipping**](cvideotransformfilter-m-bskipping.md)                       | Indica se il filtro sta rilasciando frame.                                     |
| [**m \_ itrAvgDecode**](cvideotransformfilter-m-itravgdecode.md)                 | Tempo medio impiegato per decodificare un frame.                                         |
| [**m \_ itrLate**](cvideotransformfilter-m-itrlate.md)                           | Indica la fine degli esempi in arrivo nel renderer.                                   |
| [**m \_ nFramesSinceKeyFrame**](cvideotransformfilter-m-nframessincekeyframe.md) | Numero di fotogrammi ricevuti dal filtro dall'ultimo fotogramma chiave.                    |
| [**m \_ nKeyFramePeriod**](cvideotransformfilter-m-nkeyframeperiod.md)           | Intervallo massimo osservato tra fotogrammi chiave.                                              |
| [**m \_ nWaitForKey**](cvideotransformfilter-m-nwaitforkey.md)                   | Numero massimo corrente di fotogrammi differenziali da eliminare.                                            |
| [**m \_ tDecodeStart**](cvideotransformfilter-m-tdecodestart.md)                 | Tempo impiegato per decodificare l'esempio più recente.                                  |
| Metodi protetti                                                               | Descrizione                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | Usato per segnalare un errore di streaming.                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | Notifica al filtro che è richiesta una modifica della qualità.                                        |
| [**Ricevere**](cvideotransformfilter-receive.md)                                | Riceve un campione di supporti, lo elabora e recapita un esempio di output al filtro downstream. |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | Determina se il filtro deve eliminare un campione specificato.                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | Chiamato quando il filtro passa allo stato sospeso.                                           |
| Metodi pubblici                                                                  | Descrizione                                                                                    |
| [**CVideoTransformFilter**](cvideotransformfilter-cvideotransformfilter.md)    | Metodo del costruttore.                                                                            |
| [**EndFlush**](cvideotransformfilter-endflush.md)                              | Termina un'operazione di scaricamento.                                                                        |



 

 

 



