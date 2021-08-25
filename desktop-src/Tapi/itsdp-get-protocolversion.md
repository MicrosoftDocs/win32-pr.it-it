---
description: Il metodo get ProtocolVersion ottiene la versione del protocollo \_ SDP (Session Descriptor Protocol; vedere rfc 2327).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: Metodo ITSdp::get_ProtocolVersion (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54bd664a2a1147b341d46a83c4a2fa72c66585a11fc8eaef154aa213cab8945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774491"
---
# <a name="itsdpget_protocolversion-method"></a>Metodo ITSdp::get \_ ProtocolVersion

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo get \_ ProtocolVersion** ottiene la versione del protocollo SDP (Session Descriptor Protocol; vedere rfc 2327).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProtocolVersion* \[ Cambio\]
</dt> <dd>

Puntatore alla versione del protocollo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                        |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro pProtocolVersion* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>     |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                       |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




