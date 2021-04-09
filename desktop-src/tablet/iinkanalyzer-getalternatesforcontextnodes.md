---
description: Recupera le alternative di analisi per i nodi in una raccolta IContextNodes specificata.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'Metodo IInkAnalyzer:: GetAlternatesForContextNodes (IACom. h)'
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
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129459"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>Metodo IInkAnalyzer:: GetAlternatesForContextNodes

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

*pContextNodes* \[ in\]
</dt> <dd>

Raccolta [**IContextNodes**](icontextnodes.md) per la quale vengono restituite le alternative di analisi.

</dd> <dt>

*ulMaximumAlternates* \[ in\]
</dt> <dd>

Numero massimo di alternative da restituire.

</dd> <dt>

*ppAlternates* \[ out\]
</dt> <dd>

Oggetto [**IAnalysisAlternates**](ianalysisalternates.md) che contiene le alternative di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAlternates* quando non è più necessario utilizzare l'oggetto.

 

Il [**IAnalysisAlternate**](ianalysisalternate.md) superiore viene restituito come prima alternativa della raccolta.

Gli oggetti [**IContextNode**](icontextnode.md) in *pContextNodes* non devono necessariamente rappresentare aree adiacenti del documento.

Per ogni hint di analisi nei nodi, [**IInkAnalyzer**](iinkanalyzer.md) restituisce solo l'alternativa superiore.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: getalters**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

