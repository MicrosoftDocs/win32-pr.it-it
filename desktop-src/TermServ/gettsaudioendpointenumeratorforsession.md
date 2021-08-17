---
title: Funzione di callback GetTSAudioEndpointEnumeratorForSession
description: Restituisce un riferimento a un enumeratore endpoint audio per l'ID sessione specificato.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Funzione di callback GetTSAudioEndpointEnumeratorForSession Servizi Desktop remoto
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f64af1d7e886b418ac87cd360302101a60d746d707652f605a648e9812a5547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059589"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>Funzione di callback GetTSAudioEndpointEnumeratorForSession

Restituisce un riferimento a un enumeratore endpoint audio per l'ID sessione specificato. I consumer di questo enumeratore dell'endpoint audio, ad esempio MMDevAPI.dll, chiamano questa funzione per recuperare un enumeratore dell'endpoint audio in una Servizi Desktop remoto sessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SessionId* \[ Pollici\]
</dt> <dd>

Identificatore dell'Servizi Desktop remoto sessione.

</dd> <dt>

*PpEndpointEnumerator* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore a [**un'interfaccia IMMDeviceEnumerator.**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**.

## <a name="remarks"></a>Commenti

Questa funzione non è definita in un file di intestazione. È necessario implementare ed esportare questa funzione nell'enumeratore dell'endpoint personalizzato e usare la firma illustrata nel blocco di sintassi più indietro in questo argomento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>         |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Implementazione di un enumeratore di endpoint audio personalizzato](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

