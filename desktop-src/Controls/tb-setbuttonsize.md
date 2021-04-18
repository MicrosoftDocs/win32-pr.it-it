---
title: Messaggio TB_SETBUTTONSIZE (COMmctrl. h)
description: Imposta la dimensione dei pulsanti in una barra degli strumenti.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- Controlli di Windows Message TB_SETBUTTONSIZE
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301669"
---
# <a name="tb_setbuttonsize-message"></a><span data-ttu-id="844a9-104">TB \_ SETBUTTONSIZE messaggio</span><span class="sxs-lookup"><span data-stu-id="844a9-104">TB\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="844a9-105">Imposta la dimensione dei pulsanti in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="844a9-105">Sets the size of buttons on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="844a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="844a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="844a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="844a9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="844a9-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="844a9-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="844a9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="844a9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="844a9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la larghezza, in pixel, dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="844a9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the buttons.</span></span> <span data-ttu-id="844a9-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'altezza, in pixel, dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="844a9-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="844a9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="844a9-112">Return value</span></span>

<span data-ttu-id="844a9-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="844a9-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="844a9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="844a9-114">Remarks</span></span>

<span data-ttu-id="844a9-115">**TB \_ SETBUTTONSIZE** deve essere in genere chiamato dopo l'aggiunta di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="844a9-115">**TB\_SETBUTTONSIZE** should generally be called after adding buttons.</span></span>

<span data-ttu-id="844a9-116">Usare [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) per impostare le larghezze massime e minime consentite per i pulsanti prima di aggiungerli.</span><span class="sxs-lookup"><span data-stu-id="844a9-116">Use [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="844a9-117">Usare **TB \_ SETBUTTONSIZE** per impostare le dimensioni effettive dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="844a9-117">Use **TB\_SETBUTTONSIZE** to set the actual size of buttons.</span></span>

## <a name="examples"></a><span data-ttu-id="844a9-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="844a9-118">Examples</span></span>

<span data-ttu-id="844a9-119">Il codice di esempio seguente imposta la larghezza dei pulsanti su 80 pixel e l'altezza su 30 pixel.</span><span class="sxs-lookup"><span data-stu-id="844a9-119">The following example code sets the width of buttons to 80 pixels and the height to 30 pixels.</span></span>


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a><span data-ttu-id="844a9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="844a9-120">Requirements</span></span>



| <span data-ttu-id="844a9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="844a9-121">Requirement</span></span> | <span data-ttu-id="844a9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="844a9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="844a9-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="844a9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="844a9-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="844a9-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="844a9-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="844a9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="844a9-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="844a9-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="844a9-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="844a9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="844a9-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="844a9-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

