---
title: Esecuzione di query per i gruppi in un dominio
description: I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio, nonché nella radice del dominio.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Esecuzione di query per i gruppi in un dominio AD
- Gruppi DI ACTIVE, esecuzione di query per i gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6079050519fca00a8e689d8af5c3fae9ce6baec2c02406ae56bccc3616a50bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184915"
---
# <a name="querying-for-groups-in-a-domain"></a>Esecuzione di query per i gruppi in un dominio

I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio, nonché nella radice del dominio. I gruppi potrebbero non essere sempre in un contenitore. Pertanto, è necessario cercare l'intero dominio per trovare tutti i gruppi nel dominio.

Per cercare tutti i gruppi in un dominio, impostare il punto di inizio della ricerca sulla radice del dominio, impostare l'ambito di ricerca su sottoalbero e cercare tutti gli oggetti con valore [**objectClass**](/windows/desktop/ADSchema/a-objectclass) pari a "group".

Se è necessario trovare gruppi che contengono determinati [**valori \_ \_ \_ ENUM ADS GROUP TYPE,**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) è possibile usare l'operatore DI REGOLA DI CORRISPONDENZA **LDAP BIT \_ \_ \_ \_ E** l'operatore della regola di corrispondenza per cercare gruppi con bit specifici impostati nell'attributo [**groupType.**](/windows/desktop/ADSchema/a-grouptype) Per altre informazioni sull'uso delle regole di corrispondenza, vedere [Sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).

Per altre informazioni e un esempio di codice che illustra come cercare gruppi in un dominio, vedere Codice di esempio per la ricerca di gruppi [in un dominio](example-code-for-performing-a-query-in-a-domain.md).

 

 