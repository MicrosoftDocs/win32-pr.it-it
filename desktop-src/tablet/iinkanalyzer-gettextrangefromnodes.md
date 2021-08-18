---
description: Trova l'intervallo di testo nella stringa riconosciuta che corrisponde a una raccolta di oggetti IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: Metodo IInkAnalyzer::GetTextRangeFromNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 147877ef8871f7b07e2aa501a107c1e40bd75e80009e5bee97dca03346bb853a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092131"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>Metodo IInkAnalyzer::GetTextRangeFromNodes

Trova l'intervallo di testo nella stringa riconosciuta che corrisponde a una raccolta di [**oggetti IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plStart* \[ Cambio\]
</dt> <dd>

Intero con segno a 32 bit che indica l'inizio dell'intervallo di testo. Questo parametro viene passato non inizializzato.

</dd> <dt>

*plLength* \[ Cambio\]
</dt> <dd>

Intero con segno a 32 bit che indica la lunghezza dell'intervallo di testo. Questo parametro viene passato non inizializzato.

</dd> <dt>

*pNodesToSearch* \[ Pollici\]
</dt> <dd>

Raccolta di oggetti [**IContextNode**](icontextnode.md) per cui trovare l'intervallo di testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se *pNodesToSearch* contiene oggetti [**IContextNode**](icontextnode.md) non adiacenti, questo metodo restituisce l'intervallo di testo più piccolo che copre tutti **gli oggetti IContextNode.**

Questo metodo genera un'eccezione E \_ INVALIDARG quando *pNodesToSearch* contiene un [**oggetto IContextNode**](icontextnode.md) non associato a [**IInkAnalyzer.**](iinkanalyzer.md)

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
</dt> </dl>

 

 




