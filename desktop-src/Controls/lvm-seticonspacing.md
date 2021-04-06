---
title: Messaggio LVM_SETICONSPACING (COMmctrl. h)
description: Imposta la spaziatura tra le icone nei controlli visualizzazione elenco con lo \_ stile dell'icona LVS. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetIconSpacing di ListView.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- Controlli di Windows Message LVM_SETICONSPACING
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873321"
---
# <a name="lvm_seticonspacing-message"></a><span data-ttu-id="0b896-105">\_Messaggio SETICONSPACING LVM</span><span class="sxs-lookup"><span data-stu-id="0b896-105">LVM\_SETICONSPACING message</span></span>

<span data-ttu-id="0b896-106">Imposta la spaziatura tra le icone nei controlli visualizzazione elenco con lo stile dell' [**\_ icona LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0b896-106">Sets the spacing between icons in list-view controls that have the [**LVS\_ICON**](list-view-window-styles.md) style.</span></span> <span data-ttu-id="0b896-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetIconSpacing di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .</span><span class="sxs-lookup"><span data-stu-id="0b896-107">You can send this message explicitly or by using the [**ListView\_SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b896-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b896-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b896-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b896-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b896-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0b896-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0b896-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b896-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b896-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la distanza in pixel da impostare tra le icone sull'asse x.</span><span class="sxs-lookup"><span data-stu-id="0b896-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the distance, in pixels, to set between icons on the x-axis.</span></span> <span data-ttu-id="0b896-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la distanza in pixel da impostare tra le icone sull'asse y.</span><span class="sxs-lookup"><span data-stu-id="0b896-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the distance, in pixels, to set between icons on the y-axis.</span></span> <span data-ttu-id="0b896-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0b896-114">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b896-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b896-115">Return value</span></span>

<span data-ttu-id="0b896-116">Restituisce un valore **DWORD** che contiene la distanza precedente dell'asse x nella parola bassa e la distanza dell'asse y precedente nella parola alta.</span><span class="sxs-lookup"><span data-stu-id="0b896-116">Returns a **DWORD** value that contains the previous x-axis distance in the low word, and the previous y-axis distance in the high word.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b896-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b896-117">Remarks</span></span>

<span data-ttu-id="0b896-118">I valori per *lParam* sono relativi all'angolo superiore sinistro di una bitmap icona.</span><span class="sxs-lookup"><span data-stu-id="0b896-118">Values for *lParam* are relative to the upper-left corner of an icon bitmap.</span></span> <span data-ttu-id="0b896-119">Pertanto, per impostare la spaziatura tra le icone che non si sovrappongono, i valori *lParam* devono includere le dimensioni dell'icona, più la quantità di spazio vuoto che si desidera tra le icone.</span><span class="sxs-lookup"><span data-stu-id="0b896-119">Therefore, to set spacing between icons that do not overlap, the *lParam* values must include the size of the icon, plus the amount of empty space desired between icons.</span></span> <span data-ttu-id="0b896-120">I valori che non includono la larghezza dell'icona provocheranno sovrapposizioni.</span><span class="sxs-lookup"><span data-stu-id="0b896-120">Values that do not include the width of the icon will result in overlaps.</span></span>

<span data-ttu-id="0b896-121">Quando si definisce la spaziatura delle icone, è necessario che i valori *lParam* siano impostati su 4 o più grandi.</span><span class="sxs-lookup"><span data-stu-id="0b896-121">When defining the icon spacing, the *lParam* values must set to 4 or larger.</span></span> <span data-ttu-id="0b896-122">I valori più piccoli non restituiranno il layout desiderato.</span><span class="sxs-lookup"><span data-stu-id="0b896-122">Smaller values will not yield the desired layout.</span></span> <span data-ttu-id="0b896-123">Per reimpostare le icone sulla spaziatura predefinita, impostare i valori *lParam* su-1.</span><span class="sxs-lookup"><span data-stu-id="0b896-123">To reset the icons to the default spacing, set the *lParam* values to -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b896-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b896-124">Requirements</span></span>



| <span data-ttu-id="0b896-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b896-125">Requirement</span></span> | <span data-ttu-id="0b896-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0b896-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b896-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b896-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0b896-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b896-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b896-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b896-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0b896-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b896-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b896-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b896-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b896-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b896-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

