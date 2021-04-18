---
description: Recupera il tipo di carattere con cui il controllo sta attualmente disegnando il testo.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: Messaggio WM_GETFONT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314864"
---
# <a name="wm_getfont-message"></a><span data-ttu-id="c8bb7-103">\_Messaggio WM GETfont</span><span class="sxs-lookup"><span data-stu-id="c8bb7-103">WM\_GETFONT message</span></span>

<span data-ttu-id="c8bb7-104">Recupera il tipo di carattere con cui il controllo sta attualmente disegnando il testo.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-104">Retrieves the font with which the control is currently drawing its text.</span></span>


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a><span data-ttu-id="c8bb7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8bb7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8bb7-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8bb7-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8bb7-107">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8bb7-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8bb7-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8bb7-109">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8bb7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8bb7-110">Return value</span></span>

<span data-ttu-id="c8bb7-111">Tipo: **Hfont**</span><span class="sxs-lookup"><span data-stu-id="c8bb7-111">Type: **HFONT**</span></span>

<span data-ttu-id="c8bb7-112">Il valore restituito è un handle per il tipo di carattere utilizzato dal controllo o **null** se il controllo utilizza il tipo di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="c8bb7-112">The return value is a handle to the font used by the control, or **NULL** if the control is using the system font.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8bb7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8bb7-113">Requirements</span></span>



| <span data-ttu-id="c8bb7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8bb7-114">Requirement</span></span> | <span data-ttu-id="c8bb7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c8bb7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bb7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8bb7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8bb7-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8bb7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c8bb7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8bb7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8bb7-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8bb7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8bb7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8bb7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8bb7-121"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8bb7-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8bb7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8bb7-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8bb7-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c8bb7-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8bb7-124">**\_tipo di carattere WM**</span><span class="sxs-lookup"><span data-stu-id="c8bb7-124">**WM\_SETFONT**</span></span>](wm-setfont.md)
</dt> <dt>

<span data-ttu-id="c8bb7-125">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c8bb7-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8bb7-126">Windows</span><span class="sxs-lookup"><span data-stu-id="c8bb7-126">Windows</span></span>](windows.md)
</dt> </dl>

 

 




