---
description: Modifica l'identificatore delle impostazioni locali per i tratti specificati.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: Metodo IInkAnalyzer::SetStrokesLanguageId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2a063180d89fd9f29ebcacd5b9cbd9e98e4299d82aac2328b08624e3c1557249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590341"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a>Metodo IInkAnalyzer::SetStrokesLanguageId

Modifica l'identificatore delle impostazioni locali per i tratti specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdCount* \[ Pollici\]
</dt> <dd>

Numero di identificatori di tratti in *plStrokes.*

</dd> <dt>

*plStrokes* \[ Pollici\]
</dt> <dd>

Matrice di identificatori per i tratti a cui assegnare l'identificatore delle impostazioni locali.

</dd> <dt>

*lStrokesLCID* \[ Pollici\]
</dt> <dd>

Identificatore delle impostazioni locali da assegnare ai tratti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Le impostazioni locali di un tratto vengono impostate quando si aggiunge il tratto chiamando il metodo [**IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md). Per ottenere le impostazioni locali attualmente assegnate a un tratto, chiamare il metodo [**IInkAnalyzer::GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

I tratti specificati vengono spostati in un nodo input penna non classificato (vedere [**IContextNode::GetType**](icontextnode-gettype.md)) che contiene tratti della stessa lingua. Se tale [**IContextNode**](icontextnode.md) non esiste, questo metodo crea un nuovo nodo input penna non classificato e vi sposta i tratti. Un nodo input penna non classificato è **un IContextNode** con tipo UnclassifiedInk.

Se questo metodo sposta i tratti da un [**oggetto IContextNode**](icontextnode.md) che non è un nodo input penna non classificato, questo metodo aggiunge anche i recinti di delimitazione dei tratti all'area dirty dell'analizzatore input penna (vedere [**Metodo IInkAnalyzer::GetDirtyRegion).**](iinkanalyzer-getdirtyregion.md)

Questo metodo non sposta un tratto se il *parametro lStrokeLCID* corrisponde all'identificatore della lingua corrente del tratto.

Se un tratto specificato non è associato a [**IInkAnalyzer,**](iinkanalyzer.md)questo metodo ignora l'identificatore.

Se nessuno dei tratti specificati identifica un tratto associato a [**IInkAnalyzer,**](iinkanalyzer.md)questo metodo restituisce senza aggiornare **IInkAnalyzer.**

Questo metodo restituisce un codice di errore quando strokeIds è **NULL.**

Per altre informazioni sugli identificatori di lingua, vedere Costanti e stringhe degli [identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).

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

[**Metodo IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

