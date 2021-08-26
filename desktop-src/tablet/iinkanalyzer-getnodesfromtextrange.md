---
description: Recupera una raccolta di oggetti IContextNode rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: Metodo IInkAnalyzer::GetNodesFromTextRange (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df9eb6e1e748088abaa4780aedfded4e26977018d70dd79f518159185594a90b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057821"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>Metodo IInkAnalyzer::GetNodesFromTextRange

Recupera una raccolta di [**oggetti IContextNode**](icontextnode.md) rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plStart* \[ in, out\]
</dt> <dd>

Riferimento all'inizio dell'intervallo di testo nella parte *pNodesToSearch* della stringa riconosciuta.

</dd> <dt>

*plLength* \[ in, out\]
</dt> <dd>

Riferimento alla lunghezza dell'intervallo di testo nella parte *pNodesToSearch* della stringa riconosciuta.

</dd> <dt>

*ppContextNodes* \[ Cambio\]
</dt> <dd>

Puntatore agli oggetti [**IContextNode**](icontextnode.md) rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.

</dd> <dt>

*pNodesToSearch* \[ Pollici\]
</dt> <dd>

Oggetti [**IContextNode**](icontextnode.md) a cui limitare la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

L'intervallo di testo specificato deve essere relativo alla parte *pNodesToSearch* della stringa riconosciuta di [**IInkAnalyzer**](iinkanalyzer.md)anziché alla stringa riconosciuta dell'intero **IInkAnalyzer.**

Questo metodo modifica i valori dei *parametri plStart* e *plLength* espandendo l'intervallo di testo ai limiti di parola più vicini.

Ad esempio, se la stringa riconosciuta è "I am late" e si chiama questo metodo usando i valori dei parametri 6 per *plStart* e 1 per *plLength*, che corrisponde alla lettera "a" in "late", questo metodo restituisce una raccolta contenente un singolo [**IContextNode**](icontextnode.md), InkWord o TextWord che corrisponde alla parola "late". Per questo esempio, questo metodo modifica anche il valore di *plStart* su 5 e il valore di *plLength* su 4, che corrisponde alla parola "late".

> [!Note]  
> Il *parametro plStart* è relativo alla stringa riconosciuta del *parametro pNodesToSearch.*

 

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

 

 




