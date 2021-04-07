---
description: La funzione PdhVbCreateCounterPathList Visualizza la finestra di dialogo esplorazione dei contatori delle prestazioni, che consente all'utente di selezionare diversi contatori delle prestazioni. Ogni percorso del contatore selezionato deve quindi essere letto utilizzando la funzione PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList (funzione)
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
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881761"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>PdhVbCreateCounterPathList (funzione)

La funzione **PdhVbCreateCounterPathList** Visualizza la finestra di dialogo esplorazione dei contatori delle prestazioni, che consente all'utente di selezionare diversi contatori delle prestazioni. Ogni percorso del contatore selezionato deve quindi essere letto utilizzando la funzione [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) .

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbCreateCounterPathList ( \_ ByVal DetailLevel Long, \_ ByVal CaptionString As String \_ ) Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*DetailLevel* 
</dt> <dd>

Tipi di contatori da visualizzare nella finestra di dialogo. Usare uno dei valori seguenti.



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

La funzione restituisce il numero di percorsi del contatore selezionati dall'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




