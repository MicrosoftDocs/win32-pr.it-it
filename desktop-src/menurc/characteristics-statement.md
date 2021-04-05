---
title: Caratteristiche (istruzione)
description: Definisce le informazioni su una risorsa che può essere usata da strumenti che leggono e scrivono file di definizione delle risorse.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menu di istruzioni caratteristiche e altre risorse
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045720"
---
# <a name="characteristics-statement"></a><span data-ttu-id="9782d-104">Caratteristiche (istruzione)</span><span class="sxs-lookup"><span data-stu-id="9782d-104">CHARACTERISTICS statement</span></span>

<span data-ttu-id="9782d-105">Definisce le informazioni su una risorsa che può essere usata da strumenti che leggono e scrivono file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9782d-105">Defines information about a resource that can be used by tools that read and write resource-definition files.</span></span> <span data-ttu-id="9782d-106">Il valore **DWORD** specificato viene visualizzato con la risorsa nel file. res compilato.</span><span class="sxs-lookup"><span data-stu-id="9782d-106">The specified **DWORD** value appears with the resource in the compiled .res file.</span></span> <span data-ttu-id="9782d-107">Tuttavia, il valore non viene archiviato nel file eseguibile e non ha significato per il sistema.</span><span class="sxs-lookup"><span data-stu-id="9782d-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="9782d-108">L'istruzione delle **caratteristiche** viene visualizzata prima dell'inizio del corpo di un [**acceleratore**](accelerators-resource.md), una [**finestra di dialogo**](dialog-resource.md), un [**menu**](menu-resource.md), una definizione di risorsa [**RCDATA**](rcdata-resource.md)o [**un'STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="9782d-108">The **CHARACTERISTICS** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="9782d-109">Il valore specificato si applica solo a tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="9782d-109">The specified value applies only to that resource.</span></span>

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span data-ttu-id="9782d-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="9782d-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="9782d-111">Valore **DWORD** definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9782d-111">User-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="9782d-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9782d-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9782d-113">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="9782d-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="9782d-114">**DIALOGO**</span><span class="sxs-lookup"><span data-stu-id="9782d-114">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="9782d-115">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="9782d-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="9782d-116">**MENU**</span><span class="sxs-lookup"><span data-stu-id="9782d-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="9782d-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="9782d-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="9782d-118">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="9782d-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




