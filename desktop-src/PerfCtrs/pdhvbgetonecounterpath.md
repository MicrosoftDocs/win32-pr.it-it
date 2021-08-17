---
description: La funzione PdhVbGetOneCounterPath visualizza una finestra di dialogo che consente all'utente di esplorare i contatori delle prestazioni disponibili e selezionare un contatore.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: Funzione PdhVbGetOneCounterPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: da6cc5b476373a55135d91d21163f15cb04379fff9d7c7c2cf1342451a5a201d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061159"
---
# <a name="pdhvbgetonecounterpath-function"></a>Funzione PdhVbGetOneCounterPath

La **funzione PdhVbGetOneCounterPath** visualizza una finestra di dialogo che consente all'utente di esplorare i contatori delle prestazioni disponibili e selezionare un contatore. Il contatore selezionato viene restituito nella *variabile PathString.* La *variabile PathString* deve essere dimensionata e inizializzata prima che venga chiamata questa funzione e le dimensioni ridimensionate devono essere indicate dalla *variabile PathLength.*

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. Microsoft consiglia invece di usare le funzioni descritte in [Funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbGetOneCounterPath( \_ ByVal PathString as String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString as String \_ ) As Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*PathString* 
</dt> <dd>

Variabile stringa inizializzata utilizzata per ricevere il percorso del contatore selezionato dall'utente.

</dd> <dt>

*PathLength* 
</dt> <dd>

Lunghezza dell'oggetto PathString inizializzato.

</dd> <dt>

*DetailLevel* 
</dt> <dd>

Tipi di contatori da visualizzare nella finestra di dialogo. Questo parametro può avere uno dei valori seguenti.



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

La funzione restituisce il numero di caratteri scritti nel buffer *PathString.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




