---
description: Il \_ metodo Put status imposta lo stato di un partecipante.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: 'ITParticipant: metodo:p ut_Status (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327988"
---
# <a name="itparticipantput_status-method"></a>ITParticipant: metodo di \_ stato ut:p

\[**Inserisci \_ Lo stato** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **put \_ status** imposta lo stato di un partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pITStream* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> <dt>

*fEnable* \[ in\]
</dt> <dd>

VARIANT \_ true se il partecipante è abilitato nel flusso, VARIANT \_ false se deve essere disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Metodo non implementato.<br/>                                        |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pITStream* non è un puntatore valido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pITStream* non punta a un'interfaccia valida.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>           |



 

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

[**ottenere \_ lo stato**](itparticipant-get-status.md)
</dt> </dl>

 

