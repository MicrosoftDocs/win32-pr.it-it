---
description: Il metodo getTimeline recupera la sequenza temporale a cui appartiene il gruppo.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'Metodo IAMTimelineGroup:: getTimeline (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328616"
---
# <a name="iamtimelinegroupgettimeline-method"></a>Metodo IAMTimelineGroup:: getTimeline

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetTimeline` metodo recupera la sequenza temporale a cui appartiene il gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppTimeline* \[ out\]
</dt> <dd>

Riceve l'interfaccia [**IAMTimeline**](iamtimeline.md) della sequenza temporale. Se il gruppo non fa parte di una sequenza temporale, il valore viene impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se il valore restituito in *ppTimeline* non è **null**, l'interfaccia **IAMTimeline** include un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

 

 




