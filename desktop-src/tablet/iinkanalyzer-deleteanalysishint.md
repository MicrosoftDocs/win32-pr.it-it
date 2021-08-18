---
description: Rimuove un hint di analisi da IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: Metodo IInkAnalyzer::D eleteAnalysisHint (IACom.h)
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
ms.openlocfilehash: 6f514f20ed99f7fc56725f582b815639cb9d8b3179e9e428845d7e066b6e3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967290"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>Metodo IInkAnalyzer::D eleteAnalysisHint

Rimuove un hint di analisi da [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pHintToDelete* \[ Pollici\]
</dt> <dd>

Suggerimento di analisi da [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

La rimozione di un hint di analisi non contrassegna l'area dell'hint per la rianalisi. Per contrassegnare l'area all'interno dell'hint per la rianalisi, usare il metodo [**IInkAnalyzer::SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) per impostare l'area dirty sull'unione dell'area dirty corrente e dell'area dell'hint di analisi.

L'hint viene rimosso dall'analizzatore. Tuttavia, [**L'oggetto IContextNode**](icontextnode.md) stesso non viene eliminato.

Questo metodo restituisce un codice di errore quando *pHintToDelete* è un [**IContextNode**](icontextnode.md) che non è di tipo AnalysisHint (vedere [**IContextNode::GetType**](icontextnode-gettype.md)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




