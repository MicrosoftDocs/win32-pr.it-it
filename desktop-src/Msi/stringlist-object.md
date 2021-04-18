---
description: L'oggetto String è una raccolta di stringhe. Prima di fare riferimento alle relative proprietà, il client deve verificare che l'oggetto stringa sia presente e non sia vuoto.
ms.assetid: 7021320a-d01a-43e8-90a5-6105a11a4613
title: Oggetto String.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6493b9e1723d46ce290c7472bbcee7eb9ec34725
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328061"
---
# <a name="stringlist-object"></a><span data-ttu-id="872b4-104">Oggetto String.</span><span class="sxs-lookup"><span data-stu-id="872b4-104">StringList object</span></span>

<span data-ttu-id="872b4-105">L'oggetto **String** è una raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="872b4-105">The **StringList** object is a collection of strings.</span></span> <span data-ttu-id="872b4-106">Prima di fare riferimento alle relative proprietà, il client deve verificare che l'oggetto **stringa** sia presente e non sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="872b4-106">The client must verify that the **StringList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="872b4-107">Membri</span><span class="sxs-lookup"><span data-stu-id="872b4-107">Members</span></span>

<span data-ttu-id="872b4-108">Questo tipo di membri è associato all'oggetto **String** .</span><span class="sxs-lookup"><span data-stu-id="872b4-108">The **StringList** object has these types of members:</span></span>

-   [<span data-ttu-id="872b4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="872b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="872b4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="872b4-110">Properties</span></span>

<span data-ttu-id="872b4-111">Le proprietà dell'oggetto **String** .</span><span class="sxs-lookup"><span data-stu-id="872b4-111">The **StringList** object has these properties.</span></span>



| <span data-ttu-id="872b4-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="872b4-112">Property</span></span>                                     | <span data-ttu-id="872b4-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="872b4-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="872b4-114">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="872b4-114">**Count**</span></span>](stringlist-count.md)<br/> | <span data-ttu-id="872b4-115">Restituisce il numero di elementi nell'oggetto **String** .</span><span class="sxs-lookup"><span data-stu-id="872b4-115">Returns the number of items in the **StringList** object.</span></span><br/> |
| [<span data-ttu-id="872b4-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="872b4-116">**Item**</span></span>](stringlist-item.md)<br/>   | <span data-ttu-id="872b4-117">Restituisce una stringa nella raccolta di oggetti **String** .</span><span class="sxs-lookup"><span data-stu-id="872b4-117">Returns a string in the **StringList** object collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="872b4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="872b4-118">Requirements</span></span>



| <span data-ttu-id="872b4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="872b4-119">Requirement</span></span> | <span data-ttu-id="872b4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="872b4-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="872b4-121">Versione</span><span class="sxs-lookup"><span data-stu-id="872b4-121">Version</span></span><br/> | <span data-ttu-id="872b4-122">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="872b4-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="872b4-123">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="872b4-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="872b4-124">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="872b4-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="872b4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="872b4-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="872b4-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="872b4-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="872b4-127">IID</span><span class="sxs-lookup"><span data-stu-id="872b4-127">IID</span></span><br/>     | <span data-ttu-id="872b4-128">IID \_ è definito come 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="872b4-128">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="872b4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="872b4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872b4-130">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="872b4-130">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




