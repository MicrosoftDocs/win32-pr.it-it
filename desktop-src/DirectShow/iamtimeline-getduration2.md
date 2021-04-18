---
description: 'Il metodo GetDuration2 recupera la durata della sequenza temporale. Questo metodo è equivalente a IAMTimeline:: GetDuration, ma accetta un parametro di tipo Double.'
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: 'Metodo IAMTimeline:: GetDuration2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329145"
---
# <a name="iamtimelinegetduration2-method"></a>Metodo IAMTimeline:: GetDuration2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetDuration2` metodo recupera la durata della sequenza temporale. Questo metodo è equivalente a [**IAMTimeline:: GetDuration**](iamtimeline-getduration.md), ma accetta un parametro di tipo **Double**.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDuration* 
</dt> <dd>

Riceve la durata della sequenza temporale, in secondi frazionari.

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

 

 




