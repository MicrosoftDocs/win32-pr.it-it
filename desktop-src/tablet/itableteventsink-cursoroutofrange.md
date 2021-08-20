---
description: Si verifica quando lo stilo esce dall'intervallo di rilevamento fisico (prossimità) del tablet.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: Metodo ITabletEventSink::CursorOutOfRange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 215ab448d573f83222d04547c4dccbeb88d7fe7c4358b3cca0ed09e936e286d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041673"
---
# <a name="itableteventsinkcursoroutofrange-method"></a>Metodo ITabletEventSink::CursorOutOfRange

Si verifica quando lo stilo esce dall'intervallo di rilevamento fisico (prossimità) del tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tcid* \[ Pollici\]
</dt> <dd>

Identificatore del tablet.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificatore dello stilo.

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

 

 




