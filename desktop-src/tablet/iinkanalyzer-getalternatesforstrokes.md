---
description: Recupera le alternative di analisi per i tratti con gli identificatori di tratto specificati.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'Metodo IInkAnalyzer:: GetAlternatesForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129458"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a>Metodo IInkAnalyzer:: GetAlternatesForStrokes

Recupera le alternative di analisi per i tratti con gli identificatori di tratto specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ in\]
</dt> <dd>

Il numero di identificatori di tratto in *plStrokes*.

</dd> <dt>

*plStrokes* \[ in\]
</dt> <dd>

Matrice di identificatori del tratto.

</dd> <dt>

*ulMaximumAlternates* \[ in\]
</dt> <dd>

Numero massimo di alternative di analisi restituite.

</dd> <dt>

*ppAlternates* \[ out\]
</dt> <dd>

Oggetto [**IAnalysisAlternates**](ianalysisalternates.md) che contiene le alternative di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppAlternates* quando non è più necessario utilizzare l'oggetto.

 

Il [**IAnalysisAlternate**](ianalysisalternate.md) superiore viene restituito come prima alternativa della raccolta.

Non è necessario che i tratti specificati rappresentino aree adiacenti del documento.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: getalters**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

