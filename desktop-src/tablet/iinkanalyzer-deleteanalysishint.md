---
description: Rimuove un hint di analisi da IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: Metodo IInkAnalyzer::D eleteAnalysisHint (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129467"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>IInkAnalyzer::D Metodo eleteAnalysisHint

Rimuove un hint di analisi da [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pHintToDelete* \[ in\]
</dt> <dd>

Hint di analisi di [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

La rimozione di un hint di analisi non contrassegna l'area dell'hint per la rianalisi. Per contrassegnare l'area all'interno dell'hint per la rianalisi, utilizzare il [**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) per impostare l'area dirty sull'Unione dell'area e dell'area dirty correnti dell'hint di analisi.

L'hint viene rimosso dall'analizzatore; Tuttavia, il [**IContextNode**](icontextnode.md) stesso non viene eliminato.

Questo metodo restituisce un codice di errore quando *pHintToDelete* è un [**IContextNode**](icontextnode.md) che non è di tipo AnalysisHint (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).

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

[**Metodo IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




