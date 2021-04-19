---
description: Il metodo GetNextTrans recupera la prima transizione visualizzata all'ora specificata o successiva.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'Metodo IAMTimelineTransable:: GetNextTrans (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324000"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>Metodo IAMTimelineTransable:: GetNextTrans

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetNextTrans` metodo recupera la prima transizione visualizzata all'ora specificata o successiva.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
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

Puntatore a una variabile che specifica l'ora in unità 100-nanosecondi. In input, questo valore specifica l'ora da cui trovare la transizione. Nell'output, se viene recuperata una transizione, questo valore viene impostato sull'ora di arresto della transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il metodo recupera una transizione o S \_ false se non trova una transizione. In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.

## <a name="remarks"></a>Commenti

L'ora di inizio della transizione potrebbe essere inferiore al tempo specificato in *pin*, se la transizione si estende al tempo specificato.

Se il metodo restituisce S \_ OK, l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

 

 




