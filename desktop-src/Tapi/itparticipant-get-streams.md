---
description: Il metodo \_ get Flussi crea una raccolta di flussi associati al partecipante corrente.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: Metodo ITParticipant::get_Streams (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b66447cd320110db45e1624d677c9b76e518f926da341805bd7de992d0e0eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003289"
---
# <a name="itparticipantget_streams-method"></a>Metodo ITParticipant::get \_ Flussi

\[**get \_ Flussi** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo \_ get Flussi** crea una raccolta di flussi associati al partecipante corrente. Questo metodo viene fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic. Le applicazioni C e C++ devono usare il [**metodo EnumerateStreams.**](itparticipant-enumeratestreams.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVariant* \[ Cambio\]
</dt> <dd>

Puntatore **a VARIANT** contenente un oggetto [**ITCollection di**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) [**puntatori a interfaccia ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pVariant* non è un puntatore valido.<br/>     |



 

## <a name="remarks"></a>Commenti

TAPI chiama **il metodo AddRef** sull'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) restituita da **ITParticipant::get \_ Flussi**. L'applicazione deve **chiamare Release** **sull'interfaccia ITStream** per liberare le risorse associate.

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

[**EnumerateStreams**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

