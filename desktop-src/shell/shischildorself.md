---
UID: ''
title: SHIsChildOrSelf (funzione)
description: Consente di confrontare se una finestra è uguale a, figlio di o discendente di una seconda finestra.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "104993304"
---
# <a name="shischildorself-function"></a><span data-ttu-id="75305-103">SHIsChildOrSelf (funzione)</span><span class="sxs-lookup"><span data-stu-id="75305-103">SHIsChildOrSelf function</span></span>

## <a name="description"></a><span data-ttu-id="75305-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75305-104">Description</span></span>

<span data-ttu-id="75305-105">\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="75305-105">\[This function is available through Windows XP and Windows Server 2003.</span></span>
<span data-ttu-id="75305-106">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75305-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="75305-107">Consente di confrontare se una finestra è uguale a, figlio di o discendente di una seconda finestra.</span><span class="sxs-lookup"><span data-stu-id="75305-107">Compares whether a window is equal to, a child of, or a descendant of, a second window.</span></span>

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a><span data-ttu-id="75305-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="75305-108">Parameters</span></span>

### <a name="hwndparent-in"></a><span data-ttu-id="75305-109">hwndParent [in]</span><span class="sxs-lookup"><span data-stu-id="75305-109">hwndParent [in]</span></span>

<span data-ttu-id="75305-110">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="75305-110">Type: **HWND**</span></span>

<span data-ttu-id="75305-111">Handle per la prima finestra.</span><span class="sxs-lookup"><span data-stu-id="75305-111">A handle to the first window.</span></span>

### <a name="hwnd-in"></a><span data-ttu-id="75305-112">HWND [in]</span><span class="sxs-lookup"><span data-stu-id="75305-112">hwnd [in]</span></span>

<span data-ttu-id="75305-113">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="75305-113">Type: **HWND**</span></span>

<span data-ttu-id="75305-114">Handle per una finestra da testare rispetto a *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="75305-114">A handle to a window to be tested against *hwndParent*.</span></span>

## <a name="returns"></a><span data-ttu-id="75305-115">Restituisce</span><span class="sxs-lookup"><span data-stu-id="75305-115">Returns</span></span>

<span data-ttu-id="75305-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="75305-116">Type: **HRESULT**</span></span>

<span data-ttu-id="75305-117">Restituisce **S_OK** se la finestra specificata da *HWND* è uguale a, un elemento figlio di o un discendente della finestra specificata da *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="75305-117">Returns **S_OK** if the window specified by *hwnd* is equal to, a child of, or a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="75305-118">Restituisce **S_FALSE** se la finestra specificata da HWND non è uguale a, non è un elemento figlio di e non è un discendente della finestra specificata da *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="75305-118">Returns **S_FALSE** if the window specified by hwnd is not equal to, not a child of, and not a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="75305-119">Il valore restituito non è definito se uno degli handle della finestra non è valido.</span><span class="sxs-lookup"><span data-stu-id="75305-119">The return value is undefined if either window handle is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="75305-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="75305-120">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="75305-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75305-121">See also</span></span>

[<span data-ttu-id="75305-122">IsChild</span><span class="sxs-lookup"><span data-stu-id="75305-122">IsChild</span></span>](/windows/desktop/api/winuser/nf-winuser-ischild)
