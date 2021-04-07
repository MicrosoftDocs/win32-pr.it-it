---
description: La funzione PdhVbGetOneCounterPath Visualizza una finestra di dialogo che consente all'utente di visualizzare i contatori delle prestazioni disponibili e di selezionare un contatore.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath (funzione)
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
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881757"
---
# <a name="pdhvbgetonecounterpath-function"></a>PdhVbGetOneCounterPath (funzione)

La funzione **PdhVbGetOneCounterPath** Visualizza una finestra di dialogo che consente all'utente di visualizzare i contatori delle prestazioni disponibili e di selezionare un contatore. Il contatore selezionato viene restituito nella variabile *PathString* . La variabile *PathString* deve essere dimensionata e inizializzata prima che questa funzione venga chiamata e la dimensione dimensione deve essere indicata dalla variabile *PathLength* .

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbGetOneCounterPath ( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel Long, \_ ByVal CaptionString As String \_ ) Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*PathString* 
</dt> <dd>

Variabile di stringa inizializzata utilizzata per ricevere il percorso del contatore selezionato dall'utente.

</dd> <dt>

*PathLength* 
</dt> <dd>

Lunghezza del PathString inizializzato.

</dd> <dt>

*DetailLevel* 
</dt> <dd>

Tipi di contatori da visualizzare nella finestra di dialogo. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                               | Significato                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**\_dettaglio prestazioni \_ avanzato**</dt> </dl> | Contatori che l'utente avanzato è in grado di comprendere, oltre ai contatori degli utenti meno esperti.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**\_esperto Dettagli \_ prestazioni**</dt> </dl>       | Contatori che l'utente esperto e lo sviluppatore di software possono conoscere, oltre ai contatori per gli utenti principianti e avanzati.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**dettaglio prestazioni- \_ \_ novizio**</dt> </dl>       | Solo i contatori che è probabile che l'utente del novizio possa comprendere.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**\_ \_ procedura guidata Dettagli prestazioni**</dt> </dl>       | Tutti i contatori nel sistema.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Variabile di stringa che contiene il testo che verrà visualizzato nella barra del titolo della finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il numero di caratteri scritti nel buffer *PathString* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




