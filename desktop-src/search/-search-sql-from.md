---
description: Dopo l'istruzione SELECT, si usa la clausola FROM per specificare dove cercare i documenti corrispondenti.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: Clausola FROM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6231244df2a2ec8753950ccb1a7d046c3510eff6582215d0aa3d71ebc127e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863397"
---
# <a name="from-clause"></a>Clausola FROM

Dopo l'istruzione SELECT, si usa la clausola FROM per specificare dove cercare i documenti corrispondenti. Di seguito è riportata la sintassi della clausola FROM per una query locale:


```
FROM [<ComputerName>.]SystemIndex
```



Attualmente, Windows ricerca supporta un solo catalogo, SystemIndex. Per eseguire una query sul catalogo locale di un computer remoto, includere il nome del computer prima del catalogo e un percorso Universal Naming Convention (UNC) nel computer remoto nella clausola SCOPE o DIRECTORY.

Specificare un ambito come restrizione nella clausola WHERE, come descritto [nell'argomento Predicati SCOPE e DIRECTORY.](-search-sql-folderdepth.md)

## <a name="examples"></a>Esempio


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



Nel secondo degli esempi precedenti la query è destinata a un computer remoto denominato "zarascomputer". Si noti che il nome del computer viene visualizzato nelle clausole FROM e SCOPE. Nel terzo esempio, la query è destinata a un nome di condivisione "users" in un server denominato "server" (dove il percorso UNC sarebbe utenti \\ \\ del \\ server).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Panoramica della sintassi SQL ricerca](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[Istruzione SELECT](-search-sql-select.md)
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> <dt>

[Predicati SCOPE e DIRECTORY](-search-sql-folderdepth.md)
</dt> </dl>

 

 



