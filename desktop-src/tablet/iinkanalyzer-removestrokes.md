---
description: Rimuove i tratti specificati da IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'Metodo IInkAnalyzer:: RemoveStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129450"
---
# <a name="iinkanalyzerremovestrokes-method"></a>Metodo IInkAnalyzer:: RemoveStrokes

Rimuove i tratti specificati da [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdCount* \[ in\]
</dt> <dd>

Il numero di identificatori di tratto in *plStrokes*.

</dd> <dt>

*plStrokes* \[ in\]
</dt> <dd>

Identificatori per i tratti da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questo metodo rimuove i dati del pacchetto per i riferimenti e ai tratti specificati da [**IInkAnalyzer**](iinkanalyzer.md).

Questo metodo rimuove i tratti dal nodo di contesto foglia che fa riferimento ai tratti. Se un [**IContextNode**](icontextnode.md) non fa più riferimento ad alcun tratto, questo metodo elimina **IContextNode** e tutti gli oggetti **IContextNode** predecessore che non hanno più nodi figlio.

Dopo la rimozione dei tratti da [**IContextNode**](icontextnode.md), questo metodo aggiorna l'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) per includere il rettangolo di delimitazione dei tratti rimossi.

Se un tratto identificato in *plStrokes* non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo ignora l'identificatore.

Se nessuno dei tratti identificati in *plStrokes* è associato a Ink Analyzer, questo metodo restituisce senza aggiornare [**IInkAnalyzer**](iinkanalyzer.md).

Questo metodo restituisce un codice di errore e quando *plStrokes* è null.

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

[**Metodo IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




