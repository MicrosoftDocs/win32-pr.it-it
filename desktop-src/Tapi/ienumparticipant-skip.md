---
description: Il metodo Skip ignora il successivo numero specificato di elementi nella sequenza di enumerazione. Questo metodo è nascosto ai linguaggi Visual Basic e di scripting.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: Metodo IEnumParticipant::Skip (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a55eb3298578738bb427efd6ab2b830b9a7850668aa3c9fa4712cc1bf48d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660701"
---
# <a name="ienumparticipantskip-method"></a>Metodo IEnumParticipant::Skip

\[**Skip** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Skip** ignora il successivo numero specificato di elementi nella sequenza di enumerazione. Questo metodo è nascosto ai linguaggi Visual Basic e di scripting.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Numero di elementi da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il numero di elementi ignorati è *celt*.<br/>               |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Number of elements skipped was not *celt*.<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




