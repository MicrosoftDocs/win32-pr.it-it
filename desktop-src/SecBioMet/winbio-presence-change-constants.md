---
title: Costanti WINBIO_PRESENCE_CHANGE (tipi WinBio \_ . h)
description: Vengono descritti i tipi di modifiche che possono verificarsi quando il Windows Biometric Framework monitora la presenza di singoli utenti.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047964"
---
# <a name="winbio_presence_change-constants"></a>Costanti di modifica della \_ presenza WINBIO \_

Vengono descritti i tipi di modifiche che possono verificarsi quando il Windows Biometric Framework monitora la presenza di singoli utenti.



| Costante/valore                                                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**WINBIO \_ Tipo di modifica della presenza \_ \_ \_ sconosciuto**</dt> <dt>0</dt> </dl>           | Il tipo di evento è sconosciuto. Questo valore viene utilizzato per la struttura non inizializzata.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**WINBIO \_ Aggiornamento del tipo di modifica della presenza- \_ \_ \_ \_ tutti**</dt> <dt>1</dt> </dl> | Fornisce informazioni su tutti i visi correnti nel frame della fotocamera.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**WINBIO \_ \_Arrivo del \_ tipo \_ di modifica della presenza**</dt> <dt>2</dt> </dl>              | Un nuovo volto è entrato nel frame della fotocamera.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**WINBIO \_ Tipo di modifica della presenza \_ \_ \_ Riconosci**</dt> <dt>3</dt> </dl>     | Una faccia corrisponde a un utente registrato.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**WINBIO \_ Tipo di modifica della presenza- \_ \_ \_ parte**</dt> <dt>4</dt> </dl>              | Un viso rilevato in precedenza è stato fuori dal fotogramma della fotocamera per un certo periodo di tempo.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**WINBIO \_ Tipo di modifica della presenza \_ \_ \_ Track**</dt> <dt>5</dt> </dl>                 | Fornisce informazioni sugli aggiornamenti sul riquadro e rifiuta i valori di dettaglio per un subset delle facce attualmente presenti nel frame della fotocamera.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



 

 





