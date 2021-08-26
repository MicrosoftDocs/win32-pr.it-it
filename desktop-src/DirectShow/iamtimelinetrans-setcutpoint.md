---
description: Il metodo SetCutPoint imposta l'ora in cui la transizione passa da un'origine a quella successiva, se il rendering della transizione viene eseguito come taglio.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: Metodo IAMTimelineTrans::SetCutPoint (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c411925ebe10ad35641e38ae2332605d7691ae24f0cc96ff716bd7d00e6603f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052071"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>Metodo IAMTimelineTrans::SetCutPoint

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il metodo imposta l'ora in cui la transizione passa da un'origine a quella successiva, se il rendering della transizione viene `SetCutPoint` eseguito come taglio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TLTime* 
</dt> <dd>

Punto di taglio relativo all'inizio della transizione, in unità di 100 nanosecondi. Se il valore non rientra nei limiti della transizione, viene troncato all'ora valida più vicina.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il punto di taglio è il centro della transizione. Ad esempio, in una transizione che si estende su un secondo, il punto di taglio predefinito è 0,5 secondi nella transizione.

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

[**Interfaccia IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




