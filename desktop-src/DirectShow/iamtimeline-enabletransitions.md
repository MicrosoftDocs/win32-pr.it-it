---
description: Il metodo EnableTransitions Abilita o Disabilita tutte le transizioni nella sequenza temporale.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'Metodo IAMTimeline:: EnableTransitions (qedit. h)'
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
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326797"
---
# <a name="iamtimelineenabletransitions-method"></a>Metodo IAMTimeline:: EnableTransitions

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `EnableTransitions` Metodo Abilita o Disabilita tutte le transizioni nella sequenza temporale. Se le transizioni sono disabilitate, i motori di rendering li considerano come tagli; ovvero, l'output sottoposto a rendering passa immediatamente da una traccia alla successiva. Il punto di taglio predefinito è a metà della durata della transizione. È possibile modificare il punto di taglio chiamando il metodo [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md) sulla transizione. Le transizioni disabilitate non vengono rimosse dalla sequenza temporale.

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

Valore booleano che specifica se abilitare o disabilitare le transizioni. Se **true**, le transizioni sono abilitate. Se **false**, le transizioni sono disabilitate.

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

 

 




