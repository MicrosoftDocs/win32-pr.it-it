---
description: Il metodo EnumerateStreams enumera i flussi attualmente presenti nei partecipanti. Questo metodo viene fornito per le applicazioni C e C++. Le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic, devono usare il \_ metodo Get Streams.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'Metodo ITParticipant:: EnumerateStreams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330258"
---
# <a name="itparticipantenumeratestreams-method"></a>Metodo ITParticipant:: EnumerateStreams

\[**EnumerateStreams** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **EnumerateStreams** enumera i flussi attualmente presenti nei partecipanti. Questo metodo viene fornito per le applicazioni C e C++. Le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic, devono usare il metodo [**get \_ Streams**](itparticipant-get-streams.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnumStream* \[ out\]
</dt> <dd>

Puntatore al puntatore all'interfaccia [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                     | Significato                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Il parametro *ppEnumStream* non è un puntatore valido.<br/> |



 

## <a name="remarks"></a>Commenti

TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) restituita da **ITParticipant:: EnumerateStreams**. L'applicazione deve chiamare **Release** sull'interfaccia **IEnumStream** per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ottenere i \_ flussi**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




