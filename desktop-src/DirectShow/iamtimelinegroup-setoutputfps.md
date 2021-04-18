---
description: Il metodo SetOutputFPS imposta la frequenza dei fotogrammi di output non compressi per questo gruppo.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'Metodo IAMTimelineGroup:: SetOutputFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331627"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>Metodo IAMTimelineGroup:: SetOutputFPS

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetOutputFPS` metodo imposta la frequenza dei fotogrammi di output non compressi per questo gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FPS* 
</dt> <dd>

Frequenza dei fotogrammi di output per questo gruppo, in frame al secondo. Il valore non può essere uguale a zero e non può contenere più di sette cifre dopo la posizione decimale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'output sottoposto a rendering da questo gruppo viene eseguito alla frequenza dei fotogrammi specificata e tutte le modifiche apportate al materiale di origine vengono arrotondate al limite del frame più vicino, come definito dalla frequenza dei fotogrammi. Per ottenere prestazioni ottimali, usare la stessa frequenza dei fotogrammi per tutti i gruppi, video e audio.

Il metodo [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) sovrascrive la frequenza dei fotogrammi.

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
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




