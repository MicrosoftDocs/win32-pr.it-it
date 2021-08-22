---
description: Il metodo GetCountOfType recupera in modo ricorsivo il numero di oggetti di un determinato tipo contenuto in questa composizione e tutte le relative tracce virtuali.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: Metodo IAMTimelineComp::GetCountOfType (Qedit.h)
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
ms.openlocfilehash: b0504a7adb41a0d6a45714090a39aeefda9a3ef53b2d834540f600ec3ef871a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756411"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>Metodo IAMTimelineComp::GetCountOfType

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo recupera in modo ricorsivo il numero di oggetti di un determinato tipo contenuto in questa composizione e tutte le relative tracce `GetCountOfType` virtuali.

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

*Pval* 
</dt> <dd>

Riceve in modo ricorsivo il numero di oggetti del tipo specificato contenuti in questa composizione e tutte le relative tracce virtuali.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Riceve il conteggio restituito in *pVal* più il numero di composizioni ricercate, inclusa questa.

</dd> <dt>

*MajorType* 
</dt> <dd>

Membro del tipo [**enumerato TIMELINE \_ MAJOR \_ TYPE,**](timeline-major-type.md) che specifica il tipo di oggetto da contare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure E POINTER in caso \_ contrario.

## <a name="remarks"></a>Commenti

In genere, un'applicazione non chiamerà questo metodo. Viene chiamato dal motore di rendering.

Se si contano le composizioni, il valore restituito in *pVal* è zero e il valore restituito in *pValWithComps* è il numero di composizioni. Il valore di *\* pValWithComps* include la composizione su cui si chiama il metodo . Ad esempio, se si chiama questo metodo su una composizione vuota, *\* pValWithComps* è uguale a 1.

I gruppi non possono risiedere all'interno delle composizioni, pertanto non è possibile usare questo metodo per contare i gruppi. Il conteggio restituito sarà sempre zero. Per contare i gruppi, chiamare il [**metodo IAMTimeline::GetGroupCount.**](iamtimeline-getgroupcount.md)

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

[**Interfaccia IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




