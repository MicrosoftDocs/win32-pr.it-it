---
description: La proprietà CIMType dell'oggetto SWbemProperty è un numero intero che può essere utilizzato per determinare il tipo CIM di questa proprietà. Questa proprietà è di sola lettura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Proprietà SWbemProperty. CIMType (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967656"
---
# <a name="swbempropertycimtype-property"></a><span data-ttu-id="21fb5-104">Proprietà SWbemProperty. CIMType</span><span class="sxs-lookup"><span data-stu-id="21fb5-104">SWbemProperty.CIMType property</span></span>

<span data-ttu-id="21fb5-105">La proprietà **CimType** dell'oggetto [**SWbemProperty**](swbemproperty.md) è un numero intero che può essere utilizzato per determinare il tipo CIM di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="21fb5-105">The **CIMType** property of the [**SWbemProperty**](swbemproperty.md) object is an integer that can be used to determine the CIM type of this property.</span></span> <span data-ttu-id="21fb5-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="21fb5-106">This property is read-only.</span></span>

<span data-ttu-id="21fb5-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="21fb5-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="21fb5-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="21fb5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21fb5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21fb5-109">Syntax</span></span>


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a><span data-ttu-id="21fb5-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="21fb5-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="21fb5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="21fb5-111">Remarks</span></span>

<span data-ttu-id="21fb5-112">Per ulteriori informazioni sui tipi validi per questa proprietà, vedere [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="21fb5-112">For more information about valid types for this property, see [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>

<span data-ttu-id="21fb5-113">Le istanze di oggetti incorporati vengono archiviate in oggetti compositi come proprietà di tipo **\_ oggetto CIM**.</span><span class="sxs-lookup"><span data-stu-id="21fb5-113">Instances of embedded objects are stored in composite objects as properties of type **CIM\_OBJECT**.</span></span> <span data-ttu-id="21fb5-114">Per determinare la classe di un oggetto incorporato in un'istanza di una classe composita, è necessario esaminare il qualificatore **CimType** della proprietà del tipo di **\_ oggetto CIM** .</span><span class="sxs-lookup"><span data-stu-id="21fb5-114">To determine the class of an embedded object in an instance of a composite class, you must examine the **CIMType** qualifier of the **CIM\_OBJECT** type property.</span></span>

<span data-ttu-id="21fb5-115">I riferimenti a oggetti in una classe Association sono archiviati in proprietà di tipo **CIM \_ Reference**.</span><span class="sxs-lookup"><span data-stu-id="21fb5-115">The object references in an association class are stored in properties of type **CIM\_REFERENCE**.</span></span> <span data-ttu-id="21fb5-116">Per determinare i percorsi degli oggetti effettivi è necessario esaminare il qualificatore **CimType** della proprietà del tipo di **\_ riferimento CIM** .</span><span class="sxs-lookup"><span data-stu-id="21fb5-116">To determine the actual object paths you must examine the **CIMType** qualifier of the **CIM\_REFERENCE** type property.</span></span>

## <a name="requirements"></a><span data-ttu-id="21fb5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21fb5-117">Requirements</span></span>



| <span data-ttu-id="21fb5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="21fb5-118">Requirement</span></span> | <span data-ttu-id="21fb5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="21fb5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21fb5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21fb5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="21fb5-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21fb5-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21fb5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21fb5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="21fb5-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21fb5-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21fb5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21fb5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="21fb5-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="21fb5-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="21fb5-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="21fb5-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="21fb5-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21fb5-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21fb5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="21fb5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21fb5-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21fb5-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="21fb5-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="21fb5-130">CLSID</span></span><br/>                    | <span data-ttu-id="21fb5-131">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="21fb5-131">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="21fb5-132">IID</span><span class="sxs-lookup"><span data-stu-id="21fb5-132">IID</span></span><br/>                      | <span data-ttu-id="21fb5-133">\_ISWBEMPROPERTY IID</span><span class="sxs-lookup"><span data-stu-id="21fb5-133">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




