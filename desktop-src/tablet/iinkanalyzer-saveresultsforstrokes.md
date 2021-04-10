---
description: Salva i risultati dell'analisi per i tratti specificati associati a un IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'Metodo IInkAnalyzer:: SaveResultsForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343676"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>Metodo IInkAnalyzer:: SaveResultsForStrokes

Salva i risultati dell'analisi per i tratti specificati associati a un [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ in\]
</dt> <dd>

Il numero di identificatori di tratto in **plStrokeIds**.

</dd> <dt>

*plStrokeIds* \[ in\]
</dt> <dd>

Matrice di identificatori del tratto.

</dd> <dt>

*pulSerializedDataSize* \[ in uscita\]
</dt> <dd>

Numero di byte in *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ out, retval\]
</dt> <dd>

Puntatore ai dati di analisi serializzati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) su \* *ppbSerializedData* quando le informazioni non sono più necessarie.

 

Questo metodo consente di salvare i risultati di analisi correnti per i tratti specificati. Questo metodo salva gli oggetti foglia input penna [**IContextNode**](icontextnode.md) contenenti i tratti e tutti i predecessori dei nodi di contesto. Questo metodo non salva alcun nodo dati Stroke o hint di analisi. È responsabilità dell'applicazione sincronizzare i risultati dell'analisi e i dati di Stroke corrispondenti, se il problema è permanente.

Questo metodo restituisce un codice di errore quando un oggetto [**IContextNode**](icontextnode.md) da salvare è parzialmente popolato (vedere [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

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

[**Metodo IInkAnalyzer:: LoadResults**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

