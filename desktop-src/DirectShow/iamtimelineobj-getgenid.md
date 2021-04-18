---
description: Il metodo getgenid recupera l'identificatore generato dall'oggetto. L'identificatore è un numero riservato; le applicazioni non devono utilizzarlo.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'Metodo IAMTimelineObj:: getgenid (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331279"
---
# <a name="iamtimelineobjgetgenid-method"></a>Metodo IAMTimelineObj:: getgenid

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetGenID` metodo recupera l'identificatore generato dall'oggetto. L'identificatore è un numero riservato; le applicazioni non devono utilizzarlo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* 
</dt> <dd>

Riceve l'identificatore generato.

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




