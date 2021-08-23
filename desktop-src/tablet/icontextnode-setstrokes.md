---
description: Associa i tratti specificati a questo IContextNode.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: Metodo IContextNode::SetStrokes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67834a10e5e08070c991af76fe19b720853789a9f5e2c771f5c1ed0dc4fc9754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119552601"
---
# <a name="icontextnodesetstrokes-method"></a>Metodo IContextNode::SetStrokes

Associa i tratti specificati a questo [**oggetto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ Pollici\]
</dt> <dd>

Numero di identificatori di tratti in *plStrokeIds.*

</dd> <dt>

*plStrokeIds* \[ Pollici\]
</dt> <dd>

Identificatori dei tratti da associare a [**questo oggetto IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questo metodo non aggiorna l'area dirty dell'analizzatore input penna (vedere [**Metodo IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Usare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Usare questo metodo per assegnare i dati del tratto a un nodo di contesto specifico. Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con **IInkAnalyzer,** vedere [Proxy dati con l'analisi dell'input penna](data-proxy-with-ink-analysis.md).

Se uno dei tratti specificati è già associato a [**IInkAnalyzer,**](iinkanalyzer.md)questo metodo restituisce **E \_ INVALIDARG**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IContextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




