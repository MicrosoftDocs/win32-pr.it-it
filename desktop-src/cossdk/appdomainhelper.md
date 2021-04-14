---
description: Associa un oggetto gestito a un dominio dell'applicazione, che è un ambiente isolato in cui vengono eseguite le applicazioni.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: Classe AppDomainHelper (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523442"
---
# <a name="appdomainhelper-class"></a><span data-ttu-id="ad563-103">Classe AppDomainHelper</span><span class="sxs-lookup"><span data-stu-id="ad563-103">AppDomainHelper class</span></span>

<span data-ttu-id="ad563-104">Associa un oggetto gestito a un dominio dell'applicazione, che è un ambiente isolato in cui vengono eseguite le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ad563-104">Binds a managed object to an application domain, which is an isolated environment where applications execute.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="ad563-105">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="ad563-105">When to implement</span></span>

<span data-ttu-id="ad563-106">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="ad563-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="ad563-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad563-107">Requirement</span></span> | <span data-ttu-id="ad563-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ad563-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="ad563-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="ad563-109">CLSID</span></span>      | <span data-ttu-id="ad563-110">GUID \_ AppDomainHelper</span><span class="sxs-lookup"><span data-stu-id="ad563-110">GUID\_AppDomainHelper</span></span>                                 |
| <span data-ttu-id="ad563-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="ad563-111">ProgID</span></span>     | <span data-ttu-id="ad563-112">L "System. EnterpriseServices. Internal. AppDomainHelper"</span><span class="sxs-lookup"><span data-stu-id="ad563-112">L"System.EnterpriseServices.Internal.AppDomainHelper"</span></span> |
| <span data-ttu-id="ad563-113">Interfacce</span><span class="sxs-lookup"><span data-stu-id="ad563-113">Interfaces</span></span> | [<span data-ttu-id="ad563-114">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="ad563-114">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a><span data-ttu-id="ad563-115">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ad563-115">When to use</span></span>

<span data-ttu-id="ad563-116">Usare questa classe per accedere ai metodi di [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span><span class="sxs-lookup"><span data-stu-id="ad563-116">Use this class to access the methods of [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad563-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad563-117">Remarks</span></span>

<span data-ttu-id="ad563-118">Per creare questo oggetto, chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="ad563-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="ad563-119">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="ad563-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="ad563-120">Un oggetto AppDomainHelper può essere dichiarato con "COMSVCSLib. AppDomainHelper" come nome della classe.</span><span class="sxs-lookup"><span data-stu-id="ad563-120">An AppDomainHelper object can be declared using "COMSVCSLib.AppDomainHelper" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad563-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad563-121">Requirements</span></span>



| <span data-ttu-id="ad563-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad563-122">Requirement</span></span> | <span data-ttu-id="ad563-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ad563-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ad563-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad563-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ad563-125">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad563-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ad563-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad563-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ad563-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad563-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ad563-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad563-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad563-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad563-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad563-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad563-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad563-131">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="ad563-131">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

