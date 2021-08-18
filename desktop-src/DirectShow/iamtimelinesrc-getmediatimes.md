---
description: Il metodo GetMediaTimes recupera l'ora di inizio e di arresto dei supporti.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: Metodo IAMTimelineSrc::GetMediaTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2a4b3fc716ba0865a010155e2f1e8a592cab396f5efb0c2d4afa3264da4a337
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756041"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a>Metodo IAMTimelineSrc::GetMediaTimes

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetMediaTimes` metodo recupera l'ora di inizio e di arresto dei supporti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pstart* 
</dt> <dd>

Riceve l'ora di inizio del supporto, in unità di 100 nanosecondi.

</dd> <dt>

*pStop* 
</dt> <dd>

Riceve l'ora di arresto multimediale, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

I tempi dei supporti sono relativi al file multimediale originale. Per altre informazioni, vedere [Time in DirectShow Editing Services.](time-in-directshow-editing-services.md)

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




