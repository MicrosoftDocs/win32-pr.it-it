---
title: Ricerca di gruppi in base all'ambito o al tipo in un dominio
description: Nei domini di Windows 2000 è presente una singola classe denominata Group per tutti gli ambiti di gruppo (dominio locale, globale, universale) e tipi (sicurezza, distribuzione).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Ricerca di gruppi in base all'ambito o al tipo in un dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724426"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Ricerca di gruppi in base all'ambito o al tipo in un dominio

Nei domini di Windows 2000 è presente una singola classe denominata [**Group**](/windows/desktop/ADSchema/c-group) per tutti gli ambiti di gruppo (dominio locale, globale, universale) e tipi (sicurezza, distribuzione). L'attributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) dell'oggetto Group specifica il tipo e l'ambito del gruppo.

Per utilizzare il tipo o l'ambito per la ricerca di gruppi in domini Windows 2000, utilizzare un filtro che contenga una regola di corrispondenza per l'attributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) . Per altre informazioni sulle regole di corrispondenza, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire la ricerca di gruppi in un dominio, vedere il [codice di esempio per la ricerca di gruppi in un dominio](example-code-for-performing-a-query-in-a-domain.md).

## <a name="example-ldap-query-strings"></a>Stringhe di query LDAP di esempio

Negli esempi di stringhe di query seguenti viene illustrato come costruire una stringa di query LDAP utilizzata per cercare o filtrare tipi di gruppo specifici.

Nella stringa di query seguente vengono cercati i gruppi di sicurezza. Questo esempio USA "-2147483648" come equivalente decimale del flag di **\_ sicurezza del tipo di gruppo \_ \_ \_ ADS** .


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



La stringa di query seguente cerca i gruppi di distribuzione universali; ovvero i gruppi che contengono il **tipo di gruppo ADS flag di \_ \_ \_ \_ gruppo universale** e non contengono il flag del **tipo di gruppo Ads \_ \_ \_ \_ abilitato** per la sicurezza. In questo esempio viene usato "8" come equivalente decimale del **tipo di gruppo ADS di gruppo \_ \_ \_ universale \_** e "-2147483648" come equivalente decimale del flag per la sicurezza del **tipo di \_ gruppo \_ \_ \_ ADS** .


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 