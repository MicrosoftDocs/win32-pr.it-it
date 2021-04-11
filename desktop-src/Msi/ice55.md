---
description: ICE55 verifica che tutti gli oggetti LockPermission esistano e dispongano di valori di autorizzazione validi.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232856"
---
# <a name="ice55"></a>ICE55

ICE55 verifica che tutti gli oggetti LockPermission esistano e dispongano di valori di autorizzazione validi.

## <a name="result"></a>Risultato

ICE55 pubblica un errore se un LockObject elencato nella [tabella LockPermissions](lockpermissions-table.md) non esiste o se non è stato specificato alcun livello di privilegio nella colonna autorizzazione.

## <a name="example"></a>Esempio

ICE55 segnala gli errori seguenti per l'esempio.

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[Tabella LockPermissions](lockpermissions-table.md) (parziale)



| LockObject | Tabella | Dominio | User  | Autorizzazione |
|------------|-------|--------|-------|------------|
| File1      | File  |        | guest |            |
| File3      | File  |        | guest | 1          |



 

[Tabella file](file-table.md) (parziale)



| File  | Versione | Linguaggio |
|-------|---------|----------|
| File1 | File2   |          |
| File2 | 1.0.0.0 | 1033     |



 

L'oggetto file1 contiene un valore null nella colonna autorizzazione. Ogni riga deve avere un valore nella colonna autorizzazioni. Per correggere l'errore, specificare un valore numerico in questa colonna. Se non sono necessari privilegi per questo oggetto, è necessario rimuovere la riga.

L'oggetto file3 descritto nella tabella LockPermissions non è elencato nella tabella file. Per correggere l'errore, fare riferimento a un oggetto valido.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



