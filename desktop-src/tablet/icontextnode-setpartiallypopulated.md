---
description: Modifica il valore che indica se questo IContextNode è parzialmente o completamente popolato.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'Metodo IContextNode:: SetPartiallyPopulated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049520"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>Metodo IContextNode:: SetPartiallyPopulated

Modifica il valore che indica se questo [**IContextNode**](icontextnode.md) è parzialmente o completamente popolato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fPartiallyPopulated* \[ in\]
</dt> <dd>

**Variante \_ TRUE** se il [**IContextNode**](icontextnode.md) è parzialmente popolato; in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Utilizzare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md). Per altre informazioni, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

Quando si virtualizza l'albero del documento, assicurarsi di impostare il valore PropertyGuidsForContextNodes. RotatedBoundingBox (utilizzando ContextNode. AddPropertyValue) in tutti gli oggetti ContextNode. La proprietà RotatedBoundingBox viene calcolata da InkAnalyzer e per impostazione predefinita deve essere in tutti gli ContextNode di scrittura. Tuttavia, se l'applicazione virtualizza i risultati dell'analisi impostando la proprietà PartiallyPopulated, durante la gestione dell'evento PopulateContextNode assicurarsi di popolare la proprietà RotatedBoundingBox. Se non si imposta la proprietà RotatedBoundingBox, è possibile che vengano usati potenzialmente più dati del documento nell'operazione di analisi corrente

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**\_IAnalysisProxyEvents::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**IContextNode:: CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




