---
description: Recupera il nome del pulsante dello stilo.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: 'Metodo ITabletCursorButton:: GetName'
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
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313455"
---
# <a name="itabletcursorbuttongetname-method"></a>Metodo ITabletCursorButton:: GetName

Recupera il nome del pulsante dello stilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppwszName* \[ out\]
</dt> <dd>

Nome del pulsante dello stilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

