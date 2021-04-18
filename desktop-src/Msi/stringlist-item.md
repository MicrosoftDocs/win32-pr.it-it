---
description: La proprietà Item è una proprietà di sola lettura che restituisce una stringa nella raccolta di oggetti String.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Proprietà String. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330916"
---
# <a name="stringlistitem-property"></a><span data-ttu-id="187a7-103">Proprietà String. Item</span><span class="sxs-lookup"><span data-stu-id="187a7-103">StringList.Item property</span></span>

<span data-ttu-id="187a7-104">La proprietà **Item** è una proprietà di sola lettura che restituisce una stringa nella raccolta di [**oggetti String**](stringlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="187a7-104">The **Item** property is a read-only property that returns a string in the [**StringList Object**](stringlist-object.md) collection.</span></span>

<span data-ttu-id="187a7-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="187a7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="187a7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="187a7-106">Syntax</span></span>


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a><span data-ttu-id="187a7-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="187a7-107">Property value</span></span>

<span data-ttu-id="187a7-108">Numero di indice dell'elemento con la raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="187a7-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="187a7-109">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="187a7-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="187a7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="187a7-110">Remarks</span></span>

<span data-ttu-id="187a7-111">Prima di fare riferimento alla proprietà **Item** , il client deve verificare che l' [**oggetto stringa**](stringlist-object.md) esista e non sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="187a7-111">The client must verify that the [**StringList Object**](stringlist-object.md) exists and is not empty before referencing the **Item** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="187a7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="187a7-112">Requirements</span></span>



| <span data-ttu-id="187a7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="187a7-113">Requirement</span></span> | <span data-ttu-id="187a7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="187a7-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="187a7-115">Versione</span><span class="sxs-lookup"><span data-stu-id="187a7-115">Version</span></span><br/> | <span data-ttu-id="187a7-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="187a7-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="187a7-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="187a7-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="187a7-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="187a7-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="187a7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="187a7-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="187a7-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="187a7-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="187a7-121">IID</span><span class="sxs-lookup"><span data-stu-id="187a7-121">IID</span></span><br/>     | <span data-ttu-id="187a7-122">IID \_ è definito come 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="187a7-122">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




