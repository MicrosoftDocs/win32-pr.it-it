---
description: Il \_ metodo Get TransportProtocol ottiene il protocollo di trasporto.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'Metodo ITMedia:: get_TransportProtocol (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324885"
---
# <a name="itmediaget_transportprotocol-method"></a>Metodo ITMedia:: Get \_ TransportProtocol

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ TransportProtocol** ottiene il protocollo di trasporto. Questo valore viene specificato in aggiunta al formato multimediale, in modo che lo stesso formato multimediale standard possa essere trasferito su protocolli di trasporto diversi anche quando il protocollo di rete è lo stesso, ad esempio con l'audio PCM IVA e l'audio PCM RTP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppProtocol* \[ out\]
</dt> <dd>

Puntatore alla rappresentazione **BSTR** del protocollo di trasporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppProtocol* non è un puntatore valido.<br/>   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppProtocol* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::p UT \_ TransportProtocol**](itmedia-put-transportprotocol.md)
</dt> </dl>

 

