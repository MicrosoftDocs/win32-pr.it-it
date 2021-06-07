---
title: Funzioni delle risorse (menu e altre risorse)
description: Funzioni delle risorse (menu e altre risorse)
ms.assetid: dfeaaf01-f947-453e-946e-65ad9ec40958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee066a6a111c911dd704997eeb7ed1c89ae1f417
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2021
ms.locfileid: "111550003"
---
# <a name="resource-functions-menus-and-other-resources"></a><span data-ttu-id="f82da-103">Funzioni delle risorse (menu e altre risorse)</span><span class="sxs-lookup"><span data-stu-id="f82da-103">Resource Functions (Menus and Other Resources)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f82da-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f82da-104">In This Section</span></span>

-   [<span data-ttu-id="f82da-105">**BeginUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="f82da-105">**BeginUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)
-   [<span data-ttu-id="f82da-106">**CopyImage**</span><span class="sxs-lookup"><span data-stu-id="f82da-106">**CopyImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyimage)
-   [<span data-ttu-id="f82da-107">**EndUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="f82da-107">**EndUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)
-   <span data-ttu-id="f82da-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f82da-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span></span>
-   [<span data-ttu-id="f82da-109">*EnumResNameProc*</span><span class="sxs-lookup"><span data-stu-id="f82da-109">*EnumResNameProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca)
-   [<span data-ttu-id="f82da-110">**EnumResourceLanguages**</span><span class="sxs-lookup"><span data-stu-id="f82da-110">**EnumResourceLanguages**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa)
-   [<span data-ttu-id="f82da-111">**EnumResourceLanguagesEx**</span><span class="sxs-lookup"><span data-stu-id="f82da-111">**EnumResourceLanguagesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexa)
-   [<span data-ttu-id="f82da-112">**EnumResourceNames**</span><span class="sxs-lookup"><span data-stu-id="f82da-112">**EnumResourceNames**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-enumresourcenamesa)
-   [<span data-ttu-id="f82da-113">**EnumResourceNamesEx**</span><span class="sxs-lookup"><span data-stu-id="f82da-113">**EnumResourceNamesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexa)
-   [<span data-ttu-id="f82da-114">**EnumResourceTypes**</span><span class="sxs-lookup"><span data-stu-id="f82da-114">**EnumResourceTypes**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa)
-   [<span data-ttu-id="f82da-115">**EnumResourceTypesEx**</span><span class="sxs-lookup"><span data-stu-id="f82da-115">**EnumResourceTypesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa)
-   [<span data-ttu-id="f82da-116">*EnumResTypeProc*</span><span class="sxs-lookup"><span data-stu-id="f82da-116">*EnumResTypeProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca)
-   [<span data-ttu-id="f82da-117">**Findresource**</span><span class="sxs-lookup"><span data-stu-id="f82da-117">**FindResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourcea)
-   [<span data-ttu-id="f82da-118">**FindResourceEx**</span><span class="sxs-lookup"><span data-stu-id="f82da-118">**FindResourceEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourceexa)
-   [<span data-ttu-id="f82da-119">**FreeResource**</span><span class="sxs-lookup"><span data-stu-id="f82da-119">**FreeResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freeresource)
-   [<span data-ttu-id="f82da-120">**Loadimage**</span><span class="sxs-lookup"><span data-stu-id="f82da-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
-   [<span data-ttu-id="f82da-121">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="f82da-121">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
-   [<span data-ttu-id="f82da-122">**LockResource**</span><span class="sxs-lookup"><span data-stu-id="f82da-122">**LockResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource)
-   [<span data-ttu-id="f82da-123">**SizeofResource**</span><span class="sxs-lookup"><span data-stu-id="f82da-123">**SizeofResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-sizeofresource)
-   [<span data-ttu-id="f82da-124">**UpdateResource**</span><span class="sxs-lookup"><span data-stu-id="f82da-124">**UpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-updateresourcea)

 

 
