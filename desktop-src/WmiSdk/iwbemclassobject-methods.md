---
description: L'interfaccia IWbemClassObject espone i metodi seguenti.
ms.assetid: 20BF7775-89D9-4851-8561-EEBA398A0584
ms.tgt_platform: multiple
title: Metodi IWbemClassObject
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825b3f15f17dca6dd0871bbcae3f531a90c90f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350086"
---
# <a name="iwbemclassobject-methods"></a><span data-ttu-id="a3cfb-103">Metodi IWbemClassObject</span><span class="sxs-lookup"><span data-stu-id="a3cfb-103">IWbemClassObject Methods</span></span>

<span data-ttu-id="a3cfb-104">L'interfaccia [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-104">The [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a3cfb-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a3cfb-105">In this section</span></span>

-   [<span data-ttu-id="a3cfb-106">**Metodo BeginEnumeration**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-106">**BeginEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)
-   [<span data-ttu-id="a3cfb-107">**Metodo BeginMethodEnumeration**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-107">**BeginMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginmethodenumeration)
-   [<span data-ttu-id="a3cfb-108">**Clone (metodo)**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-108">**Clone method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)
-   [<span data-ttu-id="a3cfb-109">**CompareTo (metodo)**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-109">**CompareTo method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-compareto)
-   [<span data-ttu-id="a3cfb-110">**Delete (metodo)**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-110">**Delete method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)
-   [<span data-ttu-id="a3cfb-111">**Metodo DeleteMethod**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-111">**DeleteMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-deletemethod)
-   [<span data-ttu-id="a3cfb-112">**Metodo EndEnumeration**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-112">**EndEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration)
-   [<span data-ttu-id="a3cfb-113">**Metodo EndMethodEnumeration**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-113">**EndMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endmethodenumeration)
-   [<span data-ttu-id="a3cfb-114">**Metodo Get**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-114">**Get method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)
-   [<span data-ttu-id="a3cfb-115">**Metodo GetMethod**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-115">**GetMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)
-   [<span data-ttu-id="a3cfb-116">**Metodo GetMethodOrigin**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-116">**GetMethodOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodorigin)
-   [<span data-ttu-id="a3cfb-117">**Metodo GetMethodQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-117">**GetMethodQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)
-   [<span data-ttu-id="a3cfb-118">**Metodo GetNames**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-118">**GetNames method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getnames)
-   [<span data-ttu-id="a3cfb-119">**Metodo GetObjectText**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-119">**GetObjectText method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   [<span data-ttu-id="a3cfb-120">**Metodo GetPropertyOrigin**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-120">**GetPropertyOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyorigin)
-   [<span data-ttu-id="a3cfb-121">**Metodo GetPropertyQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-121">**GetPropertyQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)
-   [<span data-ttu-id="a3cfb-122">**Metodo GetQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-122">**GetQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)
-   [<span data-ttu-id="a3cfb-123">**Metodo InheritsFrom**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-123">**InheritsFrom method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-inheritsfrom)
-   [<span data-ttu-id="a3cfb-124">**Metodo Next**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-124">**Next method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-next)
-   [<span data-ttu-id="a3cfb-125">**Metodo NextMethod**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-125">**NextMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-nextmethod)
-   [<span data-ttu-id="a3cfb-126">**Put (metodo)**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-126">**Put method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
-   [<span data-ttu-id="a3cfb-127">**Metodo PutMethod**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-127">**PutMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)
-   [<span data-ttu-id="a3cfb-128">**Metodo SpawnDerivedClass**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-128">**SpawnDerivedClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)
-   [<span data-ttu-id="a3cfb-129">**Metodo SpawnInstance**</span><span class="sxs-lookup"><span data-stu-id="a3cfb-129">**SpawnInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

 

 



