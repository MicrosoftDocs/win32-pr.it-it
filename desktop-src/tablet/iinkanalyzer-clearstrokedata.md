---
description: Cancella i dati dei pacchetti di tratti da IInkAnalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: Metodo IInkAnalyzer::ClearStrokeData (IACom.h)
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
ms.openlocfilehash: 3413d8d6fb322030afdcffb97e8739ae4ca5e2314fe968f366ce25e58d90351e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057871"
---
# <a name="iinkanalyzerclearstrokedata-method"></a>Metodo IInkAnalyzer::ClearStrokeData

Cancella i dati dei pacchetti di tratti [**da IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ Pollici\]
</dt> <dd>

Identificatore del tratto per il quale vengono cancellati i dati del pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Usare questo metodo quando i dati del pacchetto per un tratto cambiano, ad esempio quando un tratto viene spostato o trasformato in altro modo. [**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) quando è necessario che i dati del pacchetto del tratto siano stati cancellati da un tratto per il quale sono stati cancellati i dati del pacchetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




