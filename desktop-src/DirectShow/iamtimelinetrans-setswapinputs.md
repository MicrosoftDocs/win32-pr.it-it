---
description: Il metodo SetSwapInputs specifica se gli input di transizione vengono scambiati.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: Metodo IAMTimelineTrans::SetSwapInputs (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3da350c6fe34f671d7af53ca67c404b4e327690918434b5e2fb1426e4a0953ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052081"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>Metodo IAMTimelineTrans::SetSwapInputs

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetSwapInputs` metodo specifica se gli input della transizione vengono scambiati.

Per impostazione predefinita, una transizione passa dal composito di tutti i livelli con priorità più bassa al livello in cui risiede la transizione. È possibile invertire questa progressione, in modo che la transizione torni dal livello in cui risiede al composito dei livelli con priorità più bassa. Per altre informazioni, vedere [Direzione della transizione.](transition-direction.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Val* 
</dt> <dd>

Specifica se gli input vengono scambiati. Se **FALSE,** la transizione passa dal composito di tutti i livelli con priorità più bassa al livello di transizione. Se **TRUE,** la transizione va nella direzione opposta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo non modifica la direzione dell'effetto visivo. Ad esempio, una cancellazione da sinistra a destra continuerà a essere da sinistra a destra. Per modificare la direzione, impostare la **proprietà Progress** usando [**l'interfaccia IPropertySetter.**](ipropertysetter.md)

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

[**Interfaccia IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




