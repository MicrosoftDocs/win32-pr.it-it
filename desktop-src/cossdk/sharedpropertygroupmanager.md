---
description: Crea gruppi di proprietà condivisi e per ottenere l'accesso ai gruppi di proprietà condivisi esistenti.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: Classe SharedPropertyGroupManager (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877621"
---
# <a name="sharedpropertygroupmanager-class"></a><span data-ttu-id="4a6c9-103">Classe SharedPropertyGroupManager</span><span class="sxs-lookup"><span data-stu-id="4a6c9-103">SharedPropertyGroupManager class</span></span>

<span data-ttu-id="4a6c9-104">Crea gruppi di proprietà condivisi e per ottenere l'accesso ai gruppi di proprietà condivisi esistenti.</span><span class="sxs-lookup"><span data-stu-id="4a6c9-104">Creates shared property groups and to obtain access to existing shared property groups.</span></span>

<span data-ttu-id="4a6c9-105">Per ulteriori informazioni sull'utilizzo del Gestione proprietà condiviso in COM+, vedere [com+ shared gestione proprietà](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="4a6c9-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="4a6c9-106">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="4a6c9-106">When to implement</span></span>

<span data-ttu-id="4a6c9-107">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="4a6c9-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="4a6c9-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a6c9-108">Requirement</span></span> | <span data-ttu-id="4a6c9-109">Valore</span><span class="sxs-lookup"><span data-stu-id="4a6c9-109">Value</span></span> |
|------------|--------------------------------------------------------------------|
| <span data-ttu-id="4a6c9-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="4a6c9-110">CLSID</span></span>      | <span data-ttu-id="4a6c9-111">\_SHAREDPROPERTYGROUPMANAGER CLSID</span><span class="sxs-lookup"><span data-stu-id="4a6c9-111">CLSID\_SharedPropertyGroupManager</span></span>                                  |
| <span data-ttu-id="4a6c9-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="4a6c9-112">ProgID</span></span>     | <span data-ttu-id="4a6c9-113">L "MTxSpm. SharedPropertyGroupManager"</span><span class="sxs-lookup"><span data-stu-id="4a6c9-113">L"MTxSpm.SharedPropertyGroupManager"</span></span>                               |
| <span data-ttu-id="4a6c9-114">Interfacce</span><span class="sxs-lookup"><span data-stu-id="4a6c9-114">Interfaces</span></span> | [<span data-ttu-id="4a6c9-115">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="4a6c9-115">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a><span data-ttu-id="4a6c9-116">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4a6c9-116">When to use</span></span>

<span data-ttu-id="4a6c9-117">Usare questa classe per accedere ai metodi di [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="4a6c9-117">Use this class to access the methods of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6c9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a6c9-118">Remarks</span></span>

<span data-ttu-id="4a6c9-119">Per creare questo oggetto, chiamare [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="4a6c9-119">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="4a6c9-120">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="4a6c9-120">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="4a6c9-121">Un oggetto SharedPropertyGroupManager può essere dichiarato con "COMSVCSLib. SharedPropertyGroupManager" come nome della classe.</span><span class="sxs-lookup"><span data-stu-id="4a6c9-121">A SharedPropertyGroupManager object can be declared using "COMSVCSLib.SharedPropertyGroupManager" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a6c9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a6c9-122">Requirements</span></span>



| <span data-ttu-id="4a6c9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a6c9-123">Requirement</span></span> | <span data-ttu-id="4a6c9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4a6c9-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6c9-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a6c9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4a6c9-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a6c9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4a6c9-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a6c9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4a6c9-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a6c9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4a6c9-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a6c9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a6c9-130"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a6c9-130"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a6c9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a6c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a6c9-132">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="4a6c9-132">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[<span data-ttu-id="4a6c9-133">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="4a6c9-133">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="4a6c9-134">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="4a6c9-134">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> </dl>

 

 




