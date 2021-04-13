---
description: Rimuove il tratto specificato da IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'Metodo IInkAnalyzer:: RemoveStroke (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526485"
---
# <a name="iinkanalyzerremovestroke-method"></a>Metodo IInkAnalyzer:: RemoveStroke

Rimuove il tratto specificato da [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plStrokeId* \[ in\]
</dt> <dd>

Identificatore del tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questo metodo rimuove i dati del pacchetto per e i riferimenti a, il tratto specificato da [**IInkAnalyzer**](iinkanalyzer.md).

Questo metodo rimuove il tratto dal nodo di contesto foglia che fa riferimento al tratto. Se [**IContextNode**](icontextnode.md) non fa più riferimento ad alcun tratto, questo metodo elimina **IContextNode** e tutti gli oggetti **IContextNode** predecessore che non hanno più nodi figlio.

Dopo la rimozione del tratto da [**IContextNode**](icontextnode.md), questo metodo aggiorna l'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) per includere il rettangolo di delimitazione del tratto rimosso.

Se *plStrokeId* non identifica un tratto associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare Ink Analyzer.

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

[**Metodo IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




