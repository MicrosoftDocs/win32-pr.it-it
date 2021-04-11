---
description: Crea un nuovo nodo di riconoscimento personalizzato per IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'Metodo IInkAnalyzer:: CreateCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226159"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a>Metodo IInkAnalyzer:: CreateCustomRecognizer

Crea un nuovo nodo di riconoscimento personalizzato per [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalysisRecognizerId* \[ in\]
</dt> <dd>

Identificatore univoco globale (GUID) dell'oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) per il quale creare un nodo.

</dd> <dt>

*ppContextNode* \[ out\]
</dt> <dd>

Puntatore all'oggetto [**IContextNode**](icontextnode.md) che rappresenta il nuovo nodo di riconoscimento personalizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su ppContextNode quando non è più necessario utilizzare l'oggetto.

 

Questo metodo crea un nuovo [**IContextNode**](icontextnode.md) con un tipo di CustomRecognizer (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)). Aggiunge quindi il nuovo nodo di riconoscimento personalizzato alla raccolta dei sottonodi del nodo radice dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il metodo [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

