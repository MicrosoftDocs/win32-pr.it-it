---
description: Si verifica quando è disponibile un evento di sistema.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'Metodo ITabletEventSink:: SystemEvent'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314912"
---
# <a name="itableteventsinksystemevent-method"></a>Metodo ITabletEventSink:: SystemEvent

Si verifica quando è disponibile un evento di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TCID* \[ in\]
</dt> <dd>

Identificatore del tablet.

</dd> <dt>

*CID* \[ in\]
</dt> <dd>

Identificatore dello stilo.

</dd> <dt>

*evento* \[ in\]
</dt> <dd>

Codice dell'evento di sistema.

</dd> <dt>

*EventData* \[ in\]
</dt> <dd>

Dati dell'evento di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Nell'elenco seguente sono riportati i valori validi per il parametro dell'evento.

-   \_tocco se
-   SE \_ \_ tocco doppia
-   SE \_ \_ tocco destro
-   \_trascina se
-   trascina SE a \_ destra \_
-   SE è in \_ attesa di \_ INVIO
-   \_Mantieni \_ uscita
-   SE al \_ passaggio del mouse \_ immettere
-   SE il \_ passaggio del mouse viene \_ lasciato
-   SE al \_ centro \_ fare clic
-   \_chiave se
-   \_tasto di modifica se \_
-   \_modalità movimento \_ se
-   \_cursore se

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




