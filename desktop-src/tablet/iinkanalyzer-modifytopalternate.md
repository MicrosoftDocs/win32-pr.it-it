---
description: Modifica l'oggetto alternativo superiore corrente in quello alternativo specificato e cancella il tipo di conferma per tutti gli oggetti IContextNode associati all'alternativa.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: Metodo IInkAnalyzer::ModifyTopAlternate (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b35cda4534bc5c791e4815c584f6da5d9972c018283b6c9385f6bad998187505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092041"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>Metodo IInkAnalyzer::ModifyTopAlternate

Modifica l'oggetto alternativo superiore corrente in quello alternativo specificato e cancella il tipo di conferma per tutti gli oggetti [**IContextNode**](icontextnode.md) associati all'alternativa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlternate* \[ Pollici\]
</dt> <dd>

Oggetto [**IAnalysisAlternate**](ianalysisalternate.md) contenente il nuovo oggetto alternativo superiore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Per ottenere alternative di analisi, usare il metodo [**IInkAnalyzer::GetAlternates**](iinkanalyzer-getalternates.md), il metodo [**IInkAnalyzer::GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o il metodo [**IInkAnalyzer::GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Per ottenere gli [**oggetti IContextNode associati**](icontextnode.md) a un'analisi alternativa, usare il metodo [**IAnalysisAlternate::GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

Per modificare il tipo di conferma per un nodo di contesto, usare [**IContextNode::Confirm.**](icontextnode-confirm.md)

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Tipo di conferma**](confirmationtype.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




