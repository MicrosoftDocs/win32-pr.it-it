---
description: L'interfaccia IWbemServices espone i metodi seguenti.
ms.assetid: B4A2048E-6C2F-43E0-97BD-E6D37D8E4657
ms.tgt_platform: multiple
title: Metodi IWbemServices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a960ec223d16bd9258ba2d9d56518d88beab50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313178"
---
# <a name="iwbemservices-methods"></a><span data-ttu-id="6e1ac-103">Metodi IWbemServices</span><span class="sxs-lookup"><span data-stu-id="6e1ac-103">IWbemServices Methods</span></span>

<span data-ttu-id="6e1ac-104">L'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e1ac-104">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6e1ac-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6e1ac-105">In this section</span></span>

-   [<span data-ttu-id="6e1ac-106">**Metodo CancelAsyncCall**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-106">**CancelAsyncCall method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)
-   [<span data-ttu-id="6e1ac-107">**Metodo CreateClassEnum**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-107">**CreateClassEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)
-   [<span data-ttu-id="6e1ac-108">**Metodo CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-108">**CreateClassEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="6e1ac-109">**Metodo CreateInstanceEnum**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-109">**CreateInstanceEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)
-   [<span data-ttu-id="6e1ac-110">**Metodo CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-110">**CreateInstanceEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="6e1ac-111">**Metodo DeleteClass**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-111">**DeleteClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass)
-   [<span data-ttu-id="6e1ac-112">**Metodo DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-112">**DeleteClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)
-   [<span data-ttu-id="6e1ac-113">**Metodo DeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-113">**DeleteInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance)
-   [<span data-ttu-id="6e1ac-114">**Metodo DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-114">**DeleteInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="6e1ac-115">**Metodo ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-115">**ExecMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
-   [<span data-ttu-id="6e1ac-116">**Metodo ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-116">**ExecMethodAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="6e1ac-117">**Metodo ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-117">**ExecNotificationQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
-   [<span data-ttu-id="6e1ac-118">**Metodo ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-118">**ExecNotificationQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="6e1ac-119">**Metodo ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-119">**ExecQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   [<span data-ttu-id="6e1ac-120">**Metodo ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-120">**ExecQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="6e1ac-121">**Metodo GetObject**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-121">**GetObject method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)
-   [<span data-ttu-id="6e1ac-122">**Metodo GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-122">**GetObjectAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="6e1ac-123">**Metodo OpenNamespace**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-123">**OpenNamespace method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace)
-   [<span data-ttu-id="6e1ac-124">**Metodo PutClass**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-124">**PutClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
-   [<span data-ttu-id="6e1ac-125">**Metodo PutClassAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-125">**PutClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)
-   [<span data-ttu-id="6e1ac-126">**Metodo PutInstance**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-126">**PutInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)
-   [<span data-ttu-id="6e1ac-127">**Metodo PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-127">**PutInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)
-   [<span data-ttu-id="6e1ac-128">**Metodo QueryObjectSink**</span><span class="sxs-lookup"><span data-stu-id="6e1ac-128">**QueryObjectSink method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-queryobjectsink)

 

 



