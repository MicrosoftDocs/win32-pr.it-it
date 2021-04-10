---
description: Il protocollo di applicazione search-ms? è una convenzione per l'esecuzione di query sull'indice di ricerca di Windows.
ms.assetid: e8b18018-c712-4007-bb0a-af90a75780d6
title: Introduzione con argomenti di Parameter-Value
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd6e3df2ddb1d0c3f62293d3d3dc2615e855f93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225949"
---
# <a name="getting-started-with-parameter-value-arguments"></a>Introduzione con argomenti di Parameter-Value

La **ricerca-MS** ? il [protocollo applicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) è una convenzione per l'esecuzione di query sull'indice di ricerca di Windows. Il protocollo consente alle applicazioni, ad esempio Esplora risorse, di eseguire query sull'indice con argomenti di valore parametro, inclusi argomenti di proprietà, ricerche salvate in precedenza, sintassi di query avanzate (AQS), sintassi di query naturale (NQS) e identificatori del codice lingua (LCID) per l'indicizzatore e la query stessa.

Questo argomento è organizzato nel modo seguente:

- [Informazioni sugli argomenti Parameter-Value](#about-parameter-value-arguments)
- [esempi](#examples)
- [Argomenti correlati](#related-topics)

## <a name="about-parameter-value-arguments"></a>Informazioni sugli argomenti Parameter-Value

Il protocollo search-ms usa la sintassi standard codificata con URL seguente:

```
search-ms:parameter=value[&parameter=value]&
```

La sintassi inizia identificando il protocollo stesso (search-ms:). Le coppie parametro/valore sono argomenti passati al motore di ricerca, come descritto nella tabella seguente.

| Parametro                                                    | Valore                                                         | Descrizione                                                                                                                                                                                                                                                                | Versione                  |
|--------------------------------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| query                                                        | Testo con codifica URL                                              | Testo della query immesso dall'utente.                                                                                                                                                                                                                                        | Windows XP e versioni successive    |
| [InputLocale](-search-3x-wds-qryidx-localeidentifiers.md)   | Qualsiasi LCID valido                                                | Identificatore LCID che identifica la lingua di input per la query.                                                                                                                                                                                                                 | Windows XP e versioni successive    |
| [keywordlocale](-search-3x-wds-qryidx-localeidentifiers.md) | Qualsiasi LCID valido                                                | Identificatore LCID che identifica la lingua della versione internazionale dell'indicizzatore. Il valore predefinito è 1033 (en-US).                                                                                                                                                            | Windows XP e versioni successive    |
| [navigazione](-search-3x-wds-qryidx-crumb.md)                     | AQS-istruzione                                                 | Questo argomento limita l'ambito di ricerca. In Windows Vista e versioni successive, search-ms supporta AQS completi e un'implementazione speciale per un `location` argomento. In Windows XP, search-ms supporta anche AQS completi, ad eccezione di una speciale implementazione di `kind` e `store` . | Windows XP e versioni successive    |
| [sintassi](-search-3x-wds-qryidx-syntaxargument.md)           | NQS, AQS (senza distinzione tra maiuscole e minuscole)                                 | Sintassi di query da utilizzare per la ricerca nell'indice: la sintassi di query naturale o la sintassi di query avanzata (AQS). AQS è l'impostazione predefinita e viene sempre utilizzata come analizzata e supportata.                                                                                                    | Windows Vista e versioni successive |
| [stackedby](-search-3x-wds-qryidx-stackedby.md)             | Qualsiasi proprietà valida del sistema di proprietà                   | Proprietà che specifica la colonna in base alla quale eseguire lo stack dei risultati.                                                                                                                                                                                                                  | Windows Vista e versioni successive |
| [subquery](-search-3x-wds-qryidx-subquery.md)               | Percorso specificato completamente per un file di ricerca salvato ( \* . search-ms) | I risultati della sottoquery vengono utilizzati come origine per la query. Ovvero i termini della query vengono cercati in base ai risultati della sottoquery.                                                                                                                           | Windows Vista e versioni successive |
| displayname                                                  | Stringa con codifica URL                                            | Nome della ricerca corrente.                                                                                                                                                                                                                                            | Windows Vista e versioni successive |


Per informazioni correlate, vedere [la pagina relativa alla registrazione di un'applicazione in un protocollo URL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)).

## <a name="examples"></a>Esempio

```
search-ms:query=microsoft&
search-ms:query=vacation&subquery=mydepartment.search-ms&
search-ms:query=seattle&crumb=kind:pics&
search-ms:query=seattle&crumb=folder:C:\MyFolder&
```

## <a name="related-topics"></a>Argomenti correlati

[Argomenti dell'identificatore delle impostazioni locali](-search-3x-wds-qryidx-localeidentifiers.md)

[Argomento BRICIOLo](-search-3x-wds-qryidx-crumb.md)

[Argomento della sintassi](-search-3x-wds-qryidx-syntaxargument.md)

[Argomento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)

[Argomento SOTTOQUERY](-search-3x-wds-qryidx-subquery.md)
