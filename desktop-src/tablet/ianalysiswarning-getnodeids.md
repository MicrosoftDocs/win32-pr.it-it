---
description: Restituisce gli identificatori di tutti i nodi di contesto pertinenti associati a questo avviso.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: Metodo IAnalysisWarning::GetNodeIds (IACom.h)
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
ms.openlocfilehash: 97e6f4fde66faef14402c815f6b95517a2bd19adfb90eac4e865383770bc753f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967480"
---
# <a name="ianalysiswarninggetnodeids-method"></a>Metodo IAnalysisWarning::GetNodeIds

Restituisce gli identificatori di tutti i nodi di contesto pertinenti associati a questo avviso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulCount* \[ in, out\]
</dt> <dd>

Numero di GUID (Globally Unique Identifier) in *ppNodeIds*.

</dd> <dt>

*ppNodeIds* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di GUID che identifica i nodi di contesto associati all'avviso di analisi oppure **NULL** se nessun nodo di contesto è associato all'avviso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se *ppNodeIds viene* passato come **NULL,** il **metodo GetNodeIds** restituisce **S \_ OK** e il numero di rettangoli viene restituito in *pulCount*.

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppNodeIds* quando non sono più necessarie le informazioni.

 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come ottenere gli oggetti [**IContextNode**](icontextnode.md) presenti in [**IAnalysisWarning**](ianalysiswarning.md), e come ottenere solo il numero di `warning` oggetti **IContextNode**


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
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

