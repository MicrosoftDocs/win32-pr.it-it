---
description: "Il metodo ModifyStopTime2 imposta l'ora di arresto. Questo metodo è equivalente a IAMTimelineSrc:: ModifyStopTime, ma accetta un valore REFTIME."
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'Metodo IAMTimelineSrc:: ModifyStopTime2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332751"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>Metodo IAMTimelineSrc:: ModifyStopTime2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `ModifyStopTime2` metodo imposta l'ora di arresto. Questo metodo è equivalente a [**IAMTimelineSrc:: ModifyStopTime**](iamtimelinesrc-modifystoptime.md), ma accetta un valore [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stop* 
</dt> <dd>

Nuova ora di arresto, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o E \_ INVALIDARG se l'ora specificata non è valida.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




