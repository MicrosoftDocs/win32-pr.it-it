---
description: Il metodo Delete Elimina il supporto corrispondente all'indice specificato.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: Metodo ITMediaCollection::D Elimina (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329735"
---
# <a name="itmediacollectiondelete-method"></a>ITMediaCollection::D Metodo Elimina

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **Delete** Elimina il supporto corrispondente all'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice del supporto da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                                                              | Descrizione                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                     | Il metodo è riuscito.<br/>                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                             | Il valore del parametro *index* è minore di 1 o maggiore del numero corrente di elementi.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>                                            | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>                                          |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                                                   | Errore interno (dovrebbe verificarsi solo se una chiamata precedente ha restituito un errore).<br/>                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                                | Questo metodo non è ancora implementato.<br/>                                                           |
| <dl> <dt>**HRESULT \_ dal \_ codice di errore \_ ( \_ BLOB SDPBLB conf \_ \_ distrutto)**</dt> </dl> | Il BLOB SDP non esiste.<br/>                                                                   |



 

## <a name="remarks"></a>Commenti

La maggior parte degli elenchi C e C++ sono basati su 0, ma questo indice è basato su 1 per la compatibilità con Visual Basic, ovvero il primo elemento ha un numero di indice pari a 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




