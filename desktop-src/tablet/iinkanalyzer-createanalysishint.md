---
description: Aggiunge un nuovo nodo hint di analisi con un'area infinita a IInkAnalyzer.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'Metodo IInkAnalyzer:: CreateAnalysisHint (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343706"
---
# <a name="iinkanalyzercreateanalysishint-method"></a>Metodo IInkAnalyzer:: CreateAnalysisHint

Aggiunge un nuovo nodo hint di analisi con un'area infinita a [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAnalysisHint* \[ out\]
</dt> <dd>

Nuovo nodo hint di analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md) per una descrizione dei valori restituiti.

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppAnalysisHint* quando non è più necessario utilizzare l'oggetto.

 

Per fornire informazioni di contesto aggiuntive per [**IInkAnalyzer**](iinkanalyzer.md), è possibile aggiungere hint di analisi all'analizzatore di input penna. Gli hint di analisi possono migliorare l'accuratezza del riconoscimento. Ad esempio, è possibile aggiungere il controllo e le informazioni della Guida per i campi in un'applicazione form.

Questo metodo crea un nuovo [**IContextNode**](icontextnode.md) con un tipo di nodo di contesto di AnalysisHint (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)) e aggiunge il nuovo hint come sottonodo del nodo radice dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) (vedere il metodo [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).

Per aggiungere informazioni di contesto all'hint, utilizzare [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con il parametro *pPropertyDataId* impostato su una delle costanti [proprietà hint di analisi](analysis-hint-properties.md) .

Se a un hint viene assegnata un'area infinita, denominato un hint globale, [**IInkAnalyzer**](iinkanalyzer.md) applica il contesto del suggerimento a tutti gli input penna che non si trovano all'interno dell'area di un altro hint. È possibile collegare più hint a un singolo **IInkAnalyzer**. Tuttavia, solo un hint globale può essere collegato a un singolo analizzatore di input penna e nessun hint non globale può sovrapporsi. Per ulteriori informazioni sui tipi di informazioni di contesto che possono essere forniti da un hint, vedere [proprietà hint di analisi](analysis-hint-properties.md).

L'aggiunta di un hint di analisi non contrassegna l'area dell'hint per la rianalisi. Per contrassegnare l'area all'interno dell'hint per la rianalisi, utilizzare il [**Metodo IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) per impostare l'area dirty sull'Unione dell'area e dell'area dirty correnti dell'hint di analisi.

Quando si usano gli hint per un'applicazione form, l'applicazione deve evitare di combinare il contesto del testo con l'input penna nei form. Ciò significa che, ad esempio, i nomi dei campi di testo non devono essere creati nell'albero di analisi. Gli hint hanno lo scopo di associare l'input penna alle aree nelle pagine; qualsiasi contesto del testo interferisce con questa associazione Ink-to-hint. L'operazione di analisi può unire l'input penna e il contesto del testo nella stessa area di scrittura, impedendo che l'input penna venga associato all'area dell'hint.

Per altre informazioni sull'analisi dell'input penna, vedere [Cenni preliminari sull'analisi degli input penna](ink-analysis-overview.md).

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

[**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IInkAnalyzer::D Metodo eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Proprietà hint di analisi](analysis-hint-properties.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

