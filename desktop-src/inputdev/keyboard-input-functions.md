---
title: Funzioni di input da tastiera
description: Funzioni di input da tastiera
ms.assetid: 731b8209-1ca8-4667-bd39-7bd0cef45380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b690a93c2813eca7c7b4487e42bfc8664bd894
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112949"
---
# <a name="keyboard-input-functions"></a><span data-ttu-id="41b2f-103">Funzioni di input da tastiera</span><span class="sxs-lookup"><span data-stu-id="41b2f-103">Keyboard Input Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="41b2f-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="41b2f-104">In This Section</span></span>

-   [<span data-ttu-id="41b2f-105">**ActivateKeyboardLayout**</span><span class="sxs-lookup"><span data-stu-id="41b2f-105">**ActivateKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout)
-   [<span data-ttu-id="41b2f-106">**BlockInput**</span><span class="sxs-lookup"><span data-stu-id="41b2f-106">**BlockInput**</span></span>](/windows/win32/api/winuser/nf-winuser-blockinput)
-   [<span data-ttu-id="41b2f-107">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="41b2f-107">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
-   [<span data-ttu-id="41b2f-108">**GetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="41b2f-108">**GetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-getactivewindow)
-   [<span data-ttu-id="41b2f-109">**GetAsyncKeyState**</span><span class="sxs-lookup"><span data-stu-id="41b2f-109">**GetAsyncKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getasynckeystate)
-   [<span data-ttu-id="41b2f-110">**GetFocus**</span><span class="sxs-lookup"><span data-stu-id="41b2f-110">**GetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-getfocus)
-   [<span data-ttu-id="41b2f-111">**GetKBCodePage**</span><span class="sxs-lookup"><span data-stu-id="41b2f-111">**GetKBCodePage**</span></span>](/windows/win32/api/winuser/nf-winuser-getkbcodepage)
-   [<span data-ttu-id="41b2f-112">**GetKeyboardLayout**</span><span class="sxs-lookup"><span data-stu-id="41b2f-112">**GetKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)
-   [<span data-ttu-id="41b2f-113">**GetKeyboardLayoutList**</span><span class="sxs-lookup"><span data-stu-id="41b2f-113">**GetKeyboardLayoutList**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist)
-   [<span data-ttu-id="41b2f-114">**GetKeyboardLayoutName**</span><span class="sxs-lookup"><span data-stu-id="41b2f-114">**GetKeyboardLayoutName**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea)
-   [<span data-ttu-id="41b2f-115">**GetKeyboardState**</span><span class="sxs-lookup"><span data-stu-id="41b2f-115">**GetKeyboardState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardstate)
-   [<span data-ttu-id="41b2f-116">**GetKeyboardType**</span><span class="sxs-lookup"><span data-stu-id="41b2f-116">**GetKeyboardType**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardtype)
-   [<span data-ttu-id="41b2f-117">**GetKeyNameText**</span><span class="sxs-lookup"><span data-stu-id="41b2f-117">**GetKeyNameText**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeynametexta)
-   [<span data-ttu-id="41b2f-118">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="41b2f-118">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
-   [<span data-ttu-id="41b2f-119">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="41b2f-119">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
-   [<span data-ttu-id="41b2f-120">**IsWindowEnabled**</span><span class="sxs-lookup"><span data-stu-id="41b2f-120">**IsWindowEnabled**</span></span>](/windows/win32/api/winuser/nf-winuser-iswindowenabled)
-   [<span data-ttu-id="41b2f-121">**evento \_ keybd**</span><span class="sxs-lookup"><span data-stu-id="41b2f-121">**keybd\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-keybd_event)
-   [<span data-ttu-id="41b2f-122">**LoadKeyboardLayout**</span><span class="sxs-lookup"><span data-stu-id="41b2f-122">**LoadKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta)
-   [<span data-ttu-id="41b2f-123">**MapVirtualKey**</span><span class="sxs-lookup"><span data-stu-id="41b2f-123">**MapVirtualKey**</span></span>](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya)
-   [<span data-ttu-id="41b2f-124">**MapVirtualKeyEx**</span><span class="sxs-lookup"><span data-stu-id="41b2f-124">**MapVirtualKeyEx**</span></span>](/windows/win32/api/winuser/nf-winuser-mapvirtualkeyexa)
-   [<span data-ttu-id="41b2f-125">**OemKeyScan**</span><span class="sxs-lookup"><span data-stu-id="41b2f-125">**OemKeyScan**</span></span>](/windows/win32/api/winuser/nf-winuser-oemkeyscan)
-   [<span data-ttu-id="41b2f-126">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="41b2f-126">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
-   [<span data-ttu-id="41b2f-127">**SendInput**</span><span class="sxs-lookup"><span data-stu-id="41b2f-127">**SendInput**</span></span>](/windows/win32/api/winuser/nf-winuser-sendinput)
-   [<span data-ttu-id="41b2f-128">**SetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="41b2f-128">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
-   [<span data-ttu-id="41b2f-129">**Setfocus**</span><span class="sxs-lookup"><span data-stu-id="41b2f-129">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
-   [<span data-ttu-id="41b2f-130">**SetKeyboardState**</span><span class="sxs-lookup"><span data-stu-id="41b2f-130">**SetKeyboardState**</span></span>](/windows/win32/api/winuser/nf-winuser-setkeyboardstate)
-   [<span data-ttu-id="41b2f-131">**ToAscii**</span><span class="sxs-lookup"><span data-stu-id="41b2f-131">**ToAscii**</span></span>](/windows/win32/api/winuser/nf-winuser-toascii)
-   [<span data-ttu-id="41b2f-132">**ToAsciiEx**</span><span class="sxs-lookup"><span data-stu-id="41b2f-132">**ToAsciiEx**</span></span>](/windows/win32/api/winuser/nf-winuser-toasciiex)
-   [<span data-ttu-id="41b2f-133">**ToUnicode**</span><span class="sxs-lookup"><span data-stu-id="41b2f-133">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)
-   [<span data-ttu-id="41b2f-134">**ToUnicodeEx**</span><span class="sxs-lookup"><span data-stu-id="41b2f-134">**ToUnicodeEx**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicodeex)
-   [<span data-ttu-id="41b2f-135">**UnloadKeyboardLayout**</span><span class="sxs-lookup"><span data-stu-id="41b2f-135">**UnloadKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout)
-   [<span data-ttu-id="41b2f-136">**UnregisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="41b2f-136">**UnregisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-unregisterhotkey)
-   [<span data-ttu-id="41b2f-137">**VkKeyScan**</span><span class="sxs-lookup"><span data-stu-id="41b2f-137">**VkKeyScan**</span></span>](/windows/win32/api/winuser/nf-winuser-vkkeyscana)
-   [<span data-ttu-id="41b2f-138">**VkKeyScanEx**</span><span class="sxs-lookup"><span data-stu-id="41b2f-138">**VkKeyScanEx**</span></span>](/windows/win32/api/winuser/nf-winuser-vkkeyscanexa)

 

 
