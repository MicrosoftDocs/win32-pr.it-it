---
description: Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore tablet.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: Metodo ITabletEventSink::CursorUp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 586f18750e832bad653a3df92d14efb41b39547ee532913ac52c986a9b5e137c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712131"
---
# <a name="itableteventsinkcursorup-method"></a>Metodo ITabletEventSink::CursorUp

Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tcid* \[ Pollici\]
</dt> <dd>

Identificatore della tablet.

</dd> <dt>

*cid* \[ in\]
</dt> <dd>

Identificatore dello stilo.

</dd> <dt>

*nSerialNumber* \[ Pollici\]
</dt> <dd>

Numero di serie dello stilo.

</dd> <dt>

*cbPkt* \[ Pollici\]
</dt> <dd>

Numero di byte in un pacchetto di dati dello stilo.

</dd> <dt>

*pbPkt* \[ Pollici\]
</dt> <dd>

Dati dello stilo che indicano la posizione in cui lo stilo è stato elevato dal tablet.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

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

 

 




