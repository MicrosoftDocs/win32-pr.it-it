---
description: Il metodo put \_ Status imposta lo stato di un partecipante.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: Metodo ITParticipant::p ut_Status (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3552f66dea5a089ff19a0f108a21db5c3301670f246411c0a91fdda3ade8fbe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864885"
---
# <a name="itparticipantput_status-method"></a>Metodo ITParticipant::p ut \_ Status

\[**put \_ Lo** stato non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo put \_ Status** imposta lo stato di un partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pITStream* \[ Pollici\]
</dt> <dd>

Puntatore [**all'interfaccia ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)

</dd> <dt>

*fEnable* \[ Pollici\]
</dt> <dd>

VARIANT \_ TRUE se il partecipante è abilitato nel flusso, VARIANT FALSE se deve essere \_ disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Metodo non implementato.<br/>                                        |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro pITStream* non è un puntatore valido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pITStream* non punta a un'interfaccia valida.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>           |



 

## <a name="remarks"></a>Commenti

L'abilitazione o la disabilitazione dello stato di un partecipante in un flusso consente a un'applicazione di disattivare essenzialmente l'audio di un determinato partecipante.

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

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**ottenere \_ lo stato**](itparticipant-get-status.md)
</dt> </dl>

 

