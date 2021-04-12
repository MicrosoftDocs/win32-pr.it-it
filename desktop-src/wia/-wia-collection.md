---
description: Classe Collection
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Collection (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345601"
---
# <a name="collection-object"></a><span data-ttu-id="f8932-103">Collection (oggetto)</span><span class="sxs-lookup"><span data-stu-id="f8932-103">Collection object</span></span>

<span data-ttu-id="f8932-104">Classe Collection</span><span class="sxs-lookup"><span data-stu-id="f8932-104">Collection Class</span></span>

## <a name="members"></a><span data-ttu-id="f8932-105">Membri</span><span class="sxs-lookup"><span data-stu-id="f8932-105">Members</span></span>

<span data-ttu-id="f8932-106">L'oggetto **raccolta** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8932-106">The **Collection** object has these types of members:</span></span>

-   [<span data-ttu-id="f8932-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8932-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8932-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8932-108">Properties</span></span>

<span data-ttu-id="f8932-109">L'oggetto **raccolta** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8932-109">The **Collection** object has these properties.</span></span>



| <span data-ttu-id="f8932-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8932-110">Property</span></span>                                           | <span data-ttu-id="f8932-111">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="f8932-111">Access type</span></span>          | <span data-ttu-id="f8932-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8932-112">Description</span></span>                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="f8932-113">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="f8932-113">**Count**</span></span>](-wia-icollection-count.md)<br/> | <span data-ttu-id="f8932-114">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8932-114">Read-only</span></span><br/> | <span data-ttu-id="f8932-115">Restituisce il numero di membri nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="f8932-115">Returns the number of members in the collection</span></span><br/> |
| [<span data-ttu-id="f8932-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f8932-116">**Item**</span></span>](-wia-icollection-item.md)<br/>   | <span data-ttu-id="f8932-117">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8932-117">Read-only</span></span><br/> | <span data-ttu-id="f8932-118">Restituisce l'elemento specificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="f8932-118">Returns the specified item in the collection</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="f8932-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8932-119">Remarks</span></span>

### <a name="creationaccess-functions"></a><span data-ttu-id="f8932-120">Funzioni di accesso per la creazione \\</span><span class="sxs-lookup"><span data-stu-id="f8932-120">Creation\\Access Functions</span></span>

<span data-ttu-id="f8932-121">Per recuperare un riferimento all'oggetto, utilizzare uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="f8932-121">Use any of the following to retrieve a reference to the object:</span></span>



[<span data-ttu-id="f8932-122">**GetItemsFromUI**</span><span class="sxs-lookup"><span data-stu-id="f8932-122">**GetItemsFromUI**</span></span>](-wia-iwiadispatchitem-getitemsfromui.md)

[<span data-ttu-id="f8932-123">**Children**</span><span class="sxs-lookup"><span data-stu-id="f8932-123">**Children**</span></span>](-wia-iwiadispatchitem-children.md)

[<span data-ttu-id="f8932-124">**Dispositivi**</span><span class="sxs-lookup"><span data-stu-id="f8932-124">**Devices**</span></span>](-wia-iwia-devices.md)



 

## <a name="requirements"></a><span data-ttu-id="f8932-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8932-125">Requirements</span></span>



| <span data-ttu-id="f8932-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8932-126">Requirement</span></span> | <span data-ttu-id="f8932-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f8932-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8932-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8932-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f8932-129">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f8932-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8932-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8932-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f8932-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8932-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f8932-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f8932-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8932-133"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f8932-133"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




