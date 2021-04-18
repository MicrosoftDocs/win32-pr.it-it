---
description: Recupera l'oggetto pulsante specificato da uno stilo del tablet.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'Metodo ITabletCursor:: GetButton'
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
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314913"
---
# <a name="itabletcursorgetbutton-method"></a>Metodo ITabletCursor:: GetButton

Recupera l'oggetto pulsante specificato da uno stilo del tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IButton* \[ in\]
</dt> <dd>

Identificatore del pulsante da recuperare.

</dd> <dt>

*ppButton* \[ out\]
</dt> <dd>

Oggetto Button specificato dal parametro *IButton* .

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

[**Interfaccia ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




