---
description: Modifica l'identificatore delle impostazioni locali per i tratti specificati.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'Metodo IInkAnalyzer:: SetStrokesLanguageId (IACom. h)'
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
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307374"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a>Metodo IInkAnalyzer:: SetStrokesLanguageId

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

*ulStrokeIdCount* \[ in\]
</dt> <dd>

Il numero di identificatori di tratto in *plStrokes*.

</dd> <dt>

*plStrokes* \[ in\]
</dt> <dd>

Matrice di identificatori per i tratti a cui assegnare l'identificatore delle impostazioni locali.

</dd> <dt>

*lStrokesLCID* \[ in\]
</dt> <dd>

Identificatore delle impostazioni locali da assegnare ai tratti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Le impostazioni locali di un tratto vengono impostate quando si aggiunge il tratto chiamando il metodo [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), [**IInkAnalyzer:: AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Per ottenere le impostazioni locali attualmente assegnate a un tratto, chiamare il [**Metodo IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

I tratti specificati vengono spostati in un nodo Ink non classificato (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)) che contiene i tratti della stessa lingua. Se non esiste alcun [**IContextNode**](icontextnode.md) di questo tipo, questo metodo crea un nuovo nodo di input penna non classificato e lo sposta. Un nodo Ink non classificato è un **IContextNode** di tipo UnclassifiedInk.

Se questo metodo sposta i tratti da un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato, questo metodo aggiunge anche i rettangoli di delimitazione dei tratti all'area dirty dell'analizzatore dell'input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Questo metodo non sposta un tratto se il parametro *lStrokeLCID* corrisponde all'identificatore di lingua corrente del tratto.

Se un tratto specificato non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo ignora l'identificatore.

Se nessuno dei tratti specificati identifica un tratto associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare **IInkAnalyzer**.

Questo metodo restituisce un codice di errore quando strokeIds è **null**.

Per altre informazioni sugli identificatori di lingua, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).

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

[**Metodo IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

