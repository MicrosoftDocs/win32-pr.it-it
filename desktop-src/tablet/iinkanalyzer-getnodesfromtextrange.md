---
description: Recupera una raccolta di oggetti IContextNode che sono rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'Metodo IInkAnalyzer:: GetNodesFromTextRange (IACom. h)'
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
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751810"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>Metodo IInkAnalyzer:: GetNodesFromTextRange

Recupera una raccolta di oggetti [**IContextNode**](icontextnode.md) che sono rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.

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

*plStart* \[ in uscita\]
</dt> <dd>

Un riferimento all'inizio dell'intervallo di testo nella parte *pNodesToSearch* della stringa riconosciuta.

</dd> <dt>

*plLength* \[ in uscita\]
</dt> <dd>

Riferimento alla lunghezza dell'intervallo di testo nella parte *pNodesToSearch* della stringa riconosciuta.

</dd> <dt>

*ppContextNodes* \[ out\]
</dt> <dd>

Puntatore agli oggetti [**IContextNode**](icontextnode.md) rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.

</dd> <dt>

*pNodesToSearch* \[ in\]
</dt> <dd>

Oggetti [**IContextNode**](icontextnode.md) a cui limitare la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

L'intervallo di testo specificato deve essere relativo alla parte *pNodesToSearch* della stringa riconosciuta di [**IInkAnalyzer**](iinkanalyzer.md), anziché alla stringa riconosciuta dell'intero **IInkAnalyzer**.

Questo metodo consente di modificare i valori dei parametri *plStart* e *plLength* espandendo l'intervallo di testo ai limiti di parola più vicini.

Se, ad esempio, la stringa riconosciuta è "sono tardi" e si chiama questo metodo usando i valori di parametro 6 per *plStart* e 1 per *plLength*, che corrisponde alla lettera "a" in "late", questo metodo restituisce una raccolta che contiene un singolo [**IContextNode**](icontextnode.md), InkWord o TextWord che corrisponde alla parola "tardiva". Per questo esempio, questo metodo modifica anche il valore di *plStart* in 5 e il valore di *plLength* su 4, che corrisponde alla parola "tardiva".

> [!Note]  
> Il parametro *plStart* è relativo alla stringa riconosciuta del parametro *pNodesToSearch* .

 

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
</dt> </dl>

 

 




