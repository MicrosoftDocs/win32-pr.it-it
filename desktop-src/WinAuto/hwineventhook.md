---
title: HWINEVENTHOOK (windef. h)
description: Utilizzato per dichiarare una funzione hook dell'evento Window.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301683"
---
# <a name="hwineventhook"></a><span data-ttu-id="b2587-104">HWINEVENTHOOK</span><span class="sxs-lookup"><span data-stu-id="b2587-104">HWINEVENTHOOK</span></span>

<span data-ttu-id="b2587-105">Utilizzato per dichiarare una funzione hook dell'evento Window.</span><span class="sxs-lookup"><span data-stu-id="b2587-105">Used to declare a window event hook function.</span></span>


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a><span data-ttu-id="b2587-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2587-106">Remarks</span></span>

<span data-ttu-id="b2587-107">Questo tipo di dati viene utilizzato con la funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e le funzioni [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .</span><span class="sxs-lookup"><span data-stu-id="b2587-107">This data type is used with the [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function and the [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2587-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2587-108">Requirements</span></span>



| <span data-ttu-id="b2587-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2587-109">Requirement</span></span> | <span data-ttu-id="b2587-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b2587-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2587-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2587-111">Minimum supported client</span></span><br/> | <span data-ttu-id="b2587-112">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b2587-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="b2587-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2587-113">Minimum supported server</span></span><br/> | <span data-ttu-id="b2587-114">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2587-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                          |
| <span data-ttu-id="b2587-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b2587-115">Redistributable</span></span><br/>          | <span data-ttu-id="b2587-116">Active Accessibility 1,3 RDK in Windows NT 4,0 con SP6 e versioni successive e Windows 95</span><span class="sxs-lookup"><span data-stu-id="b2587-116">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>                                   |
| <span data-ttu-id="b2587-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2587-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2587-118"><dt>Windef. h (WINVER >= 0x0500) (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2587-118"><dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt></span></span> </dl> |



 

 





