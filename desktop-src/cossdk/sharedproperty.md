---
description: Imposta o Recupera il valore di una proprietà condivisa.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: Classe SharedProperty (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126579"
---
# <a name="sharedproperty-class"></a><span data-ttu-id="4f346-103">Classe SharedProperty</span><span class="sxs-lookup"><span data-stu-id="4f346-103">SharedProperty class</span></span>

<span data-ttu-id="4f346-104">Imposta o Recupera il valore di una proprietà condivisa.</span><span class="sxs-lookup"><span data-stu-id="4f346-104">Sets or retrieves the value of a shared property.</span></span>

<span data-ttu-id="4f346-105">Per informazioni generali sull'utilizzo del Gestione proprietà condiviso in COM+, vedere [Gestione proprietà condiviso com+](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="4f346-105">For general information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="4f346-106">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="4f346-106">When to implement</span></span>

<span data-ttu-id="4f346-107">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="4f346-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="4f346-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f346-108">Requirement</span></span> | <span data-ttu-id="4f346-109">Valore</span><span class="sxs-lookup"><span data-stu-id="4f346-109">Value</span></span> |
|------------|--------------------------------------------|
| <span data-ttu-id="4f346-110">Interfacce</span><span class="sxs-lookup"><span data-stu-id="4f346-110">Interfaces</span></span> | [<span data-ttu-id="4f346-111">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="4f346-111">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a><span data-ttu-id="4f346-112">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4f346-112">When to use</span></span>

<span data-ttu-id="4f346-113">Usare questa classe per accedere ai metodi di [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span><span class="sxs-lookup"><span data-stu-id="4f346-113">Use this class to access the methods of [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f346-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f346-114">Remarks</span></span>

<span data-ttu-id="4f346-115">È possibile creare un oggetto **SharedProperty** usando i metodi [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) di [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="4f346-115">You can create a **SharedProperty** object by using the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

<span data-ttu-id="4f346-116">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="4f346-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="4f346-117">Viene creato un oggetto SharedProperty chiamando i metodi [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) dell'oggetto [**SharedPropertyGroup**](sharedpropertygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="4f346-117">A SharedProperty object is created by calling the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of the [**SharedPropertyGroup**](sharedpropertygroup.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f346-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f346-118">Requirements</span></span>



| <span data-ttu-id="4f346-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f346-119">Requirement</span></span> | <span data-ttu-id="4f346-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4f346-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f346-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f346-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f346-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f346-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4f346-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f346-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f346-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f346-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4f346-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f346-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f346-126"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f346-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f346-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f346-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f346-128">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="4f346-128">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[<span data-ttu-id="4f346-129">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="4f346-129">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> <dt>

[<span data-ttu-id="4f346-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="4f346-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




