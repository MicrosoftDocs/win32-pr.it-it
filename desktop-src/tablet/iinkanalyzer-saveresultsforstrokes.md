---
description: Salva i risultati dell'analisi per i tratti specificati associati a un oggetto IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: Metodo IInkAnalyzer::SaveResultsForStrokes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fd9a95ada1385fdbb6dbc5a1e22cde0ef319156ad7c3cd7782e911d06696af37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091561"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>Metodo IInkAnalyzer::SaveResultsForStrokes

Salva i risultati dell'analisi per i tratti specificati associati a [**un oggetto IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ Pollici\]
</dt> <dd>

Numero di identificatori di tratti in **plStrokeIds.**

</dd> <dt>

*plStrokeIds* \[ Pollici\]
</dt> <dd>

Matrice di identificatori di tratti.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Numero di byte in *ppbSerializedData.*

</dd> <dt>

*ppbSerializedData* \[ out, retval\]
</dt> <dd>

Puntatore ai dati di analisi serializzati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) su \* *ppbSerializedData* quando non sono più necessarie le informazioni.

 

Questo metodo salva i risultati dell'analisi corrente per i tratti specificati. Questo metodo salva gli oggetti [**IContextNode**](icontextnode.md) foglia input penna contenenti i tratti e tutti i predecessori di tali nodi di contesto. Questo metodo non salva i dati del tratto o i nodi hint di analisi. È responsabilità dell'applicazione sincronizzare i risultati dell'analisi e i dati dei tratti corrispondenti, se vengono mantenuti.

Questo metodo restituisce un codice di errore quando un [**oggetto IContextNode**](icontextnode.md) da salvare viene popolato parzialmente (vedere [**IContextNode::GetPartiallyPopulated).**](icontextnode-getpartiallypopulated.md)

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

[**Metodo IInkAnalyzer::LoadResults**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResults**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

