---
description: Recupera l'oggetto IContextNode per un identificatore univoco globale (GUID) specificato.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'Metodo IInkAnalyzer:: FindNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049517"
---
# <a name="iinkanalyzerfindnode-method"></a>Metodo IInkAnalyzer:: FindNode

Recupera l'oggetto [**IContextNode**](icontextnode.md) per un identificatore univoco globale (Guid) specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PID* \[ in\]
</dt> <dd>

Identificatore per l'oggetto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*ppContextNodeFound* \[ out\]
</dt> <dd>

Puntatore all'oggetto [**IContextNode**](icontextnode.md) con l'identificatore *PID* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeFound* quando non è più necessario utilizzare l'oggetto.

 

Se tale oggetto [**IContextNode**](icontextnode.md) non esiste come discendente del nodo radice [**IInkAnalyzer**](iinkanalyzer.md) , viene restituito **null** .

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

[**Metodo IInkAnalyzer:: FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindLeafNodes**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

