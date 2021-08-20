---
description: Recupera tutti i nodi foglia.
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: Metodo IInkAnalyzer::FindLeafNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e5f97d428ea6de750e7cd94c3a5459f3d874b97c031189ad4d84f6234298a14c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043951"
---
# <a name="iinkanalyzerfindleafnodes-method"></a>Metodo IInkAnalyzer::FindLeafNodes

Recupera tutti i nodi foglia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppContextNodesFound* \[ Cambio\]
</dt> <dd>

Puntatore alla raccolta [**IContextNodes**](icontextnodes.md) contenente tutti i nodi foglia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodesFound* quando non è più necessario usare l'oggetto .

 

I nodi foglia non contengono nodi figlio. Esempi di nodi foglia input penna sono gli oggetti InkWord, TextWord, Image, InkDrawing e InkBullet [**IContextNode.**](icontextnode.md) Per altre informazioni, vedere [Tipi di nodo di contesto](context-node-types.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

