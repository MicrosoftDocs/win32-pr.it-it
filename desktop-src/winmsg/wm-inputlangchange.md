---
description: Inviato alla finestra interessata in primo piano dopo la modifica della lingua di input di un'applicazione. È necessario apportare impostazioni specifiche dell'applicazione e passare il messaggio alla funzione DefWindowProc, che passa il messaggio a tutte le finestre figlio di primo livello.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: WM_INPUTLANGCHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332406"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="7d518-104">Messaggio WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="7d518-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="7d518-105">Inviato alla finestra interessata in primo piano dopo la modifica della lingua di input di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d518-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="7d518-106">È necessario apportare impostazioni specifiche dell'applicazione e passare il messaggio alla funzione [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) che passa il messaggio a tutte le finestre figlio di primo livello.</span><span class="sxs-lookup"><span data-stu-id="7d518-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="7d518-107">Queste finestre figlio possono passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per fare in modo che passi il messaggio alle finestre figlio e così via.</span><span class="sxs-lookup"><span data-stu-id="7d518-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="7d518-108">Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7d518-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a><span data-ttu-id="7d518-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d518-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d518-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d518-110">*wParam*</span></span>

</dt> <dd>
  
<span data-ttu-id="7d518-111">Tipo: **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7d518-111">Type: **WPARAM**</span></span>

<span data-ttu-id="7d518-112">Tabella [codici delle](../Intl/code-pages.md) nuove impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="7d518-112">The [code page](../Intl/code-pages.md) of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="7d518-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d518-113">*lParam*</span></span>

</dt> <dd>
 
<span data-ttu-id="7d518-114">Tipo: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="7d518-114">Type: **LPARAM**</span></span>

<span data-ttu-id="7d518-115">Identificatore delle impostazioni locali di input **HKL.**</span><span class="sxs-lookup"><span data-stu-id="7d518-115">The **HKL** input locale identifier.</span></span> <span data-ttu-id="7d518-116">Per altre informazioni, vedere [Lingue, impostazioni locali e layout di tastiera.](../inputdev/about-keyboard-input.md)</span><span class="sxs-lookup"><span data-stu-id="7d518-116">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d518-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d518-117">Return value</span></span>

<span data-ttu-id="7d518-118">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7d518-118">Type: **LRESULT**</span></span>

<span data-ttu-id="7d518-119">Un'applicazione deve restituire un valore diverso da zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="7d518-119">An application should return nonzero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d518-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d518-120">Remarks</span></span>

<span data-ttu-id="7d518-121">È possibile recuperare il nome [delle impostazioni locali della](../Intl/locale-names.md) tastiera tramite la funzione [LCIDToLocaleName.](/windows/win32/api/winnls/nf-winnls-lcidtolocalename)</span><span class="sxs-lookup"><span data-stu-id="7d518-121">You can retrieve keyboard [locale name](../Intl/locale-names.md) via [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) function.</span></span> <span data-ttu-id="7d518-122">Con il nome delle impostazioni locali è possibile usare [le funzioni delle impostazioni locali moderne:](/windows/win32/intl/calling-the--locale-name--functions)</span><span class="sxs-lookup"><span data-stu-id="7d518-122">With locale name you can use [modern locale functions](/windows/win32/intl/calling-the--locale-name--functions):</span></span>

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a><span data-ttu-id="7d518-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d518-123">Requirements</span></span>

| <span data-ttu-id="7d518-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d518-124">Requirement</span></span> | <span data-ttu-id="7d518-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7d518-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d518-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d518-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7d518-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7d518-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7d518-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d518-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7d518-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7d518-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d518-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d518-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d518-131"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d518-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="7d518-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d518-132">See also</span></span>

<span data-ttu-id="7d518-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7d518-133">**Reference**</span></span>

- [<span data-ttu-id="7d518-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7d518-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [<span data-ttu-id="7d518-135">**WM \_ INPUTLANGCHANGEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="7d518-135">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)

<span data-ttu-id="7d518-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7d518-136">**Conceptual**</span></span>

- [<span data-ttu-id="7d518-137">Windows</span><span class="sxs-lookup"><span data-stu-id="7d518-137">Windows</span></span>](windows.md) 
