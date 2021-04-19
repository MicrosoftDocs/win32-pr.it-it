---
description: Il metodo EnableEffects Abilita o Disabilita tutti gli effetti nella sequenza temporale. Se gli effetti sono disabilitati, rimangono nella sequenza temporale ma non ne viene eseguito il rendering.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'Metodo IAMTimeline:: EnableEffects (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326799"
---
# <a name="iamtimelineenableeffects-method"></a>Metodo IAMTimeline:: EnableEffects

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `EnableEffects` Metodo Abilita o Disabilita tutti gli effetti nella sequenza temporale. Se gli effetti sono disabilitati, rimangono nella sequenza temporale ma non ne viene eseguito il rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valore booleano che specifica se abilitare o disabilitare gli effetti. Se **true**, gli effetti sono abilitati. Se **false**, gli effetti sono disabilitati.

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




