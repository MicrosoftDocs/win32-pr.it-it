---
description: Il metodo get \_ EnumerationIf restituisce l'interfaccia di enumerazione IEnumTime che enumera ITTime.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: Metodo ITTimeCollection::get_EnumerationIf (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb6afa99d1170180d0174bfd9b4d3f92f3733b1bee716ddd1e80b957e0c9bf33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905907"
---
# <a name="ittimecollectionget_enumerationif-method"></a>Metodo ITTimeCollection::get \_ EnumerationIf

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo get \_ EnumerationIf** restituisce [**l'interfaccia di enumerazione IEnumTime**](ienumtime.md) che enumera [**ITTime.**](ittime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ Cambio\]
</dt> <dd>

Puntatore [**all'interfaccia IEnumTime.**](ienumtime.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro pVal* non è un puntatore valido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Questo metodo è intercambiabile con [**get \_ \_ NewEnum**](ittimecollection-get--newenum.md) ad eccezione del fatto che restituisce [**IEnumTime**](ienumtime.md) anziché **IUnknown**.

TAPI chiama il **metodo AddRef** [**sull'interfaccia IEnumTime**](ienumtime.md) restituita da **ITTimeCollection::get \_ EnumerationIf**. L'applicazione deve **chiamare Release** [**sull'interfaccia IEnumTime**](ienumtime.md) per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




