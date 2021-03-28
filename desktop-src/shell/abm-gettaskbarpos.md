---
description: Recupera il rettangolo di delimitazione della barra delle applicazioni di Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Messaggio ABM_GETTASKBARPOS (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525429"
---
# <a name="abm_gettaskbarpos-message"></a><span data-ttu-id="a3d1b-103">\_Messaggio GETTASKBARPOS ABM</span><span class="sxs-lookup"><span data-stu-id="a3d1b-103">ABM\_GETTASKBARPOS message</span></span>

<span data-ttu-id="a3d1b-104">Recupera il rettangolo di delimitazione della barra delle applicazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="a3d1b-104">Retrieves the bounding rectangle of the Windows taskbar.</span></span>


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a><span data-ttu-id="a3d1b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3d1b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d1b-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="a3d1b-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="a3d1b-107">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) il cui membro **RC** riceve il rettangolo di delimitazione, in coordinate dello schermo, della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a3d1b-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure whose **rc** member receives the bounding rectangle, in screen coordinates, of the taskbar.</span></span> <span data-ttu-id="a3d1b-108">Quando si invia questo messaggio, è necessario specificare il **cbSize** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="a3d1b-108">You must specify the **cbSize** when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d1b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3d1b-109">Return value</span></span>

<span data-ttu-id="a3d1b-110">Restituisce **true** se l'operazione ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a3d1b-110">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d1b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3d1b-111">Remarks</span></span>

<span data-ttu-id="a3d1b-112">Si noti che questo vale solo per la barra delle applicazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="a3d1b-112">Note that this applies only to the system taskbar.</span></span> <span data-ttu-id="a3d1b-113">Possono essere presenti anche altri oggetti, in particolare le barre degli strumenti forniti con software di terze parti.</span><span class="sxs-lookup"><span data-stu-id="a3d1b-113">Other objects, particularly toolbars supplied with third-party software, also can be present.</span></span> <span data-ttu-id="a3d1b-114">Di conseguenza, parte dell'area dello schermo non coperta dalla barra delle applicazioni di Windows potrebbe non essere visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a3d1b-114">As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user.</span></span> <span data-ttu-id="a3d1b-115">Per recuperare l'area della schermata non coperta dalla barra delle applicazioni e da altre barre dell'app nell'area di lavoro disponibile per l'applicazione, usare la funzione [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="a3d1b-115">To retrieve the area of the screen not covered by both the taskbar and other app bars the working area available to your application , use the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d1b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3d1b-116">Requirements</span></span>



| <span data-ttu-id="a3d1b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3d1b-117">Requirement</span></span> | <span data-ttu-id="a3d1b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a3d1b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d1b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3d1b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3d1b-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a3d1b-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a3d1b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3d1b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3d1b-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3d1b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3d1b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3d1b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3d1b-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3d1b-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

