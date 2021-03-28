---
description: Imposta gli stati Nascondi automaticamente e sempre in primo piano della barra delle applicazioni di Windows.
title: Messaggio ABM_SETSTATE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977442"
---
# <a name="abm_setstate-message"></a><span data-ttu-id="623cc-103">\_Messaggio di SESTATO ABM</span><span class="sxs-lookup"><span data-stu-id="623cc-103">ABM\_SETSTATE message</span></span>

<span data-ttu-id="623cc-104">Imposta gli stati Nascondi automaticamente e sempre in primo piano della barra delle applicazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="623cc-104">Sets the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="623cc-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="623cc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623cc-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="623cc-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="623cc-107">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="623cc-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="623cc-108">È necessario specificare i membri **cbSize** e **HWND** quando si invia questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="623cc-108">You must specify the **cbSize** and **hWnd** members when sending this message.</span></span> <span data-ttu-id="623cc-109">I dati per lo stato desiderato vengono inviati nel membro **lParam** utilizzando uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="623cc-109">Data for the desired state is sent in the **lParam** member using one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="623cc-110"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="623cc-110"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="623cc-111">Nascondi automaticamente e sempre in primo piano</span><span class="sxs-lookup"><span data-stu-id="623cc-111">Autohide and always-on-top both off</span></span>

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span data-ttu-id="623cc-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**\_ALWAYSONTOP ABS**</span><span class="sxs-lookup"><span data-stu-id="623cc-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="623cc-113">Always-on-top on, Nascondi automaticamente</span><span class="sxs-lookup"><span data-stu-id="623cc-113">Always-on-top on, autohide off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span data-ttu-id="623cc-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**\_Nascondi automaticamente ABS**</span><span class="sxs-lookup"><span data-stu-id="623cc-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS\_AUTOHIDE**</span></span>


</dt> <dd>

<span data-ttu-id="623cc-115">Nascondi automaticamente on, always on-top off</span><span class="sxs-lookup"><span data-stu-id="623cc-115">Autohide on, always-on-top off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span data-ttu-id="623cc-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ Nascondi automaticamente \| ABS \_ ALWAYSONTOP**</span><span class="sxs-lookup"><span data-stu-id="623cc-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS\_AUTOHIDE \| ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="623cc-117">Nascondi automaticamente e always on-top entrambi in</span><span class="sxs-lookup"><span data-stu-id="623cc-117">Autohide and always-on-top both on</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623cc-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="623cc-118">Return value</span></span>

<span data-ttu-id="623cc-119">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="623cc-119">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="623cc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="623cc-120">Requirements</span></span>



| <span data-ttu-id="623cc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="623cc-121">Requirement</span></span> | <span data-ttu-id="623cc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="623cc-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="623cc-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="623cc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="623cc-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="623cc-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="623cc-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="623cc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="623cc-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="623cc-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="623cc-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="623cc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="623cc-128"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="623cc-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




