---
description: Recupera le informazioni su un assembly quando si utilizza codice gestito nel Common Language Runtime .NET Framework.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Classe ClrAssemblyLocator (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877522"
---
# <a name="clrassemblylocator-class"></a><span data-ttu-id="1fb67-103">Classe ClrAssemblyLocator</span><span class="sxs-lookup"><span data-stu-id="1fb67-103">ClrAssemblyLocator class</span></span>

<span data-ttu-id="1fb67-104">Recupera le informazioni su un assembly quando si utilizza codice gestito nel Common Language Runtime .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1fb67-104">Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="1fb67-105">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="1fb67-105">When to implement</span></span>

<span data-ttu-id="1fb67-106">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="1fb67-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="1fb67-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb67-107">Requirement</span></span> | <span data-ttu-id="1fb67-108">Valore</span><span class="sxs-lookup"><span data-stu-id="1fb67-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="1fb67-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="1fb67-109">CLSID</span></span>      | <span data-ttu-id="1fb67-110">GUID \_ AssemblyLocator</span><span class="sxs-lookup"><span data-stu-id="1fb67-110">GUID\_AssemblyLocator</span></span>                                 |
| <span data-ttu-id="1fb67-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="1fb67-111">ProgID</span></span>     | <span data-ttu-id="1fb67-112">L "System. EnterpriseServices. Internal. AssemblyLocator"</span><span class="sxs-lookup"><span data-stu-id="1fb67-112">L"System.EnterpriseServices.Internal.AssemblyLocator"</span></span> |
| <span data-ttu-id="1fb67-113">Interfacce</span><span class="sxs-lookup"><span data-stu-id="1fb67-113">Interfaces</span></span> | [<span data-ttu-id="1fb67-114">**IAssemblyLocator**</span><span class="sxs-lookup"><span data-stu-id="1fb67-114">**IAssemblyLocator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a><span data-ttu-id="1fb67-115">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="1fb67-115">When to use</span></span>

<span data-ttu-id="1fb67-116">Usare questa classe per accedere ai metodi di [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span><span class="sxs-lookup"><span data-stu-id="1fb67-116">Use this class to access the methods of [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span></span>

## <a name="remarks"></a><span data-ttu-id="1fb67-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fb67-117">Remarks</span></span>

<span data-ttu-id="1fb67-118">Per creare questo oggetto, chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="1fb67-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="1fb67-119">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="1fb67-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="1fb67-120">Un oggetto ClrAssemblyLocator può essere dichiarato con "COMSVCSLib. ClrAssemblyLocator" come nome della classe.</span><span class="sxs-lookup"><span data-stu-id="1fb67-120">A ClrAssemblyLocator object can be declared using "COMSVCSLib.ClrAssemblyLocator" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb67-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fb67-121">Requirements</span></span>



| <span data-ttu-id="1fb67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb67-122">Requirement</span></span> | <span data-ttu-id="1fb67-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1fb67-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb67-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fb67-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb67-125">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fb67-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1fb67-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fb67-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb67-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fb67-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1fb67-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fb67-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fb67-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fb67-129"><dt>ComSvcs.h</dt></span></span> </dl> |



 

