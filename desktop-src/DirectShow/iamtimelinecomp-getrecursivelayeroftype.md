---
description: Il metodo GetRecursiveLayerOfType esegue un ordine di profondità-primo delle tracce virtuali contenute in questa composizione e recupera l'ennesima traccia virtuale dall'ordinamento.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'Metodo IAMTimelineComp:: GetRecursiveLayerOfType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332039"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a>Metodo IAMTimelineComp:: GetRecursiveLayerOfType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetRecursiveLayerOfType` metodo esegue un ordine di profondità-primo delle tracce virtuali contenute in questa composizione e recupera la traccia virtuale *n* dall'ordinamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppVirtualTrack* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della traccia virtuale.

</dd> <dt>

*WhichLayer* 
</dt> <dd>

Specifica la traccia virtuale da recuperare, indicizzata da zero.

</dd> <dt>

*Tipo* 
</dt> <dd>

Membro del tipo [**di \_ \_ tipo principale della sequenza temporale**](timeline-major-type.md) enumerato che specifica se includere tracce nella ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                  | Descrizione                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Nessun oggetto del tipo specificato.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null** .<br/>       |



 

## <a name="remarks"></a>Commenti

In genere, un'applicazione non deve chiamare questo metodo.

Se il parametro di *tipo* è una sequenza temporale di \_ \_ tipo principale \_ , il primo ordine di profondità include le tracce. In caso contrario, include solo le composizioni e i gruppi. L'oggetto stesso è incluso nell'ordinamento.

Nella disposizione seguente, ad esempio, a partire dalla composizione A, l'ordinamento sarà B, C, F, D, E, A.

![getrecursivelayeroftype](images/composition.png)

Se il metodo ha esito positivo, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

[**Interfaccia IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




