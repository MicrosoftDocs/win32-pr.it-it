---
description: Recupera tutti gli oggetti IContextNode dell'hint di analisi associati a IInkAnalyzer e con il nome specificato.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: Metodo IInkAnalyzer::GetAnalysisHintsByName (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 24c69cd1dd321b5f142fe07b7463941fc0944a2206f1f8d6baf0ebbe8459b6ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719193"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a>Metodo IInkAnalyzer::GetAnalysisHintsByName

Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) dell'hint di analisi associati a [**IInkAnalyzer**](iinkanalyzer.md) e con il nome specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hintName* \[ Pollici\]
</dt> <dd>

Nome dell'hint per il quale eseguire la ricerca.

</dd> <dt>

*ppAnalysisHints* \[ Cambio\]
</dt> <dd>

Gli oggetti [**IContextNode**](icontextnode.md) dell'hint di analisi in [**IInkAnalyzer**](iinkanalyzer.md) con il nome specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input](classes-and-interfaces---ink-analysis.md) penna.

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAnalysisHints* quando non è più necessario usare l'oggetto .

 

Questo metodo restituisce una raccolta vuota se tali nodi hint di analisi non sono collegati a [**IInkAnalyzer.**](iinkanalyzer.md)

Un nodo hint di analisi è [**un IContextNode**](icontextnode.md) con un tipo di nodo di contesto AnalysisHint (vedere [**IContextNode::GetType**](icontextnode-gettype.md) e [Tipi di nodo di contesto).](context-node-types.md)

Per aggiungere informazioni di contesto all'hint, usare [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) con il *parametro pPropertyDataId* impostato su [](analysis-hint-properties.md) uno degli identificatori univoci globali (GUID) nelle costanti di Proprietà hint di analisi.

Per trovare i valori delle proprietà impostati in un nodo di contesto, usare [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md). Per trovare il valore di una proprietà, usare [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Metodo IInkAnalyzer::CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Metodo IInkAnalyzer::D eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

