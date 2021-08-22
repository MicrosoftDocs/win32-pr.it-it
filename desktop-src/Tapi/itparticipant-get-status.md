---
description: Il metodo get \_ Status restituisce un valore VARIANT \_ BOOL che indica lo stato del partecipante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: Metodo ITParticipant::get_Status (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1585c9605447e7b515885ecf9e30d060afb7a57d14c5b29a66025f2df9da05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060849"
---
# <a name="itparticipantget_status-method"></a>Metodo ITParticipant::get \_ Status

\[**get \_ Lo** stato non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ Status** restituisce un valore VARIANT \_ BOOL che indica lo stato del partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pITStream* \[ Pollici\]
</dt> <dd>

Puntatore [**all'interfaccia ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)

</dd> <dt>

*pStatus* \[ Cambio\]
</dt> <dd>

VARIANT \_ TRUE se il partecipante è abilitato nel flusso, VARIANT FALSE se è \_ disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Metodo non implementato.<br/>                                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>           |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pITStream* non è un puntatore valido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pITStream* non punta a un'interfaccia valida.<br/> |



 

## <a name="remarks"></a>Commenti

L'abilitazione o la disabilitazione dello stato di un partecipante in un flusso consente essenzialmente a un'applicazione di disattivare l'audio di un determinato partecipante.

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

[**Put \_ Status**](itparticipant-put-status.md)
</dt> </dl>

 

