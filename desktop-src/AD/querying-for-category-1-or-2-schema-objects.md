---
title: Esecuzione di query per gli oggetti dello schema Category 1 o 2
description: L'attributo systemFlags degli oggetti attributeSchema e classSchema è una maschera di tipo integer che contiene flag che indicano le qualità di sistema aggiuntive dell'attributo o della classe.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Esecuzione di query per la categoria 1 o 2 oggetti dello schema AD
- oggetto AD, esecuzione di query per gli oggetti dello schema di categoria 1 o 2
- ANNUNCIO dello schema, esecuzione di query per gli oggetti dello schema di categoria 1 o 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336790"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>Esecuzione di query per gli oggetti dello schema Category 1 o 2

L'attributo **systemFlags** degli oggetti **attributeSchema** e **classSchema** è una maschera di tipo integer che contiene flag che indicano le qualità di sistema aggiuntive dell'attributo o della classe. L'enumerazione [**Ads \_ SYSTEMFLAG \_ enum**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contiene valori che corrispondono ai bit che è possibile impostare nell'attributo **systemFlags** . Sono presenti altri bit **systemFlags** che non è possibile impostare, ad esempio il bit 0x10 che indica se l'attributo o la classe è la categoria 1 o la categoria 2. Il bit 0x10 è impostato per gli oggetti di categoria 1, ovvero le classi e gli attributi inclusi nello schema di base incluso nel sistema. Il bit non è impostato per le classi e gli attributi della categoria 2, che sono estensioni dello schema. Se non esiste alcuna proprietà **systemFlags** in un oggetto **attributeSchema** o **classSchema** , è la categoria 2.

Il **\_ bit della regola di corrispondenza LDAP \_ \_ \_ e** la regola di corrispondenza possono essere usati per cercare gli oggetti con il flag 0x10 impostato nell'attributo **systemFlags** . Per altre informazioni, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).

## <a name="querying-for-category-1"></a>Esecuzione di query per la categoria 1

La stringa di query seguente cerca gli attributi di categoria 1 (oggetti **attributeSchema** con il bit 0x10 impostato nella proprietà **systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



Tenere presente che, nell'esempio precedente, la sintassi della query LDAP richiede valori decimali. Pertanto, il valore esadecimale del flag deve essere convertito in Decimal. In questo caso, la categoria 1 bit è 0x10, quindi il valore del filtro deve essere specificato come 16.

## <a name="querying-for-category-2"></a>Esecuzione di query per la categoria 2

La stringa di query seguente cerca gli attributi di categoria 2 (oggetti **attributeSchema** per i quali non è impostato il bit 0x10 nella proprietà **systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



Tenere presente che questa query restituisce anche oggetti **attributeSchema** che non dispongono di una proprietà **systemFlags** e, pertanto, non hanno il flag specificato impostato.

 

 