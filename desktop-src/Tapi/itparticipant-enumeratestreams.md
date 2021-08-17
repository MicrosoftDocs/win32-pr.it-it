---
description: Il metodo EnumerateStreams enumera i flussi attualmente con i partecipanti. Questo metodo viene fornito per le applicazioni C e C++. Le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic, devono usare il metodo get \_ Flussi.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: Metodo ITParticipant::EnumerateStreams (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ec901c81bb0df666877ee06462b88da965b41bedd961e71cebbf25cd78ee30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140304"
---
# <a name="itparticipantenumeratestreams-method"></a>Metodo ITParticipant::EnumerateStreams

\[**EnumerateStreams** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo EnumerateStreams** enumera i flussi attualmente con i partecipanti. Questo metodo viene fornito per le applicazioni C e C++. Le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic, devono usare il [**metodo get \_ Flussi.**](itparticipant-get-streams.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnumStream* \[ Cambio\]
</dt> <dd>

Puntatore al [**puntatore a interfaccia IEnumStream.**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                     | Significato                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Il *parametro ppEnumStream* non è un puntatore valido.<br/> |



 

## <a name="remarks"></a>Commenti

TAPI chiama **il metodo AddRef** sull'interfaccia [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) restituita da **ITParticipant::EnumerateStreams.** L'applicazione deve **chiamare Release** **sull'interfaccia IEnumStream** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**Get \_ Flussi**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




