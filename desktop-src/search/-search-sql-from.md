---
description: Dopo l'istruzione SELECT, si utilizza la clausola FROM per specificare dove cercare i documenti corrispondenti.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: Clausola FROM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306128"
---
# <a name="from-clause"></a><span data-ttu-id="bfe25-103">Clausola FROM</span><span class="sxs-lookup"><span data-stu-id="bfe25-103">FROM Clause</span></span>

<span data-ttu-id="bfe25-104">Dopo l'istruzione SELECT, si utilizza la clausola FROM per specificare dove cercare i documenti corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="bfe25-104">Following the SELECT statement, you use the FROM clause to specify where to search for matching documents.</span></span> <span data-ttu-id="bfe25-105">Di seguito è riportata la sintassi della clausola FROM per una query locale:</span><span class="sxs-lookup"><span data-stu-id="bfe25-105">The following is the syntax of the FROM clause for a local query:</span></span>


```
FROM [<ComputerName>.]SystemIndex
```



<span data-ttu-id="bfe25-106">Attualmente, Windows Search supporta solo un catalogo, SystemIndex.</span><span class="sxs-lookup"><span data-stu-id="bfe25-106">Currently, Windows Search supports only one catalog, SystemIndex.</span></span> <span data-ttu-id="bfe25-107">Per eseguire una query sul catalogo locale di un computer remoto, includere il nome del computer prima del catalogo e un percorso di Universal Naming Convention (UNC) nel computer remoto nella clausola SCOPE o DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="bfe25-107">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

<span data-ttu-id="bfe25-108">Un ambito viene specificato come restrizione nella clausola WHERE, come descritto nell'argomento [ambito e predicati di directory](-search-sql-folderdepth.md) .</span><span class="sxs-lookup"><span data-stu-id="bfe25-108">You specify a scope as a restriction in the WHERE clause, as described in the [SCOPE and DIRECTORY Predicates](-search-sql-folderdepth.md) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="bfe25-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="bfe25-109">Examples</span></span>


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



<span data-ttu-id="bfe25-110">Nel secondo degli esempi precedenti, la query è destinata a un computer remoto denominato "zarascomputer".</span><span class="sxs-lookup"><span data-stu-id="bfe25-110">In the second of the preceding examples, the query targets a remote computer called "zarascomputer".</span></span> <span data-ttu-id="bfe25-111">Si noti che questo nome computer viene visualizzato sia nelle clausole FROM che nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="bfe25-111">Notice that this computer name appears in both the FROM and SCOPE clauses.</span></span> <span data-ttu-id="bfe25-112">Nel terzo esempio, la query è destinata a un nome di condivisione "Users" in un server denominato "Server" (dove il percorso UNC sarà \\ \\ utenti del server \\ ).</span><span class="sxs-lookup"><span data-stu-id="bfe25-112">In the third example, the query targets a share name "users" on a server named "server" (where the UNC path would be \\\\server\\users).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfe25-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfe25-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bfe25-114">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bfe25-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bfe25-115">Panoramica della sintassi SQL di ricerca</span><span class="sxs-lookup"><span data-stu-id="bfe25-115">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="bfe25-116">SELECT (istruzione)</span><span class="sxs-lookup"><span data-stu-id="bfe25-116">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

[<span data-ttu-id="bfe25-117">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="bfe25-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="bfe25-118">Predicati di ambito e DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="bfe25-118">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> </dl>

 

 



