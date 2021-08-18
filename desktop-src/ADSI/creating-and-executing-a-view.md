---
title: Creazione ed esecuzione di una vista
description: È possibile creare una vista per i dati ottenuti da Active Directory. Tenere presente che solo la definizione della vista viene archiviata in SQL Server e non nel set di risultati effettivo. Pertanto, è possibile ottenere un risultato diverso quando si richiama la visualizzazione in un secondo momento.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c4676154ea32dd06e39498e9f943b55d8dbf39694ab9c1005e942cad85f7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082725"
---
# <a name="creating-and-executing-a-view"></a>Creazione ed esecuzione di una vista

È possibile creare una vista per i dati ottenuti da Active Directory. Tenere presente che solo la definizione della vista viene archiviata in SQL Server e non nel set di risultati effettivo. Pertanto, è possibile ottenere un risultato diverso quando si richiama la visualizzazione in un secondo momento.

Nell'esempio di codice seguente viene illustrato come creare una visualizzazione.


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

 

 




