---
description: Il \_ sottoflusso get ottiene un puntatore a una matrice di interfacce ITSubStream che rappresentano i flussi sottoflussi necessari nell'evento.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Metodo ITParticipantEvent:: get_SubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328730"
---
# <a name="itparticipanteventget_substream-method"></a>Metodo ITParticipantEvent:: Get \_ substream

\[**ottenere \_ Il sottoflusso** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il **\_ sottoflusso Get** ottiene un puntatore a una matrice di interfacce [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) che rappresentano i flussi sottoflussi necessari nell'evento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSubStream* \[ out\]
</dt> <dd>

Puntatore alla matrice di puntatori [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                           | Significato                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**TAPI \_ E \_ noitems**</dt> </dl> | All'evento non è associato alcun flusso.<br/>   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>   | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>       | Il parametro *ppSubStream* non è un puntatore valido.<br/>  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

