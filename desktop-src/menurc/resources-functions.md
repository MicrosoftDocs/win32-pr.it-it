---
title: Funzioni di risorsa (menu e altre risorse)
description: Funzioni di risorsa (menu e altre risorse)
ms.assetid: dfeaaf01-f947-453e-946e-65ad9ec40958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e550bd42afcb98d2a1d7b1117c6c93d19529c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117529"
---
# <a name="resource-functions-menus-and-other-resources"></a><span data-ttu-id="3cf69-103">Funzioni di risorsa (menu e altre risorse)</span><span class="sxs-lookup"><span data-stu-id="3cf69-103">Resource Functions (Menus and Other Resources)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3cf69-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3cf69-104">In This Section</span></span>

-   [<span data-ttu-id="3cf69-105">**BeginUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="3cf69-105">**BeginUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)
-   [<span data-ttu-id="3cf69-106">**CopyImage**</span><span class="sxs-lookup"><span data-stu-id="3cf69-106">**CopyImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyimage)
-   [<span data-ttu-id="3cf69-107">**EndUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="3cf69-107">**EndUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)
-   <span data-ttu-id="3cf69-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cf69-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span></span>
-   [<span data-ttu-id="3cf69-109">*EnumResNameProc*</span><span class="sxs-lookup"><span data-stu-id="3cf69-109">*EnumResNameProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca)
-   [<span data-ttu-id="3cf69-110">**EnumResourceLanguages**</span><span class="sxs-lookup"><span data-stu-id="3cf69-110">**EnumResourceLanguages**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa)
-   [<span data-ttu-id="3cf69-111">**EnumResourceLanguagesEx**</span><span class="sxs-lookup"><span data-stu-id="3cf69-111">**EnumResourceLanguagesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexa)
-   [<span data-ttu-id="3cf69-112">**EnumResourceNames**</span><span class="sxs-lookup"><span data-stu-id="3cf69-112">**EnumResourceNames**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcenamesa)
-   [<span data-ttu-id="3cf69-113">**EnumResourceNamesEx**</span><span class="sxs-lookup"><span data-stu-id="3cf69-113">**EnumResourceNamesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexa)
-   [<span data-ttu-id="3cf69-114">**EnumResourceTypes**</span><span class="sxs-lookup"><span data-stu-id="3cf69-114">**EnumResourceTypes**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa)
-   [<span data-ttu-id="3cf69-115">**EnumResourceTypesEx**</span><span class="sxs-lookup"><span data-stu-id="3cf69-115">**EnumResourceTypesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa)
-   [<span data-ttu-id="3cf69-116">*EnumResTypeProc*</span><span class="sxs-lookup"><span data-stu-id="3cf69-116">*EnumResTypeProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca)
-   [<span data-ttu-id="3cf69-117">**Findresource**</span><span class="sxs-lookup"><span data-stu-id="3cf69-117">**FindResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourcea)
-   [<span data-ttu-id="3cf69-118">**FindResourceEx**</span><span class="sxs-lookup"><span data-stu-id="3cf69-118">**FindResourceEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourceexa)
-   [<span data-ttu-id="3cf69-119">**FreeResource**</span><span class="sxs-lookup"><span data-stu-id="3cf69-119">**FreeResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freeresource)
-   [<span data-ttu-id="3cf69-120">**Loadimage**</span><span class="sxs-lookup"><span data-stu-id="3cf69-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
-   [<span data-ttu-id="3cf69-121">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="3cf69-121">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
-   [<span data-ttu-id="3cf69-122">**LockResource**</span><span class="sxs-lookup"><span data-stu-id="3cf69-122">**LockResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource)
-   [<span data-ttu-id="3cf69-123">**SizeofResource**</span><span class="sxs-lookup"><span data-stu-id="3cf69-123">**SizeofResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-sizeofresource)
-   [<span data-ttu-id="3cf69-124">**UpdateResource**</span><span class="sxs-lookup"><span data-stu-id="3cf69-124">**UpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-updateresourcea)

 

 
