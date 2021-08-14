---
title: Ricerca di oggetti in base al nome
description: La maggior parte degli oggetti Active Directory Domain Services la proprietà cn come attributo di denominazione.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, ricerca, in base al nome
- oggetto AD , ricerca in base al nome
- Ricerca di oggetti in base al nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60624c62e9d28d35805af3c98f551a19f44edf9e27369cf7ded9e87621491cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189181"
---
# <a name="finding-objects-by-name"></a>Ricerca di oggetti in base al nome

La maggior parte degli oggetti Active Directory Domain Services **la proprietà cn** come attributo di denominazione. Alcuni oggetti, tuttavia, usano un attributo di denominazione diverso da **cn**. Ad esempio, un controller di dominio usa la **proprietà domainDNS** per l'attributo di denominazione e un'unità organizzativa usa la proprietà **organizationalUnit** per l'attributo di denominazione. Per evitare di usare un attributo di denominazione diverso per tipi di oggetto diversi, è necessario usare la proprietà **name,** che contiene il nome distinto relativo dell'oggetto, per cercare gli oggetti in base al nome.

## <a name="examples"></a>Esempio

Gli esempi di codice seguenti illustrano stringhe di query diverse che possono essere usate per trovare oggetti in base al nome.

La stringa di query seguente trova tutti gli oggetti con un nome che inizia con "Jeff".


```C++
(name=Jeff*)
```



La stringa di query seguente trova tutti gli oggetti computer con un nome che inizia con "leased" o "corp".


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



La stringa di query seguente trova tutti gli utenti e con un nome che inizia con "Karen" o "Jeff".


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




