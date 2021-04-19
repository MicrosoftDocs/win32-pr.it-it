---
description: 'Il metodo GetDefaultFPS recupera la frequenza dei fotogrammi di output predefinita, in frame al secondo (FPS). I gruppi utilizzano questo valore come frequenza dei fotogrammi predefinita. Per impostare la frequenza dei fotogrammi di un gruppo, chiamare il metodo IAMTimelineGroup:: SetOutputFPS sul gruppo.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'Metodo IAMTimeline:: GetDefaultFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327428"
---
# <a name="iamtimelinegetdefaultfps-method"></a>Metodo IAMTimeline:: GetDefaultFPS

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetDefaultFPS` metodo recupera la frequenza dei fotogrammi di output predefinita, in frame al secondo (fps). I gruppi utilizzano questo valore come frequenza dei fotogrammi predefinita. Per impostare la frequenza dei fotogrammi di un gruppo, chiamare il metodo [**IAMTimelineGroup:: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) sul gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFPS* 
</dt> <dd>

Riceve la frequenza dei fotogrammi predefinita, in frame al secondo.

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

 

 




