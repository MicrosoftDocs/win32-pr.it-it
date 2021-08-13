---
description: Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto tablet, ad esempio mouse, penna o tocco.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: Metodo ITablet2::GetDeviceKind
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e1db540b1097428e20104d95a8a7a6726566c7cd8939a11ec4041c1aa9475afd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450528"
---
# <a name="itablet2getdevicekind-method"></a>Metodo ITablet2::GetDeviceKind

Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto tablet, ad esempio mouse, penna o tocco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pKind* \[ Cambio\]
</dt> <dd>

Valore di enumerazione che indica il tipo di tablet, ad esempio mouse, penna o tocco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia e questo metodo sono stati introdotti in Windows Vista.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet2**](itablet2.md)
</dt> <dt>

[**Enumerazione TABLET \_ DEVICE \_ KIND**](tablet-device-kind.md)
</dt> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> </dl>

 

 




