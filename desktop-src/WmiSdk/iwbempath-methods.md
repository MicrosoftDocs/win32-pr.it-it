---
description: L'interfaccia IWbemPath espone i metodi seguenti.
ms.assetid: 36EC7EF6-5CCA-4D18-AB09-9EE41D1B9524
ms.tgt_platform: multiple
title: Metodi IWbemPath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ae802fd7741e5b1317160991a50bd2a535a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226943"
---
# <a name="iwbempath-methods"></a><span data-ttu-id="a1420-103">Metodi IWbemPath</span><span class="sxs-lookup"><span data-stu-id="a1420-103">IWbemPath Methods</span></span>

<span data-ttu-id="a1420-104">L'interfaccia [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a1420-104">The [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a1420-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a1420-105">In this section</span></span>

-   [<span data-ttu-id="a1420-106">**Metodo CreateClassPart**</span><span class="sxs-lookup"><span data-stu-id="a1420-106">**CreateClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-createclasspart)
-   [<span data-ttu-id="a1420-107">**Metodo DeleteClassPart**</span><span class="sxs-lookup"><span data-stu-id="a1420-107">**DeleteClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-deleteclasspart)
-   [<span data-ttu-id="a1420-108">**GetClassName (metodo)**</span><span class="sxs-lookup"><span data-stu-id="a1420-108">**GetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getclassname)
-   [<span data-ttu-id="a1420-109">**Metodo GetInfo**</span><span class="sxs-lookup"><span data-stu-id="a1420-109">**GetInfo method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getinfo)
-   [<span data-ttu-id="a1420-110">**Metodo GetKeyList**</span><span class="sxs-lookup"><span data-stu-id="a1420-110">**GetKeyList method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getkeylist)
-   [<span data-ttu-id="a1420-111">**Metodo GetNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="a1420-111">**GetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespaceat)
-   [<span data-ttu-id="a1420-112">**Metodo GetNamespaceCount**</span><span class="sxs-lookup"><span data-stu-id="a1420-112">**GetNamespaceCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespacecount)
-   [<span data-ttu-id="a1420-113">**Metodo GetScope**</span><span class="sxs-lookup"><span data-stu-id="a1420-113">**GetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscope)
-   [<span data-ttu-id="a1420-114">**Metodo GetScopeAsText**</span><span class="sxs-lookup"><span data-stu-id="a1420-114">**GetScopeAsText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopeastext)
-   [<span data-ttu-id="a1420-115">**Metodo GetScopeCount**</span><span class="sxs-lookup"><span data-stu-id="a1420-115">**GetScopeCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopecount)
-   [<span data-ttu-id="a1420-116">**Metodo GetServer**</span><span class="sxs-lookup"><span data-stu-id="a1420-116">**GetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getserver)
-   [<span data-ttu-id="a1420-117">**GetText (metodo)**</span><span class="sxs-lookup"><span data-stu-id="a1420-117">**GetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-gettext)
-   [<span data-ttu-id="a1420-118">**Metodo local**</span><span class="sxs-lookup"><span data-stu-id="a1420-118">**IsLocal method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-islocal)
-   [<span data-ttu-id="a1420-119">**Metodo IsValid**</span><span class="sxs-lookup"><span data-stu-id="a1420-119">**IsRelative method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelative)
-   [<span data-ttu-id="a1420-120">**Metodo IsRelativeOrChild**</span><span class="sxs-lookup"><span data-stu-id="a1420-120">**IsRelativeOrChild method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelativeorchild)
-   [<span data-ttu-id="a1420-121">**Metodo IsSameClassName**</span><span class="sxs-lookup"><span data-stu-id="a1420-121">**IsSameClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-issameclassname)
-   [<span data-ttu-id="a1420-122">**Metodo RemoveAllNamespaces**</span><span class="sxs-lookup"><span data-stu-id="a1420-122">**RemoveAllNamespaces method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallnamespaces)
-   [<span data-ttu-id="a1420-123">**Metodo RemoveAllScopes**</span><span class="sxs-lookup"><span data-stu-id="a1420-123">**RemoveAllScopes method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallscopes)
-   [<span data-ttu-id="a1420-124">**Metodo RemoveNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="a1420-124">**RemoveNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removenamespaceat)
-   [<span data-ttu-id="a1420-125">**Metodo RemoveScope**</span><span class="sxs-lookup"><span data-stu-id="a1420-125">**RemoveScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removescope)
-   [<span data-ttu-id="a1420-126">**Metodo seclassname**</span><span class="sxs-lookup"><span data-stu-id="a1420-126">**SetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setclassname)
-   [<span data-ttu-id="a1420-127">**Metodo SetNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="a1420-127">**SetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setnamespaceat)
-   [<span data-ttu-id="a1420-128">**Metodo sescope**</span><span class="sxs-lookup"><span data-stu-id="a1420-128">**SetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setscope)
-   [<span data-ttu-id="a1420-129">**Metodo seserver**</span><span class="sxs-lookup"><span data-stu-id="a1420-129">**SetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setserver)
-   [<span data-ttu-id="a1420-130">**SetText (metodo)**</span><span class="sxs-lookup"><span data-stu-id="a1420-130">**SetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-settext)

 

 



