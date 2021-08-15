---
description: Salva tutti i risultati dell'analisi per un IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: Metodo IInkAnalyzer::SaveResults (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 216f238776cf88a24d10f57671aa4f03c71d07962ff480d5b219653a5c9d338e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091991"
---
# <a name="iinkanalyzersaveresults-method"></a>Metodo IInkAnalyzer::SaveResults

Salva tutti i risultati dell'analisi per [**un oggetto IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulSerializedDataSize* \[ Cambio\]
</dt> <dd>

Numero di byte in *ppbSerializedData.*

</dd> <dt>

*ppbSerializedData* \[ Cambio\]
</dt> <dd>

Matrice contenente i risultati dell'analisi salvati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppbSerializedData* quando le informazioni non sono più necessarie.

 

Questo metodo salva tutti i risultati dell'analisi corrente, che includono l'hint per l'analisi corrente e i nodi del riconoscitore personalizzato (vedere [**IContextNode::GetType).**](icontextnode-gettype.md) Questo metodo non salva i dati del tratto. È responsabilità dell'applicazione sincronizzare i risultati dell'analisi e i tratti corrispondenti se i dati vengono mantenuti.

Questo metodo restituisce un codice di errore quando un [**oggetto IContextNode**](icontextnode.md) da salvare è parzialmente popolato (vedere [**IContextNode::GetPartiallyPopulated).**](icontextnode-getpartiallypopulated.md)

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

[**Metodo IInkAnalyzer::LoadResults**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

