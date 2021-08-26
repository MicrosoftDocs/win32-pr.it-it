---
description: Recupera gli identificatori univoci globali (GUID) per le proprietà che questo IInkAnalysisRecognizer può generare per i risultati dell'analisi.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: Metodo IInkAnalysisRecognizer::GetSupportedProperties (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fce33317a234d82d6045dbefa93ed582d31d92f6ff54abe9ef87949559a5d269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057861"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>Metodo IInkAnalysisRecognizer::GetSupportedProperties

Recupera gli identificatori univoci globali (GUID) per le proprietà che questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) può generare per i risultati dell'analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulPropertiesCount* \[ in, out\]
</dt> <dd>

Numero di GUID in *ppProperties.*

</dd> <dt>

*ppProperties* \[ Cambio\]
</dt> <dd>

Puntatore ai GUID delle proprietà che questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) può generare per i risultati dell'analisi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da ppProperties quando le informazioni non \*  sono più necessarie.

 

Un riconoscitore può supportare metriche di riga, numeri di riga, livelli di confidenza e così via. Per un elenco completo delle proprietà che un sistema di riconoscimento può supportare, vedere [Costanti RecognitionProperty.](recognitionproperty-constants.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Costanti RecognitionProperty](recognitionproperty-constants.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

