---
description: Si verifica quando uno stilo rientra nell'intervallo di rilevamento del digitalizzatore.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: Metodo ITabletEventSink::CursorInRange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2c9878b4c3cd28727c5d54e59a52f3fe85a44832203f70b6ff042c6beeb579dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883481"
---
# <a name="itableteventsinkcursorinrange-method"></a>Metodo ITabletEventSink::CursorInRange

Si verifica quando uno stilo rientra nell'intervallo di rilevamento del digitalizzatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tcid* \[ Pollici\]
</dt> <dd>

Identificatore dell'oggetto tablet che ha rilevato lo stilo.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificatore dell'oggetto stilo compreso nell'intervallo del digitalizzatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




