---
description: Un collegamento simbolico è un oggetto di file System che punta a un altro oggetto file system. L'oggetto a cui si fa riferimento è denominato destinazione.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Collegamenti simbolici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316766"
---
# <a name="symbolic-links"></a><span data-ttu-id="05a64-104">Collegamenti simbolici</span><span class="sxs-lookup"><span data-stu-id="05a64-104">Symbolic Links</span></span>

<span data-ttu-id="05a64-105">Un collegamento simbolico è un oggetto di file System che punta a un altro oggetto file system.</span><span class="sxs-lookup"><span data-stu-id="05a64-105">A symbolic link is a file-system object that points to another file system object.</span></span> <span data-ttu-id="05a64-106">L'oggetto a cui si fa riferimento è denominato destinazione.</span><span class="sxs-lookup"><span data-stu-id="05a64-106">The object being pointed to is called the target.</span></span>

<span data-ttu-id="05a64-107">I collegamenti simbolici sono trasparenti per gli utenti. i collegamenti vengono visualizzati come normali file o directory e possono essere utilizzati dall'utente o dall'applicazione esattamente allo stesso modo.</span><span class="sxs-lookup"><span data-stu-id="05a64-107">Symbolic links are transparent to users; the links appear as normal files or directories, and can be acted upon by the user or application in exactly the same manner.</span></span>

<span data-ttu-id="05a64-108">I collegamenti simbolici sono progettati per facilitare la migrazione e la compatibilità delle applicazioni con i sistemi operativi UNIX.</span><span class="sxs-lookup"><span data-stu-id="05a64-108">Symbolic links are designed to aid in migration and application compatibility with UNIX operating systems.</span></span> <span data-ttu-id="05a64-109">Microsoft ha implementato i collegamenti simbolici per funzionare esattamente come i collegamenti UNIX.</span><span class="sxs-lookup"><span data-stu-id="05a64-109">Microsoft has implemented its symbolic links to function just like UNIX links.</span></span>

<span data-ttu-id="05a64-110">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="05a64-110">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="05a64-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="05a64-111">In this section</span></span>



| <span data-ttu-id="05a64-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="05a64-112">Topic</span></span>                                                                                                             | <span data-ttu-id="05a64-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05a64-113">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05a64-114">Effetti dei collegamenti simbolici sulle funzioni di file System</span><span class="sxs-lookup"><span data-stu-id="05a64-114">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)<br/> | <span data-ttu-id="05a64-115">Il modo in cui i collegamenti simbolici influiscono sulle funzioni file standard che usano nomi di percorso per specificare uno o più file.</span><span class="sxs-lookup"><span data-stu-id="05a64-115">How symbolic links affect standard file functions that use path names to specify one or more files.</span></span><br/>                                        |
| [<span data-ttu-id="05a64-116">Considerazioni sulla programmazione</span><span class="sxs-lookup"><span data-stu-id="05a64-116">Programming Considerations</span></span>](symbolic-link-programming-considerations.md)<br/>                             | <span data-ttu-id="05a64-117">Considerazioni sulla programmazione per l'utilizzo di collegamenti simbolici.</span><span class="sxs-lookup"><span data-stu-id="05a64-117">Programming considerations for working with symbolic links.</span></span><br/>                                                                                |
| [<span data-ttu-id="05a64-118">Creazione di collegamenti simbolici</span><span class="sxs-lookup"><span data-stu-id="05a64-118">Creating Symbolic Links</span></span>](creating-symbolic-links.md)<br/>                                                 | <span data-ttu-id="05a64-119">Creare collegamenti simbolici che usano un percorso assoluto o relativo tramite la funzione [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .</span><span class="sxs-lookup"><span data-stu-id="05a64-119">Create symbolic links that use either an absolute or relative path by using the [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) function.</span></span><br/> |



 

## <a name="supported-operating-systems"></a><span data-ttu-id="05a64-120">Sistemi operativi supportati</span><span class="sxs-lookup"><span data-stu-id="05a64-120">Supported Operating Systems</span></span>

<span data-ttu-id="05a64-121">I collegamenti simbolici sono disponibili in NTFS a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05a64-121">Symbolic links are available in NTFS starting with Windows Vista.</span></span>

 

 




