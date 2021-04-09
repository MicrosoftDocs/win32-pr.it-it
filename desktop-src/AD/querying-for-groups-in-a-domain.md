---
title: Esecuzione di query per i gruppi in un dominio
description: I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio e nella radice del dominio.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Esecuzione di query per i gruppi in un dominio Active Directory
- Gruppi di Active Directory, esecuzione di query per i gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872265"
---
# <a name="querying-for-groups-in-a-domain"></a>Esecuzione di query per i gruppi in un dominio

I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio e nella radice del dominio. È possibile che i gruppi non siano sempre presenti in un contenitore. Pertanto, è necessario eseguire la ricerca nell'intero dominio per trovare tutti i gruppi nel dominio.

Per cercare tutti i gruppi in un dominio, impostare il punto di inizio della ricerca sulla radice del dominio, impostare l'ambito di ricerca su sottoalbero e cercare tutti gli oggetti che hanno un valore [**objectClass**](/windows/desktop/ADSchema/a-objectclass) di "Group".

Se è necessario trovare i gruppi che contengono determinati valori di [**\_ \_ \_ enumerazione di tipo gruppo ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) , è possibile usare il **bit della regola di corrispondenza LDAP \_ \_ \_ \_ e** l'operatore della regola di corrispondenza per cercare i gruppi con determinati bit impostati nell'attributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) . Per ulteriori informazioni sull'utilizzo delle regole di corrispondenza, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire la ricerca di gruppi in un dominio, vedere il [codice di esempio per la ricerca di gruppi in un dominio](example-code-for-performing-a-query-in-a-domain.md).

 

 