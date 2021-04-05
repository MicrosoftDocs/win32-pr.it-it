---
description: Si verifica quando la punta dello stilo contatta la superficie del Tablet di digitalizzazione.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'Metodo ITabletEventSink:: CursorDown'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757055"
---
# <a name="itableteventsinkcursordown-method"></a>Metodo ITabletEventSink:: CursorDown

Si verifica quando la punta dello stilo contatta la superficie del Tablet di digitalizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
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

*nSerialNumber* \[ in\]
</dt> <dd>

Numero di serie dello stilo.

</dd> <dt>

*cbPkt* \[ in\]
</dt> <dd>

Numero di byte in un pacchetto di dati Stilo.

</dd> <dt>

*pbPkt* \[ in\]
</dt> <dd>

Dati dello stilo che indicano la posizione in cui lo stilo ha toccato il tablet.

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

 

 




