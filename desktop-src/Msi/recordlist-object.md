---
description: L'oggetto di Recording è una raccolta di oggetti record. Prima di fare riferimento alle relative proprietà, è necessario verificare che l'oggetto di registrazione esista e non sia vuoto.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Oggetto Recording
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330918"
---
# <a name="recordlist-object"></a><span data-ttu-id="d93a9-104">Oggetto Recording</span><span class="sxs-lookup"><span data-stu-id="d93a9-104">RecordList object</span></span>

<span data-ttu-id="d93a9-105">L'oggetto di **Recording** è una raccolta di oggetti [**record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d93a9-105">The **RecordList** object is a collection of [**Record**](record-object.md) objects.</span></span> <span data-ttu-id="d93a9-106">Prima di fare riferimento alle relative proprietà, è necessario verificare che l'oggetto di **registrazione** esista e non sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="d93a9-106">You must verify that the **RecordList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="d93a9-107">Membri</span><span class="sxs-lookup"><span data-stu-id="d93a9-107">Members</span></span>

<span data-ttu-id="d93a9-108">Questo tipo di membri è costituito dall'oggetto **Recorder** :</span><span class="sxs-lookup"><span data-stu-id="d93a9-108">The **RecordList** object has these types of members:</span></span>

-   [<span data-ttu-id="d93a9-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d93a9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d93a9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d93a9-110">Properties</span></span>

<span data-ttu-id="d93a9-111">Le proprietà dell'oggetto di **Recording** .</span><span class="sxs-lookup"><span data-stu-id="d93a9-111">The **RecordList** object has these properties.</span></span>



| <span data-ttu-id="d93a9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d93a9-112">Property</span></span>                                     | <span data-ttu-id="d93a9-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d93a9-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="d93a9-114">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="d93a9-114">**Count**</span></span>](recordlist-count.md)<br/> | <span data-ttu-id="d93a9-115">Restituisce il numero di elementi contenuti nell'oggetto di **registrazione** .</span><span class="sxs-lookup"><span data-stu-id="d93a9-115">Returns the number of items in the **RecordList** object.</span></span><br/> |
| [<span data-ttu-id="d93a9-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d93a9-116">**Item**</span></span>](recordlist-item.md)<br/>   | <span data-ttu-id="d93a9-117">Restituisce un record in una raccolta di oggetti di un oggetto di **registrazione** .</span><span class="sxs-lookup"><span data-stu-id="d93a9-117">Returns a record in a **RecordList** object collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d93a9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d93a9-118">Requirements</span></span>



| <span data-ttu-id="d93a9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d93a9-119">Requirement</span></span> | <span data-ttu-id="d93a9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d93a9-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d93a9-121">Versione</span><span class="sxs-lookup"><span data-stu-id="d93a9-121">Version</span></span><br/> | <span data-ttu-id="d93a9-122">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d93a9-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d93a9-123">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d93a9-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d93a9-124">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="d93a9-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d93a9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d93a9-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d93a9-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d93a9-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d93a9-127">IID</span><span class="sxs-lookup"><span data-stu-id="d93a9-127">IID</span></span><br/>     | <span data-ttu-id="d93a9-128">IID \_ IRecordList è definito come 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d93a9-128">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="d93a9-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d93a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93a9-130">**Registra**</span><span class="sxs-lookup"><span data-stu-id="d93a9-130">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="d93a9-131">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d93a9-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




