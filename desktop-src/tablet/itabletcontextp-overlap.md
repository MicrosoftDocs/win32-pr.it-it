---
description: Sposta un contesto del tablet nella parte anteriore o posteriore della coda di input.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: Metodo ITabletContextP::Overlap
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: ec8b462f2d06e1613c32b795af1793776cafddd6a3531ac6a0b5385f3d3e5128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712241"
---
# <a name="itabletcontextpoverlap-method"></a>Metodo ITabletContextP::Overlap

Sposta un contesto del tablet nella parte anteriore o posteriore della coda di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bTop* \[ Pollici\]
</dt> <dd>

Indica se il contesto del tablet deve essere spostato nella parte superiore o inferiore della coda di input.

</dd> <dt>

*pdwtcid* \[ Cambio\]
</dt> <dd>

Identificatore del contesto del tablet.

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
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




