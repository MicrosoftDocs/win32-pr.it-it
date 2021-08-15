---
description: Rimuove i tratti specificati da IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: Metodo IInkAnalyzer::RemoveStrokes (IACom.h)
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
ms.openlocfilehash: e6d53d21df9734ee43cdda618c5221fd83300598d46b51bd366c50fedf5cec45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092021"
---
# <a name="iinkanalyzerremovestrokes-method"></a>Metodo IInkAnalyzer::RemoveStrokes

Rimuove i tratti specificati da [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdCount* \[ Pollici\]
</dt> <dd>

Numero di identificatori di tratto in *plStrokes.*

</dd> <dt>

*plStrokes* \[ Pollici\]
</dt> <dd>

Identificatori per i tratti da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Questo metodo rimuove i dati del pacchetto per e i riferimenti ai tratti specificati da [**IInkAnalyzer.**](iinkanalyzer.md)

Questo metodo rimuove i tratti dal nodo di contesto foglia che fa riferimento ai tratti. Se un [**oggetto IContextNode**](icontextnode.md) non fa più riferimento ad alcun tratto, questo metodo elimina gli oggetti **IContextNode** e i predecessori **IContextNode** che non hanno più nodi figlio.

Dopo che questo metodo rimuove i tratti da [**IContextNode,**](icontextnode.md)aggiorna l'area dirty dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il metodo [**IInkAnalyzer::GetDirtyRegion)**](iinkanalyzer-getdirtyregion.md)per includere il rettangolo di selezione dei tratti rimossi.

Se un tratto identificato in *plStrokes* non è associato a [**IInkAnalyzer,**](iinkanalyzer.md)questo metodo ignora l'identificatore.

Se nessuno dei tratti identificati in *plStrokes* è associato all'analizzatore input penna, questo metodo restituisce senza aggiornare [**LInkAnalyzer.**](iinkanalyzer.md)

Questo metodo restituisce il codice di errore quando *plStrokes* è Null.

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

[**Metodo IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




