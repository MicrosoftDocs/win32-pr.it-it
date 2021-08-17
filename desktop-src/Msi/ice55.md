---
description: ICE55 convalida che tutti gli oggetti LockPermission esistono e hanno valori di autorizzazione validi.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044b9993c6c50dce32c04f98d8e000f0faae4280d244c4656d7b0cbed7b49749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635142"
---
# <a name="ice55"></a>ICE55

ICE55 convalida che tutti gli oggetti LockPermission esistono e hanno valori di autorizzazione validi.

## <a name="result"></a>Risultato

ICE55 invia un errore se un LockObject elencato nella tabella [LockPermissions](lockpermissions-table.md) non esiste o se non viene specificato alcun livello di privilegio nella colonna Autorizzazione .

## <a name="example"></a>Esempio

ICE55 segnala gli errori seguenti per l'esempio.

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[Tabella LockPermissions](lockpermissions-table.md) (parziale)



| LockObject | Tabella | Dominio | Utente  | Autorizzazione |
|------------|-------|--------|-------|------------|
| File1      | File  |        | guest |            |
| File3      | File  |        | guest | 1          |



 

[Tabella file](file-table.md) (parziale)



| File  | Versione | Linguaggio |
|-------|---------|----------|
| File1 | File2   |          |
| File2 | 1.0.0.0 | 1033     |



 

L'oggetto File1 ha un valore Null nella colonna Permission. Ogni riga deve avere un valore nella colonna Autorizzazioni. Per correggere l'errore, specificare un valore numerico in questa colonna. Se non sono necessari privilegi per questo oggetto, è necessario rimuovere la riga.

L'oggetto File3 descritto nella tabella LockPermissions non è elencato nella tabella File. Per correggere l'errore, fare riferimento a un oggetto valido.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



