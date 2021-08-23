---
description: Salva i risultati dell'analisi per una raccolta di nodi di contesto specifica associata a un IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: Metodo IInkAnalyzer::SaveResultsForNodes (IACom.h)
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
ms.openlocfilehash: 4386f9b051bf1cfcda6ee55d7b83728b096dc6f69de4d87745ce564f19249565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091570"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>Metodo IInkAnalyzer::SaveResultsForNodes

Salva i risultati dell'analisi per una raccolta di nodi di contesto specifica associata a [**un oggetto IInkAnalyzer.**](iinkanalyzer.md)

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

*pContextNodes* \[ Pollici\]
</dt> <dd>

Raccolta [**IContextNode**](icontextnode.md) per cui salvare i risultati dell'analisi.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Numero di byte in *ppbSerializedData.*

</dd> <dt>

*ppbSerializedData* \[ Cambio\]
</dt> <dd>

Puntatore ai dati di analisi serializzati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) su \* *ppbSerializedData* quando le informazioni non sono più necessarie.

 

Questo metodo salva i risultati dell'analisi corrente per gli oggetti [**IContextNode**](icontextnode.md) in *pContextNodes* e tutti i relativi nodi di contesto predecessore e discendente. Questo metodo non salva i dati del tratto. È responsabilità dell'applicazione sincronizzare i risultati dell'analisi e i dati dei tratti corrispondenti, se vengono mantenuti.

Se [**l'oggetto IContextNode**](icontextnode.md) da salvare è popolato solo parzialmente, questo metodo restituisce un codice di errore (vedere [**IContextNode::GetPartiallyPopulated).**](icontextnode-getpartiallypopulated.md)

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

[**Metodo IInkAnalyzer::LoadResults**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResults**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

