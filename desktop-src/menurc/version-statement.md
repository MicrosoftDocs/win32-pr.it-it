---
title: Istruzione VERSION
description: Definisce le informazioni sulla versione di una risorsa che possono essere usate da strumenti che leggono e scrivono file di risorse.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menu di istruzioni della versione e altre risorse
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718511"
---
# <a name="version-statement"></a><span data-ttu-id="401c8-104">Istruzione VERSION</span><span class="sxs-lookup"><span data-stu-id="401c8-104">VERSION statement</span></span>

<span data-ttu-id="401c8-105">Definisce le informazioni sulla versione di una risorsa che possono essere usate da strumenti che leggono e scrivono file di risorse.</span><span class="sxs-lookup"><span data-stu-id="401c8-105">Defines version information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="401c8-106">Il valore *DWORD* specificato viene visualizzato con la risorsa nell'oggetto compilato. File RES.</span><span class="sxs-lookup"><span data-stu-id="401c8-106">The specified *dword* value appears with the resource in the compiled .RES file.</span></span> <span data-ttu-id="401c8-107">Tuttavia, il valore non viene archiviato nel file eseguibile e non ha significato per il sistema.</span><span class="sxs-lookup"><span data-stu-id="401c8-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="401c8-108">L'istruzione **Version** viene visualizzata prima dell'inizio del corpo di una definizione di risorsa [**Accelerators**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**un'STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="401c8-108">The **VERSION** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="401c8-109">Il valore specificato si applica solo a tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="401c8-109">The specified value applies only to that resource.</span></span>

``` syntax
VERSION dword
```

<dl> <dt>

<span data-ttu-id="401c8-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="401c8-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="401c8-111">Valore **DWORD** definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="401c8-111">A user-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="401c8-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="401c8-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401c8-113">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="401c8-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="401c8-114">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="401c8-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="401c8-115">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="401c8-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="401c8-116">**MENU**</span><span class="sxs-lookup"><span data-stu-id="401c8-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="401c8-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="401c8-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="401c8-118">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="401c8-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




