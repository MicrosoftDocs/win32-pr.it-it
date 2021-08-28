---
description: Il metodo get \_ EnumerationIf ottiene un puntatore a un'interfaccia di enumerazione dei supporti.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: Metodo ITMediaCollection::get_EnumerationIf (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe14475e216b5143b599aab50d12d1d0c548b5f64dd8e44edd2e6aab249905c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060859"
---
# <a name="itmediacollectionget_enumerationif-method"></a>Metodo ITMediaCollection::get \_ EnumerationIf

\[Le interfacce e i controlli di conferenza di telefonia IP di Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ EnumerationIf** ottiene un puntatore a un'interfaccia di enumerazione dei supporti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ Cambio\]
</dt> <dd>

Puntatore [**all'interfaccia IEnumMedia**](ienummedia.md) per l'elemento desiderato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pVal* non è un puntatore valido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Questo metodo è intercambiabile con [**get \_ \_ NewEnum,**](itmediacollection-get--newenum.md) ad eccezione del fatto che restituisce [**IEnumMedia**](ienummedia.md) anziché **IUnknown.**

TAPI chiama il **metodo AddRef** sull'interfaccia [**IEnumMedia**](ienummedia.md) restituita da **ITMediaCollection::get \_ Enumerationlf**. L'applicazione deve **chiamare Release** **sull'interfaccia IEnumMedia** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




