---
title: Ricerca di oggetti in base al nome
description: La maggior parte degli oggetti in Active Directory Domain Services utilizza la proprietà CN come attributo di denominazione.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, ricerca, per nome
- ANNUNCIO oggetto, ricerca per nome
- Ricerca di oggetti in base al nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707618"
---
# <a name="finding-objects-by-name"></a>Ricerca di oggetti in base al nome

La maggior parte degli oggetti in Active Directory Domain Services utilizza la proprietà **CN** come attributo di denominazione. Alcuni oggetti, tuttavia, utilizzano un attributo di denominazione diverso da **CN**. Un controller di dominio, ad esempio, usa la proprietà **domainDNS** per l'attributo Naming e un'unità organizzativa usa la proprietà **OrganizationalUnit** per l'attributo naming. Per evitare di dover utilizzare un attributo di denominazione diverso per diversi tipi di oggetto, è necessario utilizzare la proprietà **Name** , che contiene il nome distinto relativo dell'oggetto, per cercare gli oggetti in base al nome.

## <a name="examples"></a>Esempio

Negli esempi di codice riportati di seguito vengono illustrate stringhe di query diverse che possono essere utilizzate per trovare gli oggetti in base al nome.

La stringa di query seguente consente di trovare tutti gli oggetti con un nome che inizia con "Jeff".


```C++
(name=Jeff*)
```



La stringa di query seguente consente di trovare tutti gli oggetti computer con un nome che inizia con "Leased" o "Corp".


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



La stringa di query seguente consente di trovare tutti gli utenti e con un nome che inizia con "Karen" o "Jeff".


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




