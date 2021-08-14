---
description: Restituisce una stringa contenente il nome del dispositivo tablet.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: Metodo ITablet::GetName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 089bebc48fce9c720933f829ab83d04bf24fac3d8e2678369865cf2fe58650f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350680"
---
# <a name="itabletgetname-method"></a>Metodo ITablet::GetName

Restituisce una stringa contenente il nome del dispositivo tablet.

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

Puntatore a una stringa contenente il nome del dispositivo tablet.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> </dl>

 

