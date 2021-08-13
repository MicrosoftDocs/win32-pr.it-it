---
description: Il metodo GetStreamCaps recupera le funzionalità associate a un indice di formato specificato.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: Metodo ITFormatControl::GetStreamCaps (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f54cbd44a946c0fcd3cf297c4cacadc49369765b8c1b6505031a145768c3b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406111"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>Metodo ITFormatControl::GetStreamCaps

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo GetStreamCaps** recupera le funzionalità associate a un indice di formato specificato.

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

*dwIndex* \[ Pollici\]
</dt> <dd>

Indice del formato di cui viene probe.

</dd> <dt>

*ppMediaType* \[ Cambio\]
</dt> <dd>

Puntatore a un **\_ descrittore AM MEDIA \_ TYPE** del formato terminale. Per altre informazioni su **AM \_ MEDIA \_ TYPE,** vedere la documentazione di DirectX.

</dd> <dt>

*pStreamConfigCaps* \[ Cambio\]
</dt> <dd>

Struttura [**TAPI \_ STREAM CONFIG \_ \_ CAPS**](tapi-stream-config-caps.md) che fornisce informazioni dettagliate sulle funzionalità del flusso.

</dd> <dt>

*pfEnabled* \[ Cambio\]
</dt> <dd>

Indica se il formato associato all'indice corrente è abilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




