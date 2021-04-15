---
description: Cancella i dati dei pacchetti Stroke dal IInkAnalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'Metodo IInkAnalyzer:: ClearStrokeData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485084"
---
# <a name="iinkanalyzerclearstrokedata-method"></a>Metodo IInkAnalyzer:: ClearStrokeData

Cancella i dati dei pacchetti Stroke dal [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ in\]
</dt> <dd>

Identificatore del tratto per il quale vengono cancellati i dati del pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Utilizzare questo metodo quando i dati dei pacchetti per un tratto cambiano, ad esempio quando un tratto viene spostato o trasformato in altro modo. [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) quando è necessario che i dati dei pacchetti trattino da un tratto per il quale sono stati cancellati i dati del pacchetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




