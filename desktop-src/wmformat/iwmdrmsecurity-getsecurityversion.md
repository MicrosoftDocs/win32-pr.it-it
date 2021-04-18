---
title: Metodo IWMDRMSecurity GetSecurityVersion (wmdrmsdk. h)
description: Il metodo GetSecurityVersion recupera la versione del sottosistema DRM nel computer client.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Metodo GetSecurityVersion Windows Media Format
- Metodo GetSecurityVersion Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetSecurityVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327264"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a>Metodo IWMDRMSecurity:: GetSecurityVersion

Il metodo **GetSecurityVersion** recupera la versione del sottosistema DRM nel computer client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrVersion* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve il numero di versione del sottosistema DRM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Il numero di versione è espresso come stringa costituita da quattro numeri separati da punti. Il primo numero è il numero di versione principale, che in genere è impostato su 2. Il secondo numero è il numero di versione secondario, compreso tra 2 e 10. Il terzo numero è sempre impostato su 0. Il quarto numero è impostato su 0 o 1 e è un valore booleano che indica se il sottosistema è stato personalizzato. Ad esempio, un numero di versione di "2.4.0.1" indica la quarta versione secondaria della seconda versione principale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





