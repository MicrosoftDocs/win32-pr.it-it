---
description: L'interfaccia IAzScope espone i metodi seguenti.
ms.assetid: C9C6082C-1AD8-436F-8BC0-33CA579DD84C
title: Metodi IAzScope
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ce59c2d90dec79cf7af5247daf33173c818b17b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232671"
---
# <a name="iazscope-methods"></a><span data-ttu-id="bed7f-103">Metodi IAzScope</span><span class="sxs-lookup"><span data-stu-id="bed7f-103">IAzScope Methods</span></span>

<span data-ttu-id="bed7f-104">L'interfaccia [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="bed7f-104">The [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bed7f-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="bed7f-105">In this section</span></span>

-   [<span data-ttu-id="bed7f-106">**Metodo AddPolicyAdministrator**</span><span class="sxs-lookup"><span data-stu-id="bed7f-106">**AddPolicyAdministrator Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator)
-   [<span data-ttu-id="bed7f-107">**Metodo AddPolicyAdministratorName**</span><span class="sxs-lookup"><span data-stu-id="bed7f-107">**AddPolicyAdministratorName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministratorname)
-   [<span data-ttu-id="bed7f-108">**Metodo AddPolicyReader**</span><span class="sxs-lookup"><span data-stu-id="bed7f-108">**AddPolicyReader Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyreader)
-   [<span data-ttu-id="bed7f-109">**Metodo AddPolicyReaderName**</span><span class="sxs-lookup"><span data-stu-id="bed7f-109">**AddPolicyReaderName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyreadername)
-   [<span data-ttu-id="bed7f-110">**Metodo AddPropertyItem**</span><span class="sxs-lookup"><span data-stu-id="bed7f-110">**AddPropertyItem Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpropertyitem)
-   [<span data-ttu-id="bed7f-111">**Metodo CreateApplicationGroup**</span><span class="sxs-lookup"><span data-stu-id="bed7f-111">**CreateApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-createapplicationgroup)
-   [<span data-ttu-id="bed7f-112">**Metodo CreateRole**</span><span class="sxs-lookup"><span data-stu-id="bed7f-112">**CreateRole Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-createrole)
-   [<span data-ttu-id="bed7f-113">**Metodo CreateTask**</span><span class="sxs-lookup"><span data-stu-id="bed7f-113">**CreateTask Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-createtask)
-   [<span data-ttu-id="bed7f-114">**Metodo DeleteApplicationGroup**</span><span class="sxs-lookup"><span data-stu-id="bed7f-114">**DeleteApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-deleteapplicationgroup)
-   [<span data-ttu-id="bed7f-115">**Metodo DeletePolicyAdministrator**</span><span class="sxs-lookup"><span data-stu-id="bed7f-115">**DeletePolicyAdministrator Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-deletepolicyadministrator)
-   [<span data-ttu-id="bed7f-116">**Metodo DeletePolicyAdministratorName**</span><span class="sxs-lookup"><span data-stu-id="bed7f-116">**DeletePolicyAdministratorName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-deletepolicyadministratorname)
-   [<span data-ttu-id="bed7f-117">**Metodo DeletePolicyReader**</span><span class="sxs-lookup"><span data-stu-id="bed7f-117">**DeletePolicyReader Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-deletepolicyreader)
-   [<span data-ttu-id="bed7f-118">**Metodo DeletePolicyReaderName**</span><span class="sxs-lookup"><span data-stu-id="bed7f-118">**DeletePolicyReaderName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-deletepolicyreadername)
-   [<span data-ttu-id="bed7f-119">**Metodo DeletePropertyItem**</span><span class="sxs-lookup"><span data-stu-id="bed7f-119">**DeletePropertyItem Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-deletepropertyitem)
-   [<span data-ttu-id="bed7f-120">**Metodo DeleteRole**</span><span class="sxs-lookup"><span data-stu-id="bed7f-120">**DeleteRole Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-deleterole)
-   [<span data-ttu-id="bed7f-121">**Metodo DeleteTask**</span><span class="sxs-lookup"><span data-stu-id="bed7f-121">**DeleteTask Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-deletetask)
-   [<span data-ttu-id="bed7f-122">**GetProperty (metodo)**</span><span class="sxs-lookup"><span data-stu-id="bed7f-122">**GetProperty Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-getproperty)
-   [<span data-ttu-id="bed7f-123">**Metodo OpenApplicationGroup**</span><span class="sxs-lookup"><span data-stu-id="bed7f-123">**OpenApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-openapplicationgroup)
-   [<span data-ttu-id="bed7f-124">**Metodo OpenRole**</span><span class="sxs-lookup"><span data-stu-id="bed7f-124">**OpenRole Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-openrole)
-   [<span data-ttu-id="bed7f-125">**Metodo OpenTask**</span><span class="sxs-lookup"><span data-stu-id="bed7f-125">**OpenTask Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-opentask)
-   [<span data-ttu-id="bed7f-126">**Metodo SetProperty**</span><span class="sxs-lookup"><span data-stu-id="bed7f-126">**SetProperty Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-setproperty)
-   [<span data-ttu-id="bed7f-127">**Submit (metodo)**</span><span class="sxs-lookup"><span data-stu-id="bed7f-127">**Submit Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazscope-submit)

 

 



