---
title: Metodo IWMDRMLicenseQuery SetActionAllowedQueryParams (wmdrmsdk. h)
description: Il metodo SetActionAllowedQueryParams imposta le informazioni specifiche dell'ambiente per ottenere risultati di query più accurati quando si usa il metodo QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Metodo SetActionAllowedQueryParams Windows Media Format
- Metodo SetActionAllowedQueryParams Windows Media Format, interfaccia IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery-formato Windows Media, metodo SetActionAllowedQueryParams
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325558"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a>Metodo IWMDRMLicenseQuery:: SetActionAllowedQueryParams

Il metodo **SetActionAllowedQueryParams** imposta le informazioni specifiche dell'ambiente per ottenere risultati di query più accurati quando si usa il metodo [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fIsMF* \[ in\]
</dt> <dd>

Specifica se verrà eseguito il rendering del contenuto utilizzando gli oggetti di Microsoft Media Foundation SDK. **False** indica il rendering da parte degli oggetti di Windows Media Format SDK. Questo parametro è facoltativo.

</dd> <dt>

*dwAppSecLevel* \[ in\]
</dt> <dd>

Livello di sicurezza dell'applicazione di query. Questo valore è importante solo se verranno usati gli oggetti di Windows Media Format SDK. in questo caso, *fIsMF* deve essere impostato su **false**. Questo parametro è facoltativo.

</dd> <dt>

*fHasSerialNumber* \[ in\]
</dt> <dd>

Specifica se il dispositivo di destinazione per un'operazione di copia ha un numero di serie. Questo parametro è facoltativo e si applica solo alle query per le operazioni di copia.

</dd> <dt>

*bstrDeviceCert* \[ in\]
</dt> <dd>

Certificato del dispositivo di destinazione quando si usa DRM di Windows Media per i dispositivi portatili. Questo parametro è facoltativo e si applica solo alle query per le operazioni di copia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Esecuzione di query per informazioni dettagliate sui diritti**](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





