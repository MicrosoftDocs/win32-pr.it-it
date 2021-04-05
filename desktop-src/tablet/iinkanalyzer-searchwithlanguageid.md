---
description: Fornisce una ricerca basata su frasi fuzzy senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: 'Metodo IInkAnalyzer:: SearchWithLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 829878a6fd326abb8a685b644cfc222ba6921385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751794"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a>Metodo IInkAnalyzer:: SearchWithLanguageId

Fornisce una ricerca basata su frasi fuzzy senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrPhraseToMatch* \[ in\]
</dt> <dd>

Frase che verrà trovata nelle alternative per i tratti attualmente analizzati.

</dd> <dt>

*lSearchStringLanguageId* \[ in\]
</dt> <dd>

Identificatore LCID associato alla stringa passata. Utilizzato per convertire internamente il case per supportare i confronti senza distinzione tra maiuscole e minuscole.

</dd> <dt>

*pulSearchResultCount* \[ in uscita\]
</dt> <dd>

Numero massimo di risultati restituiti dalla ricerca.

</dd> <dt>

*ppulStrokeCountPerResult* \[ out\]
</dt> <dd>

Puntatore a una matrice del numero di tratti in ogni risultato della ricerca.

</dd> <dt>

*pulStrokeIdsCount* \[ in uscita\]
</dt> <dd>

Numero di ID tratto in *ppulStrokeIds*.

</dd> <dt>

*ppulStrokeIds* \[ out\]
</dt> <dd>

Puntatore a una matrice di ID tratto che rappresenta un set di set di tratti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Questa ricerca trova le sottostringhe con più parole e singole parole. Viene eseguita la ricerca sia di risultati di riconoscimento alternativi che di segmentazioni alternative.

Tutte le stringhe in ingresso verranno convertite in una singola combinazione di maiuscole e minuscole per il confronto utilizzando l'identificatore LCID del thread corrente per eseguire questa conversione per rispettare le convenzioni dei case culturali.

La stringa passata viene considerata come una frase. Le parole e i caratteri devono essere visualizzati in alterantes per i tratti nell'ordine specificato. La prima e l'ultima parola della frase possono corrispondere a sottostringhe (la prima parola che viene visualizzata alla fine di un'alternativa e l'ultima parola in corrispondenza della begginging di uno), ma tutte le altre parole (quelle all'interno della frase) devono apparire come parole intere.

Se la stringa passata non ha spazi vuoti tra i caratteri, la sottostringa può trovarsi in qualsiasi punto all'interno di una singola parola in un'alternativa.

Solo la presenza o l'assenza di spazi vuoti tra i caratteri modifica i risultati della ricerca. Lo spazio vuoto non racchiuso tra caratteri viene ignorato. Il tipo dello spazio vuoto viene ignorato (una scheda o uno spazio tra i caratteri fornirà lo stesso risultato). La quantità di spazio vuoto non è rilevante. uno spazio o due spazi tra i caratteri restituiranno lo stesso risultato.

La ricerca non genera eventi PopulateContextNode. Verranno cercati solo i tratti già popolati.

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

 

 




