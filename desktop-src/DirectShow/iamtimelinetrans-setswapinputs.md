---
description: Il metodo SetSwapInputs specifica se gli input di transizione vengono scambiati.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'Metodo IAMTimelineTrans:: SetSwapInputs (qedit. h)'
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
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332643"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>Metodo IAMTimelineTrans:: SetSwapInputs

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetSwapInputs` metodo specifica se gli input di transizione vengono scambiati.

Per impostazione predefinita, una transizione passa dalla composizione di tutti i livelli di priorità inferiore al livello in cui risiede la transizione. È possibile invertire la progressione, in modo che la transizione provenga dal livello in cui risiedono al composito di livelli di priorità inferiore. Per ulteriori informazioni, vedere [direzione di transizione](transition-direction.md).

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

Specifica se gli input vengono scambiati. Se **false**, la transizione passa dalla composizione di tutti i livelli di priorità inferiore al livello di transizione. Se **true**, la transizione passa alla direzione opposta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo non modifica la direzione dell'effetto visivo. Ad esempio, una cancellazione da sinistra a destra continuerà a essere ancora da sinistra a destra. Per modificare la direzione, impostare la proprietà **Progress** usando l'interfaccia [**IPropertySetter**](ipropertysetter.md) .

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

[**Interfaccia IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




