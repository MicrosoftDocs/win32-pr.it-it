---
description: I predicati di profondità della cartella controllano l'ambito di una ricerca specificando un percorso e se eseguire un attraversamento profondo o superficiale.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Predicati di ambito e DIRECTORY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128547"
---
# <a name="scope-and-directory-predicates"></a><span data-ttu-id="24fa2-103">Predicati di ambito e DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="24fa2-103">SCOPE and DIRECTORY Predicates</span></span>

<span data-ttu-id="24fa2-104">I predicati di profondità della cartella controllano l'ambito di una ricerca specificando un percorso e se eseguire un attraversamento profondo o superficiale.</span><span class="sxs-lookup"><span data-stu-id="24fa2-104">Folder depth predicates control the scope of a search by specifying a path and whether to perform a deep or shallow traversal.</span></span> <span data-ttu-id="24fa2-105">Di seguito viene illustrata la sintassi dei predicati di profondità della cartella:</span><span class="sxs-lookup"><span data-stu-id="24fa2-105">The following shows the syntax of the folder depth predicates:</span></span>


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



<span data-ttu-id="24fa2-106">Il predicato è seguito da un segno di uguale.</span><span class="sxs-lookup"><span data-stu-id="24fa2-106">The predicate is followed by an equal sign.</span></span> <span data-ttu-id="24fa2-107">Il percorso è exclosed tra virgolette singole e deve iniziare con un protocollo e due punti (ad esempio,, `file:` `mapi:` o `csc:` ).</span><span class="sxs-lookup"><span data-stu-id="24fa2-107">The path is exclosed in single quotes and must begin with a protocol and a colon (for example, `file:`, `mapi:`, or `csc:`).</span></span> <span data-ttu-id="24fa2-108">Il predicato di ambito esegue un attraversamento profondo del percorso, incluse tutte le sottocartelle, mentre il predicato di DIRECTORY esegue un attraversamento superficiale della sola cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="24fa2-108">The SCOPE predicate performs a deep traversal of the path, including all subfolders, while the DIRECTORY predicate does a shallow traversal of only the folder specified.</span></span> <span data-ttu-id="24fa2-109">Analogamente ad altre restrizioni di Structured Query Language (SQL), è possibile specificare più di una restrizione di profondità di cartella in una singola query.</span><span class="sxs-lookup"><span data-stu-id="24fa2-109">Like other Structured Query Language (SQL) restrictions, you can specify more than one folder depth restriction in a single query.</span></span>

<span data-ttu-id="24fa2-110">Per eseguire una query sul catalogo locale di un computer remoto, includere il nome del computer prima del catalogo e un percorso di Universal Naming Convention (UNC) nel computer remoto nella clausola SCOPE o DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="24fa2-110">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

## <a name="examples"></a><span data-ttu-id="24fa2-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="24fa2-111">Examples</span></span>


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



<span data-ttu-id="24fa2-112">Nell'esempio primo ambito viene eseguita la ricerca \\ nella \\ cartella report C: files e in tutte le relative sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="24fa2-112">The first SCOPE example searches the C:\\Files\\Reports folder and all its subfolders.</span></span> <span data-ttu-id="24fa2-113">L'esempio di DIRECTORY Cerca solo i report cartella radice C: \\ file \\ .</span><span class="sxs-lookup"><span data-stu-id="24fa2-113">The DIRECTORY example searches only the root folder C:\\Files\\Reports.</span></span>

> [!Note]  
> <span data-ttu-id="24fa2-114">Le barre rovesciate file system ( \\ ) diventano una barra di tipo URL (talvolta denominate barre) (/).</span><span class="sxs-lookup"><span data-stu-id="24fa2-114">The file system backslashes (\\) become a URL-style slash marks (sometimes called forward slashes) (/).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="24fa2-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24fa2-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="24fa2-116">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="24fa2-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24fa2-117">Clausola FROM</span><span class="sxs-lookup"><span data-stu-id="24fa2-117">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="24fa2-118">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="24fa2-118">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



