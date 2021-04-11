---
description: Salva i risultati dell'analisi per una raccolta di nodi di contesto specifica associata a un IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'Metodo IInkAnalyzer:: SaveResultsForNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129443"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>Metodo IInkAnalyzer:: SaveResultsForNodes

Salva i risultati dell'analisi per una raccolta di nodi di contesto specifica associata a un [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextNodes* \[ in\]
</dt> <dd>

Raccolta [**IContextNode**](icontextnode.md) per cui salvare i risultati dell'analisi.

</dd> <dt>

*pulSerializedDataSize* \[ in uscita\]
</dt> <dd>

Numero di byte in *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ out\]
</dt> <dd>

Puntatore ai dati di analisi serializzati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) su \* *ppbSerializedData* quando le informazioni non sono più necessarie.

 

Questo metodo consente di salvare i risultati di analisi correnti per gli oggetti [**IContextNode**](icontextnode.md) in *pContextNodes* e tutti i relativi nodi di contesto predecessore e discendente. Questo metodo non salva i dati del tratto. È responsabilità dell'applicazione sincronizzare i risultati dell'analisi e i dati di Stroke corrispondenti, se il problema è permanente.

Se l'oggetto [**IContextNode**](icontextnode.md) da salvare è solo parzialmente popolato, questo metodo restituisce un codice di errore (vedere [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

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

[**Metodo IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

