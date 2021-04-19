---
description: "Il metodo SetCutPoint2 imposta l'ora in cui la transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia. Questo metodo è equivalente a IAMTimelineTrans:: SetCutPoint, ma accetta un valore REFTIME."
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'Metodo IAMTimelineTrans:: SetCutPoint2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325035"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a>Metodo IAMTimelineTrans:: SetCutPoint2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetCutPoint2` metodo imposta l'ora in cui la transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia. Questo metodo è equivalente a [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md), ma accetta un valore [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TLTime* 
</dt> <dd>

Punto di taglio relativo all'inizio della transizione, in secondi.

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

 

 




