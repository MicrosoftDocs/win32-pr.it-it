---
description: "Il metodo GetNextTrans2 recupera la prima transizione visualizzata all'ora specificata o successiva. Questo metodo è equivalente a IAMTimelineTransable:: GetNextTrans, ma accetta un valore REFTIME."
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'Metodo IAMTimelineTransable:: GetNextTrans2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332972"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a>Metodo IAMTimelineTransable:: GetNextTrans2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetNextTrans2` metodo recupera la prima transizione visualizzata all'ora specificata o successiva. Questo metodo è equivalente a [**IAMTimelineTransable:: GetNextTrans**](iamtimelinetransable-getnexttrans.md), ma accetta un valore [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppTrans* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di transizione.

</dd> <dt>

*pInOut* 
</dt> <dd>

Puntatore a una variabile che specifica il tempo in secondi. In input, questo valore specifica l'ora da cui trovare la transizione. Nell'output, se viene recuperata una transizione, questo valore viene impostato sull'ora di arresto della transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il metodo recupera una transizione o S \_ false se non trova una transizione. In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.

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

[**Interfaccia IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




