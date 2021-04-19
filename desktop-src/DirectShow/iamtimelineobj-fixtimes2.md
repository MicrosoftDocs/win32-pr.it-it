---
description: "Il metodo FixTimes2 Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini, in base a quanto definito dall'impostazione della frequenza dei fotogrammi del gruppo padre. Questo metodo è equivalente a IAMTimelineObj:: FixTimes, ma accetta valori REFTIME."
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'Metodo IAMTimelineObj:: FixTimes2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333586"
---
# <a name="iamtimelineobjfixtimes2-method"></a>Metodo IAMTimelineObj:: FixTimes2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `FixTimes2` Metodo Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini, in base a quanto definito dall'impostazione della frequenza dei fotogrammi del gruppo padre. Questo metodo è equivalente a [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md), ma accetta valori [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStart* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di inizio, in secondi. Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di arresto, in secondi. Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o E \_ NOTINTREE se l'oggetto non fa parte di un gruppo.

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

 

 




