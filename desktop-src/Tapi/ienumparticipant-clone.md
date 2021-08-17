---
description: Il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente. Questo metodo è nascosto dai linguaggi Visual Basic e di scripting.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: Metodo IEnumParticipant::Clone (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccd4bd29442daa01e632ae83510a87eebb06cb72beafc206b04d47c3dd761db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140494"
---
# <a name="ienumparticipantclone-method"></a>Metodo IEnumParticipant::Clone

\[**La** clonazione non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente. Questo metodo è nascosto dai linguaggi Visual Basic e di scripting.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ Cambio\]
</dt> <dd>

Puntatore alla [**nuova interfaccia IEnumParticipant.**](ienumparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro ppEnum* non è un puntatore valido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Operazione non riuscita per motivi sconosciuti.<br/>                          |



 

## <a name="remarks"></a>Commenti

TAPI chiama [**il metodo AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sull'interfaccia [**IEnumParticipant**](ienumparticipant.md) restituita da **IEnumParticipant::Clone.** L'applicazione deve [**chiamare Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) **sull'interfaccia IEnumParticipant** per liberare le risorse associate.

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

 

