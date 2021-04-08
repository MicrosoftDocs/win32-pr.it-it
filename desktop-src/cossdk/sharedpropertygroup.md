---
description: Consente di creare e accedere alle proprietà condivise in un gruppo di proprietà condivise.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: Classe SharedPropertyGroup (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748170"
---
# <a name="sharedpropertygroup-class"></a><span data-ttu-id="8ad6a-103">Classe SharedPropertyGroup</span><span class="sxs-lookup"><span data-stu-id="8ad6a-103">SharedPropertyGroup class</span></span>

<span data-ttu-id="8ad6a-104">Consente di creare e accedere alle proprietà condivise in un gruppo di proprietà condivise.</span><span class="sxs-lookup"><span data-stu-id="8ad6a-104">Creates and accesses the shared properties in a shared property group.</span></span>

<span data-ttu-id="8ad6a-105">Per ulteriori informazioni sull'utilizzo del Gestione proprietà condiviso in COM+, vedere [com+ shared gestione proprietà](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="8ad6a-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="8ad6a-106">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="8ad6a-106">When to implement</span></span>

<span data-ttu-id="8ad6a-107">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="8ad6a-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="8ad6a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ad6a-108">Requirement</span></span> | <span data-ttu-id="8ad6a-109">Valore</span><span class="sxs-lookup"><span data-stu-id="8ad6a-109">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="8ad6a-110">Interfacce</span><span class="sxs-lookup"><span data-stu-id="8ad6a-110">Interfaces</span></span> | [<span data-ttu-id="8ad6a-111">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="8ad6a-111">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a><span data-ttu-id="8ad6a-112">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8ad6a-112">When to use</span></span>

<span data-ttu-id="8ad6a-113">Usare questa classe per accedere ai metodi di [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="8ad6a-113">Use this class to access the methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ad6a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ad6a-114">Remarks</span></span>

<span data-ttu-id="8ad6a-115">È possibile creare un oggetto **SharedPropertyGroup** usando il metodo [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) di [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="8ad6a-115">You can create a **SharedPropertyGroup** object using the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

<span data-ttu-id="8ad6a-116">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="8ad6a-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="8ad6a-117">Un oggetto SharedPropertyGroup viene creato chiamando il metodo [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) dell'oggetto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad6a-117">A SharedPropertyGroup object is created by calling the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ad6a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ad6a-118">Requirements</span></span>



| <span data-ttu-id="8ad6a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ad6a-119">Requirement</span></span> | <span data-ttu-id="8ad6a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8ad6a-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad6a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ad6a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8ad6a-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8ad6a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8ad6a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ad6a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8ad6a-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8ad6a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8ad6a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ad6a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ad6a-126"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ad6a-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ad6a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ad6a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad6a-128">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="8ad6a-128">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[<span data-ttu-id="8ad6a-129">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="8ad6a-129">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="8ad6a-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="8ad6a-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




