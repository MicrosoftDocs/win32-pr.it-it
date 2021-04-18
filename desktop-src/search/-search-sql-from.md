---
description: Dopo l'istruzione SELECT, si utilizza la clausola FROM per specificare dove cercare i documenti corrispondenti.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: Clausola FROM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306128"
---
# <a name="from-clause"></a>Clausola FROM

Dopo l'istruzione SELECT, si utilizza la clausola FROM per specificare dove cercare i documenti corrispondenti. Di seguito è riportata la sintassi della clausola FROM per una query locale:


```
FROM [<ComputerName>.]SystemIndex
```



Attualmente, Windows Search supporta solo un catalogo, SystemIndex. Per eseguire una query sul catalogo locale di un computer remoto, includere il nome del computer prima del catalogo e un percorso di Universal Naming Convention (UNC) nel computer remoto nella clausola SCOPE o DIRECTORY.

Un ambito viene specificato come restrizione nella clausola WHERE, come descritto nell'argomento [ambito e predicati di directory](-search-sql-folderdepth.md) .

## <a name="examples"></a>Esempio


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



Nel secondo degli esempi precedenti, la query è destinata a un computer remoto denominato "zarascomputer". Si noti che questo nome computer viene visualizzato sia nelle clausole FROM che nell'ambito. Nel terzo esempio, la query è destinata a un nome di condivisione "Users" in un server denominato "Server" (dove il percorso UNC sarà \\ \\ utenti del server \\ ).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Panoramica della sintassi SQL di ricerca](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[SELECT (istruzione)](-search-sql-select.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> <dt>

[Predicati di ambito e DIRECTORY](-search-sql-folderdepth.md)
</dt> </dl>

 

 



