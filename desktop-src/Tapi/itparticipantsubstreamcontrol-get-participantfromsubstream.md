---
description: Il \_ metodo Get ParticipantFromSubStream consente a un'applicazione di individuare i partecipanti associati a un determinato flusso di dati.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Metodo ITParticipantSubStreamControl:: get_ParticipantFromSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330468"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a>Metodo ITParticipantSubStreamControl:: Get \_ ParticipantFromSubStream

\[**ottenere \_ ParticipantFromSubStream** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ ParticipantFromSubStream** consente a un'applicazione di individuare i partecipanti associati a un determinato flusso di dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pITSubStream* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> <dt>

*ppParticipant* \[ out\]
</dt> <dd>

Puntatore alla matrice di puntatori dell'interfaccia [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                     | Descrizione                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | Il metodo è riuscito.<br/>                                                       |
| <dl> <dt>**\_puntatore E**</dt> </dl>       | Il parametro *pITSubStream* o *ppParticipant* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | Il parametro *pITSubStream* non punta a un'interfaccia valida.<br/>         |
| <dl> <dt>**TAPI \_ E \_ noitems**</dt> </dl> | Nessun partecipante associato al sottoflusso.<br/>                |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>   | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

