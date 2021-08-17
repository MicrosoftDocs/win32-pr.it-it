---
description: Il metodo GetSwapInputs recupera un valore che indica se gli input della transizione vengono scambiati.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: Metodo IAMTimelineTrans::GetSwapInputs (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 566dbc54b30619c67ffb9d804e4854d51cae86d3688bda0b48eebfeb64cdb749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316301"
---
# <a name="iamtimelinetransgetswapinputs-method"></a>Metodo IAMTimelineTrans::GetSwapInputs

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetSwapInputs` metodo recupera un valore che indica se gli input della transizione vengono scambiati.

Per impostazione predefinita, una transizione passa dal composito di tutti i livelli con priorità più bassa al livello in cui risiede la transizione. È possibile invertire questa progressione, in modo che la transizione torni dal livello in cui risiede al composito dei livelli con priorità più bassa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pval* 
</dt> <dd>

Riceve un valore booleano. Se il valore è **FALSE,** la transizione passa dal composito di tutti i livelli con priorità inferiore al livello di transizione. Se il valore è **TRUE,** la transizione va nella direzione opposta. Il valore predefinito è **FALSE.**

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

[**Interfaccia IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




