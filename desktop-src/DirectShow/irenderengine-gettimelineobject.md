---
description: Il metodo GetTimelineObject recupera la sequenza temporale attualmente in uso dal motore di rendering.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: Metodo IRenderEngine::GetTimelineObject (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c21868dc705a5c9f3b40649540fcaadb1f9219a7443d58c59964606cb7ed7d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823361"
---
# <a name="irenderenginegettimelineobject-method"></a>Metodo IRenderEngine::GetTimelineObject

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo recupera la sequenza temporale attualmente in uso dal `GetTimelineObject` motore di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppTimeline* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimeline**](iamtimeline.md) della sequenza temporale. Riceve il valore **NULL** se non è presente alcuna sequenza temporale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>                            |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>              | Puntatore non valido.<br/>                    |
| <dl> <dt>**E \_ DEVE \_ INIT \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |



 

## <a name="remarks"></a>Commenti

In caso di restituzione, se il valore di *\* ppTimeline* è diverso da **NULL,** **l'interfaccia IAMTimeline** ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




