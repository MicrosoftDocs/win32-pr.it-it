---
description: ICE98 verifica il campo della descrizione della tabella ODBCDataSource per un'origine dati ODBC. Usa la funzione SQLValidDSN per verificare che vengano usati solo caratteri validi e che la descrizione non superi la lunghezza massima consentita.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232072"
---
# <a name="ice98"></a>ICE98

ICE98 verifica il campo della descrizione della [tabella ODBCDataSource](odbcdatasource-table.md) per un'origine dati ODBC. Usa la funzione **SQLValidDSN** per verificare che vengano usati solo caratteri validi e che la descrizione non superi la lunghezza massima consentita.

## <a name="result"></a>Risultato

ICE98 invia gli avvisi seguenti.



| Avviso di ICE98                    | Descrizione                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il nome dell'origine dati non è valido. | Il valore nella colonna Descrizione della [tabella ODBCDataSource](odbcdatasource-table.md) contiene caratteri non validi o è troppo lungo, il che significa che supera la \_ lunghezza massima del \_ DSN SQL \_ di 32. |



 

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

[Riferimento ghiaccio](ice-reference.md)
</dt> <dt>

[Tabella ODBCDataSource](odbcdatasource-table.md)
</dt> </dl>

 

 



