---
description: Si verifica quando un contesto del Tablet viene eliminato definitivamente.
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: 'Metodo ITabletEventSink:: ContextDestroy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c9b5d78d4ce4032c1a7a2082fb749afc5a39949a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530031"
---
# <a name="itableteventsinkcontextdestroy-method"></a>Metodo ITabletEventSink:: ContextDestroy

Si verifica quando un contesto del Tablet viene eliminato definitivamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TCID* \[ in\]
</dt> <dd>

Identificatore del contesto del tablet da eliminare definitivamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

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

 

 




