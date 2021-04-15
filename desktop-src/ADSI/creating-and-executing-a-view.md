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
# <a name="creating-and-executing-a-view"></a><span data-ttu-id="bd89f-105">Creazione ed esecuzione di una visualizzazione</span><span class="sxs-lookup"><span data-stu-id="bd89f-105">Creating and Executing a View</span></span>

<span data-ttu-id="bd89f-106">È possibile creare una vista per i dati ottenuti da Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bd89f-106">You can create a view for data obtained from Active Directory.</span></span> <span data-ttu-id="bd89f-107">Tenere presente che solo la definizione della vista viene archiviata in SQL Server e non nel set di risultati effettivo.</span><span class="sxs-lookup"><span data-stu-id="bd89f-107">Be aware that only the view definition is stored in SQL Server, and not the actual result set.</span></span> <span data-ttu-id="bd89f-108">Pertanto, è possibile ottenere un risultato diverso quando si richiama la visualizzazione in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="bd89f-108">Therefore, you may get a different result when you invoke the view at a later time.</span></span>

<span data-ttu-id="bd89f-109">Nell'esempio di codice seguente viene illustrato come creare una vista.</span><span class="sxs-lookup"><span data-stu-id="bd89f-109">The following code sample shows how to create a view.</span></span>


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



<span data-ttu-id="bd89f-110">Usare il codice seguente per richiamare una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bd89f-110">Use the following code to invoke a view.</span></span>


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a><span data-ttu-id="bd89f-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd89f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd89f-112">Creazione di un join eterogeneo tra SQL Server e Active Directory</span><span class="sxs-lookup"><span data-stu-id="bd89f-112">Creating a Heterogeneous Join between SQL Server and Active Directory</span></span>](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




