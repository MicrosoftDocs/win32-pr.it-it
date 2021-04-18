---
description: Il metodo SetPropertySetter imposta il metodo di impostazione della proprietà dell'oggetto. Quando viene eseguito il rendering dell'oggetto, le informazioni sulle proprietà contenute nel metodo di impostazione della proprietà vengono applicate all'oggetto. Chiamare questo metodo sugli oggetti di transizione ed effetto.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'Metodo IAMTimelineObj:: SetPropertySetter (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330815"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a>Metodo IAMTimelineObj:: SetPropertySetter

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetPropertySetter` metodo imposta il metodo di impostazione della proprietà dell'oggetto. Quando viene eseguito il rendering dell'oggetto, le informazioni sulle proprietà contenute nel metodo di impostazione della proprietà vengono applicate all'oggetto. Chiamare questo metodo sugli oggetti di transizione ed effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

Puntatore all'interfaccia [**IPropertySetter**](ipropertysetter.md) del setter della proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

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

 

 




