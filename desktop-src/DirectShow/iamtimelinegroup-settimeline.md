---
description: 'Non supportata. Chiamare invece il metodo IAMTimeline:: AddGroup.'
ms.assetid: dd671fa5-ed5a-46e2-b4bd-a37f0e7458ca
title: 'Metodo IAMTimelineGroup:: setimeline (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 166d65f5ae9a14f58ed7b20763ab5e4a136df598
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331437"
---
# <a name="iamtimelinegroupsettimeline-method"></a>Metodo IAMTimelineGroup:: setimeline

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Non supportata. Chiamare invece il metodo [**IAMTimeline:: addgroup**](iamtimeline-addgroup.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTimeline(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTimeline* 
</dt> <dd>

Riservato.

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

[**Interfaccia IAMTimelineGroup**](iamtimelinegroup.md)
</dt> </dl>

 

 




