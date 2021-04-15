---
description: Restituisce gli identificatori di qualsiasi nodo di contesto pertinente associato a questo avviso.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'Metodo IAnalysisWarning:: GetNodeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526539"
---
# <a name="ianalysiswarninggetnodeids-method"></a>Metodo IAnalysisWarning:: GetNodeIds

Restituisce gli identificatori di qualsiasi nodo di contesto pertinente associato a questo avviso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulCount* \[ in uscita\]
</dt> <dd>

Il numero di identificatori univoci globali (GUID) in *ppNodeIds*.

</dd> <dt>

*ppNodeIds* \[ out\]
</dt> <dd>

Puntatore a una matrice di GUID che identifica i nodi di contesto associati a questo avviso di analisi oppure **null** se all'avviso non è associato alcun nodo di contesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se *ppNodeIds* viene passato come **null**, il metodo **GetNodeIds** restituisce **S \_ OK** e viene restituito il numero di rettangoli in *pulCount*.

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppNodeIds* quando le informazioni non sono più necessarie.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come ottenere gli oggetti [**IContextNode**](icontextnode.md) presenti in [**IAnalysisWarning**](ianalysiswarning.md), `warning` e come ottenere solo il numero di oggetti **IContextNode**


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

