---
title: Metodo IDRMStatusCallback OnStatus
description: Il metodo OnStatus riceve messaggi di stato da processi DRM asincroni.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Metodo OnStatus windows Media Format
- Metodo OnStatus windows Media Format , interfaccia IDRMStatusCallback
- Interfaccia IDRMStatusCallback windows Media Format, metodo OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c9f8c0424752ababe684b426d78001f2783d62db9781fe3d6a23ed002e91773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847455"
---
# <a name="idrmstatuscallbackonstatus-method"></a>Metodo IDRMStatusCallback::OnStatus

Il **metodo OnStatus** riceve messaggi di stato da processi DRM asincroni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato* \[ Pollici\]
</dt> <dd>

Codice di stato. I codici di messaggio sono definiti nel **tipo di enumerazione \_ MSDRM STATUS.**

</dd> <dt>

*hr* \[ Pollici\]
</dt> <dd>

Codice restituito che supporta il messaggio di stato.

</dd> <dt>

*dwType* \[ Pollici\]
</dt> <dd>

Tipo di dati a cui punta *pValue*. Impostare su uno dei valori [**dell'enumerazione \_ DRM ATTR \_ DATATYPE.**](drm-attr-datatype.md)

</dd> <dt>

*pValue* \[ Pollici\]
</dt> <dd>

Puntatore ai dati correlati al messaggio di stato. Il tipo di dati è determinato dal valore del *parametro dwType.* Per altre informazioni, vedere [**l'enumerazione \_ DRM ATTR \_ DATATYPE.**](drm-attr-datatype.md)

</dd> <dt>

*pvContext* \[ Pollici\]
</dt> <dd>

Parametro facoltativo che può essere utilizzato per identificare l'oggetto che ha inviato il messaggio. Impostando *pvContext quando* si registra questo callback, è possibile usare lo stesso callback per gestire più processi asincroni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO DI \_ DATI ATTR \_ DRM**](drm-attr-datatype.md)
</dt> <dt>

[**Interfaccia IDRMStatusCallback**](idrmstatuscallback.md)
</dt> </dl>

 

 





