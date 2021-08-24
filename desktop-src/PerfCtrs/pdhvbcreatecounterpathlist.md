---
description: La funzione PdhVbCreateCounterPathList visualizza la finestra di dialogo di esplorazione dei contatori delle prestazioni, che consente all'utente di selezionare diversi contatori delle prestazioni. Ogni percorso del contatore selezionato deve quindi essere letto usando la funzione PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: Funzione PdhVbCreateCounterPathList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 6471fe3baee14fa1853810b66a804974b05ca84d0db9bc4e7dd805085ad5c0c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775551"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>Funzione PdhVbCreateCounterPathList

La **funzione PdhVbCreateCounterPathList** visualizza la finestra di dialogo di esplorazione dei contatori delle prestazioni, che consente all'utente di selezionare diversi contatori delle prestazioni. Ogni percorso del contatore selezionato deve quindi essere letto usando la [**funzione PdhVbGetCounterPathFromList.**](pdhvbgetcounterpathfromlist.md)

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. Microsoft consiglia invece di usare le funzioni descritte in [Funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbCreateCounterPathList( \_ ByVal DetailLevel As Long, \_ ByVal CaptionString as String \_ ) As Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*DetailLevel* 
</dt> <dd>

Tipi di contatori da visualizzare nella finestra di dialogo. Usare uno dei valori seguenti.



| Valore                                                                                                                                                                               | Significato                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**PERF \_ DETAIL \_ ADVANCED**</dt> </dl> | Contatori che è probabile che l'utente avanzato comprendi, oltre ai contatori per utenti principianti.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**ESPERTO DEI DETTAGLI DI PERF \_ \_**</dt> </dl>       | Contatori che l'utente esperto e lo sviluppatore di software probabilmente comprenderanno, oltre ai contatori per gli utenti principianti e avanzati.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**NOVIZIO DETTAGLI \_ \_ PERF**</dt> </dl>       | Solo i contatori che l'utente alle prime informazioni è probabilmente in grado di comprendere.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**PROCEDURA GUIDATA DETTAGLI \_ PERF \_**</dt> </dl>       | Tutti i contatori nel sistema.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Variabile stringa che contiene il testo che verrà visualizzato nella barra della didascalia della finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il numero di percorsi dei contatori selezionati dall'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




