---
description: Il metodo GetCountOfType Recupera il numero di oggetti di un determinato tipo contenuto in questa composizione e in tutte le relative tracce virtuali, in modo ricorsivo.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'Metodo IAMTimelineComp:: GetCountOfType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332046"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>Metodo IAMTimelineComp:: GetCountOfType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetCountOfType` metodo recupera il numero di oggetti di un tipo specificato contenuto nella composizione e in tutte le relative tracce virtuali, in modo ricorsivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* 
</dt> <dd>

Riceve il numero di oggetti del tipo specificato contenuti in questa composizione e in tutte le relative tracce virtuali, in modo ricorsivo.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Riceve il conteggio restituito in *pval* più il numero di composizioni ricercate, incluso quello.

</dd> <dt>

*MajorType* 
</dt> <dd>

Membro del tipo enumerato della [**sequenza temporale \_ principale \_**](timeline-major-type.md) , che specifica il tipo di oggetto da contare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un \_ puntatore e in caso contrario.

## <a name="remarks"></a>Commenti

In genere, un'applicazione non chiamerà questo metodo. Viene chiamato dal motore di rendering.

Se si contano le composizioni, il valore restituito in *pval* è zero e il valore restituito in *pValWithComps* è il numero di composizioni. Il valore di *\* pValWithComps* include la composizione sulla quale viene chiamato il metodo. Ad esempio, se si chiama questo metodo su una composizione vuota, *\* pValWithComps* è uguale a 1.

I gruppi non possono risiedere all'interno di composizioni, pertanto non è possibile usare questo metodo per conteggiare i gruppi. Il conteggio restituito sarà sempre zero. Per conteggiare i gruppi, chiamare il metodo [**IAMTimeline:: GetGroupCount**](iamtimeline-getgroupcount.md) .

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

 

 




