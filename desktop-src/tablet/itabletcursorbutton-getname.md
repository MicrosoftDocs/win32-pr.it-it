---
description: Recupera il nome del pulsante dello stilo.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: Metodo ITabletCursorButton::GetName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 41155aa15a2efaeb789387ae3ea7c6863ab0010884ecacb2f7bd3a75453e57b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716821"
---
# <a name="itabletcursorbuttongetname-method"></a>Metodo ITabletCursorButton::GetName

Recupera il nome del pulsante dello stilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppwszName* \[ Cambio\]
</dt> <dd>

Nome del pulsante dello stilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

