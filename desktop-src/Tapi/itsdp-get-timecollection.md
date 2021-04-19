---
description: Il \_ metodo Get TimeCollection ottiene un puntatore a un'interfaccia ITTimeCollection per Conference.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'Metodo ITSdp:: get_TimeCollection (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330365"
---
# <a name="itsdpget_timecollection-method"></a>Metodo ITSdp:: Get \_ TimeCollection

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ TimeCollection** ottiene un puntatore a un'interfaccia [**ITTimeCollection**](ittimecollection.md) per Conference.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppTimeCollection* \[ out\]
</dt> <dd>

Puntatore a [**ITTimeCollection**](ittimecollection.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                                                           | Significato                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                            | Il metodo è riuscito.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | Il parametro *ppTimeCollection* non è un puntatore valido.<br/>                         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>                                   | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>                             |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                                          | Errore non specificato.<br/>                                                               |
| <dl> <dt>**HRESULT \_ dal \_ codice di errore \_ (errore di \_ dati non validi \_ )**</dt> </dl> | Si è verificato un errore interno, in genere a causa dell'errore di un metodo precedente.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Questo metodo non è ancora implementato.<br/>                                              |



 

## <a name="remarks"></a>Commenti

È possibile ottenere un puntatore [**ITTimeCollection**](ittimecollection.md) anche usando **QueryInterface**.

TAPI chiama il metodo **AddRef** sull'interfaccia [**ITTimeCollection**](ittimecollection.md) restituita da **ITSdp:: Get \_ TimeCollection**. L'applicazione deve chiamare **Release** sull'interfaccia **ITTimeCollection** per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> </dl>

 

 




