---
description: Il metodo SetTimelineObject imposta la sequenza temporale per il motore di rendering da usare.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'Metodo IRenderEngine:: SetTimelineObject (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330779"
---
# <a name="irenderenginesettimelineobject-method"></a>Metodo IRenderEngine:: SetTimelineObject

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetTimelineObject` metodo imposta la sequenza temporale per il motore di rendering da usare.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTimeline* 
</dt> <dd>

Puntatore all'interfaccia [**IAMTimeline**](iamtimeline.md) dell'oggetto della sequenza temporale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>                            |
| <dl> <dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>          | Memoria insufficiente.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>              | Puntatore non valido.<br/>                    |



 

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

[**Interfaccia IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




