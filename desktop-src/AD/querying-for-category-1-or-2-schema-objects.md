---
title: Esecuzione di query per oggetti dello schema di categoria 1 o 2
description: L'attributo systemFlags degli oggetti attributeSchema e classSchema è una maschera di bit integer che contiene flag che indicano qualità di sistema aggiuntive dell'attributo o della classe.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Esecuzione di query per oggetti dello schema di categoria 1 o 2 AD
- oggetto AD, esecuzione di query per oggetti dello schema di categoria 1 o 2
- schema AD, esecuzione di query per oggetti dello schema di categoria 1 o 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f934ba0401c7d782706e1e853819ba935c1315a267c668614878ec41045f63b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025349"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>Esecuzione di query per oggetti dello schema di categoria 1 o 2

**L'attributo systemFlags** degli **oggetti attributeSchema** e **classSchema** è una maschera di bit integer che contiene flag che indicano qualità di sistema aggiuntive dell'attributo o della classe. [**L'enumerazione ADS \_ SYSTEMFLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contiene valori che corrispondono ai bit che è possibile impostare nell'attributo **systemFlags.** Esistono altri bit **systemFlags** che non è possibile impostare, ad esempio il bit 0x10 che indica se l'attributo o la classe è di categoria 1 o categoria 2. Il 0x10 bit è impostato per gli oggetti di categoria 1, ovvero le classi e gli attributi inclusi nello schema di base incluso nel sistema. Il bit non è impostato per gli attributi e le classi di categoria 2, che sono estensioni dello schema. Se non **esiste alcuna proprietà systemFlags** in **un oggetto attributeSchema** o **classSchema,** è di categoria 2.

La regola di corrispondenza **LDAP MATCHING RULE BIT \_ \_ \_ \_ AND** può essere usata per cercare gli oggetti con il flag 0x10 impostato nell'attributo **systemFlags.** Per altre informazioni, vedere [Sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).

## <a name="querying-for-category-1"></a>Esecuzione di query per la categoria 1

La stringa di query seguente cerca gli attributi di categoria 1 (**oggetti attributeSchema** con 0x10 bit impostato nella **proprietà systemFlags.**


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



Tenere presente che, nell'esempio precedente, la sintassi della query LDAP richiede valori decimali. Pertanto, il valore esadecimale del flag deve essere convertito in decimal. In questo caso, la categoria 1 bit 0x10 quindi il valore del filtro deve essere specificato come 16.

## <a name="querying-for-category-2"></a>Esecuzione di query per la categoria 2

La stringa di query seguente cerca gli attributi di categoria 2 (**oggetti attributeSchema** che non hanno il bit 0x10 impostato nella **proprietà systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



Tenere presente che questa query restituisce anche oggetti **attributeSchema** che non dispongono di una proprietà **systemFlags** e, pertanto, in modo implicito non è impostato il flag specificato.

 

 