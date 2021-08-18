---
title: Ricerca di gruppi in base all'ambito o al tipo in un dominio
description: In Windows 2000 è disponibile una singola classe denominata gruppo per tutti gli ambiti del gruppo (dominio locale, globale, universale) e i tipi (sicurezza, distribuzione).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Ricerca di gruppi in base all'ambito o al tipo in un dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d424ce21912aa1e7fa7104099fc8359a5a1c80beeae1fc143aa0bd4aea71d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024949"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Ricerca di gruppi in base all'ambito o al tipo in un dominio

In Windows 2000 è presente una singola classe denominata [**gruppo**](/windows/desktop/ADSchema/c-group) per tutti gli ambiti di gruppo (Domain Local, Global, Universal) e i tipi (sicurezza, distribuzione). [**L'attributo groupType**](/windows/desktop/ADSchema/a-grouptype) dell'oggetto gruppo specifica il tipo di gruppo e l'ambito.

Per usare il tipo o l'ambito per cercare gruppi Windows 2000 domini, usare un filtro che contiene una regola di corrispondenza per [**l'attributo groupType.**](/windows/desktop/ADSchema/a-grouptype) Per altre informazioni sulle regole di corrispondenza, vedere [Sintassi del filtro di ricerca.](/windows/desktop/ADSI/search-filter-syntax)

Per altre informazioni e un esempio di codice che illustra come cercare gruppi in un dominio, vedere Codice di esempio per la ricerca di gruppi [in un dominio](example-code-for-performing-a-query-in-a-domain.md).

## <a name="example-ldap-query-strings"></a>Stringhe di query LDAP di esempio

Gli esempi di stringhe di query seguenti illustrano come costruire una stringa di query LDAP usata per cercare o filtrare tipi di gruppi specifici.

La stringa di query seguente consente di cercare i gruppi di sicurezza. Questo esempio usa "-2147483648" come equivalente decimale del flag **ADS \_ GROUP TYPE \_ SECURITY \_ \_ ENABLED.**


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



La stringa di query seguente consente di cercare gruppi di distribuzione universali. i gruppi che contengono il flag **ADS \_ GROUP TYPE UNIVERSAL \_ \_ \_ GROUP** e non contengono il flag **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED.** In questo esempio viene utilizzato "8" come equivalente decimale di **ADS \_ GROUP TYPE UNIVERSAL \_ \_ \_ GROUP** e "-2147483648" come equivalente decimale del flag **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED.**


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 