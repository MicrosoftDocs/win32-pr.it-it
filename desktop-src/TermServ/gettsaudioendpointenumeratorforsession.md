---
title: Funzione di callback GetTSAudioEndpointEnumeratorForSession
description: Restituisce un riferimento a un enumeratore di endpoint audio per l'ID sessione specificato.
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
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302471"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>Funzione di callback GetTSAudioEndpointEnumeratorForSession

Restituisce un riferimento a un enumeratore di endpoint audio per l'ID sessione specificato. I consumer di questo enumeratore di endpoint audio, ad esempio MMDevAPI.dll, chiamano questa funzione per recuperare un enumeratore di endpoint audio in una sessione di Servizi Desktop remoto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID sessione* \[ in\]
</dt> <dd>

Identificatore della sessione di Servizi Desktop remoto.

</dd> <dt>

*ppEndpointEnumerator* \[ out\]
</dt> <dd>

Indirizzo di un puntatore a un'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**.

## <a name="remarks"></a>Commenti

Questa funzione non è definita in un file di intestazione. È necessario implementare ed esportare questa funzione nell'enumeratore dell'endpoint personalizzato e utilizzare la firma mostrata nel blocco della sintassi più indietro in questo argomento.

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

 

