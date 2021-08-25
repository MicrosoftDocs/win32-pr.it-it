---
description: ICE98 verifica il campo di descrizione della tabella ODBCDataSource per un'origine dati ODBC. Usa la funzione SQLValidDSN per verificare che siano usati solo caratteri validi e che la descrizione non superi la lunghezza massima consentita.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f8a627b057e6c235fdb57a4f2d5d2b2cf6274e528ef4945c6a6323e1888427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894691"
---
# <a name="ice98"></a>ICE98

ICE98 verifica il campo di descrizione della tabella [ODBCDataSource](odbcdatasource-table.md) per un'origine dati ODBC. Usa la **funzione SQLValidDSN** per verificare che siano usati solo caratteri validi e che la descrizione non superi la lunghezza massima consentita.

## <a name="result"></a>Risultato

ICE98 invia gli avvisi seguenti.



| Avviso ICE98                    | Descrizione                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il nome dell'origine dati non è valido. | Il valore nella colonna Description della tabella [ODBCDataSource](odbcdatasource-table.md) contiene caratteri non validi o è troppo lungo, il che significa che supera il valore di SQL \_ MAX DSN LENGTH di \_ \_ 32. |



 

## <a name="example"></a>Esempio

ICE98 segnala gli avvisi seguenti per l'esempio:

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

[Tabella ODBCDataSource](odbcdatasource-table.md) (parziale)



| DataSource | Descrizione                      |
|------------|----------------------------------|
| BadChar    | !                                |
| TooLong    | <String of length > 32> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> <dt>

[Tabella ODBCDataSource](odbcdatasource-table.md)
</dt> </dl>

 

 



