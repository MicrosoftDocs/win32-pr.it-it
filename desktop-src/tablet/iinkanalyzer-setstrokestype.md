---
description: Modifica il tipo dei tratti specificati.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'Metodo IInkAnalyzer:: SetStrokesType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307373"
---
# <a name="iinkanalyzersetstrokestype-method"></a>Metodo IInkAnalyzer:: SetStrokesType

Modifica il tipo dei tratti specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strokeIdCount* \[ in\]
</dt> <dd>

Il numero di identificatori di tratto in *plStrokes*.

</dd> <dt>

*plStrokes* \[ in\]
</dt> <dd>

Matrice contenente gli identificatori di tratto dei tratti a cui assegnare *StrokeType*.

</dd> <dt>

*StrokeType* \[ in\]
</dt> <dd>

Valore [**StrokeType**](stroketype.md) da assegnare ai tratti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se il tipo del tratto è il [](stroketype.md) valore StrokeType **StrokeType \_ unclassifiedd**, [**IInkAnalyzer**](iinkanalyzer.md) classifica il tratto durante l'analisi dell'input penna. In caso contrario, **IInkAnalyzer** usa il tipo impostato sul tratto.

[**IInkAnalyzer**](iinkanalyzer.md) non imposta il valore del tipo di tratto come parte dell'analisi dell'input penna. Per specificare o modificare il tipo di tratto, usare il metodo [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o **IInkAnalyzer:: SetStrokesType**.

Se un tratto è associato a un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)), questo metodo sposta il tratto in un nodo Ink non classificato che contiene tratti della stessa lingua. Se non esiste alcun nodo di contesto di questo tipo, questo metodo consente di creare un nuovo nodo Ink non classificato e di aggiungervi il tratto. Un nodo Ink non classificato è un **IContextNode** di tipo UnclassifiedInk.

Se questo metodo sposta un tratto da un [**IContextNode**](icontextnode.md) che non è un nodo di input penna non classificato, questo metodo aggiunge anche il rettangolo di delimitazione del tratto all'area dirty dell'analizzatore dell'input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Questo metodo non sposta un tratto se il parametro *StrokeType* corrisponde al tipo corrente del tratto.

Se un tratto identificato in *strokeIds* non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo ignora l'identificatore.

Se nessuno dei tratti specificati identifica un tratto associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare **IInkAnalyzer**.

Impostando il tipo di tratto sui tratti associati a un oggetto ContextNode con NodeTypeAndProperties confermato, verrà generata un'eccezione InvalidOperationException.

Questo metodo restituisce un codice di errore quando *plStrokes* è **null**.

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

[**Metodo IInkAnalyzer:: GetStrokeType**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




