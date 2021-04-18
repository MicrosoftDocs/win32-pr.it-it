---
description: La proprietà Item è una proprietà di sola lettura che restituisce un record in una raccolta di oggetti di registrazione.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: Proprietà Recording. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328761"
---
# <a name="recordlistitem-property"></a><span data-ttu-id="143d9-103">Proprietà Recording. Item</span><span class="sxs-lookup"><span data-stu-id="143d9-103">RecordList.Item property</span></span>

<span data-ttu-id="143d9-104">La proprietà **Item** è una proprietà di sola lettura che restituisce un record in una raccolta di oggetti di [**registrazione**](recordlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="143d9-104">The **Item** property is a read-only property that returns a record in a [**RecordList**](recordlist-object.md) Object collection.</span></span>

<span data-ttu-id="143d9-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="143d9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="143d9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="143d9-106">Syntax</span></span>


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a><span data-ttu-id="143d9-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="143d9-107">Property value</span></span>

<span data-ttu-id="143d9-108">Numero di indice dell'elemento con la raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="143d9-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="143d9-109">L'indice è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="143d9-109">Index is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="143d9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="143d9-110">Remarks</span></span>

<span data-ttu-id="143d9-111">Il client deve verificare che l'oggetto di [**registrazione**](recordlist-object.md) esista e non sia vuoto prima di fare riferimento alla proprietà Item.</span><span class="sxs-lookup"><span data-stu-id="143d9-111">The client must verify that the [**RecordList**](recordlist-object.md) object exists and is not empty before referencing the Item property.</span></span>

## <a name="requirements"></a><span data-ttu-id="143d9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="143d9-112">Requirements</span></span>



| <span data-ttu-id="143d9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="143d9-113">Requirement</span></span> | <span data-ttu-id="143d9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="143d9-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="143d9-115">Versione</span><span class="sxs-lookup"><span data-stu-id="143d9-115">Version</span></span><br/> | <span data-ttu-id="143d9-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="143d9-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="143d9-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="143d9-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="143d9-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="143d9-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="143d9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="143d9-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="143d9-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="143d9-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="143d9-121">IID</span><span class="sxs-lookup"><span data-stu-id="143d9-121">IID</span></span><br/>     | <span data-ttu-id="143d9-122">IID \_ IRecordList è definito come 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="143d9-122">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




