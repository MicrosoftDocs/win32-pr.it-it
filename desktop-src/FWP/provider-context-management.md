---
title: Gestione del contesto del provider
description: Gestione del contesto del provider
ms.assetid: A73A6171-C81B-48EF-A689-3219E0B6B7C3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7970cdd6f3a69760a74ba4f0419ecb5022a339
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725871"
---
# <a name="provider-context-management"></a><span data-ttu-id="8e584-103">Gestione del contesto del provider</span><span class="sxs-lookup"><span data-stu-id="8e584-103">Provider Context Management</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8e584-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8e584-104">In this section</span></span>

-   [<span data-ttu-id="8e584-105">**\_Modifica del contesto del provider FWPM \_ \_ \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="8e584-105">**FWPM\_PROVIDER\_CONTEXT\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_provider_context_change_callback0)
-   [<span data-ttu-id="8e584-106">**FwpmProviderContextAdd0**</span><span class="sxs-lookup"><span data-stu-id="8e584-106">**FwpmProviderContextAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)
-   [<span data-ttu-id="8e584-107">**FwpmProviderContextAdd1**</span><span class="sxs-lookup"><span data-stu-id="8e584-107">**FwpmProviderContextAdd1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd1)
-   [<span data-ttu-id="8e584-108">**FwpmProviderContextAdd2**</span><span class="sxs-lookup"><span data-stu-id="8e584-108">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="8e584-109">**FwpmProviderContextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="8e584-109">**FwpmProviderContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0)
-   [<span data-ttu-id="8e584-110">**FwpmProviderContextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="8e584-110">**FwpmProviderContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebyid0)
-   [<span data-ttu-id="8e584-111">**FwpmProviderContextDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="8e584-111">**FwpmProviderContextDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebykey0)
-   [<span data-ttu-id="8e584-112">**FwpmProviderContextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="8e584-112">**FwpmProviderContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdestroyenumhandle0)
-   [<span data-ttu-id="8e584-113">**FwpmProviderContextEnum0**</span><span class="sxs-lookup"><span data-stu-id="8e584-113">**FwpmProviderContextEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum0)
-   [<span data-ttu-id="8e584-114">**FwpmProviderContextEnum1**</span><span class="sxs-lookup"><span data-stu-id="8e584-114">**FwpmProviderContextEnum1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum1)
-   [<span data-ttu-id="8e584-115">**FwpmProviderContextEnum2**</span><span class="sxs-lookup"><span data-stu-id="8e584-115">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="8e584-116">**FwpmProviderContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="8e584-116">**FwpmProviderContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid0)
-   [<span data-ttu-id="8e584-117">**FwpmProviderContextGetById1**</span><span class="sxs-lookup"><span data-stu-id="8e584-117">**FwpmProviderContextGetById1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid1)
-   [<span data-ttu-id="8e584-118">**FwpmProviderContextGetById2**</span><span class="sxs-lookup"><span data-stu-id="8e584-118">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="8e584-119">**FwpmProviderContextGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="8e584-119">**FwpmProviderContextGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey0)
-   [<span data-ttu-id="8e584-120">**FwpmProviderContextGetByKey1**</span><span class="sxs-lookup"><span data-stu-id="8e584-120">**FwpmProviderContextGetByKey1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey1)
-   [<span data-ttu-id="8e584-121">**FwpmProviderContextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="8e584-121">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="8e584-122">**FwpmProviderContextGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="8e584-122">**FwpmProviderContextGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetsecurityinfobykey0)
-   [<span data-ttu-id="8e584-123">**FwpmProviderContextSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="8e584-123">**FwpmProviderContextSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsetsecurityinfobykey0)
-   [<span data-ttu-id="8e584-124">**FwpmProviderContextSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="8e584-124">**FwpmProviderContextSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0)
-   [<span data-ttu-id="8e584-125">**FwpmProviderContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="8e584-125">**FwpmProviderContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscriptionsget0)
-   [<span data-ttu-id="8e584-126">**FwpmProviderContextUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="8e584-126">**FwpmProviderContextUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextunsubscribechanges0)

 

 