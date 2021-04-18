---
description: Il \_ metodo Get Status restituisce un \_ bool Variant che indica lo stato del partecipante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Metodo ITParticipant:: get_Status (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327992"
---
# <a name="itparticipantget_status-method"></a>Metodo ITParticipant:: Get \_ status

\[**ottenere \_ Lo stato** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ status** restituisce un \_ bool Variant che indica lo stato del partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pITStream* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> <dt>

*pStatus* \[ out\]
</dt> <dd>

VARIANT \_ true se il partecipante è abilitato nel flusso, VARIANT \_ false se è disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Metodo non implementato.<br/>                                        |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>           |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pITStream* non è un puntatore valido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pITStream* non punta a un'interfaccia valida.<br/> |



 

## <a name="remarks"></a>Commenti

L'abilitazione o la disabilitazione dello stato di un partecipante in un flusso consente a un'applicazione di disattivare essenzialmente un determinato partecipante.

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

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**Inserisci \_ stato**](itparticipant-put-status.md)
</dt> </dl>

 

