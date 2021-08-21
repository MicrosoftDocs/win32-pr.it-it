---
description: Il metodo get \_ Item ottiene un puntatore ITMedia corrispondente all'indice specificato.
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: Metodo ITMediaCollection::get_Item (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c74201e5c1c886c6c024deb9d133072d962ca25e16dcba26fdd35972e0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774871"
---
# <a name="itmediacollectionget_item-method"></a>Metodo ITMediaCollection::get \_ Item

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ Item** ottiene un [**puntatore ITMedia**](itmedia.md) corrispondente all'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Indice dell'elemento multimediale da ottenere.

</dd> <dt>

*pVal* \[ Cambio\]
</dt> <dd>

Puntatore [**all'interfaccia ITMedia**](itmedia.md) per l'elemento desiderato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pVal* non è un puntatore valido.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro Index* non è valido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

La maggior parte degli elenchi C e C++ è in base 0, ma questo indice è in base 1 per la compatibilità Visual Basic, ovvero il primo elemento ha un numero di indice 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




