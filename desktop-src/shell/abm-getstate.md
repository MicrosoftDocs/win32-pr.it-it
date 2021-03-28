---
description: Recupera gli Stati di Nascondi automaticamente e sempre in primo piano della barra delle applicazioni di Windows.
title: Messaggio ABM_GETSTATE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342871"
---
# <a name="abm_getstate-message"></a><span data-ttu-id="2301e-103">Messaggio di stato di ABM \_</span><span class="sxs-lookup"><span data-stu-id="2301e-103">ABM\_GETSTATE message</span></span>

<span data-ttu-id="2301e-104">Recupera gli Stati di Nascondi automaticamente e sempre in primo piano della barra delle applicazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="2301e-104">Retrieves the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a><span data-ttu-id="2301e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2301e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2301e-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="2301e-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="2301e-107">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="2301e-107">Pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="2301e-108">Quando si invia questo messaggio, è necessario specificare il membro **cbSize** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="2301e-108">You must specify the **cbSize** member when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2301e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2301e-109">Return value</span></span>

<span data-ttu-id="2301e-110">Restituisce zero se la barra delle applicazioni non è né nello stato Nascondi automaticamente né sempre in primo piano.</span><span class="sxs-lookup"><span data-stu-id="2301e-110">Returns zero if the taskbar is neither in the autohide nor always-on-top state.</span></span> <span data-ttu-id="2301e-111">In caso contrario, il valore restituito è uno o entrambi gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2301e-111">Otherwise, the return value is one or both of the following:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2301e-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2301e-112">Return code</span></span></th>
<th><span data-ttu-id="2301e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2301e-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="2301e-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2301e-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2301e-115">La barra delle applicazioni si trova nello stato always on-top.</span><span class="sxs-lookup"><span data-stu-id="2301e-115">The taskbar is in the always-on-top state.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2301e-116">A partire da Windows 7, ABS_ALWAYSONTOP non viene più restituito perché la barra delle applicazioni è sempre in tale stato.</span><span class="sxs-lookup"><span data-stu-id="2301e-116">As of Windows 7, ABS_ALWAYSONTOP is no longer returned because the taskbar is always in that state.</span></span> <span data-ttu-id="2301e-117">Il codice precedente deve essere aggiornato per ignorare l'assenza di questo valore in non presupporre che il valore restituito significhi che la barra delle applicazioni non sia nello stato always on-top.</span><span class="sxs-lookup"><span data-stu-id="2301e-117">Older code should be updated to ignore the absence of this value in not assume that return value to mean that the taskbar is not in the always-on-top state.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2301e-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2301e-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2301e-119">La barra delle applicazioni si trova nello stato Nascondi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2301e-119">The taskbar is in the autohide state.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="2301e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2301e-120">Requirements</span></span>



| <span data-ttu-id="2301e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2301e-121">Requirement</span></span> | <span data-ttu-id="2301e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2301e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2301e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2301e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2301e-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2301e-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2301e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2301e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2301e-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2301e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2301e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2301e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2301e-128"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2301e-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




