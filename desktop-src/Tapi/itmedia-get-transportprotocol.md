---
description: Il metodo get \_ TransportProtocol ottiene il protocollo di trasporto.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: Metodo ITMedia::get_TransportProtocol (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7927469ff00caab36ab45af12939c6f2f6518a415d4a764c3d04f9c715db75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682771"
---
# <a name="itmediaget_transportprotocol-method"></a>Metodo ITMedia::get \_ TransportProtocol

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ TransportProtocol** ottiene il protocollo di trasporto. Questo valore viene specificato in aggiunta al formato multimediale in modo che lo stesso formato multimediale standard possa essere trasportato su protocolli di trasporto diversi anche quando il protocollo di rete è lo stesso, ad esempio con audio PCM Iva e audio PCM RTP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppProtocol* \[ Cambio\]
</dt> <dd>

Puntatore alla **rappresentazione BSTR** del protocollo di trasporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro ppProtocol* non è un puntatore valido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il *parametro ppProtocol.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::put \_ TransportProtocol**](itmedia-put-transportprotocol.md)
</dt> </dl>

 

