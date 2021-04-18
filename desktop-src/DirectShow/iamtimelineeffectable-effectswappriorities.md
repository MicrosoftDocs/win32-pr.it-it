---
description: Il metodo EffectSwapPriorities passa i livelli di priorità di due effetti.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'Metodo IAMTimelineEffectable:: EffectSwapPriorities (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333696"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a>Metodo IAMTimelineEffectable:: EffectSwapPriorities

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `EffectSwapPriorities` metodo passa i livelli di priorità di due effetti.

Dato due valori di priorità, questo metodo scambia gli effetti con tali priorità. Quando il metodo restituisce un risultato, l'effetto che si trovava al primo livello di priorità è il secondo livello di priorità e viceversa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Priorità* 
</dt> <dd>

Primo livello di priorità in corrispondenza del quale scambiare gli effetti.

</dd> <dt>

*PriorityB* 
</dt> <dd>

Secondo livello di priorità in corrispondenza del quale scambiare gli effetti.

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

[**Interfaccia IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




