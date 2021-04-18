---
description: Il metodo GetPropertySetter Recupera il metodo di impostazione della proprietà dell'oggetto. Quando viene eseguito il rendering dell'oggetto, le informazioni sulle proprietà contenute nel metodo di impostazione della proprietà vengono applicate all'oggetto.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'Metodo IAMTimelineObj:: GetPropertySetter (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331271"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a>Metodo IAMTimelineObj:: GetPropertySetter

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetPropertySetter` metodo recupera il setter della proprietà dell'oggetto. Quando viene eseguito il rendering dell'oggetto, le informazioni sulle proprietà contenute nel metodo di impostazione della proprietà vengono applicate all'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IPropertySetter**](ipropertysetter.md) del setter della proprietà. Se l'oggetto non dispone di un setter di proprietà, il valore viene impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se il valore restituito in *pval* non è **null**, l'interfaccia **IPropertySetter** include un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




