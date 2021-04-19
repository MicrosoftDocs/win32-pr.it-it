---
description: Il metodo GetSwapInputs recupera un valore che indica se gli input di transizione vengono scambiati.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'Metodo IAMTimelineTrans:: GetSwapInputs (qedit. h)'
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
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333261"
---
# <a name="iamtimelinetransgetswapinputs-method"></a>Metodo IAMTimelineTrans:: GetSwapInputs

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetSwapInputs` metodo recupera un valore che indica se gli input di transizione vengono scambiati.

Per impostazione predefinita, una transizione passa dalla composizione di tutti i livelli di priorità inferiore al livello in cui risiede la transizione. È possibile invertire la progressione, in modo che la transizione provenga dal livello in cui risiedono al composito di livelli di priorità inferiore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* 
</dt> <dd>

Riceve un valore booleano. Se il valore è **false**, la transizione passa dalla composizione di tutti i livelli di priorità inferiore al livello di transizione. Se il valore è **true**, la transizione passa alla direzione opposta. Il valore predefinito è **false**.

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

[**Interfaccia IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




