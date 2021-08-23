---
description: Recupera il valore che indica se un oggetto IContextNode è parzialmente popolato o completamente popolato.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: Metodo IContextNode::GetPartiallyPopulated (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2fab5b5fce4d87c32fb3435fdad2cfc6b126069b40c7e5c7c2fb302ee468e480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773801"
---
# <a name="icontextnodegetpartiallypopulated-method"></a>Metodo IContextNode::GetPartiallyPopulated

Recupera il valore che indica se un oggetto [**IContextNode**](icontextnode.md) è parzialmente popolato o completamente popolato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfPartiallyPopulated* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se questo [**oggetto IContextNode**](icontextnode.md) non contiene dati completi. in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Usare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer.**](iinkanalyzer.md) Per altre informazioni, vedere [Proxy dati con analisi input penna.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**\_IAnalysisProxyEvents::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




