---
description: Il metodo EffectGetPriority Recupera il livello di priorità dell'effetto. Per un determinato oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità zero.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'Metodo IAMTimelineEffect:: EffectGetPriority (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333699"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a>Metodo IAMTimelineEffect:: EffectGetPriority

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `EffectGetPriority` metodo recupera il livello di priorità dell'effetto. Per un determinato oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* 
</dt> <dd>

Riceve il livello di priorità.

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

[**Interfaccia IAMTimelineEffect**](iamtimelineeffect.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




