---
description: API cronologia file
ms.assetid: 7488BA36-DEBE-42F1-8A12-A2DB1DE8B827
title: API cronologia file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb612a0bbbbd28b703a82bc65c5cd4d33640f760
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966038"
---
# <a name="file-history-api"></a><span data-ttu-id="b497f-103">API cronologia file</span><span class="sxs-lookup"><span data-stu-id="b497f-103">File History API</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b497f-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b497f-104">In this section</span></span>

-   [<span data-ttu-id="b497f-105">**\_stato backup \_ FH**</span><span class="sxs-lookup"><span data-stu-id="b497f-105">**FH\_BACKUP\_STATUS**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_backup_status)
-   [<span data-ttu-id="b497f-106">**\_risultato della \_ convalida del dispositivo FH \_**</span><span class="sxs-lookup"><span data-stu-id="b497f-106">**FH\_DEVICE\_VALIDATION\_RESULT**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_device_validation_result)
-   [<span data-ttu-id="b497f-107">**\_tipo di \_ criteri \_ locali FH**</span><span class="sxs-lookup"><span data-stu-id="b497f-107">**FH\_LOCAL\_POLICY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_local_policy_type)
-   [<span data-ttu-id="b497f-108">**\_ \_ categoria elemento protetto \_ FH**</span><span class="sxs-lookup"><span data-stu-id="b497f-108">**FH\_PROTECTED\_ITEM\_CATEGORY**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_protected_item_category)
-   [<span data-ttu-id="b497f-109">**\_tipi di conservazione FH \_**</span><span class="sxs-lookup"><span data-stu-id="b497f-109">**FH\_RETENTION\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_retention_types)
-   [<span data-ttu-id="b497f-110">**\_tipi di \_ unità di destinazione FH \_**</span><span class="sxs-lookup"><span data-stu-id="b497f-110">**FH\_TARGET\_DRIVE\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_drive_types)
-   [<span data-ttu-id="b497f-111">**\_tipo di \_ proprietà di destinazione FH \_**</span><span class="sxs-lookup"><span data-stu-id="b497f-111">**FH\_TARGET\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_property_type)
-   [<span data-ttu-id="b497f-112">**FhConfigMgr**</span><span class="sxs-lookup"><span data-stu-id="b497f-112">**FhConfigMgr**</span></span>](fhconfigmgr.md)
-   [<span data-ttu-id="b497f-113">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="b497f-113">FhManagew.exe</span></span>](fhmanagew-exe.md)
-   [<span data-ttu-id="b497f-114">**FhReassociation**</span><span class="sxs-lookup"><span data-stu-id="b497f-114">**FhReassociation**</span></span>](fhreassociation.md)
-   [<span data-ttu-id="b497f-115">**FhServiceClosePipe**</span><span class="sxs-lookup"><span data-stu-id="b497f-115">**FhServiceClosePipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceclosepipe)
-   [<span data-ttu-id="b497f-116">**FhServiceOpenPipe**</span><span class="sxs-lookup"><span data-stu-id="b497f-116">**FhServiceOpenPipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceopenpipe)
-   [<span data-ttu-id="b497f-117">**FhServiceReloadConfiguration**</span><span class="sxs-lookup"><span data-stu-id="b497f-117">**FhServiceReloadConfiguration**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicereloadconfiguration)
-   [<span data-ttu-id="b497f-118">**FhServiceBlockBackup**</span><span class="sxs-lookup"><span data-stu-id="b497f-118">**FhServiceBlockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceblockbackup)
-   [<span data-ttu-id="b497f-119">**FhServiceStartBackup**</span><span class="sxs-lookup"><span data-stu-id="b497f-119">**FhServiceStartBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestartbackup)
-   [<span data-ttu-id="b497f-120">**FhServiceStopBackup**</span><span class="sxs-lookup"><span data-stu-id="b497f-120">**FhServiceStopBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestopbackup)
-   [<span data-ttu-id="b497f-121">**FhServiceUnblockBackup**</span><span class="sxs-lookup"><span data-stu-id="b497f-121">**FhServiceUnblockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceunblockbackup)
-   [<span data-ttu-id="b497f-122">**IFhConfigMgr**</span><span class="sxs-lookup"><span data-stu-id="b497f-122">**IFhConfigMgr**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr)
-   [<span data-ttu-id="b497f-123">**IFhReassociation**</span><span class="sxs-lookup"><span data-stu-id="b497f-123">**IFhReassociation**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation)
-   [<span data-ttu-id="b497f-124">**IFhScopeIterator**</span><span class="sxs-lookup"><span data-stu-id="b497f-124">**IFhScopeIterator**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhscopeiterator)
-   [<span data-ttu-id="b497f-125">**IFhTarget**</span><span class="sxs-lookup"><span data-stu-id="b497f-125">**IFhTarget**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhtarget)

 

 



