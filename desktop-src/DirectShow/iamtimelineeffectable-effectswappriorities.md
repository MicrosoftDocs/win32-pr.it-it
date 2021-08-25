---
description: Il metodo EffectSwapPriorities cambia i livelli di priorità di due effetti.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: Metodo IAMTimelineEffectable::EffectSwapPriorities (Qedit.h)
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
ms.openlocfilehash: 6e79f3f83422290600b4b6e75dbf15daff161f5e913a0300645254cdf94e7c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928231"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a>Metodo IAMTimelineEffectable::EffectSwapPriorities

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `EffectSwapPriorities` metodo cambia i livelli di priorità di due effetti.

Dati due valori di priorità, questo metodo scambia gli effetti a tali priorità. Quando il metodo viene restituito, l'effetto al primo livello di priorità è al secondo livello di priorità e viceversa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PrioritàA* 
</dt> <dd>

Primo livello di priorità in corrispondenza del quale scambiare gli effetti.

</dd> <dt>

*PrioritàB* 
</dt> <dd>

Secondo livello di priorità in corrispondenza del quale scambiare gli effetti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




