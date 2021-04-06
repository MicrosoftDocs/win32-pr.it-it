---
title: Metodo OnStatus IDRMStatusCallback
description: Il metodo OnStatus riceve i messaggi di stato dai processi DRM asincroni.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- OnStatus metodo Windows Media Format
- Metodo OnStatus Windows Media Format, interfaccia IDRMStatusCallback
- Interfaccia IDRMStatusCallback Windows Media Format, metodo OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045600"
---
# <a name="idrmstatuscallbackonstatus-method"></a>Metodo IDRMStatusCallback:: OnStatus

Il metodo **OnStatus** riceve i messaggi di stato dai processi DRM asincroni.

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

*Stato* \[ di in\]
</dt> <dd>

Codice di stato. I codici di messaggio sono definiti nel tipo di enumerazione **\_ dello stato MSDRM** .

</dd> <dt>

*risorse umane* \[ in\]
</dt> <dd>

Codice restituito che supporta il messaggio di stato.

</dd> <dt>

*dwType* \[ in\]
</dt> <dd>

Tipo di dati a cui punta *pValue*. Impostare su uno dei valori dell'enumerazione di [**\_ \_ tipo di dati DRM attr**](drm-attr-datatype.md) .

</dd> <dt>

*pValue* \[ in\]
</dt> <dd>

Puntatore ai dati correlati al messaggio di stato. Il tipo di dati è determinato dal valore del parametro *dwType* . Per ulteriori informazioni, vedere l'enumerazione del tipo di dati di [**DRM \_ attr \_**](drm-attr-datatype.md) .

</dd> <dt>

*pvContext* \[ in\]
</dt> <dd>

Parametro facoltativo che può essere usato per identificare l'oggetto che ha inviato il messaggio. Impostando *pvContext* quando si registra questo callback, è possibile utilizzare lo stesso callback per gestire più processi asincroni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**tipo di dati attr di DRM \_ \_**](drm-attr-datatype.md)
</dt> <dt>

[**Interfaccia IDRMStatusCallback**](idrmstatuscallback.md)
</dt> </dl>

 

 





