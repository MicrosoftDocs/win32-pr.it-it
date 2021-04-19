---
description: Il \_ metodo Get mediacollection ottiene un puntatore all'interfaccia ITMediaCollection per la conferenza.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Metodo ITSdp:: get_MediaCollection (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326487"
---
# <a name="itsdpget_mediacollection-method"></a>Metodo ITSdp:: Get \_ mediacollection

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ mediacollection** ottiene un puntatore all'interfaccia [**ITMediaCollection**](itmediacollection.md) per la conferenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppMediaCollection* \[ out\]
</dt> <dd>

Puntatore a [**ITMediaCollection**](itmediacollection.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                                                           | Significato                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                            | Il metodo è riuscito.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | Il parametro *ppMediaCollection* non è un puntatore valido.<br/>                        |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>                                   | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>                             |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                                          | Errore non specificato.<br/>                                                               |
| <dl> <dt>**HRESULT \_ dal \_ codice di errore \_ (errore di \_ dati non validi \_ )**</dt> </dl> | Si è verificato un errore interno, in genere a causa dell'errore di un metodo precedente.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Questo metodo non è ancora implementato.<br/>                                              |



 

## <a name="remarks"></a>Commenti

È possibile ottenere un puntatore [**ITMediaCollection**](itmediacollection.md) anche usando **QueryInterface**.

TAPI chiama il metodo **AddRef** sull'interfaccia [**ITMediaCollection**](itmediacollection.md) restituita da **ITSdp:: Get \_ mediacollection**. L'applicazione deve chiamare **Release** sull'interfaccia **ITMediaCollection** per liberare risorse associate.

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

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




