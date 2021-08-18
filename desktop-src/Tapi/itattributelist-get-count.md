---
description: Il metodo get \_ Count ottiene il numero di attributi.
ms.assetid: dc607f09-4cca-4ef0-8b86-dbc5e6edcfdd
title: Metodo ITAttributeList::get_Count (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83033546b75e7dda9da26fa910404e2739f40d651e0be79338b49fb5c98b9415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762447"
---
# <a name="itattributelistget_count-method"></a>Metodo ITAttributeList::get \_ Count

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ Count** ottiene il numero di attributi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ Cambio\]
</dt> <dd>

Conteggio degli attributi nell'elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pVal* non è un puntatore valido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITAttributeList**](itattributelist.md)
</dt> </dl>

 

 




