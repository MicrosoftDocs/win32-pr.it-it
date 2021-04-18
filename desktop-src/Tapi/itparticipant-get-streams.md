---
description: Il \_ metodo Get Streams crea una raccolta di flussi associati al partecipante corrente.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Metodo ITParticipant:: get_Streams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327991"
---
# <a name="itparticipantget_streams-method"></a>Metodo ITParticipant:: Get \_ Streams

\[**ottenere \_ I flussi** non sono disponibili per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ Streams** crea una raccolta di flussi associati al partecipante corrente. Questo metodo viene fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic. Le applicazioni C e C++ devono usare il metodo [**EnumerateStreams**](itparticipant-enumeratestreams.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVariant* \[ out\]
</dt> <dd>

Puntatore a **Variant** contenente un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) di puntatori dell'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pVariant* non è un puntatore valido.<br/>     |



 

## <a name="remarks"></a>Commenti

TAPI chiama il metodo **AddRef** sull'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) restituita dai **\_ flussi ITParticipant:: Get**. L'applicazione deve chiamare **Release** sull'interfaccia **ITStream** per liberare risorse associate.

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

[**EnumerateStreams**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

