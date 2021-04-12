---
description: Componenti BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componenti BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232678"
---
# <a name="blob-components"></a><span data-ttu-id="28bb0-103">Componenti BLOB</span><span class="sxs-lookup"><span data-stu-id="28bb0-103">BLOB Components</span></span>

<span data-ttu-id="28bb0-104">Un oggetto binario di grandi dimensioni (BLOB) include i componenti gerarchici seguenti:</span><span class="sxs-lookup"><span data-stu-id="28bb0-104">A binary large object (BLOB) includes the following hierarchical components:</span></span>

-   <span data-ttu-id="28bb0-105">Proprietari</span><span class="sxs-lookup"><span data-stu-id="28bb0-105">Owners</span></span>
-   <span data-ttu-id="28bb0-106">Categorie</span><span class="sxs-lookup"><span data-stu-id="28bb0-106">Categories</span></span>
-   <span data-ttu-id="28bb0-107">Tag</span><span class="sxs-lookup"><span data-stu-id="28bb0-107">Tags</span></span>
-   <span data-ttu-id="28bb0-108">Valori</span><span class="sxs-lookup"><span data-stu-id="28bb0-108">Values</span></span>

## <a name="textual-representation"></a><span data-ttu-id="28bb0-109">Rappresentazione testuale</span><span class="sxs-lookup"><span data-stu-id="28bb0-109">Textual Representation</span></span>

<span data-ttu-id="28bb0-110">Per praticità, i BLOB vengono visualizzati nel formato proprietario: Categoria: Tag: valore in cui compaiono quando vengono salvati in un file.</span><span class="sxs-lookup"><span data-stu-id="28bb0-110">For convenience, BLOBs appear in the Owner:Category:Tag:Value format that they appear in when saved to a file.</span></span> <span data-ttu-id="28bb0-111">La struttura interna del BLOB è opaca perché rappresenta i puntatori e le tabelle.</span><span class="sxs-lookup"><span data-stu-id="28bb0-111">The internal structure of the BLOB is opaque because it represents pointers and tables.</span></span> <span data-ttu-id="28bb0-112">Ecco ad esempio una voce di un BLOB che può essere usata per configurare un NPP:</span><span class="sxs-lookup"><span data-stu-id="28bb0-112">For example, here is an entry from a BLOB that can be used to configure an NPP:</span></span>

``` syntax
NPP:Configure:BufferSize=32768
```

<span data-ttu-id="28bb0-113">Il proprietario è NPP.</span><span class="sxs-lookup"><span data-stu-id="28bb0-113">The Owner is NPP.</span></span> <span data-ttu-id="28bb0-114">La categoria è configure, il tag è BufferSize e il valore è 32768.</span><span class="sxs-lookup"><span data-stu-id="28bb0-114">The Category is Configure, the Tag is BufferSize, and the Value is 32768.</span></span>

 

 



