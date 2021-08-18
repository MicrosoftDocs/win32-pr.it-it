---
description: Recupera le alternative di analisi per i nodi in una raccolta IContextNodes specificata.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: Metodo IInkAnalyzer::GetAlternatesForContextNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc282906bae70a28f612a8c1fd0a5a67ea1343c73f5ededf0d6c85a8bfd60aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939860"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>Metodo IInkAnalyzer::GetAlternatesForContextNodes

Recupera le alternative di analisi per i nodi in una raccolta [**IContextNodes**](icontextnodes.md) specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextNodes* \[ Pollici\]
</dt> <dd>

Raccolta [**IContextNodes**](icontextnodes.md) per cui vengono restituite le alternative di analisi.

</dd> <dt>

*ulMaximumAlternates* \[ Pollici\]
</dt> <dd>

Numero massimo di alternative da restituire.

</dd> <dt>

*ppAlternates* \[ Cambio\]
</dt> <dd>

Oggetto [**IAnalysisAlternates**](ianalysisalternates.md) contenente le alternative di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAlternates* quando non è più necessario usare l'oggetto .

 

[**L'elemento IAnalysisAlternate superiore**](ianalysisalternate.md) viene restituito come prima alternativa della raccolta.

Gli [**oggetti IContextNode**](icontextnode.md) in *pContextNodes* non devono rappresentare aree adiacenti del documento.

Per ogni hint di analisi nei nodi, [**IInkAnalyzer**](iinkanalyzer.md) restituisce solo l'alternativa superiore.

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

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAlternates**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Metodo IInkAnalyzer::ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

