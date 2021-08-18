---
description: Modifica l'identificatore delle impostazioni locali per il tratto specificato.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: Metodo IInkAnalyzer::SetStrokeLanguageId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc91d7d8a710d2640c31e639146bd6a2fd1deac854420d7ceac1bbfdd778022c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091481"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a>Metodo IInkAnalyzer::SetStrokeLanguageId

Modifica l'identificatore delle impostazioni locali per il tratto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ Pollici\]
</dt> <dd>

Identificatore del tratto a cui assegnare l'identificatore delle impostazioni locali.

</dd> <dt>

*lStrokeLCID* \[ Pollici\]
</dt> <dd>

Identificatore delle impostazioni locali da assegnare al tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Le impostazioni locali di un tratto vengono impostate quando si aggiunge il tratto chiamando il metodo [**IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md), il metodo [**IInkAnalyzer::AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), il metodo [**IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)o il metodo [**IInkAnalyzer::AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Per ottenere le impostazioni locali attualmente assegnate a un tratto, chiamare il metodo [**IInkAnalyzer::GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

Il tratto specificato viene spostato in un nodo input penna non classificato (vedere [**IContextNode::GetType)**](icontextnode-gettype.md)che contiene tratti della stessa lingua. Se non esiste [**alcun elemento IContextNode**](icontextnode.md) di questo tipo, questo metodo crea un nuovo nodo input penna non classificato e vi sposta il tratto. Un nodo input penna non classificato è **un elemento IContextNode** di tipo UnclassifiedInk.

Se questo metodo sposta un tratto da un [**oggetto IContextNode**](icontextnode.md) che non è un nodo input penna non classificato, questo metodo aggiunge anche il rettangolo di selezione del tratto all'area dirty dell'analizzatore input penna (vedere [**Metodo IInkAnalyzer::GetDirtyRegion).**](iinkanalyzer-getdirtyregion.md)

Questo metodo non sposta un tratto se il *parametro lStrokeLCID* corrisponde all'identificatore della lingua corrente del tratto.

Se il tratto specificato non è associato a [**IInkAnalyzer,**](iinkanalyzer.md)questo metodo restituisce senza aggiornare **LInkAnalyzer.**

Per altre informazioni sugli identificatori di lingua, vedere Costanti e stringhe degli [identificatori di lingua.](/windows/desktop/Intl/language-identifier-constants-and-strings)

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

[**Metodo IInkAnalyzer::SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

