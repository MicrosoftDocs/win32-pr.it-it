---
title: Enumerazione degli oggetti contenitore
description: Per convenzione, tutti gli elementi in un'enumerazione in ADSI devono avere lo stesso tipo di dati di automazione. Ad esempio, un'enumerazione non deve restituire alcuni elementi come VARIANT di tipo VT \_ I4 e altri come Variant di tipo VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297685"
---
# <a name="enumerating-container-objects"></a><span data-ttu-id="4b1de-104">Enumerazione degli oggetti contenitore</span><span class="sxs-lookup"><span data-stu-id="4b1de-104">Enumerating Container Objects</span></span>

<span data-ttu-id="4b1de-105">Per convenzione, tutti gli elementi in un'enumerazione in ADSI devono avere lo stesso tipo di dati di automazione.</span><span class="sxs-lookup"><span data-stu-id="4b1de-105">By convention, all items in an enumeration in ADSI must be of the same Automation data type.</span></span> <span data-ttu-id="4b1de-106">Ad esempio, un'enumerazione non deve restituire alcuni elementi come **Variant** di tipo **VT \_ I4** e altri come **Variant** di tipo **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="4b1de-106">For example, an enumeration should not return some items as a **VARIANT** of type **VT\_I4** and others as a **VARIANT** of type **VT\_BSTR**.</span></span>

<span data-ttu-id="4b1de-107">Per enumerare un elenco di elementi gestiti da un oggetto, un client richiede la creazione di un oggetto di enumerazione per il tipo specifico di informazioni elencate.</span><span class="sxs-lookup"><span data-stu-id="4b1de-107">To enumerate a list of items that an object maintains, a client requests the creation of an enumeration object for the specific type of information being listed.</span></span> <span data-ttu-id="4b1de-108">In ADSI il client può elencare gli oggetti in oggetti spazio dei nomi, oggetti contenitore generici, oggetti raccolta, oggetti membro o oggetti dello schema.</span><span class="sxs-lookup"><span data-stu-id="4b1de-108">In ADSI, the client may list the objects in namespace objects, generic container objects, collection objects, member objects, or schema objects.</span></span> <span data-ttu-id="4b1de-109">ADSI fornisce un filtro che può essere impostato e modificato per limitare le corrispondenze in qualsiasi enumerazione tramite la proprietà [**IADsContainer. Filter**](iadscontainer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="4b1de-109">ADSI provides a filter that can be set and modified to limit the matches in any enumeration though the [**IADsContainer.Filter**](iadscontainer-property-methods.md) property.</span></span> <span data-ttu-id="4b1de-110">Esempi di implementazioni degli oggetti enumeratore sono disponibili nel codice del componente provider di esempio per gli oggetti contenitore ADs seguenti.</span><span class="sxs-lookup"><span data-stu-id="4b1de-110">Examples of implementations of enumerator objects can be found in the example provider component code for the following ADs container objects.</span></span>



| <span data-ttu-id="4b1de-111">Tipo di oggetto</span><span class="sxs-lookup"><span data-stu-id="4b1de-111">Object type</span></span>         | <span data-ttu-id="4b1de-112">codice</span><span class="sxs-lookup"><span data-stu-id="4b1de-112">code</span></span>         |
|---------------------|--------------|
| <span data-ttu-id="4b1de-113">Contenitore generico</span><span class="sxs-lookup"><span data-stu-id="4b1de-113">Generic Container</span></span>   | <span data-ttu-id="4b1de-114">cenumobj. cpp</span><span class="sxs-lookup"><span data-stu-id="4b1de-114">cenumobj.cpp</span></span> |
| <span data-ttu-id="4b1de-115">Contenitore spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b1de-115">Namespace Container</span></span> | <span data-ttu-id="4b1de-116">cenumns. cpp</span><span class="sxs-lookup"><span data-stu-id="4b1de-116">cenumns.cpp</span></span>  |
| <span data-ttu-id="4b1de-117">Contenitore dello schema</span><span class="sxs-lookup"><span data-stu-id="4b1de-117">Schema Container</span></span>    | <span data-ttu-id="4b1de-118">cenumsch. cpp</span><span class="sxs-lookup"><span data-stu-id="4b1de-118">cenumsch.cpp</span></span> |



 

<span data-ttu-id="4b1de-119">Per informazioni sul lato client, vedere [raccolte e gruppi](collections-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="4b1de-119">For client-side information, see [Collections and Groups](collections-and-groups.md).</span></span>

 

 




