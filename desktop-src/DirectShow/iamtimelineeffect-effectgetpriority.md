---
description: Il metodo EffectGetPriority recupera il livello di priorità dell'effetto. Per un determinato oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità zero.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: Metodo IAMTimelineEffect::EffectGetPriority (Qedit.h)
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
ms.openlocfilehash: 62a66024961d0b36b0706510754092e1da3a9e7c6bc72bee6bc9c9b0dacf3187
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812391"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a>Metodo IAMTimelineEffect::EffectGetPriority

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `EffectGetPriority` metodo recupera il livello di priorità dell'effetto. Per un determinato oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pval* 
</dt> <dd>

Riceve il livello di priorità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineEffect**](iamtimelineeffect.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




