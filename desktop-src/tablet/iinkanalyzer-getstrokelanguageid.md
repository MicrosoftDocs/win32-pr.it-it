---
description: Restituisce l'identificatore delle impostazioni locali del tratto specificato.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'Metodo IInkAnalyzer:: GetStrokeLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751802"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>Metodo IInkAnalyzer:: GetStrokeLanguageId

Restituisce l'identificatore delle impostazioni locali del tratto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ in\]
</dt> <dd>

Identificatore del tratto.

</dd> <dt>

*lStrokeLCID* \[ out\]
</dt> <dd>

Identificatore delle impostazioni locali per il tratto specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Le impostazioni locali del tratto vengono impostate quando si aggiunge il tratto chiamando il metodo [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), [**IInkAnalyzer:: AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes Method**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md). Per modificare le impostazioni locali del tratto, usare il metodo [**IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) o [**IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).

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

[**Metodo IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




