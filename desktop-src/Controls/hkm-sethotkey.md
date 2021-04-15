---
title: Messaggio HKM_SETHOTKEY (COMmctrl. h)
description: Imposta la combinazione di tasti di scelta rapida per un controllo tasto di scelta.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- Controlli di Windows Message HKM_SETHOTKEY
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517650"
---
# <a name="hkm_sethotkey-message"></a><span data-ttu-id="b17b2-104">\_Messaggio SEHOTKEY HKM</span><span class="sxs-lookup"><span data-stu-id="b17b2-104">HKM\_SETHOTKEY message</span></span>

<span data-ttu-id="b17b2-105">Imposta la combinazione di tasti di scelta rapida per un controllo tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="b17b2-105">Sets the hot key combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b17b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b17b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b17b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b17b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b17b2-108">Il [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) del [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è il codice della chiave virtuale del tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="b17b2-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="b17b2-109">[**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) di **LOWORD** è il modificatore di chiave che indica le chiavi che definiscono una combinazione di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="b17b2-109">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that indicates the keys that define a hot key combination.</span></span> <span data-ttu-id="b17b2-110">Per un elenco di valori dei flag di modifica, vedere la descrizione del messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="b17b2-110">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="b17b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b17b2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b17b2-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b17b2-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b17b2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b17b2-113">Return value</span></span>

<span data-ttu-id="b17b2-114">Restituisce sempre zero.</span><span class="sxs-lookup"><span data-stu-id="b17b2-114">Always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b17b2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b17b2-115">Requirements</span></span>



| <span data-ttu-id="b17b2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17b2-116">Requirement</span></span> | <span data-ttu-id="b17b2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b17b2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b17b2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b17b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b17b2-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b17b2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b17b2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b17b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b17b2-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b17b2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b17b2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b17b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b17b2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b17b2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

