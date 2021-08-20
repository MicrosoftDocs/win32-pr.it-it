---
description: Si verifica quando viene aggiunto un nuovo stilo al sistema.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: Metodo ITabletEventSink::CursorNew
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 989c61d7f9ae4ce6b4f3136887d087605c61eff759bac7664a84388d2b509b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857140"
---
# <a name="itableteventsinkcursornew-method"></a>Metodo ITabletEventSink::CursorNew

Si verifica quando viene aggiunto un nuovo stilo al sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tcid* \[ Pollici\]
</dt> <dd>

Identificatore del contesto del tablet in cui è stato aggiunto il nuovo stilo.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificatore del nuovo oggetto stilo.

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
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




