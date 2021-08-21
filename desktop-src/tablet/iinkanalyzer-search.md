---
description: 'Metodo IInkAnalyzer::Search: fornisce una ricerca fuzzy e senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.'
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: Metodo IInkAnalyzer::Search (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a5ebbec010d84f510d9bd2786b20fee1deaa34039720d842df77cbe0f1ca9825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091501"
---
# <a name="iinkanalyzersearch-method"></a>Metodo IInkAnalyzer::Search

Fornisce una ricerca fuzzy basata su frasi senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrPhraseToMatch* \[ Pollici\]
</dt> <dd>

Frase che verrà trovata nelle alternative per i tratti attualmente analizzati.

</dd> <dt>

*pulSearchResultCount* \[ in, out\]
</dt> <dd>

Numero massimo di risultati restituiti dalla ricerca.

</dd> <dt>

*ppulStrokeCountPerResult* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice del numero di tratti in ogni risultato della ricerca.

</dd> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Numero di ID di tratto in *ppulStrokeIds.*

</dd> <dt>

*ppulStrokeIds* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di ID tratto che rappresenta un set di tratti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Questa ricerca trova sottostringhe di più parole e singole parole. Vengono cercati sia i risultati del riconoscimento alternativo che le segmentazioni alternative.

Tutte le stringhe in ingresso verranno convertite in una singola distinzione tra maiuscole e minuscole per il confronto utilizzando l'LCID del thread corrente per eseguire questa conversione per rispettare le convenzioni relative alle maiuscole e minuscole relative alle impostazioni cultura.

La stringa passata viene considerata come una frase. Le parole e i caratteri devono essere visualizzati negli alterante per i tratti nell'ordine specificato. La prima e l'ultima parola della frase possono essere abbinate come sottostringhe (la prima parola visualizzata alla fine di un'alternativa e l'ultima parola visualizzata all'inizio della frase), ma tutte le altre parole (quelle all'interno della frase) devono essere visualizzate come parole intere.

Se la stringa passata non contiene spazi vuoti tra i caratteri, la sottostringa può essere trovata in qualsiasi punto all'interno di una singola parola in un'alternativa.

Solo la presenza o l'assenza di spazi vuoti tra i caratteri modifica i risultati della ricerca. Gli spazi vuoti non racchiusi tra caratteri vengono ignorati. Il tipo di spazio vuoto viene ignorato (una tabulazione o uno spazio tra i caratteri offrirà lo stesso risultato). La quantità di spazi vuoti non è importante: uno o due spazi tra i caratteri offriranno lo stesso risultato.

La ricerca non genera eventi PopulateContextNode. Verranno cercati solo i tratti già popolati.

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
</dt> </dl>

 

 




