---
description: Considerazioni sulla programmazione per l'utilizzo di collegamenti simbolici.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Considerazioni sulla programmazione (file system locali)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320824"
---
# <a name="programming-considerations-local-file-systems"></a><span data-ttu-id="e34b8-103">Considerazioni sulla programmazione (file system locali)</span><span class="sxs-lookup"><span data-stu-id="e34b8-103">Programming Considerations (Local File Systems)</span></span>

<span data-ttu-id="e34b8-104">Quando si utilizzano i collegamenti simbolici, tenere presenti le considerazioni di programmazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="e34b8-104">Keep the following programming considerations in mind when working with symbolic links:</span></span>

-   <span data-ttu-id="e34b8-105">I collegamenti simbolici possono puntare a una destinazione inesistente.</span><span class="sxs-lookup"><span data-stu-id="e34b8-105">Symbolic links can point to a non-existent target.</span></span>
-   <span data-ttu-id="e34b8-106">Quando si crea un collegamento simbolico, il sistema operativo non verifica se la destinazione esiste.</span><span class="sxs-lookup"><span data-stu-id="e34b8-106">When creating a symbolic link, the operating system does not check to see if the target exists.</span></span>
-   <span data-ttu-id="e34b8-107">Se un'applicazione tenta di aprire una destinazione inesistente, viene restituito il **file di errore \_ \_ non \_ trovato** .</span><span class="sxs-lookup"><span data-stu-id="e34b8-107">If an application tries to open a non-existent target, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>
-   <span data-ttu-id="e34b8-108">I collegamenti simbolici sono reparse point.</span><span class="sxs-lookup"><span data-stu-id="e34b8-108">Symbolic links are reparse points.</span></span> <span data-ttu-id="e34b8-109">Per ulteriori informazioni, vedere [determinare se una directory è una cartella montata](determining-whether-a-directory-is-a-volume-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="e34b8-109">For more information, see [Determining Whether a Directory Is a Mounted Folder](determining-whether-a-directory-is-a-volume-mount-point.md).</span></span>
-   <span data-ttu-id="e34b8-110">È consentito un massimo di 63 punti di analisi (e pertanto collegamenti simbolici) in un percorso specifico.</span><span class="sxs-lookup"><span data-stu-id="e34b8-110">There is a maximum of 63 reparse points (and therefore symbolic links) allowed in a particular path.</span></span>

    <span data-ttu-id="e34b8-111">**Windows Server 2003 e Windows XP:** È previsto un limite di 31 punti di analisi in un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="e34b8-111">**Windows Server 2003 and Windows XP:** There is a limit of 31 reparse points on any given path.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e34b8-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e34b8-112">Related topics</span></span>

<dl> <span data-ttu-id="e34b8-113"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e34b8-113"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="e34b8-114">Collegamenti reali e giunzioni</span><span class="sxs-lookup"><span data-stu-id="e34b8-114">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> </dl>

 

 



