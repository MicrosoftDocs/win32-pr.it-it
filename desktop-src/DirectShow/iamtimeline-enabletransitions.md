---
description: Il metodo EnableTransitions abilita o disabilita tutte le transizioni nella sequenza temporale.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: Metodo IAMTimeline::EnableTransitions (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9356ac53488f68e54a05a85e8e287850138ee131f80dd3bb45b81cf606b5a351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401072"
---
# <a name="iamtimelineenabletransitions-method"></a>Metodo IAMTimeline::EnableTransitions

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `EnableTransitions` metodo abilita o disabilita tutte le transizioni nella sequenza temporale. Se le transizioni sono disabilitate, i motori di rendering le trattano come riduzioni. ciò significa che l'output di cui è stato eseguito il rendering passa immediatamente da una traccia all'altra. Il punto di taglio predefinito si trova a metà della durata della transizione. È possibile modificare il punto di taglio chiamando il [**metodo IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) sulla transizione. Le transizioni disabilitate non vengono rimosse dalla sequenza temporale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valore booleano che specifica se abilitare o disabilitare le transizioni. Se **TRUE,** le transizioni sono abilitate. Se **FALSE,** le transizioni sono disabilitate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




