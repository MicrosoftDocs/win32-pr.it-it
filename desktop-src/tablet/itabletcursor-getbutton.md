---
description: Recupera l'oggetto pulsante specificato da uno stilo tablet.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: Metodo ITabletCursor::GetButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 49306160a0c14badc23cb2f359400d0fb2947012078a9318315a6697050f48dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938631"
---
# <a name="itabletcursorgetbutton-method"></a>Metodo ITabletCursor::GetButton

Recupera l'oggetto pulsante specificato da uno stilo tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iButton* \[ Pollici\]
</dt> <dd>

Identificatore del pulsante da recuperare.

</dd> <dt>

*ppButton* \[ Cambio\]
</dt> <dd>

Oggetto pulsante specificato dal *parametro iButton.*

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

[**Interfaccia ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




