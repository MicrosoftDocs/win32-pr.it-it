---
description: Il metodo GetOutputFPS recupera la frequenza dei fotogrammi di output di questo gruppo.
ms.assetid: e6dfa4a9-4d44-4ce7-9aec-3564fd337ff6
title: 'Metodo IAMTimelineGroup:: GetOutputFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f02e7db36e5ea61e3c738b4c2d92678674bfcec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333681"
---
# <a name="iamtimelinegroupgetoutputfps-method"></a>Metodo IAMTimelineGroup:: GetOutputFPS

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetOutputFPS` metodo recupera la frequenza dei fotogrammi di output di questo gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetOutputFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFPS* 
</dt> <dd>

Riceve la frequenza dei fotogrammi di output, in frame al secondo.

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
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




