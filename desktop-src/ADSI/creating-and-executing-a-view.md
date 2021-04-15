---
title: Creazione ed esecuzione di una visualizzazione
description: È possibile creare una vista per i dati ottenuti da Active Directory. Tenere presente che solo la definizione della vista viene archiviata in SQL Server e non nel set di risultati effettivo. Pertanto, è possibile ottenere un risultato diverso quando si richiama la visualizzazione in un secondo momento.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47a0956acb8f9d0268240e677f62a2e395b4fed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395294"
---
# <a name="creating-and-executing-a-view"></a>Creazione ed esecuzione di una visualizzazione

È possibile creare una vista per i dati ottenuti da Active Directory. Tenere presente che solo la definizione della vista viene archiviata in SQL Server e non nel set di risultati effettivo. Pertanto, è possibile ottenere un risultato diverso quando si richiama la visualizzazione in un secondo momento.

Nell'esempio di codice seguente viene illustrato come creare una vista.


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



Usare il codice seguente per richiamare una visualizzazione.


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un join eterogeneo tra SQL Server e Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




