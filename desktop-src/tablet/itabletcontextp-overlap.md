---
description: Sposta un contesto del tablet nella parte anteriore o posteriore della coda di input.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'Metodo ITabletContextP:: sovrapposizione'
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
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316824"
---
# <a name="itabletcontextpoverlap-method"></a>Metodo ITabletContextP:: sovrapposizione

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

*bTop* \[ in\]
</dt> <dd>

Indica se il contesto del tablet deve essere spostato nella parte superiore o inferiore della coda di input.

</dd> <dt>

*pdwtcid* \[ out\]
</dt> <dd>

Identificatore di contesto della tavoletta.

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

[**Interfaccia ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




