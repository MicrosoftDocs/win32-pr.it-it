---
description: La proprietà Children dell'oggetto Item recupera una raccolta di oggetti Item. Gli elementi in questa raccolta rappresentano elementi che sono elementi figlio diretti di questo elemento nell'albero gerarchico. Di sola lettura.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item. Children (proprietà)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308232"
---
# <a name="itemchildren-property"></a><span data-ttu-id="f0f83-105">Item. Children (proprietà)</span><span class="sxs-lookup"><span data-stu-id="f0f83-105">Item.Children property</span></span>

<span data-ttu-id="f0f83-106">La proprietà **Children** dell'oggetto [**Item**](-wia-item.md) recupera una raccolta di oggetti **Item** .</span><span class="sxs-lookup"><span data-stu-id="f0f83-106">The **Children** property of the [**Item**](-wia-item.md) object retrieves a collection of **Item** objects.</span></span> <span data-ttu-id="f0f83-107">Gli elementi in questa raccolta rappresentano elementi che sono elementi figlio diretti di questo elemento nell'albero gerarchico.</span><span class="sxs-lookup"><span data-stu-id="f0f83-107">The items in this collection represent items that are direct children of this item in the hierarchical tree.</span></span> <span data-ttu-id="f0f83-108">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f0f83-108">Read-only.</span></span>

<span data-ttu-id="f0f83-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f0f83-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f83-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0f83-110">Syntax</span></span>


```JScript
propVal = Item.Children
```



## <a name="property-value"></a><span data-ttu-id="f0f83-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f0f83-111">Property value</span></span>

<span data-ttu-id="f0f83-112">Variabile che riceve gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="f0f83-112">Variable that receives the objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0f83-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0f83-113">Remarks</span></span>

<span data-ttu-id="f0f83-114">Usare questa proprietà per esplorare l'albero gerarchico di oggetti [**elemento**](-wia-item.md) che rappresentano un dispositivo, le cartelle e i file che risiedono nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0f83-114">Use this property to navigate the hierarchical tree of [**Item**](-wia-item.md) objects that represent a device, the folders and the files that reside on the device.</span></span>

<span data-ttu-id="f0f83-115">La proprietà **Children** è una raccolta di oggetti [**Item**](-wia-item.md) solo dal livello direttamente sotto questo oggetto **Item** nell'albero.</span><span class="sxs-lookup"><span data-stu-id="f0f83-115">The **Children** property is a collection of [**Item**](-wia-item.md) objects only from the level directly beneath this **Item** object in the tree.</span></span> <span data-ttu-id="f0f83-116">Per spostarsi verso il basso nella struttura ad albero, usare questa proprietà in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="f0f83-116">To navigate further levels down the tree, use this property recursively.</span></span>

<span data-ttu-id="f0f83-117">Se l'elemento non può o non contiene elementi figlio, questa proprietà restituisce una raccolta vuota.</span><span class="sxs-lookup"><span data-stu-id="f0f83-117">If the item cannot or does not have any child items, this property returns an empty collection.</span></span>

> [!Note]  
> <span data-ttu-id="f0f83-118">Questa raccolta è in base 0.</span><span class="sxs-lookup"><span data-stu-id="f0f83-118">This collection is 0-based.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f0f83-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="f0f83-119">Examples</span></span>

<span data-ttu-id="f0f83-120">Nell'esempio seguente viene illustrato l'utilizzo della proprietà **Children** per recuperare ed enumerare una raccolta di elementi figlio di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0f83-120">The following example demonstrates the use of the **Children** property to retrieve and enumerate a collection of the child items of a device.</span></span> <span data-ttu-id="f0f83-121">Se il dispositivo è una fotocamera digitale, la raccolta contiene in genere elementi di cartelle e immagini.</span><span class="sxs-lookup"><span data-stu-id="f0f83-121">If the device is a digital camera, the collection typically contains folder and image items.</span></span> <span data-ttu-id="f0f83-122">Se il dispositivo è uno scanner, la raccolta contiene in genere elementi che rappresentano i letti di analisi.</span><span class="sxs-lookup"><span data-stu-id="f0f83-122">If the device is a scanner, the collection typically contains items that represent scanning beds.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="f0f83-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0f83-123">Requirements</span></span>



| <span data-ttu-id="f0f83-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0f83-124">Requirement</span></span> | <span data-ttu-id="f0f83-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f0f83-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f83-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0f83-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f0f83-127">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f0f83-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0f83-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0f83-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f0f83-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0f83-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f0f83-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f0f83-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0f83-131"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f0f83-131"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




