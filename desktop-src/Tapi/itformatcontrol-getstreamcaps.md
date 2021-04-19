---
description: Il metodo GetStreamCaps recupera le funzionalità associate a un indice di formato specificato.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'Metodo ITFormatControl:: GetStreamCaps (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329456"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>Metodo ITFormatControl:: GetStreamCaps

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **GetStreamCaps** recupera le funzionalità associate a un indice di formato specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Indice del formato di cui viene eseguito il probe.

</dd> <dt>

*ppMediaType* \[ out\]
</dt> <dd>

Puntatore a un descrittore del **\_ \_ tipo di supporto am** del formato terminale. Per ulteriori informazioni sul **\_ \_ tipo di supporto am**, vedere la documentazione di DirectX.

</dd> <dt>

*pStreamConfigCaps* \[ out\]
</dt> <dd>

Struttura [**di \_ \_ \_ Caps di configurazione del flusso TAPI**](tapi-stream-config-caps.md) che fornisce informazioni dettagliate sulle funzionalità di flusso.

</dd> <dt>

*pfEnabled* \[ out\]
</dt> <dd>

Indica se il formato associato all'indice corrente è abilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**\_ \_ tappi configurazione flusso TAPI \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




